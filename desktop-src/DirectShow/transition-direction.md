---
description: Übergangsrichtung
ms.assetid: d18525de-bb75-4c5e-b387-cfec7ba03df7
title: Übergangsrichtung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2097f13225c7691780646d77a18d048a48e31eda498955bdc53a0c954728c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951493"
---
# <a name="transition-direction"></a>Übergangsrichtung

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein.\]

Ein Übergang geht von Eingabe A zu Eingabe B und von Zeit t₀ zu t₁. Daher kann die *Richtung* eines Übergangs eine von zwei Dingen bedeuten:

-   Die Zuordnung von Zeitachsenebenen zu Eingaben.
-   Der Fortschritt im Laufe der Zeit.

Die erste ist die *Eingaberichtung,* und die zweite ist die *Fortschrittsrichtung*. Sie können beide Richtungen steuern.

-   Eingaberichtung: Standardmäßig erfolgt ein Übergang von der zusammengesetzten Ebene mit niedrigerer Priorität zu der Ebene, die den Übergang enthält. Um diese Richtung umzukehren, rufen Sie die [**IAMTimelineTrans::SetSwapInputs-Methode auf.**](iamtimelinetrans-setswapinputs.md)
-   Statusrichtung: Die meisten Übergänge unterstützen eine Standardmäßige **Progress-Eigenschaft,** die angibt, welcher Prozentsatz des Übergangs in der Ausgabe zu einem bestimmten Zeitpunkt wiedergegeben wird. Standardmäßig wechselt der Wert der **Progress-Eigenschaft** während der Dauer des Übergangs von 0,0 auf 1,0. Um den Fortschritt umzukehren, legen Sie die **Progress-Eigenschaft** auf 1.0 bis 0.0 fest.

Das folgende Diagramm veranschaulicht den Unterschied zwischen Eingaberichtung und Fortschrittsrichtung. Es zeigt vier Variationen eines standardmäßigen [SMPTE-Zurücksetzungsübergangs.](smpte-wipe-transition.md)

![Zurücksetzungsrichtungen](images/wipedirections.png)

Der Übergang befindet sich auf Spur 1. Standardmäßig wird das Zurücksetzen von links nach rechts und von Track 0 zu Track 1 geleitet. Das Austauschen von Eingaben bewirkt, dass das Zurücksetzen von Spur 1 zu Track 0 wechselt, aber immer noch von links nach rechts. Wenn Sie den Fortschritt umkehren, wird der Übergang von rechts nach links durchgeführt. Sie können beides kombinieren, wie ganz links dargestellt.

Weitere Informationen dazu, wie DES Übergänge rendert, finden Sie unter [Das Zeitachsenmodell.](the-timeline-model.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Effekten und Übergängen](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



