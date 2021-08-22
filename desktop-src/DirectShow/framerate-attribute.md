---
description: Das Framerate-Attribut gibt eine Framerate in Frames pro Sekunde an.
ms.assetid: 541a86e3-7736-4de4-b509-f8d61ef9bc58
title: framerate-Attribut (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2939126dbd849538bb30fcf7729e5f91dafa292b6db512398c915c8f8de2c9a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015658"
---
# <a name="framerate-attribute-directshow"></a>framerate-Attribut (DirectShow)

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Das `framerate` -Attribut gibt eine Framerate in Frames pro Sekunde an.

## <a name="possible-values"></a>Mögliche Werte

Gleitkommawert. Der Wert muss die führende Null vor der Dezimalstelle enthalten. Beispiel: 0.3, nicht .3. Verwenden Sie nicht mehr als sieben Dezimalstellen.

## <a name="applies-to"></a>Gilt für

[**Clip,**](clip-element.md) [**Gruppe,**](group-element.md) [**Zeitachse**](timeline-element.md)

## <a name="remarks"></a>Hinweise

Für das **Clip-Element** gibt dieses Attribut die Standardbildrate der Quelle an. Geben Sie das Attribut für stille Bilder und DIB-Sequenzen an. Legen Sie für ein Stillbild den Wert auf 0 (null) fest. Verwenden Sie für eine DIB-Sequenz einen Wert ungleich null. Der Standardwert ist 0 (null).

Für das **Gruppenelement** gibt dieses Attribut die Ausgabebildrate für die Gruppe an.

Für das **Zeitachsenelement** gibt dieses Attribut die Standardbildrate für alle Gruppen an.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[XTL-Attribute](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineSrc::SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md)
</dt> <dt>

[**IAMTimelineGroup::SetOutputFPS**](iamtimelinegroup-setoutputfps.md)
</dt> <dt>

[**IAMTimeline::SetDefaultFPS**](iamtimeline-setdefaultfps.md)
</dt> </dl>

 

 



