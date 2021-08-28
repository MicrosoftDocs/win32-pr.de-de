---
title: WMT_VIDEOIMAGE_TRANSITION_WHEEL (Wmsdkidl.h)
description: Der Radübergang zeigt das neue Bild, indem vier Linien um einen gemeinsamen Pivotpunkt gedreht werden, z. B. die Speichen eines Rads.
ms.assetid: 426217be-789b-4b78-b0ea-de9629ecd46c
keywords:
- WMT_VIDEOIMAGE_TRANSITION_WHEEL Windows-Medienformat
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_WHEEL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b77e8640f21bd06194b2fe6b1e7048d85b323e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469267"
---
# <a name="wmt_videoimage_transition_wheel"></a>WMT \_ VIDEOIMAGE \_ TRANSITION \_ WHEEL

Der Radübergang zeigt das neue Bild, indem vier Linien um einen gemeinsamen Pivotpunkt gedreht werden, z. B. die Speichen eines Rads.

## <a name="parameters"></a>Parameter

In der folgenden Tabelle werden die von diesem Übergang verwendeten Parameter beschrieben und die Elemente der [**WMT \_ VIDEOIMAGE \_ SAMPLE2-Struktur**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) aufgelistet, der sie zugewiesen sind.




| Parameter | Strukturmember | BESCHREIBUNG | 
|-----------|------------------|-------------|
| X zentrieren | <strong>fEffectPara0</strong> | X-Koordinate relativ zum Videorahmen der Mitte des Radeffekts. | 
| Y zentrieren | <strong>fEffectPara1</strong> | Y-Koordinate relativ zum Videorahmen der Mitte des Radeffekts. | 
| Angle | <strong>fEffectPara2</strong> | Drehwinkel der Speichen des Radeffekts in Grad. Der Wert 0,0 gibt das alte Bild an, ohne dass ein neues Bild angezeigt wird. Der Wert 90,0 gibt an, dass das neue Bild vollständig angezeigt wird. Die Bewegung von 0,0 zu 90,0 wird als Drehung der Speichen im Uhrzeigersinn angezeigt.<br /> | 
| Aufbau | <strong>fEffectPara3</strong> | Legen Sie auf einen der folgenden Werte fest:<ul><li>0 : Gibt die normale Komposition an, bei der das vorherige Bild den Hintergrund und das aktuelle Bild den Vordergrund darstellt.</li><li>1 – Gibt die umgekehrte Komposition an, bei der das aktuelle Bild das Hintergrundbild und das vorherige Bild der Vordergrund ist.</li></ul> | 




 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Videobildübergänge**](video-image-transitions.md)
</dt> </dl>

 

 





