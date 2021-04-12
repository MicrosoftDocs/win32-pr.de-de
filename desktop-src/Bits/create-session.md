---
title: Create-Session
description: Verwenden Sie das Create-Session Paket, um eine Uploadsitzung mit dem BITS-Server anzufordern.
ms.assetid: eeb8ff83-2a7f-4fef-9df7-8c12febfcf36
keywords:
- Create-Session Bits
topic_type:
- apiref
api_name:
- Create-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 425ad3bd36305f94547cf2cd8b13c1a420491499
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104471860"
---
# <a name="create-session"></a>Create-Session

Verwenden Sie das Paket " **Create-Session** ", um eine Uploadsitzung mit dem BITS-Server anzufordern.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Create-Session
BITS-Supported-Protocols: {guid1} ... {guidN}
```

## <a name="headers"></a>Header

<dl> <dt>

<span id="BITS_POST"></span><span id="bits_post"></span>Bits- \_ Post
</dt> <dd>

Bits-spezifisches Verb, das dieses Paket für den BITS-Server identifiziert.

Ersetzen Sie Remote-URL durch den absoluten oder relativen URI. Ersetzen Sie in der Regel Remote-URL durch den Remote Dateinamen des Auftrags. Überlegungen zum Netzwerk Lastenausgleich finden Sie unter dem Bits-Host-ID-Header.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>Bits-Pakettyp
</dt> <dd>

Identifiziert dieses Anforderungspaket als Create-Session Paket.

</dd> <dt>

<span id="BITS-Supported-Protocols"></span><span id="bits-supported-protocols"></span><span id="BITS-SUPPORTED-PROTOCOLS"></span>Bits-unterstützte Protokolle
</dt> <dd>

Durch Leerzeichen getrennte Liste der Protokolle, die vom Client unterstützt werden. Verwenden Sie Zeichen folgen-GUIDs, um die Protokolle zu identifizieren. Geben Sie die Liste in der bevorzugten Reihenfolge als die am wenigsten bevorzugte Liste an. In der folgenden Tabelle wird das Protokoll aufgelistet, das vom BITS-Client unterstützt wird. {GUID1} ersetzen... {guidn} mit einer oder mehreren Zeichen folgen-GUIDs aus der Liste.



| Protokoll                                          | BESCHREIBUNG                         |
|---------------------------------------------------|-------------------------------------|
| {7df0354d-249b-430t-820d-3d2a9bef 4931}<br/> | Bits 1,5-uploadprotokoll<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Sie sollten ein [**Ping**](ping.md) -Paket senden, um eine HTTP-Verbindung herzustellen, bevor Sie das Create-Session Paket senden. Das Create-Session Paket kann auch die Verbindung herstellen. Das Create-Session Paket ist jedoch weniger effizient.

Der Server wählt das gewünschte Protokoll aus der Liste aus, die der Client im Header Bits-supported-Protokolls bereitstellt. Der Server gibt das ausgewählte Protokoll im BITS-Protocol-Header der Bestätigung für das Antwortpaket " [**Create-Session**](ack-for-create-session.md) " zurück.

Der Client erwartet, dass der Server eine Bestätigung für das Antwortpaket " [**Create-Session**](ack-for-create-session.md) " zurückgibt. Wenn der Server eine Sitzung einrichten konnte, verwendet der Client das [**fragmentanforderungs**](fragment.md) Paket, um Bereiche der Datei an den Server zu senden.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Bestätigung für Create-Session**](ack-for-create-session.md)
</dt> <dt>

[**Fragment**](fragment.md)
</dt> <dt>

[**Ping**](ping.md)
</dt> </dl>

 

 





