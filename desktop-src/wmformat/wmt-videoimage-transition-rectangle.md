---
title: WMT_VIDEOIMAGE_TRANSITION_RECTANGLE (Wmsdkidl.h)
description: Der Rechteckübergang zeigt das neue Bild in einem Rechteck innerhalb des Rahmens an.
ms.assetid: 2e238cd5-1da5-4145-a44d-b2658559fa0f
keywords:
- WMT_VIDEOIMAGE_TRANSITION_RECTANGLE Windows-Medienformat
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_RECTANGLE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8721455c09a263d9c856358d2ca55bb818ac48e5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467397"
---
# <a name="wmt_videoimage_transition_rectangle"></a>WMT \_ VIDEOIMAGE \_ TRANSITION \_ RECTANGLE

Der Rechteckübergang zeigt das neue Bild in einem Rechteck innerhalb des Rahmens an.

## <a name="parameters"></a>Parameter

In der folgenden Tabelle werden die von diesem Übergang verwendeten Parameter beschrieben und die Member der [**WMT \_ VIDEOIMAGE \_ SAMPLE2-Struktur**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) aufgeführt, der sie zugewiesen sind.




| Parameter | Struktur-Member | BESCHREIBUNG | 
|-----------|------------------|-------------|
| X zentrieren | <strong>fEffectPara0</strong> | X-Koordinate, relativ zum Videoframe, der Mitte des Rechtecks. | 
| Y zentrieren | <strong>fEffectPara1</strong> | Y-Koordinate, relativ zum Videoframe, der Mitte des Rechtecks. | 
| Breite | <strong>fEffectPara2</strong> | Breite des Rechtecks in Pixel. | 
| Höhe | <strong>fEffectPara3</strong> | Höhe des Rechtecks in Pixel. | 
| Aufbau | <strong>fEffectPara4</strong> | Legen Sie auf einen der folgenden Werte fest:<ul><li>0 : Gibt die normale Komposition an, bei der das vorherige Bild der Hintergrund und das aktuelle Bild der Vordergrund ist.</li><li>1 : Gibt die umgekehrte Komposition an, bei der das aktuelle Bild das Hintergrundbild und das vorherige Bild der Vordergrund ist.</li></ul> | 




 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Videobildübergänge**](video-image-transitions.md)
</dt> </dl>

 

 





