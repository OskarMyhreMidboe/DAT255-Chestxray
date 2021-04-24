# DAT255-Chestxray
Using FastAI to predict COVID-19 on chestxray dataset: https://github.com/ieee8023/covid-chestxray-dataset


## The idea
I used a RESNET34 model to try and differentiate the diffrence between pasients with COVID-19 and healthy patients or patients with other lung-type infections/viruses.

## Methods
I tried to use progressive resizing, freezing and unfreezing the model in training and finding the optimal learning rate compared to loss.

## Problems underways
### The CSV-file
The CSV-file provided contained some elements that didn't link to any pictures which caused some problems in the begining. I tried to fix the issue with some code but since it was just 23 entries that needed editing i just edited the CSV-file myself, which worked splendid.
### Dataset
The dataset contained 3 different type of x-rays; forward-facing, side-facing and above-layerd. This is represented in the top-losses so the optimal solution here would be to remove the side-facing and above-layerd pictures as they were a minotiry and just work with the front-faced ones. But as i started late on the project i found no time to do this.
### Model not predicting well on the unseesn data
My model did not work as well as hoped, in fact it missed-predicted on about half of the pictures i fed it. I think if i had tweaked the dataset as mentioned above, or just chose a different better datset like this one: https://www.kaggle.com/tawsifurrahman/covid19-radiography-database i would end up with a better model.
