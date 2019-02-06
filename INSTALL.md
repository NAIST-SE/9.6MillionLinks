# Full dataset (links per language)

All the links targeted in our study are provided at [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.2550683.svg)](https://doi.org/10.5281/zenodo.2550683).

||**#links**|
|:---|---:|
|C|1,602,156|
|C++|1,686,575|
|Java|2,925,909|
|JavaScript|1,533,219|
|Python|413,020|
|PHP|1,405525|
|Ruby|88,298|
|**sum**|**9,654,702**|

Each csv file contains the following fields:
- language
- domain of a link
- link location
- link

# Other resources

### Comment Lister
Comment extraction is reproducible with a new set of Git repositories. See [details](https://github.com/takashi-ishio/CommentLister).

### Qualitative coding
Our coding results of 1146 links for RQ2 (link target) and RQ3 (link purpose) are available [here](https://docs.google.com/spreadsheets/d/e/2PACX-1vTQl_MtM5TsWBLbHvVqDsbGnN4KG6KRAlX1MlfMXMdTcrUtQb0eXTO3pEPj39d8ohCdFNi6Oui4cSjg/pubhtml?gid=0&single=true).

**coding guide for RQ2**
- *404* - link target does not exist (anymore) or cannot be accessed
- *licence* - licence of a software project
- *software homepage* - main web presence of a library or software project
- *specification* - anything that resembles a requirements document or a technical standard
- *organization homepage* - main web presence of an organization or company
- *other* - anything that does not fit the other codes, including if sign-in is required
- *tutorial or article* - technical article or tutorial, without commenting section (blog post otherwise)
- *API documentation* - documentation of an API element
- *blog post* - technical content with a commenting section
- *application* - interactive application (e.g., web application, online utility)
- *bug report* - bug report or issue in an online bug/issue tracker
- *research paper* - academic paper
- *personal homepage* - personal homepage of one individual
- *code* - a source code file
- *forum thread* - thread in a forum or entire forum
- *GitHub profile* - profile of a GitHub contributor
- *book content* - chapter/section of a book or entire book
- *Q\&A thread* - question-and-answer thread, but not Stack Overflow
- *Stack Overflow* - question-and-answer thread on Stack Overflow

**coding guide for RQ3**
- *metadata* - the link relates to the author of the source, a related organization, or the license
- *source/attribution* - the comment explicitly indicates that the link is a source of some aspect of the source code (e.g., algorithm)
- *source code context* - the link adds additional information to the source code (use this code for things that do not obviously fit into any of the previous)
- *see-also* - the comment explicitly indicates that the link points to additional reading material (usually accompanied by a phrase such as "see also").
- *commented-out source code* - the link is part of the source code, e.g., as a parameter value, but has been commented out
- *link-only* - the comment only contains the link
- *self-admitted technical debt* - bug-related, like workaround, under development, and so on
- *@see* - the link is accompanied by "@see", but no further explanation

**Pull Requests for RQ7**
- *Closed* 
-- https://github.com/BrowserSync/browser-sync/pull/1593
- https://github.com/shirasagi/shirasagi/pull/2289
- https://github.com/onepercentclub/bluebottle/pull/3372
- https://github.com/ShipSoft/FairShip/pull/133
- https://github.com/mutalyzer/mutalyzer/pull/454
- https://github.com/sveawebpay/php-integration/pull/82
- https://github.com/cms-sw/cmssw/pull/24370
- https://github.com/BlackToppStudios/Mezzanine/pull/182
- https://github.com/mockingbirdnest/Principia/pull/1905

- *Open*  
- https://github.com/dzavalishin/phantomuserland/pull/468
- https://github.com/refluster/lab/pull/12
- https://github.com/densho/ddr-cmdln/pull/87
- https://github.com/netzbasis/openbsd-src/pull/1
- https://github.com/ci-bonfire/Bonfire/pull/1303
