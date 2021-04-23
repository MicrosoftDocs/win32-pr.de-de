---
title: Positionieren und Verschieben von Videorechtecke im Kompositionsraum
description: Positionieren und Verschieben von Videorechtecke im Kompositionsraum
ms.assetid: 97e7bb24-79f6-4638-a9c4-ac09dbd29be9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96955fc2107036299ab6f530eeda76374a0a0315
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909628"
---
# <a name="position-and-move-video-rectangles-in-composition-space"></a>Positionieren und Verschieben von Videorechtecke im Kompositionsraum

Wenn der VMR mehrere Eingabedatenströme gemischt, positioniert er jeden Stream innerhalb eines normalisierten Rechtecks, das als "Kompositionsraum" bezeichnet wird. Innerhalb des Kompositionsraums bilden die Koordinaten (0,0, 0,0) bis (1,0, 1,0) das sichtbare Videorechteck. Alle Koordinaten, die außerhalb dieses Rechtecks liegen, werden abgeschnitten.

Eine Anwendung kann Sondereffekte beim Verschieben, Strecken und Verkleinern des Videos aus einem Eingabestream ausführen, indem das Zielrechteck im Kompositionsraum für diesen Stream geändert wird. Wenn das angegebene Rechteck eine andere Größe als das native Videorechteck hat, wird das native Video verkleinert oder gestreckt, damit es passt. Das Zielrechteck wird durch Aufrufen der [**IVMRMixerControl::SetOutputRect-Methode**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setmixingprefs) angegeben.

Angenommen, Stream 0 (entspricht Pin 0) enthält den Hauptvideostream, und Stream 1 (entspricht Pin 1) enthält ein sekundäres Video. Stream 1 kann vollständig im Offscreen positioniert werden, indem ein normalisiertes Rechteck von { -1,0f, 0,0f, 0,0f, 1,0f } angegeben wird. Stream 1 kann dann in den sichtbaren Bereich verschoben werden, indem die linke und rechte Seite des Rechtecks bei nachfolgenden Aufrufen von **SetOutputRect geändert wird:**



| Bezeichnung | Wert |
|--------|-----------------------------|
| Zeit   | Rechteck                   |
| t + 0  | { -1.0f, 0.0f, 0.0f, 1.0f } |
| t + 1  | { -0.9f, 0.0f, 0.1f, 1.0f } |
| t + 2  | { -0.8f, 0.0f, 0.2f, 1.0f } |
| ...    | ...                         |
| t + 10 | { 0.0f, 0.0f, 1.0f, 1.0f }  |



 

![Verschieben eines Videostreams im Kompositionsbereich](images/composition-space.png)

Zum Zeitpunkt t+10 ist das Video aus Stream 1 vollständig sichtbar. In diesem Beispiel wurde die native Größe von Stream 1 beibehalten, während er verschoben wurde. Sie können das Rechteck auch strecken oder verkleinern, um interessante Effekte zu erzeugen. Sie können das Video auch vertikal drehen, indem Sie einen höheren Wert für den oberen als den unteren Wert angeben, oder das Video horizontal spiegeln, indem Sie einen höheren Wert für die linke als die rechte Seite angeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des VMR-Gemischtmodus](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



