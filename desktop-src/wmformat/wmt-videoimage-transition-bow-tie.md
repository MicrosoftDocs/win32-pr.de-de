---
title: WMT_VIDEOIMAGE_TRANSITION_BOW_TIE (Wmsdkidl.h)
description: Der Übergang der Bogenbinde zeigt das neue Bild in einer Reihe von Dreiecken auf gegenüberliegenden Seiten des Rahmens.
ms.assetid: d98da767-eea7-460c-ae5f-6bef9d93ad9d
keywords:
- WMT_VIDEOIMAGE_TRANSITION_BOW_TIE Windows-Medienformat
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
ms.openlocfilehash: 6f77cd2782bad6e4f83b5a4d1e719b0c21d704fefd2d4cccacfc0690a4fb0fa4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843951"
---
# <a name="wmt_videoimage_transition_bow_tie"></a>WMT \_ VIDEOIMAGE \_ TRANSITION \_ BOW \_ TIE

Der Übergang der Bogenbinde zeigt das neue Bild in einer Reihe von Dreiecken auf gegenüberliegenden Seiten des Rahmens.

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
<td>Breite</td>
<td><strong>fEffectPara0</strong></td>
<td>Breite der einzelnen dreieckigen Seiten der Schleifenbinde.</td>
</tr>
<tr class="even">
<td>Höhe</td>
<td><strong>fEffectPara1</strong></td>
<td>Höhe jeder dreieckigen Seite der Schleifenbinde.</td>
</tr>
<tr class="odd">
<td>Direction</td>
<td><strong>fEffectPara2</strong></td>
<td>Legen Sie auf einen der folgenden Werte fest:
<ul>
<li>0 – Gibt den horizontalen Schleifenbindereffekt an, bei dem die Dreiecke von der rechten und linken Seite des Rahmens gelangen.</li>
<li>1 : Gibt einen vertikalen Schleifenbindereffekt an, bei dem die Dreiecke von oben und unten in den Rahmen eintreten.</li>
</ul></td>
</tr>
<tr class="even">
<td>Aufbau</td>
<td><strong>fEffectPara3</strong></td>
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

 

 





