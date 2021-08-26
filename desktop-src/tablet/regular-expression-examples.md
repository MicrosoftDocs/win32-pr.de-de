---
description: Die folgenden Beispiele zeigen einige handschriftliche reguläre Ausdrücke, die Sie erstellen können.
ms.assetid: b4954e05-64d0-434a-96fd-6185671252d0
title: Beispiele für reguläre Ausdrücke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d1f3ac4428058a2c74b0285cd52c13a265b92c3379cef1f2ae8b2f35e19fbff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934690"
---
# <a name="regular-expression-examples"></a>Beispiele für reguläre Ausdrücke

Die folgenden Beispiele zeigen einige handschriftliche reguläre Ausdrücke, die Sie erstellen können.



| Ausdruck                                                                                                                                                                                                                                                                                  | BESCHREIBUNG                                                                                                                                                               | Treffer                                                                          | Nicht übereinstimmende                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-------------------------------------------|
| s(!IS \_ ONECHAR)+p<br/>                                                                                                                                                                                                                                                                | Entspricht jedem Wort, das mit Kleinbuchstaben "s" beginnt, ein oder mehrere Zeichen enthält (wie durch den IS \_ ONECHAR-Eingabebereich definiert), und endet mit einem Kleinbuchstaben "p".<br/> | stop<br/> Suppe<br/> Schlep<br/> s234p<br/>               | Beenden<br/> sp<br/>             |
| (0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9)<br/>                                                                                                                                                                                                                                                   | Entspricht einer beliebigen einstelligen Zahl von 1 bis 9.<br/>                                                                                                                         | 1<br/> 6<br/> 0<br/>                                           | 42<br/> Einen<br/>              |
| (0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9 \| , \| -)+<br/>                                                                                                                                                                                                                                            | Entspricht einer oder mehreren einstelligen Ziffern, Kommas oder Bindestrichen. Nützlich zum Beschränken der Eingabe auf einen Bereich oder eine Reihe von Zahlen, z. B. einen Bereich von Seiten, die gedruckt werden sollen.<br/>               | 1<br/> 1-6<br/> 2,4,7<br/> 2-6,9,135<br/> ,,,<br/> | drei<br/> 7 bis 9<br/>   |
| (0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9)(0 \| 1 \| 2 \| 3 \| \| 4 \| 6 \| 7 \| 8 \| 9)(0 \| 1 \| 2 \| \| 3 \| 4 \| 5 6 \| 7 \| 8 \| 9)-(0 \| 1 \| 2 \| \| 3 4 \| \| 5 \| 6 \| 7 8 \| 9)(0 \| 1 \| 2 \| \| 3 4 \| 4) \| 5 6 \| 7 \| 8 \| 9)-(0 \| 1 \| 2 \| \| 3 \| 4 \| 5 6 \| 7 \| 8 \| 9)(0 \| 1 \| \| 2 3 \| \| 4 \| 5 \| 6 \| 7 8 \| 9)(0 \| 1 \| 2 \| 3 \| 4 \| \| 5 \| 7 \| 8 \| 9)(0 \| 1 \| 2 \| 3 \| 4 \| 5 \| \| 7 \| 8 \| 9)<br/> | Eine Sozialversicherungsnummer. Das Format einer Sozialversicherungsnummer ist *nnn*  -  *nn nn*  -  *nnnn*.<br/>                                                                     | 123-45-6789<br/>                                                           | 12-123-12<br/> 12-2-3456<br/> |



 

 

 




