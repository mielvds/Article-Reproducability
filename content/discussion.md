## Discussion
{:#discussion}

The scientific process preaches _standing on the shoulders of giants_.
This entails continuing existing work to derive new work, but
also, enabling others to build upon our work.
An essential aspect of this process is reproducibility of experimental results.
This concept also applies to Web research,
but the Web itself, is also an ideal platform to _improve_ the scientific process.

Components.js deliberately adds semantics and Linked Data to Dependency Injection in order to accurately refer to experimental software, 
automatically discover component wiring, but also facilitate independently replacing and evaluating components.
Therefore it supports improved replication of experimental software.
A large number of computer science articles report software only by name or version number.
This information is insufficient for readers
to understand which _exact_ version of the software,
which versions of its _dependencies_,
and which detailed _configuration_ of the software's components
has obtained the reported results.
Therefore, potential users do not necessarily obtain the correct software installation
that will behave according to the article's conclusions.
Moreover, other researchers might fail
in reproducing the same results
because of differences in any such aspects.

[Claerbout's Principle](cite:providesQuotationFor WaveLab) explains that
<q>an article about computational science in a scientific publication
is not the scholarship itself, it is merely **advertising** of the scholarship.
The actual scholarship is the complete software development environment
and the complete set of instructions which generated the figures.</q>
This stresses the importance of reproducibility,
and essentially mandates a detailed description
of the executed experiment,
all of the involved artifacts and actors,
and the processing of the retrieved data.
In essence, this entails the complete chain of provenance illustrated in [](#description-diagram),
that links the research article to the data and the experiment that generates it,
as well as all aspects surrounding that experiment.

<figure id="description-diagram">
<img src="description-diagram.svg" alt="[description diagram]">
<figcaption markdown="block">
A _research article_ is based on _result data_,
which are the outcomes of an _experiment_.
The experiment in turn also has (multiple) provenance chains,
and this article focuses on _software configurations_ and _software modules_.
</figcaption>
</figure>

Through this work, we make it easier to build sustainable research platforms,
which helps pave the stairs to the shoulders of giants.
The Linked Data Fragments server, for instance, is a reusable research platform.
The LDF server and client can be compatible with multiple APIs, support multiple features, and use multiple, interchangeable algorithms.
Components.js requires only one "core version" to exist, while many alternative configurations can co-exist.
Support for different APIs and algorithms are simply pluggable components that are referred to within a configuration.
Since components and configurations are identified by an IRI,
they can exist anywhere on the Web.
Based on an IRI, the injection framework can therefore instantiate software,
and wire its dependent components together.
The power of the Web is thereby leveraged, simplifying the replication of existing experiments
and the creation of new ones.
