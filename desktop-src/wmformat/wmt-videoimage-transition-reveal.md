---
title: WMT_VIDEOIMAGE_TRANSITION_REVEAL (wmsdkidl. h)
description: Der übereinungs Übergang zeigt das neue Bild entlang einer geraden Linie an, die von einer Seite des Frames stammt.
ms.assetid: 75ff6155-6b28-474a-b5d1-c3f1b3873b8e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_REVEAL Windows Media-Format
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
ms.openlocfilehash: a9aa385912cf106955dd33e06824d0b3668fcd97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365602"
---
# <a name="wmt_videoimage_transition_reveal"></a>WMT \_ Videoimage- \_ Übergang \_ offenlegen

Der übereinungs Übergang zeigt das neue Bild entlang einer geraden Linie an, die von einer Seite des Frames stammt.

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
<td>Entfernung</td>
<td><strong>fEffectPara0</strong></td>
<td>Der Umfang des neuen Bilds in Pixel. Dieser Wert ist relativ zur Ursprungsseite des Frames.</td>
</tr>
<tr class="even">
<td>Richtung</td>
<td><strong>fEffectPara1</strong></td>
<td>Die Richtung der Offenlegung. Legen Sie einen der folgenden Werte fest:<br/>
<ul>
<li>0-offenlegen rechts; von der linken Seite des Frames ausgehen.</li>
<li>1-offen Links anzeigen; von der rechten Seite des Frames ausgehen.</li>
<li>2-nach oben anzeigen vom unteren Rand des Frames ausgehen.</li>
<li>3: nach unten anzeigen vom oberen Rand des Frames ausgehen.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Aufbau</td>
<td><strong>fEffectPara2</strong></td>
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

 

 





