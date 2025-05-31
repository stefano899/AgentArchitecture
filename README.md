# Asta  
> DALI Multi-Agent Systems Framework  

This multi-agent system simulates an auction where the **auctioneer** acts as the central agent responsible for managing the auction. The auctioneer handles the item provided by an agent called the **owner** and processes bids from **buyers** (bidders).  

The owner provides the auctioneer with an unlimited number of the same item and sets a selling price. Anyone offering a price equal to or higher than the agreed price wins the item.  

To decide whether to start the auction, the auctioneer rolls a die with values from 1 to 3. If the die returns a 1, the auction begins.  
If, after a certain amount of time, the auctioneer has not started the auction, the bidders will send a reminder, forcing the auctioneer to open it.  

The system will be developed for **Windows**.  
The **FIPA primitive** used in this project, using the `"messageA"` call, is:  
`send_message(External_event, sender)`.  

[Repository Link](https://github.com/stefano899/AgentArchitecture)  

## Agents  

### Auctioneer  
- The central agent of the system.  
- Manages bids received from buyers.  
- Sells the item.  

### Owner  
- Owns the item to be sold.  
- Has an unlimited supply of that item.  
- Makes the item available for sale.  

### Bidders  
- Submit bids for the item.  
- If a bidder wins an item, they can no longer bid in the auction.  

## Sequence Diagram  

![Sequence Diagram](sequenceAsta.png)  

## Event/Action Table – Auctioneer  

| Event/Action        | Description |
|---------------------|-------------|
| `prontoI`          | The auctioneer greets everyone and declares readiness, if not done already. |
| `richiesta_oggettoI` | If the auctioneer does not have the item for auction, they request it from the owner. |
| `oggettoE`         | Receives the item from the owner. |
| `decido_se_aprireI` | Rolls a die with numbers from 1 to 3; if it lands on 1, the auction is opened. |
| `sollecitoE`       | If the auctioneer does not open the auction, bidders send a reminder. |
| `apro_offerteI`    | The auctioneer starts the auction. |
| `invia_messaggioA` | The auctioneer informs bidders that the auction is open. |
| `propostaE`       | The auctioneer receives bids from bidders and stores them in a list. |
| `monitoro_offerteI` | The auctioneer checks that all bids have been received. |
| `considero_offerteA` | The auctioneer declares the auction closed and begins evaluating bids. |
| `verifica_offerte(L)` | The auctioneer checks if each bid meets or exceeds the owner's asking price—accepting successful bids and rejecting others. |

## Event/Action Table – Owner  

| Event/Action        | Description |
|---------------------|-------------|
| `prontoI`          | The owner greets everyone and declares readiness, if not done already. |
| `richiestaE`       | Receives a request from the auctioneer to provide an item for auction. |
| `richiesta_invioE` | Receives a request from a winning bidder to send the item. The owner flips a coin—if heads, the item is sent; otherwise, it is not. |

## Event/Action Table – Bidder  

| Event/Action        | Description |
|---------------------|-------------|
| `prontoI`          | The bidder greets everyone and declares readiness, if not done already. |
| `attendo_banditoreI` | The bidder waits for the auctioneer to open the auction. |
| `no_aperturaI`     | If the auctioneer delays opening the auction, bidders send a reminder. |
| `aperturaE`        | The bidder receives a message from the auctioneer stating that the auction is open. |
| `faccio_offertaI`  | The bidder submits an offer for the item. |
| `contatto_banditoreI` | The bidder sends the bid to the auctioneer. |
| `accettataE`       | The bidder's offer is accepted, and they request item shipment from the owner. |

## Execution Example  
![Execution](Esecuzione.png)  

## Installation  
To run the program, you need **Windows** and the latest version of **SICStus Prolog**, specifically **SICStus Prolog VC16 4.9.0**.  

[Download Link](https://sicstus.sics.se/download4.html)  
In the `"startmas.bat"` file, replace the `"sictus_home"` section with your SICStus Prolog VC16 4.9.0 installation path.  

Inside the `"Asta Particolare"` folder, create `"work"` and `"log"` directories, then launch `"startmas.bat"` to start the program.  

---
