<h1 align="center">PreGAN+</h1>
<div align="center">
  <a href="https://github.com/imperial-qore/PreGAN/blob/master/LICENSE">
    <img src="https://img.shields.io/badge/License-BSD%203--Clause-red.svg" alt="License">
  </a>
   <a>
    <img src="https://img.shields.io/badge/python-3.7%20%7C%203.8-blue.svg" alt="Python 3.7, 3.8">
  </a>
   <a>
    <img src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fimperial-qore%2FPreGAN&count_bg=%23FFC401&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false" alt="Hits">
  </a>
   <a href="https://github.com/imperial-qore/PreGAN/actions">
    <img src="https://github.com/imperial-qore/COSCO/workflows/DeFog-Benchmarks/badge.svg" alt="Actions Status">
  </a>
 <br>
   <a>
    <img src="https://img.shields.io/docker/pulls/shreshthtuli/yolo?label=docker%20pulls%3A%20yolo" alt="Docker pulls yolo">
  </a>
   <a>
    <img src="https://img.shields.io/docker/pulls/shreshthtuli/pocketsphinx?label=docker%20pulls%3A%20pocketsphinx" alt="Docker pulls pocketsphinx">
  </a>
   <a>
    <img src="https://img.shields.io/docker/pulls/shreshthtuli/aeneas?label=docker%20pulls%3A%20aeneas" alt="Docker pulls aeneas">
  </a>
</div>

Typical mobile edge computing infrastructures have to contend with unreliable computing devices at their end-points. The limited resource capacities of mobile edge devices gives rise to frequent contentions, node overloads or failures. This is exacerbated by the strict deadlines of modern applications. To avoid failures, fault-tolerant approaches utilize preemptive migration to transfer active tasks across nodes and prevent nodes running at capacity. However, prior work struggles to dynamically adapt in settings with highly volatile workloads or even accurately detect and diagnose anomalies for optimal remediation. To meet the strict service level objectives of contemporary workloads, there is a need for dynamic fault-tolerant methods that can quickly adapt to changes in edge environments while having parsimonious remediation in the form of preemptive migration to avoid stressing the system network. This work proposes PreGAN, featuring a Generative Adversarial Network (GAN) based approach to predict contentions, pinpoint specific resource types with high chance of overload, and generate migration decisions to proactively avoid system downtime. PreGAN leverages coupled-simulations to train the GAN model at run-time and a few-shot fault classifier to update decisions of an underpinning scheduler. We also extend it to PreGAN+ that also periodically tunes the decision model using semi-supervised training and a Transformer based neural network for low tuning time, albeit with higher memory overheads.  Experiments on a Raspberry-Pi based edge environment demonstrate that both models outperform state-of-the-art baselines in fault detection and diagnosis scores by up to 12.5% and 31.2% respectively. This also translates in improvements in Quality of Service against baseline approaches.

## Quick Test
Clone repo.
```console
git clone https://github.com/imperial-qore/PreGANPlus.git
cd PreGAN/
```
Install dependencies.
```console
sudo apt -y update
python3 -m pip --upgrade pip
python3 -m pip install matplotlib scikit-learn
python3 -m pip install -r requirements.txt
python3 -m pip install torch==1.7.1+cpu torchvision==0.8.2+cpu -f https://download.pytorch.org/whl/torch_stable.html
export PATH=$PATH:~/.local/bin
```
Change line 117 in `main.py` to use one of the implemented fault-tolerance techniques: `PreGANPlusRecovery`, `PreGANRecovery`, `PCFTRecovery`, `DFTMRecovery`, `ECLBRecovery` or `CMODLBRecovery` and run the code using the following command.
```console
python3 main.py
````

## External Links
| Items | Contents | 
| --- | --- |
| **Pre-print** | (coming soon) |
| **Video** | https://youtu.be/Pp82aZu5dJw |
| **Contact**| Shreshth Tuli ([@shreshthtuli](https://github.com/shreshthtuli))  |
| **Funding**| Imperial President's scholarship |


```

## License

BSD-3-Clause. 
Copyright (c) 2022, Shreshth Tuli.
All rights reserved.

See License file for more details.
