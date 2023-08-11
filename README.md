# Multilayer Perceptron [XOR Gate]

Single Layer Perceptron can only be used for Linearly Seperable data. For Non Linearly Seperable cases we must use Multilayer Perceptron.

We use a summation and an activation function: 
```
def summation(x,w,b):
  sum_h = [0,0]
  for i in range(len(x)):
    sum_h[i] = (x[0]*w[:2][i]+x[1]*w[2:][i])+b[i]
    #sum_h[i] = np.dot(x,w[:2][i])[0]+b[i]
  return sum_h

def activation(sum):
  if sum >= 0:
    return 1
  else:
    return 0
```