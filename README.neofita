# Kuramoto-model
def F(Theta,omega,K,N):
    import numpy as np
    omega = np.random.normal(0,1.0,(N,)) #valore atteso 0 ampiezza intervallo 01 dim 20 
    Fk=np.zeros(N)
  #modello kuramoto Ti'=omega +k/N*sum (sin Tj-Ti)
    
    for i in xrange(N):
        Fk[i]=omega[i]
        for j in xrange(N):
            Fk[i]=Fk[i]+(K/N)*np.sin(Theta[j]-Theta[i])
    return Fk
'''
'''
import numpy as np
np.random.seed(5)
N=50                #num oscillatori
ntime=1000
h=0.1
K=0.5
T=np.zeros(ntime)
Theta0=np.linspace(0,2*np.pi,N)
omega=np.random.randn(N)
Theta=np.zeros((N,ntime))
Theta[:,0]=Theta0
#algoritmo like eulero problemi diff primo ordine
for i in xrange(ntime-1):
    T[i+1]=(i+1)*h
    Theta[:,i+1]=Theta[:,i]+h*F(Theta[:,i],omega,K,N)

print Theta
print omega
import matplotlib.pyplot as plt
plt.plot(T,Theta.T)
plt.show()
