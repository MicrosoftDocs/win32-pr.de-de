---
title: WMT_VIDEOIMAGE_TRANSITION_DIAMOND (wmsdkidl. h)
description: Der rautenübergang zeigt das neue Bild in einem Diamanten.
ms.assetid: ff36a64d-62f7-424d-acc9-a7902926a90c
keywords:
- WMT_VIDEOIMAGE_TRANSITION_DIAMOND Windows Media-Format
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
ms.openlocfilehash: 9e3abfa337edd58fc536e530eb0ff6473c9a9d28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373614"
---
# <a name="wmt_videoimage_transition_diamond"></a>WMT \_ Videoimage- \_ Übergangs Raute \_

Der rautenübergang zeigt das neue Bild in einem Diamanten.

## <a name="parameters"></a>Parameter

In der folgenden Tabelle werden die Parameter beschrieben, die von diesem Übergang verwendet werden, und es werden die Elemente der [**WMT \_ Videoimage \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) -Struktur aufgelistet, der Sie zugewiesen sind.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Parameter</th>
<th>Strukturmember</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>X zentrieren</td>
<td><strong>fEffectPara0</strong></td>
<td>X-Koordinate relativ zum Videorahmen der Mitte des Diamanten.</td>
</tr>
<tr class="even">
<td>Y zentrieren</td>
<td><strong>fEffectPara1</strong></td>
<td>Y-Koordinate relativ zum Videorahmen der Mitte des Diamanten.</td>
</tr>
<tr class="odd">
<td>Breite</td>
<td><strong>fEffectPara2</strong></td>
<td>Breite des Diamanten in Pixel.</td>
</tr>
<tr class="even">
<td>Höhe</td>
<td><strong>fEffectPara3</strong></td>
<td>Höhe des Diamanten in Pixel.</td>
</tr>
<tr class="odd">
<td>Aufbau</td>
<td><strong>fEffectPara4</strong></td>
<td>Legen Sie einen der folgenden Werte fest:
<ul>
<li>0-gibt die normale Komposition an, in der das vorherige Bild den Hintergrund ist, und das aktuelle Bild ist der Vordergrund.</li>
<li>1: gibt die umgekehrte Komposition an, in der das aktuelle Bild das Hintergrundbild ist, und das vorherige Bild der Vordergrund.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmsdkidl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Video Bild Übergänge**](video-image-transitions.md)
</dt> </dl>

 

 





