## Чтобы все работало пришлось доработать задание:
- Поставить более низкие версии компонентов python, rasa и SQLAlchemy.
- Использовать команду: rasa run --enable-api -vv --cors "*"
- Обучить ассистента более качественно используя 1000 epoch.


## Скриншоты проверочного общения с ботом
<details>
  
<summary>Скриншоты</summary>

![](https://github.com/Boropwnz/architecture-sprint-5/blob/rasa/src/Result/1.jpg)
![](https://github.com/Boropwnz/architecture-sprint-5/blob/rasa/src/Result/2.jpg)
![](https://github.com/Boropwnz/architecture-sprint-5/blob/rasa/src/Result/3.jpg)

</details>

## Лог работы сервера rasa

<details>
  
<summary>Весь лог</summary>
  
```
(rasaenv) PS S:\Software Architecture\Yandex Practice\5_Task_In\architecture-sprint-5\src> rasa run --enable-api -vv --cors "*"
s:\software architecture\yandex practice\5_task_in\architecture-sprint-5\src\rasaenv\lib\site-packages\rasa\shared\utils\validation.py:134: DeprecationWarning: pkg_resources is deprecated as an API. See https://setuptools.pypa.io/en/latest/pkg_resources.html
  import pkg_resources
s:\software architecture\yandex practice\5_task_in\architecture-sprint-5\src\rasaenv\lib\site-packages\pkg_resources\__init__.py:3117: DeprecationWarning: Deprecated call to `pkg_resources.declare_namespace('mpl_toolkits')`.
Implementing implicit namespace packages (as specified in PEP 420) is preferred to `pkg_resources.declare_namespace`. See https://setuptools.pypa.io/en/latest/references/keywords.html#keyword-namespace-packages
  declare_namespace(pkg)
s:\software architecture\yandex practice\5_task_in\architecture-sprint-5\src\rasaenv\lib\site-packages\pkg_resources\__init__.py:3117: DeprecationWarning: Deprecated call to `pkg_resources.declare_namespace('ruamel')`.
Implementing implicit namespace packages (as specified in PEP 420) is preferred to `pkg_resources.declare_namespace`. See https://setuptools.pypa.io/en/latest/references/keywords.html#keyword-namespace-packages
  declare_namespace(pkg)
2025-04-13 22:28:44 DEBUG    rasa.cli.utils  - Parameter 'credentials' not set. Using default location 'credentials.yml' instead.
s:\software architecture\yandex practice\5_task_in\architecture-sprint-5\src\rasaenv\lib\site-packages\sanic_cors\extension.py:39: DeprecationWarning: distutils Version classes are deprecated. Use packaging.version instead.
  SANIC_VERSION = LooseVersion(sanic_version)
2025-04-13 22:28:46 DEBUG    h5py._conv  - Creating converter from 7 to 5
2025-04-13 22:28:46 DEBUG    h5py._conv  - Creating converter from 5 to 7
2025-04-13 22:28:46 DEBUG    h5py._conv  - Creating converter from 7 to 5
2025-04-13 22:28:46 DEBUG    h5py._conv  - Creating converter from 5 to 7
2025-04-13 22:28:46 DEBUG    jax._src.path  - etils.epath was not found. Using pathlib for file I/O.
s:\software architecture\yandex practice\5_task_in\architecture-sprint-5\src\rasaenv\lib\site-packages\tensorflow\lite\python\util.py:52: DeprecationWarning: jax.xla_computation is deprecated. Please use the AOT APIs.
  from jax import xla_computation as _xla_computation
2025-04-13 22:28:48 DEBUG    rasa.core.utils  - Available web server routes:
/conversations/<conversation_id:path>/messages     POST                           add_message
/conversations/<conversation_id:path>/tracker/events POST                           append_events
/webhooks/rasa                                     GET                            custom_webhook_RasaChatInput.health
/webhooks/rasa/webhook                             POST                           custom_webhook_RasaChatInput.receive
/webhooks/rest                                     GET                            custom_webhook_RestInput.health
/webhooks/rest/webhook                             POST                           custom_webhook_RestInput.receive
/model/test/intents                                POST                           evaluate_intents
/model/test/stories                                POST                           evaluate_stories
/conversations/<conversation_id:path>/execute      POST                           execute_action
/domain                                            GET                            get_domain
/                                                  GET                            hello
/model                                             PUT                            load_model
/model/parse                                       POST                           parse
/conversations/<conversation_id:path>/predict      POST                           predict
/conversations/<conversation_id:path>/tracker/events PUT                            replace_events
/conversations/<conversation_id:path>/story        GET                            retrieve_story
/conversations/<conversation_id:path>/tracker      GET                            retrieve_tracker
/status                                            GET                            status
/model/predict                                     POST                           tracker_predict
/model/train                                       POST                           train
/conversations/<conversation_id:path>/trigger_intent POST                           trigger_intent
/model                                             DELETE                         unload_model
/version                                           GET                            version
2025-04-13 22:28:48 INFO     root  - Starting Rasa server on http://0.0.0.0:5005
2025-04-13 22:28:48 DEBUG    rasa.core.utils  - Using the default number of Sanic workers (1).
s:\software architecture\yandex practice\5_task_in\architecture-sprint-5\src\rasaenv\lib\site-packages\rasa\shared\core\slot_mappings.py:224: UserWarning: Slot auto-fill has been removed in 3.0 and replaced with a new explicit mechanism to set slots. Please refer to https://rasa.com/docs/rasa/domain#slots to learn more.
  rasa.shared.utils.io.raise_warning(
2025-04-13 22:28:48 DEBUG    rasa.telemetry  - Skipping telemetry reporting: no license hash found.
2025-04-13 22:28:48 DEBUG    rasa.core.tracker_store  - Connected to InMemoryTrackerStore.
2025-04-13 22:28:48 DEBUG    rasa.core.lock_store  - Connected to lock store 'InMemoryLockStore'.
2025-04-13 22:28:48 DEBUG    rasa.core.nlg.generator  - Instantiated NLG to 'TemplatedNaturalLanguageGenerator'.
2025-04-13 22:28:48 INFO     rasa.core.processor  - Loading model models\20250413-222817-chunky-bracket.tar.gz...
2025-04-13 22:28:48 DEBUG    rasa.engine.storage.local_model_storage  - Extracted model to 'C:\Users\Boromir\AppData\Local\Temp\tmpyf0mfhrm'.
2025-04-13 22:28:48 DEBUG    rasa.engine.graph  - Node 'nlu_message_converter' loading 'NLUMessageConverter.load' and kwargs: '{}'.
2025-04-13 22:28:48 DEBUG    rasa.engine.graph  - Node 'run_WhitespaceTokenizer0' loading 'WhitespaceTokenizer.load' and kwargs: '{}'.
2025-04-13 22:28:48 DEBUG    rasa.engine.graph  - Node 'run_RegexFeaturizer1' loading 'RegexFeaturizer.load' and kwargs: '{}'.
2025-04-13 22:28:48 DEBUG    rasa.engine.storage.local_model_storage  - Resource 'train_RegexFeaturizer1' was requested for reading.
2025-04-13 22:28:48 DEBUG    rasa.engine.graph  - Node 'run_LexicalSyntacticFeaturizer2' loading 'LexicalSyntacticFeaturizer.load' and kwargs: '{}'.
2025-04-13 22:28:48 DEBUG    rasa.engine.storage.local_model_storage  - Resource 'train_LexicalSyntacticFeaturizer2' was requested for reading.
2025-04-13 22:28:48 DEBUG    rasa.engine.graph  - Node 'run_CountVectorsFeaturizer3' loading 'CountVectorsFeaturizer.load' and kwargs: '{}'.
2025-04-13 22:28:48 DEBUG    rasa.engine.storage.local_model_storage  - Resource 'train_CountVectorsFeaturizer3' was requested for reading.
2025-04-13 22:28:48 DEBUG    rasa.engine.graph  - Node 'run_LanguageModelFeaturizer4' loading 'LanguageModelFeaturizer.load' and kwargs: '{}'.
2025-04-13 22:28:49 DEBUG    rasa.nlu.featurizers.dense_featurizer.lm_featurizer  - Loading Tokenizer and Model for bert
2025-04-13 22:28:49 DEBUG    urllib3.connectionpool  - Starting new HTTPS connection (1): huggingface.co:443
2025-04-13 22:28:49 DEBUG    urllib3.connectionpool  - https://huggingface.co:443 "HEAD /bert-base-cased/resolve/main/tokenizer_config.json HTTP/1.1" 200 0
2025-04-13 22:28:49 DEBUG    urllib3.connectionpool  - https://huggingface.co:443 "HEAD /bert-base-cased/resolve/main/config.json HTTP/1.1" 200 0
Some weights of the PyTorch model were not used when initializing the TF 2.0 model TFBertModel: ['cls.predictions.transform.dense.weight', 'cls.predictions.transform.LayerNorm.weight', 'cls.predictions.transform.LayerNorm.bias', 'cls.seq_relationship.weight', 'cls.predictions.transform.dense.bias', 'cls.seq_relationship.bias', 'cls.predictions.bias']
- This IS expected if you are initializing TFBertModel from a PyTorch model trained on another task or with another architecture (e.g. initializing a TFBertForSequenceClassification model from a BertForPreTraining model).
- This IS NOT expected if you are initializing TFBertModel from a PyTorch model that you expect to be exactly identical (e.g. initializing a TFBertForSequenceClassification model from a BertForSequenceClassification model).
All the weights of TFBertModel were initialized from the PyTorch model.
If your task is similar to the task the model of the checkpoint was trained on, you can already use TFBertModel for predictions without further training.
2025-04-13 22:28:50 DEBUG    rasa.engine.graph  - Node 'run_DIETClassifier5' loading 'DIETClassifier.load' and kwargs: '{}'.
2025-04-13 22:28:50 DEBUG    rasa.engine.storage.local_model_storage  - Resource 'train_DIETClassifier5' was requested for reading.
2025-04-13 22:28:50 DEBUG    rasa.utils.tensorflow.models  - Loading the model from C:\Users\Boromir\AppData\Local\Temp\tmpu2sw_1g7\train_DIETClassifier5\DIETClassifier.tf_model with finetune_mode=False...
2025-04-13 22:28:50 DEBUG    rasa.nlu.classifiers.diet_classifier  - You specified 'DIET' to train entities, but no entities are present in the training data. Skipping training of entities.
2025-04-13 22:28:50 DEBUG    rasa.nlu.classifiers.diet_classifier  - Following metrics will be logged during training:
2025-04-13 22:28:50 DEBUG    rasa.nlu.classifiers.diet_classifier  -   t_loss (total loss)
2025-04-13 22:28:50 DEBUG    rasa.nlu.classifiers.diet_classifier  -   i_acc (intent acc)
2025-04-13 22:28:50 DEBUG    rasa.nlu.classifiers.diet_classifier  -   i_loss (intent loss)
2025-04-13 22:28:56 DEBUG    rasa.utils.tensorflow.models  - Finished loading the model.
s:\software architecture\yandex practice\5_task_in\architecture-sprint-5\src\rasaenv\lib\site-packages\rasa\utils\train_utils.py:530: UserWarning: constrain_similarities is set to `False`. It is recommended to set it to `True` when using cross-entropy loss.
  rasa.shared.utils.io.raise_warning(
2025-04-13 22:28:56 DEBUG    rasa.engine.graph  - Node 'run_EntitySynonymMapper6' loading 'EntitySynonymMapper.load' and kwargs: '{}'.
2025-04-13 22:28:56 DEBUG    rasa.engine.storage.local_model_storage  - Resource 'train_EntitySynonymMapper6' was requested for reading.
2025-04-13 22:28:56 DEBUG    rasa.nlu.extractors.entity_synonyms  - Failed to load ABCMeta from model storage. Resource 'train_EntitySynonymMapper6' doesn't exist.
2025-04-13 22:28:56 DEBUG    rasa.engine.graph  - Node 'run_ResponseSelector7' loading 'ResponseSelector.load' and kwargs: '{}'.
2025-04-13 22:28:56 DEBUG    rasa.engine.storage.local_model_storage  - Resource 'train_ResponseSelector7' was requested for reading.
2025-04-13 22:28:56 DEBUG    rasa.nlu.classifiers.diet_classifier  - Failed to load ABCMeta from model storage. Resource 'train_ResponseSelector7' doesn't exist.
2025-04-13 22:28:56 DEBUG    rasa.engine.storage.local_model_storage  - Resource 'train_ResponseSelector7' was requested for reading.
2025-04-13 22:28:56 DEBUG    rasa.nlu.selectors.response_selector  - Failed to load ResponseSelector from model storage. Resource 'train_ResponseSelector7' doesn't exist.
2025-04-13 22:28:56 DEBUG    rasa.engine.graph  - Node 'run_RegexMessageHandler' loading 'RegexMessageHandler.load' and kwargs: '{}'.
2025-04-13 22:28:56 DEBUG    rasa.engine.graph  - Node 'domain_provider' loading 'DomainProvider.load' and kwargs: '{}'.
2025-04-13 22:28:56 DEBUG    rasa.engine.storage.local_model_storage  - Resource 'domain_provider' was requested for reading.
s:\software architecture\yandex practice\5_task_in\architecture-sprint-5\src\rasaenv\lib\site-packages\rasa\shared\core\slot_mappings.py:224: UserWarning: Slot auto-fill has been removed in 3.0 and replaced with a new explicit mechanism to set slots. Please refer to https://rasa.com/docs/rasa/domain#slots to learn more.
  rasa.shared.utils.io.raise_warning(
2025-04-13 22:28:56 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' loading 'MemoizationPolicy.load' and kwargs: '{}'.
2025-04-13 22:28:56 DEBUG    rasa.engine.storage.local_model_storage  - Resource 'train_MemoizationPolicy0' was requested for reading.
2025-04-13 22:28:56 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' loading 'RulePolicy.load' and kwargs: '{}'.
2025-04-13 22:28:56 DEBUG    rasa.engine.storage.local_model_storage  - Resource 'train_RulePolicy1' was requested for reading.
2025-04-13 22:28:56 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' loading 'TEDPolicy.load' and kwargs: '{}'.
2025-04-13 22:28:56 DEBUG    rasa.engine.storage.local_model_storage  - Resource 'train_TEDPolicy2' was requested for reading.
2025-04-13 22:28:56 DEBUG    rasa.utils.tensorflow.models  - Loading the model from C:\Users\Boromir\AppData\Local\Temp\tmpu2sw_1g7\train_TEDPolicy2\ted_policy.tf_model with finetune_mode=False...
2025-04-13 22:29:03 DEBUG    rasa.utils.tensorflow.models  - Finished loading the model.
2025-04-13 22:29:03 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' loading 'RuleOnlyDataProvider.load' and kwargs: '{}'.
2025-04-13 22:29:03 DEBUG    rasa.engine.storage.local_model_storage  - Resource 'train_RulePolicy1' was requested for reading.
2025-04-13 22:29:03 DEBUG    rasa.engine.graph  - Node 'select_prediction' loading 'DefaultPolicyPredictionEnsemble.load' and kwargs: '{}'.
2025-04-13 22:29:03 INFO     root  - Rasa server is up and running.
2025-04-13 22:29:03 INFO     root  - Enabling coroutine debugging. Loop id 2429022932320.
2025-04-13 22:29:19 DEBUG    rasa.core.lock_store  - Issuing ticket for conversation 'PractikumStudent'.
2025-04-13 22:29:19 DEBUG    rasa.core.lock_store  - Acquiring lock for conversation 'PractikumStudent'.
2025-04-13 22:29:19 DEBUG    rasa.core.lock_store  - Acquired lock for conversation 'PractikumStudent'.
2025-04-13 22:29:19 DEBUG    rasa.core.tracker_store  - Could not find tracker for conversation ID 'PractikumStudent'.
2025-04-13 22:29:19 DEBUG    rasa.core.tracker_store  - No event broker configured. Skipping streaming events.
2025-04-13 22:29:19 DEBUG    rasa.core.processor  - Starting a new session for conversation ID 'PractikumStudent'.
2025-04-13 22:29:19 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[]
2025-04-13 22:29:19 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=action_session_start rasa_events=[<rasa.shared.core.events.SessionStarted object at 0x00000235B6EEBBB0>, ActionExecuted(action: action_listen, policy: None, confidence: None)]
2025-04-13 22:29:19 DEBUG    rasa.core.processor  - [debug    ] processor.slots.log            slot_values=     topic: None
        session_started_metadata: None
2025-04-13 22:29:19 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__message__': [<rasa.core.channels.channel.UserMessage object at 0x00000235B6E76280>], '__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x00000235AFD8AEE0>}, targets: ['run_RegexMessageHandler'] and ExecutionContext(model_id='90a3e5012afd48b8ba180ef46c29c727', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-04-13 22:29:19 DEBUG    rasa.engine.graph  - Node 'nlu_message_converter' running 'NLUMessageConverter.convert_user_message'.
2025-04-13 22:29:19 DEBUG    rasa.engine.graph  - Node 'run_WhitespaceTokenizer0' running 'WhitespaceTokenizer.process'.
2025-04-13 22:29:19 DEBUG    rasa.engine.graph  - Node 'run_RegexFeaturizer1' running 'RegexFeaturizer.process'.
2025-04-13 22:29:19 DEBUG    rasa.engine.graph  - Node 'run_LexicalSyntacticFeaturizer2' running 'LexicalSyntacticFeaturizer.process'.
2025-04-13 22:29:19 DEBUG    rasa.engine.graph  - Node 'run_CountVectorsFeaturizer3' running 'CountVectorsFeaturizer.process'.
2025-04-13 22:29:19 DEBUG    rasa.engine.graph  - Node 'run_LanguageModelFeaturizer4' running 'LanguageModelFeaturizer.process'.
2025-04-13 22:29:19 DEBUG    rasa.engine.graph  - Node 'run_DIETClassifier5' running 'DIETClassifier.process'.
2025-04-13 22:29:19 DEBUG    rasa.engine.graph  - Node 'run_EntitySynonymMapper6' running 'EntitySynonymMapper.process'.
2025-04-13 22:29:19 DEBUG    rasa.engine.graph  - Node 'run_ResponseSelector7' running 'ResponseSelector.process'.
2025-04-13 22:29:19 DEBUG    rasa.nlu.classifiers.diet_classifier  - There is no trained model for 'ResponseSelector': The component is either not trained or didn't receive enough training data.
2025-04-13 22:29:19 DEBUG    rasa.nlu.selectors.response_selector  - Adding following selector key to message property: default
2025-04-13 22:29:19 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-04-13 22:29:19 DEBUG    rasa.engine.graph  - Node 'run_RegexMessageHandler' running 'RegexMessageHandler.process'.
2025-04-13 22:29:19 DEBUG    rasa.core.processor  - [debug    ] processor.message.parse        parse_data_entities=[] parse_data_intent={'name': 'deny', 'confidence': 0.22197797894477844} parse_data_text=привет
2025-04-13 22:29:19 DEBUG    rasa.core.processor  - Logged UserUtterance - tracker now has 4 events.
2025-04-13 22:29:19 DEBUG    rasa.core.actions.action  - Validating extracted slots: topic
2025-04-13 22:29:19 DEBUG    rasa.core.processor  - [debug    ] processor.extract.slots        action_extract_slot=action_extract_slots len_extraction_events=1 rasa_events=[SlotSet(key: topic, value: привет)]
2025-04-13 22:29:19 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x00000235AFD8AEE0>}, targets: ['select_prediction'] and ExecutionContext(model_id='90a3e5012afd48b8ba180ef46c29c727', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-04-13 22:29:19 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-04-13 22:29:19 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-04-13 22:29:19 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-04-13 22:29:19 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{}, {'user': {'intent': 'deny'}, 'prev_action': {'action_name': 'action_listen'}}]
2025-04-13 22:29:19 DEBUG    rasa.core.policies.memoization  - There is no memorised next action
2025-04-13 22:29:19 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-04-13 22:29:19 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user text: привет | previous action name: action_listen
2025-04-13 22:29:19 DEBUG    rasa.core.policies.rule_policy  - There is no applicable rule.
2025-04-13 22:29:19 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: deny | previous action name: action_listen
2025-04-13 22:29:19 DEBUG    rasa.core.policies.rule_policy  - There is no applicable rule.
2025-04-13 22:29:19 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-04-13 22:29:19 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'utter_architecture_response' based on user intent.
2025-04-13 22:29:19 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-04-13 22:29:19 DEBUG    rasa.core.policies.ensemble  - Made prediction using user intent.
2025-04-13 22:29:19 DEBUG    rasa.core.policies.ensemble  - Added `DefinePrevUserUtteredFeaturization(False)` event.
2025-04-13 22:29:19 DEBUG    rasa.core.policies.ensemble  - Predicted next action using TEDPolicy.
2025-04-13 22:29:19 DEBUG    rasa.core.processor  - Predicted next action 'utter_architecture_response' with confidence 0.71.
2025-04-13 22:29:19 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[<rasa.shared.core.events.DefinePrevUserUtteredFeaturization object at 0x00000235B6EFEC40>]
2025-04-13 22:29:19 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=utter_architecture_response rasa_events=[BotUttered('Архитектура ПО включает выбор структур, которые обеспечивают масштабируемость, гибкость и поддерживаемость приложения. Задайте конкретный вопрос по этой теме, и я помогу вам с информацией.', {"elements": null, "quick_replies": null, "buttons": null, "attachment": null, "image": null, "custom": null}, {"utter_action": "utter_architecture_response"}, 1744572559.7770076)]
2025-04-13 22:29:19 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x00000235AFD8AEE0>}, targets: ['select_prediction'] and ExecutionContext(model_id='90a3e5012afd48b8ba180ef46c29c727', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-04-13 22:29:19 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-04-13 22:29:19 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-04-13 22:29:19 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-04-13 22:29:19 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'deny'}, 'prev_action': {'action_name': 'action_listen'}}, {'user': {'intent': 'deny'}, 'prev_action': {'action_name': 'utter_architecture_response'}}]
2025-04-13 22:29:19 DEBUG    rasa.core.policies.memoization  - There is no memorised next action
2025-04-13 22:29:19 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-04-13 22:29:19 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: deny | previous action name: action_listen
[state 2] user intent: deny | previous action name: utter_architecture_response
2025-04-13 22:29:19 DEBUG    rasa.core.policies.rule_policy  - There is no applicable rule.
2025-04-13 22:29:19 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-04-13 22:29:19 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'action_listen' based on user intent.
2025-04-13 22:29:19 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-04-13 22:29:19 DEBUG    rasa.core.policies.ensemble  - Predicted next action using TEDPolicy.
2025-04-13 22:29:19 DEBUG    rasa.core.processor  - Predicted next action 'action_listen' with confidence 0.93.
2025-04-13 22:29:19 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[]
2025-04-13 22:29:19 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=action_listen rasa_events=[]
2025-04-13 22:29:19 DEBUG    rasa.core.tracker_store  - No event broker configured. Skipping streaming events.
2025-04-13 22:29:19 DEBUG    rasa.core.lock_store  - Deleted lock for conversation 'PractikumStudent'.
2025-04-13 22:29:32 DEBUG    rasa.core.lock_store  - Issuing ticket for conversation 'PractikumStudent'.
2025-04-13 22:29:32 DEBUG    rasa.core.lock_store  - Acquiring lock for conversation 'PractikumStudent'.
2025-04-13 22:29:32 DEBUG    rasa.core.lock_store  - Acquired lock for conversation 'PractikumStudent'.
2025-04-13 22:29:32 DEBUG    rasa.core.tracker_store  - Recreating tracker for id 'PractikumStudent'
2025-04-13 22:29:32 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__message__': [<rasa.core.channels.channel.UserMessage object at 0x00000235AFD8A3A0>], '__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x00000235B47230D0>}, targets: ['run_RegexMessageHandler'] and ExecutionContext(model_id='90a3e5012afd48b8ba180ef46c29c727', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-04-13 22:29:32 DEBUG    rasa.engine.graph  - Node 'nlu_message_converter' running 'NLUMessageConverter.convert_user_message'.
2025-04-13 22:29:32 DEBUG    rasa.engine.graph  - Node 'run_WhitespaceTokenizer0' running 'WhitespaceTokenizer.process'.
2025-04-13 22:29:32 DEBUG    rasa.engine.graph  - Node 'run_RegexFeaturizer1' running 'RegexFeaturizer.process'.
2025-04-13 22:29:32 DEBUG    rasa.engine.graph  - Node 'run_LexicalSyntacticFeaturizer2' running 'LexicalSyntacticFeaturizer.process'.
2025-04-13 22:29:32 DEBUG    rasa.engine.graph  - Node 'run_CountVectorsFeaturizer3' running 'CountVectorsFeaturizer.process'.
2025-04-13 22:29:32 DEBUG    rasa.engine.graph  - Node 'run_LanguageModelFeaturizer4' running 'LanguageModelFeaturizer.process'.
2025-04-13 22:29:33 DEBUG    rasa.engine.graph  - Node 'run_DIETClassifier5' running 'DIETClassifier.process'.
2025-04-13 22:29:33 DEBUG    rasa.engine.graph  - Node 'run_EntitySynonymMapper6' running 'EntitySynonymMapper.process'.
2025-04-13 22:29:33 DEBUG    rasa.engine.graph  - Node 'run_ResponseSelector7' running 'ResponseSelector.process'.
2025-04-13 22:29:33 DEBUG    rasa.nlu.classifiers.diet_classifier  - There is no trained model for 'ResponseSelector': The component is either not trained or didn't receive enough training data.
2025-04-13 22:29:33 DEBUG    rasa.nlu.selectors.response_selector  - Adding following selector key to message property: default
2025-04-13 22:29:33 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-04-13 22:29:33 DEBUG    rasa.engine.graph  - Node 'run_RegexMessageHandler' running 'RegexMessageHandler.process'.
2025-04-13 22:29:33 DEBUG    rasa.core.processor  - [debug    ] processor.message.parse        parse_data_entities=[] parse_data_intent={'name': 'goodbye', 'confidence': 0.2204301506280899} parse_data_text=Привет
2025-04-13 22:29:33 DEBUG    rasa.core.processor  - Logged UserUtterance - tracker now has 10 events.
2025-04-13 22:29:33 DEBUG    rasa.core.actions.action  - Validating extracted slots: topic
2025-04-13 22:29:33 DEBUG    rasa.core.processor  - [debug    ] processor.extract.slots        action_extract_slot=action_extract_slots len_extraction_events=1 rasa_events=[SlotSet(key: topic, value: Привет)]
2025-04-13 22:29:33 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x00000235B47230D0>}, targets: ['select_prediction'] and ExecutionContext(model_id='90a3e5012afd48b8ba180ef46c29c727', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-04-13 22:29:33 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-04-13 22:29:33 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-04-13 22:29:33 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-04-13 22:29:33 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'deny'}, 'prev_action': {'action_name': 'utter_architecture_response'}}, {'user': {'intent': 'goodbye'}, 'prev_action': {'action_name': 'action_listen'}}]
2025-04-13 22:29:33 DEBUG    rasa.core.policies.memoization  - There is no memorised next action
2025-04-13 22:29:33 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-04-13 22:29:33 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: deny | previous action name: action_listen
[state 2] user intent: deny | previous action name: utter_architecture_response
[state 3] user text: Привет | previous action name: action_listen
2025-04-13 22:29:33 DEBUG    rasa.core.policies.rule_policy  - There is no applicable rule.
2025-04-13 22:29:33 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: deny | previous action name: action_listen
[state 2] user intent: deny | previous action name: utter_architecture_response
[state 3] user intent: goodbye | previous action name: action_listen
2025-04-13 22:29:33 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'utter_goodbye'.
2025-04-13 22:29:33 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-04-13 22:29:33 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'utter_goodbye' based on user intent.
2025-04-13 22:29:33 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-04-13 22:29:33 DEBUG    rasa.core.policies.ensemble  - Made prediction using user intent.
2025-04-13 22:29:33 DEBUG    rasa.core.policies.ensemble  - Added `DefinePrevUserUtteredFeaturization(False)` event.
2025-04-13 22:29:33 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-04-13 22:29:33 DEBUG    rasa.core.processor  - Predicted next action 'utter_goodbye' with confidence 1.00.
2025-04-13 22:29:33 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[<rasa.shared.core.events.DefinePrevUserUtteredFeaturization object at 0x00000235B6F01E50>]
2025-04-13 22:29:33 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=utter_goodbye rasa_events=[BotUttered('До свидания! Если появятся вопросы по архитектуре ПО, обращайтесь.', {"elements": null, "quick_replies": null, "buttons": null, "attachment": null, "image": null, "custom": null}, {"utter_action": "utter_goodbye"}, 1744572573.0817199)]
2025-04-13 22:29:33 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x00000235B47230D0>}, targets: ['select_prediction'] and ExecutionContext(model_id='90a3e5012afd48b8ba180ef46c29c727', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-04-13 22:29:33 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-04-13 22:29:33 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-04-13 22:29:33 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-04-13 22:29:33 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'goodbye'}, 'prev_action': {'action_name': 'action_listen'}}, {'user': {'intent': 'goodbye'}, 'prev_action': {'action_name': 'utter_goodbye'}}]
2025-04-13 22:29:33 DEBUG    rasa.core.policies.memoization  - There is a memorised next action 'action_listen'
2025-04-13 22:29:33 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-04-13 22:29:33 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: deny | previous action name: action_listen
[state 2] user intent: deny | previous action name: utter_architecture_response
[state 3] user intent: goodbye | previous action name: action_listen
[state 4] user intent: goodbye | previous action name: utter_goodbye
2025-04-13 22:29:33 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'action_listen'.
2025-04-13 22:29:33 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-04-13 22:29:33 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'action_listen' based on user intent.
2025-04-13 22:29:33 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-04-13 22:29:33 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-04-13 22:29:33 DEBUG    rasa.core.processor  - Predicted next action 'action_listen' with confidence 1.00.
2025-04-13 22:29:33 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[]
2025-04-13 22:29:33 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=action_listen rasa_events=[]
2025-04-13 22:29:33 DEBUG    rasa.core.tracker_store  - No event broker configured. Skipping streaming events.
2025-04-13 22:29:33 DEBUG    rasa.core.lock_store  - Deleted lock for conversation 'PractikumStudent'.
2025-04-13 22:29:37 DEBUG    rasa.core.lock_store  - Issuing ticket for conversation 'PractikumStudent'.
2025-04-13 22:29:37 DEBUG    rasa.core.lock_store  - Acquiring lock for conversation 'PractikumStudent'.
2025-04-13 22:29:37 DEBUG    rasa.core.lock_store  - Acquired lock for conversation 'PractikumStudent'.
2025-04-13 22:29:37 DEBUG    rasa.core.tracker_store  - Recreating tracker for id 'PractikumStudent'
2025-04-13 22:29:37 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__message__': [<rasa.core.channels.channel.UserMessage object at 0x00000235AFD8AEE0>], '__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x00000235B6EEBD30>}, targets: ['run_RegexMessageHandler'] and ExecutionContext(model_id='90a3e5012afd48b8ba180ef46c29c727', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-04-13 22:29:37 DEBUG    rasa.engine.graph  - Node 'nlu_message_converter' running 'NLUMessageConverter.convert_user_message'.
2025-04-13 22:29:37 DEBUG    rasa.engine.graph  - Node 'run_WhitespaceTokenizer0' running 'WhitespaceTokenizer.process'.
2025-04-13 22:29:37 DEBUG    rasa.engine.graph  - Node 'run_RegexFeaturizer1' running 'RegexFeaturizer.process'.
2025-04-13 22:29:37 DEBUG    rasa.engine.graph  - Node 'run_LexicalSyntacticFeaturizer2' running 'LexicalSyntacticFeaturizer.process'.
2025-04-13 22:29:37 DEBUG    rasa.engine.graph  - Node 'run_CountVectorsFeaturizer3' running 'CountVectorsFeaturizer.process'.
2025-04-13 22:29:37 DEBUG    rasa.engine.graph  - Node 'run_LanguageModelFeaturizer4' running 'LanguageModelFeaturizer.process'.
2025-04-13 22:29:37 DEBUG    rasa.engine.graph  - Node 'run_DIETClassifier5' running 'DIETClassifier.process'.
2025-04-13 22:29:37 DEBUG    rasa.engine.graph  - Node 'run_EntitySynonymMapper6' running 'EntitySynonymMapper.process'.
2025-04-13 22:29:37 DEBUG    rasa.engine.graph  - Node 'run_ResponseSelector7' running 'ResponseSelector.process'.
2025-04-13 22:29:37 DEBUG    rasa.nlu.classifiers.diet_classifier  - There is no trained model for 'ResponseSelector': The component is either not trained or didn't receive enough training data.
2025-04-13 22:29:37 DEBUG    rasa.nlu.selectors.response_selector  - Adding following selector key to message property: default
2025-04-13 22:29:37 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-04-13 22:29:37 DEBUG    rasa.engine.graph  - Node 'run_RegexMessageHandler' running 'RegexMessageHandler.process'.
2025-04-13 22:29:37 DEBUG    rasa.core.processor  - [debug    ] processor.message.parse        parse_data_entities=[] parse_data_intent={'name': 'deny', 'confidence': 0.2738727331161499} parse_data_text=Окей
2025-04-13 22:29:37 DEBUG    rasa.core.processor  - Logged UserUtterance - tracker now has 16 events.
2025-04-13 22:29:37 DEBUG    rasa.core.actions.action  - Validating extracted slots: topic
2025-04-13 22:29:37 DEBUG    rasa.core.processor  - [debug    ] processor.extract.slots        action_extract_slot=action_extract_slots len_extraction_events=1 rasa_events=[SlotSet(key: topic, value: Окей)]
2025-04-13 22:29:37 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x00000235B6EEBD30>}, targets: ['select_prediction'] and ExecutionContext(model_id='90a3e5012afd48b8ba180ef46c29c727', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-04-13 22:29:37 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-04-13 22:29:37 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-04-13 22:29:37 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-04-13 22:29:37 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'goodbye'}, 'prev_action': {'action_name': 'utter_goodbye'}}, {'user': {'intent': 'deny'}, 'prev_action': {'action_name': 'action_listen'}}]
2025-04-13 22:29:37 DEBUG    rasa.core.policies.memoization  - There is no memorised next action
2025-04-13 22:29:37 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-04-13 22:29:37 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: deny | previous action name: action_listen
[state 2] user intent: deny | previous action name: utter_architecture_response
[state 3] user intent: goodbye | previous action name: action_listen
[state 4] user intent: goodbye | previous action name: utter_goodbye
[state 5] user text: Окей | previous action name: action_listen
2025-04-13 22:29:37 DEBUG    rasa.core.policies.rule_policy  - There is no applicable rule.
2025-04-13 22:29:37 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: deny | previous action name: action_listen
[state 2] user intent: deny | previous action name: utter_architecture_response
[state 3] user intent: goodbye | previous action name: action_listen
[state 4] user intent: goodbye | previous action name: utter_goodbye
[state 5] user intent: deny | previous action name: action_listen
2025-04-13 22:29:37 DEBUG    rasa.core.policies.rule_policy  - There is no applicable rule.
2025-04-13 22:29:37 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-04-13 22:29:37 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'utter_architecture_response' based on user intent.
2025-04-13 22:29:37 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-04-13 22:29:37 DEBUG    rasa.core.policies.ensemble  - Made prediction using user intent.
2025-04-13 22:29:37 DEBUG    rasa.core.policies.ensemble  - Added `DefinePrevUserUtteredFeaturization(False)` event.
2025-04-13 22:29:37 DEBUG    rasa.core.policies.ensemble  - Predicted next action using TEDPolicy.
2025-04-13 22:29:37 DEBUG    rasa.core.processor  - Predicted next action 'utter_architecture_response' with confidence 0.70.
2025-04-13 22:29:37 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[<rasa.shared.core.events.DefinePrevUserUtteredFeaturization object at 0x00000235B6EEB160>]
2025-04-13 22:29:37 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=utter_architecture_response rasa_events=[BotUttered('Архитектура ПО включает выбор структур, которые обеспечивают масштабируемость, гибкость и поддерживаемость приложения. Задайте конкретный вопрос по этой теме, и я помогу вам с информацией.', {"elements": null, "quick_replies": null, "buttons": null, "attachment": null, "image": null, "custom": null}, {"utter_action": "utter_architecture_response"}, 1744572577.6976264)]
2025-04-13 22:29:37 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x00000235B6EEBD30>}, targets: ['select_prediction'] and ExecutionContext(model_id='90a3e5012afd48b8ba180ef46c29c727', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-04-13 22:29:37 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-04-13 22:29:37 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-04-13 22:29:37 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-04-13 22:29:37 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'deny'}, 'prev_action': {'action_name': 'action_listen'}}, {'user': {'intent': 'deny'}, 'prev_action': {'action_name': 'utter_architecture_response'}}]
2025-04-13 22:29:37 DEBUG    rasa.core.policies.memoization  - There is no memorised next action
2025-04-13 22:29:37 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-04-13 22:29:37 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: deny | previous action name: action_listen
[state 2] user intent: deny | previous action name: utter_architecture_response
[state 3] user intent: goodbye | previous action name: action_listen
[state 4] user intent: goodbye | previous action name: utter_goodbye
[state 5] user intent: deny | previous action name: action_listen
[state 6] user intent: deny | previous action name: utter_architecture_response
2025-04-13 22:29:37 DEBUG    rasa.core.policies.rule_policy  - There is no applicable rule.
2025-04-13 22:29:37 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-04-13 22:29:37 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'action_listen' based on user intent.
2025-04-13 22:29:37 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-04-13 22:29:37 DEBUG    rasa.core.policies.ensemble  - Predicted next action using TEDPolicy.
2025-04-13 22:29:37 DEBUG    rasa.core.processor  - Predicted next action 'action_listen' with confidence 0.93.
2025-04-13 22:29:37 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[]
2025-04-13 22:29:37 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=action_listen rasa_events=[]
2025-04-13 22:29:37 DEBUG    rasa.core.tracker_store  - No event broker configured. Skipping streaming events.
2025-04-13 22:29:37 DEBUG    rasa.core.lock_store  - Deleted lock for conversation 'PractikumStudent'.
2025-04-13 22:29:46 DEBUG    rasa.core.lock_store  - Issuing ticket for conversation 'PractikumStudent'.
2025-04-13 22:29:46 DEBUG    rasa.core.lock_store  - Acquiring lock for conversation 'PractikumStudent'.
2025-04-13 22:29:46 DEBUG    rasa.core.lock_store  - Acquired lock for conversation 'PractikumStudent'.
2025-04-13 22:29:46 DEBUG    rasa.core.tracker_store  - Recreating tracker for id 'PractikumStudent'
2025-04-13 22:29:46 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__message__': [<rasa.core.channels.channel.UserMessage object at 0x00000235AFD8AB80>], '__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x00000235B6E866A0>}, targets: ['run_RegexMessageHandler'] and ExecutionContext(model_id='90a3e5012afd48b8ba180ef46c29c727', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-04-13 22:29:46 DEBUG    rasa.engine.graph  - Node 'nlu_message_converter' running 'NLUMessageConverter.convert_user_message'.
2025-04-13 22:29:46 DEBUG    rasa.engine.graph  - Node 'run_WhitespaceTokenizer0' running 'WhitespaceTokenizer.process'.
2025-04-13 22:29:46 DEBUG    rasa.engine.graph  - Node 'run_RegexFeaturizer1' running 'RegexFeaturizer.process'.
2025-04-13 22:29:46 DEBUG    rasa.engine.graph  - Node 'run_LexicalSyntacticFeaturizer2' running 'LexicalSyntacticFeaturizer.process'.
2025-04-13 22:29:46 DEBUG    rasa.engine.graph  - Node 'run_CountVectorsFeaturizer3' running 'CountVectorsFeaturizer.process'.
2025-04-13 22:29:46 DEBUG    rasa.engine.graph  - Node 'run_LanguageModelFeaturizer4' running 'LanguageModelFeaturizer.process'.
2025-04-13 22:29:46 DEBUG    rasa.engine.graph  - Node 'run_DIETClassifier5' running 'DIETClassifier.process'.
2025-04-13 22:29:46 DEBUG    rasa.engine.graph  - Node 'run_EntitySynonymMapper6' running 'EntitySynonymMapper.process'.
2025-04-13 22:29:46 DEBUG    rasa.engine.graph  - Node 'run_ResponseSelector7' running 'ResponseSelector.process'.
2025-04-13 22:29:46 DEBUG    rasa.nlu.classifiers.diet_classifier  - There is no trained model for 'ResponseSelector': The component is either not trained or didn't receive enough training data.
2025-04-13 22:29:46 DEBUG    rasa.nlu.selectors.response_selector  - Adding following selector key to message property: default
2025-04-13 22:29:46 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-04-13 22:29:46 DEBUG    rasa.engine.graph  - Node 'run_RegexMessageHandler' running 'RegexMessageHandler.process'.
2025-04-13 22:29:46 DEBUG    rasa.core.processor  - [debug    ] processor.message.parse        parse_data_entities=[] parse_data_intent={'name': 'goodbye', 'confidence': 0.2530815303325653} parse_data_text=Пока
2025-04-13 22:29:46 DEBUG    rasa.core.processor  - Logged UserUtterance - tracker now has 22 events.
2025-04-13 22:29:46 DEBUG    rasa.core.actions.action  - Validating extracted slots: topic
2025-04-13 22:29:46 DEBUG    rasa.core.processor  - [debug    ] processor.extract.slots        action_extract_slot=action_extract_slots len_extraction_events=1 rasa_events=[SlotSet(key: topic, value: Пока)]
2025-04-13 22:29:46 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x00000235B6E866A0>}, targets: ['select_prediction'] and ExecutionContext(model_id='90a3e5012afd48b8ba180ef46c29c727', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-04-13 22:29:46 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-04-13 22:29:46 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-04-13 22:29:46 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-04-13 22:29:46 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'deny'}, 'prev_action': {'action_name': 'utter_architecture_response'}}, {'user': {'intent': 'goodbye'}, 'prev_action': {'action_name': 'action_listen'}}]
2025-04-13 22:29:46 DEBUG    rasa.core.policies.memoization  - There is no memorised next action
2025-04-13 22:29:46 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-04-13 22:29:46 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: deny | previous action name: action_listen
[state 2] user intent: deny | previous action name: utter_architecture_response
[state 3] user intent: goodbye | previous action name: action_listen
[state 4] user intent: goodbye | previous action name: utter_goodbye
[state 5] user intent: deny | previous action name: action_listen
[state 6] user intent: deny | previous action name: utter_architecture_response
[state 7] user text: Пока | previous action name: action_listen
2025-04-13 22:29:46 DEBUG    rasa.core.policies.rule_policy  - There is no applicable rule.
2025-04-13 22:29:46 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: deny | previous action name: action_listen
[state 2] user intent: deny | previous action name: utter_architecture_response
[state 3] user intent: goodbye | previous action name: action_listen
[state 4] user intent: goodbye | previous action name: utter_goodbye
[state 5] user intent: deny | previous action name: action_listen
[state 6] user intent: deny | previous action name: utter_architecture_response
[state 7] user intent: goodbye | previous action name: action_listen
2025-04-13 22:29:46 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'utter_goodbye'.
2025-04-13 22:29:46 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-04-13 22:29:46 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'utter_goodbye' based on user intent.
2025-04-13 22:29:46 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-04-13 22:29:46 DEBUG    rasa.core.policies.ensemble  - Made prediction using user intent.
2025-04-13 22:29:46 DEBUG    rasa.core.policies.ensemble  - Added `DefinePrevUserUtteredFeaturization(False)` event.
2025-04-13 22:29:46 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-04-13 22:29:46 DEBUG    rasa.core.processor  - Predicted next action 'utter_goodbye' with confidence 1.00.
2025-04-13 22:29:46 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[<rasa.shared.core.events.DefinePrevUserUtteredFeaturization object at 0x00000235AEC5BFD0>]
2025-04-13 22:29:46 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=utter_goodbye rasa_events=[BotUttered('До свидания! Если появятся вопросы по архитектуре ПО, обращайтесь.', {"elements": null, "quick_replies": null, "buttons": null, "attachment": null, "image": null, "custom": null}, {"utter_action": "utter_goodbye"}, 1744572586.8328137)]
2025-04-13 22:29:46 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x00000235B6E866A0>}, targets: ['select_prediction'] and ExecutionContext(model_id='90a3e5012afd48b8ba180ef46c29c727', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-04-13 22:29:46 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-04-13 22:29:46 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-04-13 22:29:46 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-04-13 22:29:46 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'goodbye'}, 'prev_action': {'action_name': 'action_listen'}}, {'user': {'intent': 'goodbye'}, 'prev_action': {'action_name': 'utter_goodbye'}}]
2025-04-13 22:29:46 DEBUG    rasa.core.policies.memoization  - There is a memorised next action 'action_listen'
2025-04-13 22:29:46 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-04-13 22:29:46 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: deny | previous action name: action_listen
[state 2] user intent: deny | previous action name: utter_architecture_response
[state 3] user intent: goodbye | previous action name: action_listen
[state 4] user intent: goodbye | previous action name: utter_goodbye
[state 5] user intent: deny | previous action name: action_listen
[state 6] user intent: deny | previous action name: utter_architecture_response
[state 7] user intent: goodbye | previous action name: action_listen
[state 8] user intent: goodbye | previous action name: utter_goodbye
2025-04-13 22:29:46 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'action_listen'.
2025-04-13 22:29:46 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-04-13 22:29:46 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'action_listen' based on user intent.
2025-04-13 22:29:46 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-04-13 22:29:46 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-04-13 22:29:46 DEBUG    rasa.core.processor  - Predicted next action 'action_listen' with confidence 1.00.
2025-04-13 22:29:46 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[]
2025-04-13 22:29:46 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=action_listen rasa_events=[]
2025-04-13 22:29:46 DEBUG    rasa.core.tracker_store  - No event broker configured. Skipping streaming events.
2025-04-13 22:29:46 DEBUG    rasa.core.lock_store  - Deleted lock for conversation 'PractikumStudent'.
2025-04-13 22:29:52 DEBUG    rasa.core.lock_store  - Issuing ticket for conversation 'PractikumStudent'.
2025-04-13 22:29:52 DEBUG    rasa.core.lock_store  - Acquiring lock for conversation 'PractikumStudent'.
2025-04-13 22:29:52 DEBUG    rasa.core.lock_store  - Acquired lock for conversation 'PractikumStudent'.
2025-04-13 22:29:52 DEBUG    rasa.core.tracker_store  - Recreating tracker for id 'PractikumStudent'
2025-04-13 22:29:52 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__message__': [<rasa.core.channels.channel.UserMessage object at 0x00000235B5A65880>], '__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x00000235B6E86C70>}, targets: ['run_RegexMessageHandler'] and ExecutionContext(model_id='90a3e5012afd48b8ba180ef46c29c727', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-04-13 22:29:52 DEBUG    rasa.engine.graph  - Node 'nlu_message_converter' running 'NLUMessageConverter.convert_user_message'.
2025-04-13 22:29:52 DEBUG    rasa.engine.graph  - Node 'run_WhitespaceTokenizer0' running 'WhitespaceTokenizer.process'.
2025-04-13 22:29:52 DEBUG    rasa.engine.graph  - Node 'run_RegexFeaturizer1' running 'RegexFeaturizer.process'.
2025-04-13 22:29:52 DEBUG    rasa.engine.graph  - Node 'run_LexicalSyntacticFeaturizer2' running 'LexicalSyntacticFeaturizer.process'.
2025-04-13 22:29:52 DEBUG    rasa.engine.graph  - Node 'run_CountVectorsFeaturizer3' running 'CountVectorsFeaturizer.process'.
2025-04-13 22:29:52 DEBUG    rasa.engine.graph  - Node 'run_LanguageModelFeaturizer4' running 'LanguageModelFeaturizer.process'.
2025-04-13 22:29:52 DEBUG    rasa.engine.graph  - Node 'run_DIETClassifier5' running 'DIETClassifier.process'.
2025-04-13 22:29:52 DEBUG    rasa.engine.graph  - Node 'run_EntitySynonymMapper6' running 'EntitySynonymMapper.process'.
2025-04-13 22:29:52 DEBUG    rasa.engine.graph  - Node 'run_ResponseSelector7' running 'ResponseSelector.process'.
2025-04-13 22:29:52 DEBUG    rasa.nlu.classifiers.diet_classifier  - There is no trained model for 'ResponseSelector': The component is either not trained or didn't receive enough training data.
2025-04-13 22:29:52 DEBUG    rasa.nlu.selectors.response_selector  - Adding following selector key to message property: default
2025-04-13 22:29:52 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-04-13 22:29:52 DEBUG    rasa.engine.graph  - Node 'run_RegexMessageHandler' running 'RegexMessageHandler.process'.
2025-04-13 22:29:52 DEBUG    rasa.core.processor  - [debug    ] processor.message.parse        parse_data_entities=[] parse_data_intent={'name': 'goodbye', 'confidence': 0.3242991268634796} parse_data_text=Досвидания
2025-04-13 22:29:52 DEBUG    rasa.core.processor  - Logged UserUtterance - tracker now has 28 events.
2025-04-13 22:29:52 DEBUG    rasa.core.actions.action  - Validating extracted slots: topic
2025-04-13 22:29:52 DEBUG    rasa.core.processor  - [debug    ] processor.extract.slots        action_extract_slot=action_extract_slots len_extraction_events=1 rasa_events=[SlotSet(key: topic, value: Досвидания)]
2025-04-13 22:29:52 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x00000235B6E86C70>}, targets: ['select_prediction'] and ExecutionContext(model_id='90a3e5012afd48b8ba180ef46c29c727', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-04-13 22:29:52 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-04-13 22:29:52 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-04-13 22:29:52 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-04-13 22:29:52 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'goodbye'}, 'prev_action': {'action_name': 'utter_goodbye'}}, {'user': {'intent': 'goodbye'}, 'prev_action': {'action_name': 'action_listen'}}]
2025-04-13 22:29:52 DEBUG    rasa.core.policies.memoization  - There is no memorised next action
2025-04-13 22:29:52 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-04-13 22:29:52 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: deny | previous action name: action_listen
[state 2] user intent: deny | previous action name: utter_architecture_response
[state 3] user intent: goodbye | previous action name: action_listen
[state 4] user intent: goodbye | previous action name: utter_goodbye
[state 5] user intent: deny | previous action name: action_listen
[state 6] user intent: deny | previous action name: utter_architecture_response
[state 7] user intent: goodbye | previous action name: action_listen
[state 8] user intent: goodbye | previous action name: utter_goodbye
[state 9] user text: Досвидания | previous action name: action_listen
2025-04-13 22:29:52 DEBUG    rasa.core.policies.rule_policy  - There is no applicable rule.
2025-04-13 22:29:52 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: deny | previous action name: action_listen
[state 2] user intent: deny | previous action name: utter_architecture_response
[state 3] user intent: goodbye | previous action name: action_listen
[state 4] user intent: goodbye | previous action name: utter_goodbye
[state 5] user intent: deny | previous action name: action_listen
[state 6] user intent: deny | previous action name: utter_architecture_response
[state 7] user intent: goodbye | previous action name: action_listen
[state 8] user intent: goodbye | previous action name: utter_goodbye
[state 9] user intent: goodbye | previous action name: action_listen
2025-04-13 22:29:52 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'utter_goodbye'.
2025-04-13 22:29:52 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-04-13 22:29:52 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'utter_goodbye' based on user intent.
2025-04-13 22:29:52 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-04-13 22:29:52 DEBUG    rasa.core.policies.ensemble  - Made prediction using user intent.
2025-04-13 22:29:52 DEBUG    rasa.core.policies.ensemble  - Added `DefinePrevUserUtteredFeaturization(False)` event.
2025-04-13 22:29:52 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-04-13 22:29:52 DEBUG    rasa.core.processor  - Predicted next action 'utter_goodbye' with confidence 1.00.
2025-04-13 22:29:52 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[<rasa.shared.core.events.DefinePrevUserUtteredFeaturization object at 0x00000235B6E9FE80>]
2025-04-13 22:29:52 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=utter_goodbye rasa_events=[BotUttered('До свидания! Если появятся вопросы по архитектуре ПО, обращайтесь.', {"elements": null, "quick_replies": null, "buttons": null, "attachment": null, "image": null, "custom": null}, {"utter_action": "utter_goodbye"}, 1744572592.2014866)]
2025-04-13 22:29:52 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x00000235B6E86C70>}, targets: ['select_prediction'] and ExecutionContext(model_id='90a3e5012afd48b8ba180ef46c29c727', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-04-13 22:29:52 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-04-13 22:29:52 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-04-13 22:29:52 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-04-13 22:29:52 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'goodbye'}, 'prev_action': {'action_name': 'action_listen'}}, {'user': {'intent': 'goodbye'}, 'prev_action': {'action_name': 'utter_goodbye'}}]
2025-04-13 22:29:52 DEBUG    rasa.core.policies.memoization  - There is a memorised next action 'action_listen'
2025-04-13 22:29:52 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-04-13 22:29:52 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: deny | previous action name: action_listen
[state 2] user intent: deny | previous action name: utter_architecture_response
[state 3] user intent: goodbye | previous action name: action_listen
[state 4] user intent: goodbye | previous action name: utter_goodbye
[state 5] user intent: deny | previous action name: action_listen
[state 6] user intent: deny | previous action name: utter_architecture_response
[state 7] user intent: goodbye | previous action name: action_listen
[state 8] user intent: goodbye | previous action name: utter_goodbye
[state 9] user intent: goodbye | previous action name: action_listen
[state 10] user intent: goodbye | previous action name: utter_goodbye
2025-04-13 22:29:52 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'action_listen'.
2025-04-13 22:29:52 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-04-13 22:29:52 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'action_listen' based on user intent.
2025-04-13 22:29:52 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-04-13 22:29:52 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-04-13 22:29:52 DEBUG    rasa.core.processor  - Predicted next action 'action_listen' with confidence 1.00.
2025-04-13 22:29:52 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[]
2025-04-13 22:29:52 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=action_listen rasa_events=[]
2025-04-13 22:29:52 DEBUG    rasa.core.tracker_store  - No event broker configured. Skipping streaming events.
2025-04-13 22:29:52 DEBUG    rasa.core.lock_store  - Deleted lock for conversation 'PractikumStudent'.
2025-04-13 22:29:54 DEBUG    rasa.core.lock_store  - Issuing ticket for conversation 'PractikumStudent'.
2025-04-13 22:29:54 DEBUG    rasa.core.lock_store  - Acquiring lock for conversation 'PractikumStudent'.
2025-04-13 22:29:54 DEBUG    rasa.core.lock_store  - Acquired lock for conversation 'PractikumStudent'.
2025-04-13 22:29:54 DEBUG    rasa.core.tracker_store  - Recreating tracker for id 'PractikumStudent'
2025-04-13 22:29:54 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__message__': [<rasa.core.channels.channel.UserMessage object at 0x00000235AFD8AB80>], '__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x00000235B6E86C70>}, targets: ['run_RegexMessageHandler'] and ExecutionContext(model_id='90a3e5012afd48b8ba180ef46c29c727', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-04-13 22:29:54 DEBUG    rasa.engine.graph  - Node 'nlu_message_converter' running 'NLUMessageConverter.convert_user_message'.
2025-04-13 22:29:54 DEBUG    rasa.engine.graph  - Node 'run_WhitespaceTokenizer0' running 'WhitespaceTokenizer.process'.
2025-04-13 22:29:54 DEBUG    rasa.engine.graph  - Node 'run_RegexFeaturizer1' running 'RegexFeaturizer.process'.
2025-04-13 22:29:54 DEBUG    rasa.engine.graph  - Node 'run_LexicalSyntacticFeaturizer2' running 'LexicalSyntacticFeaturizer.process'.
2025-04-13 22:29:54 DEBUG    rasa.engine.graph  - Node 'run_CountVectorsFeaturizer3' running 'CountVectorsFeaturizer.process'.
2025-04-13 22:29:54 DEBUG    rasa.engine.graph  - Node 'run_LanguageModelFeaturizer4' running 'LanguageModelFeaturizer.process'.
2025-04-13 22:29:54 DEBUG    rasa.engine.graph  - Node 'run_DIETClassifier5' running 'DIETClassifier.process'.
2025-04-13 22:29:54 DEBUG    rasa.engine.graph  - Node 'run_EntitySynonymMapper6' running 'EntitySynonymMapper.process'.
2025-04-13 22:29:54 DEBUG    rasa.engine.graph  - Node 'run_ResponseSelector7' running 'ResponseSelector.process'.
2025-04-13 22:29:54 DEBUG    rasa.nlu.classifiers.diet_classifier  - There is no trained model for 'ResponseSelector': The component is either not trained or didn't receive enough training data.
2025-04-13 22:29:54 DEBUG    rasa.nlu.selectors.response_selector  - Adding following selector key to message property: default
2025-04-13 22:29:54 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-04-13 22:29:54 DEBUG    rasa.engine.graph  - Node 'run_RegexMessageHandler' running 'RegexMessageHandler.process'.
2025-04-13 22:29:54 DEBUG    rasa.core.processor  - [debug    ] processor.message.parse        parse_data_entities=[] parse_data_intent={'name': 'goodbye', 'confidence': 0.2204301506280899} parse_data_text=Привет
2025-04-13 22:29:54 DEBUG    rasa.core.processor  - Logged UserUtterance - tracker now has 34 events.
2025-04-13 22:29:54 DEBUG    rasa.core.actions.action  - Validating extracted slots: topic
2025-04-13 22:29:54 DEBUG    rasa.core.processor  - [debug    ] processor.extract.slots        action_extract_slot=action_extract_slots len_extraction_events=1 rasa_events=[SlotSet(key: topic, value: Привет)]
2025-04-13 22:29:54 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x00000235B6E86C70>}, targets: ['select_prediction'] and ExecutionContext(model_id='90a3e5012afd48b8ba180ef46c29c727', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-04-13 22:29:54 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-04-13 22:29:54 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-04-13 22:29:54 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-04-13 22:29:54 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'goodbye'}, 'prev_action': {'action_name': 'utter_goodbye'}}, {'user': {'intent': 'goodbye'}, 'prev_action': {'action_name': 'action_listen'}}]
2025-04-13 22:29:54 DEBUG    rasa.core.policies.memoization  - There is no memorised next action
2025-04-13 22:29:54 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-04-13 22:29:54 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: deny | previous action name: action_listen
[state 2] user intent: deny | previous action name: utter_architecture_response
[state 3] user intent: goodbye | previous action name: action_listen
[state 4] user intent: goodbye | previous action name: utter_goodbye
[state 5] user intent: deny | previous action name: action_listen
[state 6] user intent: deny | previous action name: utter_architecture_response
[state 7] user intent: goodbye | previous action name: action_listen
[state 8] user intent: goodbye | previous action name: utter_goodbye
[state 9] user intent: goodbye | previous action name: action_listen
[state 10] user intent: goodbye | previous action name: utter_goodbye
[state 11] user text: Привет | previous action name: action_listen
2025-04-13 22:29:54 DEBUG    rasa.core.policies.rule_policy  - There is no applicable rule.
2025-04-13 22:29:54 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: deny | previous action name: action_listen
[state 2] user intent: deny | previous action name: utter_architecture_response
[state 3] user intent: goodbye | previous action name: action_listen
[state 4] user intent: goodbye | previous action name: utter_goodbye
[state 5] user intent: deny | previous action name: action_listen
[state 6] user intent: deny | previous action name: utter_architecture_response
[state 7] user intent: goodbye | previous action name: action_listen
[state 8] user intent: goodbye | previous action name: utter_goodbye
[state 9] user intent: goodbye | previous action name: action_listen
[state 10] user intent: goodbye | previous action name: utter_goodbye
[state 11] user intent: goodbye | previous action name: action_listen
2025-04-13 22:29:54 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'utter_goodbye'.
2025-04-13 22:29:54 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-04-13 22:29:54 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'utter_goodbye' based on user intent.
2025-04-13 22:29:54 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-04-13 22:29:54 DEBUG    rasa.core.policies.ensemble  - Made prediction using user intent.
2025-04-13 22:29:54 DEBUG    rasa.core.policies.ensemble  - Added `DefinePrevUserUtteredFeaturization(False)` event.
2025-04-13 22:29:54 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-04-13 22:29:54 DEBUG    rasa.core.processor  - Predicted next action 'utter_goodbye' with confidence 1.00.
2025-04-13 22:29:54 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[<rasa.shared.core.events.DefinePrevUserUtteredFeaturization object at 0x00000235B6E9FC70>]
2025-04-13 22:29:54 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=utter_goodbye rasa_events=[BotUttered('До свидания! Если появятся вопросы по архитектуре ПО, обращайтесь.', {"elements": null, "quick_replies": null, "buttons": null, "attachment": null, "image": null, "custom": null}, {"utter_action": "utter_goodbye"}, 1744572594.7391474)]
2025-04-13 22:29:54 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x00000235B6E86C70>}, targets: ['select_prediction'] and ExecutionContext(model_id='90a3e5012afd48b8ba180ef46c29c727', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-04-13 22:29:54 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-04-13 22:29:54 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-04-13 22:29:54 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-04-13 22:29:54 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'goodbye'}, 'prev_action': {'action_name': 'action_listen'}}, {'user': {'intent': 'goodbye'}, 'prev_action': {'action_name': 'utter_goodbye'}}]
2025-04-13 22:29:54 DEBUG    rasa.core.policies.memoization  - There is a memorised next action 'action_listen'
2025-04-13 22:29:54 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-04-13 22:29:54 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: deny | previous action name: action_listen
[state 2] user intent: deny | previous action name: utter_architecture_response
[state 3] user intent: goodbye | previous action name: action_listen
[state 4] user intent: goodbye | previous action name: utter_goodbye
[state 5] user intent: deny | previous action name: action_listen
[state 6] user intent: deny | previous action name: utter_architecture_response
[state 7] user intent: goodbye | previous action name: action_listen
[state 8] user intent: goodbye | previous action name: utter_goodbye
[state 9] user intent: goodbye | previous action name: action_listen
[state 10] user intent: goodbye | previous action name: utter_goodbye
[state 11] user intent: goodbye | previous action name: action_listen
[state 12] user intent: goodbye | previous action name: utter_goodbye
2025-04-13 22:29:54 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'action_listen'.
2025-04-13 22:29:54 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-04-13 22:29:54 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'action_listen' based on user intent.
2025-04-13 22:29:54 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-04-13 22:29:54 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-04-13 22:29:54 DEBUG    rasa.core.processor  - Predicted next action 'action_listen' with confidence 1.00.
2025-04-13 22:29:54 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[]
2025-04-13 22:29:54 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=action_listen rasa_events=[]
2025-04-13 22:29:54 DEBUG    rasa.core.tracker_store  - No event broker configured. Skipping streaming events.
2025-04-13 22:29:54 DEBUG    rasa.core.lock_store  - Deleted lock for conversation 'PractikumStudent'.
2025-04-13 22:29:58 DEBUG    rasa.core.lock_store  - Issuing ticket for conversation 'PractikumStudent'.
2025-04-13 22:29:58 DEBUG    rasa.core.lock_store  - Acquiring lock for conversation 'PractikumStudent'.
2025-04-13 22:29:58 DEBUG    rasa.core.lock_store  - Acquired lock for conversation 'PractikumStudent'.
2025-04-13 22:29:58 DEBUG    rasa.core.tracker_store  - Recreating tracker for id 'PractikumStudent'
2025-04-13 22:29:58 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__message__': [<rasa.core.channels.channel.UserMessage object at 0x00000235AFD8AFA0>], '__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x00000235AEBC0850>}, targets: ['run_RegexMessageHandler'] and ExecutionContext(model_id='90a3e5012afd48b8ba180ef46c29c727', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-04-13 22:29:58 DEBUG    rasa.engine.graph  - Node 'nlu_message_converter' running 'NLUMessageConverter.convert_user_message'.
2025-04-13 22:29:58 DEBUG    rasa.engine.graph  - Node 'run_WhitespaceTokenizer0' running 'WhitespaceTokenizer.process'.
2025-04-13 22:29:58 DEBUG    rasa.engine.graph  - Node 'run_RegexFeaturizer1' running 'RegexFeaturizer.process'.
2025-04-13 22:29:58 DEBUG    rasa.engine.graph  - Node 'run_LexicalSyntacticFeaturizer2' running 'LexicalSyntacticFeaturizer.process'.
2025-04-13 22:29:58 DEBUG    rasa.engine.graph  - Node 'run_CountVectorsFeaturizer3' running 'CountVectorsFeaturizer.process'.
2025-04-13 22:29:58 DEBUG    rasa.engine.graph  - Node 'run_LanguageModelFeaturizer4' running 'LanguageModelFeaturizer.process'.
2025-04-13 22:29:58 DEBUG    rasa.engine.graph  - Node 'run_DIETClassifier5' running 'DIETClassifier.process'.
2025-04-13 22:29:58 DEBUG    rasa.engine.graph  - Node 'run_EntitySynonymMapper6' running 'EntitySynonymMapper.process'.
2025-04-13 22:29:58 DEBUG    rasa.engine.graph  - Node 'run_ResponseSelector7' running 'ResponseSelector.process'.
2025-04-13 22:29:58 DEBUG    rasa.nlu.classifiers.diet_classifier  - There is no trained model for 'ResponseSelector': The component is either not trained or didn't receive enough training data.
2025-04-13 22:29:58 DEBUG    rasa.nlu.selectors.response_selector  - Adding following selector key to message property: default
2025-04-13 22:29:58 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-04-13 22:29:58 DEBUG    rasa.engine.graph  - Node 'run_RegexMessageHandler' running 'RegexMessageHandler.process'.
2025-04-13 22:29:58 DEBUG    rasa.core.processor  - [debug    ] processor.message.parse        parse_data_entities=[] parse_data_intent={'name': 'greet', 'confidence': 0.20236606895923615} parse_data_text=Здравствуйте
2025-04-13 22:29:58 DEBUG    rasa.core.processor  - Logged UserUtterance - tracker now has 40 events.
2025-04-13 22:29:58 DEBUG    rasa.core.actions.action  - Validating extracted slots: topic
2025-04-13 22:29:58 DEBUG    rasa.core.processor  - [debug    ] processor.extract.slots        action_extract_slot=action_extract_slots len_extraction_events=1 rasa_events=[SlotSet(key: topic, value: Здравствуйте)]
2025-04-13 22:29:58 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x00000235AEBC0850>}, targets: ['select_prediction'] and ExecutionContext(model_id='90a3e5012afd48b8ba180ef46c29c727', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-04-13 22:29:58 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-04-13 22:29:58 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-04-13 22:29:58 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-04-13 22:29:58 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'goodbye'}, 'prev_action': {'action_name': 'utter_goodbye'}}, {'user': {'intent': 'greet'}, 'prev_action': {'action_name': 'action_listen'}}]
2025-04-13 22:29:58 DEBUG    rasa.core.policies.memoization  - There is no memorised next action
2025-04-13 22:29:58 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-04-13 22:29:58 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: deny | previous action name: action_listen
[state 2] user intent: deny | previous action name: utter_architecture_response
[state 3] user intent: goodbye | previous action name: action_listen
[state 4] user intent: goodbye | previous action name: utter_goodbye
[state 5] user intent: deny | previous action name: action_listen
[state 6] user intent: deny | previous action name: utter_architecture_response
[state 7] user intent: goodbye | previous action name: action_listen
[state 8] user intent: goodbye | previous action name: utter_goodbye
[state 9] user intent: goodbye | previous action name: action_listen
[state 10] user intent: goodbye | previous action name: utter_goodbye
[state 11] user intent: goodbye | previous action name: action_listen
[state 12] user intent: goodbye | previous action name: utter_goodbye
[state 13] user text: Здравствуйте | previous action name: action_listen
2025-04-13 22:29:58 DEBUG    rasa.core.policies.rule_policy  - There is no applicable rule.
2025-04-13 22:29:58 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: deny | previous action name: action_listen
[state 2] user intent: deny | previous action name: utter_architecture_response
[state 3] user intent: goodbye | previous action name: action_listen
[state 4] user intent: goodbye | previous action name: utter_goodbye
[state 5] user intent: deny | previous action name: action_listen
[state 6] user intent: deny | previous action name: utter_architecture_response
[state 7] user intent: goodbye | previous action name: action_listen
[state 8] user intent: goodbye | previous action name: utter_goodbye
[state 9] user intent: goodbye | previous action name: action_listen
[state 10] user intent: goodbye | previous action name: utter_goodbye
[state 11] user intent: goodbye | previous action name: action_listen
[state 12] user intent: goodbye | previous action name: utter_goodbye
[state 13] user intent: greet | previous action name: action_listen
2025-04-13 22:29:58 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'utter_greet'.
2025-04-13 22:29:58 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-04-13 22:29:58 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'utter_greet' based on user intent.
2025-04-13 22:29:58 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-04-13 22:29:58 DEBUG    rasa.core.policies.ensemble  - Made prediction using user intent.
2025-04-13 22:29:58 DEBUG    rasa.core.policies.ensemble  - Added `DefinePrevUserUtteredFeaturization(False)` event.
2025-04-13 22:29:58 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-04-13 22:29:58 DEBUG    rasa.core.processor  - Predicted next action 'utter_greet' with confidence 1.00.
2025-04-13 22:29:58 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[<rasa.shared.core.events.DefinePrevUserUtteredFeaturization object at 0x00000235BAEA79D0>]
2025-04-13 22:29:58 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=utter_greet rasa_events=[BotUttered('Привет! Чем могу помочь в области архитектуры программного обеспечения?', {"elements": null, "quick_replies": null, "buttons": null, "attachment": null, "image": null, "custom": null}, {"utter_action": "utter_greet"}, 1744572598.6489527)]
2025-04-13 22:29:58 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x00000235AEBC0850>}, targets: ['select_prediction'] and ExecutionContext(model_id='90a3e5012afd48b8ba180ef46c29c727', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-04-13 22:29:58 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-04-13 22:29:58 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-04-13 22:29:58 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-04-13 22:29:58 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'greet'}, 'prev_action': {'action_name': 'action_listen'}}, {'user': {'intent': 'greet'}, 'prev_action': {'action_name': 'utter_greet'}}]
2025-04-13 22:29:58 DEBUG    rasa.core.policies.memoization  - There is a memorised next action 'action_listen'
2025-04-13 22:29:58 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-04-13 22:29:58 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: deny | previous action name: action_listen
[state 2] user intent: deny | previous action name: utter_architecture_response
[state 3] user intent: goodbye | previous action name: action_listen
[state 4] user intent: goodbye | previous action name: utter_goodbye
[state 5] user intent: deny | previous action name: action_listen
[state 6] user intent: deny | previous action name: utter_architecture_response
[state 7] user intent: goodbye | previous action name: action_listen
[state 8] user intent: goodbye | previous action name: utter_goodbye
[state 9] user intent: goodbye | previous action name: action_listen
[state 10] user intent: goodbye | previous action name: utter_goodbye
[state 11] user intent: goodbye | previous action name: action_listen
[state 12] user intent: goodbye | previous action name: utter_goodbye
[state 13] user intent: greet | previous action name: action_listen
[state 14] user intent: greet | previous action name: utter_greet
2025-04-13 22:29:58 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'action_listen'.
2025-04-13 22:29:58 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-04-13 22:29:58 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'action_listen' based on user intent.
2025-04-13 22:29:58 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-04-13 22:29:58 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-04-13 22:29:58 DEBUG    rasa.core.processor  - Predicted next action 'action_listen' with confidence 1.00.
2025-04-13 22:29:58 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[]
2025-04-13 22:29:58 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=action_listen rasa_events=[]
2025-04-13 22:29:58 DEBUG    rasa.core.tracker_store  - No event broker configured. Skipping streaming events.
2025-04-13 22:29:58 DEBUG    rasa.core.lock_store  - Deleted lock for conversation 'PractikumStudent'.
2025-04-13 22:30:01 DEBUG    rasa.core.lock_store  - Issuing ticket for conversation 'PractikumStudent'.
2025-04-13 22:30:01 DEBUG    rasa.core.lock_store  - Acquiring lock for conversation 'PractikumStudent'.
2025-04-13 22:30:01 DEBUG    rasa.core.lock_store  - Acquired lock for conversation 'PractikumStudent'.
2025-04-13 22:30:01 DEBUG    rasa.core.tracker_store  - Recreating tracker for id 'PractikumStudent'
2025-04-13 22:30:01 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__message__': [<rasa.core.channels.channel.UserMessage object at 0x00000235AFD8AEE0>], '__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x00000235AEBC0850>}, targets: ['run_RegexMessageHandler'] and ExecutionContext(model_id='90a3e5012afd48b8ba180ef46c29c727', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-04-13 22:30:01 DEBUG    rasa.engine.graph  - Node 'nlu_message_converter' running 'NLUMessageConverter.convert_user_message'.
2025-04-13 22:30:01 DEBUG    rasa.engine.graph  - Node 'run_WhitespaceTokenizer0' running 'WhitespaceTokenizer.process'.
2025-04-13 22:30:01 DEBUG    rasa.engine.graph  - Node 'run_RegexFeaturizer1' running 'RegexFeaturizer.process'.
2025-04-13 22:30:01 DEBUG    rasa.engine.graph  - Node 'run_LexicalSyntacticFeaturizer2' running 'LexicalSyntacticFeaturizer.process'.
2025-04-13 22:30:01 DEBUG    rasa.engine.graph  - Node 'run_CountVectorsFeaturizer3' running 'CountVectorsFeaturizer.process'.
2025-04-13 22:30:01 DEBUG    rasa.engine.graph  - Node 'run_LanguageModelFeaturizer4' running 'LanguageModelFeaturizer.process'.
2025-04-13 22:30:01 DEBUG    rasa.engine.graph  - Node 'run_DIETClassifier5' running 'DIETClassifier.process'.
2025-04-13 22:30:01 DEBUG    rasa.engine.graph  - Node 'run_EntitySynonymMapper6' running 'EntitySynonymMapper.process'.
2025-04-13 22:30:01 DEBUG    rasa.engine.graph  - Node 'run_ResponseSelector7' running 'ResponseSelector.process'.
2025-04-13 22:30:01 DEBUG    rasa.nlu.classifiers.diet_classifier  - There is no trained model for 'ResponseSelector': The component is either not trained or didn't receive enough training data.
2025-04-13 22:30:01 DEBUG    rasa.nlu.selectors.response_selector  - Adding following selector key to message property: default
2025-04-13 22:30:01 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-04-13 22:30:01 DEBUG    rasa.engine.graph  - Node 'run_RegexMessageHandler' running 'RegexMessageHandler.process'.
2025-04-13 22:30:01 DEBUG    rasa.core.processor  - [debug    ] processor.message.parse        parse_data_entities=[] parse_data_intent={'name': 'goodbye', 'confidence': 0.2204301506280899} parse_data_text=Привет
2025-04-13 22:30:01 DEBUG    rasa.core.processor  - Logged UserUtterance - tracker now has 46 events.
2025-04-13 22:30:01 DEBUG    rasa.core.actions.action  - Validating extracted slots: topic
2025-04-13 22:30:01 DEBUG    rasa.core.processor  - [debug    ] processor.extract.slots        action_extract_slot=action_extract_slots len_extraction_events=1 rasa_events=[SlotSet(key: topic, value: Привет)]
2025-04-13 22:30:01 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x00000235AEBC0850>}, targets: ['select_prediction'] and ExecutionContext(model_id='90a3e5012afd48b8ba180ef46c29c727', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-04-13 22:30:01 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-04-13 22:30:01 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-04-13 22:30:01 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-04-13 22:30:01 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'greet'}, 'prev_action': {'action_name': 'utter_greet'}}, {'user': {'intent': 'goodbye'}, 'prev_action': {'action_name': 'action_listen'}}]
2025-04-13 22:30:01 DEBUG    rasa.core.policies.memoization  - There is no memorised next action
2025-04-13 22:30:01 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-04-13 22:30:01 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: deny | previous action name: action_listen
[state 2] user intent: deny | previous action name: utter_architecture_response
[state 3] user intent: goodbye | previous action name: action_listen
[state 4] user intent: goodbye | previous action name: utter_goodbye
[state 5] user intent: deny | previous action name: action_listen
[state 6] user intent: deny | previous action name: utter_architecture_response
[state 7] user intent: goodbye | previous action name: action_listen
[state 8] user intent: goodbye | previous action name: utter_goodbye
[state 9] user intent: goodbye | previous action name: action_listen
[state 10] user intent: goodbye | previous action name: utter_goodbye
[state 11] user intent: goodbye | previous action name: action_listen
[state 12] user intent: goodbye | previous action name: utter_goodbye
[state 13] user intent: greet | previous action name: action_listen
[state 14] user intent: greet | previous action name: utter_greet
[state 15] user text: Привет | previous action name: action_listen
2025-04-13 22:30:01 DEBUG    rasa.core.policies.rule_policy  - There is no applicable rule.
2025-04-13 22:30:01 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: deny | previous action name: action_listen
[state 3] user intent: goodbye | previous action name: action_listen
[state 4] user intent: goodbye | previous action name: utter_goodbye
[state 5] user intent: deny | previous action name: action_listen
[state 6] user intent: deny | previous action name: utter_architecture_response
[state 7] user intent: goodbye | previous action name: action_listen
[state 8] user intent: goodbye | previous action name: utter_goodbye
[state 9] user intent: goodbye | previous action name: action_listen
[state 10] user intent: goodbye | previous action name: utter_goodbye
[state 11] user intent: goodbye | previous action name: action_listen
[state 12] user intent: goodbye | previous action name: utter_goodbye
[state 13] user intent: greet | previous action name: action_listen
[state 14] user intent: greet | previous action name: utter_greet
[state 15] user intent: goodbye | previous action name: action_listen
2025-04-13 22:30:01 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'utter_goodbye'.
2025-04-13 22:30:01 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-04-13 22:30:01 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'utter_goodbye' based on user intent.
2025-04-13 22:30:01 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-04-13 22:30:01 DEBUG    rasa.core.policies.ensemble  - Made prediction using user intent.
2025-04-13 22:30:01 DEBUG    rasa.core.policies.ensemble  - Added `DefinePrevUserUtteredFeaturization(False)` event.
2025-04-13 22:30:01 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-04-13 22:30:01 DEBUG    rasa.core.processor  - Predicted next action 'utter_goodbye' with confidence 1.00.
2025-04-13 22:30:01 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[<rasa.shared.core.events.DefinePrevUserUtteredFeaturization object at 0x00000235B3537550>]
2025-04-13 22:30:01 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=utter_goodbye rasa_events=[BotUttered('До свидания! Если появятся вопросы по архитектуре ПО, обращайтесь.', {"elements": null, "quick_replies": null, "buttons": null, "attachment": null, "image": null, "custom": null}, {"utter_action": "utter_goodbye"}, 1744572601.7175171)]
2025-04-13 22:30:01 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x00000235AEBC0850>}, targets: ['select_prediction'] and ExecutionContext(model_id='90a3e5012afd48b8ba180ef46c29c727', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-04-13 22:30:01 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-04-13 22:30:01 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-04-13 22:30:01 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-04-13 22:30:01 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'goodbye'}, 'prev_action': {'action_name': 'action_listen'}}, {'user': {'intent': 'goodbye'}, 'prev_action': {'action_name': 'utter_goodbye'}}]
2025-04-13 22:30:01 DEBUG    rasa.core.policies.memoization  - There is a memorised next action 'action_listen'
2025-04-13 22:30:01 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-04-13 22:30:01 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: deny | previous action name: action_listen
[state 2] user intent: deny | previous action name: utter_architecture_response
[state 3] user intent: goodbye | previous action name: action_listen
[state 4] user intent: goodbye | previous action name: utter_goodbye
[state 6] user intent: deny | previous action name: utter_architecture_response
[state 7] user intent: goodbye | previous action name: action_listen
[state 8] user intent: goodbye | previous action name: utter_goodbye
[state 9] user intent: goodbye | previous action name: action_listen
[state 10] user intent: goodbye | previous action name: utter_goodbye
[state 11] user intent: goodbye | previous action name: action_listen
[state 12] user intent: goodbye | previous action name: utter_goodbye
[state 13] user intent: greet | previous action name: action_listen
[state 14] user intent: greet | previous action name: utter_greet
[state 15] user intent: goodbye | previous action name: action_listen
[state 16] user intent: goodbye | previous action name: utter_goodbye
2025-04-13 22:30:01 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'action_listen'.
2025-04-13 22:30:01 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-04-13 22:30:01 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'action_listen' based on user intent.
2025-04-13 22:30:01 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-04-13 22:30:01 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-04-13 22:30:01 DEBUG    rasa.core.processor  - Predicted next action 'action_listen' with confidence 1.00.
2025-04-13 22:30:01 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[]
2025-04-13 22:30:01 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=action_listen rasa_events=[]
2025-04-13 22:30:01 DEBUG    rasa.core.tracker_store  - No event broker configured. Skipping streaming events.
2025-04-13 22:30:01 DEBUG    rasa.core.lock_store  - Deleted lock for conversation 'PractikumStudent'.
(rasaenv) PS S:\Software Architecture\Yandex Practice\5_Task_In\architecture-sprint-5\src> rasa train nlu
s:\software architecture\yandex practice\5_task_in\architecture-sprint-5\src\rasaenv\lib\site-packages\rasa\shared\utils\validation.py:134: DeprecationWarning: pkg_resources is deprecated as an API. See https://setuptools.pypa.io/en/latest/pkg_resources.html
  import pkg_resources
s:\software architecture\yandex practice\5_task_in\architecture-sprint-5\src\rasaenv\lib\site-packages\pkg_resources\__init__.py:3117: DeprecationWarning: Deprecated call to `pkg_resources.declare_namespace('mpl_toolkits')`.
Implementing implicit namespace packages (as specified in PEP 420) is preferred to `pkg_resources.declare_namespace`. See https://setuptools.pypa.io/en/latest/references/keywords.html#keyword-namespace-packages
  declare_namespace(pkg)
s:\software architecture\yandex practice\5_task_in\architecture-sprint-5\src\rasaenv\lib\site-packages\pkg_resources\__init__.py:3117: DeprecationWarning: Deprecated call to `pkg_resources.declare_namespace('ruamel')`.
Implementing implicit namespace packages (as specified in PEP 420) is preferred to `pkg_resources.declare_namespace`. See https://setuptools.pypa.io/en/latest/references/keywords.html#keyword-namespace-packages
  declare_namespace(pkg)
s:\software architecture\yandex practice\5_task_in\architecture-sprint-5\src\rasaenv\lib\site-packages\tensorflow\lite\python\util.py:52: DeprecationWarning: jax.xla_computation is deprecated. Please use the AOT APIs.
  from jax import xla_computation as _xla_computation
2025-04-13 22:33:04 INFO     rasa.engine.training.hooks  - Restored component 'RegexFeaturizer' from cache.
2025-04-13 22:33:04 INFO     rasa.engine.training.hooks  - Restored component 'LexicalSyntacticFeaturizer' from cache.
2025-04-13 22:33:04 INFO     rasa.engine.training.hooks  - Restored component 'CountVectorsFeaturizer' from cache.
Some weights of the PyTorch model were not used when initializing the TF 2.0 model TFBertModel: ['cls.predictions.transform.LayerNorm.bias', 'cls.predictions.transform.dense.weight', 'cls.predictions.transform.LayerNorm.weight', 'cls.predictions.bias', 'cls.seq_relationship.weight', 'cls.seq_relationship.bias', 'cls.predictions.transform.dense.bias']
- This IS expected if you are initializing TFBertModel from a PyTorch model trained on another task or with another architecture (e.g. initializing a TFBertForSequenceClassification model from a BertForPreTraining model).
- This IS NOT expected if you are initializing TFBertModel from a PyTorch model that you expect to be exactly identical (e.g. initializing a TFBertForSequenceClassification model from a BertForSequenceClassification model).
All the weights of TFBertModel were initialized from the PyTorch model.
If your task is similar to the task the model of the checkpoint was trained on, you can already use TFBertModel for predictions without further training.
2025-04-13 22:33:07 INFO     rasa.engine.training.hooks  - Starting to train component 'DIETClassifier'.
s:\software architecture\yandex practice\5_task_in\architecture-sprint-5\src\rasaenv\lib\site-packages\rasa\utils\train_utils.py:530: UserWarning: constrain_similarities is set to `False`. It is recommended to set it to `True` when using cross-entropy loss.
  rasa.shared.utils.io.raise_warning(
Epochs: 100%|████████████████████████████████████████████████████████████████████████████| 1000/1000 [00:31<00:00, 31.51it/s, t_loss=0.389, i_acc=1]
2025-04-13 22:33:39 INFO     rasa.engine.training.hooks  - Finished training component 'DIETClassifier'.
2025-04-13 22:33:39 INFO     rasa.engine.training.hooks  - Starting to train component 'ResponseSelector'.
2025-04-13 22:33:39 INFO     rasa.nlu.selectors.response_selector  - Retrieval intent parameter was left to its default value. This response selector will be trained on training examples combining all retrieval intents.
2025-04-13 22:33:39 INFO     rasa.engine.training.hooks  - Finished training component 'ResponseSelector'.
2025-04-13 22:33:39 INFO     rasa.engine.training.hooks  - Restored component 'EntitySynonymMapper' from cache.
Your Rasa model is trained and saved at 'models\nlu-20250413-223303-median-axe.tar.gz'.
(rasaenv) PS S:\Software Architecture\Yandex Practice\5_Task_In\architecture-sprint-5\src> rasa train
s:\software architecture\yandex practice\5_task_in\architecture-sprint-5\src\rasaenv\lib\site-packages\rasa\shared\utils\validation.py:134: DeprecationWarning: pkg_resources is deprecated as an API. See https://setuptools.pypa.io/en/latest/pkg_resources.html
  import pkg_resources
s:\software architecture\yandex practice\5_task_in\architecture-sprint-5\src\rasaenv\lib\site-packages\pkg_resources\__init__.py:3117: DeprecationWarImplementing implicit namespace packages (as specified in PEP 420) is preferred to `pkg_resources.declare_namespace`. See https://setuptools.pypa.io/en/latest/references/keywords.html#keyword-namespace-packages
  declare_namespace(pkg)
s:\software architecture\yandex practice\5_task_in\architecture-sprint-5\src\rasaenv\lib\site-packages\pkg_resources\__init__.py:3117: DeprecationWarning: Deprecated call to `pkg_resources.declare_namespace('ruamel')`.
Implementing implicit namespace packages (as specified in PEP 420) is preferred to `pkg_resources.declare_namespace`. See https://setuptools.pypa.io/en/latest/references/keywords.html#keyword-namespace-packages
  declare_namespace(pkg)
2025-04-13 22:35:14 INFO     rasa.cli.train  - Started validating domain and training data...
s:\software architecture\yandex practice\5_task_in\architecture-sprint-5\src\rasaenv\lib\site-packages\tensorflow\lite\python\util.py:52: DeprecationWarning: jax.xla_computation is deprecated. Please use the AOT APIs.
  from jax import xla_computation as _xla_computation
2025-04-13 22:35:16 INFO     rasa.validator  - Validating intents...
s:\software architecture\yandex practice\5_task_in\architecture-sprint-5\src\rasaenv\lib\site-packages\rasa\shared\utils\io.py:99: UserWarning: The intent 'affirm' is not used in any story or rule.
s:\software architecture\yandex practice\5_task_in\architecture-sprint-5\src\rasaenv\lib\site-packages\rasa\shared\utils\io.py:99: UserWarning: The intent 'deny' is not used in any story or rule.
2025-04-13 22:35:16 INFO     rasa.validator  - Validating uniqueness of intents and stories...
2025-04-13 22:35:16 INFO     rasa.validator  - Validating utterances...
s:\software architecture\yandex practice\5_task_in\architecture-sprint-5\src\rasaenv\lib\site-packages\rasa\shared\utils\io.py:99: UserWarning: The utterance 'utter_acknowledge' is not used in any story or rule.
s:\software architecture\yandex practice\5_task_in\architecture-sprint-5\src\rasaenv\lib\site-packages\rasa\shared\utils\io.py:99: UserWarning: The utterance 'default' is not used in any story or rule.
2025-04-13 22:35:16 INFO     rasa.validator  - Story structure validation...
Processed story blocks: 100%|█████████████████████████████████████████████████████████████████████████| 3/3 [00:00<00:00, 2997.36it/s, # trackers=1]
2025-04-13 22:35:16 INFO     rasa.core.training.story_conflict  - Considering all preceding turns for conflict analysis.
2025-04-13 22:35:16 INFO     rasa.validator  - No story structure conflicts found.
2025-04-13 22:35:18 INFO     rasa.engine.training.hooks  - Restored component 'RegexFeaturizer' from cache.
2025-04-13 22:35:18 INFO     rasa.engine.training.hooks  - Restored component 'LexicalSyntacticFeaturizer' from cache.
2025-04-13 22:35:18 INFO     rasa.engine.training.hooks  - Restored component 'CountVectorsFeaturizer' from cache.
Some weights of the PyTorch model were not used when initializing the TF 2.0 model TFBertModel: ['cls.predictions.transform.dense.bias', 'cls.predictions.bias', 'cls.predictions.transform.dense.weight', 'cls.seq_relationship.bias', 'cls.predictions.transform.LayerNorm.bias', 'cls.predictions.transform.LayerNorm.weight', 'cls.seq_relationship.weight']
- This IS expected if you are initializing TFBertModel from a PyTorch model trained on another task or with another architecture (e.g. initializing a TFBertForSequenceClassification model from a BertForPreTraining model).
- This IS NOT expected if you are initializing TFBertModel from a PyTorch model that you expect to be exactly identical (e.g. initializing a TFBertForSequenceClassification model from a BertForSequenceClassification model).
All the weights of TFBertModel were initialized from the PyTorch model.
If your task is similar to the task the model of the checkpoint was trained on, you can already use TFBertModel for predictions without further training.
2025-04-13 22:35:22 INFO     rasa.engine.training.hooks  - Starting to train component 'DIETClassifier'.
s:\software architecture\yandex practice\5_task_in\architecture-sprint-5\src\rasaenv\lib\site-packages\rasa\utils\train_utils.py:530: UserWarning: constrain_similarities is set to `False`. It is recommended to set it to `True` when using cross-entropy loss.
  rasa.shared.utils.io.raise_warning(
Epochs: 100%|████████████████████████████████████████████████████████████████████████████| 1000/1000 [00:30<00:00, 32.56it/s, t_loss=0.349, i_acc=1]
2025-04-13 22:35:53 INFO     rasa.engine.training.hooks  - Finished training component 'DIETClassifier'.
2025-04-13 22:35:53 INFO     rasa.engine.training.hooks  - Starting to train component 'ResponseSelector'.
2025-04-13 22:35:53 INFO     rasa.nlu.selectors.response_selector  - Retrieval intent parameter was left to its default value. This response selector will be trained on training examples combining all retrieval intents.
2025-04-13 22:35:53 INFO     rasa.engine.training.hooks  - Finished training component 'ResponseSelector'.
Processed story blocks: 100%|█████████████████████████████████████████████████████████████████████████| 3/3 [00:00<00:00, 3000.22it/s, # trackers=1]
Processed story blocks: 100%|█████████████████████████████████████████████████████████████████████████| 3/3 [00:00<00:00, 2995.22it/s, # trackers=3]
Processed story blocks: 100%|█████████████████████████████████████████████████████████████████████████| 3/3 [00:00<00:00, 750.01it/s, # trackers=12]
Processed story blocks: 100%|█████████████████████████████████████████████████████████████████████████| 3/3 [00:00<00:00, 230.76it/s, # trackers=39]
Processed rules: 100%|████████████████████████████████████████████████████████████████████████████████| 4/4 [00:00<00:00, 3299.35it/s, # trackers=1]
2025-04-13 22:35:53 INFO     rasa.engine.training.hooks  - Starting to train component 'TEDPolicy'.
Processed trackers: 100%|█████████████████████████████████████████████████████████████████████████| 120/120 [00:00<00:00, 10908.94it/s, # action=18]
Epochs: 100%|█████████████████████████████████████████████████████████████████| 1000/1000 [00:28<00:00, 34.91it/s, t_loss=0.177, loss=0.0251, acc=1]
2025-04-13 22:36:22 INFO     rasa.engine.training.hooks  - Finished training component 'TEDPolicy'.
2025-04-13 22:36:22 INFO     rasa.engine.training.hooks  - Restored component 'EntitySynonymMapper' from cache.
2025-04-13 22:36:22 INFO     rasa.engine.training.hooks  - Restored component 'MemoizationPolicy' from cache.
2025-04-13 22:36:22 INFO     rasa.engine.training.hooks  - Restored component 'RulePolicy' from cache.
Your Rasa model is trained and saved at 'models\20250413-223517-uniform-aroma.tar.gz'.
(rasaenv) PS S:\Software Architecture\Yandex Practice\5_Task_In\architecture-sprint-5\src> rasa run --enable-api -vv --cors "*"
s:\software architecture\yandex practice\5_task_in\architecture-sprint-5\src\rasaenv\lib\site-packages\rasa\shared\utils\validation.py:134: DeprecationWarning: pkg_resources is deprecated as an API. See https://setuptools.pypa.io/en/latest/pkg_resources.html
  import pkg_resources
s:\software architecture\yandex practice\5_task_in\architecture-sprint-5\src\rasaenv\lib\site-packages\pkg_resources\__init__.py:3117: DeprecationWarning: Deprecated call to `pkg_resources.declare_namespace('mpl_toolkits')`.
Implementing implicit namespace packages (as specified in PEP 420) is preferred to `pkg_resources.declare_namespace`. See https://setuptools.pypa.io/en/latest/references/keywords.html#keyword-namespace-packages
  declare_namespace(pkg)
s:\software architecture\yandex practice\5_task_in\architecture-sprint-5\src\rasaenv\lib\site-packages\pkg_resources\__init__.py:3117: DeprecationWarning: Deprecated call to `pkg_resources.declare_namespace('ruamel')`.
Implementing implicit namespace packages (as specified in PEP 420) is preferred to `pkg_resources.declare_namespace`. See https://setuptools.pypa.io/en/latest/references/keywords.html#keyword-namespace-packages
  declare_namespace(pkg)
2025-04-13 22:37:07 DEBUG    rasa.cli.utils  - Parameter 'credentials' not set. Using default location 'credentials.yml' instead.
s:\software architecture\yandex practice\5_task_in\architecture-sprint-5\src\rasaenv\lib\site-packages\sanic_cors\extension.py:39: DeprecationWarning: distutils Version classes are deprecated. Use packaging.version instead.
  SANIC_VERSION = LooseVersion(sanic_version)
2025-04-13 22:37:09 DEBUG    h5py._conv  - Creating converter from 7 to 5
2025-04-13 22:37:09 DEBUG    h5py._conv  - Creating converter from 5 to 7
2025-04-13 22:37:09 DEBUG    h5py._conv  - Creating converter from 7 to 5
2025-04-13 22:37:09 DEBUG    h5py._conv  - Creating converter from 5 to 7
2025-04-13 22:37:09 DEBUG    jax._src.path  - etils.epath was not found. Using pathlib for file I/O.
s:\software architecture\yandex practice\5_task_in\architecture-sprint-5\src\rasaenv\lib\site-packages\tensorflow\lite\python\util.py:52: DeprecationWarning: jax.xla_computation is deprecated. Please use the AOT APIs.
  from jax import xla_computation as _xla_computation
2025-04-13 22:37:10 DEBUG    rasa.core.utils  - Available web server routes:
/conversations/<conversation_id:path>/messages     POST                           add_message
/conversations/<conversation_id:path>/tracker/events POST                           append_events
/webhooks/rasa                                     GET                            custom_webhook_RasaChatInput.health
/webhooks/rasa/webhook                             POST                           custom_webhook_RasaChatInput.receive
/webhooks/rest                                     GET                            custom_webhook_RestInput.health
/webhooks/rest/webhook                             POST                           custom_webhook_RestInput.receive
/model/test/intents                                POST                           evaluate_intents
/model/test/stories                                POST                           evaluate_stories
/conversations/<conversation_id:path>/execute      POST                           execute_action
/domain                                            GET                            get_domain
/                                                  GET                            hello
/model                                             PUT                            load_model
/model/parse                                       POST                           parse
/conversations/<conversation_id:path>/predict      POST                           predict
/conversations/<conversation_id:path>/tracker/events PUT                            replace_events
/conversations/<conversation_id:path>/story        GET                            retrieve_story
/conversations/<conversation_id:path>/tracker      GET                            retrieve_tracker
/status                                            GET                            status
/model/predict                                     POST                           tracker_predict
/model/train                                       POST                           train
/conversations/<conversation_id:path>/trigger_intent POST                           trigger_intent
/model                                             DELETE                         unload_model
/version                                           GET                            version
2025-04-13 22:37:10 INFO     root  - Starting Rasa server on http://0.0.0.0:5005
2025-04-13 22:37:10 DEBUG    rasa.core.utils  - Using the default number of Sanic workers (1).
s:\software architecture\yandex practice\5_task_in\architecture-sprint-5\src\rasaenv\lib\site-packages\rasa\shared\core\slot_mappings.py:224: UserWarning: Slot auto-fill has been removed in 3.0 and replaced with a new explicit mechanism to set slots. Please refer to https://rasa.com/docs/rasa/domain#slots to learn more.
  rasa.shared.utils.io.raise_warning(
2025-04-13 22:37:11 DEBUG    rasa.telemetry  - Skipping telemetry reporting: no license hash found.
2025-04-13 22:37:11 DEBUG    rasa.core.tracker_store  - Connected to InMemoryTrackerStore.
2025-04-13 22:37:11 DEBUG    rasa.core.lock_store  - Connected to lock store 'InMemoryLockStore'.
2025-04-13 22:37:11 DEBUG    rasa.core.nlg.generator  - Instantiated NLG to 'TemplatedNaturalLanguageGenerator'.
2025-04-13 22:37:11 INFO     rasa.core.processor  - Loading model models\20250413-223517-uniform-aroma.tar.gz...
2025-04-13 22:37:11 DEBUG    rasa.engine.storage.local_model_storage  - Extracted model to 'C:\Users\Boromir\AppData\Local\Temp\tmp5_8wu2bj'.
2025-04-13 22:37:11 DEBUG    rasa.engine.graph  - Node 'nlu_message_converter' loading 'NLUMessageConverter.load' and kwargs: '{}'.
2025-04-13 22:37:11 DEBUG    rasa.engine.graph  - Node 'run_WhitespaceTokenizer0' loading 'WhitespaceTokenizer.load' and kwargs: '{}'.
2025-04-13 22:37:11 DEBUG    rasa.engine.graph  - Node 'run_RegexFeaturizer1' loading 'RegexFeaturizer.load' and kwargs: '{}'.
2025-04-13 22:37:11 DEBUG    rasa.engine.storage.local_model_storage  - Resource 'train_RegexFeaturizer1' was requested for reading.
2025-04-13 22:37:11 DEBUG    rasa.engine.graph  - Node 'run_LexicalSyntacticFeaturizer2' loading 'LexicalSyntacticFeaturizer.load' and kwargs: '{}'.
2025-04-13 22:37:11 DEBUG    rasa.engine.storage.local_model_storage  - Resource 'train_LexicalSyntacticFeaturizer2' was requested for reading.
2025-04-13 22:37:11 DEBUG    rasa.engine.graph  - Node 'run_CountVectorsFeaturizer3' loading 'CountVectorsFeaturizer.load' and kwargs: '{}'.
2025-04-13 22:37:11 DEBUG    rasa.engine.storage.local_model_storage  - Resource 'train_CountVectorsFeaturizer3' was requested for reading.
2025-04-13 22:37:11 DEBUG    rasa.engine.graph  - Node 'run_LanguageModelFeaturizer4' loading 'LanguageModelFeaturizer.load' and kwargs: '{}'.
2025-04-13 22:37:12 DEBUG    rasa.nlu.featurizers.dense_featurizer.lm_featurizer  - Loading Tokenizer and Model for bert
2025-04-13 22:37:12 DEBUG    urllib3.connectionpool  - Starting new HTTPS connection (1): huggingface.co:443
2025-04-13 22:37:12 DEBUG    urllib3.connectionpool  - https://huggingface.co:443 "HEAD /bert-base-cased/resolve/main/tokenizer_config.json HTTP/1.1" 200 0
2025-04-13 22:37:12 DEBUG    urllib3.connectionpool  - https://huggingface.co:443 "HEAD /bert-base-cased/resolve/main/config.json HTTP/1.1" 200 0
Some weights of the PyTorch model were not used when initializing the TF 2.0 model TFBertModel: ['cls.seq_relationship.bias', 'cls.predictions.transform.LayerNorm.weight', 'cls.predictions.transform.dense.bias', 'cls.seq_relationship.weight', 'cls.predictions.transform.dense.weight', 'cls.predictions.transform.LayerNorm.bias', 'cls.predictions.bias']
- This IS expected if you are initializing TFBertModel from a PyTorch model trained on another task or with another architecture (e.g. initializing a TFBertForSequenceClassification model from a BertForPreTraining model).
- This IS NOT expected if you are initializing TFBertModel from a PyTorch model that you expect to be exactly identical (e.g. initializing a TFBertForSequenceClassification model from a BertForSequenceClassification model).
All the weights of TFBertModel were initialized from the PyTorch model.
If your task is similar to the task the model of the checkpoint was trained on, you can already use TFBertModel for predictions without further training.
2025-04-13 22:37:13 DEBUG    rasa.engine.graph  - Node 'run_DIETClassifier5' loading 'DIETClassifier.load' and kwargs: '{}'.
2025-04-13 22:37:13 DEBUG    rasa.engine.storage.local_model_storage  - Resource 'train_DIETClassifier5' was requested for reading.
2025-04-13 22:37:13 DEBUG    rasa.utils.tensorflow.models  - Loading the model from C:\Users\Boromir\AppData\Local\Temp\tmp75ds8s1x\train_DIETClassifier5\DIETClassifier.tf_model with finetune_mode=False...
2025-04-13 22:37:13 DEBUG    rasa.nlu.classifiers.diet_classifier  - You specified 'DIET' to train entities, but no entities are present in the training data. Skipping training of entities.
2025-04-13 22:37:13 DEBUG    rasa.nlu.classifiers.diet_classifier  - Following metrics will be logged during training:
2025-04-13 22:37:13 DEBUG    rasa.nlu.classifiers.diet_classifier  -   t_loss (total loss)
2025-04-13 22:37:13 DEBUG    rasa.nlu.classifiers.diet_classifier  -   i_acc (intent acc)
2025-04-13 22:37:13 DEBUG    rasa.nlu.classifiers.diet_classifier  -   i_loss (intent loss)
2025-04-13 22:37:19 DEBUG    rasa.utils.tensorflow.models  - Finished loading the model.
s:\software architecture\yandex practice\5_task_in\architecture-sprint-5\src\rasaenv\lib\site-packages\rasa\utils\train_utils.py:530: UserWarning: constrain_similarities is set to `False`. It is recommended to set it to `True` when using cross-entropy loss.
  rasa.shared.utils.io.raise_warning(
2025-04-13 22:37:19 DEBUG    rasa.engine.graph  - Node 'run_EntitySynonymMapper6' loading 'EntitySynonymMapper.load' and kwargs: '{}'.
2025-04-13 22:37:19 DEBUG    rasa.engine.storage.local_model_storage  - Resource 'train_EntitySynonymMapper6' was requested for reading.
2025-04-13 22:37:19 DEBUG    rasa.nlu.extractors.entity_synonyms  - Failed to load ABCMeta from model storage. Resource 'train_EntitySynonymMapper6' doesn't exist.
2025-04-13 22:37:19 DEBUG    rasa.engine.graph  - Node 'run_ResponseSelector7' loading 'ResponseSelector.load' and kwargs: '{}'.
2025-04-13 22:37:19 DEBUG    rasa.engine.storage.local_model_storage  - Resource 'train_ResponseSelector7' was requested for reading.
2025-04-13 22:37:19 DEBUG    rasa.nlu.classifiers.diet_classifier  - Failed to load ABCMeta from model storage. Resource 'train_ResponseSelector7' doesn't exist.
2025-04-13 22:37:19 DEBUG    rasa.engine.storage.local_model_storage  - Resource 'train_ResponseSelector7' was requested for reading.
2025-04-13 22:37:19 DEBUG    rasa.nlu.selectors.response_selector  - Failed to load ResponseSelector from model storage. Resource 'train_ResponseSelector7' doesn't exist.
2025-04-13 22:37:19 DEBUG    rasa.engine.graph  - Node 'run_RegexMessageHandler' loading 'RegexMessageHandler.load' and kwargs: '{}'.
2025-04-13 22:37:19 DEBUG    rasa.engine.graph  - Node 'domain_provider' loading 'DomainProvider.load' and kwargs: '{}'.
2025-04-13 22:37:19 DEBUG    rasa.engine.storage.local_model_storage  - Resource 'domain_provider' was requested for reading.
s:\software architecture\yandex practice\5_task_in\architecture-sprint-5\src\rasaenv\lib\site-packages\rasa\shared\core\slot_mappings.py:224: UserWarning: Slot auto-fill has been removed in 3.0 and replaced with a new explicit mechanism to set slots. Please refer to https://rasa.com/docs/rasa/domain#slots to learn more.
  rasa.shared.utils.io.raise_warning(
2025-04-13 22:37:19 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' loading 'MemoizationPolicy.load' and kwargs: '{}'.
2025-04-13 22:37:19 DEBUG    rasa.engine.storage.local_model_storage  - Resource 'train_MemoizationPolicy0' was requested for reading.
2025-04-13 22:37:19 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' loading 'RulePolicy.load' and kwargs: '{}'.
2025-04-13 22:37:19 DEBUG    rasa.engine.storage.local_model_storage  - Resource 'train_RulePolicy1' was requested for reading.
2025-04-13 22:37:19 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' loading 'TEDPolicy.load' and kwargs: '{}'.
2025-04-13 22:37:19 DEBUG    rasa.engine.storage.local_model_storage  - Resource 'train_TEDPolicy2' was requested for reading.
2025-04-13 22:37:19 DEBUG    rasa.utils.tensorflow.models  - Loading the model from C:\Users\Boromir\AppData\Local\Temp\tmp75ds8s1x\train_TEDPolicy2\ted_policy.tf_model with finetune_mode=False...
2025-04-13 22:37:26 DEBUG    rasa.utils.tensorflow.models  - Finished loading the model.
2025-04-13 22:37:26 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' loading 'RuleOnlyDataProvider.load' and kwargs: '{}'.
2025-04-13 22:37:26 DEBUG    rasa.engine.storage.local_model_storage  - Resource 'train_RulePolicy1' was requested for reading.
2025-04-13 22:37:26 DEBUG    rasa.engine.graph  - Node 'select_prediction' loading 'DefaultPolicyPredictionEnsemble.load' and kwargs: '{}'.
2025-04-13 22:37:26 INFO     root  - Rasa server is up and running.
2025-04-13 22:37:26 INFO     root  - Enabling coroutine debugging. Loop id 2023390940368.
2025-04-13 22:37:37 DEBUG    rasa.core.lock_store  - Issuing ticket for conversation 'PractikumStudent'.
2025-04-13 22:37:37 DEBUG    rasa.core.lock_store  - Acquiring lock for conversation 'PractikumStudent'.
2025-04-13 22:37:37 DEBUG    rasa.core.lock_store  - Acquired lock for conversation 'PractikumStudent'.
2025-04-13 22:37:37 DEBUG    rasa.core.tracker_store  - Could not find tracker for conversation ID 'PractikumStudent'.
2025-04-13 22:37:37 DEBUG    rasa.core.tracker_store  - No event broker configured. Skipping streaming events.
2025-04-13 22:37:37 DEBUG    rasa.core.processor  - Starting a new session for conversation ID 'PractikumStudent'.
2025-04-13 22:37:37 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[]
2025-04-13 22:37:37 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=action_session_start rasa_events=[<rasa.shared.core.events.SessionStarted object at 0x000001D749678E50>, ActionExecuted(action: action_listen, policy: None, confidence: None)]
2025-04-13 22:37:37 DEBUG    rasa.core.processor  - [debug    ] processor.slots.log            slot_values=     topic: None
        session_started_metadata: None
2025-04-13 22:37:37 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__message__': [<rasa.core.channels.channel.UserMessage object at 0x000001D741CB7C70>], '__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x000001D741CB7370>}, targets: ['run_RegexMessageHandler'] and ExecutionContext(model_id='ce53162aff6141fc931f2ec26509cd63', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-04-13 22:37:37 DEBUG    rasa.engine.graph  - Node 'nlu_message_converter' running 'NLUMessageConverter.convert_user_message'.
2025-04-13 22:37:37 DEBUG    rasa.engine.graph  - Node 'run_WhitespaceTokenizer0' running 'WhitespaceTokenizer.process'.
2025-04-13 22:37:37 DEBUG    rasa.engine.graph  - Node 'run_RegexFeaturizer1' running 'RegexFeaturizer.process'.
2025-04-13 22:37:37 DEBUG    rasa.engine.graph  - Node 'run_LexicalSyntacticFeaturizer2' running 'LexicalSyntacticFeaturizer.process'.
2025-04-13 22:37:37 DEBUG    rasa.engine.graph  - Node 'run_CountVectorsFeaturizer3' running 'CountVectorsFeaturizer.process'.
2025-04-13 22:37:37 DEBUG    rasa.engine.graph  - Node 'run_LanguageModelFeaturizer4' running 'LanguageModelFeaturizer.process'.
2025-04-13 22:37:37 DEBUG    rasa.engine.graph  - Node 'run_DIETClassifier5' running 'DIETClassifier.process'.
2025-04-13 22:37:37 DEBUG    rasa.engine.graph  - Node 'run_EntitySynonymMapper6' running 'EntitySynonymMapper.process'.
2025-04-13 22:37:37 DEBUG    rasa.engine.graph  - Node 'run_ResponseSelector7' running 'ResponseSelector.process'.
2025-04-13 22:37:37 DEBUG    rasa.nlu.classifiers.diet_classifier  - There is no trained model for 'ResponseSelector': The component is either not trained or didn't receive enough training data.
2025-04-13 22:37:37 DEBUG    rasa.nlu.selectors.response_selector  - Adding following selector key to message property: default
2025-04-13 22:37:37 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-04-13 22:37:37 DEBUG    rasa.engine.graph  - Node 'run_RegexMessageHandler' running 'RegexMessageHandler.process'.
2025-04-13 22:37:37 DEBUG    rasa.core.processor  - [debug    ] processor.message.parse        parse_data_entities=[] parse_data_intent={'name': 'greet', 'confidence': 0.9999991655349731} parse_data_text=Привет
2025-04-13 22:37:37 DEBUG    rasa.core.processor  - Logged UserUtterance - tracker now has 4 events.
2025-04-13 22:37:37 DEBUG    rasa.core.actions.action  - Validating extracted slots: topic
2025-04-13 22:37:37 DEBUG    rasa.core.processor  - [debug    ] processor.extract.slots        action_extract_slot=action_extract_slots len_extraction_events=1 rasa_events=[SlotSet(key: topic, value: Привет)]
2025-04-13 22:37:37 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x000001D741CB7370>}, targets: ['select_prediction'] and ExecutionContext(model_id='ce53162aff6141fc931f2ec26509cd63', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-04-13 22:37:37 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-04-13 22:37:37 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-04-13 22:37:37 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-04-13 22:37:37 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{}, {'user': {'intent': 'greet'}, 'prev_action': {'action_name': 'action_listen'}}]
2025-04-13 22:37:37 DEBUG    rasa.core.policies.memoization  - There is a memorised next action 'utter_greet'
2025-04-13 22:37:37 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-04-13 22:37:37 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user text: Привет | previous action name: action_listen
2025-04-13 22:37:37 DEBUG    rasa.core.policies.rule_policy  - There is no applicable rule.
2025-04-13 22:37:37 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: greet | previous action name: action_listen
2025-04-13 22:37:37 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'utter_greet'.
2025-04-13 22:37:37 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-04-13 22:37:37 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'utter_greet' based on user intent.
2025-04-13 22:37:37 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-04-13 22:37:37 DEBUG    rasa.core.policies.ensemble  - Made prediction using user intent.
2025-04-13 22:37:37 DEBUG    rasa.core.policies.ensemble  - Added `DefinePrevUserUtteredFeaturization(False)` event.
2025-04-13 22:37:37 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-04-13 22:37:37 DEBUG    rasa.core.processor  - Predicted next action 'utter_greet' with confidence 1.00.
2025-04-13 22:37:37 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[<rasa.shared.core.events.DefinePrevUserUtteredFeaturization object at 0x000001D741CCB310>]
2025-04-13 22:37:37 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=utter_greet rasa_events=[BotUttered('Привет! Чем могу помочь в области архитектуры программного обеспечения?', {"elements": null, "quick_replies": null, "buttons": null, "attachment": null, "image": null, "custom": null}, {"utter_action": "utter_greet"}, 1744573057.4144459)]
2025-04-13 22:37:37 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x000001D741CB7370>}, targets: ['select_prediction'] and ExecutionContext(model_id='ce53162aff6141fc931f2ec26509cd63', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-04-13 22:37:37 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-04-13 22:37:37 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-04-13 22:37:37 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-04-13 22:37:37 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'greet'}, 'prev_action': {'action_name': 'action_listen'}}, {'user': {'intent': 'greet'}, 'prev_action': {'action_name': 'utter_greet'}}]
2025-04-13 22:37:37 DEBUG    rasa.core.policies.memoization  - There is a memorised next action 'action_listen'
2025-04-13 22:37:37 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-04-13 22:37:37 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: greet | previous action name: action_listen
[state 2] user intent: greet | previous action name: utter_greet
2025-04-13 22:37:37 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'action_listen'.
2025-04-13 22:37:37 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-04-13 22:37:37 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'action_listen' based on user intent.
2025-04-13 22:37:37 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-04-13 22:37:37 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-04-13 22:37:37 DEBUG    rasa.core.processor  - Predicted next action 'action_listen' with confidence 1.00.
2025-04-13 22:37:37 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[]
2025-04-13 22:37:37 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=action_listen rasa_events=[]
2025-04-13 22:37:37 DEBUG    rasa.core.tracker_store  - No event broker configured. Skipping streaming events.
2025-04-13 22:37:37 DEBUG    rasa.core.lock_store  - Deleted lock for conversation 'PractikumStudent'.
2025-04-13 22:37:45 DEBUG    rasa.core.lock_store  - Issuing ticket for conversation 'PractikumStudent'.
2025-04-13 22:37:45 DEBUG    rasa.core.lock_store  - Acquiring lock for conversation 'PractikumStudent'.
2025-04-13 22:37:45 DEBUG    rasa.core.lock_store  - Acquired lock for conversation 'PractikumStudent'.
2025-04-13 22:37:45 DEBUG    rasa.core.tracker_store  - Recreating tracker for id 'PractikumStudent'
2025-04-13 22:37:45 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__message__': [<rasa.core.channels.channel.UserMessage object at 0x000001D741CB7E50>], '__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x000001D741CB7AF0>}, targets: ['run_RegexMessageHandler'] and ExecutionContext(model_id='ce53162aff6141fc931f2ec26509cd63', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-04-13 22:37:45 DEBUG    rasa.engine.graph  - Node 'nlu_message_converter' running 'NLUMessageConverter.convert_user_message'.
2025-04-13 22:37:45 DEBUG    rasa.engine.graph  - Node 'run_WhitespaceTokenizer0' running 'WhitespaceTokenizer.process'.
2025-04-13 22:37:45 DEBUG    rasa.engine.graph  - Node 'run_RegexFeaturizer1' running 'RegexFeaturizer.process'.
2025-04-13 22:37:45 DEBUG    rasa.engine.graph  - Node 'run_LexicalSyntacticFeaturizer2' running 'LexicalSyntacticFeaturizer.process'.
2025-04-13 22:37:45 DEBUG    rasa.engine.graph  - Node 'run_CountVectorsFeaturizer3' running 'CountVectorsFeaturizer.process'.
2025-04-13 22:37:45 DEBUG    rasa.engine.graph  - Node 'run_LanguageModelFeaturizer4' running 'LanguageModelFeaturizer.process'.
2025-04-13 22:37:45 DEBUG    rasa.engine.graph  - Node 'run_DIETClassifier5' running 'DIETClassifier.process'.
2025-04-13 22:37:45 DEBUG    rasa.engine.graph  - Node 'run_EntitySynonymMapper6' running 'EntitySynonymMapper.process'.
2025-04-13 22:37:45 DEBUG    rasa.engine.graph  - Node 'run_ResponseSelector7' running 'ResponseSelector.process'.
2025-04-13 22:37:45 DEBUG    rasa.nlu.classifiers.diet_classifier  - There is no trained model for 'ResponseSelector': The component is either not trained or didn't receive enough training data.
2025-04-13 22:37:45 DEBUG    rasa.nlu.selectors.response_selector  - Adding following selector key to message property: default
2025-04-13 22:37:45 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-04-13 22:37:45 DEBUG    rasa.engine.graph  - Node 'run_RegexMessageHandler' running 'RegexMessageHandler.process'.
2025-04-13 22:37:45 DEBUG    rasa.core.processor  - [debug    ] processor.message.parse        parse_data_entities=[] parse_data_intent={'name': 'greet', 'confidence': 0.9999991655349731} parse_data_text=Добрый день!
2025-04-13 22:37:45 DEBUG    rasa.core.processor  - Logged UserUtterance - tracker now has 10 events.
2025-04-13 22:37:45 DEBUG    rasa.core.actions.action  - Validating extracted slots: topic
2025-04-13 22:37:45 DEBUG    rasa.core.processor  - [debug    ] processor.extract.slots        action_extract_slot=action_extract_slots len_extraction_events=1 rasa_events=[SlotSet(key: topic, value: Добрый день!)]
2025-04-13 22:37:45 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x000001D741CB7AF0>}, targets: ['select_prediction'] and ExecutionContext(model_id='ce53162aff6141fc931f2ec26509cd63', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-04-13 22:37:45 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-04-13 22:37:45 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-04-13 22:37:45 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-04-13 22:37:45 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'greet'}, 'prev_action': {'action_name': 'utter_greet'}}, {'user': {'intent': 'greet'}, 'prev_action': {'action_name': 'action_listen'}}]
2025-04-13 22:37:45 DEBUG    rasa.core.policies.memoization  - There is no memorised next action
2025-04-13 22:37:45 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-04-13 22:37:45 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: greet | previous action name: action_listen
[state 2] user intent: greet | previous action name: utter_greet
[state 3] user text: Добрый день! | previous action name: action_listen
2025-04-13 22:37:45 DEBUG    rasa.core.policies.rule_policy  - There is no applicable rule.
2025-04-13 22:37:45 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: greet | previous action name: action_listen
[state 2] user intent: greet | previous action name: utter_greet
[state 3] user intent: greet | previous action name: action_listen
2025-04-13 22:37:45 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'utter_greet'.
2025-04-13 22:37:45 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-04-13 22:37:45 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'utter_greet' based on user intent.
2025-04-13 22:37:45 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-04-13 22:37:45 DEBUG    rasa.core.policies.ensemble  - Made prediction using user intent.
2025-04-13 22:37:45 DEBUG    rasa.core.policies.ensemble  - Added `DefinePrevUserUtteredFeaturization(False)` event.
2025-04-13 22:37:45 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-04-13 22:37:45 DEBUG    rasa.core.processor  - Predicted next action 'utter_greet' with confidence 1.00.
2025-04-13 22:37:45 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[<rasa.shared.core.events.DefinePrevUserUtteredFeaturization object at 0x000001D741C316A0>]
2025-04-13 22:37:45 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=utter_greet rasa_events=[BotUttered('Привет! Чем могу помочь в области архитектуры программного обеспечения?', {"elements": null, "quick_replies": null, "buttons": null, "attachment": null, "image": null, "custom": null}, {"utter_action": "utter_greet"}, 1744573065.9773784)]
2025-04-13 22:37:45 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x000001D741CB7AF0>}, targets: ['select_prediction'] and ExecutionContext(model_id='ce53162aff6141fc931f2ec26509cd63', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-04-13 22:37:45 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-04-13 22:37:45 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-04-13 22:37:45 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-04-13 22:37:45 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'greet'}, 'prev_action': {'action_name': 'action_listen'}}, {'user': {'intent': 'greet'}, 'prev_action': {'action_name': 'utter_greet'}}]
2025-04-13 22:37:45 DEBUG    rasa.core.policies.memoization  - There is a memorised next action 'action_listen'
2025-04-13 22:37:45 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-04-13 22:37:45 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: greet | previous action name: action_listen
[state 2] user intent: greet | previous action name: utter_greet
[state 3] user intent: greet | previous action name: action_listen
[state 4] user intent: greet | previous action name: utter_greet
2025-04-13 22:37:45 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'action_listen'.
2025-04-13 22:37:45 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-04-13 22:37:45 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'action_listen' based on user intent.
2025-04-13 22:37:45 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-04-13 22:37:45 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-04-13 22:37:45 DEBUG    rasa.core.processor  - Predicted next action 'action_listen' with confidence 1.00.
2025-04-13 22:37:45 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[]
2025-04-13 22:37:45 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=action_listen rasa_events=[]
2025-04-13 22:37:45 DEBUG    rasa.core.tracker_store  - No event broker configured. Skipping streaming events.
2025-04-13 22:37:45 DEBUG    rasa.core.lock_store  - Deleted lock for conversation 'PractikumStudent'.
2025-04-13 22:37:56 DEBUG    rasa.core.lock_store  - Issuing ticket for conversation 'PractikumStudent'.
2025-04-13 22:37:56 DEBUG    rasa.core.lock_store  - Acquiring lock for conversation 'PractikumStudent'.
2025-04-13 22:37:56 DEBUG    rasa.core.lock_store  - Acquired lock for conversation 'PractikumStudent'.
2025-04-13 22:37:56 DEBUG    rasa.core.tracker_store  - Recreating tracker for id 'PractikumStudent'
2025-04-13 22:37:56 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__message__': [<rasa.core.channels.channel.UserMessage object at 0x000001D741CCBFD0>], '__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x000001D741CB7280>}, targets: ['run_RegexMessageHandler'] and ExecutionContext(model_id='ce53162aff6141fc931f2ec26509cd63', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-04-13 22:37:56 DEBUG    rasa.engine.graph  - Node 'nlu_message_converter' running 'NLUMessageConverter.convert_user_message'.
2025-04-13 22:37:56 DEBUG    rasa.engine.graph  - Node 'run_WhitespaceTokenizer0' running 'WhitespaceTokenizer.process'.
2025-04-13 22:37:56 DEBUG    rasa.engine.graph  - Node 'run_RegexFeaturizer1' running 'RegexFeaturizer.process'.
2025-04-13 22:37:56 DEBUG    rasa.engine.graph  - Node 'run_LexicalSyntacticFeaturizer2' running 'LexicalSyntacticFeaturizer.process'.
2025-04-13 22:37:56 DEBUG    rasa.engine.graph  - Node 'run_CountVectorsFeaturizer3' running 'CountVectorsFeaturizer.process'.
2025-04-13 22:37:56 DEBUG    rasa.engine.graph  - Node 'run_LanguageModelFeaturizer4' running 'LanguageModelFeaturizer.process'.
2025-04-13 22:37:56 DEBUG    rasa.engine.graph  - Node 'run_DIETClassifier5' running 'DIETClassifier.process'.
2025-04-13 22:37:56 DEBUG    rasa.engine.graph  - Node 'run_EntitySynonymMapper6' running 'EntitySynonymMapper.process'.
2025-04-13 22:37:56 DEBUG    rasa.engine.graph  - Node 'run_ResponseSelector7' running 'ResponseSelector.process'.
2025-04-13 22:37:56 DEBUG    rasa.nlu.classifiers.diet_classifier  - There is no trained model for 'ResponseSelector': The component is either not trained or didn't receive enough training data.
2025-04-13 22:37:56 DEBUG    rasa.nlu.selectors.response_selector  - Adding following selector key to message property: default
2025-04-13 22:37:56 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-04-13 22:37:56 DEBUG    rasa.engine.graph  - Node 'run_RegexMessageHandler' running 'RegexMessageHandler.process'.
2025-04-13 22:37:56 DEBUG    rasa.core.processor  - [debug    ] processor.message.parse        parse_data_entities=[] parse_data_intent={'name': 'ask_architecture', 'confidence': 0.9999992847442627} parse_data_text=Расскижи об архитектуре
2025-04-13 22:37:56 DEBUG    rasa.core.processor  - Logged UserUtterance - tracker now has 16 events.
2025-04-13 22:37:56 DEBUG    rasa.core.actions.action  - Validating extracted slots: topic
2025-04-13 22:37:56 DEBUG    rasa.core.processor  - [debug    ] processor.extract.slots        action_extract_slot=action_extract_slots len_extraction_events=1 rasa_events=[SlotSet(key: topic, value: Расскижи об архитектуре)]
2025-04-13 22:37:56 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x000001D741CB7280>}, targets: ['select_prediction'] and ExecutionContext(model_id='ce53162aff6141fc931f2ec26509cd63', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-04-13 22:37:56 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-04-13 22:37:56 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-04-13 22:37:56 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-04-13 22:37:56 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'greet'}, 'prev_action': {'action_name': 'utter_greet'}}, {'user': {'intent': 'ask_architecture'}, 'prev_action': {'action_name': 'action_listen'}}]
2025-04-13 22:37:56 DEBUG    rasa.core.policies.memoization  - There is a memorised next action 'utter_architecture_response'
2025-04-13 22:37:56 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-04-13 22:37:56 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: greet | previous action name: action_listen
[state 2] user intent: greet | previous action name: utter_greet
[state 3] user intent: greet | previous action name: action_listen
[state 4] user intent: greet | previous action name: utter_greet
[state 5] user text: Расскижи об архитектуре | previous action name: action_listen
2025-04-13 22:37:56 DEBUG    rasa.core.policies.rule_policy  - There is no applicable rule.
2025-04-13 22:37:56 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: greet | previous action name: action_listen
[state 2] user intent: greet | previous action name: utter_greet
[state 3] user intent: greet | previous action name: action_listen
[state 4] user intent: greet | previous action name: utter_greet
[state 5] user intent: ask_architecture | previous action name: action_listen
2025-04-13 22:37:56 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'utter_architecture_response'.
2025-04-13 22:37:56 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-04-13 22:37:56 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'utter_architecture_response' based on user intent.
2025-04-13 22:37:56 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-04-13 22:37:56 DEBUG    rasa.core.policies.ensemble  - Made prediction using user intent.
2025-04-13 22:37:56 DEBUG    rasa.core.policies.ensemble  - Added `DefinePrevUserUtteredFeaturization(False)` event.
2025-04-13 22:37:56 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-04-13 22:37:56 DEBUG    rasa.core.processor  - Predicted next action 'utter_architecture_response' with confidence 1.00.
2025-04-13 22:37:56 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[<rasa.shared.core.events.DefinePrevUserUtteredFeaturization object at 0x000001D73D308A30>]
2025-04-13 22:37:56 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=utter_architecture_response rasa_events=[BotUttered('Архитектура ПО включает выбор структур, которые обеспечивают масштабируемость, гибкость и поддерживаемость приложения. Задайте конкретный вопрос по этой теме, и я помогу вам с информацией.', {"elements": null, "quick_replies": null, "buttons": null, "attachment": null, "image": null, "custom": null}, {"utter_action": "utter_architecture_response"}, 1744573076.9762135)]
2025-04-13 22:37:56 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x000001D741CB7280>}, targets: ['select_prediction'] and ExecutionContext(model_id='ce53162aff6141fc931f2ec26509cd63', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-04-13 22:37:56 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-04-13 22:37:56 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-04-13 22:37:56 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-04-13 22:37:56 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'ask_architecture'}, 'prev_action': {'action_name': 'action_listen'}}, {'user': {'intent': 'ask_architecture'}, 'prev_action': {'action_name': 'utter_architecture_response'}}]
2025-04-13 22:37:56 DEBUG    rasa.core.policies.memoization  - There is a memorised next action 'action_listen'
2025-04-13 22:37:56 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-04-13 22:37:56 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: greet | previous action name: action_listen
[state 2] user intent: greet | previous action name: utter_greet
[state 3] user intent: greet | previous action name: action_listen
[state 4] user intent: greet | previous action name: utter_greet
[state 5] user intent: ask_architecture | previous action name: action_listen
[state 6] user intent: ask_architecture | previous action name: utter_architecture_response
2025-04-13 22:37:56 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'action_listen'.
2025-04-13 22:37:56 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-04-13 22:37:56 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'action_listen' based on user intent.
2025-04-13 22:37:56 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-04-13 22:37:56 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-04-13 22:37:56 DEBUG    rasa.core.processor  - Predicted next action 'action_listen' with confidence 1.00.
2025-04-13 22:37:56 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[]
2025-04-13 22:37:56 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=action_listen rasa_events=[]
2025-04-13 22:37:56 DEBUG    rasa.core.tracker_store  - No event broker configured. Skipping streaming events.
2025-04-13 22:37:56 DEBUG    rasa.core.lock_store  - Deleted lock for conversation 'PractikumStudent'.
2025-04-13 22:39:47 DEBUG    rasa.core.lock_store  - Issuing ticket for conversation 'PractikumStudent'.
2025-04-13 22:39:47 DEBUG    rasa.core.lock_store  - Acquiring lock for conversation 'PractikumStudent'.
2025-04-13 22:39:47 DEBUG    rasa.core.lock_store  - Acquired lock for conversation 'PractikumStudent'.
2025-04-13 22:39:47 DEBUG    rasa.core.tracker_store  - Recreating tracker for id 'PractikumStudent'
2025-04-13 22:39:47 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__message__': [<rasa.core.channels.channel.UserMessage object at 0x000001D741CCB760>], '__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x000001D73D308A00>}, targets: ['run_RegexMessageHandler'] and ExecutionContext(model_id='ce53162aff6141fc931f2ec26509cd63', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-04-13 22:39:47 DEBUG    rasa.engine.graph  - Node 'nlu_message_converter' running 'NLUMessageConverter.convert_user_message'.
2025-04-13 22:39:47 DEBUG    rasa.engine.graph  - Node 'run_WhitespaceTokenizer0' running 'WhitespaceTokenizer.process'.
2025-04-13 22:39:47 DEBUG    rasa.engine.graph  - Node 'run_RegexFeaturizer1' running 'RegexFeaturizer.process'.
2025-04-13 22:39:47 DEBUG    rasa.engine.graph  - Node 'run_LexicalSyntacticFeaturizer2' running 'LexicalSyntacticFeaturizer.process'.
2025-04-13 22:39:47 DEBUG    rasa.engine.graph  - Node 'run_CountVectorsFeaturizer3' running 'CountVectorsFeaturizer.process'.
2025-04-13 22:39:47 DEBUG    rasa.engine.graph  - Node 'run_LanguageModelFeaturizer4' running 'LanguageModelFeaturizer.process'.
2025-04-13 22:39:47 DEBUG    rasa.engine.graph  - Node 'run_DIETClassifier5' running 'DIETClassifier.process'.
2025-04-13 22:39:47 DEBUG    rasa.engine.graph  - Node 'run_EntitySynonymMapper6' running 'EntitySynonymMapper.process'.
2025-04-13 22:39:47 DEBUG    rasa.engine.graph  - Node 'run_ResponseSelector7' running 'ResponseSelector.process'.
2025-04-13 22:39:47 DEBUG    rasa.nlu.classifiers.diet_classifier  - There is no trained model for 'ResponseSelector': The component is either not trained or didn't receive enough training data.
2025-04-13 22:39:47 DEBUG    rasa.nlu.selectors.response_selector  - Adding following selector key to message property: default
2025-04-13 22:39:47 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-04-13 22:39:47 DEBUG    rasa.engine.graph  - Node 'run_RegexMessageHandler' running 'RegexMessageHandler.process'.
2025-04-13 22:39:47 DEBUG    rasa.core.processor  - [debug    ] processor.message.parse        parse_data_entities=[] parse_data_intent={'name': 'ask_architecture', 'confidence': 0.9999872446060181} parse_data_text=А что ты скажешь про микросервисы?
2025-04-13 22:39:47 DEBUG    rasa.core.processor  - Logged UserUtterance - tracker now has 22 events.
2025-04-13 22:39:47 DEBUG    rasa.core.actions.action  - Validating extracted slots: topic
2025-04-13 22:39:47 DEBUG    rasa.core.processor  - [debug    ] processor.extract.slots        action_extract_slot=action_extract_slots len_extraction_events=1 rasa_events=[SlotSet(key: topic, value: А что ты скажешь про микросервисы?)]
2025-04-13 22:39:47 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x000001D73D308A00>}, targets: ['select_prediction'] and ExecutionContext(model_id='ce53162aff6141fc931f2ec26509cd63', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-04-13 22:39:47 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-04-13 22:39:47 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-04-13 22:39:47 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-04-13 22:39:47 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'ask_architecture'}, 'prev_action': {'action_name': 'utter_architecture_response'}}, {'user': {'intent': 'ask_architecture'}, 'prev_action': {'action_name': 'action_listen'}}]
2025-04-13 22:39:47 DEBUG    rasa.core.policies.memoization  - There is no memorised next action
2025-04-13 22:39:47 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-04-13 22:39:47 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: greet | previous action name: action_listen
[state 2] user intent: greet | previous action name: utter_greet
[state 3] user intent: greet | previous action name: action_listen
[state 4] user intent: greet | previous action name: utter_greet
[state 5] user intent: ask_architecture | previous action name: action_listen
[state 6] user intent: ask_architecture | previous action name: utter_architecture_response
[state 7] user text: А что ты скажешь про микросервисы? | previous action name: action_listen
2025-04-13 22:39:47 DEBUG    rasa.core.policies.rule_policy  - There is no applicable rule.
2025-04-13 22:39:47 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: greet | previous action name: action_listen
[state 2] user intent: greet | previous action name: utter_greet
[state 3] user intent: greet | previous action name: action_listen
[state 4] user intent: greet | previous action name: utter_greet
[state 5] user intent: ask_architecture | previous action name: action_listen
[state 6] user intent: ask_architecture | previous action name: utter_architecture_response
[state 7] user intent: ask_architecture | previous action name: action_listen
2025-04-13 22:39:47 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'utter_architecture_response'.
2025-04-13 22:39:47 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-04-13 22:39:47 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'utter_architecture_response' based on user intent.
2025-04-13 22:39:47 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-04-13 22:39:47 DEBUG    rasa.core.policies.ensemble  - Made prediction using user intent.
2025-04-13 22:39:47 DEBUG    rasa.core.policies.ensemble  - Added `DefinePrevUserUtteredFeaturization(False)` event.
2025-04-13 22:39:47 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-04-13 22:39:47 DEBUG    rasa.core.processor  - Predicted next action 'utter_architecture_response' with confidence 1.00.
2025-04-13 22:39:47 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[<rasa.shared.core.events.DefinePrevUserUtteredFeaturization object at 0x000001D741CBF610>]
2025-04-13 22:39:47 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=utter_architecture_response rasa_events=[BotUttered('Архитектура ПО включает выбор структур, которые обеспечивают масштабируемость, гибкость и поддерживаемость приложения. Задайте конкретный вопрос по этой теме, и я помогу вам с информацией.', {"elements": null, "quick_replies": null, "buttons": null, "attachment": null, "image": null, "custom": null}, {"utter_action": "utter_architecture_response"}, 1744573187.6744127)]
2025-04-13 22:39:47 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x000001D73D308A00>}, targets: ['select_prediction'] and ExecutionContext(model_id='ce53162aff6141fc931f2ec26509cd63', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-04-13 22:39:47 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-04-13 22:39:47 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-04-13 22:39:47 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-04-13 22:39:47 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'ask_architecture'}, 'prev_action': {'action_name': 'action_listen'}}, {'user': {'intent': 'ask_architecture'}, 'prev_action': {'action_name': 'utter_architecture_response'}}]
2025-04-13 22:39:47 DEBUG    rasa.core.policies.memoization  - There is a memorised next action 'action_listen'
2025-04-13 22:39:47 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-04-13 22:39:47 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: greet | previous action name: action_listen
[state 2] user intent: greet | previous action name: utter_greet
[state 3] user intent: greet | previous action name: action_listen
[state 4] user intent: greet | previous action name: utter_greet
[state 5] user intent: ask_architecture | previous action name: action_listen
[state 6] user intent: ask_architecture | previous action name: utter_architecture_response
[state 7] user intent: ask_architecture | previous action name: action_listen
[state 8] user intent: ask_architecture | previous action name: utter_architecture_response
2025-04-13 22:39:47 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'action_listen'.
2025-04-13 22:39:47 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-04-13 22:39:47 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'action_listen' based on user intent.
2025-04-13 22:39:47 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-04-13 22:39:47 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-04-13 22:39:47 DEBUG    rasa.core.processor  - Predicted next action 'action_listen' with confidence 1.00.
2025-04-13 22:39:47 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[]
2025-04-13 22:39:47 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=action_listen rasa_events=[]
2025-04-13 22:39:47 DEBUG    rasa.core.tracker_store  - No event broker configured. Skipping streaming events.
2025-04-13 22:39:47 DEBUG    rasa.core.lock_store  - Deleted lock for conversation 'PractikumStudent'.
2025-04-13 22:39:58 DEBUG    rasa.core.lock_store  - Issuing ticket for conversation 'PractikumStudent'.
2025-04-13 22:39:58 DEBUG    rasa.core.lock_store  - Acquiring lock for conversation 'PractikumStudent'.
2025-04-13 22:39:58 DEBUG    rasa.core.lock_store  - Acquired lock for conversation 'PractikumStudent'.
2025-04-13 22:39:58 DEBUG    rasa.core.tracker_store  - Recreating tracker for id 'PractikumStudent'
2025-04-13 22:39:58 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__message__': [<rasa.core.channels.channel.UserMessage object at 0x000001D71B595D60>], '__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x000001D741CB7C70>}, targets: ['run_RegexMessageHandler'] and ExecutionContext(model_id='ce53162aff6141fc931f2ec26509cd63', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-04-13 22:39:58 DEBUG    rasa.engine.graph  - Node 'nlu_message_converter' running 'NLUMessageConverter.convert_user_message'.
2025-04-13 22:39:58 DEBUG    rasa.engine.graph  - Node 'run_WhitespaceTokenizer0' running 'WhitespaceTokenizer.process'.
2025-04-13 22:39:58 DEBUG    rasa.engine.graph  - Node 'run_RegexFeaturizer1' running 'RegexFeaturizer.process'.
2025-04-13 22:39:58 DEBUG    rasa.engine.graph  - Node 'run_LexicalSyntacticFeaturizer2' running 'LexicalSyntacticFeaturizer.process'.
2025-04-13 22:39:58 DEBUG    rasa.engine.graph  - Node 'run_CountVectorsFeaturizer3' running 'CountVectorsFeaturizer.process'.
2025-04-13 22:39:58 DEBUG    rasa.engine.graph  - Node 'run_LanguageModelFeaturizer4' running 'LanguageModelFeaturizer.process'.
2025-04-13 22:39:58 DEBUG    rasa.engine.graph  - Node 'run_DIETClassifier5' running 'DIETClassifier.process'.
2025-04-13 22:39:58 DEBUG    rasa.engine.graph  - Node 'run_EntitySynonymMapper6' running 'EntitySynonymMapper.process'.
2025-04-13 22:39:58 DEBUG    rasa.engine.graph  - Node 'run_ResponseSelector7' running 'ResponseSelector.process'.
2025-04-13 22:39:58 DEBUG    rasa.nlu.classifiers.diet_classifier  - There is no trained model for 'ResponseSelector': The component is either not trained or didn't receive enough training data.
2025-04-13 22:39:58 DEBUG    rasa.nlu.selectors.response_selector  - Adding following selector key to message property: default
2025-04-13 22:39:58 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-04-13 22:39:58 DEBUG    rasa.engine.graph  - Node 'run_RegexMessageHandler' running 'RegexMessageHandler.process'.
2025-04-13 22:39:58 DEBUG    rasa.core.processor  - [debug    ] processor.message.parse        parse_data_entities=[] parse_data_intent={'name': 'goodbye', 'confidence': 0.9996421337127686} parse_data_text=Спасибо, пока!
2025-04-13 22:39:58 DEBUG    rasa.core.processor  - Logged UserUtterance - tracker now has 28 events.
2025-04-13 22:39:58 DEBUG    rasa.core.actions.action  - Validating extracted slots: topic
2025-04-13 22:39:58 DEBUG    rasa.core.processor  - [debug    ] processor.extract.slots        action_extract_slot=action_extract_slots len_extraction_events=1 rasa_events=[SlotSet(key: topic, value: Спасибо, пока!)]
2025-04-13 22:39:58 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x000001D741CB7C70>}, targets: ['select_prediction'] and ExecutionContext(model_id='ce53162aff6141fc931f2ec26509cd63', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-04-13 22:39:58 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-04-13 22:39:58 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-04-13 22:39:58 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-04-13 22:39:58 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'ask_architecture'}, 'prev_action': {'action_name': 'utter_architecture_response'}}, {'user': {'intent': 'goodbye'}, 'prev_action': {'action_name': 'action_listen'}}]
2025-04-13 22:39:58 DEBUG    rasa.core.policies.memoization  - There is no memorised next action
2025-04-13 22:39:58 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-04-13 22:39:58 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: greet | previous action name: action_listen
[state 2] user intent: greet | previous action name: utter_greet
[state 3] user intent: greet | previous action name: action_listen
[state 4] user intent: greet | previous action name: utter_greet
[state 5] user intent: ask_architecture | previous action name: action_listen
[state 6] user intent: ask_architecture | previous action name: utter_architecture_response
[state 7] user intent: ask_architecture | previous action name: action_listen
[state 8] user intent: ask_architecture | previous action name: utter_architecture_response
[state 9] user text: Спасибо, пока! | previous action name: action_listen
2025-04-13 22:39:58 DEBUG    rasa.core.policies.rule_policy  - There is no applicable rule.
2025-04-13 22:39:58 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: greet | previous action name: action_listen
[state 2] user intent: greet | previous action name: utter_greet
[state 3] user intent: greet | previous action name: action_listen
[state 4] user intent: greet | previous action name: utter_greet
[state 5] user intent: ask_architecture | previous action name: action_listen
[state 6] user intent: ask_architecture | previous action name: utter_architecture_response
[state 7] user intent: ask_architecture | previous action name: action_listen
[state 8] user intent: ask_architecture | previous action name: utter_architecture_response
[state 9] user intent: goodbye | previous action name: action_listen
2025-04-13 22:39:58 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'utter_goodbye'.
2025-04-13 22:39:58 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-04-13 22:39:58 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'utter_goodbye' based on user intent.
2025-04-13 22:39:58 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-04-13 22:39:58 DEBUG    rasa.core.policies.ensemble  - Made prediction using user intent.
2025-04-13 22:39:58 DEBUG    rasa.core.policies.ensemble  - Added `DefinePrevUserUtteredFeaturization(False)` event.
2025-04-13 22:39:58 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-04-13 22:39:58 DEBUG    rasa.core.processor  - Predicted next action 'utter_goodbye' with confidence 1.00.
2025-04-13 22:39:58 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[<rasa.shared.core.events.DefinePrevUserUtteredFeaturization object at 0x000001D73D3083D0>]
2025-04-13 22:39:58 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=utter_goodbye rasa_events=[BotUttered('До свидания! Если появятся вопросы по архитектуре ПО, обращайтесь.', {"elements": null, "quick_replies": null, "buttons": null, "attachment": null, "image": null, "custom": null}, {"utter_action": "utter_goodbye"}, 1744573198.687786)]
2025-04-13 22:39:58 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x000001D741CB7C70>}, targets: ['select_prediction'] and ExecutionContext(model_id='ce53162aff6141fc931f2ec26509cd63', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-04-13 22:39:58 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-04-13 22:39:58 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-04-13 22:39:58 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-04-13 22:39:58 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'goodbye'}, 'prev_action': {'action_name': 'action_listen'}}, {'user': {'intent': 'goodbye'}, 'prev_action': {'action_name': 'utter_goodbye'}}]
2025-04-13 22:39:58 DEBUG    rasa.core.policies.memoization  - There is a memorised next action 'action_listen'
2025-04-13 22:39:58 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-04-13 22:39:58 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: greet | previous action name: action_listen
[state 2] user intent: greet | previous action name: utter_greet
[state 3] user intent: greet | previous action name: action_listen
[state 4] user intent: greet | previous action name: utter_greet
[state 5] user intent: ask_architecture | previous action name: action_listen
[state 6] user intent: ask_architecture | previous action name: utter_architecture_response
[state 7] user intent: ask_architecture | previous action name: action_listen
[state 8] user intent: ask_architecture | previous action name: utter_architecture_response
[state 9] user intent: goodbye | previous action name: action_listen
[state 10] user intent: goodbye | previous action name: utter_goodbye
2025-04-13 22:39:58 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'action_listen'.
2025-04-13 22:39:58 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-04-13 22:39:58 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'action_listen' based on user intent.
2025-04-13 22:39:58 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-04-13 22:39:58 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-04-13 22:39:58 DEBUG    rasa.core.processor  - Predicted next action 'action_listen' with confidence 1.00.
2025-04-13 22:39:58 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[]
2025-04-13 22:39:58 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=action_listen rasa_events=[]
2025-04-13 22:39:58 DEBUG    rasa.core.tracker_store  - No event broker configured. Skipping streaming events.
2025-04-13 22:39:58 DEBUG    rasa.core.lock_store  - Deleted lock for conversation 'PractikumStudent'.
2025-04-13 22:40:03 DEBUG    rasa.core.lock_store  - Issuing ticket for conversation 'PractikumStudent'.
2025-04-13 22:40:03 DEBUG    rasa.core.lock_store  - Acquiring lock for conversation 'PractikumStudent'.
2025-04-13 22:40:03 DEBUG    rasa.core.lock_store  - Acquired lock for conversation 'PractikumStudent'.
2025-04-13 22:40:03 DEBUG    rasa.core.tracker_store  - Recreating tracker for id 'PractikumStudent'
2025-04-13 22:40:03 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__message__': [<rasa.core.channels.channel.UserMessage object at 0x000001D742E54EB0>], '__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x000001D741CBFC10>}, targets: ['run_RegexMessageHandler'] and ExecutionContext(model_id='ce53162aff6141fc931f2ec26509cd63', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-04-13 22:40:03 DEBUG    rasa.engine.graph  - Node 'nlu_message_converter' running 'NLUMessageConverter.convert_user_message'.
2025-04-13 22:40:03 DEBUG    rasa.engine.graph  - Node 'run_WhitespaceTokenizer0' running 'WhitespaceTokenizer.process'.
2025-04-13 22:40:03 DEBUG    rasa.engine.graph  - Node 'run_RegexFeaturizer1' running 'RegexFeaturizer.process'.
2025-04-13 22:40:03 DEBUG    rasa.engine.graph  - Node 'run_LexicalSyntacticFeaturizer2' running 'LexicalSyntacticFeaturizer.process'.
2025-04-13 22:40:03 DEBUG    rasa.engine.graph  - Node 'run_CountVectorsFeaturizer3' running 'CountVectorsFeaturizer.process'.
2025-04-13 22:40:03 DEBUG    rasa.engine.graph  - Node 'run_LanguageModelFeaturizer4' running 'LanguageModelFeaturizer.process'.
2025-04-13 22:40:03 DEBUG    rasa.engine.graph  - Node 'run_DIETClassifier5' running 'DIETClassifier.process'.
2025-04-13 22:40:03 DEBUG    rasa.engine.graph  - Node 'run_EntitySynonymMapper6' running 'EntitySynonymMapper.process'.
2025-04-13 22:40:03 DEBUG    rasa.engine.graph  - Node 'run_ResponseSelector7' running 'ResponseSelector.process'.
2025-04-13 22:40:03 DEBUG    rasa.nlu.classifiers.diet_classifier  - There is no trained model for 'ResponseSelector': The component is either not trained or didn't receive enough training data.
2025-04-13 22:40:03 DEBUG    rasa.nlu.selectors.response_selector  - Adding following selector key to message property: default
2025-04-13 22:40:03 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-04-13 22:40:03 DEBUG    rasa.engine.graph  - Node 'run_RegexMessageHandler' running 'RegexMessageHandler.process'.
2025-04-13 22:40:03 DEBUG    rasa.core.processor  - [debug    ] processor.message.parse        parse_data_entities=[] parse_data_intent={'name': 'goodbye', 'confidence': 0.9999821186065674} parse_data_text=До свидания
2025-04-13 22:40:03 DEBUG    rasa.core.processor  - Logged UserUtterance - tracker now has 34 events.
2025-04-13 22:40:03 DEBUG    rasa.core.actions.action  - Validating extracted slots: topic
2025-04-13 22:40:03 DEBUG    rasa.core.processor  - [debug    ] processor.extract.slots        action_extract_slot=action_extract_slots len_extraction_events=1 rasa_events=[SlotSet(key: topic, value: До свидания)]
2025-04-13 22:40:03 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x000001D741CBFC10>}, targets: ['select_prediction'] and ExecutionContext(model_id='ce53162aff6141fc931f2ec26509cd63', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-04-13 22:40:03 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-04-13 22:40:03 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-04-13 22:40:03 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-04-13 22:40:03 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'goodbye'}, 'prev_action': {'action_name': 'utter_goodbye'}}, {'user': {'intent': 'goodbye'}, 'prev_action': {'action_name': 'action_listen'}}]
2025-04-13 22:40:03 DEBUG    rasa.core.policies.memoization  - There is no memorised next action
2025-04-13 22:40:03 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-04-13 22:40:03 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: greet | previous action name: action_listen
[state 2] user intent: greet | previous action name: utter_greet
[state 3] user intent: greet | previous action name: action_listen
[state 4] user intent: greet | previous action name: utter_greet
[state 5] user intent: ask_architecture | previous action name: action_listen
[state 6] user intent: ask_architecture | previous action name: utter_architecture_response
[state 7] user intent: ask_architecture | previous action name: action_listen
[state 8] user intent: ask_architecture | previous action name: utter_architecture_response
[state 9] user intent: goodbye | previous action name: action_listen
[state 10] user intent: goodbye | previous action name: utter_goodbye
[state 11] user text: До свидания | previous action name: action_listen
2025-04-13 22:40:03 DEBUG    rasa.core.policies.rule_policy  - There is no applicable rule.
2025-04-13 22:40:03 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: greet | previous action name: action_listen
[state 2] user intent: greet | previous action name: utter_greet
[state 3] user intent: greet | previous action name: action_listen
[state 4] user intent: greet | previous action name: utter_greet
[state 5] user intent: ask_architecture | previous action name: action_listen
[state 6] user intent: ask_architecture | previous action name: utter_architecture_response
[state 7] user intent: ask_architecture | previous action name: action_listen
[state 8] user intent: ask_architecture | previous action name: utter_architecture_response
[state 9] user intent: goodbye | previous action name: action_listen
[state 10] user intent: goodbye | previous action name: utter_goodbye
[state 11] user intent: goodbye | previous action name: action_listen
2025-04-13 22:40:03 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'utter_goodbye'.
2025-04-13 22:40:03 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-04-13 22:40:03 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'utter_goodbye' based on user intent.
2025-04-13 22:40:03 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-04-13 22:40:03 DEBUG    rasa.core.policies.ensemble  - Made prediction using user intent.
2025-04-13 22:40:03 DEBUG    rasa.core.policies.ensemble  - Added `DefinePrevUserUtteredFeaturization(False)` event.
2025-04-13 22:40:03 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-04-13 22:40:03 DEBUG    rasa.core.processor  - Predicted next action 'utter_goodbye' with confidence 1.00.
2025-04-13 22:40:03 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[<rasa.shared.core.events.DefinePrevUserUtteredFeaturization object at 0x000001D73D2F94F0>]
2025-04-13 22:40:03 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=utter_goodbye rasa_events=[BotUttered('До свидания! Если появятся вопросы по архитектуре ПО, обращайтесь.', {"elements": null, "quick_replies": null, "buttons": null, "attachment": null, "image": null, "custom": null}, {"utter_action": "utter_goodbye"}, 1744573203.743447)]
2025-04-13 22:40:03 DEBUG    rasa.engine.runner.dask  - Running graph with inputs: {'__tracker__': <rasa.shared.core.trackers.DialogueStateTracker object at 0x000001D741CBFC10>}, targets: ['select_prediction'] and ExecutionContext(model_id='ce53162aff6141fc931f2ec26509cd63', should_add_diagnostic_data=False, is_finetuning=False, node_name=None).
2025-04-13 22:40:03 DEBUG    rasa.engine.graph  - Node 'rule_only_data_provider' running 'RuleOnlyDataProvider.provide'.
2025-04-13 22:40:03 DEBUG    rasa.engine.graph  - Node 'domain_provider' running 'DomainProvider.provide_inference'.
2025-04-13 22:40:03 DEBUG    rasa.engine.graph  - Node 'run_MemoizationPolicy0' running 'MemoizationPolicy.predict_action_probabilities'.
2025-04-13 22:40:03 DEBUG    rasa.core.policies.memoization  - [debug    ] memoization.predict.actions    tracker_states=[{'user': {'intent': 'goodbye'}, 'prev_action': {'action_name': 'action_listen'}}, {'user': {'intent': 'goodbye'}, 'prev_action': {'action_name': 'utter_goodbye'}}]
2025-04-13 22:40:03 DEBUG    rasa.core.policies.memoization  - There is a memorised next action 'action_listen'
2025-04-13 22:40:03 DEBUG    rasa.engine.graph  - Node 'run_RulePolicy1' running 'RulePolicy.predict_action_probabilities'.
2025-04-13 22:40:03 DEBUG    rasa.core.policies.rule_policy  - [debug    ] rule_policy.actions.find       current_states=
[state 1] user intent: greet | previous action name: action_listen
[state 2] user intent: greet | previous action name: utter_greet
[state 3] user intent: greet | previous action name: action_listen
[state 4] user intent: greet | previous action name: utter_greet
[state 5] user intent: ask_architecture | previous action name: action_listen
[state 6] user intent: ask_architecture | previous action name: utter_architecture_response
[state 7] user intent: ask_architecture | previous action name: action_listen
[state 8] user intent: ask_architecture | previous action name: utter_architecture_response
[state 9] user intent: goodbye | previous action name: action_listen
[state 10] user intent: goodbye | previous action name: utter_goodbye
[state 11] user intent: goodbye | previous action name: action_listen
[state 12] user intent: goodbye | previous action name: utter_goodbye
2025-04-13 22:40:03 DEBUG    rasa.core.policies.rule_policy  - There is a rule for the next action 'action_listen'.
2025-04-13 22:40:03 DEBUG    rasa.engine.graph  - Node 'run_TEDPolicy2' running 'TEDPolicy.predict_action_probabilities'.
2025-04-13 22:40:03 DEBUG    rasa.core.policies.ted_policy  - TED predicted 'action_listen' based on user intent.
2025-04-13 22:40:03 DEBUG    rasa.engine.graph  - Node 'select_prediction' running 'DefaultPolicyPredictionEnsemble.combine_predictions_from_kwargs'.
2025-04-13 22:40:03 DEBUG    rasa.core.policies.ensemble  - Predicted next action using RulePolicy.
2025-04-13 22:40:03 DEBUG    rasa.core.processor  - Predicted next action 'action_listen' with confidence 1.00.
2025-04-13 22:40:03 DEBUG    rasa.core.processor  - [debug    ] processor.actions.policy_prediction prediction_events=[]
2025-04-13 22:40:03 DEBUG    rasa.core.processor  - [debug    ] processor.actions.log          action_name=action_listen rasa_events=[]
2025-04-13 22:40:03 DEBUG    rasa.core.tracker_store  - No event broker configured. Skipping streaming events.
2025-04-13 22:40:03 DEBUG    rasa.core.lock_store  - Deleted lock for conversation 'PractikumStudent'.

```
</details>
