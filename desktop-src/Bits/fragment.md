---
title: Fragment
description: Verwenden Sie das Fragmentpaket, um ein Fragment der Uploaddatei an den Server zu senden.
ms.assetid: d6df7e47-a240-4be2-a9c4-24a13e622861
keywords:
- Fragment-BITS
topic_type:
- apiref
api_name:
- Fragment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 613acaabc017b9e673d2cba6a64f84db054a4cdc0d73a0639fcf8455edff8298
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528830"
---
# <a name="fragment"></a>Fragment

Verwenden Sie das **Fragmentpaket,** um ein Fragment der Uploaddatei an den Server zu senden.

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

<span id="BITS_POST"></span><span id="bits_post"></span>BITS \_ POST
</dt> <dd>

BITS-spezifisches Verb, das dieses Paket an den BITS-Server identifiziert.

Ersetzen Sie remote-URL durch den absoluten oder relativen URI. Ersetzen Sie remote-URL in der Regel durch den Remotedateinamen des Auftrags. Überlegungen zum Netzwerklastenausgleich finden Sie im Bits-Host-Id-Header im [**Create-Session-Paket.**](create-session.md)

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type
</dt> <dd>

Identifiziert dieses Anforderungspaket als Fragmentpaket.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Sitzungs-ID
</dt> <dd>

Zeichenfolgen-GUID, die die Sitzung mit dem Server identifiziert. Ersetzen Sie {guid} durch den Sitzungsbezeichner, den der Server im [**Antwortpaket Ack for Create-Session**](ack-for-create-session.md) zurückgibt.

</dd> <dt>

<span id="Content-Name"></span><span id="content-name"></span><span id="CONTENT-NAME"></span>Content-Name
</dt> <dd>

Geben Sie diesen Header nur mit dem ursprünglichen Fragment an. Ersetzen Sie filename durch den Namen des lokalen Dateinamens aus dem Auftrag. Der Name enthält nicht den Pfad.

</dd> <dt>

<span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Inhaltslänge
</dt> <dd>

Ersetzen Sie length durch die Anzahl der im Fragmenttext gesendeten Bytes.

</dd> <dt>

<span id="Content-Range"></span><span id="content-range"></span><span id="CONTENT-RANGE"></span>Inhaltsbereich
</dt> <dd>

Teilt dem Server mit, wo der Bereich in der Zieldatei angewendet werden soll. Ersetzen Sie range durch die Start- und Endoffsets des Bereichs in der Zieldatei. Die Offsets sind nullbasiert. Wenn der angegebene Bereich einen vorhandenen Bereich überlappt, schreibt BITS nur den nicht überlappenden Teil des Bereichs. BITS überschreibt keinen vorhandenen Inhalt. Wenn das erste Paket beispielsweise den Bereich 0 bis 100 und das zweite Paket den Bereich 50 bis 150 enthielt, schreibt BITS nur Bytes von 101 bis 150 aus dem zweiten Paket. Ersetzen Sie total-length durch die Gesamtzahl der Bytes in der Datei.

</dd> <dt>

<span id="Content-Encoding"></span><span id="content-encoding"></span><span id="CONTENT-ENCODING"></span>Inhaltscodierung
</dt> <dd>

Ersetzen Sie die Codierung durch den Codierungstyp, den der Client für das Fragment verwendet. Der Client muss die Codierung verwenden, die der Server im Accept-Encoding Header des [**Antwortpakets "Ack for Create-Session"**](ack-for-create-session.md) identifiziert. Der Server verwendet den Codierungstyp, um das Fragment zu decodieren. Alle Fragmente müssen dieselbe Codierung angeben.

Senden Sie diesen Header nicht, wenn der Codierungstyp Identity lautet. Der BITS-Server unterstützt nur die Identitätscodierung.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das Fragment ist ein Bytebereich, der im Text des Pakets gesendet wird. Der Client sendet die Fragmente in sequenzieller Reihenfolge, beginnend mit Offset 0 (null). Der Server verfolgt nicht zusammenhängende Bereiche nicht nach. Wenn der Client nicht zusammenhängende Bereiche sendet, gibt der Server einen HTTP 416-Rückgabecode (range-not-satisfiable) in der Antwort [**"Ack for Fragment"**](ack-for-fragment.md) zurück.

Die *Content-xxxx-Header* sind HTTP 1.1-Standardheader. Weitere Informationen zu den *Content-xxxx-Headern* finden Sie in der [RFC 2616-Spezifikation.](https://www.ietf.org/rfc/rfc2616.txt)

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ack für Fragment**](ack-for-fragment.md)
</dt> <dt>

[**Sitzung schließen**](close-session.md)
</dt> <dt>

[**Create-Session**](create-session.md)
</dt> </dl>

 

 




