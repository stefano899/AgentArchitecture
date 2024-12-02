# Asta
> DALI Multi Agent Systems Framework

Questo sistema multi agente propone di simulare un'asta in cui il banditore risulta essere l'agente centrale che si occupa di gestire l'asta, prendendo in carico l'oggetto di un agente chiamato "proprietario" e di prendere in carico le offerte dei compratori (bidders).
Il proprietario mette a disposizione un numero illimitato dello stesso oggetto e sancisce un prezzo di vendita: chiunque offra un prezzo superiore o uguale a quello concordato dal proprietario, si aggiudica l'oggetto.
Il sistema sarà sviluppato su windows.


## Agenti

* Banditore:
  - E' l'agente centrale del programma.
  - Gestisce le offerte ricevute dai compratori.
  - Mette in vendita l'oggetto. 

* Proprietario:
  - E' il proprietario dell'oggetto che vuole vendere;
  - Ha a disposizione risorse risorse illimitate di quell'oggetto;
  - E' colui che rende disponibile la vendita dell'oggetto;
  

* Bidders:
  - Sono coloro che fanno delle offerte al banditore;
  - Se il bidder ha acquistato un oggetto, non può più fare delle offerte.

## Sequence Diagram

You can download DALI and test it by running an example DALI MAS:
```sh
git clone https://github.com/AAAI-DISIM-UnivAQ/DALI.git
cd DALI/Examples/advanced
bash startmas.sh
```
&nbsp;&nbsp;&nbsp;&nbsp; You will see different windows opening:
* &nbsp;&nbsp;&nbsp;&nbsp; Prolog LINDA server (active_server_wi.pl)
* &nbsp;&nbsp;&nbsp;&nbsp; Prolog FIPA client (active_user_wi.pl) 
* &nbsp;&nbsp;&nbsp;&nbsp; 1 instance of DALI metaintepreter for each agent (active_dali_wi.pl)

**Windows:**

You can download DALI from https://github.com/AAAI-DISIM-UnivAQ/DALI.git.
*  Unzip the repository, go to the folder "DALI/Examples/basic", and test if DALI works by duble clicking "startmas.bat" file (this will launch an example DALI MAS). \
\
&nbsp;&nbsp;&nbsp;&nbsp; You will see different windows opening:
* &nbsp;&nbsp;&nbsp;&nbsp; Prolog LINDA server (active_server_wi.pl)
* &nbsp;&nbsp;&nbsp;&nbsp; Prolog FIPA client (active_user_wi.pl) 
* &nbsp;&nbsp;&nbsp;&nbsp; 1 instance of DALI metaintepreter for each agent (active_dali_wi.pl)


## Usage example

You can find some examples into the Example folder, where examples are divided into 3 subfolders:
* __basic__: aimed at basic Windows-based setup, no agent types, every agent living in a separated sicstus window.
* __advanced__: more complex, aimed at Unix-like based environment, with agent type, instances, each agent living in a separated xterm console.
* __more__: MAS examples derived from our students projects.


## Development setup
To create a new DALI MAS, you can use an example as a boilerplate:
1.  Create a folder to contain your project, for example let's call it "projectFolder"
2.  Copy the folder "DALI/src" into "projectFolder"
3.  In "projectFolder", create a folder that will contain your DALI app, for example let's call it "DALIappFolder"
4.  Copy the content of "DALI/Examples/advanced" folder in "projectFolder/DALIappFolder"
5.  Rewrite the files contained in "projectFolder/DALIappFolder/mas/instances" and in "projectFolder/DALIappFolder/mas/instances"
    in a proper way (see DALI documentation), in order to create your DALI MAS.
6.  Open the "startmas" file and change the following variables according to your paths:
* **sicstus_home:** The SICStus prolog path
* **main_home:**  # The "projectFolder" path, in relation to the "startmas" file position (in this example it is "..")
* **dali_home:**  # The "projectFolder/src" folder path, in relation to the "startmas" file position (in this example it is "../src")
* **conf_dir:**  # The "projectFolder/conf" folder path, in relation to the "startmas" file position (in this example it is "conf")


## Release History

Check [release history](http://github.com/AAAI-DISIM-UnivAQ/DALI/releases) page.


## Contacts

Giovanni De Gasperis – [@giodegas](http://x.com/giodegas) – giovanni.degasperis-at-univaq-it

Distributed under the Apache License 2.0. See ``LICENSE`` for more information.

[http://github.com/AAAI-DISIM-UnivAQ](http://github.com/AAAI-DISIM-UnivAQ)


## Contributing
To complete
1. Fork it (<https://github.com/AAAI-DISIM-UnivAQ/DALI/fork>)
2. Create your feature branch (`git checkout -b feature/fooBar`)
3. Commit your changes (`git commit -am 'Add some fooBar'`)
4. Push to the branch (`git push origin feature/fooBar`)
5. Create a new Pull Request

## Examples of Applications:

* in Robotics: coordination among store delivery robots: [Video](https://youtu.be/1dfWthhUovk) from S. Valentini:
   [![Delivery robots cordination](https://img.youtube.com/vi/1dfWthhUovk/0.jpg)](https://www.youtube.com/watch?v=1dfWthhUovk)

## References
* DALI 1.0 original URL: http://www.di.univaq.it/stefcost/Sito-Web-DALI/WEB-DALI (no more active)
* COSTANTINI, Stefania. [*The DALI Agent-Oriented Logic Programming Language: Summary and References 2015.*](http://people.disim.univaq.it/stefcost/pubbls/Dali_References.pdf)
* COSTANTINI S, TOCCHIO A. [*A logic programming language for multi-agent systems.*](docs/DALI_Language_description.pdf) Logics in Artificial Intelligence, Springer Berlin Heidelberg, 2002, pp:1-13.
* COSTANTINI S, TOCCHIO A. *The DALI logic programming agent-oriented language.* In Logics in Artificial Intelligence Springer Berlin Heidelberg, 2004, pp:685-688.
* COSTANTINI S, TOCCHIO A. *DALI: An Architecture for Intelligent Logical Agents.* In: AAAI Spring Symposium: Emotion, Personality, and Social Behavior. 2008. pp:13-18.
* BEVAR V, COSTANTINI S, TOCCHIO A, DE GASPERIS G. *A multi-agent system for industrial fault detection and repair.* In: Advances on Practical Applications of Agents and Multi-Agent Systems. Springer Berlin Heidelberg, 2012. pp:47-55.
* DE GASPERIS, G, BEVAR V, COSTANTINI S, TOCCHIO A, PAOLUCCI A. *Demonstrator of a multi-agent system for industrial fault detection and repair.* In: Advances on Practical Applications of Agents and Multi-Agent Systems. Springer Berlin Heidelberg, 2012. pp:237-240.
* DE GASPERIS Giovanni. *DETF 1st Release (Version 14.08a).* Zenodo. [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.1044488.svg)](https://doi.org/10.5281/zenodo.1044488), 2014, August 6. 
* COSTANTINI, Stefania; DE GASPERIS, Giovanni; NAZZICONE, Giulio. *DALI for cognitive robotics: principles and prototype implementation.* In: International Symposium on Practical Aspects of Declarative Languages. Springer, Cham, 2017. p. 152-162.
* COSTANTINI, Stefania, DE GASPERIS, Giovanni, PITONI Valentina, SALUTARI Agnese. [*DALI: A multi agent system framework for the web, cognitive robotic and complex event processing.*](http://ceur-ws.org/Vol-1949/CILCpaper05.pdf), [CILC 2017](http://cilc2017.unina.it), 32nd Italian Conference on Computational Logic
26-28 September 2017, Naples, Italy
* RAFANELLI, Andrea; COSTANTINI, Stefania; DE GASPERIS, Giovanni. [*A Multi-Agent-System framework for flooding events. 2022*](https://ceur-ws.org/Vol-3261/paper11.pdf). WOA 2022: 23rd Workshop From Objects to Agents, September 1–2, Genova, Italy
* COSTANTINI, Stefania. [*Ensuring trustworthy and ethical behaviour in intelligent logical agents](https://academic.oup.com/logcom/article/32/2/443/6513773). Journal of Logic and Computation, 2022, 32.2: 443-478.