# Research Artifact: 9.6 Million Links in Source Code Comments

https://github.com/NAIST-SE/9.6MillionLinks/

This is a research artifact for the ICSE'19 paper **9.6 Million Links in Source Code Comments: Purpose, Evolution, and Decay**. This artifact is a data repository including all 9,654,702 links associated with the information of languages and comment location (GitHub links including account names, repository names, commit hashes, file paths, and line numbers) and the processed data. The purpose of this artifact is enabling researchers to replicate our mixed-methods quantitative results of the paper, and to reuse our around 9.6 million links in source code comments for further software engineering research.

Since our full dataset exceeds the file size limitation of GitHub, we published a separate version of this archive including the full dataset on Zenodo: [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.2550683.svg)](https://doi.org/10.5281/zenodo.2550683).

## Contents
- `INSTALL.md` - description of the full dataset and other resources
- `LICENSE.md` - [CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/)
- `README.md` - this file
- `STATUS.md` - application of an artifact badge of reusable
- `paper.pdf` - the accepted paper
- `full_dataset` - 9.6 million links avaiable at [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.2550683.svg)](https://doi.org/10.5281/zenodo.2550683)

## Processed data
### RQ2 and RQ3
- [Coding results](https://docs.google.com/spreadsheets/d/e/2PACX-1vTQl_MtM5TsWBLbHvVqDsbGnN4KG6KRAlX1MlfMXMdTcrUtQb0eXTO3pEPj39d8ohCdFNi6Oui4cSjg/pubhtml?gid=0&single=true)
### RQ4
- [Link evolution](https://docs.google.com/spreadsheets/d/e/2PACX-1vTJuBHzh_kxtazWb1-S5BHWaLcvSmoFp1um1lkdouMjFpcvXoI1Wr46mnHWJojZqXkHp3XyQrHS_whx/pubhtml?gid=0&single=true)
### RQ5
- Changes to the link target
  - [Link targets downloaded on August 11](https://drive.google.com/file/d/1x7ZWGnAw-AdhXLJuUWYZSCCi8tgRDGat/view?usp=sharing)
  - [Link targets downloaded on August 21](https://drive.google.com/file/d/1DsfwrVssjCRxqSr7pIobvM2lUF9yExYJ/view?usp=sharing)
  - [Raw output of file comparison](https://drive.google.com/open?id=16zqToSbGTQ_GoIxpSu3Q0Dwhhg5VoW-O)
  - [Analysis of file comparison](https://docs.google.com/spreadsheets/d/e/2PACX-1vRuPi2QKV86GKB2gJ_ZUDgwYQmf9zhZ5yr4v3PnkR7KZYGNcO9KUktop24bhYQSHCyvXQDpkWzCT9OH/pubhtml?gid=0&single=true)
- Stack Overflow case study for RQ5
  - We executed the following two queries for questions and answers on [SOTorrent](https://empirical-software.engineering/projects/sotorrent/) BigQuery
  - [Results](https://docs.google.com/spreadsheets/d/e/2PACX-1vSZWFHF64PWwWZRucE_jW72Qk3ugFErXMZ8LrLvF0GnoOpuPOPRhPG4T0A3BJriOKt_7mGVG2oer-dw/pubhtml?gid=0&single=true)

_Answers_
```
SELECT Event, COUNT(*)
FROM [sotorrent-org.2018_06_17.EditHistory]
WHERE PostId IN (
	SELECT PostId
	FROM [sotorrent-org.2018_06_17.Threads]
	WHERE ParentId = (
	  SELECT ParentID
	  FROM [sotorrent-org.2018_06_17.Threads]
	  WHERE PostId= <ANSWERID>
	)
)
AND TIMESTAMP(CreationDate) > TIMESTAMP(<COMMIT_TIME_STAMP>)
GROUP BY Event;
```
_Questions_
```
SELECT Event, COUNT(*)
FROM [sotorrent-org.2018_06_17.EditHistory]
WHERE PostId IN (
	SELECT PostId
	FROM [sotorrent-org.2018_06_17.Threads]
	WHERE ParentId = <QUESTIONID>
)
AND TIMESTAMP(CreationDate) > TIMESTAMP(<COMMIT_TIME_STAMP>)
GROUP BY Event;
```
### RQ6
- [Link decay](https://drive.google.com/file/d/1khPoSnqT-4g_caaLeaQWtSXEf9fkD6sJ/view?usp=sharing) - HTTP status codes for 382,650 distince links
### RQ7
- **Closed** 
  - https://github.com/BrowserSync/browser-sync/pull/1593
  - https://github.com/shirasagi/shirasagi/pull/2289
  - https://github.com/onepercentclub/bluebottle/pull/3372
  - https://github.com/ShipSoft/FairShip/pull/133
  - https://github.com/mutalyzer/mutalyzer/pull/454
  - https://github.com/sveawebpay/php-integration/pull/82
  - https://github.com/cms-sw/cmssw/pull/24370
  - https://github.com/BlackToppStudios/Mezzanine/pull/182
  - https://github.com/mockingbirdnest/Principia/pull/1905

- **Open**  
  - https://github.com/dzavalishin/phantomuserland/pull/468
  - https://github.com/refluster/lab/pull/12
  - https://github.com/densho/ddr-cmdln/pull/87
  - https://github.com/netzbasis/openbsd-src/pull/1
  - https://github.com/ci-bonfire/Bonfire/pull/1303

## Authors
- [Hideaki Hata](https://hideakihata.github.io/)
- [Christoph Treude](http://ctreude.ca/)
- [Raula Gaikovina Kula](https://raux.github.io/)
- [Takashi Ishio](https://takashi-ishio.github.io/)
