# negotiation-dialogue-survey
Category on the negotiation dialogue papers


## Datasets

- **Discourse Structure and Dialogue Acts in Multiparty Dialogue: the STAC Corpus** (LREC 2016) [[paper](https://aclanthology.org/L16-1432.pdf)] [[data](https://aclanthology.org/attachments/D/D15/D15-1109.Attachment.zip)] (Yufei)
This paper describes the STAC benchmark, which is a corpus of multi-party dialogue annotated with discourse structure in the style of
SDRT and dialogue act, including offer, counter-offer, acceptance, refusal and other. The main motivation of this benchmark is to better understand the linguistic strategies adopted by players to achieve their conversational goals, especially when their goals are opposed, via the discourse structure in the dialogue.

- **Deal or No Deal? Learning for Negotiation Dialogues** (EMNLP 2017) [[paper](https://arxiv.org/pdf/1706.05125.pdf)] [[data](https://github.com/facebookresearch/end-to-end-negotiator)] (Yufei)
This paper collects the first large-scale two-party negotiation dialogue benchmark. In the data annotation stage, both annotators are only shown their own sets of items with a value for each and both of them are asked to maximize their total score after negotiation. This paper further proposes an end-to-end dialogue model to learn to response in the negotiation dialogue. For each negotiation dialogue, this paper splits it into two training examples from the perspective of each annotator. Finally, this paper proposes dialogue rollouts, which is to first generate a small number of responses and then similate the future conversation for each candidate. The model selects the candidate outputs with the highest expected reward. The experiments find that dialogue rollouts dramatically improves the output quality.


- **Decoupling Strategy and Generation in Negotiation Dialogues** (EMNLP 2018) [[paper](https://aclanthology.org/D18-1256.pdf)] [[data](https://stanfordnlp.github.io/cocoa/)] (Tao) - Done
-  **A Dynamic Strategy Coach for Effective Negotiation** (SIGDIAL 2019) [[paper](https://aclanthology.org/W19-5943.pdf)] [[data](https://github.com/zhouyiheng11/Negotiation-Coach)] (Tao) - Done
-  **Keeping up appearances: Computational modeling of face acts in persuasion oriented discussions.** (EMNLP 2020) [[paper](https://aclanthology.org/2020.emnlp-main.605.pdf)] [[code](https://github.com/ShoRit/face-acts)] (Tao) - Done
- **CaSiNo: A Corpus of Campsite Negotiation Dialogues for Automatic Negotiation Systems**  (NAACL 2021) [[paper](https://aclanthology.org/2021.naacl-main.254.pdf)] [[data](https://github.com/kushalchawla/CaSiNo)]  (Zhuang) 
CaSiNo is a corpus that includes thousand of negotiation dialogues in English. On the one hand, the settings in some negotiation datasets use strict communication protocols, thus failing to capture the richness and diversity in language use. On the other hand, some datasets include more open-ended negotiation dialogues. But the evaluation of negotiation performance is difficult for open-ended dialogues. CaSiNo overcomes the two shortcomings by emulating real-world negotiations while still following a tractable closed-domain abstraction from the negotiation literature. CaSiNo also defines nine negotiation strategies and annotates each utterance with one of the strategies. In addition, CaSiNo proposes a model to automatically predict the strategy for each utterance.

- **Dialogue Act-based Breakdown Detection in Negotiation Dialogues** (EACL 2021) [[paper](https://aclanthology.org/2021.eacl-main.63.pdf)] [[data](https://github.com/gucci-j/negotiation-breakdown-detection)]  (Zhuang)

They build a negotiation dataset in the interview scenario, including 2639 dialogues. They also annotated the dialogue acts for the dialogue and several models to detect the dialogue acts.


- **Towards Emotional Support Dialog Systems** (ACL 2021) [[paper](https://aclanthology.org/2021.acl-long.269.pdf)] [[data](https://github.com/thu-coai/Emotional-Support-Conversation)] (Haolan)

- **Initiative Taking in Negotiation** (SIGDIAL 2014) [[paper](https://aclanthology.org/W14-4325.pdf)] [no data link]  (Haolan)

- (Persuasion Dialogue) **Persuasion for Good: Towards a Personalized Persuasive Dialogue System for Social Good** (ACL 2019) [[paper](https://arxiv.org/pdf/1906.06725.pdf)][[data](https://gitlab.com/ucdavisnlp/persuasionforgood)] (Zhuang)

This paper designed a data collection to collect persuasive dialogue. They collected 1017 dialogues and annotated ten types of persuasion strategies. They also build a classifier using context information to predict the persuasion strategies. They also analyze the relationships between individuals’ personality, morality, value systems, and their willingness for donation.

- **An Item Response Theory Framework for Persuasion** (NAACL-findings 2022) [[paper](https://aclanthology.org/2022.findings-naacl.7.pdf)][[code \& data](https://github.com/akornilo/IRT_Persuasion)] [Education Scenarios]  (Haolan)

## Methods

- **Opponent Modeling in Negotiation Dialogues by Related Data Adaptation** (NAACL 2022 findings) [[paper](https://arxiv.org/abs/2205.00344)][[code](https://github.com/kushalchawla/opponent-modeling)] (Yufei)
This paper focuses on modeling the component's preference (i.e.,  the relative importance that the opponent assigns to each issue under discussion) using the partial dialogues. This could be very imporant in the negotiation process in real-world scenario. The authors propose transformer-based ranker over the negotiation items. In addition, they also make use the external dataset, CaSiNo and DealOrNoDeal dialogue data, to construct additional explicty supervision signals for this ranking task. The experiments show that the proposed methods achieve strong performance in zero-shot and
few-shot settings.

- **Computationally modelling resisting strategies in persuasive conversations** (EACL 2021) [[paper](https://aclanthology.org/2021.eacl-main.7.pdf)][[code](https://github.com/americast/resper)] (Yufei)

This paper focuses on modeling resisting strageties in the persuasive/Negotiation dialogues (i.e., Persuasion4Good and Craigslist Bargain). The authors first propose 7 different resisting strategies from social and cognitive psychology literatures, including Source Derogation, Counter Argument, Personal Choice, Information Inquiry, Self Pity, Hesitance and Self-assertion. This paper further proposes RESPER, a sequence labelling model with BERT and GRU module, that detects the resisting strageties used in each utterance. The paper also finds that incorperating these resisting strageties improves the accuracy for dialogues outcome prediction.


- **DialoGraph: Incorporating Interpretable Strategy-Graph Networks into Negotiation Dialogues** (ICLR 2021) [[paper](https://openreview.net/pdf?id=kDnal_bbb-E)] [[code](https://github.com/rishabhjoshi/DialoGraph_ICLR21)]  (Tao) - Done
- **Augmenting non-collaborative dialog systems with explicit semantic and strategic dialog history** (ICLR 2020) [[paper](https://openreview.net/forum?id=ryxQuANKPB)] (Yufei)

  This paper focuses on improving the performance of non-collaborative dialogs by learning Dialog Act and Strategy using finite state transducers (FSTs). Given the dialog history, two classifiers are used to predict Dialog Act and Strategy for each utterance. These predicted Dialog Act and Strategy labels are fed into FSTs. The outcome of FSTs are used as part of inputs to the dialog generator. The experiment results show that incorperating these information successfully improve the generated dialog quality.
  
  
  
- **Improving Dialog Systems for Negotiation with Personality Modeling** (ACL 2021) [[paper](https://aclanthology.org/2021.acl-long.56.pdf)] [[code](https://github.com/princeton-nlp/NegotiationToM)] (Yufei)
- **A deep reinforcement learning-based agent for negotiation with multiple communication channels** (ICTAI 2021) [[paper](https://ieeexplore.ieee.org/abstract/document/9643383)] [[code]] (Tao)
- **Towards Emotion-Aware Agents For Negotiation Dialogues** (20219th ICACII) [[paper](https://arxiv.org/pdf/2107.13165.pdf)]  (Haolan)

- **End-to-end trainable non-collaborative dialog system.** (AAAI 2021) [[paper](https://ojs.aaai.org/index.php/AAAI/article/view/6345)]  (Haolan)
- **Keeping up appearances: Computational modeling of face acts in persuasion oriented discussions.** (EMNLP 2020) [[paper](https://aclanthology.org/2020.emnlp-main.605.pdf)] [[code](https://github.com/ShoRit/face-acts)] (Zhuang)
Face is an important point in politeness research. It reflects the ‘public self-image’ that every rational adult member of society claims for themselves. This work studies the face acts in persuasion conversations. 
The major contributions of this work are: i) The definition of face acts, such as the acts that attack one’s face and those acts that raise one’s face. ii) The model that predicts the face acts. iii) The model that predicts the outcomes of the face acts (e.g. donation success).

- **Learning Goal-oriented Dialogue Policy with Opposite Agent Awareness** (AACL 2020) [[paper](https://aclanthology.org/2020.aacl-main.16.pdf)]

- **SOGO: A Social Intelligent Negotiation Dialogue System** (IVA 2018) [[paper](https://dl.acm.org/doi/pdf/10.1145/3267851.3267880)] (Zhuang)

- **Combining search with structured data to create a more engaging user experience in open domain dialogue** (SCAI 2017) [[paper](https://arxiv.org/pdf/1709.05411.pdf)]  (Haolan)

- **Reinforcement Learning of Multi-Issue Negotiation Dialogue Policies** (SIGDIAL 2015) [[paper](https://aclanthology.org/W15-4621.pdf)]  (Haolan)
- **Single-Agent vs. Multi-Agent Techniques for Concurrent Reinforcement Learning of Negotiation Dialogue Policies** (ACL 2014) [[paper](https://aclanthology.org/P14-1047.pdf)] (Zhuang)
- **Reinforcement Learning of Two-Issue Negotiation Dialogue Policies** (SIGDIAL 2013) [[paper](https://aclanthology.org/W13-4016.pdf)]
- **Grounding Strategic Conversation: Using negotiation dialogues to predict trades in a win-lose game** (EMNLP 2013) [[paper](https://aclanthology.org/D13-1035.pdf)]  (Haolan)
- **Negotiating causal implicatures** (SIGDIAL 2010) [[paper](https://aclanthology.org/W10-4312.pdf)] (Zhuang) 

This work designs a dialogue manager that infers and negotiates causal implicatures in the dialogues. For example, in this conversation, 
 
Mary: The chest is locked, the crown is inside

Bill: Give me the crown

Bill causally implicated: Unlock the chest 

The dialogue manager would infer that the chest should be unlocked first to give Bill the crown. So this work seems to be unrelated to the negotiation we are referring to.

- **Getting to yes: Negotiating agreement without giving in.** [book]
- **Reinforcement Learning of Argumentation Dialogue Policies in Negotiation** (INTERSPEECH 2011) [[paper](https://kgeorgila.github.io/publications/georgila_interspeech11.pdf)] (Tao) - Done
- **Arguments, Dialogue, and Negotiation** (Academia 2020) [[paper](https://d1wqtxts1xzle7.cloudfront.net/30687575/AmgoudParsonsMaudetECAI2000-with-cover-page-v2.pdf?Expires=1652160854&Signature=WkneuVUrjuFTPbYNNEVOKVipmvy1~RurCgykDQTzMc70DpdKW~KDnNaqOzQtaedgNlu32XTz0QUAHzMhkFuK7qOkrjoubt6HTpJKo~vi7Sk53tGQsJiiHJd7yxj4~l3zTvovlkQR2EZpT9U9cnLUEDUOM1jeR9ADexEXskVlA-whqaihqkU0md6y0t8pML9dne9GCC6V3xvwcyJTJH2-lpddPxrKqEPnsLkOQP9dXHvl9c7yDZpN6A5qS8JnmqMiCMtlZov~yzaVoVxCvFPyBzY~iEMOxzN9xB30KHUXFRLcAIIThwwe4HpU6C2crRJNGREVNFYnq8-JyFR0siLwmQ__&Key-Pair-Id=APKAJLOHF5GGSLRBV4ZA)]  (Haolan)
- **Summarizing Multilingual Spoken Negotiation Dialogues** (ACL 2000) [[paper](https://aclanthology.org/P00-1040.pdf)]  (Haolan)
- **Response Generation in Collaborative Negotiation** (ACL 1995) [[paper](https://aclanthology.org/P95-1019.pdf)] (Yufei)
- **Modeling Negotiation Subdialogues** (ACL 1992) [[paper](https://aclanthology.org/P92-1025.pdf)]  (Haolan & Yufei)
- **Multi-party, multiissue, multi-strategy negotiation for multi-modal virtual agents.** (In International Workshop on Intelligent Virtual Agent 2008) [[paper](https://link.springer.com/chapter/10.1007/978-3-540-85483-8_12)]  (Haolan)
- **Negotiating rationally** (1993, citation>1000) [[paper](https://books.google.com.au/books?hl=zh-CN&lr=&id=Ua7sAgAAQBAJ&oi=fnd&pg=PR7&dq=Negotiating+rationally.+1993&ots=BX50I0akaZ&sig=BXTGdHK9pbyVdeqo4-UXWfQyFjM#v=onepage&q=Negotiating%20rationally.%201993&f=false)]  (Haolan & Tao)
 
- **Meaning Negotiation in Dialogue** (COLING 1982) [[paper](https://aclanthology.org/C82-2044.pdf)]  (Haolan & Zhuang)
This paper seems to be not related to the Negotiation we expected. It was discussing how to find the meaning of the utterance to deal with complex language problems. 

- **Negotiation as a Challenge Problem for Virtual Humans** [[paper](https://www.researchgate.net/profile/Jonathan-Gratch-2/publication/282671174_Negotiation_as_a_Challenge_Problem_for_Virtual_Humans/links/561aa3b908aea8036722b651/Negotiation-as-a-Challenge-Problem-for-Virtual-Humans.pdf)]  (Haolan)

## Evaluation

- **Evaluating and Enhancing the Robustness of Dialogue Systems: A Case Study on a Negotiation Agent** (NAACL 2019) [[paper](https://aclanthology.org/N19-1336.pdf)] [[code](https://github.com/cmhcbb/Robustness-of-Dialogue-systems)] (Yufei & Tao) - Done
- **Evaluating Persuasion Strategies and Deep Reinforcement Learning methods for Negotiation Dialogue agents** (EACL 2017) [[paper](https://aclanthology.org/E17-2077.pdf)] (Zhuang & Haolan)

This paper evaluated the effectiveness of various negotiation strategies. The evaluation is conducted by human subjects communicating with multiple chatbot subjects using different negotiation strategies. The chatbot is learned with deep reinforcement learning. They found that persuasion strategy and a strategy learned with reinforcement learning perform the best.

- **Evaluation of a Fully Automatic Cooperative Persuasive Dialogue System** [[paper](https://link.springer.com/chapter/10.1007/978-3-319-19291-8_15)] (Haolan)
- 


## Relevant to Negotiation

- **Essentials of negotiation** [[Book](http://proz-x.com/stephanlangdon/Academic/Neg/Essentials%20of%20Negotiation%20-%20Roy%20J.%20Lewicki,%20Bruce%20Barry.pdf)]
- **Iamhaggler: A negotiation agent for complex environments** [[Book](https://link.springer.com/content/pdf/10.1007/978-3-642-24696-8.pdf)]
- **On the cultural basis of gender differences in negotiation** (Exp Econ 2018) [[paper](https://link.springer.com/content/pdf/10.1007/s10683-017-9547-y.pdf)] (Yufei)
- **Learning about the opponent in automated bilateral negotiation: a comprehensive survey of opponent modeling techniques** (Auto Agent Multi-Agent System 2016) [[paper](https://link.springer.com/content/pdf/10.1007/s10458-015-9309-1.pdf)] (Yufei)
- **Toward Natural Turn-Taking in a Virtual Human Negotiation Agent** (AAAI Spring Symposium 2015) [[paper](https://www.aaai.org/ocs/index.php/SSS/SSS15/paper/viewFile/10335/10100)]   (Haolan)
- **The importance of the agenda in bargaining** (Games and Economic Behavior 1990) [[paper](https://www.tau.ac.il/~fersht/Papers/1990%20The%20importance%20of%20the%20agenda%20in%20bargaining.pdf)]  (Haolan & Zhuang)
- **Comparing The Accuracy of Frequentist and Bayesian Models in Human-Agent Negotiation** (the 21st ACM International Conference on Intelligent Virtual Agents 2021) [[paper](https://dl.acm.org/doi/pdf/10.1145/3472306.3478354)] (Tao) - Done
- **Assessing common errors students make when negotiating** (the 19st ACM International Conference on Intelligent Virtual Agents 2019) [[paper](https://dl.acm.org/doi/pdf/10.1145/3308532.3329470)] (Zhuang)
- **Detecting User’s Likes and Dislikes for a Virtual Negotiating Agent** (ICMI 2018) [[paper](https://dl.acm.org/doi/pdf/10.1145/3242969.3243024)]  (Haolan)


## Persuasive Negotiation (Persuasion)

- **Exploiting Personal Characteristics of Debaters for Predicting Persuasiveness** (ACL 2020) [[paper](https://aclanthology.org/2020.acl-main.632.pdf)] (Yufei)
- **Seamlessly Integrating Factual Information and Social Content with Persuasive Dialogue** (Arxiv 2022) [[paper](https://arxiv.org/pdf/2203.07657.pdf)] (Yufei)
- **Refine and Imitate: Reducing Repetition and Inconsistency in Persuasion Dialogues via Reinforcement Learning and Human Demonstration** (EMNLP-findings 2021) [[paper](https://aclanthology.org/2021.findings-emnlp.295.pdf)] [[code](https://github.com/wyshi/consistency)]  (Tao) - Done
- **Understanding User Resistance Strategies in Persuasive Conversations** (EMNLP-findings 2021) [[paper](https://aclanthology.org/2020.findings-emnlp.431.pdf)] (Haolan)
- **Hierarchical Argumentation Structure for Persuasive Argumentative Dialogue Generation** (IEICE TRANS 2020) [[paper](https://www.jstage.jst.go.jp/article/transinf/E103.D/2/E103.D_2019EDP7147/_pdf)]  (Tao) - Done
- **Empathetic Persuasion: Reinforcing Empathy and Persuasiveness in Dialogue Systems** (NAACL-findings 2022) [[paper](https://aclanthology.org/2022.findings-naacl.63.pdf)] (Zhuang)

A novel task of incorporating empathy when generating persuasive responses. An empathetic persuasive dialogue system by fine-tuning a Maximum Likelihood Estimation (MLE)-based language model in a Reinforcement Learning (RL) framework.

- **An Item Response Theory Framework for Persuasion** (NAACL-findings 2022) [[paper](https://aclanthology.org/2022.findings-naacl.7.pdf)][[code \& data](https://github.com/akornilo/IRT_Persuasion)] [Education Scenarios] (Tao)
- **A Study of the Impact of Persuasive Argumentation in Political Debates** (NAACL 2016) [[paper](https://aclanthology.org/N16-1166.pdf)] (Zhuang)

Annotated the Persuasive Argumentation in the corpus of Political Debates. Specifically, they annotated the Semantic Frames, which is the description of context in which a word sense is used. Studied the speaker’s influence on an audience based on his/her persuasiveness language and argumentation styles during a political debate.

- **Exploring the Role of Prior Beliefs for Argument Persuasion** (NAACL 2018) [[paper](https://aclanthology.org/N18-1094.pdf)]  (Haolan)
- **A Corpus for Modeling User and Language Effects in Argumentation on Online Debating** (ACL 2019) [[paper](https://aclanthology.org/P19-1057.pdf)] [[data](https://esdurmus.github.io/ddo.md)]  (Haolan & Zhuang)

Previous work in debating datasets lacks user profiles. This paper proposes datasets including 78 376 debates generated over a 10-year period. The dataset also includes comprehensive user information. Meanwhile, they studied which linguistic and user profile factors influence the debate winning rate most.

- **Analyzing the Persuasive Effect of Style in News Editorial Argumentation** (ACL 2020) [[paper](https://aclanthology.org/2020.acl-main.287.pdf)] (Haolan & Tao)
- **Modeling Persuasive Discourse to Adaptively Support Students’ Argumentative Writing** (ACL 2022) [[paper](https://aclanthology.org/2022.acl-long.599.pdf)] (Zhuang)

An argumentation annotation approach to model the structure of argumentative discourse in student-written business model pitches. Annotated the argument components, argumentative relations and persuasiveness scores.

- **Persuasion: Theory and research** [[Book](http://www.uky.edu/~ngrant/CJT780/readings/Day%201/cjt780/OKeefe2004.pdf)] 
- **Winning arguments: Interaction dynamics and persuasion strategies in good-faith online discussions** (WWW 2016) [[paper](https://dl.acm.org/doi/pdf/10.1145/2872427.2883081)]  (Haolan)
- **Perceived effectiveness of interpersonal persuasion strategies in computer-mediated communication** [[paper](https://www.sciencedirect.com/science/article/pii/S0747563203000062)] (Computer Scenario) ( Haolan & Yufei)

 
## Survey Papers in Other Dialogue Tracks
- **A Survey on Recent Advances and Challenges in Reinforcement Learning Methods for Task-Oriented Dialogue Policy Learning** (2022) [[paper](https://arxiv.org/pdf/2202.13675.pdf)] (Haolan & Yufei & Zhuang & Tao)
- **The AI Doctor Is In: A Survey of Task-Oriented Dialogue Systems for Healthcare Applications** （ACL 2022）[[paper](https://aclanthology.org/2022.acl-long.458.pdf)]
- **A Survey on Dialogue Systems: Recent Advances and New Frontiers** (KDD 2019) [[paper](https://www.kdd.org/exploration_files/19-2-Article3.pdf)]
- **Recent Advances in Deep Learning Based Dialogue Systems: A Systematic Survey** (2021) [[paper](https://arxiv.org/pdf/2105.04387.pdf)]
- **Survey on evaluation methods for dialogue systems** (AI Review 2021) [[paper](https://link.springer.com/article/10.1007/s10462-020-09866-x)]
- **A survey on empathetic dialogue systems** (Information Fusion 2021) [[paper](https://sentic.net/empathetic-dialogue-systems.pdf)]
- **A survey of response generation of dialogue systems** (IJCIE 2020) [[paper](https://publications.waset.org/10011629/a-survey-of-response-generation-of-dialogue-systems)]
- **Who Says What to Whom: A Survey of Multi-Party Conversations** (IJCAI 2022 Survey Track) [[paper]()]
- **A Survey on Dialogue Summarization: Recent Advances and New Frontiers** (IJCAI 2022 Survey Track) [[paper](https://arxiv.org/pdf/2107.03175.pdf)]
- **Challenges in Building Intelligent Open-domain Dialog Systems** (TOIS 2020) [[paper](https://arxiv.org/pdf/1905.05709.pdf)]
- **Recent advances and challenges in task-oriented dialog systems** (Science China 2020) [[paper](https://link.springer.com/article/10.1007/s11431-020-1692-3)]
- **A Survey of Document Grounded Dialogue Systems (DGDS)** (2019) [[paper](https://arxiv.org/pdf/2004.13818.pdf)] 
- **A Survey of Knowledge Sources in Dialogue Systems** (1999) [[paper](https://ep.liu.se/ea/cis/1999/026/cis99026.pdf)]
- **A Survey on Spoken Language Understanding: Recent Advances and New Frontiers** (IJCAI 2021 Survey Track) [[paper](https://arxiv.org/abs/2103.03095)]

