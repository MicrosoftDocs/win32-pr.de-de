---
description: Ein Modell, das die Lautstärke des orientierten Sounds beschreibt.
ms.assetid: 15252358-d932-22f4-f13a-8e4b8487dd86
title: Audiokegel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 215659ab08c33066abfade2faf206f6360a51051
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364228"
---
# <a name="sound-cones"></a>Audiokegel

Ein Modell, das die Lautstärke des orientierten Sounds beschreibt.

Ein Sound ohne Ausrichtung hat dieselbe Amplitude in der angegebenen Entfernung in alle Richtungen. Ein Sound mit einer Ausrichtung ist in der Richtung der Ausrichtung laut Loudest. Das Modell, das die Lautstärke des orientierten Sounds beschreibt, wird als audiokegel bezeichnet. Audiokegel bestehen aus einem inneren (oder inneren) Kegel und einem äußeren (oder äußeren) Kegel. Der äußere Kegelwinkel muss immer größer oder gleich dem inneren Kegelwinkel sein.

In jedem Winkel im Inneren Kegel wird das Volume des Sounds auf das innere Kegel Volume festgelegt. Dabei wird das Basis Volume des Puffers, die Entfernung vom Listener, die Ausrichtung des Listener, wenn der Listener über einen eigenen Kegel verfügt usw. berücksichtigt.

In jedem Winkel außerhalb des äußeren Kegel wird das normale Volume durch einen von der Anwendung festgelegten Faktor gedämpft. Die Volumeebene für außen Kegel wird als lineare Amplitude-Scaler ausgedrückt: 1,0 f stellt keine auf das ursprüngliche Signal angewendete Dämpfung dar, 0,5 f bezeichnet eine Dämpfung von 6 dB, und 0,0 f führt zu einer Ruhe Minderung. Die Verstärkung (Volume > 1,0 f) ist ebenfalls zulässig und wird nicht geklammert. Der gültige volumebereich ist tatsächlich 0,0 f bis 2,0 f.

Zwischen dem inneren und äußeren Kegel besteht eine Übergangszone zwischen dem inneren Volume und dem externen Volume. Das Volume nähert sich dem äußeren Volume des Cone, wenn sich der Winkel vergrößert.

Kegel können andere Parameter als das Volume beeinflussen. Der niedrige Durchlauf Filter und die sendersendeebene können ebenfalls beeinträchtigt werden, sodass die Technik noch dramatischer wird. Beispielsweise kann mit einem Kegel auf dem Listener alle Klänge hinter dem Listener angegeben werden, um einen wenig gedämpften Wert zu erhalten, und einen geringfügig höheren Inhalt für das Direct-Verhältnis zu erhalten. Diese stellen weitere Hinweise bereit, dass der Sound hinter dem Benutzer liegt. Dadurch wird der Realismus verbessert.

In der folgenden Abbildung ist das Konzept der Sound Kegel dargestellt.

![audiokegel](images/common-audio-concepts-sound-cones.png)

Wenn Sie audiokegel ordnungsgemäß entwerfen, können Sie Ihre Anwendung mit dramatischen Effekten versehen. Sie können z. b. eine Audioquelle in der Mitte eines Raums positionieren und deren Ausrichtung auf eine öffnende Tür in einem Gang festlegen. Legen Sie dann den Winkel des inneren Kegel so fest, dass er sich auf die Breite der Tür erstreckt, den äußeren Kegel etwas breiter macht und schließlich das äußere Kegel Volume als nicht hörbar festgelegt wird. Ein Listener, der sich entlang des Flurs bewegt, wird den Sound nur dann hören, wenn er sich in der Nähe der Der Sound ist laut laudest, wenn der Listener vor dem öffnenden Tor übergibt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Allgemeine audiokonzepte](common-audio-concepts.md)
</dt> <dt>

[X3DAudio](x3daudio-overview.md)
</dt> <dt>

[**X3DAUDIO- \_ Kegel**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_cone)
</dt> </dl>

 

 



