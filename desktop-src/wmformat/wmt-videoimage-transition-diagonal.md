---
title: WMT_VIDEOIMAGE_TRANSITION_DIAGONAL (wmsdkidl. h)
description: Der Diagonale Übergang zeigt das neue Bild entlang einer diagonalen Linie, die in einer Ecke des Frames steht.
ms.assetid: 1aaaf9e8-bbb8-4289-948e-5d352798e831
keywords:
- WMT_VIDEOIMAGE_TRANSITION_DIAGONAL Windows Media-Format
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
ms.openlocfilehash: b6affa3e0727972e66e1ab6584c94ec233a11655
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358297"
---
# <a name="wmt_videoimage_transition_diagonal"></a>Übergang von WMT \_ Videoimage \_ \_ Diagonal

Der Diagonale Übergang zeigt das neue Bild entlang einer diagonalen Linie, die in einer Ecke des Frames steht.

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
<td>Breite des diagonalen Abschnitts in Pixel.</td>
</tr>
<tr class="even">
<td>Höhe</td>
<td><strong>fEffectPara1</strong></td>
<td>Höhe des diagonalen Abschnitts in Pixel.</td>
</tr>
<tr class="odd">
<td>Richtung</td>
<td><strong>fEffectPara2</strong></td>
<td>Bestimmt die Ecke, aus der der Übergang stammt. Legen Sie einen der folgenden Wert fest:<br/>
<ul>
<li>0 (oben rechts)</li>
<li>1-obere linke Seite</li>
<li>2-unten rechts</li>
<li>3-unten links</li>
</ul></td>
</tr>
<tr class="even">
<td>Aufbau</td>
<td><strong>fEffectPara3</strong></td>
<td>Legen Sie einen der folgenden Werte fest:
<ul>
<li>0-gibt die normale Komposition an, in der das vorherige Bild den Hintergrund ist, und das aktuelle Bild ist der Vordergrund.</li>
<li>1: gibt eine umgekehrte Komposition an, in der das aktuelle Bild das Hintergrundbild ist, und das vorherige Bild ist der Vordergrund.</li>
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

 

 





