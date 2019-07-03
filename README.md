# Reinforcement learning

This repository contains codes that I have reproduced for various RL algorithms.

## Implemented Algorithms

| **Algorithms**              | **Discrete**                      | **Continuous**                    | Multithreaded                     | Multiprocessing                  | **Tested on**            |
| --------------------------- | --------------------------------- | --------------------------------- |-----------------------------------|----------------------------------|--------------------------|
| DQN                         | :heavy_check_mark:                |                                   |                                   |                                  | CartPole-v0              |
| Double DQN (DDQN)           | :heavy_check_mark:                |                                   |                                   |                                  | CartPole-v0              |
| Dueling DDQN                | :heavy_check_mark:                |                                   |                                   |                                  | CartPole-v0              |
| Dueling DDQN + PER          | :heavy_check_mark:                |                                   |                                   |                                  | CartPole-v0              |
| A3C <sup>(1)</sup>          | :heavy_check_mark:                | :heavy_check_mark:                | :heavy_check_mark:                | :heavy_check_mark:               | CartPole-v0, Pendulum-v0 |
| DPPO <sup>(2)</sup>         |                                   | :heavy_check_mark:                |                                   | :heavy_check_mark:<sup>(3)</sup> | Pendulum-v0              |
| RDN + PPO                   |                                   | :heavy_check_mark:                |                                   |                                  | MountainCarContinuous-v0 |

<sup><sup>(1): N-step returns used for critic's target.</sup></sup><br>
<sup><sup>(1): GAE used for computation of TD lambda return (for critic's target) & policy's advantage.</sup></sup><br>
<sup><sup>(3): Distributed Tensorflow & Python's multiprocessing used.</sup></sup><br>

## Blog

Check out my [blog](https://ChuaCheowHuan.github.io/) for more information on my repositories.






1) Deep Q networks (DQN) [code](https://github.com/ChuaCheowHuan/reinforcement_learning/blob/master/DQN_variants/DQN/DQN_cartpole.ipynb)

>A Deep Q Network implementation in tensorflow with target network & random
experience replay. CartPole-v0 is used as the discrete environment. [writeup](https://chuacheowhuan.github.io/DQN/)

2) Double DQN (DDQN) [code](https://github.com/ChuaCheowHuan/reinforcement_learning/blob/master/DQN_variants/DDQN/double_DQN_cartpole.ipynb)

>A Double Deep Q Network (DDQN) implementation in tensorflow with random
experience replay. [writeup](https://chuacheowhuan.github.io/DDQN/)

3) Duelling DDQN [code](https://github.com/ChuaCheowHuan/reinforcement_learning/blob/master/DQN_variants/duel_DDQN/duelling_DDQN_cartpole.ipynb)

>A Dueling Double Deep Q Network (Dueling DDQN) implementation in tensorflow
with random experience replay. CartPole-v0 is used as the discrete environment. [writeup](https://chuacheowhuan.github.io/Duel_DDQN/)

4) Duelling DDQN with PER [code](https://github.com/ChuaCheowHuan/reinforcement_learning/blob/master/DQN_variants/duel_DDQN_PER/duelling_DDQN_PER_cartpole.ipynb)

>A Dueling Double Deep Q Network with Priority Experience Replay
(Duel DDQN with PER) implementation in tensorflow. CartPole-v0 is used as the
discrete environment. [writeup](https://chuacheowhuan.github.io/Duel_DDQN_with_PER/)

5) Asynchronous Advantage Actor Critic (A3C) discrete with N-step targets (missing terms are treated as zero) [code](https://github.com/ChuaCheowHuan/reinforcement_learning/blob/master/A3C/A3C_disc_miss.ipynb)

>A3C (Asynchronous Advantage Actor Critic) implementation with
Tensorflow. This is a multi-threaded version. CartPole-v0 is used as the
discrete environment. [writeup](https://chuacheowhuan.github.io/A3C_disc_thread_nStep/)

6) A3C discrete with N-step targets (maximum possible terms are used) [code](https://github.com/ChuaCheowHuan/reinforcement_learning/blob/master/A3C/A3C_disc_max.ipynb)

>A3C (Asynchronous Advantage Actor Critic) implementation with
Tensorflow. This is a multi-threaded version. CartPole-v0 is used as the
discrete environment. [writeup](https://chuacheowhuan.github.io/A3C_disc_thread_nStep/)

7) A3C continuous with N-step targets (maximum possible terms are used) [code](https://github.com/ChuaCheowHuan/reinforcement_learning/blob/master/A3C/A3C_cont_max.ipynb)

>A3C (Asynchronous Advantage Actor Critic) implementation with
Tensorflow. This is a multi-threaded version. Pendulum-v0 is used as for
continuous environment. [writeup](https://chuacheowhuan.github.io/A3C_cont_thread_nStep/)

8) A3C discrete with N-step targets (maximum possible terms are used) (Implementated with distributed Tensorflow and Python's multiprocessing package) [code](https://github.com/ChuaCheowHuan/reinforcement_learning/blob/master/A3C/A3C_disc_max_dist.ipynb)

>A3C (Asynchronous Advantage Actor Critic) implementation with
distributed Tensorflow and Python's multiprocessing package.
CartPole-v0 is used as the discrete environment. [writeup](https://chuacheowhuan.github.io/A3C_dist_tf/)

9) Distributed Proximal Policy Optimization (DPPO) continuous (normalized running rewards with GAE) implementation with distributed Tensorflow and Python's multiprocessing package. [code](https://github.com/ChuaCheowHuan/reinforcement_learning/blob/master/DPPO/DPPO_cont_GAE_dist_GPU.ipynb)

>Pendulum-v0 is used as the continuous environment. [writeup](https://chuacheowhuan.github.io/DPPO_dist_tf/)

10) RDN (Random Distillation Network) with Proximal Policy Optimization (PPO) Tensorflow.

Full code:

>[Jupyter notebook](https://github.com/ChuaCheowHuan/reinforcement_learning/blob/master/RDN_PPO/RDN_PPO_cont_ftr_nsn_mtCar_php.ipynb)

>[Python file](https://github.com/ChuaCheowHuan/reinforcement_learning/blob/master/RDN_PPO/RDN_PPO_cont_ftr_nsn_mtcar_php.py)

>MountainCarContinuous-v0 is used as the continuous environment. [writeup](https://chuacheowhuan.github.io/RDN/)
