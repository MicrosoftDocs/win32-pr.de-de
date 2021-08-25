---
title: WMT_VIDEOIMAGE_TRANSITION_STAR (Wmsdkidl.h)
description: Der Sternübergang zeigt das neue Bild in einem Fünf-Punkte-Stern im Rahmen an.
ms.assetid: d16f73ce-0fa8-47b4-8146-32f276e6d16c
keywords:
- WMT_VIDEOIMAGE_TRANSITION_STAR windows Media Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_STAR
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7524e51908f7d941aa04b138cc67ba6c4ab6a2a8
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479496"
---
# <a name="wmt_videoimage_transition_star"></a>WMT \_ VIDEOIMAGE \_ TRANSITION \_ STAR

Der Sternübergang zeigt das neue Bild in einem Fünf-Punkte-Stern im Rahmen an.

## <a name="parameters"></a>Parameter

In der folgenden Tabelle werden die von diesem Übergang verwendeten Parameter beschrieben und die Member der [**WMT \_ VIDEOIMAGE \_ SAMPLE2-Struktur**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) aufgeführt, der sie zugewiesen sind.




| Parameter | Struktur-Member | BESCHREIBUNG | 
|-----------|------------------|-------------|
| X zentrieren | <strong>fEffectPara0</strong> | X-Koordinate, relativ zum Videoframe, der Mitte des Sterns. | 
| Y zentrieren | <strong>fEffectPara1</strong> | Y-Koordinate, relativ zum Videoframe, der Mitte des Sterns. | 
| Radius | <strong>fEffectPara2</strong> | Radius des Kreises, der durch die Punkte des Sterns definiert wird, in Pixel. | 
| Aufbau | <strong>fEffectPara3</strong> | Legen Sie auf einen der folgenden Werte fest:<ul><li>0 : Gibt die normale Komposition an, bei der das vorherige Bild der Hintergrund und das aktuelle Bild der Vordergrund ist.</li><li>1 : Gibt die umgekehrte Komposition an, bei der das aktuelle Bild das Hintergrundbild und das vorherige Bild der Vordergrund ist.</li></ul> | 




 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Videobildübergänge**](video-image-transitions.md)
</dt> </dl>

 

 





