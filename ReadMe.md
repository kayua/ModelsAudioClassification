# Sound classification - Neural Network Models
---------------------
This repository contains the implemented code for the classification of mosquito audios using deep neural networks. It includes state-of-the-art algorithms and advanced techniques employed in the study, providing a robust basis for the analysis and categorization of complex acoustic patterns. 


![Spectrogramas](Layout/AudioSegments.png?raw=true "")
[View original publication](https://www.sciencedirect.com/science/article/pii/S1746809424004002)

The code made available aims to facilitate the replication of the experiments and the application of state-of-the-art methodologies in audio processing and bioacoustics. The implementation contains the definitions of the models, layers, blocks and loss functions necessary for the correct functioning of the models, as well as an evaluation framework that allows the analysis of the models' performance.

---------------------
## Neural Network Topologies

This repository contains the implementation and evaluation of six distinct deep neural network topologies for audio recognition. Each topology was developed for the analysis and identification of specific acoustic patterns in the audio emitted by mosquito wings, providing a robust technical basis for the comparative evaluation of the proposed solutions. Below are listed each of the topologies present in this repository, as well as their structure and original work.

### Original Papers:

1. Audio Spectrogram Transformer [https://arxiv.org/abs/2104.01778]
2. Long Short Term Memory [https://www.bioinf.jku.at/publications/older/2604.pdf]
3. Conformer [https://arxiv.org/abs/2005.08100]
4. Wav2Vec2 [https://arxiv.org/abs/2006.11477]
5. Residual [https://doi.org/10.1016/j.bspc.2024.106342]
6. MLP [https://ieeexplore.ieee.org/document/8942209]

---------------------
## Models:
<table>
    <tbody>
        <tr>
            <th width="20%">AST Topology</th>
            <th width="20%">LSTM Topology</th>
            <th width="20%">Conformer Topology</th>
        </tr>
        <tr>
            <td><img src="Layout/AST-Model.png"></td>
            <td><img src="Layout/LSTM-Model.png"></td>
            <td><img src="Layout/Conformer-Model.png"></td>
        </tr>
    </tbody>
    <tbody>
        <tr>
            <th width="20%">Wav2Vec2 Topology</th>
            <th width="20%">Residual Topology</th>
            <th width="20%">MLP Topology</th>
        </tr>
        <tr>
            <td><img src="Layout/Wav2Vec2-Model.png"></td>
            <td><img src="Layout/Residual-Model.png"></td>
            <td><img src="Layout/MultiLayerPerceptron-Model.png"></td>
        </tr>
    </tbody>
</table>

## Experimental Evaluation

### Dataset for Experiments

Description of the datasets used for training and validating the models as well as the link to obtain them.

<table>
    <tbody> 
        <tr>
            <th width="10%">Dataset Description</th>
        </tr>
        <tr>
            <td><img src="Layout/Dataset-Description.png" alt="" style="max-width:100%;"></td>
        </tr>

</table>


### Fitting Analysis
Impact of the number of epochs on average error for Dense topology (arrangements A=3, window width W=11), LSTM topology (arrangements A=3, window width W=11), and Conv. topology (arrangements A=8, squared window width W=H=256).

<table>
    <tbody> 
        <tr>
            <th width="10%">AST Topology</th>
            <th width="10%">LSTM Topology</th>
            <th width="10%">Conformer Topology</th>
        </tr>
        <tr>
            <td><img src="Layout/dense_error.png" alt="" style="max-width:100%;"></td>
            <td><img src="Layout/lstm_error.png" alt="" style="max-width:100%;"></td>
            <td><img src="Layout/conv_error.png" alt="" style="max-width:100%;"></td>
        </tr>
   <tbody> 
        <tr>
            <th width="10%">Wav2Vec2</th>
            <th width="10%">Residual</th>
            <th width="10%">MLP</th>
        </tr>
        <tr>
            <td><img src="Layout/dense_error.png" alt="" style="max-width:100%;"></td>
            <td><img src="Layout/lstm_error.png" alt="" style="max-width:100%;"></td>
            <td><img src="Layout/conv_error.png" alt="" style="max-width:100%;"></td>
        </tr>

</table>

### Confusion Matrices
Multiclass confusion matrices for each of the evaluated models. The configurations were defined based on the best configuration found among those evaluated.
<table>
    <tbody> 
        <tr>
            <th width="10%">AST Topology</th>
            <th width="10%">LSTM Topology</th>
            <th width="10%">Conformer Topology</th>
        </tr>
        <tr>
            <td><img src="Layout/ConfusionMatrices_AST.png" alt="" style="max-width:100%;"></td>
            <td><img src="Layout/ConfusionMatrices_LSTM.png" alt="" style="max-width:100%;"></td>
            <td><img src="Layout/ConfusionMatrices_Conformer.png" alt="2" style="max-width:100%;"></td>
        </tr>
   <tbody> 
        <tr>
            <th width="10%">Wav2Vec2</th>
            <th width="10%">Residual</th>
            <th width="10%">MLP</th>
        </tr>
        <tr>
            <td><img src="Layout/ConfusionMatrices_Wav2Vec2.png" alt="" style="max-width:100%;"></td>
            <td><img src="Layout/ConfusionMatrices_Residual.png" alt="" style="max-width:100%;"></td>
            <td><img src="Layout/ConfusionMatrices_MLP.png" alt="" style="max-width:100%;"></td>
        </tr>

</table>

###  Parameter Sensitivity Analysis

Parameter sensitivity of Conv. topology withuniform probabilistic injected failure Fprob =10%
<table>
    <tbody>
        <tr>
            <th width="20%">Convolutional Topology</th>
        </tr>
        <tr>
            <td><img src="https://github.com/kayua/Regenerating-Datasets-With-Convolutional-Network/blob/master/layout/sens_conv.png" alt="" style="max-width:50%;"></td>
        </tr>


</table>


### Comparing our Neural Networks
Comparison of topologies MLP, LSTM (LS), and CNN for probabilistic injected failure and monitoring injected failure.
<table>
    <tbody> 
        <tr>
            <th width="10%">Probabilistic Injected Failure</th>
            <th width="10%">Monitoring Injected Failure</th>
        </tr>
        <tr>
            <td><img src="https://github.com/kayua/Regenerating-Datasets-With-Convolutional-Network/blob/master/layout/comparison_nn_pif.png" alt="2018-06-04 4 33 16" style="max-width:100%;"></td>
            <td><img src="https://github.com/kayua/Regenerating-Datasets-With-Convolutional-Network/blob/master/layout/comparison_nn_mif.png" alt="2018-06-04 4 40 06" style="max-width:101%;"></td>
        </tr>
        
</table>

### Comparison with the State-of-the-Art (Convolutional vs Probabilistic)

Comparison between the best neural network model and state-of-the-art probabilistic technique. Values obtained for probabilistic error injection and monitoring error injection.
<table>
    <tbody>
        <tr>
            <th width="20%">Convolutional vs Probabilistic</th>
        </tr>
        <tr>
            <td><img src="https://github.com/kayua/Regenerating-Datasets-With-Convolutional-Network/blob/master/layout/results.png" alt="2018-06-04 4 33 16" style="max-width:120%;"></td>
        </tr>


</table>

### Qualitative Analysis

Impact, in terms of number (left) and duration (right) of a trace (S1) failed (Fmon = 20) and regenerated using the proposed BB-based (topology=Conv., threshold α =0.50, arrangements A =8, squared window width W = H =256) and prior probabilistic-based (threshold α =0.75).

<table>
    <tbody> 
        <tr>
            <th width="10%">Sessions Duration</th>
            <th width="10%">Number Sessions</th>
        </tr>
        <tr>
            <td><img src="https://github.com/kayua/Regenerating-Datasets-With-Convolutional-Network/blob/master/layout/CDF_duration.png" alt="2018-06-04 4 33 16" style="max-width:100%;"></td>
            <td><img src="https://github.com/kayua/Regenerating-Datasets-With-Convolutional-Network/blob/master/layout/CDF_number_sessions.png" alt="2018-06-04 4 40 06" style="max-width:100%;"></td>
        </tr>
        
</table>

## Steps to Install:

1. Upgrade and update
    - sudo apt-get update
    - sudo apt-get upgrade 
    
2. Installation of application and internal dependencies
    - git clone [https://github.com/kayua/ModelsAudioClassification]
    - pip install -r requirements.txt
    
3. Test installation:
    - python3 main.py -h


## Run experiments:

###  Run (all F_prob experiments)
`python3 run_jnsm_mif.py -c lstm`

### Run (only one F_prob scenario)
`python3 main.py`

###  Run (all F_mon experiments)
`python3 run_mif.py -c lstm`

### Run (only one F_mon scenario)
`python3 main_mif.py`


### Input parameters:

    Arguments(run_TNSM.py):
        
       -h, --help            Show this help message and exit

    --------------------------------------------------------------
   
    Arguments(main.py):

          -h, --help            Show this help message and exit

        --------------------------------------------------------------




## Requirements:

`matplotlib 3.4.1`
`tensorflow 2.4.1`
`tqdm 4.60.0`
`numpy 1.18.5`

`keras 2.4.3`
`setuptools 45.2.0`
`h5py 2.10.0`




