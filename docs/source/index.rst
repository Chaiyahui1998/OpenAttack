OpenAttack
=======================================

OpenAttack is an open-source Python-based textual adversarial attack toolkit, 
which handles the whole process of textual adversarial attacking, including 
preprocessing text, accessing the victim model, generating adversarial examples 
and evaluation.

------------------
Uses
------------------

OpenAttack has following features:

1. **High usability.** OpenAttack provides easy-to-use APIs that can support the whole process of textual adversarial attacks;
2. **Full coverage of attack model types.** OpenAttack supports sentence-/word-/character-level perturbations and gradient-/score-/decision-based/blind attack models;
3. **Great flexibility and extensibility.** You can easily attack a customized victim model or develop and evaluate a customized attack model;
4. **Comprehensive Evaluation.** OpenAttack can thoroughly evaluate an attack model from attack effectiveness, adversarial example quality and attack efficiency.


OpenAttack has a wide range of uses, including:

1. Providing various handy baselines for attack models;
2. Comprehensively evaluating attack models using its thorough evaluation metrics;
3. Assisting in quick development of new attack models with the help of its common attack components;
4. Evaluating the robustness of a machine learning model against various adversarial attacks;
5. Conducting adversarial training to improve robustness of a machine learning model by enriching the training data with generated adversarial examples.


---------------
Toolkit Design
---------------

Considering the significant distinctions among different attack models, we leave considerable freedom for the skeleton design of attack models, and focus more on streamlining the general processing of adversarial attacking and the common components used in attack models.

OpenAttack has 7 main modules:

.. image:: /images/toolkit_framework.png

* **TextProcessor**: processing the original text sequence so as to assist attack models in generating adversarial examples.
* **Classifier**: wrapping victim classification models
* **Attacker**: involving various attack models
* **Substitute**: packing different word/character substitution methods which are widely used in word- and character-level attack models.
* **Metric**: providing several adversarial example quality metrics which can serve as either the constraints on the adversarial examples during attacking or evaluation metrics for evaluating adversarial attacks.
* **AttackEval**: evaluating textual adversarial attacks from attack effectiveness, adversarial example quality and attack efficiency.
* **DataManager**: managing all the data as well as saved models that are used in other modules

.. toctree::
   :maxdepth: 1
   :hidden:
   :caption: Getting Started

   Introduction <quickstart/introduction>
   Installation <quickstart/installation>

.. toctree::
   :maxdepth: 1
   :hidden:
   :caption: Examples

   Example 1: Basic Usage <examples/example1>
   Example 2: Customized Victim Model <examples/example2>
   Example 3: Customized Attack Model <examples/example3>
   Example 4: Customized Measurement <examples/example4>
   Example 5: Adversarial Training <examples/example5>
   Example 6: Attacks on Chinese Dataset <examples/example6>

.. toctree::
   :maxdepth: 2
   :hidden:
   :caption: Modules

   DataManager <apis/data_manager>
   Attacker <apis/attacker>
   Substitute <apis/substitute>
   Metric <apis/metric>
   TextProcessor <apis/text_processor>
   AttackEval <apis/attack_eval>
   Classifier <apis/classifier>
   utils <apis/utils>

.. toctree::
   :maxdepth: 2
   :hidden:
   :caption: Data

   AttackAssist <data/AttackAssist>
   TProcess <data/TProcess>
   Victim <data/Victim>

Indices and tables
==================

* :ref:`search`