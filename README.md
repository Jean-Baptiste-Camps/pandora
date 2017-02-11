pandora
==========

A Tagger-Lemmatizer for Latin


### Install

For now, installation needs to be done by pulling the repository and installing the required libraries yourself.

#### Environment free

*Note* : if you have CUDA installed, you should do `pip install -r requirements-gpu.txt` instead

```bash
git clone https://github.com/hipster-philology/pandora.git
cd pandora
pip install -r requirements.txt
```

#### Virtualenv

**For CUDA-Ready machines owner**:

```bash
git clone https://github.com/hipster-philology/pandora.git
cd pandora
virtualenv env
source env/bin/activate
pip install -r requirements-gpu.txt
```

**For the others**:

```bash
git clone https://github.com/hipster-philology/pandora.git
cd pandora
virtualenv env
source env/bin/activate
pip install -r requirements.txt
```

### Scripts

*Note* : with Virtualenv install, do not forget to do `source env/bin/activate`.

#### main.py

`main.py` allows you to train your own models :

```bash
python main.py --help
python main.py config.txt --dev /path/to/dev/resources --train /path/to/train/resources
python main.py config.txt --dev /path/to/dev/resources --train /path/to/train/resources --nb_epochs 1
```

#### unseen.py

`unseen.py` allows you to annotate a string or folder

```bash
python unseen.py --help
python unseen.py path/to/model/dir --string --input "Cur in theatrum, Cato severe, venisti?"
python unseen.py path/to/model/dir --input /path/to/dir/to/annotate/ --output /path/to/output/dir/
python unseen.py path/to/model/dir --tokenized_input --input /path/to/dir/to/annotate/ --output /path/to/output/dir/ 
```
