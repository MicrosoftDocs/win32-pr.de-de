---
title: WMT_VIDEOIMAGE_TRANSITION_WHEEL (wmsdkidl. h)
description: Der radübergang zeigt das neue Bild durch Drehen von vier Zeilen um einen gemeinsamen Pivotpunkt, wie z. b. die Spokes eines Rades.
ms.assetid: 426217be-789b-4b78-b0ea-de9629ecd46c
keywords:
- WMT_VIDEOIMAGE_TRANSITION_WHEEL Windows Media-Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_WHEEL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42f39d3355cfce3397c379bf7edafaae77ccfafe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369310"
---
# <a name="wmt_videoimage_transition_wheel"></a>WMT \_ Videoimage- \_ Übergangs \_ Rad

Der radübergang zeigt das neue Bild durch Drehen von vier Zeilen um einen gemeinsamen Pivotpunkt, wie z. b. die Spokes eines Rades.

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
<td>X-Koordinate relativ zum Videorahmen der Mitte des radeffekts.</td>
</tr>
<tr class="even">
<td>Y zentrieren</td>
<td><strong>fEffectPara1</strong></td>
<td>Y-Koordinate relativ zum Videorahmen der Mitte des radeffekts.</td>
</tr>
<tr class="odd">
<td>Angle</td>
<td><strong>fEffectPara2</strong></td>
<td>Der Drehwinkel für die Spokes des radeffekts in Grad. Der Wert 0,0 gibt das alte Bild an, ohne dass ein neues Bild angezeigt wird. Der Wert 90,0 gibt an, dass das neue Bild vollständig offengelegt ist. Die Verschiebung von 0,0 zu 90,0 wird als Drehung im Uhrzeigersinn der Spokes angezeigt.<br/></td>
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

 

 





