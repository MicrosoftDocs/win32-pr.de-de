---
title: WMT_VIDEOIMAGE_TRANSITION_DIAMOND (Wmsdkidl.h)
description: Der Rautenübergang zeigt das neue Bild in einer Raute an.
ms.assetid: ff36a64d-62f7-424d-acc9-a7902926a90c
keywords:
- WMT_VIDEOIMAGE_TRANSITION_DIAMOND windows Media Format
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
ms.openlocfilehash: af271c220fc48924905a067336a438baec1ef0ac4b2dca1b266d3ea77d665f71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117653281"
---
# <a name="wmt_videoimage_transition_diamond"></a>WMT \_ VIDEOIMAGE \_ TRANSITION \_ DIAMOND

Der Rautenübergang zeigt das neue Bild in einer Raute an.

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
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>X zentrieren</td>
<td><strong>fEffectPara0</strong></td>
<td>X-Koordinate relativ zum Videoframe des Mittelpunkts der Raute.</td>
</tr>
<tr class="even">
<td>Y zentrieren</td>
<td><strong>fEffectPara1</strong></td>
<td>Y-Koordinate relativ zum Videoframe des Mittelpunkts der Raute.</td>
</tr>
<tr class="odd">
<td>Breite</td>
<td><strong>fEffectPara2</strong></td>
<td>Breite der Raute in Pixel.</td>
</tr>
<tr class="even">
<td>Höhe</td>
<td><strong>fEffectPara3</strong></td>
<td>Höhe der Raute in Pixel.</td>
</tr>
<tr class="odd">
<td>Aufbau</td>
<td><strong>fEffectPara4</strong></td>
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

 

 





