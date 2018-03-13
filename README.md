# 756project
A comparison of Scalability between Reinforcement Learning and Evolution Strategies on Benchmark Problems

** References

https://blog.openai.com/evolution-strategies/ :

"In particular, ES is simpler to implement (there is no need for backpropagation), it is easier to scale in a distributed setting, it does not suffer in settings with sparse rewards, and has fewer hyperparameters. This outcome is surprising because ES resembles simple hill-climbing in a high-dimensional space based only on finite differences along a few random directions at each step."

" Highly parallelizable. ES only requires workers to communicate a few scalars between each other, while in RL it is necessary to synchronize entire parameter vectors (which can be millions of numbers). Intuitively, this is because we control the random seeds on each worker, so each worker can locally reconstruct the perturbations of the other workers. Thus, all that we need to communicate between workers is the reward of each perturbation. As a result, we observed linear speedups in our experiments as we added on the order of thousands of CPU cores to the optimization."

 "ES is easy to implement and scale. Running on a computing cluster of 80 machines and 1,440 CPU cores, our implementation is able to train a 3D MuJoCo humanoid walker in only 10 minutes (A3C on 32 cores takes about 10 hours). Using 720 cores we can also obtain comparable performance to A3C on Atari while cutting down the training time from 1 day to 1 hour."

"Since ES requires negligible communication between workers, we were able to solve one of the hardest MuJoCo tasks (a 3D humanoid) using 1,440 CPUs across 80 machines in only 10 minutes. As a comparison, in a typical setting 32 A3C workers on one machine would solve this task in about 10 hours. It is also possible that the performance of RL could also improve with more algorithmic and engineering effort, but we found that naively scaling A3C in a standard cloud CPU setting is challenging due to high communication bandwidth requirements."

"On Atari, ES trained on 720 cores in 1 hour achieves comparable performance to A3C trained on 32 cores in 1 day. "

"Compared to this work and much of the work it has inspired, our focus is specifically on scaling these algorithms to large-scale, distributed settings, finding components that make the algorithms work better with deep neural networks (e.g. virtual batch norm), and evaluating them on modern RL benchmarks."


 https://eng.uber.com/deep-neuroevolution/

 https://www.oreilly.com/ideas/neuroevolution-a-different-kind-of-deep-learning :
 
 "That is, neuroevolution is just as eligible to benefit from massive hardware investment as conventional deep learning, if not more. The advantage for neuroevolution, as with all evolutionary algorithms, is that a population of ANNs is intrinsically and easily processed in parallel—if you have 100 ANNs in the population and 100 processors, you can evaluate all of those networks at the same time, in the time it takes to evaluate a single network. That kind of speed-up can radically expand the potential applications of the method."

One consequence is that labs with access to large-scale computing clusters can see that they might be sitting on a neuroevolution goldmine, prompting a new generation of researchers and next-generation neuroevolution experiments to grow out of labs largely otherwise invested in conventional deep learning."

[[https://arxiv.org/pdf/1602.01783.pdf][Asynchronous Methods for Deep Reinforcement Learning]] :

"By using 100 sep-arate  actor-learner  processes  and  30  parameter  server  in-stances, a total of 130 machines, Gorila was able to significantly outperform DQN over 49 Atari games.  On many games Gorila reached the score achieved by DQN over 20 times faster than DQN."

[[https://github.com/DEAP/deap][DEAP: Distributed Evolutionary Algorithms in Python]]

[[https://www.cs.cmu.edu/~muli/file/parameter_server_osdi14.pdf][Scaling Distributed Machine Learning with the Parameter Server]]

[[https://arxiv.org/pdf/1706.10059.pdf][Deep Reinforcement Learning for Portfolio Optimization]]

### Project Proposal:
https://github.com/LinuxIsCool/756project/blob/master/project_notes.org
