---
title: WMT_VIDEOIMAGE_TRANSITION_FLIP (Wmsdkidl.h)
description: Der Kippübergang dreht das alte Bild auf einer y-Achse durch die Mitte des Rahmens. Das neue Bild wird als Rückseite des alten Bilds angezeigt.
ms.assetid: ff9990ef-962c-4dbb-b2bc-3bee070d2044
keywords:
- WMT_VIDEOIMAGE_TRANSITION_FLIP Windows-Medienformat
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
ms.openlocfilehash: a194067fd8a5bb34569723245b68996163d0cd9a2eef332e6f42fceb8187eecb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590650"
---
# <a name="wmt_videoimage_transition_flip"></a>WMT \_ VIDEOIMAGE \_ TRANSITION \_ FLIP

Der Kippübergang dreht das alte Bild auf einer y-Achse durch die Mitte des Rahmens. Das neue Bild wird als Rückseite des alten Bilds angezeigt.

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
<td>Angle</td>
<td><strong>fEffectPara0</strong></td>
<td>Drehwinkel von 0,0 bis 180,0 Grad.</td>
</tr>
<tr class="even">
<td>Aufbau</td>
<td><strong>fEffectPara1</strong></td>
<td>Legen Sie auf einen der folgenden Werte fest:
<ul>
<li>0 : Gibt die normale Komposition an, bei der das vorherige Bild der Hintergrund und das aktuelle Bild der Vordergrund ist.</li>
<li>1 : Gibt die umgekehrte Komposition an, bei der das aktuelle Bild das Hintergrundbild und das vorherige Bild der Vordergrund ist.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Hinweise

Sie können den Effekt dieses Übergangs so visualisieren, als ob beide Bilder physische Fotos sind, die von einem Back-to-Back-Bild miteinander verknaben. Der Übergang hat den gleichen Effekt wie das Halten von zwei solchen Fotos in der Mitte des unteren Rands und deren Drehung um 180 Grad.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Videobildübergänge**](video-image-transitions.md)
</dt> </dl>

 

 





