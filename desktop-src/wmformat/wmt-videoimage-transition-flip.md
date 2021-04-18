---
title: WMT_VIDEOIMAGE_TRANSITION_FLIP (wmsdkidl. h)
description: Der Flip-Übergang dreht das alte Bild auf einer y-Achse durch die Mitte des Frames. Das neue Bild wird als Rückseite des alten Bilds angezeigt.
ms.assetid: ff9990ef-962c-4dbb-b2bc-3bee070d2044
keywords:
- WMT_VIDEOIMAGE_TRANSITION_FLIP Windows Media-Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FLIP
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc92ad1dfffd945b89293dd9207289aa47645d4f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358802"
---
# <a name="wmt_videoimage_transition_flip"></a>WMT \_ Videoimage- \_ Übergang \_ kippen

Der Flip-Übergang dreht das alte Bild auf einer y-Achse durch die Mitte des Frames. Das neue Bild wird als Rückseite des alten Bilds angezeigt.

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
<td>Angle</td>
<td><strong>fEffectPara0</strong></td>
<td>Drehwinkel zwischen 0,0 und 180,0 Grad.</td>
</tr>
<tr class="even">
<td>Aufbau</td>
<td><strong>fEffectPara1</strong></td>
<td>Legen Sie einen der folgenden Werte fest:
<ul>
<li>0-gibt die normale Komposition an, in der das vorherige Bild den Hintergrund ist, und das aktuelle Bild ist der Vordergrund.</li>
<li>1: gibt die umgekehrte Komposition an, in der das aktuelle Bild das Hintergrundbild ist, und das vorherige Bild der Vordergrund.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Bemerkungen

Sie können die Auswirkung dieses Übergangs visualisieren, als ob beide Bilder physische Foto-und Back-to-Back-Listen darstellen. Der Übergang hat denselben Effekt wie das halten zweier solcher Fotos in der Mitte des unteren Rands und Rotieren der Fotos um 180 Grad.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmsdkidl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Video Bild Übergänge**](video-image-transitions.md)
</dt> </dl>

 

 





