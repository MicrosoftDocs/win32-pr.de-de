---
title: ncadg_mq-Attribut
description: Das Schlüsselwort ncadg \_ mq identifiziert Microsoft Message Queuing Services (MSMQ) als Transportprotokoll für den Endpunkt. Dieses Protokoll ist veraltet und sollte nicht in neuen Anwendungen verwendet werden.
ms.assetid: 7472fc47-c1f0-4578-8aef-b655505e0563
keywords:
- ncadg_mq-Attribut MIDL
topic_type:
- apiref
api_name:
- ncadg_mq
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0164211a267760a533d8d164a76387dbbcfba8a0aad8e4ac6ecaf20ed770708a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067020"
---
# <a name="ncadg_mq-attribute"></a>ncadg \_ mq-Attribut

Das Schlüsselwort **ncadg \_ mq** identifiziert Microsoft Message Queuing Services (MSMQ) als Transportprotokoll für den Endpunkt. Dieses Protokoll ist veraltet und sollte nicht in neuen Anwendungen verwendet werden.

``` syntax
endpoint("ncadg_mq:server-name")
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Servername* 
</dt> <dd>

Gibt den Namen des Servers oder Hosts an. Der Name ist eine Zeichenfolge und kann ein vollqualifizierter Domänenname sein.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Um das **ncadg \_ mq-Transportprotokoll** verwenden zu können, müssen die MSMQ-Komponenten vollständig installiert sein, und die Client- und Serversysteme müssen über die MQ-Protokolle erreichbar sein.

Das **ncadg \_ mq-Protokoll** unterstützt keine dynamischen Endpunkte oder [**Broadcastaufrufe.**](broadcast.md) Wie bei anderen Datagrammprotokollen unterstützt **ncadg \_ mq** keine Rückrufe. Alle Funktionen, die das [**Rückrufattribut**](callback.md) verwenden, schlagen fehl.

> [!Note]  
> Diese Protokollfamilie wird in Windows XP nicht unterstützt.

 

## <a name="examples"></a>Beispiele

Die Syntax des Nachrichtenwarteschlangenprotokolls wird unabhängig von der IDL-Spezifikation definiert. Der MIDL-Compiler führt eine Syntaxüberprüfung durch, garantiert jedoch nicht, dass die Endpunktspezifikation korrekt ist. Einige Fehler können zur Laufzeit und nicht während der Kompilierung gemeldet werden.

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_mq:rainier") 
]
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sendung**](broadcast.md)
</dt> <dt>

[**Rückruf**](callback.md)
</dt> <dt>

[**Endpunkt**](endpoint.md)
</dt> <dt>

[IDL-Datei (Interface Definition)](interface-definition-idl-file.md)
</dt> <dt>

[**Nachricht**](message.md)
</dt> <dt>

[RPC-Message Queuing](/windows/desktop/Rpc/rpc-message-queuing)
</dt> <dt>

[Zeichenfolgenbindung](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 