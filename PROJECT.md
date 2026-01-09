Hi! The whole plan of this repo is to construct a mathematically rigorous model for dynamic sparse networks on a continuum (DSNC). Ideally, we'd love to have a continuous time model on a continuum of agents of finitely many baseline types s.t.
• agents form links and befriend with other agents at a Poisson rate (regardless of types). Link formation is per-agent (not per-pair), ensuring finite degree and non-explosion on finite horizons.
• existing links remove at a Poisson rate (regardless of types)
• Idiosyncratic type transformation at given Poisson rates on agent level
• link-induced type transformation at given Poisson rates on link level. For each existing link $(i, j)$, there is an independent Poisson clock of rate that triggers a transition (possibly changing one or both endpoints' types). For example, type S agent might become type I because of her type I friends' influence via their links. Such influences are link-independent.)
All these Poisson rates are independent. At any time t, this network is sparse, because each agent would only have finitely many friends.
This seems like a math model, but eventually we are going to endogenize some of the Poisson rates by considering some types of agents behaviors.

The main technical issue is the measurability issue of a continuum of independent random variables --- here in our model the random variable is the rooted tree structure on agent i.

What's great is that literature has already done very similar things for random matching. Duffie and Sun 2007 have a rigorous model for instantaneous random matching with finite types. They use nonstandard analysis to get a larger sigma algebra to allow for a continuum of independent random variables and then use Sun 2006's exact law of large number (ELLN) to lift micro-level dynamics to macro, aggregate dynamics, describing them with ODEs. Furthermore, Duffie, Qiao, and Sun 2025 constructed a model of continuously time random matching, extending their previous result from one-shot, static to continuous time. My advisor Ben Golub, my coauthor Yueh-Sheng Hsu, and I believe that their setup and their language are exactly what we can build our model on. Our model would be an extension of their model, with agents' types being a lot more (from their and their neighbors' types to types of rooted trees).

Here's a to-do list in order, subject to change:
• Understand various versions of ELLN (Sun 2006): partially done
• Learn nonstandard analysis and understand the construction of Fubini extension (static matching) in DS 2007: partially done
• Understand the construction of Fubini extension (dynamic matching) in DS 2025
• Do the construction of Fubini extension for DSNC with my coauthor and agents: We might not have to reinvent the wheel, instead only having to modify DS 2025's approach.
• Prove our stochastic process satisfies essential pairwise independence so that we can leverage ELLN and move from micro to macro dynamics.
• Study the properties of this infinite set of ODEs: 
• I have some ideas to show that in our model, pair approximation is exact. We'll talk about this later.
til this point all the main math is done, then the 
• Economic part: endogenize some of the Poisson rates.