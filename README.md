# Moshi Interruption Controller

A lightweight controller for deciding when a full-duplex voice assistant should yield the floor.

Natural conversation includes both listener feedback and genuine interruptions. An assistant should continue through brief acknowledgments while responding promptly when the user wants to speak.

Our approach combines frozen Moshi speech representations with a 632K-parameter causal controller. It learns from conversational event intervals using noisy-OR supervision, identifying interruption cues without requiring precise frame-level boundaries. During inference, the controller continuously processes both audio channels and produces interruption decisions.

Experiments on TurnBench show strong interruption recall with controlled false positives. Compared with max-pooling interval supervision, noisy-OR achieves similar overall recall while reducing long-tail detection latency.

The project explores a practical way to adapt pretrained speech representations for responsive turn-taking with a small trainable component.
