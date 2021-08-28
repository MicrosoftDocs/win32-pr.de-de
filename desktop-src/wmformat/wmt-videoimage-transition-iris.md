---
title: WMT_VIDEOIMAGE_TRANSITION_IRIS (Wmsdkidl.h)
description: Der Irisübergang zeigt das neue Bild entlang einer x-Achse und einer y-Achse an. Der visuelle Effekt dieses Übergangs ist, dass das neue Bild in einem erweiternden Kreuz angezeigt wird, das alle Seiten des Frames erreicht.
ms.assetid: 7390d959-a566-43e7-937d-1e617bc98a6e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_IRIS Windows-Medienformat
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_IRIS
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 919af0b15ef8a7437c9852df3ff12623553cdabf
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472966"
---
# <a name="wmt_videoimage_transition_iris"></a>WMT \_ VIDEOIMAGE \_ TRANSITION \_ IRIS

Der Irisübergang zeigt das neue Bild entlang einer x-Achse und einer y-Achse an. Der visuelle Effekt dieses Übergangs ist, dass das neue Bild in einem erweiternden Kreuz angezeigt wird, das alle Seiten des Frames erreicht.

## <a name="parameters"></a>Parameter

In der folgenden Tabelle werden die von diesem Übergang verwendeten Parameter beschrieben und die Elemente der [**WMT \_ VIDEOIMAGE \_ SAMPLE2-Struktur**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) aufgelistet, der sie zugewiesen sind.




| Parameter | Strukturmember | BESCHREIBUNG | 
|-----------|------------------|-------------|
| X zentrieren | <strong>fEffectPara0</strong> | X-Koordinate relativ zum Videorahmen der Mitte des Iriseffekts. | 
| Y zentrieren | <strong>fEffectPara1</strong> | Y-Koordinate relativ zum Videorahmen der Mitte des Iriseffekts. | 
| Breite | <strong>fEffectPara2</strong> | Breite der vertikalen Linie, die das neue Bild in Pixel angibt. | 
| Höhe | <strong>fEffectPara3</strong> | Höhe der horizontalen Linie, die das neue Bild in Pixel angibt. | 
| Aufbau | <strong>fEffectPara4</strong> | Legen Sie auf einen der folgenden Werte fest:<ul><li>0 : Gibt die normale Komposition an, bei der das vorherige Bild den Hintergrund und das aktuelle Bild den Vordergrund darstellt.</li><li>1 : Gibt die umgekehrte Komposition an, bei der das aktuelle Bild das Hintergrundbild und das vorherige Bild der Vordergrund ist.</li></ul> | 




 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Videobildübergänge**](video-image-transitions.md)
</dt> </dl>

 

 





