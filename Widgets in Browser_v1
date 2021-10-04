#!/usr/bin/env python
# coding: utf-8

# In[1]:


import warnings
warnings.filterwarnings('ignore')

import ipywidgets as widgets
from IPython.display import display, clear_output


# In[ ]:


#!jupyter nbextension enable --py widgetsnbextension --sys-prefix
#!jupyter serverextension enable voila --sys-prefix


# In[23]:


# Image Widget
file = open("D:\AIM 29th March2021\Pic_example.jfif", "rb")
image = file.read()

image_headline=widgets.Image(
               value=image,
               format='jfif',
               width='300' 
            )
label_headline=widgets.Label(
                  value='Aim toolkit cover',
                  style={'description_width': 'initial'}
            )
vbox_headline=widgets.VBox([image_headline,label_headline])                        


# In[12]:


# Team Mate Name
grand = widgets.ToggleButtons(
        options=['Steve_jobs','Bill_gates']
)


# In[13]:


# Name
name=widgets.Text(placeholder = 'Your name here')


# In[14]:


# Date
date = widgets.DatePicker(description='Chose the demo date') 


# In[15]:


# Number of people presetn for Demo
Demo_team = widgets.IntSlider(
                value=3, # default
                min=0,
                max=15,
                step=1,
                style={'description_width':'initial','handle_color':'#16a085'}
         )


# In[16]:


# Button to send
Send_button =widgets.Button(
            description='Send to Business',
            tooltip='Send',
            style={'description_width':'initial'}
        )
output=widgets.Output()

def on_button_clicked(event):
    with output:
        clear_output()
        print("Sent message: ")
        print(f"Hello Business Heads! This is the development lead {grand.value},{name.value}")
        print(f"we are presenting the demo on {date.value} about AIM_toolkit, is that okay with you!")
        print(f"Also, if you do not mind, I will bring my dev team of {Demo_team.value} members for this demo!")
Send_button.on_click(on_button_clicked)

vbox_result=widgets.VBox([Send_button,output])


# In[17]:


# stacked right hand side
text_0 = widgets.HTML(value="<h1>Hello Business Heads!</h1>")
text_1 = widgets.HTML(value="<h2>This is the development lead</h2>")
text_2 = widgets.HTML(value="<h2>we are presenting the demo on</h2>")
text_3 = widgets.HTML(value="<h2>about AIM_toolkit, is that okay with you!</h2>")
text_4 = widgets.HTML(value="<h2>Also, if you do not mind, I will bring my dev team of </h2>")
text_5 = widgets.HTML(value="<h2>for this demo!</h2>")

vbox_text=widgets.VBox([text_0,text_1,grand,name,text_2,date,text_3,text_4,Demo_team,text_5,vbox_result])


# In[24]:


page=widgets.HBox([vbox_headline,vbox_text])
display(page)


# In[25]:


get_ipython().system('pip freeze >requirements.txt')


# In[ ]:




