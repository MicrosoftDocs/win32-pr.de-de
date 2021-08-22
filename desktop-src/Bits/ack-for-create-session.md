---
title: Ack für Create-Session
description: Verwenden Sie Ack für Create-Session Paket, um die Create-Session Anforderung des Clients zu bestätigen.
ms.assetid: eeb8ff83-2a7f-4fef-9df7-8c12febfcf36
keywords:
- Ack für Create-Session BITS
topic_type:
- apiref
api_name:
- Ack for Create-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9dbfcaeab897d55064fe11a506cefbc9d85dd6852a32d279133e6fe7a33a692
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588800"
---
# <a name="ack-for-create-session"></a>Ack für Create-Session

Verwenden Sie den **Ack für das Create-Session-Paket,** um die [**Create-Session-Anforderung**](create-session.md) des Clients zu bestätigen.

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

<span id="reason-code"></span><span id="REASON-CODE"></span>reason-code
</dt> <dd>

Ersetzen Sie reason-code durch den HTTP-Ursachencode. Die folgende Tabelle zeigt die typischen Ursachencodes für eine Antwort auf eine [**Create-Session-Anforderung.**](create-session.md) Eine Liste der HTTP-Ursachencodes finden Sie unter [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).



| Ursachencode    | BESCHREIBUNG                                                                         |
|----------------|-------------------------------------------------------------------------------------|
| 200<br/> | OK. Die Anforderung wurde erfolgreich gesendet.<br/>                                          |
| 201<br/> | Erstellt. Die Sitzung wurde erstellt.<br/>                                        |
| 403<br/> | Unzulässig. Der Benutzer darf keine Dateien in die angegebene URL hochladen.<br/> |
| 404<br/> | Nicht gefunden. Die angegebene URL ist nicht vorhanden.<br/>                             |
| 409<br/> | Konflikt. Die Datei ist auf dem Server vorhanden und kann nicht überschrieben werden.<br/>       |



 

</dd> <dt>

<span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>reason-description
</dt> <dd>

Ersetzen Sie reason-description durch die HTTP-Beschreibung, die dem Ursachencode zugeordnet ist. Legen Sie beispielsweise reason-description auf OK fest, wenn reason-code 200 ist.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type
</dt> <dd>

Identifiziert dieses Antwortpaket als Ack-Paket.

</dd> <dt>

<span id="BITS-Protocol"></span><span id="bits-protocol"></span><span id="BITS-PROTOCOL"></span>BITS-Protokoll
</dt> <dd>

Zeichenfolgen-GUID, die das Protokoll identifiziert, das der Server für diese Sitzung verwenden möchte. Ersetzen Sie {guid} durch den Protokollbezeichner aus der Liste der Protokolle, die der Client in die [**Create-Session-Anforderung**](create-session.md) einschließt. Der BITS-Supported-Protocol-Header enthält die Liste. Schließen Sie diesen Header nur ein, wenn der Reason-Code 200 oder 201 ist.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Sitzungs-ID
</dt> <dd>

Zeichenfolgen-GUID, die diese Sitzung für den Client identifiziert. Ersetzen Sie {guid} durch den Sitzungsbezeichner, den der Client in allen nachfolgenden Anforderungspaketen sendet.

BITS verwendet eine GUID, um die Sitzung zu identifizieren. Sie können jedoch eine beliebige http-rechtliche Zeichenfolge mit bis zu 100 Zeichen verwenden.

</dd> <dt>

<span id="BITS-Host-Id"></span><span id="bits-host-id"></span><span id="BITS-HOST-ID"></span>BITS-Host-ID
</dt> <dd>

Optional. Schließen Sie diesen Header nur ein, wenn die [BITS-IIS-Erweiterungseigenschaft](bits-iis-extension-properties.md)BITSHostId festgelegt ist. Ersetzen Sie PublicHostName durch den Servernamen oder die IP-Adresse aus der BITSHostId-Eigenschaft.

Der Client muss den Serverteil der Remote-URL für alle nachfolgenden Pakete ersetzen. Wenn der Client diesen Hostnamen in nachfolgenden Paketen nicht angibt, wird der Auftrag möglicherweise erneut auf einem anderen Server in der Farm gestartet, sodass eine Partuploaddatei auf dem vorherigen Server verbleibt.

</dd> <dt>

<span id="BITS-Host-Id-Fallback-Timeout"></span><span id="bits-host-id-fallback-timeout"></span><span id="BITS-HOST-ID-FALLBACK-TIMEOUT"></span>BITS-Host-Id-Fallback-Timeout
</dt> <dd>

Optional. Schließen Sie diesen Header nur ein, wenn der BITS-Host-Id-Header angegeben ist. Ersetzen Sie Timeout durch den Timeoutwert aus der BITSHostIdFallbackTimeout-Eigenschaft. Die BITSHostIdFallbackTimeout-Eigenschaft ist eine der [BITS-IIS-Erweiterungseigenschaften.](bits-iis-extension-properties.md)

Der Client verwendet den Time out-Zeitraum, um zu bestimmen, wie lange versucht wird, erneut eine Verbindung mit dem servernamen herzustellen, der im BITS-Host-Id-Header angegeben ist, bevor er auf den Hostnamen zurückgesetzt wird, der im Remotedateinamen des Auftrags angegeben ist. Der Timer beginnt, wenn BITS keine Verbindung mit dem BITS-Host-Id-Server herstellen kann. Der Timer wird zurückgesetzt, wenn eine Verbindung mit dem Server wiederhergestellt wird. Wenn kein Time out-Zeitraum angegeben ist, wird der Client nie auf den Hostnamen zurückgesetzt, der im Remotedateinamen angegeben ist.

</dd> <dt>

<span id="Accept-Encoding"></span><span id="accept-encoding"></span><span id="ACCEPT-ENCODING"></span>Accept-Encoding
</dt> <dd>

Identifiziert das Codierungsschema, das für die an den Server gesendeten Fragmente verwendet werden soll. Das Fragmentpaket enthält das codierte Fragment im Text des Pakets. Der BITS-Server erfordert Identitätscodierung (Klartext). Schließen Sie diesen Header nur ein, wenn reason-code 200 oder 201 ist.

</dd> <dt>

<span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Inhaltslänge
</dt> <dd>

Ersetzen Sie length durch die Anzahl der Bytes, die im Text der Antwort enthalten sind. Erforderlich, auch wenn der Text der Antwort keinen Inhalt enthält.

</dd> <dt>

<span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code
</dt> <dd>

Ersetzen Sie den Fehlercode durch eine Hexadezimalzahl, die einen HRESULT-Wert darstellt, der einem serverseitigen Fehler zugeordnet ist. Schließen Sie diesen Header nur ein, wenn reason-code nicht 200 oder 201 ist.

</dd> <dt>

<span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-Context
</dt> <dd>

Ersetzen Sie error-context durch eine Hexadezimalzahl, die den Kontext darstellt, in dem der Fehler aufgetreten ist. Geben Sie die Hexadezimalzahl für [**BG ERROR CONTEXT REMOTE \_ \_ \_ \_ FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) an, wenn der Server den Fehler generiert hat. Geben Sie andernfalls die Hexadezimalzahl für **BG ERROR CONTEXT REMOTE \_ \_ \_ \_ APPLICATION** (0x7) an, wenn der Fehler von der Anwendung generiert wurde, an die die Uploaddatei übergeben wird. Schließen Sie diesen Header nur ein, wenn der Reason-Code nicht 200 oder 201 ist.

</dd> </dl>

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Create-Session**](create-session.md)
</dt> </dl>

 

 





