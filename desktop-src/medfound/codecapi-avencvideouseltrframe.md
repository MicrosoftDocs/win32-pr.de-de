---
description: Gibt an, dass der aktuelle Frame mit einem oder mehreren LTR-Frames codiert wird.
ms.assetid: 51FD6E36-9CDF-4005-942F-7A92CA706F38
title: CODECAPI_AVEncVideoUseLTRFrame -Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c438a4e6e2656c5e952062d9e3c1c0000899f2c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473156"
---
# <a name="codecapi_avencvideouseltrframe-property"></a>CODECAPI \_ AVEncVideoUseLTRFrame-Eigenschaft

Gibt an, dass der aktuelle Frame mit einem oder mehreren LTR-Frames codiert wird.

## <a name="data-type"></a>Datentyp

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncVideoUseLTRFrame**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieses Steuerelements enthält zwei Felder, wobei jedes Feld 16 Bits hat.




| Wert | Bedeutung | 
|-------|---------|
| <span id="The_first_field"></span><span id="the_first_field"></span><span id="THE_FIRST_FIELD"></span><dl><dt><strong>Das erste Feld</strong></dt><dt>Bits[0..15]</dt></dl> | Gibt an, welche LTR-Frames für die Codierung des aktuellen Frames zulässig sind. <br /><strong>H.264/AVC-Encoder:</strong><br /> Dies ist eine Bitmap, die angibt, welche LTR-Frames als Verweis für diesen Frame verwendet werden können. Das am wenigsten signifikante Bit entspricht LTR-Index 0, das zweite am wenigsten signifikante Bit dem LTR-Index 1 usw.<br /> Dieser Wert darf nicht 0 sein.<br /> Der höchste von diesem Wert angegebene Index darf nicht größer als die maximale Anzahl von LTR-Frames sein, die in der <a href="codecapi-avencvideoltrbuffercontrol.md">CODECAPI_AVEncVideoLTRBufferControl</a> Eigenschaft weniger als eins angegeben ist.<br /> | 
| <span id="The_second_field"></span><span id="the_second_field"></span><span id="THE_SECOND_FIELD"></span><dl><dt><strong>Das zweite Feld</strong></dt><dt>Bits[16..31]</dt></dl> | Flag, das angibt, ob zusätzliche Einschränkungen für die Codierung nachfolgender Frames erforderlich sind. <br /><strong>H.264/AVC-Encoder:</strong><br /> 1 befindet sich auf dem einzigen gültigen Wert für dieses Feld. Alle anderen Werte sind ungültig und für die zukünftige Verwendung reserviert.<br /> Wenn das Flag 1 ist, codiert der Encoder nachfolgende Frames gemäß den folgenden Einschränkungen in der Codierungsreihenfolge:<br /><ul><li>Es dürfen keine kurzzeitigen Verweisframes in der Codierungsreihenfolge verwendet werden, die älter als der aktuelle Frame ist, oder die zukünftige Codierung in der Codierungsreihenfolge.</li><li>Es dürfen keine LTR-Frames verwendet werden, die nicht vom neuesten CODECAPI_AVEncVideoUseLTRFrame-Steuerelement beschrieben werden.</li><li>Es können LTR-Frames verwendet werden, die nach dem aktuellen Frame aktualisiert wurden.</li></ul> | 




 

## <a name="remarks"></a>Hinweise

**H.264/AVC-Encoder:**

Diese Eigenschaft sollte nicht aufgerufen werden, wenn ein ausstehender Aufruf zur Verwendung eines LTR-Frames mithilfe der CODECAPI \_ AVEncVideoUseLTRFrame-Eigenschaft ausgegeben wurde und der Encoder noch keinen Frame generiert hat, der die LTR verwendet hat. Anders ausgedrückt: Der Encoder sollte CODECAPI \_ AVEncVideoUseLTRFrame-Anforderungen nicht in die Warteschlange stellen.

Wenn eine CODECAPI \_ AVEncVideoUseLTRFrame-Anforderung übermittelt wird, während eine andere CODECAPI \_ AVEncVideoUseLTRFrame-Anforderung noch aussteht, sollte die ältere Anforderung gelöscht werden.

Das Aufrufen von CODECAPI \_ AVEncVideoUseLTRFrame für einen Nicht-Basisebenenrahmen ist gültig und muss für den Nicht-Basisebenenrahmen ohne Verzögerung auf einen Basisebenenrahmen angewendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 \|Desktop-Apps UWP-Apps\]<br/>                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[R2-Desktop-Apps \| UWP-Apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 




