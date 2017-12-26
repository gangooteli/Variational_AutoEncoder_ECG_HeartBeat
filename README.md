# Variational_AutoEncoder_ECG_HeartBeat
Variational Autoencoder for ECG heartbeat dataset


Problem Statement:
Given a heartbeat, need to detect whether heart beat is normal or abnormal.
If it is detected as abnormal, how much severe is the condition of patient.

Dataset:
Physionet dataset: https://www.physionet.org/challenge/2016/sources/

Solutions Implemented:
Implemented a variational AutoEncoder which will be trained on only normal
heartbeat dataset. The trained model will learn the representation of normal
heartbeat using VAE. Now given a heartbeat to model, if loss of the model is
greater than a certain threshold, it will be classified as abnormal heartbeat.
Apart from that, more the difference of loss from threshold, more is the
severity of the patient. 


Proposed new Solutions to try out for better convergence and improvement of 
accuracy:
Use dynamic RNN model to feed the heartbeat of different sizes and train
on both normal and abnormal dataset.
And classify it into normal and normal heartbeat. The sequence to sequence
model might work much better in learning the representation of data as
data is sequential in nature.
1) Seq2Seq only
2) Seq2Seq + Attention
3) Attention only
