---
title: Cancel-Session
description: Verwenden Sie das Cancel-Session Paket, um die Uploadsitzung mit dem BITS-Server zu beenden.
ms.assetid: 670d061e-ab73-4aa8-85ba-2c9693794235
keywords:
- Cancel-Session Bits
topic_type:
- apiref
api_name:
- Cancel-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 017097bea656309aabf3d773f34152805fd6a579
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106338630"
---
# <a name="cancel-session"></a>Cancel-Session

Verwenden Sie das **Cancel-Session-** Paket, um die Uploadsitzung mit dem BITS-Server zu beenden.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Cancel-Session
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

Identifiziert dieses Anforderungspaket als Cancel-Session Paket.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>Bits-Session-ID
</dt> <dd>

Zeichen folgen-GUID, die die Sitzung mit dem Server identifiziert. Ersetzen Sie {GUID} durch die Sitzungs-ID, die der Server in der Bestätigung für das Antwortpaket " [**Create-Session**](ack-for-create-session.md) " zurückgibt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Dieses Paket bricht einen Uploadauftrag ab, wenn er vor dem Senden des letzten Fragments gesendet wird. Cancel-Session hat keine Auswirkung auf eine Datei, deren letztes Fragment bereits gesendet wurde. Wenn der BITS-Server das letzte Fragment empfängt, schreibt er die Datei in das endgültige Ziel und stellt die Datei im Falle einer Upload-Antwort an die Serveranwendung an. Beim Upload-Reply-Fall bricht das Cancel-Session Paket den Antwort Teil eines Upload-Antwort-Auftrags ab.

Der BITS-Server gibt alle Ressourcen frei und löscht beim Empfang dieses Pakets alle temporären Dateien.

Der BITS-Client sendet dieses Paket, wenn der Benutzer den Auftrag abbricht.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Bestätigung für Create-Session**](ack-for-create-session.md)
</dt> <dt>

[**Sitzung schließen**](close-session.md)
</dt> </dl>

 

 




