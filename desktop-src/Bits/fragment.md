---
title: Fragment
description: Verwenden Sie das Fragment-Paket, um ein Fragment der Uploaddatei an den Server zu senden.
ms.assetid: d6df7e47-a240-4be2-a9c4-24a13e622861
keywords:
- Fragmentbits
topic_type:
- apiref
api_name:
- Fragment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f5103e90ec84a20ff4c04d9036a744919d9b1fd
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104101282"
---
# <a name="fragment"></a>Fragment

Verwenden Sie das **Fragment** -Paket, um ein Fragment der Uploaddatei an den Server zu senden.

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Fragment
BITS-Session-Id: {guid}
Content-Name: filename
Content-Length: length
Content-Range: Bytes range/total-length
Content-Encoding: encoding
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

Identifiziert dieses Anforderungspaket als fragmentpaket.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>Bits-Session-ID
</dt> <dd>

Zeichen folgen-GUID, die die Sitzung mit dem Server identifiziert. Ersetzen Sie {GUID} durch die Sitzungs-ID, die der Server in der Bestätigung für das Antwortpaket " [**Create-Session**](ack-for-create-session.md) " zurückgibt.

</dd> <dt>

<span id="Content-Name"></span><span id="content-name"></span><span id="CONTENT-NAME"></span>Inhalts Name
</dt> <dd>

Geben Sie diesen Header nur mit dem anfänglichen Fragment an. Ersetzen Sie filename durch den Namen des lokalen Datei namens aus dem Auftrag. Der Name enthält nicht den Pfad.

</dd> <dt>

<span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Inhalts Länge
</dt> <dd>

Ersetzen Sie die Länge durch die Anzahl von Bytes, die im Fragmenttext gesendet werden.

</dd> <dt>

<span id="Content-Range"></span><span id="content-range"></span><span id="CONTENT-RANGE"></span>Inhalts Bereich
</dt> <dd>

Weist den Server an, wo der Bereich in der Zieldatei angewendet werden soll. Ersetzen Sie Range durch die Start-und Endoffsets des Bereichs in der Zieldatei. Die Offsets sind NULL basiert. Wenn der angegebene Bereich einen vorhandenen Bereich überlappt, schreibt Bits nur den nicht überlappenden Bereich des Bereichs. Vorhandene Inhalte werden von Bits nicht überschrieben. Wenn das erste Paket z. b. den Bereich von 0 bis 100 enthielt und das zweite Paket den Bereich 50 bis 150 enthielt, schreibt Bits nur die Bytes 101 über 150 aus dem zweiten Paket. Ersetzen Sie Total-Length durch die Gesamtzahl der Bytes in der Datei.

</dd> <dt>

<span id="Content-Encoding"></span><span id="content-encoding"></span><span id="CONTENT-ENCODING"></span>Inhalts Codierung
</dt> <dd>

Ersetzen Sie Encoding durch den Codierungstyp, den der Client für das Fragment verwendet. Der Client muss die Codierung verwenden, die der Server im Accept-Encoding-Header der Bestätigung für das Antwortpaket [**Create-Session**](ack-for-create-session.md) identifiziert. Der Server verwendet den Codierungstyp zum Decodieren des Fragments. Alle Fragmente müssen dieselbe Codierung angeben.

Senden Sie diesen Header nicht, wenn der Codierungstyp Identity ist. Der BITS-Server unterstützt nur die Identitäts Codierung.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das Fragment ist ein Bereich von Bytes, die im Text des Pakets gesendet werden. Der Client sendet die Fragmente in sequenzieller Reihenfolge, beginnend mit Offset 0; der Server verfolgt nicht zusammenhängende Bereiche nach. Wenn der Client nicht zusammenhängende Bereiche sendet, gibt der Server in der Bestätigung [**für die fragmentantwort**](ack-for-fragment.md) einen HTTP 416-Rückgabecode (Bereichs-nicht-satis-fähig) zurück.

Die Content-*xxxx* -Header sind HTTP 1,1-Standard Header. Weitere Informationen zu den Content-*xxxx* -Headern finden Sie in der Spezifikation von [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt) .

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Bestätigung für Fragment**](ack-for-fragment.md)
</dt> <dt>

[**Sitzung schließen**](close-session.md)
</dt> <dt>

[**Create-Session**](create-session.md)
</dt> </dl>

 

 




