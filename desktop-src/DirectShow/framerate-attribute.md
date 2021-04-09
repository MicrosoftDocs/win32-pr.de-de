---
description: Das Framerate-Attribut gibt ein Framerate in Frames pro Sekunde an.
ms.assetid: 541a86e3-7736-4de4-b509-f8d61ef9bc58
title: Framerate-Attribut (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f1af5deb8ae2a851b328fcd6d9ffa3923328708
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103957904"
---
# <a name="framerate-attribute-directshow"></a>Framerate-Attribut (DirectShow)

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Das- `framerate` Attribut gibt einen Framerate in Frames pro Sekunde an.

## <a name="possible-values"></a>Mögliche Werte

Gleitkommawert. Der Wert muss die führende Null vor der Dezimalstelle enthalten. Beispielsweise 0,3, nicht. 3. Verwenden Sie nicht mehr als sieben Dezimalziffern.

## <a name="applies-to"></a>Gilt für

[**Clip**](clip-element.md), [**Gruppe**](group-element.md), [**Zeitachse**](timeline-element.md)

## <a name="remarks"></a>Bemerkungen

Für das **Clip** -Element gibt dieses Attribut die Standardbildrate der Quelle an. Geben Sie das-Attribut für weiterhin Bilder und DIB-Sequenzen an. Legen Sie für ein Image den Wert auf 0 (null) fest. Verwenden Sie für eine DIB-Sequenz einen Wert ungleich 0 (null). Der Standardwert ist 0 (null).

Für das **Group** -Element gibt dieses Attribut die Ausgabe Frame Rate für die Gruppe an.

Für das **Timeline** -Element gibt dieses Attribut die Standardbildrate für alle Gruppen an.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[XTL-Attribute](xtl-attributes.md)
</dt> <dt>

[**Iamtimelinesrc:: setdefaultfps**](iamtimelinesrc-setdefaultfps.md)
</dt> <dt>

[**Iamtimelinegroup:: setoutputfps**](iamtimelinegroup-setoutputfps.md)
</dt> <dt>

[**Iamtimeline:: setdefaultfps**](iamtimeline-setdefaultfps.md)
</dt> </dl>

 

 



