---
layout: post
title: DAWN of a New Era
comments: true
author: Peter Bailis, Kunle Olukotun, Chris Ré, and Matei Zaharia
---

We are in the golden age of machine learning and artificial intelligence. Sustained algorithmic
advances coupled with the availability of massive datasets and fast parallel computing have led to
breakthroughs in applications that would have been considered science fiction even a few years ago.
Over the past five years, voice-driven personal assistants have become commonplace, image
recognition systems have reached human quality, and autonomous vehicles are rapidly become broadly
available. Given these successes, there is no doubt that machine learning will transform most areas
of our economy and society. Businesses, governments and scientific labs are clamoring to see how
machine learning can tackle their problems.

Unfortunately, although new machine learning (ML) applications are impressive, they are very
expensive to build. Every major new ML product, such as Apple Siri, Amazon Alexa, or Tesla
Autopilot, required large and costly teams of domain experts, data scientists, data engineers, and
DevOps to realize. Even within these successful organizations, ML remains a rare and expensive
commodity. Moreover, many application areas require even more effort to obtain training data to feed
their ML algorithms; for example, even though an ML algorithm achieves human quality in identifying
pictures of dogs on the Internet (thanks to millions of available labeled images), the algorithm
will not achieve the same quality identifying cancer in medical images unless an organization
expends countless hours of human expert time creating training data sets. Finally, once an ML
product is built, it requires effort to deploy, operate, and monitor at scale, especially if
critical business processes will rely on it. In summary, ML technology is at a similar stage to
early digital computers, where armies of technicians clad in white labored to keep a small handful
of machines operating in production: ML technology clearly has tremendous potential, but today’s
ML-powered systems remain far too expensive to build for most application domains.

To address this potential, our group at Stanford is beginning a new, five-year research project to
design systems infrastructure and tools for \textit{usable machine learning}, called DAWN (Data
Analytics for What’s Next). Our goal is _not_ to improve ML algorithms, which are almost always “good
enough” for many important applications, but instead to make ML _usable_ so that small teams of non-ML
experts can apply ML to their problems, achieve high-quality results, and deploy production systems
that can be used in critical applications. While today’s ML successes have required large and costly
teams of statisticians and engineers, we would like to make similar successes attainable for domain
experts—for example, a hospital optimizing medical procedures, a scientist parsing terabytes of data
from instruments, or a business applying ML to its domain-specific problems. Major improvements in
the usability of machine learning are mandatory to realize its potential. In brief, we ask:

_How can we enable anyone with domain expertise to build their own production-quality data products
(without requiring a team of PhDs in machine learning, databases, and distributed systems, and
without understanding the latest hardware)?_

At first, our goal of usable machine learning might appear too ambitious—how can we expect one or
two domain experts to match work that today requires teams of tens to hundreds? Our observation is
that such revolutions ``democratizing’’ computing technology have happened before. For example,
although textual search is a complex field requiring sophisticated algorithms and data structures,
today, search is ubiquitous. Non-expert users rely on search engines every day, and any developer
can add search to an application by linking a library such as Lucene or Solr. These libraries offer
good enough results out of the box, and simple enough tuning options, to be usable by non-experts.
Similarly, in the 1970s, relational databases revolutionized data management. Before modern
databases, organizations built computer applications using low-level code that had to directly
manipulate on-disk data structures and implement complex processing algorithms. Databases
encapsulated this complexity behind simple interfaces that any developer can use, and that most
users can even _tune_ without understanding system internals. As a result, organizations need to spend
far less effort to build a data management application, and many run thousands of such applications.

With history as a guide, our key observation is that most of the effort in industrial ML
applications is _not_ spent in devising new learning algorithms or models but is instead spent in
three other areas: _data preparation_, _feature selection_, and _productionization_ (cf.
~\cite{ml-credit-card}). Data preparation means acquiring, producing and cleaning enough training
data to feed into an ML algorithm: without this quality data, ML algorithms fall flat. Feature
selection means identifying the data characteristics and behaviors of interest: what aspects of data
are most important, and what would a domain expert implicitly or explicitly say about a given data
point? Productionization means deploying, monitoring and debugging a robust product: how can an
organization check that the ML algorithm deployed is working, debug issues that arise, and make the
system robust to changes in data? In the large teams that build ML products such as Siri, most of
the individuals work on data preparation, feature selection, productionization, and the distributed
systems infrastructure to drive these tasks at scale, _not_ on training ML algorithms. However, thus
far, these critical process of the ML product pipeline have received far less attention than model
training and new model tweaks—both from the research community and the open source software
community—and, based on our prior work in this area, we see substantial opportunity to greatly
reduce the effort for these tasks.

Stay tuned.
