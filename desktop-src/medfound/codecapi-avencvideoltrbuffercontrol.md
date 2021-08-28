---
description: Gibt die maximale Anzahl von LTR-Frames (Long Term Reference) an, die von der Anwendung gesteuert werden.
ms.assetid: C34AD867-5F94-4414-A282-ECC392678635
title: CODECAPI_AVEncVideoLTRBufferControl (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cca2e24e8295969609ba325a2abf24be76fb07c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481926"
---
# <a name="codecapi_avencvideoltrbuffercontrol-property"></a>CODECAPI \_ AVEncVideoLTRBufferControl(Eigenschaft)

Gibt die maximale Anzahl von LTR-Frames (Long Term Reference) an, die von der Anwendung gesteuert werden.

## <a name="data-type"></a>Datentyp

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncVideoLTRBufferControl**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieses Steuerelements enthält zwei Felder, wobei jedes Feld 16 Bits enthält.




| Wert | Bedeutung | 
|-------|---------|
| <span id="The_first_field"></span><span id="the_first_field"></span><span id="THE_FIRST_FIELD"></span><dl><dt><strong>Das erste Feld</strong></dt><dt>Bits[0..15]</dt></dl> | Die Anzahl von LTR-Frames, die von der Anwendung gesteuert werden.<br /><strong>H.264/AVC-Encoder:</strong><br /> Wenn der Wert N und N nicht null ist, muss der Encoder bei jedem IDR-Frame die Frames nach dem IDR-Frame (und einschließlich des IDR-Frames) automatisch als LTR-Frames markieren, solange alle drei der folgenden Bedingungen gelten:<ul><li>Der Frame ist noch nicht so festgelegt, dass er als langfristiger Referenzrahmen markiert wird.</li><li>Der Frame ist ein Basisebenenrahmen. Beispielsweise ist das <strong>Syntaxelement temporal_id</strong> gleich 0.</li><li>Die Anzahl der derzeit als LTR markierten Frames ist kleiner als N.</li></ul><br /> | 
| <span id="The_second_field"></span><span id="the_second_field"></span><span id="THE_SECOND_FIELD"></span><dl><dt><strong>Das zweite Feld</strong></dt><dt>Bits[16..31]</dt></dl> | Der Vertrauensmodus des LTR-Steuerelements.<br /><strong>H.264/AVC-Encoder:</strong><br /> 1 (Vertrauen bis) bedeutet, dass der Encoder einen LTR-Frame verwenden darf, es sei denn, die App macht ihn explizit über das CODECAPI_AVEncVideoUseLTRFrame <a href="codecapi-avencvideouseltrframe.md">ungültig.</a> <br /> Andere Werte sind ungültig und für die zukünftige Verwendung reserviert.<br /> | 




 

## <a name="remarks"></a>Hinweise

Dies ist eine statische API.

Der Standardwert muss 0 sein.

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

 

 




