---
description: Die TSPI LINE \_ QOSINFO-Meldung bewirkt, dass TAPI ein QOS-Ereignis aus löst. Weitere Informationen finden Sie unter ITQOSEvent.
ms.assetid: b2844d12-c524-42ab-aeb9-8daf4e07a436
title: LINE_QOSINFO (Tspi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f0e6273eb31447f0e0c9543dfa191a25869fa08f05be8a5c639ceb101deff47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873320"
---
# <a name="line_qosinfo-message"></a>LINE \_ QOSINFO-Nachricht

Die TSPI **LINE \_ QOSINFO-Meldung** bewirkt, dass TAPI ein QOS-Ereignis aus löst. Weitere [**Informationen finden Sie unter ITQOSEvent.**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent)


```C++
        
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*htLine* 
</dt> <dd>

Das TAPI-Handle für die Zeile.

</dd> <dt>

*htCall* 
</dt> <dd>

Das TAPI-Handle für den Aufruf.

</dd> <dt>

*dwMsg* 
</dt> <dd>

Der Wert LINE \_ QOSINFO.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Ein Member des [**QOS EVENT-Enumerators, \_**](/windows/win32/api/tapi3if/ne-tapi3if-qos_event) der den Ereignistyp identifiziert.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Eine [Medientypkonst](./tapiprotocol--constants.md) constant, die das Medium des Aufrufs identifiziert, der diesem Ereignis zugeordnet ist.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.2<br/>                                                      |
| Header<br/>       | <dl> <dt>Tspi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_QOS-EREIGNIS**](/windows/win32/api/tapi3if/ne-tapi3if-qos_event)
</dt> <dt>

[**ITQOSEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent)
</dt> </dl>

 

