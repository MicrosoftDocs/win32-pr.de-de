---
title: Close-Session
description: Verwenden Sie das Close-Session Paket, um dem BITS-Server mitzuteilen, dass der Dateiupload abgeschlossen ist, und um die Sitzung zu beenden.
ms.assetid: 9d4b658a-8b41-4678-b996-f2174784cdd6
keywords:
- Close-Session BITS
topic_type:
- apiref
api_name:
- Close-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1ae1318a99e690b13f4f0cad03624fb351c359efbcb1be9e105076ce53ceba2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021198"
---
# <a name="close-session"></a>Close-Session

Verwenden Sie das **Paket "Sitzung schließen",** um dem BITS-Server mitzuteilen, dass der Dateiupload abgeschlossen ist, und um die Sitzung zu beenden.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Close-Session
BITS-Session-Id: {guid}
```

## <a name="headers"></a>Header

<dl> <dt>

<span id="BITS_POST"></span><span id="bits_post"></span>BITS \_ POST
</dt> <dd>

BITS-spezifisches Verb, das dieses Paket an den BITS-Server identifiziert.

Ersetzen Sie remote-URL durch den absoluten oder relativen URI. Ersetzen Sie in der Regel remote-URL durch den Remotedateinamen des Auftrags. Überlegungen zum Netzwerklastenausgleich finden Sie im Bits-Host-Id-Header im [**Create-Session-Paket.**](create-session.md)

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type
</dt> <dd>

Identifiziert dieses Anforderungspaket als Close-Session Paket.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Sitzungs-ID
</dt> <dd>

Zeichenfolgen-GUID, die die Sitzung mit dem Server identifiziert. Ersetzen Sie {guid} durch den Sitzungsbezeichner, den der Server im [**Antwortpaket Ack for Create-Session**](ack-for-create-session.md) zurückgibt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der BITS-Server gibt alle Ressourcen frei und löscht alle temporären Dateien, wenn er dieses Paket empfängt.

Bei Upload-Antwort-Aufträgen müssen Sie die Antwort herunterladen, bevor Sie **Close-Session** senden. Andernfalls geht die Antwort verloren.

Wenn Sie dieses Paket senden, bevor Sie alle Fragmente hochladen, wird die Uploaddatei gelöscht. Sie können keine Teildatei hochladen.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Ack for Close-Session**](ack-for-close-session.md)
</dt> <dt>

[**Cancel-Session**](cancel-session.md)
</dt> <dt>

[**Create-Session**](create-session.md)
</dt> </dl>

 

 




