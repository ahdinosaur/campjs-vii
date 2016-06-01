# nature's best practices for distributed systems

TODO get local remark copy

## hi

i'm [Mikey (@ahdinosaur)](http://dinosaur.is)

from [Enspiral](http://enspiral.com)

???

i have no idea what i'm saying

i will use imprecise terminology

- http://cacm.acm.org/magazines/2015/1/181614-distributed-information-processing-in-biological-and-computational-systems/abstract
- http://www.ribbonfarm.com/2015/03/04/gardens-need-walls-on-boundaries-ritual-and-beauty/
- http://networkcultures.org/unlikeus/resources/articles/what-is-a-federated-network/

## overview

- introduction
- natural networks
- global peer-to-peer networks
- local peer-to-peer networks

## introduction

### nature

life is hard to kill

???

try killing the fungus spores in your fridge

### systems 101

- networks: who you connect to
- messages: what you say
- signals: how you connect

example: our global socio-economic system

???

### coordination problems

>  Coordination problems are cases in which everyone agrees that a certain action would be best, but the free market cannot coordinate them into taking that action.

every intelligent person knows climate change is a problem to be solved.

yet we're not doing enough to solve it.

???

- http://www.raikoth.net/libertarian.html#coordination_problems

## natural networks

### stigmergy over control

central planning and control is a common solution to coordination problems.

> Most biological systems are distributed and must make decisions and respond to stimuli without a centralized coordinator and under severe constraints (energy conservation, limited communication range, limited messaging language, among others)

???

- http://cacm.acm.org/magazines/2015/1/181614-distributed-information-processing-in-biological-and-computational-systems/abstract
- https://en.wikipedia.org/wiki/Stigmergy

### simple over complex

rather than sophisticated synchronous protocols (like the OAuth dance),

most natural systems communicate with simple asynchronous messages

![](./complex-vs-simple-commmunication.png)

### randomized over deterministic

![](deterministic-vs-randomized-algorithms)

???

> A stochastic event or system is one that is unpredictable due to the influence of a random variable.

- https://en.wikipedia.org/wiki/Stochastic

### beeping

![](./beeping.png)

fly brains specialize cells with Max Independent Set

???

beeping: 

> Beeping: The beeping model17 (Fig- re 2a) assumes the only message hat can be sent or received is a beep (a unary signal). The model assumes an anonymous broadcast network in which nodes have no knowledge about the topology of the network or even an upper bound on its size. In each time slot a node can either beep or be si- lent. At a particular time slot, beeping nodes receive no feedback (they can- not determine if other nodes beeped as well), while silent nodes can only differentiate between two states: none of its neighbors beeping, or at least one neighbor beeping. Such a model is also appropriate for cellular signaling net- works as discussed here.

fly brains: developing fly brains select a subset of cells to become sensory bristles on the fly's forehead.

- http://cacm.acm.org/magazines/2015/1/181614-distributed-information-processing-in-biological-and-computational-systems/abstract

### stone-age

![](./stone-age.png)

![](./slime-mold-routing.jpg)

???

> Foraging slime molds have also been shown to adaptively adjust their networks of tubular junctions based on the distribution and availability of food sources in the area, which is typically unknown a priori. 52
> Slime molds also forage using breadth-first search using real cellular material, which is later pruned when optimal paths are found.  

- http://cacm.acm.org/magazines/2015/1/181614-distributed-information-processing-in-biological-and-computational-systems/abstract
- http://www.wired.com/2010/01/slime-mold-grows-network-just-like-tokyo-rail-system/

### population

![](./population.png)

harvester ants forage for food with Transmission Control Protocol (TCP)

???

> A recent study demonstrated that with limited communication, ants solve the foraging problem by implementing a version of the Transmission Control Protocol (TCP), which is used on the Internet to determine available bandwidth when routing packets. If packet acknowledgments (ACKs) are received quickly, the sender assumes bandwidth is available and boosts transmission; but if ACKs are returned slowly, the sender assumes the network is congested and throttles down transmission. Similarly, the important factor for the ants is the rate of antennal contacts (a binary indicator) between ants currently in the nest and successful ants (with food) returning to the nest. If the rate of contact is high, it implies food in the environment is plentiful, and thus outgoing ants also leave the nest at a faster rate.

- http://cacm.acm.org/magazines/2015/1/181614-distributed-information-processing-in-biological-and-computational-systems/abstract
- http://priceonomics.com/the-independent-discovery-of-tcpip-by-ants/

### fractals

example: human organism -> organs -> tissues -> cells -> organelles -> large molecules -> small molecules -> atoms -> particles

???

blood-brain barrier protects brain from bad actors.

example: brains are composed of fractal agents

> For our purposes, an agent is an entity capable of autonomous, intelligent, goal-directed behavior.

![](agency-in-the-brain.png)

> Thus there is, in this view, an internal 'economy' in the brain, in which neurons must compete with each other for resources. This design stands in contrast to the standard, Von Neumann computer architecture, whose parts never have to worry about where their energy is coming from. Without resource contention, there's no need for selfishness. And this is, in part, why computers are less flexible and adaptable — less plastic — than brains.

???

- http://www.meltingasphalt.com/neurons-gone-wild/
- https://blog.dinosaur.is/life-as-a-holon/
- Aida, K., Natsume, W. and Futakata, Y. Distributed computing with hierarchical master-worker paradigm for parallel branch and bound algorithm.  In Proceedings of the 31 st International Symposium on Cluster Computing and the Grid.  IEEE Computer Society, Washington, DC, 2003.  

### small worlds

![](./speed-vs-robustness.png)

> A small-world network is a type of mathematical graph in which most nodes are not neighbors of one another, but most nodes can be reached from every other node by a small number of hops or steps

???

> For example, dense topologies with clique-like structures are often used in instances where little-to-no noise is expected, whereas sparser topologies are preferred when networks are expected to face more noise.40
>
> Of course, spars- er topologies are also less efficient (in terms of routing distance, for example) which means execution times will be longer for such topologies. Weakly linked modules, on the other hand, can isolate occasional noise into nearly independent modules that each per- form efficiently.56

- http://cacm.acm.org/magazines/2015/1/181614-distributed-information-processing-in-biological-and-computational-systems/abstract

> Small-world properties are found in many real-world phenomena, including websites with navigation menus, food chains, electric power grids, metabolite processing networks, networks of brain neurons, voter networks, telephone call graphs, and social influence networks.
>
> Networks of connected proteins have small world properties such as power-law obeying degree distributions.[9] Similarly transcriptional networks, in which the nodes are genes, and they are linked if one gene has an up or down-regulatory genetic influence on the other, have small world network properties.[10]
>
> It is hypothesized by some researchers such as Barabási that the prevalence of small world networks in biological systems may reflect an evolutionary advantage of such an architecture. One possibility is that small-world networks are more robust to perturbations than other network architectures. If this were the case, it would provide an advantage to biological systems that are subject to damage by mutation or viral infection.
>
> By contrast, in a random network, in which all nodes have roughly the same number of connections, deleting a random node is likely to increase the mean-shortest path length slightly but significantly for almost any node deleted. In this sense, random networks are vulnerable to random perturbations, whereas small-world networks are robust. However, small-world networks are vulnerable to targeted attack of hubs, whereas random networks cannot be targeted for catastrophic failure.
>
> Appropriately, viruses have evolved to interfere with the activity of hub proteins such as p53, thereby bringing about the massive changes in cellular behavior which are conducive to viral replication.

https://en.wikipedia.org/wiki/Small-world_network


### handling failure

instead of using sophisticated consensus algorithms, nature uses toplogical features to handle failures.

![](./toplogy-on-speed-and-robustness.png)

???

example: viruses, cells 

> In distributed computing, failures have primarily been handled by majority voting methods, 37 by using dedicated failure detectors, 25 or via cryptography.  41 In contrast, most biological systems rely on various network topological features to handle failures.

...

> underlying network topology. For example, activity-dependent plasticity of synapses is a well-known phenomenon by which neural networks are shaped by environmental stimuli. These sig- nals are processed in a streaming fash- ion, and input patterns can change the topology of the networks designed to
process them.

- http://cacm.acm.org/magazines/2015/1/181614-distributed-information-processing-in-biological-and-computational-systems/abstract

## global distributed networks

???

- https://blog.dinosaur.is/global-vs-local-systems/

### example: internet service providers

> The very fabric of the Internet can be torn apart by a malicious ISP or even an honest mistake. On April 8th, 2010, an employee at China Telecom misconfigured a router - causing widespread Internet outages lasting up to fifteen minutes.

???

https://docs.meshwith.me/project-goals.html

- Pakistani ISP uses BGP to blackhole internet

### example: global registries

CA certs and DNS are based on central registries.

Namecoin distributes the protocol, but not the registry.

???

- how do we deal with multiple nicknames in real life?

### example: mobile network providers

i have phone with a radio, you have phone with a radio, we can't connect because a base station is down.

peer -> middleman -> peer

### example: buying a bicycle with Bitcoin

let's say i'm buying a bicycle from a neighbor.

with Bitcoin, i have to send a message to random strangers (miners) to participate in a global consensus process.

???

- cost of Bitcoin global consensus is large amounts of duplicate CPU work in Proof-of-Work cycles
- within a very few degrees of trust separation from my neighbor, we could be doing local consensus
- cost of Ethereum global computation is large amounts of duplicate memory and CPU work in computation cycles

### example: downloading a file with Bittorrent

when i download a file with Bittorrent, i connect to random strangers.

this means it's easy to monitor who is downloading what.

### example: twitter abuse

since everyone is connected to everyone, there's no barrier to abusing someone on Twitter.

the victim is the one who has to signal a block, rather than permit the message before.

???

- also easy to spam
  - email
  - distributed hash tables

### example: global socio-economic networks

the economy is converging on mega-corporations, at the expense of small business.

many of these mega-corps act as middleman within closed markets: Uber.

???

- peer -> middleman -> peer
  - where middleman sets price for both supplier and consumer
  - workers on both sides assume all risk, no risk for middleman
- winner-take-all effects of global networks (Uber)

### example: global culture

the world is converging on a uniform culture, at the expense of diversity.

- what narratives and metaphors do you use to express your world view?
- how might these bias or blind your thinking?

???

- https://github.com/RichardLitt/endangered-languages

reality is neither objective nor global.

> Westerners, he says, prefer to understand things as mechanisms, while the Chinese prefer to understand things as organisms — and these are two very different kinds of processes.

- http://www.meltingasphalt.com/technical-debt-of-the-west/

reality is subjective and local.

- https://github.com/ssbc/secure-scuttlebutt/issues/86

## local peer-to-peer networks

### why local?

> On the biological side, as technology continues to improve and sheds light on molecular and cellular decision-making, we believe computational perspectives will be essential to understand how local, distributed rules give rise to robust, global systems.

???

- http://cacm.acm.org/magazines/2015/1/181614-distributed-information-processing-in-biological-and-computational-systems/abstract

- global networks of ant colonies
- planet ecology


### systems of the future

- networks: you connect to local agents (based on social or geographic proximity)
- messages: you say things subjective to your view
- signals: you use gossip protocols to relay information

### local agents

- individual
- professional
  - [family](https://github.com/enspiral-root-systems)
  - [community](http://devacademy.co.nz)
  - [network](http://enspiral.com)
- regional
  - suburb
  - city
  - state

### subjective views

- my friends call me Mikey
- my parents call me Michael
- i call myself dinosaur

### gossip protocols

relay a message through who's local to you.

example: i run into Alice in town. "hey what's the lastest you've heard from Bob?"

???

> [biological] message sizes are usually one bit or of constant size indicting that unlike many traditional distributed algorithms, biological processes do not use such an identifier to label the sender and receiver

blockchain message gossip

- https://en.wikipedia.org/wiki/Gossip_protocol
- https://github.com/ssbc/scuttlebot
- https://github.com/substack/swarmbot

### example: secure scuttlebutt (SSB)

peer-to-peer log store:
 
- each user has a feed associated with a public and private keypair
- each feed is a linked list of message signed with the associated private key
- messages can reference each other to create links (and indexes)
- each user gossips with who they "follow", and who those users "follow"
- public messages are plain JSON objects
- private messages with the public key of the intended recipient
  - try to decrypt to see if it is for you

### example: Patchwork

peer-to-peer social network:

- each user can create "about" messages for any other user (name, avatar, ...)
- any user can create "post" messages which provide Twitter / Facebook style communication

also [git-ssb](https://github.com/clehner/git-ssb) and [git-ssb-web](https://github.com/clehner/git-ssb-web), which replicates git and GitHub, respectively.

### demo

## thanks

:3

- [Patchwork](https://ssbc.github.io/patchwork): proof-of-concept for truly distributed social network
- [scuttlebot](https://scuttlebot.io): underlying peer-to-peer log store
- [Value Flows](https://valueflo.ws): protocols for fractal socio-economic systems

# leftover content (notes)

## agent trust networks

> @dominictarr: you just interact with your friends, etc, and following someone is basically saying "this user is a real human, not a bot, and not a scammer" That is a expression of trust. Sometimes they may make a mistake, and trust someone who turns out to be a jerk, for this reason, trust must be revokeable.
Thus, instead of just signing each other's keys (as in gpg) we need to be able to sign a variety of statements about those keys. Those keys must also sign statements about other things (posts, or links to external files etc) so that the statements about those external things are tied into a specific context.

- https://github.com/ssbc/secure-scuttlebutt/issues/65#issuecomment-64903674

> @mixmix: My favourite way of thinking about all this is that truly decentralised p2p is actually alarmingly similar to your everyday social interactions - no-one is really a boss, anyone can lie, trust matters, and you ignore stuff and people that have bad reputation.
Also, no-one can stop you talking with friends... and you don't need to be able to reach america to be able to talk

- http://hyper.mixmix.io/?source=https%253A%252F%252Fgithub.com%252Fmixmix%252Fblogposts%252Fblob%252Fmaster%252Funcapturable_distribution.md

## permaculture

- symbiotic relationships
  - companion planting (e.g. carrots with sage)
  - 1 + 1 = 3

### leaders

alpha wolf is boss of pack, not boss of all packs.

large molecule doesn't get bonus and become organelle

## other links

- https://github.com/du5t/spaceship
- http://artbrock.com/blog/perspectives-blockchains-and-cryptocurrencies

### example: B.A.T.M.A.N

https://en.wikipedia.org/wiki/B.A.T.M.A.N.
