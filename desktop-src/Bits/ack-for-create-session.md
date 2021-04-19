---
title: Bestätigung für Create-Session
description: Verwenden Sie die Bestätigung für Create-Session Paket, um die Create-Session Anforderung des Clients zu bestätigen.
ms.assetid: eeb8ff83-2a7f-4fef-9df7-8c12febfcf36
keywords:
- Bestätigung für Create-Session Bits
topic_type:
- apiref
api_name:
- Ack for Create-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d978ec4c5693a5087734975c412b999ed7d5890
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "106339524"
---
# <a name="ack-for-create-session"></a>Bestätigung für Create-Session

Verwenden Sie das Paket " **ACK for Create-Session** ", um die Anforderung zum [**Erstellen einer Sitzung**](create-session.md) zu bestätigen.

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
BITS-Protocol: {guid}
BITS-Session-Id: {guid}
BITS-Host-Id: PublicHostName
BITS-Host-Id-Fallback-Timeout: Timeout
Accept-Encoding: Identity
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a>Header

<dl> <dt>

<span id="reason-code"></span><span id="REASON-CODE"></span>Grund: Code
</dt> <dd>

Ersetzen Sie Reason-Code durch den HTTP-Ursachen Code. In der folgenden Tabelle werden die typischen Ursachen Codes für eine Antwort auf eine Anforderung zum [**Erstellen einer Sitzung**](create-session.md) angezeigt. Eine Liste der http-Ursachen Codes finden Sie unter [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).



| Ursachencode    | BESCHREIBUNG                                                                         |
|----------------|-------------------------------------------------------------------------------------|
| 200<br/> | OK. Die Anforderung wurde erfolgreich gesendet.<br/>                                          |
| 201<br/> | Erstellt. Die Sitzung wurde erstellt.<br/>                                        |
| 403<br/> | Unzulässig. Der Benutzer darf keine Dateien in die angegebene URL hochladen.<br/> |
| 404<br/> | Nicht gefunden. Die angegebene URL ist nicht vorhanden.<br/>                             |
| 409<br/> | Konflikt. Die Datei ist auf dem Server vorhanden und kann nicht überschrieben werden.<br/>       |



 

</dd> <dt>

<span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>Ursache: Beschreibung
</dt> <dd>

Ersetzen Sie Reason-Description durch die http-Beschreibung, die dem Ursachen Code zugeordnet ist. Legen Sie beispielsweise Reason-Description auf OK fest, wenn der Grund Code 200 ist.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>Bits-Pakettyp
</dt> <dd>

Identifiziert dieses Antwortpaket als ACK-Paket.

</dd> <dt>

<span id="BITS-Protocol"></span><span id="bits-protocol"></span><span id="BITS-PROTOCOL"></span>BITS-Protokoll
</dt> <dd>

Zeichen folgen-GUID, die das Protokoll identifiziert, das der Server für diese Sitzung verwenden möchte. Ersetzen Sie {GUID} durch die Protokoll-ID aus der Liste der Protokolle, die der Client in der [**Create-Session-**](create-session.md) Anforderung enthält. der Bits-supported-Protocol-Header enthält die Liste. Fügen Sie diesen Header nur ein, wenn der Grund Code 200 oder 201 ist.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>Bits-Session-ID
</dt> <dd>

Zeichen folgen-GUID, die diese Sitzung für den Client identifiziert. Ersetzen Sie {GUID} durch die Sitzungs-ID, die der Client in allen nachfolgenden Anforderungs Paketen sendet.

Bits verwendet eine GUID zum Identifizieren der Sitzung, Sie können jedoch jede beliebige http-Zeichenfolge mit bis zu 100 Zeichen verwenden.

</dd> <dt>

<span id="BITS-Host-Id"></span><span id="bits-host-id"></span><span id="BITS-HOST-ID"></span>Bits-Host-ID
</dt> <dd>

Dies ist optional. Fügen Sie diesen Header nur ein, wenn die [BITS-IIS-Erweiterungs Eigenschaft](bits-iis-extension-properties.md), bitshostid, festgelegt ist. Ersetzen Sie publichostname durch den Servernamen oder die IP-Adresse aus der bitshostid-Eigenschaft.

Der Client muss den Serverteil der Remote-URL für alle nachfolgenden Pakete ersetzen. Wenn der Client diesen Hostnamen für nachfolgende Pakete nicht angibt, wird der Auftrag möglicherweise erneut auf einem anderen Server in der Farm gestartet, wobei eine partielle Uploaddatei auf dem vorherigen Server belassen wird.

</dd> <dt>

<span id="BITS-Host-Id-Fallback-Timeout"></span><span id="bits-host-id-fallback-timeout"></span><span id="BITS-HOST-ID-FALLBACK-TIMEOUT"></span>Bits-Host-ID-Fallback-Timeout
</dt> <dd>

Dies ist optional. Fügen Sie diesen Header nur ein, wenn der Bits-Host-ID-Header angegeben ist. Ersetzen Sie Timeout durch den Timeout Wert aus der bitshostidfallbacktimeout-Eigenschaft. Die bitshostidfallbacktimeout-Eigenschaft ist eine der [BITS-IIS-Erweiterungs Eigenschaften](bits-iis-extension-properties.md).

Der Client verwendet den Timeout Zeitraum, um zu bestimmen, wie lange versucht wird, erneut eine Verbindung mit dem im Bits-Host-ID-Header angegebenen Servernamen herzustellen, bevor auf den Hostnamen zurückgegriffen wird, der im Remote Dateinamen des Auftrags angegeben ist. Der Timer beginnt, wenn Bits keine Verbindung mit dem Bits-Host-ID-Server herstellen kann. Der Zeitgeber wird zurückgesetzt, wenn eine Verbindung mit dem Server wieder hergestellt wird. Wenn kein Timeout Wert angegeben wird, wird der im Remote Dateinamen angegebene Hostname nie vom Client wieder hergestellt.

</dd> <dt>

<span id="Accept-Encoding"></span><span id="accept-encoding"></span><span id="ACCEPT-ENCODING"></span>Accept-Encoding
</dt> <dd>

Identifiziert das Codierungsschema, das in den an den Server gesendeten Fragmenten verwendet werden soll. Das fragmentpaket enthält das codierte Fragment im Text des Pakets. Der BITS-Server erfordert die Identitäts Codierung (Klartext). Fügen Sie diesen Header nur ein, wenn der Grund Code 200 oder 201 ist.

</dd> <dt>

<span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Inhalts Länge
</dt> <dd>

Ersetzen Sie length durch die Anzahl der Bytes, die im Text der Antwort enthalten sind. Erforderlich, auch wenn der Text der Antwort keinen Inhalt enthält.

</dd> <dt>

<span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>Bits-Fehler Code
</dt> <dd>

Ersetzen Sie Error-Code durch eine hexadezimale Zahl, die einen HRESULT-Wert darstellt, der einem serverseitigen Fehler zugeordnet ist. Fügen Sie diesen Header nur ein, wenn Reason-Code nicht 200 oder 201 ist.

</dd> <dt>

<span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>Bits-Fehler-Kontext
</dt> <dd>

Ersetzen Sie Error-Context durch eine hexadezimale Zahl, die den Kontext darstellt, in dem der Fehler aufgetreten ist. Geben Sie die hexadezimale Zahl der [**\_ \_ \_ Remote \_ Datei des BG-Fehler Kontexts**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) an, wenn der Server den Fehler generiert hat. Andernfalls geben Sie die hexadezimale Zahl für eine **BG- \_ Fehler \_ Kontext- \_ Remote \_ Anwendung** (0x7) an, wenn der Fehler von der Anwendung generiert wurde, an die die Uploaddatei weitergeleitet wird. Fügen Sie diesen Header nur ein, wenn der Grund Code nicht 200 oder 201 ist.

</dd> </dl>

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Create-Session**](create-session.md)
</dt> </dl>

 

 





