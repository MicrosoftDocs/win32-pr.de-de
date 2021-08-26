---
description: Eine Swapkette ist eine Sammlung von Puffern, die zum Anzeigen von Frames für den Benutzer verwendet werden.
ms.assetid: aefc0680-cbe6-42eb-8c00-eaa343eee469
title: Was ist eine Austauschkette? (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91666ffeb05dd7020a4caad1c11777842d7222cdc4cd6b04cd862edea5fff764
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068810"
---
# <a name="what-is-a-swap-chain-direct3d-9"></a>Was ist eine Austauschkette? (Direct3D 9)

Eine Swapkette ist eine Sammlung von Puffern, die zum Anzeigen von Frames für den Benutzer verwendet werden. Jedes Mal, wenn eine Anwendung einen neuen Frame für die Anzeige präsentiert, wird der erste Puffer in der Austauschkette an die Stelle des angezeigten Puffers. Dieser Prozess wird als Austauschen oder Kippen bezeichnet.

Ein Grafikadapter enthält einen Zeiger auf eine Oberfläche, die das auf dem Monitor angezeigte Bild darstellt, das als Frontpuffer bezeichnet wird. Wenn der Monitor aktualisiert wird, sendet die Grafikkarte den Inhalt des Frontpuffers an den Monitor, um angezeigt zu werden. Dies führt jedoch zu einem Problem beim Rendern von Echtzeitgrafiken. Das Kernstück des Problems ist, dass die Aktualisierungsraten der Überwachung im Vergleich zum Rest des Computers sehr langsam sind. Allgemeine Aktualisierungsraten reichen von 60 Hz (60-mal pro Sekunde) bis 100 Hz. Wenn Ihre Anwendung den Frontpuffer aktualisiert, während sich der Monitor in der Mitte einer Aktualisierung befindet, wird das angezeigte Bild halbiert, wobei die obere Hälfte der Anzeige das alte Bild enthält, und die untere Hälfte das neue Bild enthält. Dieses Problem wird als "Tränkung" bezeichnet.

Direct3D implementiert zwei Optionen, um Reißer zu vermeiden:

-   Eine Option, die nur Updates des Monitors für den vertikalen Rückziehvorgang (oder die vertikale Synchronisierung) zu lässt. Ein Monitor aktualisiert in der Regel sein Bild, indem er einen lichten Pin horizontal bewegt, von der oberen linken Seite des Monitors zickt und unten rechts endet. Wenn der Lichtpin den unteren Rand erreicht, wird der Lichtpin vom Monitor neu gecalibt, indem er wieder nach oben links bewegt wird, damit der Prozess erneut gestartet werden kann. Diese Neusynchronisierung wird als vertikale Synchronisierung bezeichnet. Während einer vertikalen Synchronisierung wird vom Monitor nichts gezeichnungt, sodass alle Aktualisierungen des Frontpuffers erst angezeigt werden, wenn der Monitor wieder gezeichnen wird. Die vertikale Synchronisierung ist relativ langsam. ist jedoch nicht langsam genug, um eine komplexe Szene während des Wartens zu rendern. Was erforderlich ist, um Dasins zu vermeiden und komplexe Szenen rendern zu können, ist ein Prozess, der als Zurückpufferung bezeichnet wird.
-   Eine Option zur Verwendung einer Technik, die als Zurückpufferung bezeichnet wird. Die Zurückpufferung ist der Prozess, bei dem eine Szene auf eine Off-Screen-Oberfläche gezeichnungt wird, die als Hintergrundpuffer bezeichnet wird. Beachten Sie, dass jede andere Oberfläche als der Frontpuffer als Off-Screen-Oberfläche bezeichnet wird, da sie nie direkt vom Monitor angezeigt wird. Durch die Verwendung eines Hintergrundpuffers kann eine Anwendung eine Szene rendern, wenn sich das System im Leerlauf befindet (d. h. keine Fenstermeldungen warten), ohne die Aktualisierungsrate des Monitors berücksichtigen zu müssen. Die Zurückpufferung führt zu einer zusätzlichen Komplikation der Art und Weise, wie und wann der Puffer zurück in den Frontpuffer bewegt werden soll.

Der Vorgang zum Verschieben des Zurückpuffers in den Frontpuffer wird als Oberflächenkippen bezeichnet. Da die Grafikkarte einfach einen Zeiger auf eine Oberfläche verwendet, um den Frontpuffer zu darstellen, ist nur eine einfache Zeigeränderung erforderlich, um den Hintergrundpuffer auf den Frontpuffer zu setzen. Wenn eine Anwendung Direct3D anlädt, den Hintergrundpuffer dem Frontpuffer zu präsentieren, "kippt Direct3D" einfach die beiden Oberflächenzeer. Das Ergebnis ist, dass der Backpuffer jetzt der neue Frontpuffer und der alte Frontpuffer der neue Backpuffer ist. Ein Surface Flip wird immer dann aufgerufen, wenn eine Anwendung das Direct3D-Gerät bittet, den Hintergrundpuffer zu präsentieren. Direct3D kann jedoch so eingerichtet werden, dass die Anforderungen in die Warteschlange gestellt werden, bis eine vertikale Synchronisierung erfolgt. Diese Option wird als Präsentationsintervall des Direct3D-Geräts bezeichnet. Beachten Sie, dass die Daten im neuen Hintergrundpuffer möglicherweise nicht wiederverwendbar sind, je nachdem, wie eine Anwendung angibt, wie Direct3D das Spiegeln der Oberfläche behandeln soll. Oberflächenumkehrung ist ein wichtiger Schlüssel in Multimedia-, Animations- und Spielsoftware. dies entspricht der Art und Weise, wie Sie Animationen mit einem Papierpad erstellen können. Auf jeder Seite ändert der Interpret die Abbildungen geringfügig, sodass die Zeichnung animiert wird, wenn Sie schnell zwischen den Blättern blättern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Oberflächen](direct3d-surfaces.md)
</dt> <dt>

[Spiegelnde Oberflächen (Direct3D 9)](flipping-surfaces.md)
</dt> </dl>

 

 



