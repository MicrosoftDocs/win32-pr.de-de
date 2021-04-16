---
description: Übergangs Richtung
ms.assetid: d18525de-bb75-4c5e-b387-cfec7ba03df7
title: Übergangs Richtung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01d43ec4258d2f23c8b8961e3e1b8fd3d554b057
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104553564"
---
# <a name="transition-direction"></a>Übergangs Richtung

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

Ein Übergang wechselt von Eingabe a zu Eingabe B und von time t ₀ zu t ₁. Daher kann die *Richtung* eines Übergangs eine von zwei Faktoren bedeuten:

-   Die Zuordnung von Zeitachsen Ebenen zu Eingaben.
-   Der Fortschritt im Laufe der Zeit.

Der erste ist die *Eingabe Richtung*, die zweite ist die Status *Richtung*. Beide Richtungen können gesteuert werden.

-   Eingabe Richtung: Standardmäßig geht ein Übergang von der zusammengesetzten der Ebenen mit niedrigerer Priorität zur Ebene, die den Übergang enthält. Um diese Richtung umzukehren, nennen Sie die [**iamtimelinetrans:: setionwapinputs**](iamtimelinetrans-setswapinputs.md) -Methode.
-   Fortschritts Richtung: die meisten Übergänge unterstützen **eine Standardstatus** Eigenschaft, die angibt, welcher Prozentsatz des Übergangs in der Ausgabe zu einem bestimmten Zeitpunkt reflektiert wird. Standardmäßig geht der **Wert der Status-Eigenschaft während** der Übergangs Dauer von 0,0 auf 1,0. Um den Fortschritt umzukehren, legen Sie die Status **-Eigenschaft auf** Go von 1,0 auf 0,0 fest.

Im folgenden Diagramm wird der Unterschied zwischen Eingabe Richtung und Fortschritt Richtung veranschaulicht. Es zeigt vier Abweichungen bei einem standardmäßigen [SMPTE](smpte-wipe-transition.md) -Umleitungs Übergang.

![Anweisungen zum Löschen](images/wipedirections.png)

Der Übergang befindet sich auf der Spur 1. Standardmäßig wechselt die zurück Löschung von links nach rechts und von Track 0 zur Nachverfolgung 1. Das Austauschen von Eingaben bewirkt, dass die zurück Löschung von der Spur 1 zur Nachverfolgung von 0, aber von links nach rechts, ausgelöst wird. Wenn Sie den Fortschritt umkehren, wechselt der Übergang von rechts nach links. Sie können beides kombinieren, wie in der linken Abbildung gezeigt.

Weitere Informationen zum Rendern von Übergängen durch des finden Sie [im Zeitachsen Modell](the-timeline-model.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Effekten und Übergängen](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



