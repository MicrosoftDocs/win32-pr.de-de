---
title: Ack für Fragment
description: Verwenden Sie das Paket "Ack for Fragment", um die Fragmentanforderung des Clients zu bestätigen.
ms.assetid: f5466489-2d5e-4850-a39c-37bc4923a7ac
keywords:
- Ack für Fragment-BITS
topic_type:
- apiref
api_name:
- Ack for Fragment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecd4b8bf5580a5724c689ced1886051006d34cd3c9ba0561d253f36428178c0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702120"
---
# <a name="ack-for-fragment"></a>Ack für Fragment

Verwenden Sie das **Paket "Ack for Fragment",** um die [**Fragmentanforderung**](fragment.md) des Clients zu bestätigen.

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
BITS-Session-Id: {guid}
BITS-Received-Content-Range: range
BITS-Reply-URL: url
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a>Header

<dl> <dt>

<span id="reason-code"></span><span id="REASON-CODE"></span>reason-code
</dt> <dd>

Ersetzen Sie reason-code durch einen HTTP-Ursachencode. Die folgende Tabelle zeigt die typischen Ursachencodes für eine Antwort auf eine [**Fragmentanforderung.**](fragment.md) Eine Liste der HTTP-Ursachencodes finden Sie unter [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).



| Ursachencode    | BESCHREIBUNG                                                                                                            |
|----------------|------------------------------------------------------------------------------------------------------------------------|
| 200<br/> | OK. Die Anforderung wurde erfolgreich gesendet.<br/>                                                                             |
| 416<br/> | Range-Not-Satisfiable. Der Client hat ein Fragment gesendet, dessen Bereich nicht mit dem vorherigen Fragment verbunden ist.<br/> |



 

</dd> <dt>

<span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>Ursachenbeschreibung
</dt> <dd>

Ersetzen Sie reason-description durch die HTTP-Beschreibung, die dem Ursachencode zugeordnet ist. Legen Sie beispielsweise reason-description auf OK fest, wenn reason-code 200 ist.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type
</dt> <dd>

Identifiziert dieses Antwortpaket als Ack-Paket.

</dd> <dt>

<span id="BITS-Received-Content-Range"></span><span id="bits-received-content-range"></span><span id="BITS-RECEIVED-CONTENT-RANGE"></span>BITS-Received-Content-Range
</dt> <dd>

Nullbasierter Offset zum nächsten Byte, das der Server vom Client erwartet. Wenn das Fragment beispielsweise den Bereich 128 212 enthält, würden Sie den Bereich auf 213 festlegen.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Sitzungs-ID
</dt> <dd>

Zeichenfolgen-GUID, die die Sitzung für den Client identifiziert. Ersetzen Sie {guid} durch den Sitzungsbezeichner, den der Client im [**Fragmentanforderungspaket**](fragment.md) gesendet hat. Wenn Sie den Sitzungsbezeichner nicht erkennen, legen Sie den HEADER BITS-Error-Code auf BG \_ E SESSION NOT FOUND \_ \_ \_ fest.

</dd> <dt>

<span id="BITS-Reply-URL"></span><span id="bits-reply-url"></span><span id="BITS-REPLY-URL"></span>BITS-Reply-URL
</dt> <dd>

Enthält die URL zu den Antwortdaten eines Upload-Antwort-Auftrags. Fügen Sie diesen Header in die endgültige Fragmentantwort ein, nachdem der Upload abgeschlossen ist, und Sie erhalten ggf. eine Antwort von der Serveranwendung.

Verwenden Sie den Content-Range-Header aus der Fragmentanforderung, um zu bestimmen, ob der Upload abgeschlossen ist. Der Upload ist abgeschlossen, wenn der Endoffset des Bereichswerts gleich dem Gesamtlängenwert minus 1 ist.

Der BITS-Server sendet die Uploaddatei an die Serveranwendung, nachdem festgestellt wurde, dass der Upload abgeschlossen ist. Die Serveranwendung verarbeitet die Datei und generiert die Antwort. Der BITS-Server legt den Wert von BITS-Reply-URL auf die URL der Antwortdatei aus der Serveranwendung fest.

</dd> <dt>

<span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Inhaltslänge
</dt> <dd>

Ersetzen Sie length durch die Anzahl der Bytes, die im Text der Antwort enthalten sind. Content-Length ist erforderlich, auch wenn der Text der Antwort keinen Inhalt enthält.

</dd> <dt>

<span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code
</dt> <dd>

Ersetzen Sie den Fehlercode durch eine Hexadezimalzahl, die einen HRESULT-Wert darstellt, der einem serverseitigen Fehler zugeordnet ist. Schließen Sie diesen Header nur ein, wenn reason-code nicht 200 oder 201 ist.

</dd> <dt>

<span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-Context
</dt> <dd>

Ersetzen Sie error-context durch eine Hexadezimalzahl, die den Kontext darstellt, in dem der Fehler aufgetreten ist. Geben Sie die Hexadezimalzahl für [**BG ERROR CONTEXT REMOTE \_ \_ \_ \_ FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) an, wenn der Server den Fehler generiert hat. Geben Sie andernfalls die Hexadezimalzahl für **BG ERROR CONTEXT REMOTE \_ \_ \_ \_ APPLICATION** (0x7) an, wenn der Fehler von der Anwendung generiert wurde, an die die Uploaddatei übergeben wird. Schließen Sie diesen Header nur ein, wenn der Reason-Code nicht 200 oder 201 ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn die Sitzung für einen Upload-Antwort-Auftrag vorgesehen ist, kann es zu einer Verzögerung kommen, bevor der Client die endgültige **Ack for Fragment-Antwort** empfängt. Die Dauer der Verzögerung hängt von der Zeitspanne ab, die die Serveranwendung (Anwendung, an die der Server die Uploaddatei sendet) benötigt, um die Antwort zu generieren.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Create-Session**](create-session.md)
</dt> <dt>

[**Fragment**](fragment.md)
</dt> </dl>

 

 





