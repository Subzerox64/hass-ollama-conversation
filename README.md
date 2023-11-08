# Ollama Conversation

The Ollama integration adds a conversation agent powered by [Ollama][ollama] in Home Assistant.

This conversation agent is unable to control your house. The Ollama conversation agent can be used in automations, but not as a [sentence trigger][sentence-trigger]. It can only query information that has been provided by Home Assistant. To be able to answer questions about your house, Home Assistant will need to provide Ollama with the details of your house, which include areas, devices and their states.

## Installation

To install the __Ollama Conversation__ integration to your Home Assistant instance, use this My button:

[![Open your Home Assistant instance and open a repository inside the Home Assistant Community Store.](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=ej52&repository=hass-ollama-conversation&category=integration)

#### Manual Insallation
If the above My button doesn’t work, you can also perform the following steps manually:

* Browse to your Home Assistant instance.
* Go to HACS > Integrations > Custom Repositories.
* Add custom repository.
  * Repository is `ej52/hass-ollama-conversation`.
  * Category is `Integration`.
* Click ___Explore & Download Repositories___.
* From the list, select Ollama Conversation.
* In the bottom right corner, click the ___Download___ button.
* Follow the instructions on screen to complete the installation.

#### Note:
HACS does not "configure" the integration for you, You must add Ollama Conversation after installing via HACS.

* Browse to your Home Assistant instance.
* Go to Settings > Devices & Services.
* In the bottom right corner, select the ___Add Integration___ button.
* From the list, select Ollama Conversation.
* Follow the instructions on screen to complete the setup.

## Options
Options for Ollama Conversation can be set via the user interface, by taking the following steps:

* Browse to your Home Assistant instance.
* Go to Settings > Devices & Services.
* If multiple instances of Ollama Conversation are configured, choose the instance you want to configure.
* Select the integration, then select ___Configure___.


| Option                   | Description                                                                                                                                                                                                         |
| ------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Prompt Template          | The starting text for the AI language model to generate new text from. This text can include information about your Home Assistant instance, devices, and areas and is written using Home Assistant Templating. |
| Completion Model         | The model used to generate response.                                                                                                                                                                                |
| Context Size             | Sets the size of the context window used to generate the next token.                                                                                                                                                |
| Maximum Tokens           | The maximum number of words or “tokens” that the AI model should generate in its completion of the prompt.                                                                                                          |
| Temperature              | The temperature of the model. A higher value (e.g., 0.95) will lead to more unexpected results, while a lower value (e.g. 0.5) will be more deterministic results.                                              |
| Top K                    | Reduces the probability of generating nonsense. A higher value (e.g. 100) will give more diverse answers, while a lower value (e.g. 10) will be more conservative.                                              |
| Top P                    | Works together with top-k. A higher value (e.g., 0.95) will lead to more diverse text, while a lower value (e.g., 0.5) will generate more focused and conservative text.                                        |


## Contributions are welcome!

If you want to contribute to this please read the [Contribution guidelines](CONTRIBUTING.md)

### Discussions
Discussions for this integration over on [Home Assistant Community][discussions]

***

[ollama]: https://ollama.ai/
[ollama-github]: https://github.com/jmorganca/ollama
[sentence-trigger]: https://www.home-assistant.io/docs/automation/trigger/#sentence-trigger
