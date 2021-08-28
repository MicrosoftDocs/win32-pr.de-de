---
title: WMT_VIDEOIMAGE_TRANSITION_REVEAL (Wmsdkidl.h)
description: Der Reveal-Übergang zeigt das neue Bild entlang einer geraden Linie, die von einer Seite des Frames stammt.
ms.assetid: 75ff6155-6b28-474a-b5d1-c3f1b3873b8e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_REVEAL Windows-Medienformat
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_REVEAL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 140271d365d9673c948c4ff6f540e9bef33e8006
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469317"
---
# <a name="wmt_videoimage_transition_reveal"></a>WMT \_ VIDEOIMAGE \_ TRANSITION \_ REVEAL

Der Reveal-Übergang zeigt das neue Bild entlang einer geraden Linie, die von einer Seite des Frames stammt.

## <a name="parameters"></a>Parameter

In der folgenden Tabelle werden die von diesem Übergang verwendeten Parameter beschrieben und die Elemente der [**WMT \_ VIDEOIMAGE \_ SAMPLE2-Struktur**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) aufgelistet, der sie zugewiesen sind.




| Parameter | Strukturmember | BESCHREIBUNG | 
|-----------|------------------|-------------|
| Distance | <strong>fEffectPara0</strong> | Die Menge des angezeigten neuen Bilds in Pixel. Dieser Wert ist relativ zur Ursprungsseite des Frames. | 
| Direction | <strong>fEffectPara1</strong> | Richtung des aufschlussenden . Legen Sie auf einen der folgenden Werte fest:<br /><ul><li>0 – Rechts zeigen; stammen von der linken Seite des Frames.</li><li>1 – Links zeigen; stammen von der rechten Seite des Frames.</li><li>2 – Aufwärts zeigen; stammen vom unteren Rand des Frames.</li><li>3– Nach unten zeigen; stammen aus dem oberen Rand des Frames.</li></ul> | 
| Aufbau | <strong>fEffectPara2</strong> | Legen Sie auf einen der folgenden Werte fest:<ul><li>0 : Gibt die normale Komposition an, bei der das vorherige Bild den Hintergrund und das aktuelle Bild den Vordergrund darstellt.</li><li>1 : Gibt die umgekehrte Komposition an, bei der das aktuelle Bild das Hintergrundbild und das vorherige Bild der Vordergrund ist.</li></ul> | 




 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Videobildübergänge**](video-image-transitions.md)
</dt> </dl>

 

 





