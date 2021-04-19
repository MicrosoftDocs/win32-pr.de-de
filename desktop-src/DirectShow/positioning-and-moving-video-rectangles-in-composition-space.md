---
title: Positionieren und Verschieben von Video Rechtecke im Kompositions Bereich
description: Positionieren und Verschieben von Video Rechtecke im Kompositions Bereich
ms.assetid: 97e7bb24-79f6-4638-a9c4-ac09dbd29be9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef766d1ae739e46a2c56bfab81b4243c9dcf6f10
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345400"
---
# <a name="position-and-move-video-rectangles-in-composition-space"></a>Positionieren und Verschieben von Video Rechtecke im Kompositions Bereich

Wenn der VMR mehrere Eingabedaten Ströme mischt, positioniert er jeden Stream innerhalb eines normalisierten Rechtecks, das als "Kompositions Raum" bezeichnet wird. Innerhalb des Kompositions Raums bilden die Koordinaten (0,0, 0,0) bis (1,0, 1,0) das sichtbare Video Rechteck. Alle Koordinaten, die außerhalb dieses Rechtecks liegen, werden abgeschnitten.

Eine Anwendung kann besondere Effekte durch das Verschieben, Strecken und Verkleinern des Videos aus einem Eingabestream durch Ändern des Ziel Rechtecks im Kompositions Raum für diesen Stream durchführen. Wenn das angegebene Rechteck eine andere Größe hat als das systemeigene Video Rechteck, wird das native Video verkleinert oder gestreckt. Das Ziel Rechteck wird durch Aufrufen der [**ivmrmixercontrol:: setoutputrect**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setmixingprefs) -Methode angegeben.

Nehmen wir beispielsweise an, dass Stream 0 (entspricht Pin 0) den hauptvideostream enthält, und Stream 1 (entspricht Pin 1) enthält ein sekundäres Video. Stream 1 kann durch Angabe eines normalisierten Rechtecks ({-1.0 f, 0,0 f, 0,0 f, 1.0 f}) vollständig ausgelagert werden. Stream 1 kann dann in den sichtbaren Bereich verschoben werden, indem die linke und die Rechte Seite des Rechtecks bei aufeinander folgenden Aufrufen von **setoutputrect** geändert werden:



|        |                             |
|--------|-----------------------------|
| Time   | Rechteck                   |
| t + 0  | {-1.0 f, 0,0 f, 0,0 f, 1.0 f} |
| t + 1  | {-0.9 f, 0,0 f, 0,1 f, 1.0 f} |
| t + 2  | {-0,8 f, 0,0 f, 0,2 f, 1.0 f} |
| ...    | ...                         |
| t + 10 | {0,0 f, 0,0 f, 1.0 f, 1.0 f}  |



 

![Verschieben eines Videodaten Stroms im Kompositions Bereich](images/composition-space.png)

Zum Zeitpunkt t + 10 ist das Video aus Stream 1 vollständig sichtbar. In diesem Beispiel wurde die systemeigene Größe von Stream 1 während der Verschiebung beibehalten. Sie können das Rechteck auch Strecken oder verkleinern, um interessante Effekte zu erzeugen. Sie können das Video auch vertikal kippen, indem Sie einen größeren Wert für den oberen als den unteren Wert angeben oder das Video horizontal spiegeln, indem Sie einen größeren Wert für Links als die Rechte angeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des VMR-Mischungs Modus](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



