# SyferText v0.0.1 Release Notes
**Functionalities**:

  - > Extended the set\_attribute functionality for `Doc` and `Token` to cover checking and removing of an attribute (\#80 by @Akramz )

  - > Added `Span` class: `span` is a slice from a `Doc` object (\#78 by @bicycleman15 and @sachin-101 )

  - > Enabled lazy loading of language models: The `syfertext_en_core_web_lg` model should now be installed as a package (\#81 by @AlanAboudib )

  - > Created [<span class="underline">`syfertext_en_core_web_lg`</span>](https://github.com/Nilanshrajput/syfertext_en_core_web_lg) package ( by @AlanAboudib )

  - > Created `SimpleTagger` which class creates a custom attribute for `tokens` of a `Doc` ( \#24 by @AlanAboudib ) 

  - > Added custom attributes to `Doc` objects ( \#32 by @bicycleman15  )

  - > Compex `Tokenizer` with prefix, suffix, infix and exception cases functionalities(#36 by @Nilanshrajput )

  - > Created vector() method as property in the `Doc` class (\#37 by @prashantksharma and @bicycleman15  )

  - > Add `StringStore` class and Integrategration with `Doc` and `Vocab` for removing text attribute from `Doc` class and reconstruct text from hash keys (\#38 by @sachin-101 )

  - > Added pipelines/subpipelines functionality which is a `PySyft` object that encapsulates one or more pipe components that operate on the same worker. (\#40 by @AlanAboudib )

  - > Added excluded\_tokens argument in doc get\_vector to ignore tokens when getting the average vector of the doc.(\#48 by @AntonioLopardo )

  - > Removed pre-loaded strings in `StringStore` now string will only be added when it is encountered first. (\#60 by @bicycleman15 )

  - > Added PySyft serde.py support ( [<span class="underline">commit</span>](https://github.com/OpenMined/SyferText/commit/9228a291201f2e8061c4936df47dad8d73f65a86) by @AlanAboudib )

  - > Created Vector() method as property in the Doc class ( [<span class="underline">commit</span>](https://github.com/OpenMined/SyferText/commit/1ee5cb8b8ac83f364ce6c05d184ea911de9b81c3) by @AnasuyaAcharya )

**Bug Fixes**:

  - > Bug fix: annotations in \_\_future\_\_ module is not supported in python3.6 (\#94 by @Nilanshrajput )

  - > Tokenize empty strings, returns an empty doc(\[\]) for empty strings ("") (\#77 by @Nilanshrajput )

  - > Doc owner fix (\#74 by @bicycleman15 )

  - > Handle out of vocabulary tokens ( [<span class="underline">commit</span>](https://github.com/OpenMined/SyferText/commit/3c940c243483330685d64ae0555a052ead4395da) @dzlab )

  - > Removed unnecessary install step in main.yml for CI ([<span class="underline">commit</span>](https://github.com/OpenMined/SyferText/commit/5deed866a4239b7df0c3bb588439a4d44e62228e) by @dzlab )

**Examples and Tutorials**:

  - > Sentiment Classifier Training [<span class="underline">Usecase</span>](https://github.com/OpenMined/SyferText/blob/master/tutorials/usecases/UC01%20-%20Sentiment%20Classifier%20-%20Private%20Datasets%20-%20\(Secure%20Training\).ipynb) (\#66 by @AlanAboudib )

  - > Add [<span class="underline">tutorial</span>](https://github.com/OpenMined/SyferText/blob/master/tutorials/Part%202%20-%20\(Getting%20Started\)%20Using%20SimpleTagger.ipynb) for SimpleTagger (\#87 by @AntonioLopardo )

  - > [<span class="underline">Tutorial</span>](https://github.com/OpenMined/SyferText/blob/master/tutorials/Part%200%20-%20\(Getting%20Started\)%20Local%20Tokenization.ipynb) for Local Tokenization (by @AlanAboudib )

  - > [<span class="underline">Tutorial</span>](https://github.com/OpenMined/SyferText/blob/master/tutorials/Part%201%20-%20\(Getting%20Started\)%20Remote%20Tokenization.ipynb) for Remote Tokenization (by @AlanAboudib )

**Documentation**:

  - > Update README.md (\#88 by @Prince326 )

**Tests and Builds**:

  - > Updated setup.py to point to Syft on PyPI (\#98 by @AlanAboudib )

  - > Add PR checklist/Template (#13 by @dzlab )

  - > Added black and flake pre-commit hooks (\#42 by @sachin-101 )

  - > Added tests for pipeline (\#53 by @sachin-101 )

  - > Added .gitignore file (by @MarcioPorto  )

  - > Created main.yml for CI ( [<span class="underline">commit</span>](https://github.com/OpenMined/SyferText/commit/6f7cc9692cd99a3872d2d7ac59d7cf62ade7565c) by @AlanAboudib )

  - > added test for notebooks ( [<span class="underline">commit</span>](https://github.com/OpenMined/SyferText/commit/4a4f91d92a1378524e09c11116939403e20d8f78) by @dzlab )

  - > added black checking to pytest in CI ( [<span class="underline">commit</span>](https://github.com/OpenMined/SyferText/commit/a9b6f04e1ef1cf83472feaf6f9622ed35d966435) by @AlanAboudib )

**Classes and Files[WIP]**:

  - > \`Language\`: Inspired by spaCy Language class. It Orchestrates the interactions between different components of the pipeline to accomplish core text-processing task. It creates the Doc object which is the container into which all text-processing pipeline components feed their results.

  - > \`Doc\`: The Doc class is a container for holding a sequence of Token. Provides access for spans, tokens and vectors for each token.

  - > \`StringStore\`: StringStore object acts as a lookup table. It looks up strings by 64-bit hashes and vice-versa looks up hashes by their corresponding strings.

  - > \`Token\`:
