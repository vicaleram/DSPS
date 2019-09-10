# Section 3 

# Goal: compare the distribution of time gaps between earthquakes for magnitude M > Mk with that of  
time gaps between earthquakes of magnitude M > Ml for various values of Ml and Mk.
If a scaling law holds the distributions should be “the same” 
i.e. you cannot rule out that they are drawn from the same parent distribution. 
The KS test is designed to test this last hypothesis.

Before performing the test though, the distributions must be scaled by the average gap time and cleaned of events too close in time.


# pseudocode:

```
For all Mk values of M{
	# remove gaps below minimum gap threshold
	x_Mk =  gaps > M_k
	xreduced_Mk = x_Mk where x_Mk > threshold # this can be achieved by broadcasting in python
	For i in [1,2]: # do it twice
	}
# Rescale the time gaps distribution by the mean value of the time gaps.
Rx = 1 / mean(xreduced_Mk)
xreduced_Mk  = xreduced_Mk * Rx


For all Mk values of M {
   For all Ml values of M greater than Mk{
	Perform the KS test on (Mkm, Ml)
	}
   }

```
