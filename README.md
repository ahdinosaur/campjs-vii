# nature's best practices for distributed systems

hi, i'm Mikey (@ahdinosaur)

???

i have no idea what i'm saying

- http://cacm.acm.org/magazines/2015/1/181614-distributed-information-processing-in-biological-and-computational-systems/abstract
- https://github.com/du5t/spaceship

## systems 101

- networks: who you connect to
- messages: what you say
- signals: how you connect

## stigmergy

> Most biological systems are distributed and must make decisions and respond to stimuli without a centralized coordinator and under severe constraints (energy conservation, limited communication range, limited messaging language, among others)

- http://cacm.acm.org/magazines/2015/1/181614-distributed-information-processing-in-biological-and-computational-systems/abstract
- https://en.wikipedia.org/wiki/Stigmergy

## ants discover tcp

> A recent study demonstrated that with limited communication, ants solve the foraging problem by implementing a version of the Transmission Control Protocol (TCP), which is used on the Internet to determine available bandwidth when routing packets. If packet acknowledgments (ACKs) are received quickly, the sender assumes bandwidth is available and boosts transmission; but if ACKs are returned slowly, the sender assumes the network is congested and throttles down transmission. Similarly, the important factor for the ants is the rate of antennal contacts (a binary indicator) between ants currently in the nest and successful ants (with food) returning to the nest. If the rate of contact is high, it implies food in the environment is plentiful, and thus outgoing ants also leave the nest at a faster rate.

- http://cacm.acm.org/magazines/2015/1/181614-distributed-information-processing-in-biological-and-computational-systems/abstract
- http://priceonomics.com/the-independent-discovery-of-tcpip-by-ants/

## robustness

> In distributed computing, failures have primarily been handled by majority voting methods, 37 by using dedicated failure detectors, 25 or via cryptography.  41 In contrast, most biological systems rely on various network topological features to handle failures.

- http://cacm.acm.org/magazines/2015/1/181614-distributed-information-processing-in-biological-and-computational-systems/abstract

## slime mold discover network routing

> Foraging slime molds have also been shown to adaptively adjust their networks of tubular junctions based on the distribution and availability of food sources in the area, which is typically unknown a priori. 52
> Slime molds also forage using breadth-first search using real cellular material, which is later pruned when optimal paths are found.  

- http://cacm.acm.org/magazines/2015/1/181614-distributed-information-processing-in-biological-and-computational-systems/abstract
- http://www.wired.com/2010/01/slime-mold-grows-network-just-like-tokyo-rail-system/

## message strategies

> message sizes are usually one bit or of constant size indicting that unlike many traditional distributed algorithms, biological processes do not use such an identifier to label the sender and receiver

blockchain message gossip

- https://en.wikipedia.org/wiki/Gossip_protocol
- https://github.com/ssbc/scuttlebot
- https://github.com/substack/swarmbot

## neurons discover economic systems

> Thus there is, in this view, an internal 'economy' in the brain, in which neurons must compete with each other for resources. This design stands in contrast to the standard, Von Neumann computer architecture, whose parts never have to worry about where their energy is coming from. Without resource contention, there's no need for selfishness. And this is, in part, why computers are less flexible and adaptable — less plastic — than brains.

- http://www.meltingasphalt.com/neurons-gone-wild/

## brains are composed of agents

> For our purposes, an agent is an entity capable of autonomous, intelligent, goal-directed behavior.

![](agency-in-the-brain.png)

- http://www.meltingasphalt.com/neurons-gone-wild/
- https://blog.dinosaur.is/life-as-a-holon/

## agent trust networks

> @dominictarr: you just interact with your friends, etc, and following someone is basically saying "this user is a real human, not a bot, and not a scammer" That is a expression of trust. Sometimes they may make a mistake, and trust someone who turns out to be a jerk, for this reason, trust must be revokeable.
Thus, instead of just signing each other's keys (as in gpg) we need to be able to sign a variety of statements about those keys. Those keys must also sign statements about other things (posts, or links to external files etc) so that the statements about those external things are tied into a specific context.

- https://github.com/ssbc/secure-scuttlebutt/issues/65#issuecomment-64903674

> @mixmix: My favourite way of thinking about all this is that truly decentralised p2p is actually alarmingly similar to your everyday social interactions - no-one is really a boss, anyone can lie, trust matters, and you ignore stuff and people that have bad reputation.
Also, no-one can stop you talking with friends... and you don't need to be able to reach america to be able to talk

- http://hyper.mixmix.io/?source=https%253A%252F%252Fgithub.com%252Fmixmix%252Fblogposts%252Fblob%252Fmaster%252Funcapturable_distribution.md

## problem with globals

[reality is neither objective nor global.](http://www.meltingasphalt.com/technical-debt-of-the-west/)

[reality is subjective and local.](https://github.com/ssbc/secure-scuttlebutt/issues/86)

## example: buying a bicycle

let's say i'm buying a bicycle from a neighbor.

why should i have to connect to some random strangers to participate in a global consensus process in order to send digital coins to my neighbor?

it's likely that i'm within a very few degrees of separation from my neighbor, i should gossip through this local network.

## decentralized trust-ful

- networks: you connect to peers you trust
- signals: local subjective protocols

## gossip

## where to go from here

- [Value Flows](https://valueflo.ws): socio-economic infrastructure
- [ssb ecosystem](https://ssbc.github.io): technical infrastructure

## thanks

:3
