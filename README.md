ENVEROMRNT SETUP:
Evaluate various libraries for returning structured LLM output
    
Install the python 3.13.3 version :
 

https://www.python.org � downloads � python-3.13.3

 

Libraries
 
Langchain
instructor
Pydantic
Guardrails AI (guardrails-ai)
jsonformer	
structured-llm	

 Langchain :
 
 pip install langchain

Instructor:
 
 pip install instructor

Pydantic :
 
 pip install pydantic

Guardrails:
 
 pip install Guardrails

jsonformer:
 
 pip install jsonformer

structured-llm:

pip install structured-llm
 



#### Windows

1. Download the `.exe` installer.
2. Check ? **Add Python to PATH** during installation.
3. Run:

   ```run in cmd
   python --version
   ```

#### Ubuntu

``` run in cmd
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt update
sudo apt install python3.13 python3.13-venv python3.13-dev
python3.13 --version
```

#### macOS

1. Install Homebrew if not available:

   ```run in cmd
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```
2. Then:

   ```run in cmd
   brew install python@3.13
   python3.13 --version
   ```
---

### Step 2: Create a Virtual Environment

```run in cmd
python3.13 -m venv llm-env
source llm-env/bin/activate      # macOS/Linux
llm-env\Scripts\activate         # Windows
```
---

### Step 3: Install Required Libraries

```bash
pip install langchain instructor pydantic guardrails-ai jsonformer structured-llm
```
---

##  Library Descriptions

### 1. LangChain

* Framework to build LLM-powered apps.
* Supports memory, chaining, agents, and structured outputs using `pydantic` schemas.
* Supports OpenAI, HuggingFace, and local models.

 Example:

```python
from langchain.output_parsers import PydanticOutputParser
```

---

###  2. Instructor

* OpenAI function-calling wrapper using **Pydantic** models.
* Helps retrieve LLM outputs as structured Python objects.

 Example:

```python
from instructor import patch
from pydantic import BaseModel
```

---

### 3. Pydantic

* Python library for data validation using type hints.
* Used by other tools to validate and enforce structure in LLM outputs.

 Example:

```python
from pydantic import BaseModel

```

---

###  4. Guardrails AI

* Define rules and constraints for LLM outputs.
* Supports validation, transformation, and re-prompting using YAML or Python.


---

### 5. jsonformer

* Generates JSON from transformers using **schema-guided decoding**.
* Enforces structure during generation (not post-processing).
* Great for streaming structured outputs.

 Use with:

```python
from jsonformer.main import Jsonformer
```

---

### 6. structured-llm

* Lightweight library for getting structured outputs using OpenAI or Anthropic.
* Uses JSON schemas with auto-validation.

 Example:

```python
from structured_llm import OpenAIStructuredGenerator
```

---

## Final Test

Test if all libraries are correctly installed:

```bash
python -c "import langchain, instructor, pydantic, guardrails, jsonformer, structured_llm; print('All imports successful')"
```
---
