# 对PNAS Paper: Flat teams drive scientific innovation提供的数据的尝试
## **1. 总结**
>
PNAS paper里的data没法直接用，原因有两个：①PLOS data做了预处理，聚合为了五大类贡献，**但是没有 recources 这个类**；②其他三个期刊只有contribution的**原文且十分具体**，需要进一步预处理。PNAS的贡献声明相当简略（和聚合后的PLOS ONE 差不多），Nature和Science的非常具体，没有明显的类别。所以必须去看**PLOS ONE本身**的数据，即含Resources的。

## **2. PNAS paper (2022) 数据的概要**
数据由Flat teams drive scientific innovation提供，包含89,575条研究活动（PNAS, Nature, Science, and PLOS ONE from 2003 to 2020），包括作者贡献，其主要研究对象是leadership（一个研究中，领导者角色的比例，~0.4）。用89K的实际的data，推断了16M没有明确作者贡献的文献（1950-2015，作者数量>=2的文献）。
> 
**2.1 数据的收录范围**
PNAS (18,354 during 2003–2015)
Nature (9,364 during 2006–2020)
Science (1,176 during 2018–2020)
PLOS ONE (60,681 during 2006–2014)


**2.2 其他和author contribution contribution相关的data/study**
C. Haeussler, H. Sauermann, Division of labor in collaborative knowledge production: The role of team size and interdisciplinarity. Res. Policy 49, 103987 (2020).
V. Lariviere ` et al., Contributorship and division of labor in knowledge production. Social Stud. Sci. 46,417–435 (2016).


**2.3 下面总结PNAS paper (2022) 中，各期刊的contribution data的结构**

Flat teams drive scientific innovation提供的contribution data很原始，并没有很好的清洗过。

> 
**2.3.1 PLOS ONE**

数据是半结构化的，但是没有resources。 这个文档的**最后**会有进一步说明。

example 1
>{'performed experiment': ['TS', 'MG'], 
'analyzed data': ['TS'], 
'conceived designed experiment': ['TS'], 
'wrote paper': ['TS']}

example 2
> {'performed experiment': ['RB-P', 'AM', 'RN', 'LC', 'DM', 'AC', 'MS'], 
'analyzed data': ['RB-P', 'AM', 'RN'], 
'conceived designed experiment': ['FM', 'GM'], 
'contributed reagent material analysis tool': ['RB-P', 'AM']}

example 3
> {'performed experiment': ['JMS', 'VBM'], 
'analyzed data': ['JMS', 'VBM'], 
'conceived designed experiment': ['JMS', 'VBM'], 
'contributed reagent material analysis tool': ['JMS', 'VBM']}

**Nature**

非结构化，贡献说明很具体。

example 1
>P.F.W. designed and performed the numerical simulations, created the graphical outputs, and drafted the manuscript. S.K.A. conceived the investigation, consulted on the simulations, and revised the manuscript. C.R.D. developed the numerical model, assisted in designing the experiments, acquired the computer resources required, and revised the manuscript.

example 2
> T.Y. and H.S. designed, performed, and analysed all experiments and wrote the manuscript. M.I.-K., T.G., H.H., M.S., T.K., A.Y., and A.U. performed embryo manipulation. N.M. performed data analysis. Y.O. performed histopathological analysis. S.H. performed establishment of iPSCs. H.M. performed data analysis. D.T.R. wrote the manuscript. M.H. performed embryo manipulation and data analysis. H.N. designed the study and wrote the manuscript.

example 3
> E.S., J.-L.T. and A.I. planned the project. E.S. and A.I. designed, analysed and interpreted data and wrote the manuscript. E.S., L.S.B.B. and T.M. performed experiments and analysed data. H.D. bred and cared for mice. J.-L.T. provided AAV material. S.A., M.B. and K.A. provided expertise, materials and analysis of data.

**Science**

和Nature的情况很类似
> 
example 1

> K.S. generated cell lines, established cell synchronization protocols, performed synchronized time courses, and performed imaging analyses. J.H.G. and N.N. performed Hi-C analyses. A.G. and J.N. performed polymer simulations. L.A.M. and A.G. designed and analyzed coarse-grained models, with A.G. serving as the lead modeler. A.G. analyzed condensin ChIP data. L.X. and J.R.P. prepared 1NM-PP1. I.S. performed chromatin-enriched proteomics analyses. M.T.K. provided constructs for cell line engineering. A.G., J.H.G., K.S., J.N., W.C.E., L.A.M., and J.D. designed the project and analyzed the data. All authors contributed to writing the manuscript.
> 
example 2

> R.W. conceived the study, oversaw data collection, led the conceptual development, and wrote the manuscript. J.R.R. performed the analysis and prepared the figures. J.R.R., N.M.W., I.B., and D.P.C. contributed to the conceptual development. D.P.C. led field work and collected data. J.G. identified pollinators. J.R.R., N.M.W., I.B., D.P.C., and J.G. commented on the manuscript.

example 3

> D.K., D.J.S., and S.O. conceptualized the pure reconstitution and developed the methodology; D.J.S., S.O., R.X., R.J.T, and A.H.G. performed validation and investigation for the reconstitution. D.K., R.X., R.J.T., and A.H.G. conceptualized flow cytometry of the proteoliposomes. R.X., R.J.T., and A.H.G. developed the flow cytometry methodology and performed validation and investigations. D.K., D.J.N., R.X., R.J.T., and A.H.G. conceptualized the confocal microscopy. R.X., R.J.T., A.H.G., and P.J.F. developed the confocal microscopy methodology and performed validation and investigations. Resources were provided by D.K. and D.J.N. D.K., R.X., R.J.T. D.J.S., and A.H.G. wrote the manuscript, and all authors contributed edits. D.K. and D.J.N administered the project and acquired funding.

**PNAS**

非结构化，和本文聚合的PLOS ONE的结果类似

example 1

> M.R.K. and D.E.A. designed research; M.R.K., R.E.L., and S.K. performed research; R.E.L. contributed new reagents/analytic tools; M.R.K. and D.E.A. analyzed data; and M.R.K. and D.E.A. wrote the paper.

example 2

> S.N., J.K.-V., H.F., and J.F. designed research; S.N., J.K.-V., S.R., M.F., T.D., and T.P. performed research; S.N., J.K.-V., S.R., T.U., A.N., M.C.E.V.M., and J.F. analyzed data; and S.N., J.K.-V., S.R., T.D., H.F., and J.F. wrote the paper.

example 3

> H.S.K., V.L.D., and T.M.D. designed research; H.S.K., Y.L., J.-H.S., S.S.K., and B.S.G. performed research; A.J.K., O.P., and J.C.T. contributed new reagents/analytic tools; H.S.K., Y.L., J.-H.S., S.S.K., V.L.D., and T.M.D. analyzed data; and H.S.K., V.L.D., and T.M.D. wrote the paper.

## 3. 对PNAS Paper提供的data的一些简单分析
**PLOS ONE 作者团队规模**

60,681 篇文章 during 2006–2014


合著者人数|文章数
| --- | ------ |
1 | 0
2 | 5204
3 | 7928
4 | 8847
5 | 8939
6 | 7730
7 | 6708
8 | 5358
9 | 4064
10 | 3031
11 | 2043
12 | 1457
13 | 922
14 | 683
15 | 469
··· | ···
56 | 1
**PLOS ONE文献里提及某类贡献的比例，64383篇文章（有96.5%的文章有performed experiment记录）**
|贡献类型 | 比例 |
| --- | ------ |
performed experiment | 0.965
analyzed data | 0.994
conceived designed experiment | 0.988
wrote paper | 0.943
contributed reagent material analysis tool | 0.751
revised manuscript | 0.005

**PLOS ONE提及贡献的比例（统计人数，即每种贡献平均占一篇文章作者数的%多少）**
|贡献类型 | 比例 |
| --- | ------ |
performed experiment | 0.529
analyzed data | 0.553
conceived designed experiment | 0.502
wrote paper | 0.470
contributed reagent material analysis tool | 0.373
revised manuscript | 0.003



**PLOS ONE 提及贡献的比例（统计人次）**

|贡献类型 | 比例 |
| --- | ------ |
performed experiment | 0.218
analyzed data | 0.228
conceived designed experiment | 0.206
wrote paper | 0.194
contributed reagent material analysis tool | 0.153
revised manuscript | 0.001



