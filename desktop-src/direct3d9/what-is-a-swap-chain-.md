---
description: Eine austauschkette ist eine Auflistung von Puffern, die zum Anzeigen von Frames für den Benutzer verwendet werden.
ms.assetid: aefc0680-cbe6-42eb-8c00-eaa343eee469
title: Was ist eine austauschkette? (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8fc1fd2d313c70a680d9b276a3aabedc6d8cff
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213855"
---
# <a name="what-is-a-swap-chain-direct3d-9"></a>Was ist eine austauschkette? (Direct3D 9)

Eine austauschkette ist eine Auflistung von Puffern, die zum Anzeigen von Frames für den Benutzer verwendet werden. Jedes Mal, wenn eine Anwendung einen neuen Frame für die Anzeige darstellt, wird der erste Puffer in der SwapChain an der Stelle des angezeigten Puffers angezeigt. Dieser Prozess wird als Austausch oder Flipping bezeichnet.

Ein Grafikadapter enthält einen Zeiger auf eine Oberfläche, die das auf dem Monitor angezeigte Bild darstellt, das als Front Buffer bezeichnet wird. Während der Aktualisierung des Monitors sendet die Grafikkarte den Inhalt des Front Puffers an den Monitor, der angezeigt werden soll. Dies führt jedoch zu einem Problem beim Rendern von Echtzeitgrafiken. Das Herzstück des Problems ist, dass die Monitor Aktualisierungs Raten im Vergleich zum restlichen Computer sehr langsam sind. Allgemeine Aktualisierungs Raten liegen zwischen 60 Hz (60 mal pro Sekunde) und 100 Hz. Wenn die Anwendung den Frontpuffer aktualisiert, während sich der Monitor in der Mitte einer Aktualisierung befindet, wird das Bild, das angezeigt wird, in der Hälfte mit der oberen Hälfte der Anzeige, die das alte Bild enthält, und der unteren Hälfte mit dem neuen Bild abgeschnitten. Dieses Problem wird als "zerreißen" bezeichnet.

Direct3D implementiert zwei Optionen, um das Zerreißen zu vermeiden:

-   Eine Option, mit der nur Updates des Monitors für den vertikalen Vorgang zum erneuten verfolgen (oder vertikalen synchronisieren) zugelassen werden. Ein Monitor aktualisiert in der Regel sein Bild, indem er eine helle Pin horizontal bewegt, von oben links auf dem Monitor bis zur unteren rechten Ecke. Wenn die helle Pin den unteren Rand erreicht, wird die helle PIN durch den Monitor wiederholt, indem Sie nach oben links verschoben wird, damit der Prozess wieder gestartet werden kann. Diese Neukalibrierung wird als vertikale Synchronisierung bezeichnet. Während einer vertikalen Synchronisierung wird vom Monitor nichts gezeichnet, sodass ein Update des Front-Puffers erst angezeigt wird, wenn der Monitor erneut gezeichnet wird. Die vertikale Synchronisierung ist relativ langsam. Es ist jedoch nicht langsam genug, um eine komplexe Szene während des Wartens zu erzeugen. Was erforderlich ist, um das Zerreißen zu vermeiden und komplexe Szenen zu Rendering, ist ein Prozess, der als Rück Pufferung bezeichnet wird.
-   Eine Option zur Verwendung einer Methode, die als backpufferung bezeichnet wird. Bei der Back Pufferung wird eine Szene auf eine Bildschirmoberfläche gezeichnet, die als BackBuffer bezeichnet wird. Beachten Sie, dass jede Oberfläche, die nicht der Vorder-Puffer ist, als Offscreen-Oberfläche bezeichnet wird, da Sie niemals direkt vom Monitor angezeigt wird. Mithilfe eines Hintergrund Puffers kann eine Anwendung eine Szene immer dann Rendering, wenn sich das System im Leerlauf befindet (d. h., es werden keine Windows-Meldungen gewartet), ohne dass die Aktualisierungsrate des Monitors berücksichtigt werden muss. Die Back Pufferung führt zu einer zusätzlichen Komplikation, wie und wann der Hintergrund Puffer in den Vordergrund Puffer verschoben werden soll.

Der Prozess des Verschiebens des Hintergrund Puffers in den Vordergrund Puffer wird als Oberflächen flipperung bezeichnet. Da die Grafikkarte einfach einen Zeiger auf eine Oberfläche verwendet, um den Vorder-Puffer darzustellen, ist nur eine einfache Zeiger Änderung erforderlich, um den Hintergrund Puffer auf den Vorder-Puffer festzulegen. Wenn eine Anwendung die Direct3D zur Darstellung des Hintergrund Puffers für den vorderen Puffer auffordert, werden die beiden Oberflächen Zeiger von Direct3D einfach "gekippt". Das Ergebnis ist, dass der Hintergrund Puffer nun der neue Front-Puffer ist und der alte Frontpuffer der neue Hintergrund Puffer ist. Ein Surface-Flip wird immer dann aufgerufen, wenn eine Anwendung das Direct3D-Gerät anfordert, den Hintergrund Puffer darzustellen. Direct3D kann jedoch so eingerichtet werden, dass die Anforderungen in die Warteschlange eingereiht werden, bis eine vertikale Synchronisierung erfolgt Diese Option wird als Präsentations Intervall des Direct3D-Geräts bezeichnet. Beachten Sie, dass die Daten im neuen Hintergrund Puffer möglicherweise nicht wiederverwendbar sind, je nachdem, wie eine Anwendung angibt, wie Direct3D das Oberflächen Flipping behandeln soll. Das Oberflächen kippen ist ein wichtiger Punkt in Multimedia-, Animations-und Spielsoftware. Dies entspricht der Art und Weise, wie Sie Animationen mit einem Papierblatt durchführen können. Auf jeder Seite ändert der Künstler die Abbildungen leicht, sodass das Zeichnen beim schnellen kippen zwischen den Blättern animiert erscheint.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Oberflächen](direct3d-surfaces.md)
</dt> <dt>

[Flipping-Oberflächen (Direct3D 9)](flipping-surfaces.md)
</dt> </dl>

 

 



