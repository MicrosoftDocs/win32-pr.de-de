---
description: Gibt an, dass der aktuelle Frame mit einem oder mehreren Ltr-Frames codiert wird.
ms.assetid: 51FD6E36-9CDF-4005-942F-7A92CA706F38
title: CODECAPI_AVEncVideoUseLTRFrame-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 252933180e8212c94c3c2b2442397c53d0f9c559
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749353"
---
# <a name="codecapi_avencvideouseltrframe-property"></a>Codecapi \_ avencvideouseltrframe (Eigenschaft)

Gibt an, dass der aktuelle Frame mit einem oder mehreren Ltr-Frames codiert wird.

## <a name="data-type"></a>Datentyp

**Ulong** (VT \_ UI4)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avencvideouseltrframe**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieses Steuer Elements enthält zwei Felder, in denen jedes Feld über 16 Bits verfügt.



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
<td><span id="The_first_field"></span><span id="the_first_field"></span><span id="THE_FIRST_FIELD"></span><dl> <dt><strong>Die ersten feldbits</strong></dt> <dt>[0.. 15]</dt> </dl></td>
<td>Gibt an, welche Ltr-Frames zum Codieren des aktuellen Frames zulässig sind. <br/> <strong>H. 264/AVC-Encoder:</strong><br/> Dies ist eine Bitmap, die angibt, welche Ltr-Frames als Verweis für diesen Frame verwendet werden können. Das unwichtigste Bit entspricht dem Ltr-Index 0, das zweite unwichtigste Bit entspricht dem Ltr-Index 1 usw.<br/> Dieser Wert darf nicht 0 sein.<br/> Der höchste Index, der durch diesen Wert angegeben wird, darf nicht größer als die maximale Anzahl von Ltr-Frames sein, die in der <a href="codecapi-avencvideoltrbuffercontrol.md">CODECAPI_AVEncVideoLTRBufferControl</a> -Eigenschaft festgelegt ist.<br/></td>
</tr>
<tr class="even">
<td><span id="The_second_field"></span><span id="the_second_field"></span><span id="THE_SECOND_FIELD"></span><dl> <dt><strong>Das zweite Feld</strong></dt> <dt>Bits [16.. 31]</dt> </dl></td>
<td>Flag, das angibt, ob für das Codieren von nachfolgenden Frames zusätzliche Einschränkungen erforderlich sind. <br/> <strong>H. 264/AVC-Encoder:</strong><br/> 1 ist der einzige gültige Wert für dieses Feld. Alle anderen Werte sind ungültig und sind für die zukünftige Verwendung reserviert.<br/> Wenn das Flag 1 ist, muss der Encoder nachfolgende Frames in der Codierungs Reihenfolge codieren, die den folgenden Einschränkungen unterliegen:<br/>
<ul>
<li>Es dürfen keine kurzfristigen Verweis Rahmen in der Codierungs Reihenfolge verwendet werden, die älter als der aktuelle Frame oder in der Codierungs Reihenfolge ist.</li>
<li>Es dürfen keine Ltr-Frames verwendet werden, die nicht vom letzten CODECAPI_AVEncVideoUseLTRFrame Steuerelement beschrieben werden.</li>
<li>Es können Ltr-Frames verwendet werden, die nach dem aktuellen Frame aktualisiert wurden.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Bemerkungen

**H. 264/AVC-Encoder:**

Diese Eigenschaft sollte nicht aufgerufen werden, wenn ein ausstehender Aufruf zur Verwendung eines Ltr-Frames mithilfe der codecapi- \_ Eigenschaft "avencvideouseltrframe" ausgegeben wurde und der Encoder noch keinen Frame generiert hat, der die Ltr verwendet hat. Anders ausgedrückt: der Encoder sollte codecapi- \_ krecvideouseltrframe-Anforderungen nicht in die Warteschlange stellen.

Wenn eine codecapi-Regel " \_ avencvideouseltrframe" übermittelt wird, während eine andere codecapi-Datei " \_ avencvideouseltrframe" noch aussteht, sollte die ältere Anforderung gelöscht werden.

Das Aufrufen von codecapi \_ avencvideouseltrframe auf einem nicht-Basisschicht Rahmen ist gültig und sollte auf den nicht-Basisschicht Rahmen angewendet werden, ohne dass ein basisebenenframe verzögert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1 \[ Desktop-Apps \| UWP-apps\]<br/>                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




