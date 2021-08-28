---
title: WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL (Wmsdkidl.h)
description: Der Seitenrollübergang transformiert das alte Bild mit einem Seitenumkehreffekt, der das neue Bild darunter zeigt.
ms.assetid: 50efa4e9-0d3a-4b85-96b0-6d5cd637ca98
keywords:
- WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL windows Media Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bfa69988f5b5414eac3e27b3371bca0e0a28810
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474976"
---
# <a name="wmt_videoimage_transition_page_roll"></a>WMT \_ VIDEOIMAGE \_ TRANSITION \_ PAGE \_ ROLL

Der Seitenrollübergang transformiert das alte Bild mit einem Seitenumkehreffekt, der das neue Bild darunter zeigt.

## <a name="parameters"></a>Parameter

In der folgenden Tabelle werden die von diesem Übergang verwendeten Parameter beschrieben und die Member der [**WMT \_ VIDEOIMAGE \_ SAMPLE2-Struktur**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) aufgeführt, der sie zugewiesen sind.




| Parameter | Struktur-Member | BESCHREIBUNG | 
|-----------|------------------|-------------|
| Radius | <strong>fEffectPara0</strong> | Radius des Rolls im Seitenrolleffekt. | 
| Distance | <strong>fEffectPara1</strong> | Die Menge des neuen Bilds, das durch den Seitenrolleffekt in Pixel angezeigt wird. | 
| Direction | <strong>fEffectPara2</strong> | Ecke oder Seite des Videoframes, aus der der Seitenroll stammt. Legen Sie auf einen der folgenden Werte fest:<br /><ul><li>0 – Linke Seite</li><li>1– Rechte Seite</li><li>2 – Unten</li><li>3 – Oben</li><li>4– Linke untere Ecke</li><li>5: Rechte untere Ecke</li><li>6 – Obere linke Ecke</li><li>7 – Obere rechte Ecke</li></ul> | 
| Aufbau | <strong>fEffectPara3</strong> | Legen Sie auf einen der folgenden Werte fest:<ul><li>0 : Gibt die normale Komposition an, bei der das vorherige Bild der Hintergrund und das aktuelle Bild der Vordergrund ist.</li><li>1 : Gibt die umgekehrte Komposition an, bei der das aktuelle Bild das Hintergrundbild und das vorherige Bild der Vordergrund ist.</li></ul> | 




 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Videobildübergänge**](video-image-transitions.md)
</dt> </dl>

 

 





