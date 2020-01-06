# Steg for å klargjøre din maskin til ELMED219

Her er en oppskrift du kan følge dersom du ønsker å bruke din egen maskin under ELMED219. Alternativt kan du bruke f.eks. [Google Colab](https://colab.research.google.com/) eller [Deepnote](https://www.deepnote.com); mer informasjon om disse kommer.
#test

## Anaconda
Vi anbefaler at du installerer Python via [Anaconda Distribution](https://www.anaconda.com/distribution). Pass på å velge "Python 3.7 version. Vi skal bruke Conda Package Management System, som kommer med Anaconda Distribution. Fra [dokumentasjonen](https://conda.io/docs):
> Conda is an open source package management system and environment management system that runs on Windows, macOS and Linux. Conda quickly installs, runs and updates packages and their dependencies. Conda easily creates, saves, loads and switches between environments on your local computer. 

Etter installasjonen kjør `python --version` i et terminalvindu (i "Anaconda Prompt" om du bruker Windows). Hvis output inneholder "Python 3.7" og "Anaconda" er du klar for neste steg.

## GitHub
Koden i kurset er hostet på kode-delingsplattformen GitHub (der du leser dette). Hvis du ikke allerede har en GitHub-konto bør du opprette en konto nå. Vi anbefaler at du bruker plattformen for dine egne prosjekter i løpet av kurset. https://github.com/join.

## Kaggle
[Kaggle](https://www.kaggle.com) er et online felleskap av "data scientists" som arrangerer data science-konkurranser og hoster en stor samling datasett. Kursprosjektet i ELMED219 vil organiseres på Kaggle. Opprett en konto her: https://www.kaggle.com. 

## Installer og test kurs-omgivelsene

Etter at du har installert Anaconda gå gjennom følgende steg (hvis du bruker Windows, bruk "Anaconda Prompt").

### Installer Git
```bash
conda install git
```
### Last ned repositoriet: 
```bash
git clone https://github.com/MMIV-ML/ELMED219-2020
cd ELMED219-2020
```
### Konfigurer Python-omgivelsene
```bash
conda env update
```

### Aktiver omgivelsene:
```bash
conda activate elmed219
```
Hvis du bruker Linux eller MacOS og kommandoen over feiler, skriv 
```bash 
source ~/.bash_profile
``` 
og forsøk `conda activate elmed219` igjen. Hvis dette feiler, aktiver omgivelsene ved å skrive `source activate elmed219` istedenfor.

### Installer en Jupyter kernel
```bash
python -m ipykernel install --user --name elmed219 --display-name "ELMED219"
```

### Test din installasjon
Gå gjennom notebooken `0.0-test.ipynb` i `notebooks`-katalogen:
```bash
cd notebooks
jupyter notebook
```
Du kan også bruke [JupyterLab](https://github.com/jupyterlab/jupyterlab): `jupyter lab`.

## Oppdater
Koden og omgivelsene oppdateres underveis i kurset. Kjør følgende kommandoer regelmessig:
* Update code: `git pull`
* Update environment: 
```bash
conda activate elmed219
conda env update
```

# Troubleshooting
