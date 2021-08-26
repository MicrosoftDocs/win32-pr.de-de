---
description: Parameterkurven
ms.assetid: c073e7d0-c119-4c36-a5b2-b31dd6326ac8
title: Parameterkurven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5130cf158271ffe3cb3da5e4e16b5fffa8a5a6994b14b9f8766fe20cdf1510ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997380"
---
# <a name="parameter-curves"></a>Parameterkurven

Medienparameter können einer Kurve im Laufe der Zeit folgen. Jede Kurve wird durch eine mathematische Formel und zwei Endpunkte beschrieben. Jeder Endpunkt wird durch eine Bezugszeit und den Wert der Kurve zu diesem Zeitpunkt definiert. Die Formel wird verwendet, um Zwischenwerte zwischen den Punkten zu berechnen und die Form der Kurve zu bestimmen. Die möglichen Kurven sind:

-   Springen
-   Linear
-   Square
-   Inverses Quadrat
-   Sinus

"Springen" bedeutet, direkt zum Endwert zu springen. Die anderen Kurven sind im folgenden Diagramm dargestellt.

![Parameterkurven](images/param-curves01.png)

Mathematisch funktionieren die Kurven wie folgt. Angenommen, eine Kurve beginnt zu dem Zeitpunkt *₀* mit dem Wert *v*₀ und endet zu dem Zeitpunkt, zu dem *t*₁ mit dem Wert *v*₁. Die beiden Punkte, die die Kurve definieren, sind (*t*₀, *v*₀) und (*t*₁, *v*₁).

-   Lassen Sie ^*nicht* die Gesamtdauer der Kurve, *t*₁–*t ₀.*
-   Lassen Sie ^*v* das Intervall zwischen den Anfangs- und Endwerten sein, *v*₁–*v*₀.
-   Lassen Sie *zu jedem* *Zeitpunkt* t, ₀ <= *t*  <=  *t ₁* ist, LASS *t*' = *t*–*t*₀.

![Parameterberechnung](images/param-curves02.png)

Der Wert des Parameters zum Zeitpunkt *t* ist:

*v* = f( ^*t*' / Y *t* ) \* ); v *v*  +  *₀*

Dabei ist f(x) eine Funktion, die durch den Kurventyp bestimmt wird:

-   Linear: y = x
-   Square: y = x^2
-   Inverses Quadrat: y = sqrt(x)
-   Sinus: y = \[ sin(πx – π/2) + 1 \] / 2

Beachten Sie, dass *^t*' < ^*t ist,* sodass der Begriff ^*t*'/ ^*t t* zwischen 0 und 1 liegt. Daher liegt f(x) auch zwischen 0 und 1, und *v* liegt immer zwischen *v*₀ *und v*₁. Dies gilt unabhängig davon, ob *v*₀ < *v*₁ oder umgekehrt. Anders ausgedrückt: Die Kurve wird durch das Rechteck *(t*₀, *v*₀, *t*₁, *v*₁) gebunden.

Für die Sinuskurve liegt der Wert von (πx – π/2) zwischen –π/2 und π/2, was bedeutet, dass sin(πx – π/2) zwischen –1 und 1 liegt. Das Ergebnis wird dann normalisiert, sodass f(x) in den Bereich (0–1) fällt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medienparameter](media-parameters.md)
</dt> </dl>

 

 



