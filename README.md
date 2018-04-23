# Matplotlib
Some of the basics Plots in matplotlib. 

commonly used markers:
=======================
        "o" 	circle
        "v" 	triangle_down
        "^" 	triangle_up
        "<" 	triangle_left
        ">" 	triangle_right
        "8" 	octagon
        "s" 	square
        "p" 	pentagon
        "P" 	plus (filled) (caps 'P')
        "*" 	star
        "h" 	hexagon1
        "H" 	hexagon2
        "+" 	plus
        "x" 	x
        "X" 	x (filled)
        "D" 	diamond
---------------------------------------------------------

commonly used colors:
======================
        ‘b’ 	blue
        ‘g’ 	green
        ‘r’ 	red
        ‘c’ 	cyan
        ‘m’ 	magenta
        ‘y’ 	yellow
        ‘k’ 	black
        ‘w’ 	white
-----------------------------------------------------------

'''


Simple Plot along with various attributes:
============================================
from matplotlib import pyplot  as plt
import numpy as np
plt.plot([1,2,3,4,5],[1,2,3,4,5], 'g^') #plt.plot(x, y, linewidth=2.0, color='r', label='line 1')
#plt.axis([0, 10, 0, 10]) #plt.axis([xmin, xmax, ymin, ymax]) sets specifies the viewport of the axes
#plt.xlim(0,4)
#plt.ylim(0,4)
plt.xticks(np.arange(1, 10, 2.0)) #plt.xticks(np.arange(min_val, max_values(excludes last values), interval_value))
plt.legend(['test','train'], loc='upper right')
#plt.xscale("log")
#plt.xaxis.set_major_formatter(np.arange(0, 10, 0.5))
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.title('graph')
plt.show
---------------------------------------------------------------------------------------

Adding multiple plots
===============================

from matplotlib import pyplot  as plt
plt.plot([1,2,3,4,5],[1,2,3,4,5])
plt.plot([1,2,3,4,5],[5,4,3,2,1])
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.title('graph')
plt.show
---------------------------------------------------------------------------------------------
Adding styles to the graph and adding legends
==============================================

      from matplotlib import pyplot  as plt
      from matplotlib import style
      style.use('ggplot')
      plt.plot([1,2,3,4,5],[1,2,3,4,5],color='g',label='line 1',linewidth=5)
      plt.plot([1,2,3,4,5],[5,4,3,2,1],color='y',label='line 2',linewidth=5)
      plt.xlabel('X-axis')
      plt.ylabel('Y-axis')
      plt.title('graph')
      plt.legend()
      plt.grid(True,color='w') #shows the grid in graph
      plt.show
---------------------------------------------------------------------------------------------
Bar graph
=================================

      from matplotlib import pyplot  as plt
      plt.bar([1,2,3,4,5],[1,2,3,4,5],label='line 1',color='g')
      plt.bar([1,2,3,4,5],[5,4,3,2,1],label='line 2',color='b')
      plt.xlabel('X-axis')
      plt.ylabel('Y-axis')
      plt.title('graph')
      plt.legend()
      plt.show
-----------------------------------------------------------------------------------------------
Histogram
==================================

      from matplotlib import pyplot  as plt
      plt.hist([1,2,3,4,5,5,4,3,2,3,3,3,8,6,5,43,43,3,34,4,3,3,2,2,3,3],[6,7,8,9,10],histtype='bar',rwidth=0.3,label='line 1',color='g')
      plt.xlabel('X-axis')
      plt.ylabel('Y-axis')
      plt.title('graph')
      plt.legend()
      plt.show
-----------------------------------------------------------------------------------------------

scatterplot
====================================
      from matplotlib import pyplot  as plt
      plt.scatter([1,2,3,4,5],[1,7,8,9,10],label='line 1',color='k')
      plt.xlabel('X-axis')
      plt.ylabel('Y-axis')
      plt.title('graph')
      plt.legend()
      plt.show
------------------------------------------------------------------------------------------------

pie chart
====================================

      from matplotlib import pyplot  as plt
      slices=[5,10,25,50]
      labels=['eating','sleeping','gaming','studying']
      cols=['y','r','g','b']
      plt.pie(slices,labels=labels,colors=cols,startangle=90,shadow=True,explode=(0.5,0.3,0,0),autopct='%1.1f%%')
      plt.title('pie chart')
      plt.show()
-----------------------------------------------------------------------------------------------------

working with multiple plot
============================================

      from matplotlib import pyplot  as plt
      import numpy as np

      t1=np.arange(0.0,5.0,0.1)
      t2=np.arange(0.0,5.0,0.1)
      #print (t2)

      plt.subplot(221) #plt.subplot(nrows, ncols, index, **kwargs)
      plt.plot(t1,t2)

      plt.subplot(222)
      plt.plot(t1,t2)

      plt.subplot(224)
      plt.plot(t1,t2)

      plt.show()
--------------------------------------------------------------------------------------------------------------------
