---
title: WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL (wmsdkidl. h)
description: Der Seiten rollenübergang transformiert das alte Bild mit einem Seitenumbruch Effekt und zeigt das neue Bild unterhalb an.
ms.assetid: 50efa4e9-0d3a-4b85-96b0-6d5cd637ca98
keywords:
- WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL Windows Media-Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4167395dbe00242af42f30713438f33e88f2dda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364836"
---
# <a name="wmt_videoimage_transition_page_roll"></a>WMT \_ Videoimage- \_ Übergangs \_ Seite \_ (Rollup)

Der Seiten rollenübergang transformiert das alte Bild mit einem Seitenumbruch Effekt und zeigt das neue Bild unterhalb an.

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
<td>Radius</td>
<td><strong>fEffectPara0</strong></td>
<td>Der Radius des Rollbacks im Seiten Roll Effekt.</td>
</tr>
<tr class="even">
<td>Entfernung</td>
<td><strong>fEffectPara1</strong></td>
<td>Die Menge des neuen Bilds, das durch den Seiten rollffekt in Pixel angezeigt wird.</td>
</tr>
<tr class="odd">
<td>Richtung</td>
<td><strong>fEffectPara2</strong></td>
<td>Die Ecke oder Seite des Video Rahmens, von der die Seiten Ausführung ausgeht. Legen Sie einen der folgenden Werte fest:<br/>
<ul>
<li>0-linke Seite</li>
<li>1-Rechte Seite</li>
<li>2-unten</li>
<li>3-oben</li>
<li>4-untere linke Ecke</li>
<li>5-untere rechte Ecke</li>
<li>6-obere linke Ecke</li>
<li>7-obere rechte Ecke</li>
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

 

 





