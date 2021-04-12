---
description: 'Die Position, die Geschwindigkeit und die Ausrichtung von Soundquellen und Listenern im 3D-Raum werden durch kartesische Koordinaten dargestellt, bei denen es sich um Werte auf drei Achsen handelt: die x-Achse, die y-Achse und die z-Achse.'
ms.assetid: b6315e21-0758-e4c8-195f-4b83c7b61784
title: Koordinaten von 3D-Raum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3081c1a3a6c497d53d093c98732a9d381996c96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216793"
---
# <a name="coordinates-of-3d-space"></a>Koordinaten von 3D-Raum

Die Position, die Geschwindigkeit und die Ausrichtung von Soundquellen und Listenern im 3D-Raum werden durch kartesische Koordinaten dargestellt, bei denen es sich um Werte auf drei Achsen handelt: die x-Achse, die y-Achse und die z-Achse.

Die Achsen sind relativ zu einem von der Anwendung festgelegten Standpunkt. Werte auf der x-Achse steigen von links nach rechts, auf der y-Achse von unten nach oben und auf der z-Achse von fast zu weit.

Die **X3DAUDIO- \_ Vektor** Struktur enthält Werte, die die Position, die Geschwindigkeit oder die Ausrichtung auf den drei Achsen beschreiben.

Die Vektoren werden in der Reihenfolge (x, y, z) als drei Werte in Klammern eingeschlossen und durch Kommas getrennt.

Für die Position befinden sich die Werte in benutzerdefinierten Welteinheiten.

Der Vektor beschreibt die Geschwindigkeit der Bewegung entlang jeder Achse in Welteinheiten pro Sekunde.

Aus Gründen der Ausrichtung befinden sich die Werte in beliebigen Einheiten und sind relativ zueinander. Wenn z. b. die Basis Ansicht der 3D-Welt dem Horizont Nordweg zusteht und die Ausrichtung des Listener (-1, 0, 1) ist, wird der Listener mit Nordwest angezeigt. Da sich die Werte in einem Vektor nicht in absoluten Einheiten befinden, könnte der Vektor gleichermaßen als (-5, 0, 5) oder (-0,25, 0, 0,25) ausgedrückt werden.

3D-Vektoren arbeiten ähnlich wie 2D-Vektoren, aber mit einer zusätzlichen Achse in der nach-unten-Richtung. Sie können sehen, wie Vektoren im 2D-Raum funktionieren, indem Sie Sie auf einem Blatt mit Diagramm Papier zeichnen. Lassen Sie die Werte von unten nach oben im Papier und von links nach rechts vergrößern. Eine Linie, die von (0,0) bis (1, 1) gezeichnet wird, hat dieselbe Ausrichtung bzw. Richtung wie eine, die von (0,0) bis (5, 5) gezeichnet wird. Die zweite Zeile weist jedoch auf eine größere Entfernung oder Geschwindigkeit hin.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Allgemeine audiokonzepte](common-audio-concepts.md)
</dt> <dt>

[X3DAudio Übersicht](x3daudio-overview.md)
</dt> </dl>

 

 



