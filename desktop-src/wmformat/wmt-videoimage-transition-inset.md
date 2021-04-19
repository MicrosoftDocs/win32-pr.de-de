---
title: WMT_VIDEOIMAGE_TRANSITION_INSET (wmsdkidl. h)
description: Der einfügen-Übergang zeigt das neue Bild in einem Rechteck an, das aus einer Ecke des Frames stammt.
ms.assetid: fd8bc4b7-0546-4897-ab7b-a320bbd126ef
keywords:
- WMT_VIDEOIMAGE_TRANSITION_INSET Windows Media-Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_INSET
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddd41887fafaae2756e2dafe3d57d4f1a86edf46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354113"
---
# <a name="wmt_videoimage_transition_inset"></a>WMT \_ Videoimage- \_ Übergangs \_ inmenge

Der einfügen-Übergang zeigt das neue Bild in einem Rechteck an, das aus einer Ecke des Frames stammt.

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
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Breite</td>
<td><strong>fEffectPara0</strong></td>
<td>Breite des insets in Pixel.</td>
</tr>
<tr class="even">
<td>Höhe</td>
<td><strong>fEffectPara1</strong></td>
<td>Die Höhe des insets in Pixel.</td>
</tr>
<tr class="odd">
<td>Richtung</td>
<td><strong>fEffectPara2</strong></td>
<td>Ecke, von der die inmenge stammt. Legen Sie einen der folgenden Werte fest:<br/>
<ul>
<li>0-unten links</li>
<li>1-untere rechte Seite</li>
<li>2-obere linke Seite</li>
<li>3-obere rechte</li>
</ul></td>
</tr>
<tr class="even">
<td>Aufbau</td>
<td><strong>fEffectPara3</strong></td>
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

 

 





