# cs550-lab-2-simple-communication-protocol-in-stainless-solved
**TO GET THIS SOLUTION VISIT:** [CS550 Lab 2-Simple communication protocol in Stainless Solved](https://www.ankitcodinghub.com/product/cs550-lab-2-simple-communication-protocol-in-stainless-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;118167&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;2&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (2 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS550 Lab 2-Simple communication protocol in Stainless Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (2 votes)    </div>
    </div>
In this second lab, you will use stainless to verify a simple communication protocol. As we will see, Stainless also allows us to prove properties on traits and classes, which are at the core of every Scala program.

By now you should already have some familiarities with Stainless. You can nonetheless find useful ressources in the handout of Lab 1 or on Stainless repository.

Getting the source

To start working on this lab, you can either clone this entire repository, or download the present directory alone from Gitlab (there should be a button for this on the top right of the web interface).

The protocol

The communication protocol we will prove properties about involves two Endpoints that both hold a sending and a receiving buffer. They contain respetively the messages that still need to be sent, and the ones already received. The messages go through a Network that can be queried to know whether they have been transmitted. The protocol is then defined as follow:

1. The sender sends a message over the network.

2. It then queries the network to know whether the message has been transmitted.

3. If this is the case, drop the last message sent from the buffer of the sender and add it to the buffer of the receiver. Otherwise skip to step 4.

4. Repeat step 1 with the updated sender and receiver.

In practice this means a message will be sent over and over until it has been transmitted. Since we want to reason about finite programs, we will run the protocol for a finite number of iterations. The method simulating the protocol is Network.messageExchange.

Goal of the lab

The protocol, in addition to the classes representing the Network and the Endpoints of the communication, are already implemented. The goal of the lab is proving some properties of the protocol such as its correctness, optimality conditions etc…

On Linux and WSL

stainless SimpleProtocol.scala

On Mac

stainless –solvers=smt-z3 SimpleProtocol.scala “`

The provided configuration file (stainless.conf) will automatically set the SMT solver’s timeout to 2 seconds. You can also pass other options by default such as –compact (only displaying VCs Stainless was not able to prove) or –watch by adding respectively compact=true and watch=true as new lines in the configuration file.

Submission

Once you’ve completed all proofs, you can submit your SimpleProtocol.scala file on Moodle. Only one member of each group should submit a solution.
