---
description: Parameter Kurven
ms.assetid: c073e7d0-c119-4c36-a5b2-b31dd6326ac8
title: Parameter Kurven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc3c482112c8bd76217f5cbdabdf3cda13b09c3e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125017"
---
# <a name="parameter-curves"></a>Parameter Kurven

Medien Parameter können im Laufe der Zeit eine Kurve verfolgen. Jede Kurve wird durch eine mathematische Formel und zwei Endpunkte beschrieben. Jeder Endpunkt wird durch eine Verweis Zeit und den Wert der Kurve zu diesem Zeitpunkt definiert. Die Formel wird verwendet, um Zwischenwerte zwischen den Punkten zu berechnen, und bestimmt die Form der Kurve. Mögliche Kurven:

-   Gelenks
-   Linear
-   Square
-   Umgekehrtes Quadrat
-   Ston

"Jump" bedeutet, dass Sie direkt zum Endwert springen. Die anderen Kurven werden im folgenden Diagramm dargestellt.

![Parameter Kurven](images/param-curves01.png)

Die Kurven funktionieren mathematisch wie folgt. Angenommen, eine Kurve beginnt bei Time *t*₀ mit dem Wert *v*₀ und endet mit Time *t*₁ mit dem Wert *v*₁. Die beiden Punkte, die die Kurve definieren, sind (*t*₀, *v*₀) und (*t*₁, *v*₁).

-   Legen Sie die Gesamtdauer der Kurve ( *t*₁ –*t*₀) ab.
-   *Lassen Sie* das Intervall zwischen den Anfangs-und Endwerten *v*₁ –*v*₀.
-   Zu einem beliebigen Zeitpunkt *t* , d. ₀. *t*<= *t*  <=  *t*₁, lassen Sie *t*' = t –*t*₀.

![Parameter Berechnung](images/param-curves02.png)

Der Wert des-Parameters zum Zeitpunkt *t* ist:

*v* = f (,*t*"/-*t* ) Version v \*   +  *v*₀

Dabei ist f (x) eine Funktion, die durch den Kurven-Typ bestimmt wird:

-   Linear: y = x
-   Quadrat: y = x ^ 2
-   Umgekehrtes Quadrat: y = sqrt (x)
-   Sinus: y = \[ Sin (-x – μ/2) + 1 \] /2

Beachten Sie,*dass "<-t"* lautet, sodass der Begriff "-*t"/*"*t* " zwischen 0 und *1 liegt.* Daher liegt f (x) auch zwischen 0 und 1, und *v* liegt immer zwischen *v*₀ und *v*₁. Dies gilt unabhängig davon, ob *v*₀ < *v*₁ oder umgekehrt. Das heißt, die Kurve wird durch das Rechteck (*t*₀, *v*₀, *t*₁, *v*₁) begrenzt.

Bei der Sinuskurve reicht der Wert von ("– x)/2" von "–./2" zu "-/2". Dies bedeutet, dass sich der Wert von "Sin (-x – μ/2)" von "– 1 bis 1" erstreckt. Das Ergebnis wird dann normalisiert, sodass f (x) in den Bereich (0 – 1) fällt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medien Parameter](media-parameters.md)
</dt> </dl>

 

 



