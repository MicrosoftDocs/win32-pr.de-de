---
title: ncadg_mq-Attribut
description: Das ncadg \_ MQ-Schlüsselwort identifiziert Microsoft Message Queuing Services (MSMQ) als Transportprotokoll für den Endpunkt. Dieses Protokoll ist veraltet und sollte in neuen Anwendungen nicht verwendet werden.
ms.assetid: 7472fc47-c1f0-4578-8aef-b655505e0563
keywords:
- ncadg_mq Attribut-Mittel l
topic_type:
- apiref
api_name:
- ncadg_mq
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0acc433b55ba9f3c6d8919bef9b8db470bc0f5a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948657"
---
# <a name="ncadg_mq-attribute"></a>ncadg \_ MQ-Attribut

Das **ncadg \_ MQ** -Schlüsselwort identifiziert Microsoft Message Queuing Services (MSMQ) als Transportprotokoll für den Endpunkt. Dieses Protokoll ist veraltet und sollte in neuen Anwendungen nicht verwendet werden.

``` syntax
endpoint("ncadg_mq:server-name")
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Servername* 
</dt> <dd>

Gibt den Namen des Servers oder Hosts an. Der Name ist eine Zeichenfolge und kann ein voll qualifizierter Domänen Name sein.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Um das **ncadg \_ MQ** -Transportprotokoll verwenden zu können, müssen die MSMQ-Komponenten vollständig installiert sein, und die Client-und Serversysteme müssen über die MQ-Protokolle erreichbar sein.

Das **ncadg \_ MQ** -Protokoll unterstützt keine dynamischen Endpunkte oder [**Broadcast**](broadcast.md) Aufrufe. Wie bei anderen datagrammprotokollen unterstützt **ncadg \_ MQ** keine Rückrufe. alle Funktionen, die das [**Rückruf**](callback.md) Attribut verwenden, schlagen fehl.

> [!Note]  
> Diese Protokollfamilie wird in Windows XP nicht unterstützt.

 

## <a name="examples"></a>Beispiele

Die Syntax des Message-Queue-Protokolls wird unabhängig von der IDL-Spezifikation definiert. Der mittlerer l-Compiler führt einige Syntax Überprüfungen durch, garantiert jedoch nicht, dass die Endpunkt Spezifikation korrekt ist. Einige Fehler werden möglicherweise zur Laufzeit gemeldet, nicht während der Kompilierung.

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

[**aus**](broadcast.md)
</dt> <dt>

[**Rückruf**](callback.md)
</dt> <dt>

[**Dreher**](endpoint.md)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Nachricht**](message.md)
</dt> <dt>

[RPC-Message Queuing](/windows/desktop/Rpc/rpc-message-queuing)
</dt> <dt>

[Zeichen folgen Bindung](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 