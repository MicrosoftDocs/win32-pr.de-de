---
title: Create-Session
description: Verwenden Sie das Create-Session Paket, um eine Uploadsitzung mit dem BITS-Server anzufordern.
ms.assetid: eeb8ff83-2a7f-4fef-9df7-8c12febfcf36
keywords:
- Create-Session BITS
topic_type:
- apiref
api_name:
- Create-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 639db08c5a29b09f5c32d7b0243de66f2c4dced001a1ff2afa7e74837c8d67e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021188"
---
# <a name="create-session"></a>Create-Session

Verwenden Sie das **Paket Create-Session,** um eine Uploadsitzung mit dem BITS-Server anzufordern.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Create-Session
BITS-Supported-Protocols: {guid1} ... {guidN}
```

## <a name="headers"></a>Header

<dl> <dt>

<span id="BITS_POST"></span><span id="bits_post"></span>BITS \_ POST
</dt> <dd>

BITS-spezifisches Verb, das dieses Paket an den BITS-Server identifiziert.

Ersetzen Sie remote-URL durch den absoluten oder relativen URI. Ersetzen Sie in der Regel remote-URL durch den Remotedateinamen des Auftrags. Überlegungen zum Netzwerklastenausgleich finden Sie im Header BITS-Host-Id.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type
</dt> <dd>

Identifiziert dieses Anforderungspaket als Create-Session Paket.

</dd> <dt>

<span id="BITS-Supported-Protocols"></span><span id="bits-supported-protocols"></span><span id="BITS-SUPPORTED-PROTOCOLS"></span>BITS-supported-protocols
</dt> <dd>

Durch Leerzeichen getrennte Liste der Protokolle, die der Client unterstützt. Verwenden Sie Zeichenfolgen-GUIDs, um die Protokolle zu identifizieren. Geben Sie die Liste in der Reihenfolge der Präferenz von den meisten bis zu den am wenigsten bevorzugten an. In der folgenden Tabelle ist das Protokoll aufgeführt, das der BITS-Client unterstützt. Ersetzen Sie {guid1} ... {guidN} mit mindestens einer Zeichenfolgen-GUIDs aus der Liste.



| Protokoll                                          | BESCHREIBUNG                         |
|---------------------------------------------------|-------------------------------------|
| {7df0354d-249b-430f-820d-3d2a9bef4931}<br/> | BITS 1.5 Hochladen Protocol<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Hinweise

Sie sollten ein [**Ping-Paket**](ping.md) senden, um eine HTTP-Verbindung herzustellen, bevor Sie das Create-Session Paket senden. Das Create-Session Paket kann auch die Verbindung herstellen. die Create-Session Pakets ist jedoch weniger effizient.

Der Server wählt das Protokoll aus der Liste aus, die der Client im Header BITS-Supported-Protocols bereitstellt. Der Server gibt das ausgewählte Protokoll im BITS-Protocol-Header des [**Antwortpakets "Ack for Create-Session"**](ack-for-create-session.md) zurück.

Der Client erwartet, dass der Server ein Antwortpaket vom Typ [**"Ack" für "Create-Session"**](ack-for-create-session.md) zurückgibt. Wenn der Server eine Sitzung einrichten konnte, verwendet der Client das [**Fragmentanforderungspaket,**](fragment.md) um Bereiche der Datei an den Server zu senden.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ack für Create-Session**](ack-for-create-session.md)
</dt> <dt>

[**Fragment**](fragment.md)
</dt> <dt>

[**Pingen**](ping.md)
</dt> </dl>

 

 





