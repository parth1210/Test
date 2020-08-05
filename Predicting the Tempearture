import datetime,time
from sklearn.linear_model import LinearRegression


# utility function

def predictTemperature(startDate, endDate, temperature, n):
    w = int(len(temperature)/24)
    p = []
    for i in range(1,((24*w)+1)):
        p.append(i)
 
    lm = LinearRegression()
    lm.fit(np.asarray(p).reshape(-1,1),temperature)
    
    f = p[-1]+1
    z = []
    for i in range(24*n):
        z.append(f)
        f += 1
    return(lm.predict(np.asarray(z).reshape(-1,1)).tolist())
