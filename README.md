# **SY09 Projet**

## **Jeu de données utilisé**

Prédiction de faillite d'entreprise : [Données financières de sociétés pour anticiper les risques de faillite](https://www.kaggle.com/datasets/fedesoriano/company-bankruptcy-prediction).

---

## Glossaire des Termes Financiers et Comptables

Liste de définitions qui facilitent la compréhension du jeu de données relatif à l'analyse de faillite.

### Actif  
Ensemble des ressources contrôlées par une entreprise. Cela inclut les biens physiques (immobilisations, stocks, équipements), les droits (créances, brevets) et tout autre élément ayant une valeur économique mesurable pouvant être converti en liquidités.

### Passif 
Ensemble des obligations financières d’une entreprise. Il s’agit notamment des dettes (à court terme et à long terme), des provisions pour risques et de toutes les charges à payer envers des tiers.

### Capitaux Propres 
Montant financé par les actionnaires (capital social, réserves, résultats non distribués). Ils représentent la valeur nette d’une entreprise une fois le passif soustrait à l’actif.

### Amortissement
Répartition du coût d’un actif immobilisé sur sa durée d’utilisation prévue. Permet de constater progressivement la dépréciation de la valeur d’un actif.

### Immobilisations
Biens durables destinés à rester dans l’entreprise sur le long terme. On distingue généralement les immobilisations corporelles (terrains, bâtiments, machines) et incorporelles (brevets, logiciels).

### Fonds de Roulement
Différence entre l’actif circulant (ressources à court terme) et le passif circulant (dettes à court terme). Cet indicateur mesure la capacité de l’entreprise à financer son cycle d’exploitation.

### Liquidité
Capacité de l’entreprise à répondre à ses obligations financières à court terme en convertissant rapidement ses actifs en trésorerie.

### Dette
Obligation de rembourser des sommes empruntées. On distingue généralement entre les dettes à court terme (remboursables dans l’année) et les dettes à long terme (échéance supérieure à un an).

### Ratio Financier
Indicateur calculé à partir des états financiers (bilan, compte de résultat) pour évaluer la performance, la solvabilité, la liquidité ou la rentabilité d’une entreprise. Par exemple : 
- Ratio d’endettement  
- Ratio de liquidité  
- ROA (*Return on Assets*)  
- ROE (*Return on Equity*)

### Valeur Comptable
Valeur d’un actif telle que comptabilisée dans les livres de l’entreprise, après déduction des amortissements. Pour les capitaux propres, c’est la somme des apports des actionnaires augmentée des résultats non distribués.

### Flux de Trésorerie
Mouvement de liquidités (entrées et sorties d’argent) sur une période donnée. Les flux de trésorerie permettent d’évaluer la capacité d'une entreprise à financer ses activités, rembourser ses dettes et réinvestir.

### Ratio d’Amortissement
Indicateur qui exprime la proportion des amortissements par rapport à l’actif ou au chiffre d’affaires. Il permet d’évaluer l’impact de la dépréciation des actifs sur la performance de l’entreprise.

---

# Description des variables du jeu de données

Ce jeu de données comporte 95 variables (X1 à X95) plus la variable **Y** (cible).  
La plupart sont des **ratios financiers** ou des **indicateurs** mesurant la santé de l’entreprise sous différents angles (rentabilité, liquidité, solvabilité, etc.).  

---

## catégorie des données

**Variable qualitatives** (binaire):
- Y (Bankrupt?)
- X85 (Liability-Assets Flag)
- X94 (Net Income Flag) => inutile car composé que de la même valeur pour toutes les variables

**Variables quantitatives** (tout le reste des variables)

---

## Liste de thèmes de variables

- Variable cible
- Solvabilité
- Structure du capital / endettement
- Rentabilité
- Efficacité / Rotation
- Flux de trésorerie
- Croissance
- Liquidité et structure de l’actif
- Autre indicateurs (je sais pas où les mettre ¯\_(ツ)_/¯)

---

## 1. Variable cible

1. **Y – Bankrupt?**  
   - Indique si l’entreprise est en faillite (**1**) ou non (**0**).  
   - **Type** : Qualitatif (binaire).

---

## 2. Solvabilité
  
> Ces variables évaluent la capacité globale de l’entreprise à honorer ses dettes, que ce soit via les actifs disponibles, la couverture des intérêts, ou encore la marge (gross margin). Elles englobent souvent des notions que l’on retrouve dans les « ratios de liquidité » et de « solvabilité ».

2. **X1 – ROA(C) before interest and depreciation before interest**  
   - Mesure le rendement des actifs avant paiement des intérêts et avant comptabilisation des amortissements. Indique la performance brute des actifs.  
   - **Type** : Quantitatif.

3. **X2 – ROA(A) before interest and % after tax**  
   - Rendement des actifs en tenant compte de l’imposition (après impôt) mais avant intérêts.  
   - **Type** : Quantitatif.

4. **X3 – ROA(B) before interest and depreciation after tax**  
   - Rendement des actifs après impôt, sans inclure les intérêts et amortissements dans les coûts.  
   - **Type** : Quantitatif.

5. **X4 – Operating Gross Margin**  
   - Marge brute d’exploitation (marge sur coûts directs) : proportion du chiffre d’affaires restant après le coût de production ou d’achat.  
   - **Type** : Quantitatif.

6. **X5 – Realized Sales Gross Margin**  
   - Marge brute « réalisée » sur les ventes : similaire à la marge brute mais peut différer selon la comptabilisation des ventes réelles.  
   - **Type** : Quantitatif.

7. **X6 – Operating Profit Rate**  
   - Taux de profit opérationnel : part du chiffre d’affaires qui se transforme en bénéfice d’exploitation.  
   - **Type** : Quantitatif.

8. **X7 – Pre-tax Net Interest Rate**  
   - Taux de bénéfice avant impôt : part des ventes qui se transforme en bénéfice avant impôt.  
   - **Type** : Quantitatif.

9. **X8 – After-tax Net Interest Rate**  
   - Taux de bénéfice net : part des ventes qui se transforme en bénéfice après impôt.  
   - **Type** : Quantitatif.

10. **X9 – Non-industry income and expenditure / revenue**  
    - Poids des revenus/dépenses hors activité principale rapportés au chiffre d’affaires.  
    - **Type** : Quantitatif.

11. **X10 – Continuous interest rate (after tax)**  
    - Rendement net « continu », hors éléments exceptionnels, après impôt, sur le chiffre d’affaires.  
    - **Type** : Quantitatif.

27. **X11 – Operating Expense Rate**  
    - Part du chiffre d’affaires dédiée aux dépenses d’exploitation.  
    - **Type** : Quantitatif.

28. **X12 – Research and development expense rate**  
    - Part du chiffre d’affaires investie en R&D.  
    - **Type** : Quantitatif.

29. **X13 – Cash flow rate**  
    - *(Flux de trésorerie opérationnel) / (Dettes à court terme)* : capacité à couvrir les dettes à court terme.  
    - **Type** : Quantitatif.

12. **X19 – Persistent EPS in the Last Four Seasons**  
    - Bénéfice par action (EPS) « persistant » sur 4 trimestres (souvent hors éléments non-récurrents).  
    - **Type** : Quantitatif.

18. **X20 – Cash Flow Per Share**  
    - Flux de trésorerie opérationnel divisé par le nombre d’actions (indique la capacité à générer du cash par action).  
    - **Type** : Quantitatif.

19. **X68 - Retained Earnings to Total Assets**  
    - Indique la proportion des bénéfices non distribués par rapport aux actifs totaux. 
    - **Type** : Quantitatif.

---

## 3. Structure du capital / endettement
 
> Indicateurs portant sur la structure financière (poids de la dette vs. capitaux propres, dépendance à l’emprunt, levier financier). Ils permettent d’évaluer comment l’entreprise se finance à moyen/long terme.

47. **X14 – Interest-bearing debt interest rate**  
   - *(Dettes portant intérêt) / (Equity)* : poids de la dette rémunérée dans les capitaux propres.  
   - **Type** : Quantitatif.

48. **X35 – Interest Expense Ratio**  
   - *(Frais d’intérêts) / (Chiffre d’affaires)* : coût de la dette par rapport aux ventes.  
   - **Type** : Quantitatif.

49. **X36 – Total debt / Total net worth**  
   - Rapport entre la dette totale et la valeur nette de l’entreprise.  
   - **Type** : Quantitatif.

50. **X37 – Debt ratio %**  
   - *(Total dettes) / (Total actifs)* : part de l’actif financée par la dette.  
   - **Type** : Quantitatif.

51. **X38 – Net worth / Assets**  
   - *(Capitaux propres) / (Actifs)* : part de l’actif financée par les fonds propres.  
   - **Type** : Quantitatif.

52. **X39 – Long-term fund suitability ratio (A)**  
   - *(Dettes à long terme + Capitaux propres) / (Immobilisations)* : indique la couverture des actifs à long terme par des ressources longues.  
   - **Type** : Quantitatif.

53. **X40 – Borrowing dependency**  
   - Mesure la dépendance à l’endettement portant intérêt (souvent un ratio sur le total des dettes).  
   - **Type** : Quantitatif.

54. **X41 – Contingent liabilities / Net worth**  
   - Poids des engagements hors bilan (dettes potentielles) rapportés aux capitaux propres.  
   - **Type** : Quantitatif.

55. **X85 – Liability-Assets Flag**  
   - Indicateur binaire : **1** si l’entreprise a plus de dettes que d’actifs, **0** sinon.  
   - **Type** : Qualitatif (binaire).

56. **X91 – Liability to Equity**  
   - *(Total dettes) / (Capitaux propres)* : ratio d’endettement classique.  
   - **Type** : Quantitatif.

57. **X92 – Degree of Financial Leverage (DFL)**  
   - Mesure la sensibilité du bénéfice net aux variations du bénéfice d’exploitation (impact des charges d’intérêt).  
   - **Type** : Quantitatif.

58. **X93 – Interest Coverage Ratio**  
   - Souvent *(EBIT) / (Frais d’intérêts)* : capacité à payer les intérêts de la dette via le résultat d’exploitation.  
   - **Type** : Quantitatif.

59. **X94 – Net Income Flag**  
   - Indicateur binaire : **1** si l’entreprise a un résultat net négatif deux années consécutives, **0** sinon.  
   - **Type** : Qualitatif (binaire).

60. **X95 – Equity to Liability**  
   - *(Capitaux propres) / (Dettes)* : inverse d’un ratio d’endettement.  
   - **Type** : Quantitatif.

---

## 4. Rentabilité
 
> Ratios qui évaluent dans quelle mesure l’entreprise génère des bénéfices à partir de ses ressources (actifs, capital, ventes…).

13. **X42 – Operating profit / Paid-in capital**  
    - Compare le bénéfice d’exploitation au capital versé par les actionnaires.  
    - **Type** : Quantitatif.

14. **X43 – Net profit before tax / Paid-in capital**  
    - Compare le bénéfice avant impôt au capital versé.  
    - **Type** : Quantitatif.

15. **X86 – Net Income to Total Assets**  
    - Bénéfice net / Actifs totaux (un ratio de rentabilité).  
    - **Type** : Quantitatif.

16. **X89 – Gross Profit to Sales**  
    - Marge brute sur ventes : part du chiffre d’affaires restant après le coût direct des produits vendus.  
    - **Type** : Quantitatif.

17. **X90 – Net Income to Stockholder’s Equity**  
    - Rendement des capitaux propres (ROE) : *bénéfice net / fonds*.  
    - **Type** : Quantitatif.

---

## 5. Efficacité / rotation
  
> Indicateurs de la vitesse de rotation (stocks, créances, etc.) et de la productivité (ventes par employé…), utiles pour juger l’efficacité opérationnelle de l’entreprise.

61. **X44 – Inventory and accounts receivable / Net value**  
    - *(Stocks + Créances clients) / (Capitaux propres)* : mesure l’importance du BFR par rapport aux fonds propres.  
    - **Type** : Quantitatif.

62. **X45 – Total Asset Turnover**  
    - *(Ventes) / (Actifs totaux)* : vitesse de rotation des actifs (combien d’euros de ventes pour 1€ d’actif).  
    - **Type** : Quantitatif.

63. **X46 – Accounts Receivable Turnover**  
    - *(Ventes) / (Créances clients)* : rapidité de recouvrement des créances.  
    - **Type** : Quantitatif.

64. **X47 – Average Collection Days**  
    - Nombre moyen de jours nécessaire pour encaisser les ventes à crédit (délais clients).  
    - **Type** : Quantitatif.

65. **X48 – Inventory Turnover Rate**  
    - *(Coût des ventes) / (Stock moyen)* : vitesse à laquelle les stocks sont vendus et renouvelés.  
    - **Type** : Quantitatif.

66. **X49 – Fixed Assets Turnover Frequency**  
    - *(Ventes) / (Actifs immobilisés)* : efficacité d’utilisation des immobilisations pour générer des ventes.  
    - **Type** : Quantitatif.

67. **X50 – Net Worth Turnover Rate**  
    - *(Ventes) / (Capitaux propres)* : indique combien d’euros de ventes sont générés par 1€ de fonds propres.  
    - **Type** : Quantitatif.

68. **X51 – Revenue per person**  
    - *(Ventes) / (Nombre d’employés)* : productivité commerciale par employé.  
    - **Type** : Quantitatif.

69. **X52 – Operating profit per person**  
    - *(Bénéfice d’exploitation) / (Nombre d’employés)* : productivité opérationnelle par employé.  
    - **Type** : Quantitatif.

70. **X53 – Allocation rate per person**  
    - *(Actifs immobilisés) / (Nombre d’employés)* : montant d’investissements (actifs fixes) par employé.  
    - **Type** : Quantitatif.

71. **X71 – Current Asset Turnover Rate**  
    - *(Ventes) / (Actifs à court terme)* : vitesse d’utilisation des actifs circulants pour générer des ventes.  
    - **Type** : Quantitatif.

72. **X72 – Quick Asset Turnover Rate**  
    - *(Ventes) / (Actifs liquides)* : vitesse de rotation des actifs très rapidement mobilisables (cash, créances).  
    - **Type** : Quantitatif.

73. **X73 – Working Capital Turnover Rate**  
    - *(Ventes) / (Fonds de roulement)* : combien de chiffre d'affaire est généré par le fonds de roulement.  
    - **Type** : Quantitatif.

74. **X74 – Cash Turnover Rate**  
    - *(Ventes) / (Trésorerie)* : vitesse de rotation de la trésorerie.  
    - **Type** : Quantitatif.

---

## 6. Flux de trésorerie
 
> Ces indicateurs portent sur les flux de trésorerie (CFO) : la part de cash générée, sa répartition, et la capacité à rembourser la dette par ces flux.

75. **X32 – Cash Reinvestment %**  
    - Pourcentage de trésorerie réinvesti (souvent après dividendes).  
    - **Type** : Quantitatif.

76. **X75 – Cash Flow to Sales**  
    - *(Flux de trésorerie opérationnel) / (Ventes)* : part du chiffre d'affaire convertie en cash.  
    - **Type** : Quantitatif.

77. **X80 – Cash Flow to Total Assets**  
    - *(Flux de trésorerie opérationnel) / (Actifs totaux)* : capacité à générer du cash par rapport à la taille de l’entreprise.  
    - **Type** : Quantitatif.

78. **X81 – Cash Flow to Liability**  
    - *(Flux de trésorerie opérationnel) / (Dettes totales)* : capacité à rembourser la dette par le flux d’exploitation.  
    - **Type** : Quantitatif.

79. **X82 – CFO to Assets**  
    - Variante proche de X80 : *(Cash Flow from Operations / Actifs)*.  
    - **Type** : Quantitatif.

80. **X83 – Cash Flow to Equity**  
    - *(Flux de trésorerie opérationnel) / (Capitaux propres)* : capacité à rémunérer les actionnaires via le cash.  
    - **Type** : Quantitatif.

---

## 7. Croissance
 
> Les ratios de croissance montrent l’évolution temporelle (sur plusieurs exercices) des ventes, des bénéfices, des actifs, etc.

19. **X24 – Realized Sales Gross Profit Growth Rate**  
    - Taux de croissance de la marge brute réalisée sur les ventes, d’une période à l’autre.  
    - **Type** : Quantitatif.

20. **X25 – Operating Profit Growth Rate**  
    - Taux de croissance du profit d’exploitation.  
    - **Type** : Quantitatif.

21. **X26 – After-tax Net Profit Growth Rate**  
    - Taux de croissance du bénéfice net après impôt.  
    - **Type** : Quantitatif.

22. **X27 – Regular Net Profit Growth Rate**  
    - Taux de croissance du bénéfice net récurrent (hors éléments exceptionnels).  
    - **Type** : Quantitatif.

23. **X28 – Continuous Net Profit Growth Rate**  
    - Taux de croissance du bénéfice net en excluant les gains ou pertes de cession exceptionnels.  
    - **Type** : Quantitatif.

24. **X29 – Total Asset Growth Rate**  
    - Taux de croissance du total des actifs.  
    - **Type** : Quantitatif.

25. **X30 – Net Value Growth Rate**  
    - Taux de croissance de la valeur nette (capitaux propres).  
    - **Type** : Quantitatif.

26. **X31 – Total Asset Return Growth Rate Ratio**  
    - Mesure l’évolution du rendement des actifs (comparaison de ROA sur plusieurs périodes).  
    - **Type** : Quantitatif.

---

## 8. Liquidité et structure de l’actif

> Variables portant spécifiquement sur la répartition de l’actif (stocks, trésorerie, créances), la capacité à faire face aux dettes à **court terme** et les liens entre fonds de roulement, actifs, etc.

30. **X33 – Current Ratio**  
    - *(Actifs à court terme) / (Passifs à court terme)* : solvabilité à court terme.  
    - **Type** : Quantitatif.

31. **X34 – Quick Ratio (Acid Test)**  
    - *(Actifs à court terme – Stocks) / (Passifs à court terme)* : liquidité immédiate (plus strict que le Current Ratio).  
    - **Type** : Quantitatif.

32. **X54 – Working Capital to Total Assets**  
    - *(Fonds de roulement) / (Actifs totaux)*.  
    - **Type** : Quantitatif.

33. **X55 – Quick Assets / Total Assets**  
    - Proportion d’actifs immédiatement liquides (trésorerie, créances) dans l’actif total.  
    - **Type** : Quantitatif.

34. **X56 – Current Assets / Total Assets**  
    - Part des actifs à court terme (stocks, créances, trésorerie) dans l’actif total.  
    - **Type** : Quantitatif.

35. **X57 – Cash / Total Assets**  
    - Part de trésorerie dans l’actif total.  
    - **Type** : Quantitatif.

36. **X58 – Quick Assets / Current Liability**  
    - Rapport entre les actifs liquides et les dettes à court terme.  
    - **Type** : Quantitatif.

37. **X59 – Cash / Current Liability**  
    - Rapport entre la trésorerie et les dettes à court terme.  
    - **Type** : Quantitatif.

38. **X60 – Current Liability to Assets**  
    - Poids des dettes à court terme dans l’actif total.  
    - **Type** : Quantitatif.

39. **X61 – Operating Funds to Liability**  
    - Mesure la part des ressources d’exploitation (souvent le fonds de roulement) par rapport à l’ensemble des dettes.  
    - **Type** : Quantitatif.

40. **X62 – Inventory / Working Capital**  
    - Proportion des stocks dans le fonds de roulement.  
    - **Type** : Quantitatif.

41. **X63 – Inventory / Current Liability**  
    - Poids des stocks par rapport aux dettes à court terme.  
    - **Type** : Quantitatif.

42. **X64 – Current Liabilities / Liability**  
    - Proportion de la dette totale qui est à court terme.  
    - **Type** : Quantitatif.

43. **X65 – Working Capital / Equity**  
    - Fonds de roulement rapporté aux capitaux propres.  
    - **Type** : Quantitatif.

44. **X66 – Current Liabilities / Equity**  
    - Rapport entre les dettes à court terme et les capitaux propres.  
    - **Type** : Quantitatif.

45. **X67 – Long-term Liability to Current Assets**  
    - Dettes à long terme par rapport aux actifs à court terme (liquidités, créances, stocks).  
    - **Type** : Quantitatif.

46. **X84 – Current Liability to Current Assets**  
    - Inverse du Current Ratio : *(Dettes CT) / (Actifs CT)*.  
    - **Type** : Quantitatif.

---

## 9. Autres indicateurs
 
> Indicateurs qui ne rentrent pas aisément dans les catégories ci‑dessus : taux d’imposition effectif, valeur par action selon différents référentiels, part des dépenses dans l’actif, etc.

81. **X15 – Tax rate (A)**  
    - Taux d’imposition effectif de l’entreprise.  
    - **Type** : Quantitatif.

82. **X16 – Net Value Per Share (B)**  
    - Valeur comptable par action (version B) : capitaux propres / nombre d’actions.  
    - **Type** : Quantitatif.

83. **X17 – Net Value Per Share (A)**  
    - Idem, version A (possiblement un autre référentiel comptable).  
    - **Type** : Quantitatif.

84. **X18 – Net Value Per Share (C)**  
    - Idem, version C.  
    - **Type** : Quantitatif.

85. **X21 – Revenue Per Share (Yuan ¥)**  
    - Ventes par action : chiffre d’affaires / nombre d’actions.  
    - **Type** : Quantitatif.

86. **X22 – Operating Profit Per Share (Yuan ¥)**  
    - Bénéfice d’exploitation par action.  
    - **Type** : Quantitatif.

87. **X23 – Per Share Net profit before tax (Yuan ¥)**  
    - Bénéfice avant impôt par action.  
    - **Type** : Quantitatif.

89. **X69 – Total income / Total expense**  
    - Rapport global revenus/dépenses, indicateur de couverture des coûts.  
    - **Type** : Quantitatif.

88. **X70 – Total expense / Assets**  
    - Part des dépenses totales dans l’actif : indique le poids des charges sur la structure de l’entreprise.  
    - **Type** : Quantitatif.

90. **X76 – Fixed Assets to Assets**  
    - Part des immobilisations (bâtiments, machines) dans l’actif total.  
    - **Type** : Quantitatif.

91. **X77 – Current Liability to Liability**  
    - Part des dettes à court terme dans l’ensemble des dettes (similaire à X64, selon définitions).  
    - **Type** : Quantitatif.

92. **X78 – Current Liability to Equity**  
    - Dettes à court terme / Capitaux propres (similaire à X66).  
    - **Type** : Quantitatif.

93. **X79 – Equity to Long-term Liability**  
    - Compare les capitaux propres aux dettes à long terme.  
    - **Type** : Quantitatif.

94. **X87 – Total assets to GNP price**  
    - Compare la taille de l’entreprise (total des actifs) au PIB/GNP (place de la société dans l’économie).  
    - **Type** : Quantitatif.

95. **X88 – No-credit Interval**  
    - Nombre de jours pendant lesquels l’entreprise peut fonctionner sans emprunter (basé sur la trésorerie et les dépenses).  
    - **Type** : Quantitatif.
# utc_sy09_projet
