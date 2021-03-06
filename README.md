# sound-noise-reduction-rprop
Application to create neural nets, which can reduce noise from sound.

# General

App allows you to record or upload audio, make it 'noisy' and train neural nets using Parallel Resilient Backpropagation (rprop) form Accord c# library to then recover 'clear' audio.

# Neural euristics

I used neural net with 250, 180, 50, 1 nodes, sigmoid function with alpha = 0,25.

Learining rate eta+ was fixed at 1.2 and eta- at 0.5.

I shuffled noise every 100 iterations of training with total number of iterations of 500.

# Used noise

Noise can be found in NoiseReduction/Audio/Noise and it was taken from SPIB database http://spib.linse.ufsc.br/noise.html

# Valid neuro nets

Some of the neuro nets in project are damaged. If you want to test out 'best' neuro net you can find it in 'demos' folder. There are 5 nets, based on iterations number.

To test it out: open project in Visual Studio, then use right part of the interface to upload 'clean speech', 'noisy speech', press button below, find your neural net in 'demos' folder, save 'recovered speech'.

# How to use

Run the .sln in NoiseReduction folder (use Microsoft Visual Studio).

Interface can be split into three parts. 

Top left corner allows you to record or upload your 'speech' (Select Speech), upload noise (Select Noise) and save session (Save Session). After you uploaded 'speech and noise' you can press the 'add noise to speech' button or set different fraction of a noise first.

Lower you will find section to train your neural net. There are various options that can be set. Or you can upload some of your previous network for further training.

Right part of the app is to test your nets. Upload 'speech' and 'noisy speech', press the button and select neural net to reduce the noise.

# Demos

Go to github folder demos. There you can find initial sounds, sounds with noise and recovered sounds. Files "Word Яблоко Чист", "Яблоко шум" and "Яблоко очищ" are those on which neural net was trained, and "Word Груша Чист", "Груша шум" and "Груша очищ" are test sounds.
