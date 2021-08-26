---
title: WMT_VIDEOIMAGE_TRANSITION_SLIDE (Wmsdkidl.h)
description: Der Schiebeübergang zeigt das neue Bild an, indem das alte Bild aus dem Rahmen geschiebet wird.
ms.assetid: 925bcf92-5608-48ca-9bdc-dd08bcd8b8d5
keywords:
- WMT_VIDEOIMAGE_TRANSITION_SLIDE Windows-Medienformat
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_SLIDE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9866706528cab038042adc8d098743ce6588c805
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476336"
---
# <a name="wmt_videoimage_transition_slide"></a>WMT \_ VIDEOIMAGE \_ TRANSITION \_ SLIDE

Der Schiebeübergang zeigt das neue Bild an, indem das alte Bild aus dem Rahmen geschiebet wird.

## <a name="parameters"></a>Parameter

In der folgenden Tabelle werden die von diesem Übergang verwendeten Parameter beschrieben und die Elemente der [**WMT \_ VIDEOIMAGE \_ SAMPLE2-Struktur**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) aufgelistet, der sie zugewiesen sind.




| Parameter | Strukturmember | BESCHREIBUNG | 
|-----------|------------------|-------------|
| Distance | <strong>fEffectPara0</strong> | Abstand in Pixel, in dem das alte Bild aus dem Rahmen schiebet. | 
| Direction | <strong>fEffectPara1</strong> | Richtung, in die das alte Bild schiebet. Legen Sie auf einen der folgenden Werte fest:<br /><ul><li>0 – Nach rechts schieben.</li><li>1 – Nach links schieben.</li><li>2 – Nach oben schieben.</li><li>3 – Nach unten gleiten.</li></ul> | 
| Aufbau | <strong>fEffectPara2</strong> | Legen Sie auf einen der folgenden Werte fest:<ul><li>0 : Gibt die normale Komposition an, bei der das vorherige Bild den Hintergrund und das aktuelle Bild den Vordergrund darstellt.</li><li>1 : Gibt die umgekehrte Komposition an, bei der das aktuelle Bild das Hintergrundbild und das vorherige Bild der Vordergrund ist.</li></ul> | 




 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Videobildübergänge**](video-image-transitions.md)
</dt> </dl>

 

 





