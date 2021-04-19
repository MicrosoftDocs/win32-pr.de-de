---
description: Die folgenden Beispiele zeigen einige reguläre Ausdrücke, die Sie erstellen können.
ms.assetid: b4954e05-64d0-434a-96fd-6185671252d0
title: Beispiele für reguläre Ausdrücke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11fe207be6378754bfe4b3e504d51e6ff49cadba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366171"
---
# <a name="regular-expression-examples"></a>Beispiele für reguläre Ausdrücke

Die folgenden Beispiele zeigen einige reguläre Ausdrücke, die Sie erstellen können.



| Ausdruck                                                                                                                                                                                                                                                                                  | BESCHREIBUNG                                                                                                                                                               | Treffer                                                                          | Nicht übereinstimmende                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-------------------------------------------|
| s (! ist \_ OneChar) + p<br/>                                                                                                                                                                                                                                                                | Entspricht einem beliebigen Wort, das mit einem Kleinbuchstaben beginnt, mindestens ein Zeichen enthält (wie durch den \_ OneChar-Eingabebereich definiert), und endet mit einem Kleinbuchstaben "p".<br/> | stop<br/> Suppe<br/> Schlep<br/> s234p<br/>               | Stop<br/> sp<br/>             |
| (0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9)<br/>                                                                                                                                                                                                                                                   | Entspricht einer beliebigen einzelnen Ziffer, 1 bis 9.<br/>                                                                                                                         | 1<br/> 6<br/> 0<br/>                                           | 42<br/> Eine<br/>              |
| (0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9 \| , \| -) +<br/>                                                                                                                                                                                                                                            | Findet eine Entsprechung für eine oder mehrere Ziffern, Kommas oder Bindestriche. Nützlich, um die Eingabe auf einen Bereich oder eine Reihe von Zahlen zu beschränken, z. b. einen Seitenbereich, der gedruckt werden soll.<br/>               | 1<br/> 1-6<br/> 2, 4, 7<br/> 2-6, 9135<br/> ,,,<br/> | drei<br/> 7 bis 9<br/>   |
| (0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9) (0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9) (0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 7 8 9) \| \| \| -(0 1 2 \| \| \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9) (0 1 2 3 4 5 \| \| \| \| \| \| 6 \| 7 \| 8 \| 9)-(0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9) (0 1 2 3 4 \| \| \| \| \| 5 \| 6 \| 7 \| 8 9) (0 1 2 3 4 \| \| \| \| \| \| 5 \| 6 \| 7 8 9) \| \| (0 \| 1 \| 2 \| 3 \| 4 \| 5 \| 6 \| 7 \| 8 \| 9)<br/> | Eine Sozialversicherungsnummer. Das Format einer Sozialversicherungsnummer ist *nnn*  -  *NN*  -  *nnnn*.<br/>                                                                     | 123-45-6789<br/>                                                           | 12-123-12<br/> 12-2-3456<br/> |



 

 

 




