---
description: Die TSPI-Zeilen- \_ qosinfo-Nachricht bewirkt, dass TAPI ein QoS-Ereignis auslöst. Weitere Informationen finden Sie unter itqoabvent.
ms.assetid: b2844d12-c524-42ab-aeb9-8daf4e07a436
title: LINE_QOSINFO Meldung (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d35ff19601ab6acd9a3d8e8aebf1e59b06a4f17e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351354"
---
# <a name="line_qosinfo-message"></a>Zeilen- \_ qosinfo-Meldung

Die TSPI- **Zeilen- \_ qosinfo** -Nachricht bewirkt, dass TAPI ein QoS-Ereignis auslöst. Weitere Informationen finden Sie unter [**itqoabvent**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent) .


```C++
        
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*htline* 
</dt> <dd>

Der TAPI-Handle für die Zeile.

</dd> <dt>

*"htcall"* 
</dt> <dd>

Der TAPI-Handle für den-Befehl.

</dd> <dt>

*dwmsg* 
</dt> <dd>

Die Wert Zeile \_ qosinfo.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Ein Member des [**QoS- \_ Ereignis**](/windows/win32/api/tapi3if/ne-tapi3if-qos_event) Enumerators, der den Ereignistyp identifiziert.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Eine [Medientyp](./tapiprotocol--constants.md) Konstante, die die Medien des diesem Ereignis zugeordneten Aufrufes angibt.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,2<br/>                                                      |
| Header<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**QoS- \_ Ereignis**](/windows/win32/api/tapi3if/ne-tapi3if-qos_event)
</dt> <dt>

[**Itqoabvent**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent)
</dt> </dl>

 

