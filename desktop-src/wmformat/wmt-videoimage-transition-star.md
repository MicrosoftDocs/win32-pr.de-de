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
ms.openlocfilehash: 2fd5a00c7cf68feea13dc0e617e5fe2adb34551032c8ec54bda6e0810fbb092e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118195170"
---
# <a name="wmt_videoimage_transition_star"></a>WMT \_ VIDEOIMAGE \_ TRANSITION \_ STAR

Der Sternübergang zeigt das neue Bild in einem Fünf-Punkte-Stern im Rahmen an.

## <a name="parameters"></a>Parameter

In der folgenden Tabelle werden die von diesem Übergang verwendeten Parameter beschrieben und die Member der [**WMT \_ VIDEOIMAGE \_ SAMPLE2-Struktur**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) aufgeführt, der sie zugewiesen sind.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Parameter</th>
<th>Struktur-Member</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>X zentrieren</td>
<td><strong>fEffectPara0</strong></td>
<td>X-Koordinate, relativ zum Videoframe, der Mitte des Sterns.</td>
</tr>
<tr class="even">
<td>Y zentrieren</td>
<td><strong>fEffectPara1</strong></td>
<td>Y-Koordinate, relativ zum Videoframe, der Mitte des Sterns.</td>
</tr>
<tr class="odd">
<td>Radius</td>
<td><strong>fEffectPara2</strong></td>
<td>Radius des Kreises, der durch die Punkte des Sterns definiert wird, in Pixel.</td>
</tr>
<tr class="even">
<td>Aufbau</td>
<td><strong>fEffectPara3</strong></td>
<td>Legen Sie auf einen der folgenden Werte fest:
<ul>
<li>0 : Gibt die normale Komposition an, bei der das vorherige Bild der Hintergrund und das aktuelle Bild der Vordergrund ist.</li>
<li>1 : Gibt die umgekehrte Komposition an, bei der das aktuelle Bild das Hintergrundbild und das vorherige Bild der Vordergrund ist.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Videobildübergänge**](video-image-transitions.md)
</dt> </dl>

 

 





