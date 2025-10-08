# The Ghost in the Browser: A Spatio-Temporal Framework for Detecting Autonomous Browsing Agents

## Abstract
Web traffic today is a complex mix of human users and automated agents, ranging from benign crawlers to adversarial scanners capable of widespread attacks. The most recent evolution of this threat comes from autonomous browsing agents, powered by Large Language Models (LLMs). These agents can automate complex tasks for adversarial purposes, from account hijacking to bypassing CAPTCHAs at scale, rendering many traditional bot defenses obsolete. This work introduces WebGuard, a spatio-temporal framework to detect autonomous browsing agents by creating rich, behavioral fingerprints from their interaction with web applications. WebGuard moves beyond analyzing simple mouse dynamics to capture the timing and location of over 40 distinct browser events. By applying supervised machine learning architectures to this fine-grained data, we can distinguish between human users and various classes of autonomous agents, including the latest LLM-powered systems. Evaluated on a real-world dataset of over 20 billion interaction artifacts, our framework achieves over 95\% detection accuracy in hundreds of milliseconds with a communication overhead below 18KB per second. This approach provides a robust, real-time method to expose these ghosts in the browser, re-establishing a clear line between human and machine activity on the modern web.


## Repository Structure
The repository includes different modules introduced in the corresponding paper. You can find details of each module in the following.

### Collector
The collector module includes both `server` and `client` codes of the data collection process. Details of the collector module can be found in a dedicated [README](collector/README.md) file included in the directory.

### Data
We have provided sample traces from each of the experimented agent types. Additionally, `data` directory includes the required codes for preprocessing of the raw json files to be used in future analysis.

### Deep Learning
The utilized `LSTM` and `1D-CNN` model architectures, as well as the required codes for training and test phases are available in the `Deep Learning` directory. 
