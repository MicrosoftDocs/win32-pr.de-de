---
description: Sie können Microsoft Direct3D verwenden, um natürliche Phänomene im Zusammenhang mit Energie Releases zu simulieren.
ms.assetid: a16af13d-3a38-42b5-900b-ff58a0c917b2
title: Feuer, Flares und Explosionen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 708730bd8e5f198664bb20c11fa98243ac98f0d6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745568"
---
# <a name="fire-flares-and-explosions-direct3d-9"></a>Feuer, Flares und Explosionen (Direct3D 9)

Sie können Microsoft Direct3D verwenden, um natürliche Phänomene im Zusammenhang mit Energie Releases zu simulieren. Beispielsweise kann eine Anwendung die Darstellung von Fire generieren, indem Sie Flammen ähnliche Texturen auf eine Reihe von Plakaten anwendet. Dies ist besonders wirksam, wenn die Anwendung eine Sequenz von Fire-Texturen verwendet, um die Flammen der einzelnen Billboards im Feuer zu animieren. Wenn Sie die Geschwindigkeit der Animations Wiedergabe von Billboard zu Billboard verändern, wird das Aussehen echter Flammen vergrößert. Der Anschein von gemischten 3D-Flammen kann erreicht werden, indem die Billboards und die Texturen auf den Plakaten geschigeln werden.

Sie können Flares und blinkte simulieren, indem Sie nacheinander hellere Licht Zuordnungen auf alle primitiven in einer Szene anwenden. Obwohl es sich hierbei um ein Rechenverfahren mit hohem Aufwand handelt, kann die Anwendung eine lokalisierte Fackel oder einen Blitz simulieren. Das heißt, der Teil der Szene, in dem die Fackel oder der Speicherstick zuerst ausgelöst werden kann.

Ein weiteres Verfahren besteht darin, ein Billboard vor der Szene zu positionieren, damit der gesamte renderzielbereich abgedeckt wird. Die Anwendung wendet in der Zwischenzeit aufeinander folgender Whiter-Texturen an und verringert die Transparenz im Zeitverlauf. Die gesamte Szene wird in weiß angezeigt, wenn die Zeit verstrichen ist. Dabei handelt es sich um eine Methode mit geringem Verwaltungsaufwand zum Erstellen eines Flare. Bei dieser Vorgehensweise kann es jedoch schwierig sein, die Darstellung eines hellen Sticks aus einer einzelnen Point Light-Quelle zu generieren.

Explosionen können in einem 3D-Szenen Verfahren angezeigt werden, das den für Feuer, blinken und Flares verwendeten Verfahren ähnelt. Beispielsweise kann Ihre Anwendung ein Billboard verwenden, um eine Schockwelle und eine steigende rauche beim Auftreten der Explosion anzuzeigen. Gleichzeitig kann Ihre Anwendung eine Reihe von Plakaten verwenden, um Flammen zu simulieren. Außerdem kann es ein einzelnes Billboard vor der Szene positionieren, um der gesamten Szene ein Licht auffallen hinzuzufügen.

Energie Balken können mithilfe von Billboards simuliert werden. Die Anwendung kann Sie auch mithilfe von primitiven anzeigen, die als Linien Listen oder Zeilen Streifen definiert sind. Weitere Informationen finden Sie unter [Zeilen Listen](line-lists.md) und [Zeilen Streifen](line-strips.md).

Die Anwendung kann Force-Felder mithilfe von oder als Dreiecks Listen definierte primitive erstellen. Wenn Sie ein Feld vom Typ "Force" aus Dreiecks Listen erstellen möchten, definieren Sie eine Gruppe von zusammenhängenden Dreiecken in einer Dreiecks Liste, die gleichmäßig über dem Bereich liegt, der im Feld "Force" Durch die Lücken zwischen den Dreiecken kann der Benutzer die Szene hinter den Dreiecken sehen, wie Sie es bei der Betrachtung eines Force-Felds erwarten. Wenden Sie eine Textur auf die Dreiecks Liste an, die den Dreiecken die Darstellung des leuchtendes mit Energie verleiht. Weitere Informationen finden Sie unter [Dreieck Listen](triangle-lists.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Alpha Beispiele](alpha-examples.md)
</dt> </dl>

 

 



