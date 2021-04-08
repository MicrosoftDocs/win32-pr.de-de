---
title: Close-Session
description: Verwenden Sie das Close-Session Paket, um dem BITS-Server mitzuteilen, dass der Datei Upload abgeschlossen ist, und um die Sitzung zu beenden.
ms.assetid: 9d4b658a-8b41-4678-b996-f2174784cdd6
keywords:
- Close-Session Bits
topic_type:
- apiref
api_name:
- Close-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fe791ba4706689fd23dea8886f5b8f54f135841
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857128"
---
# <a name="close-session"></a>Close-Session

Verwenden Sie das **Close-Session-** Paket, um dem BITS-Server mitzuteilen, dass der Datei Upload abgeschlossen ist, und um die Sitzung zu beenden.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Close-Session
BITS-Session-Id: {guid}
```

## <a name="headers"></a>Header

<dl> <dt>

<span id="BITS_POST"></span><span id="bits_post"></span>Bits- \_ Post
</dt> <dd>

Bits-spezifisches Verb, das dieses Paket für den BITS-Server identifiziert.

Ersetzen Sie Remote-URL durch den absoluten oder relativen URI. Ersetzen Sie in der Regel Remote-URL durch den Remote Dateinamen des Auftrags. Überlegungen zum Netzwerk Lastenausgleich finden Sie im "Bits-Host-ID"-Header im Paket " [**Create-Session**](create-session.md) ".

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>Bits-Pakettyp
</dt> <dd>

Identifiziert dieses Anforderungspaket als Close-Session Paket.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>Bits-Session-ID
</dt> <dd>

Zeichen folgen-GUID, die die Sitzung mit dem Server identifiziert. Ersetzen Sie {GUID} durch die Sitzungs-ID, die der Server in der Bestätigung für das Antwortpaket " [**Create-Session**](ack-for-create-session.md) " zurückgibt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der BITS-Server gibt alle Ressourcen frei und löscht beim Empfang dieses Pakets alle temporären Dateien.

Für Upload-Antwort-Aufträge müssen Sie die Antwort vor dem Senden der **Close-Session** herunterladen. Andernfalls geht die Antwort verloren.

Wenn Sie dieses Paket vor dem Hochladen aller Fragmente senden, wird die Uploaddatei gelöscht. eine partielle Datei kann nicht hochgeladen werden.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Bestätigung für Close-Session**](ack-for-close-session.md)
</dt> <dt>

[**Abbrechen-Sitzung**](cancel-session.md)
</dt> <dt>

[**Create-Session**](create-session.md)
</dt> </dl>

 

 




