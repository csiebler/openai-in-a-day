# OpenAI in a day

*This technical workshop will provide an introduction to OpenAI and an overview of Azure OpenAI Studio. Participants will be prompted to complete engineering exercises and use OpenAI to access company data. They will also learn about embedding solution accelerators and prototyping one use case from start to finish. The workshop will conclude with a Q&A and wrap-up.*

## Agenda

### 🌅 Morning (9:00 – 12:00)

> *Fokus: Introduction and first steps*

* Intro (90min)
  * 📣 Intro OpenAI (45mins)
  * 📣 Azure OpenAI Studio (45mins)
* 🧑🏼‍💻 Prompt Engineering Exercises (90mins)
  * OpenAI cookbook examples (30min)
  * Extendes examples on slides (60min)

### 🌆 Afternoon (1:00 – 4:30)

> *Fokus: Solutions*

* 📣 Using OpenAI to access company data (45min)
  * How to bring your own data
  * Fine-tuning, embedding
  * Solutions Call Center, Q&A
* Customer Solutions Insights / Best Practices (30min)
* FAQ (30min)
* 💻 Presentation of embeddings solution accelerator (30min)
* 💻 Prototyping one use case (start generic, then embeddings scenario) from start to finish (60min)
  * Use case architecture
  * Data acquisition
  * Data clearning
  * Prompt engineering
  * Testing
  * Productization
    * ResponsibleAI
    * DevOps practices
    * Best practices

## Preparation

## OpenAI subscription and deployments

* Create an OpenAI account
* Create 'text-davinci-003' and 'text-embedding-ada-002' deployments

### Devcontainer / Codespaces

For usage of devcontainer make sure:

#### Codespaces

* Go to Github repository and click on `Code` button
* Edit the `credentials.env` file including OpenAI endpoint and key before starting any notebooks

#### Devcontainer

* Install [Docker](https://www.docker.com/products/docker-desktop)
* Install [Visual Studio Code](https://code.visualstudio.com/)
* Install [Remote - Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) extension
* Clone this repository
* Open the repository in Visual Studio Code
* Click on the green button in the bottom left corner of the window
* Select `Reopen in Container`
* Wait for the container to be built and started
* Edit `credentials.env` file including OpenAI endpoint and key before starting any notebooks

### Bring your own "Anaconda"

Make sure you have the requirements installed in your Python environment using `pip install -r requirements.txt`.
