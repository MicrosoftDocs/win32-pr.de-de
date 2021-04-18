---
title: WMT_VIDEOIMAGE_TRANSITION_IRIS (wmsdkidl. h)
description: Der Iris-Übergang zeigt das neue Bild entlang einer x-Achse und einer y-Achse an. Der visuelle Effekt dieses Übergangs besteht darin, dass das neue Bild in einem erweiternden quer Sprung zu allen Seiten des Frames angezeigt wird.
ms.assetid: 7390d959-a566-43e7-937d-1e617bc98a6e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_IRIS Windows Media-Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_IRIS
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd216c7387f850f317417717c50216dd63449843
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372141"
---
# <a name="wmt_videoimage_transition_iris"></a>WMT \_ Videoimage- \_ Übergangs \_ IRIS

Der Iris-Übergang zeigt das neue Bild entlang einer x-Achse und einer y-Achse an. Der visuelle Effekt dieses Übergangs besteht darin, dass das neue Bild in einem erweiternden quer Sprung zu allen Seiten des Frames angezeigt wird.

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
<td>X-Koordinate relativ zum Videorahmen der Mitte des IRIS-Effekts.</td>
</tr>
<tr class="even">
<td>Y zentrieren</td>
<td><strong>fEffectPara1</strong></td>
<td>Y-Koordinate relativ zum Videorahmen der Mitte des Schwert Effekts.</td>
</tr>
<tr class="odd">
<td>Breite</td>
<td><strong>fEffectPara2</strong></td>
<td>Breite der vertikalen Linie, die das neue Bild offenbart, in Pixel.</td>
</tr>
<tr class="even">
<td>Höhe</td>
<td><strong>fEffectPara3</strong></td>
<td>Höhe der horizontalen Linie, die das neue Bild aufzeigt, in Pixel.</td>
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

 

 





