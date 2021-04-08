---
title: Bestätigung für Fragment
description: Verwenden Sie das ACK for Fragment-Paket, um die fragmentanforderung des Clients zu bestätigen.
ms.assetid: f5466489-2d5e-4850-a39c-37bc4923a7ac
keywords:
- Bestätigung für fragmentbits
topic_type:
- apiref
api_name:
- Ack for Fragment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef28381313ce00fd6089ebf845ed342ccae455c7
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "103949207"
---
# <a name="ack-for-fragment"></a>Bestätigung für Fragment

Verwenden Sie das **ACK for Fragment** -Paket, um die [**fragmentanforderung**](fragment.md) des Clients zu bestätigen.

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

<span id="reason-code"></span><span id="REASON-CODE"></span>Grund: Code
</dt> <dd>

Ersetzen Sie Reason-Code durch einen HTTP-Ursachen Code. In der folgenden Tabelle sind die typischen Ursachen Codes für eine Antwort auf eine [**fragmentanforderung**](fragment.md) aufgeführt. Eine Liste der http-Ursachen Codes finden Sie unter [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).



| Ursachencode    | BESCHREIBUNG                                                                                                            |
|----------------|------------------------------------------------------------------------------------------------------------------------|
| 200<br/> | OK. Die Anforderung wurde erfolgreich gesendet.<br/>                                                                             |
| 416<br/> | Bereich-nicht-befriedbar. Der Client hat ein Fragment gesendet, dessen Bereich nicht zusammenhängend mit dem vorherigen Fragment ist.<br/> |



 

</dd> <dt>

<span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>Ursache: Beschreibung
</dt> <dd>

Ersetzen Sie Reason-Description durch die http-Beschreibung, die dem Ursachen Code zugeordnet ist. Legen Sie beispielsweise Reason-Description auf OK fest, wenn der Grund Code 200 ist.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>Bits-Pakettyp
</dt> <dd>

Identifiziert dieses Antwortpaket als ACK-Paket.

</dd> <dt>

<span id="BITS-Received-Content-Range"></span><span id="bits-received-content-range"></span><span id="BITS-RECEIVED-CONTENT-RANGE"></span>Bits-empfangen-Content-Range
</dt> <dd>

NULL basierter Offset zum nächsten Byte, den der Server vom Client erwartet. Wenn das Fragment z. b. den Bereich 128 212 enthielt, legen Sie Bereich auf 213 fest.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>Bits-Session-ID
</dt> <dd>

Zeichen folgen-GUID, die die Sitzung für den Client identifiziert. Ersetzen Sie {GUID} durch den Sitzungs Bezeichner, den der Client im [**fragmentanforderungs**](fragment.md) Paket gesendet hat. Wenn Sie die Sitzungs-ID nicht erkennen, legen Sie den Bits-Error-Code-Header auf BG \_ E \_ Session \_ nicht \_ gefunden fest.

</dd> <dt>

<span id="BITS-Reply-URL"></span><span id="bits-reply-url"></span><span id="BITS-REPLY-URL"></span>Bits-Antwort-URL
</dt> <dd>

Enthält die URL zu den Antwortdaten eines Upload-Antwort-Auftrags. Fügen Sie diesen Header in die endgültige fragmentantwort ein, nachdem der Upload abgeschlossen ist, und Sie erhalten ggf. eine Antwort von der Serveranwendung.

Verwenden Sie den Content-Range-Header aus der fragmentanforderung, um zu bestimmen, ob der Upload fertiggestellt wurde. Der Upload ist abgeschlossen, wenn der Ende Offset des Bereichs Werts dem Wert der Gesamtlänge minus 1 entspricht.

Der BITS-Server sendet die Uploaddatei an die Serveranwendung, nachdem er den Abschluss des Uploads festgelegt hat. Die Serveranwendung verarbeitet die Datei und generiert die Antwort. Der BITS-Server legt den Wert von Bits-Reply-URL auf die URL der Antwortdatei von der Serveranwendung fest.

</dd> <dt>

<span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Inhalts Länge
</dt> <dd>

Ersetzen Sie length durch die Anzahl der Bytes, die im Text der Antwort enthalten sind. Content-length ist erforderlich, auch wenn der Text der Antwort keinen Inhalt enthält.

</dd> <dt>

<span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>Bits-Fehler Code
</dt> <dd>

Ersetzen Sie Error-Code durch eine hexadezimale Zahl, die einen HRESULT-Wert darstellt, der einem serverseitigen Fehler zugeordnet ist. Schließen Sie diesen Header nur ein, wenn Reason-Code nicht 200 oder 201 ist.

</dd> <dt>

<span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>Bits-Fehler-Kontext
</dt> <dd>

Ersetzen Sie Error-Context durch eine hexadezimale Zahl, die den Kontext darstellt, in dem der Fehler aufgetreten ist. Geben Sie die hexadezimale Zahl der [**\_ \_ \_ Remote \_ Datei des BG-Fehler Kontexts**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) an, wenn der Server den Fehler generiert hat. Andernfalls geben Sie die hexadezimale Zahl für eine **BG- \_ Fehler \_ Kontext- \_ Remote \_ Anwendung** (0x7) an, wenn der Fehler von der Anwendung generiert wurde, an die die Uploaddatei weitergeleitet wird. Fügen Sie diesen Header nur ein, wenn der Grund Code nicht 200 oder 201 ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn die Sitzung für einen Upload-Antwort-Auftrag gilt, kann es zu einer Verzögerung kommen, bevor der Client die endgültige Bestätigung **für die fragmentantwort** erhält. Die Länge der Verzögerung hängt von der Zeitspanne ab, die die Serveranwendung (auf die der Server die Uploaddatei sendet) benötigt, um die Antwort zu generieren.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Create-Session**](create-session.md)
</dt> <dt>

[**Fragment**](fragment.md)
</dt> </dl>

 

 





