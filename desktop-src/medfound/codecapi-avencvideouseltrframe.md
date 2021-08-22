---
description: Gibt an, dass der aktuelle Frame mit einem oder mehreren LTR-Frames codiert wird.
ms.assetid: 51FD6E36-9CDF-4005-942F-7A92CA706F38
title: CODECAPI_AVEncVideoUseLTRFrame (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19b4df79755ed03873f0393d93f7e21ab8046af6295309207dc976f87eb0ee99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118743806"
---
# <a name="codecapi_avencvideouseltrframe-property"></a>CODECAPI \_ AVEncVideoUseLTRFrame (Eigenschaft)

Gibt an, dass der aktuelle Frame mit einem oder mehreren LTR-Frames codiert wird.

## <a name="data-type"></a>Datentyp

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncVideoUseLTRFrame**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieses Steuerelements enthält zwei Felder, wobei jedes Feld 16 Bits enthält.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Wert</th>
<th>Bedeutung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="The_first_field"></span><span id="the_first_field"></span><span id="THE_FIRST_FIELD"></span><dl> <dt><strong>Das erste Feld</strong></dt> <dt>Bits[0..15]</dt> </dl></td>
<td>Gibt an, welche LTR-Frames für die Codierung des aktuellen Frames zulässig sind. <br/> <strong>H.264/AVC-Encoder:</strong><br/> Dies ist eine Bitmap, die angibt, welche LTR-Frames als Referenz für diesen Frame verwendet werden können. Das am wenigsten signifikante Bit entspricht LTR-Index 0, das zweite am wenigsten signifikante Bit entspricht LTR-Index 1 usw.<br/> Dieser Wert darf nicht 0 sein.<br/> Der höchste durch diesen Wert angegebene Index darf nicht größer als <a href="codecapi-avencvideoltrbuffercontrol.md"></a> die maximale Anzahl von LTR-Frames sein, die in der CODECAPI_AVEncVideoLTRBufferControl eigenschaft kleiner als eins angegeben ist.<br/></td>
</tr>
<tr class="even">
<td><span id="The_second_field"></span><span id="the_second_field"></span><span id="THE_SECOND_FIELD"></span><dl> <dt><strong>Das zweite Feld</strong></dt> <dt>Bits[16..31]</dt> </dl></td>
<td>Flag, das angibt, ob zusätzliche Einschränkungen für die Codierung nachfolgender Frames erforderlich sind. <br/> <strong>H.264/AVC-Encoder:</strong><br/> 1 gilt für den einzigen gültigen Wert für dieses Feld. Alle anderen Werte sind ungültig und für die zukünftige Verwendung reserviert.<br/> Wenn das Flag 1 ist, muss der Encoder nachfolgende Frames in der Codierungs reihenfolge codieren, die den folgenden Einschränkungen unterliegt:<br/>
<ul>
<li>Es dürfen keine kurzfristigen Referenzframes in der Codierungs reihenfolge verwendet werden, die älter als der aktuelle Frame oder die zukünftige Codierung in der Codierungs reihenfolge ist.</li>
<li>Es dürfen keine LTR-Frames verwendet werden, die nicht vom letzten Steuerelement CODECAPI_AVEncVideoUseLTRFrame werden.</li>
<li>Möglicherweise werden LTR-Frames verwendet, die nach dem aktuellen Frame aktualisiert wurden.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Hinweise

**H.264/AVC-Encoder:**

Diese Eigenschaft sollte nicht aufgerufen werden, wenn ein ausstehender Aufruf zur Verwendung eines LTR-Frames mithilfe der CODECAPI-Eigenschaft AVEncVideoUseLTRFrame ausgegeben wurde und der Encoder noch keinen Frame generiert hat, der die LTR verwendet \_ hat. Anders ausgedrückt: Der Encoder sollte \_ CODECAPI-AVEncVideoUseLTRFrame-Anforderungen nicht in die Warteschlange stellen.

Wenn eine CODECAPI AVEncVideoUseLTRFrame-Anforderung übermittelt wird, während eine andere \_ CODECAPI AVEncVideoUseLTRFrame-Anforderung noch aussteht, sollte die ältere Anforderung \_ gelöscht werden.

Der Aufruf von CODECAPI AVEncVideoUseLTRFrame in einem Nicht-Basisebenenframe ist gültig und gilt ohne Verzögerung für einen Basisebenenrahmen für den \_ Nicht-Basisebenenrahmen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Desktop-Apps \| UWP-Apps\]<br/>                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[R2-Desktop-Apps \| UWP-Apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 




