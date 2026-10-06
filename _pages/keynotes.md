---
layout: page_plain
title: Keynotes
permalink: /keynotes/
order: 3
published: true
---


## [Dalal Alrajeh](https://www.doc.ic.ac.uk/~da04/), Imperial College London, UK 
<img src="{{ site.baseurl }}{% link assets/images/people/da.jpg %}" class="imageSpeaker" align="right"/>

 <p style="min-height: 170px;">


<br/>

</p>


**From Intent to Guarantees: Building Trustworthy Software Systems**

Trustworthy software systems depend not only on correct implementations, but on the quality of the specifications that capture what they should do and the assumptions about the environments in which they operate. This raises fundamental challenges: how can we identify weaknesses and conflicts in specifications, determine whether their requirements can actually be realised, and maintain meaningful guarantees as systems and their environments evolve? 
 
In this talk, I will present our work on specification analysis and evolution for safe and trustworthy systems. I will discuss how realizability can expose unavoidable boundary conditions—situations in which requirements inevitably conflict—and provide targeted feedback for specification repair. I will then consider what happens when assumptions that underpin system guarantees are violated at runtime, presenting approaches that use inductive learning to adapt specifications while preserving their intended guarantees as far as possible. Finally, I will show how these ideas extend to adaptive shielding for reinforcement learning, enabling safety specifications to evolve in response to unexpected environment behaviour. 

<!--
([Presentation slides](../assets/presentations/Keynote%20SEFM_25_Elvira_Albert.pdf)) 
-->




## [Elizabeth Polgreen](https://polgreen.github.io), University of Edinburgh, UK 

 <img src="{{ site.baseurl }}{% link assets/images/people/polgreen.png %}" class="imageSpeaker" align="right"/>


 <p style="min-height: 170px;">


<br/>

</p>


**Reading Between the Lines of Code** 

Formal verification is hard. It is even harder when you do not know what property you should be verifying. 
People are notoriously bad at stating precisely what they want, and natural language is inherently ambiguous. As a result, much of the software and hardware we rely on comes without usable specifications for formal verification. Even when specifications do exist, they are often insufficiently detailed for automated verification tools to prove the properties we care about. This gap is becoming increasingly important as AI-generated code enters the software and hardware ecosystem: we may be able to generate implementations faster than ever, but understanding what those implementations are supposed to do remains a core challenge.

This talk will discuss our group’s attempts to close this gap through specification mining: automatically inferring the properties that are implicit in code, designs, and their behaviour. Drawing on classical program synthesis techniques as well as large language models, we are exploring methods for efficiently mining specifications for both hardware and software. Our aim is to reduce the manual burden of formal verification and, ultimately, to enable the verification of systems without requiring users to write formal specifications by hand. 




