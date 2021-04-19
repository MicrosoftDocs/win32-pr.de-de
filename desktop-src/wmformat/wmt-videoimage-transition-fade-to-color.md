---
title: WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR (wmsdkidl. h)
description: Der Übergang zwischen den Farben wird vom Bild zu einem Frame mit voll Tonfarbe aufgelöst.
ms.assetid: 4ec52682-1ca2-436d-b7ce-2a9d407ff50e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR Windows Media-Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3873a24cee74e8cad3f6cd91d39f20a72ffa8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369495"
---
# <a name="wmt_videoimage_transition_fade_to_color"></a>WMT \_ Videoimage \_ - \_ Übergang \_ in \_ Farbe ausblenden

Der Übergang zwischen den Farben wird vom Bild zu einem Frame mit voll Tonfarbe aufgelöst.

## <a name="parameters"></a>Parameter

In der folgenden Tabelle werden die Parameter beschrieben, die von diesem Übergang verwendet werden, und es werden die Elemente der [**WMT \_ Videoimage \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) -Struktur aufgelistet, der Sie zugewiesen sind.



| Parameter         | Strukturmember | BESCHREIBUNG                                                                                                                                                                                                               |
|-------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Red               | **fEffectPara0** | Roter Wert der Hintergrundfarbe. Legen Sie auf eine Zahl zwischen 0 und 255 fest.                                                                                                                                                     |
| Grün             | **fEffectPara1** | Grüner Wert der Hintergrundfarbe. Legen Sie auf eine Zahl zwischen 0 und 255 fest.                                                                                                                                                   |
| Blau              | **fEffectPara2** | Der blaue Wert der Hintergrundfarbe. Legen Sie auf eine Zahl zwischen 0 und 255 fest.                                                                                                                                                    |
| Hintergrund Gewichtung | **fEffectPara3** | Gewichtung der Hintergrundfarbe. Dieser Parameter gibt den Prozentsatz der Hintergrundfarbe in der Mischung als Dezimalwert an. Um z. b. die Hintergrundfarbe um 30% zu mischen und das Bild 70% der Mischung zu erstellen, legen Sie auf 0,30 fest. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmsdkidl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Video Bild Übergänge**](video-image-transitions.md)
</dt> </dl>

 

 





