---
title: Cancel-Session
description: Verwenden Sie Cancel-Session Paket, um die Uploadsitzung mit dem BITS-Server zu beenden.
ms.assetid: 670d061e-ab73-4aa8-85ba-2c9693794235
keywords:
- Cancel-Session BITS
topic_type:
- apiref
api_name:
- Cancel-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d570a49d1a5ba632fbbb453b6397338af70d29b0dc837db12193d2889c867eaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835109"
---
# <a name="cancel-session"></a>Cancel-Session

Verwenden Sie **das Paket Cancel-Session,** um die Uploadsitzung mit dem BITS-Server zu beenden.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Cancel-Session
BITS-Session-Id: {guid}
```

## <a name="headers"></a>Header

<dl> <dt>

<span id="BITS_POST"></span><span id="bits_post"></span>BITS \_ POST
</dt> <dd>

BITS-spezifisches Verb, das dieses Paket an den BITS-Server identifiziert.

Ersetzen Sie remote-URL durch den absoluten oder relativen URI. Ersetzen Sie in der Regel remote-URL durch den Remotedateinamen des Auftrags. Überlegungen zum Netzwerklastenausgleich finden Sie im Bits-Host-Id-Header im [**Paket "Create-Session".**](create-session.md)

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type
</dt> <dd>

Identifiziert dieses Anforderungspaket als Cancel-Session Paket.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id
</dt> <dd>

Zeichenfolgen-GUID, die die Sitzung mit dem Server identifiziert. Ersetzen Sie {guid} durch den Sitzungsbezeichner, den der Server im [**Antwortpaket Ack for Create-Session**](ack-for-create-session.md) zurückgibt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Dieses Paket bricht einen Uploadauftrag ab, wenn er gesendet wird, bevor das letzte Fragment gesendet wird. Cancel-Session hat keine Auswirkungen auf eine Datei, deren letztes Fragment bereits gesendet wurde. Wenn der BITS-Server das letzte Fragment empfängt, schreibt er die Datei in das endgültige Ziel und sendet die Datei im Fall einer Upload-Antwort an die Serveranwendung. Im Upload-Antwort-Fall bricht das Cancel-Session den Antwortteil eines Upload-Antwort-Auftrags ab.

Der BITS-Server gibt alle Ressourcen frei und löscht alle temporären Dateien, wenn er dieses Paket empfängt.

Der BITS-Client sendet dieses Paket, wenn der Benutzer den Auftrag abbricht.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Ack for Create-Session**](ack-for-create-session.md)
</dt> <dt>

[**Close-Session**](close-session.md)
</dt> </dl>

 

 




