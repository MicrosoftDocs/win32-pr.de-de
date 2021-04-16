---
description: Gibt die maximale Anzahl von Ltr-Frames (Long Term Reference) an, die von der Anwendung gesteuert werden.
ms.assetid: C34AD867-5F94-4414-A282-ECC392678635
title: CODECAPI_AVEncVideoLTRBufferControl-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33adfc7d0ba2db87c2127489d9496dc5e0bb4158
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524632"
---
# <a name="codecapi_avencvideoltrbuffercontrol-property"></a>Codecapi \_ avencvideoltrbuffercontrol (Eigenschaft)

Gibt die maximale Anzahl von Ltr-Frames (Long Term Reference) an, die von der Anwendung gesteuert werden.

## <a name="data-type"></a>Datentyp

**Ulong** (VT \_ UI4)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avencvideoltrbuffercontrol**

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
<td>Die Anzahl der von der Anwendung kontrollierten Ltr-Frames.<br/> <strong>H. 264/AVC-Encoder:</strong><br/> Wenn der Wert n und n ungleich 0 (null) ist, muss der Encoder bei jedem IDR-Frame automatisch die Frames nach dem IDR-Frame (und dem IDR-Frame) als Ltr-Frames markieren, solange alle drei der folgenden Bedingungen zutreffen:
<ul>
<li>Der Frame ist nicht bereits so festgelegt, dass er als langfristiger Verweis Rahmen gekennzeichnet wird.</li>
<li>Der Frame ist ein basisebenenframe. Beispielsweise <strong>temporal_id</strong> -Syntax Element gleich 0 (null).</li>
<li>Die Anzahl der zurzeit als Ltr markierten Frames ist kleiner als N.</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span id="The_second_field"></span><span id="the_second_field"></span><span id="THE_SECOND_FIELD"></span><dl> <dt><strong>Das zweite Feld</strong></dt> <dt>Bits [16.. 31]</dt> </dl></td>
<td>Der Vertrauensstellungs Modus des Ltr-Steuer Elements.<br/> <strong>H. 264/AVC-Encoder:</strong><br/> 1 (Trust until) bedeutet, dass der Encoder einen Ltr-Frame verwenden kann, es sei denn, die APP macht Sie explizit über das <a href="codecapi-avencvideouseltrframe.md">CODECAPI_AVEncVideoUseLTRFrame</a> -Steuerelement ungültig. <br/> Andere Werte sind ungültig und sind für die zukünftige Verwendung reserviert.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Bemerkungen

Dies ist eine statische API.

Der Standardwert muss 0 sein.

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

 

 




