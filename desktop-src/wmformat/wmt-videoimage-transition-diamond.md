---
title: WMT_VIDEOIMAGE_TRANSITION_DIAMOND (Wmsdkidl.h)
description: Der Rautenübergang zeigt das neue Bild in einer Raute an.
ms.assetid: ff36a64d-62f7-424d-acc9-a7902926a90c
keywords:
- WMT_VIDEOIMAGE_TRANSITION_DIAMOND Windows-Medienformat
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_DIAMOND
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38731c93ae9ada520f286ae1662d45ec95d399d4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473496"
---
# <a name="wmt_videoimage_transition_diamond"></a>WMT \_ VIDEOIMAGE \_ TRANSITION \_ DIAMOND

Der Rautenübergang zeigt das neue Bild in einer Raute an.

## <a name="parameters"></a>Parameter

In der folgenden Tabelle werden die von diesem Übergang verwendeten Parameter beschrieben und die Elemente der [**WMT \_ VIDEOIMAGE \_ SAMPLE2-Struktur**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) aufgelistet, der sie zugewiesen sind.




| Parameter | Strukturmember | BESCHREIBUNG | 
|-----------|------------------|-------------|
| X zentrieren | <strong>fEffectPara0</strong> | X-Koordinate relativ zum Videorahmen der Rautenmitte. | 
| Y zentrieren | <strong>fEffectPara1</strong> | Y-Koordinate relativ zum Videorahmen der Rautenmitte. | 
| Breite | <strong>fEffectPara2</strong> | Breite des Rautens in Pixel. | 
| Höhe | <strong>fEffectPara3</strong> | Höhe des Diamanten in Pixel. | 
| Aufbau | <strong>fEffectPara4</strong> | Legen Sie auf einen der folgenden Werte fest:<ul><li>0 : Gibt die normale Komposition an, bei der das vorherige Bild den Hintergrund und das aktuelle Bild den Vordergrund darstellt.</li><li>1 – Gibt die umgekehrte Komposition an, bei der das aktuelle Bild das Hintergrundbild und das vorherige Bild der Vordergrund ist.</li></ul> | 




 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Videobildübergänge**](video-image-transitions.md)
</dt> </dl>

 

 





