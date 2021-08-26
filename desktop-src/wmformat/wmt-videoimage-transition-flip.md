---
title: WMT_VIDEOIMAGE_TRANSITION_FLIP (Wmsdkidl.h)
description: Durch den Flip-Übergang wird das alte Bild auf einer y-Achse durch die Mitte des Rahmens gedreht. Das neue Bild wird als Rückseite des alten Bilds angezeigt.
ms.assetid: ff9990ef-962c-4dbb-b2bc-3bee070d2044
keywords:
- WMT_VIDEOIMAGE_TRANSITION_FLIP Windows-Medienformat
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FLIP
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2a3bfe94e001c6a65256facd5484a015d00f245
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475756"
---
# <a name="wmt_videoimage_transition_flip"></a>WMT \_ VIDEOIMAGE \_ TRANSITION \_ FLIP

Durch den Flip-Übergang wird das alte Bild auf einer y-Achse durch die Mitte des Rahmens gedreht. Das neue Bild wird als Rückseite des alten Bilds angezeigt.

## <a name="parameters"></a>Parameter

In der folgenden Tabelle werden die von diesem Übergang verwendeten Parameter beschrieben und die Elemente der [**WMT \_ VIDEOIMAGE \_ SAMPLE2-Struktur**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) aufgelistet, der sie zugewiesen sind.




| Parameter | Strukturmember | BESCHREIBUNG | 
|-----------|------------------|-------------|
| Angle | <strong>fEffectPara0</strong> | Drehwinkel von 0,0 bis 180,0 Grad. | 
| Aufbau | <strong>fEffectPara1</strong> | Legen Sie auf einen der folgenden Werte fest:<ul><li>0 : Gibt die normale Komposition an, bei der das vorherige Bild den Hintergrund und das aktuelle Bild den Vordergrund darstellt.</li><li>1 – Gibt die umgekehrte Komposition an, bei der das aktuelle Bild das Hintergrundbild und das vorherige Bild der Vordergrund ist.</li></ul> | 




 

## <a name="remarks"></a>Hinweise

Sie können die Auswirkungen dieses Übergangs so visualisieren, als wären beide Bilder physische Fotos, die wieder zusammengekleben würden. Der Übergang hat den gleichen Effekt wie das Halten von zwei fotos dieser Art in der Mitte des unteren Rands und deren Drehung um 180 Grad.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Videobildübergänge**](video-image-transitions.md)
</dt> </dl>

 

 





