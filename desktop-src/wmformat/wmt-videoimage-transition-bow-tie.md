---
title: WMT_VIDEOIMAGE_TRANSITION_BOW_TIE (wmsdkidl. h)
description: Der Bogen Binder Übergang zeigt das neue Bild in einer Reihe von Dreiecken auf gegenüberliegenden Seiten des Rahmens an.
ms.assetid: d98da767-eea7-460c-ae5f-6bef9d93ad9d
keywords:
- WMT_VIDEOIMAGE_TRANSITION_BOW_TIE Windows Media-Format
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_BOW_TIE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd4d426c335a30853085a2501206ccd6e7efc7e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355881"
---
# <a name="wmt_videoimage_transition_bow_tie"></a>WMT \_ Videoimage- \_ Übergangs \_ Bogen \_ Tie

Der Bogen Binder Übergang zeigt das neue Bild in einer Reihe von Dreiecken auf gegenüberliegenden Seiten des Rahmens an.

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
<td>Breite jeder dreieckigen Seite des Bogen links.</td>
</tr>
<tr class="even">
<td>Höhe</td>
<td><strong>fEffectPara1</strong></td>
<td>Die Höhe jeder dreieckigen Seite des Bogen-links.</td>
</tr>
<tr class="odd">
<td>Richtung</td>
<td><strong>fEffectPara2</strong></td>
<td>Legen Sie einen der folgenden Werte fest:
<ul>
<li>0-gibt den horizontalen bogeneiendeeffekt an, in dem die Dreiecke von der rechten und linken Seite des Frames eingegeben werden.</li>
<li>1: gibt den vertikalen Bogen Binder Effekt an, in dem die Dreiecke vom oberen und unteren Rand des Frames eingegeben werden.</li>
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

 

 





