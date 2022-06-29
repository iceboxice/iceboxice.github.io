June 27, 2022  

Welcome to the wonderful world of widgets.  
==========================================

Today's widget is a guide on how to allow guests to interact with Jupyter Notebook files <em>in situ</em>.

STEPS  
1. print modules versions needed for the environment
2. paste output into created "requirements.txt" file
3. upload both .txt and .ipynb files to repository
4. use mybinder.org to link/use repository with JupyterLab
5. copy-paste generated launch-binder-SVG-button embed link to share  

# STEP 1 example
```python
# import environment modules
import ipywidgets
import seaborn
import matplotlib.pyplot

print('\n'.join(f'{m.__name__}=={m.__version__}' for m in globals().values() if getattr(m, '__version__', None)))
```
Example Output  

![image](https://user-images.githubusercontent.com/105950393/175803193-fbe4bb8e-ff26-4d57-b980-b283194e6a98.png)  


# STEP 4    
<img src="https://user-images.githubusercontent.com/105950393/175803135-64c09980-486e-444b-86f3-489b14b527aa.png" height="800" />


# STEP 5 example  
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/iceboxice/binder/main)

<ins>Reference</ins>  
<https://stackoverflow.com/questions/40428931/package-for-listing-version-of-packages-used-in-a-jupyter-notebook>
<https://www.youtube.com/watch?v=owSGVOov9pQ>
