# Respiratory Audio Analysis
Classify person as healthy and unhealthy based on respiratory audio sounds.

## Dataset
The Respiratory Sound database was originally compiled to support the scientific challenge organized at Int. Conf. on Biomedical Health Informatics - ICBHI 2017. The current version of this database is made freely available for research and contains both the public and the private dataset of the ICBHI challenge.

The Respiratory Sound Database contains audio samples, collected independently by two research teams in two different countries, over several years. Most of the database consists of audio samples recorded by the School of Health Sciences, University of Aveiro (ESSUA) research team at the Respiratory Research and Rehabilitation Laboratory (Lab3R), ESSUA and at Hospital Infante D. Pedro, Aveiro, Portugal. The second research team, from the Aristotle University of Thessaloniki (AUTH) and the University of Coimbra (UC), acquired respiratory sounds at the Papanikolaou General Hospital, Thessaloniki and at the General Hospital of Imathia (Health Unit of Naousa), Greece.

Link: https://bhichallenge.med.auth.gr/

The demographic info file has 6 columns:
  - Patient number
  - Age
  - Sex
  - Adult BMI (kg/m2)
  - Child Weight (kg)
  - Child Height (cm)
  - 
Each audio file name is divided into 5 elements, separated with underscores (_).
1. Patient number (101,102,...,226)
2. Recording index
3. Chest location 
      a. Trachea (Tc)
      b. Anterior left (Al)
      c. Anterior right (Ar)
      d. Posterior left (Pl)
      e. Posterior right (Pr)
      f. Lateral left (Ll)
      g. Lateral right (Lr)
4. Acquisition mode 
     a. sequential/single channel (sc), 
     b. simultaneous/multichannel (mc)
5. Recording equipment 
     a. AKG C417L Microphone (AKGC417L), 
     b. 3M Littmann Classic II SE Stethoscope (LittC2SE), 
     c. 3M Litmmann 3200 Electronic Stethoscope (Litt3200), 
     d.  WelchAllyn Meditron Master Elite Electronic Stethoscope (Meditron)

The annotation text files have four columns:
- Beginning of respiratory cycle(s)
- End of respiratory cycle(s)
- Presence/absence of crackles (presence=1, absence=0)
- Presence/absence of wheezes (presence=1, absence=0)

The abbreviations used in the diagnosis file are:
- COPD: Chronic Obstructive Pulmonary Disease
- LRTI: Lower Respiratory Tract Infection
- URTI: Upper Respiratory Tract Infection

## Methodology
Librosa python package for music and audio analysis is used to extract features from the audio files which are later used for training the classifiers.


## Results
Four classifiers are applied to the dataset
1. Logistic Regression
2. Decision Tree
3. SVM
4. Simple Neural Network

The classifiers yielded the following performances

![image](https://user-images.githubusercontent.com/59551550/149991595-47687123-d7a4-4845-afa9-60dbce3cda5b.png)

Logistic Regression: 99.15254237288136

Decision Tree: 100.0

SVM: 98.58757062146893

Neural Network: 98.87005686759949
