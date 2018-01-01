# pre10

i am starting

import copy, numpy as np

def sigmoid(x):
    output = 1/(1+np.exp(-x))
    return output
def sigmoid_ouput_to_derivative(output):
    return output*(1-output)

int2binary={}
binary_dim=8

largest_number=pow(2,binary_dim)

binary = np.unpackbits(  np.array([range(largest_number)],dtype=np.uint8).T            ,axis=1)


for i in range(largest_number):
    int2binary[i]=binary[i]


alpha=0.1
input_dim=2

hidden_dim = 16
output_dim = 1

synapse_0 =2*np.random.random((input_dim,hidden_dim))-1
synapse_1 =2*np.random.random((hidden_dim,output_dim))-1
synapse_h= 2*np.random.random((hidden_dim,hidden_dim))-1
