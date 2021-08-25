---
description: Markiert den aktuellen Frame als LTR-Frame.
ms.assetid: D70A54D6-DA9B-40E5-B130-0AA9C5363DF0
title: CODECAPI_AVEncVideoMarkLTRFrame-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a62f7bed0fd913dd17e06055ad259f4c8ed7037d90df2ecc53100e14ec4e505a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606430"
---
# <a name="codecapi_avencvideomarkltrframe-property"></a>CODECAPI \_ AVEncVideoMarkLTRFrame-Eigenschaft

Markiert den aktuellen Frame als LTR-Frame.

## <a name="data-type"></a>Datentyp

**ULONG** (VT \_ UI4)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncVideoMarkLTRFrame**

## <a name="remarks"></a>Hinweise

**H.264/AVC-Encoder:**

Der Wert dieses Steuerelements ist der Wert der H.264-Syntax *LongTermFramIdx,* die dem aktuellen Frame zugeordnet ist. Wenn sich der aktuelle Frame nicht in der Basisebene befindet, z. B. ist die *temporale \_ ID* des Syntaxelements nicht gleich 0, gilt diese Eigenschaft für den nächsten Basisebenenframe in der Codierungsreihenfolge.

Diese Eigenschaft sollte nicht aufgerufen werden, wenn ein ausstehender Aufruf zum Markieren eines LTR-Frames mithilfe der CODECAPI \_ AVEncVideoMarkLTRFrame-Eigenschaft ausgegeben wurde und der Encoder noch keinen Frame als LTR markiert hat. Anders ausgedrückt: Der Encoder sollte CODECAPI \_ AVEncVideoMarkLTRFrame-Anforderungen nicht in die Warteschlange stellen. Wenn eine CODECAPI \_ AVEncVideoMarkLTRFrame-Anforderung übermittelt wird, während eine andere CODECAPI \_ AVEncVideoMarkLTRFrame-Anforderung noch aussteht, sollte die ältere Anforderung gelöscht werden.

Die CODECAPI \_ AVEncVideoMarkLTRFrame-Eigenschaft ist dynamisch und kann während der Codierungssitzung festgelegt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 \|Desktop-Apps UWP-Apps\]<br/>                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[R2-Desktop-Apps \| UWP-Apps\]<br/>                        |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 




