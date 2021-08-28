---
title: WMT_VIDEOIMAGE_TRANSITION_DIAGONAL (Wmsdkidl.h)
description: Der diagonale Übergang zeigt das neue Bild entlang einer diagonalen Linie, die in einer Ecke des Rahmens entstanden ist.
ms.assetid: 1aaaf9e8-bbb8-4289-948e-5d352798e831
keywords:
- WMT_VIDEOIMAGE_TRANSITION_DIAGONAL Windows-Medienformat
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_DIAGONAL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea028777580f7414a834a0aa3e73e18db607eccd
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471986"
---
# <a name="wmt_videoimage_transition_diagonal"></a>WMT \_ VIDEOIMAGE \_ TRANSITION \_ DIAGONAL

Der diagonale Übergang zeigt das neue Bild entlang einer diagonalen Linie, die in einer Ecke des Rahmens entstanden ist.

## <a name="parameters"></a>Parameter

In der folgenden Tabelle werden die von diesem Übergang verwendeten Parameter beschrieben und die Member der [**WMT \_ VIDEOIMAGE \_ SAMPLE2-Struktur**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) aufgeführt, der sie zugewiesen sind.




| Parameter | Struktur-Member | Beschreibung | 
|-----------|------------------|-------------|
| Breite | <strong>fEffectPara0</strong> | Breite des diagonalen Abschnitts in Pixel. | 
| Höhe | <strong>fEffectPara1</strong> | Höhe des diagonalen Abschnitts in Pixel. | 
| Direction | <strong>fEffectPara2</strong> | Bestimmt die Ecke, aus der der Übergang stammt. Legen Sie auf eine der folgenden Bedingungen fest:<br /><ul><li>0 – Oben rechts</li><li>1 – Links oben</li><li>2 – Unten rechts</li><li>3– Unten links</li></ul> | 
| Aufbau | <strong>fEffectPara3</strong> | Legen Sie auf einen der folgenden Werte fest:<ul><li>0 : Gibt die normale Komposition an, bei der das vorherige Bild der Hintergrund und das aktuelle Bild der Vordergrund ist.</li><li>1 : Gibt die umgekehrte Komposition an, bei der das aktuelle Bild das Hintergrundbild und das vorherige Bild der Vordergrund ist.</li></ul> | 




 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Videobildübergänge**](video-image-transitions.md)
</dt> </dl>

 

 





