---
title: WMT_VIDEOIMAGE_TRANSITION_FILLED_V (Wmsdkidl.h)
description: Der ausgefüllte V-Übergang zeigt das neue Bild in einem Dreieck an, das von einer Seite des Rahmens stammt.
ms.assetid: d256178f-cb1d-4d36-9d30-e6dd6b3b23ec
keywords:
- WMT_VIDEOIMAGE_TRANSITION_FILLED_V Windows-Medienformat
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FILLED_V
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfbf032700959dd21a560b879357de2800ac657b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466157"
---
# <a name="wmt_videoimage_transition_filled_v"></a>WMT \_ VIDEOIMAGE \_ TRANSITION \_ FILLED \_ V

Der ausgefüllte V-Übergang zeigt das neue Bild in einem Dreieck an, das von einer Seite des Rahmens stammt.

## <a name="parameters"></a>Parameter

In der folgenden Tabelle werden die von diesem Übergang verwendeten Parameter beschrieben und die Elemente der [**WMT \_ VIDEOIMAGE \_ SAMPLE2-Struktur**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) aufgelistet, der sie zugewiesen sind.




| Parameter | Strukturmember | Beschreibung | 
|-----------|------------------|-------------|
| Breite | <strong>fEffectPara0</strong> | Breite des ausgefüllten V in Pixel. | 
| Höhe | <strong>fEffectPara1</strong> | Höhe des ausgefüllten V in Pixel. | 
| Direction | <strong>fEffectPara2</strong> | Richtung, aus der das gefüllte V stammt. Legen Sie auf einen der folgenden Werte fest:<br /><ul><li>0 : Gibt von der linken Seite des Frames ein.</li><li>1 : Gibt von der rechten Seite des Rahmens ein.</li><li>2 : Gibt vom unteren Rand des Frames ein.</li><li>3 : Gibt von oben im Frame ein.</li></ul> | 
| Aufbau | <strong>fEffectPara3</strong> | Legen Sie auf einen der folgenden Werte fest:<ul><li>0 : Gibt die normale Komposition an, bei der das vorherige Bild den Hintergrund und das aktuelle Bild den Vordergrund darstellt.</li><li>1 – Gibt die umgekehrte Komposition an, bei der das aktuelle Bild das Hintergrundbild und das vorherige Bild der Vordergrund ist.</li></ul> | 




 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Videobildübergänge**](video-image-transitions.md)
</dt> </dl>

 

 





