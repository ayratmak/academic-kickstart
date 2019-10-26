---
title: "The Ivory Game"
date: 2019-03-07T21:13:12Z
draft: false
tags: ["stackelberg game","mixed equilibrium","poaching","security","elephants"]
---
{{< figure library="1" src="elephants.jpg" >}}

_Poaching remains a serious threat to the wildlife with some animal populations now critically endangered. The population of tigers in the world has fallen by 95% since the beginning of last century largely due to poaching activities. Three out of nine species now completely extinct. Most of the endangered animals such as elephants and rhinos now exist in protected areas of specially established national parks. The rangers however find it difficult to patrol the parks given the vastness of the territories that stretch for hundreds of miles. Often times limited resources on the ground mean that rangers need to know the location of poachers' next strikes._


## Game Theory - an effective weapon to combat poaching

Game theory is the study of strategic interaction such as conflict or cooperation between decision-makers. When combating poaching, the two sides of the interaction are the conservation agencies' rangers and poachers. Each side wants to take a suitable action that maximises their payoffs, such that the outcome is in the agent's best interest.

The problem that game theory helps to solve in this environment is understanding how to deploy randomised patrols in order to maximise the probability of catching ivory poachers. The advantage of game theoretic and behavioural economics models in the context of patrolling is that they help to understand how an agent should randomise patrolling to not be predictable. The goal of game theory is to find an equilibrium randomisation solution to the patrolling problem.


## Ground patrolling can be modelled with game theory

Head of security at the Big Life foundation in Kenya - Craig Miller and his team spend days and nights protecting elephants on the ground in the vast savanna. This does not only involve collecting elephant snares and scaring off poachers but also keeping an eye local residents that seek revenge with the elephants for destroying their food crops.

They key for Craig's patrols is to appear in unpredictable places at unpredictable times, such there are no clear patterns in the surveillance cycle. Randomness however is not easy in practice as people tend to follow patterns even when their goal is to be unpredictable. Let's examine an economic model where the search space can be represented as a network, taking Craig and his team as an example.  

Craig and his team are "Defenders" in the set-up of our game and can travel to different locations during the course of their shifts. Poachers and disgruntled farmers are "Attackers", who need to be detected within a given time period in order to stop the attack. The game itself is zero-sum, meaning that it's a win for one party - loss for the other situation that we are looking at.


## Stackelberg Games are implemented to combat poaching

Set-up of the above can be formalised into the Stackelberg game framework. Stackelberg model provides a formulation of the game where one party acts first, with their actions being observed by the adversaries who conduct surveillance and react. The model is based on sequential moves where one party acts first and the other responds. Stackelberg games are widely used in the security setting, as security personnel deployment is easily observable.

The way of deploying resources for defenders is through selection of routes to patrol the territory. Rangers protect targets that are distributed along the territory while following a given route.
The territory itself can be divided into equal square grids of a certain size. This is indicated in diagram a. Coverage area where there are 4 equal sized sections.

Defenders needs to protect a set of targets T using scarcely available resources. Attackers in the model can monitor the Defenders' actions over time and is able to learn the Defender's strategy and adapt as necessary. In game theory, the actions that agents choose are indicated by their strategies, in our case -
	- … Defender's pure strategy is to deploy a set of resources R on patrolling routes (these are significantly restricted are not sufficient to cover all targets T)
	- … Attacker's pure strategy is to select and attack a certain target


## Mixed strategy is key to outsmart poachers

As Attackers can observe and adapt to Defenders' patrolling behaviour, Defenders need to avoid pure strategies and instead select a mix of alternating pure strategies to pick from. The mixed strategy of the defender is defined as randomisation over the pure strategy resulting in a certain probability distribution.

Associated with each target are payoff values that indicate the utility of a player (defender or attacker) when an attack succeeds or fails. The outcome payoff then depends on: (a) attacked target and (b) whether the target is protected by a defender.

The solution to this game is a mixed strategy for the defender that maximises his payoff. The attacker then learns the defender's mixed strategy and adjust his own best-response action. The defender's mixed strategy solution is  
A probability distribution over all of his possible pure strategies. This implies that there is a probability percentage associated with covering every target. Such probabilistic assignment of defender's scarce resources to targets is known as a Stackelberg equilibrium.


## Randomising over routes is required

Imagine a simple example where there is one ranger that needs to patrol the territory that consists of four target locations illustrated with four cells in a. Coverage area. The ranger then has a choice of three possible routes that she can take in order to patrol the targets. Each of the patrol routes starts at the base camp location in upper-left square (diagram b) and then proceeds to one of the other three targets, thus covering two targets with every route.

{{< figure library="1" src="patrol2.png" >}}

## Human rationality needs to be taken into account

As poaching attacks happen regularly and the interaction is between the same individuals on both sides, the recurring behaviour should be modelled as a repeated game. The repeated nature of the game in turn implies that the learning behaviour of the Attackers has to be adjusted for given the relevant observations. In Stackelberg security games a number of behavioural models are used to predict how human agents act over time. In reality, economic models need to also account for bounded rationality - the idea that suggests that individuals' rationality when making a decision is hindered by the available information, cognitive limitations and time constraints. The bounded rationality of humans implies that adversaries do not always choose the targets the maximise their payoffs.  

PAWS, a game theory based tool to assist conservation agencies, makes use of a bounded rationality model to predict an adversary's response to the defender's strategy. The model implies that attackers determine their strategy based on a number of observable features such as (i) probability that targets are protected, (ii) probability that they will be caught, (iii) reward for a successful attack and (iv) penalty for being captured. Based on these parameters that model then calculates the subjective utility for an adversary and makes a prediction which targets have a higher likelihood to be attacked. PAWS also attempts to incorporate the learning behaviour of adversaries. By making observations on adversaries' past activities, the bounded rationality model can be used to update parameters on subjective utilities.

## Other domain features can be considered

The real life scenarios tend to be more complicated that the economic model outlined above suggests. Other domain features that affect the creation of patrols such as (a) terrain information, (2) patrolling constraints and (3) uncertainty in wildlife distribution also need to be considered. All three of the constraints are crucial to creating a stable strategy to combat poaching activities and can be considered in the model by making the necessary adjustments.

---
