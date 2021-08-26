---
description: Ein Modell, das die Lautheit des orientierten Sounds beschreibt.
ms.assetid: 15252358-d932-22f4-f13a-8e4b8487dd86
title: Soundkegel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d1dc6b55ce1cc98b1875dff7079a0a304ef77c5567966808a4678f01f2297ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005774"
---
# <a name="sound-cones"></a>Soundkegel

Ein Modell, das die Lautheit des orientierten Sounds beschreibt.

Ein Sound ohne Ausrichtung hat in einer bestimmten Entfernung in alle Richtungen dieselbe Amplitude. Ein Sound mit einer Ausrichtung ist in Richtung der Ausrichtung am lautesten. Das Modell, das die Lautheit des ausgerichteten Sounds beschreibt, wird als Soundkegel bezeichnet. Soundkegel besteht aus einem inneren (oder inneren) Kegel und einem äußeren (oder äußeren) Kegel. Der Außenkegelwinkel muss immer gleich oder größer als der innere Kegelwinkel sein.

Bei jedem Winkel innerhalb des inneren Kegels wird die Lautstärke des Sounds auf das innere Kegelvolumen festgelegt. Dies berücksichtigt das grundlegende Volume des Puffers, den Abstand zum Listener, die Ausrichtung des Listeners, wenn der Listener über einen eigenen Kegel verfügt, und so weiter.

Bei jedem Winkel außerhalb des äußeren Kegels wird das normale Volumen durch einen von der Anwendung festgelegten Faktor abgedämpft. Die Außenkegelvolumenebene wird als linearer Amplitudenskalierer ausgedrückt: 1,0 f stellt keine Dämpfung dar, die auf das ursprüngliche Signal angewendet wird, 0,5 f steht für eine Dämpfung von 6 dB, und 0,0 f führt zu Stille. Die Verstärkung (Volume > 1.0 f) ist ebenfalls zulässig und wird nicht geklammert. Der gültige Volumebereich liegt tatsächlich zwischen 0,0 f und 2,0 f.

Zwischen den inneren und äußeren Kegeln ist eine Zone des Übergangs vom inneren Volume zum externen Volume. Das Volume nähert sich dem äußeren Volume des Kegels, wenn der Winkel zunimmt.

Kegel können sich auf andere Parameter als das Volume auswirken. Der Niedrige-Durch-Filter und die Sendeebene des Halles können ebenfalls betroffen sein, wodurch die Technik noch drastischer wird. Bei einer Kegelung auf dem Listener kann beispielsweise angegeben werden, dass alle Sounds hinter dem Listener ein wenig muffiert werden und einen etwas höheren Inhalt im Verhältnis von Hall zu direktem Verhältnis haben. Diese bieten weitere Hinweise darauf, dass sich der Sound hinter dem Benutzer befindet. Dadurch wird der Realismus verbessert.

Die folgende Abbildung zeigt das Konzept von Soundkegeln.

![Soundkegel](images/common-audio-concepts-sound-cones.png)

Das ordnungsgemäße Entwerfen von Soundkegeln kann Ihrer Anwendung drastische Effekte hinzufügen. Beispielsweise können Sie eine Soundquelle in der Mitte eines Raums positionieren und ihre Ausrichtung auf eine offene Tür in einem Hall festlegen. Legen Sie dann den Winkel des Inneren Kegels so fest, dass er sich auf die Breite des Einganges erstreckt, den Außenkegel etwas breiter macht und schließlich das äußere Kegelvolumen auf unhörbar festlegen. Ein Listener, der sich entlang des Halles bewegt, beginnt, den Sound erst zu hören, wenn er sich in der Nähe des Eingangs befindet. Der Sound wird am lautesten sein, wenn der Listener vor der offenen Tür übergeht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Allgemeine Audiokonzepte](common-audio-concepts.md)
</dt> <dt>

[X3DAudio](x3daudio-overview.md)
</dt> <dt>

[**X3DAUDIO \_ CONE**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_cone)
</dt> </dl>

 

 



