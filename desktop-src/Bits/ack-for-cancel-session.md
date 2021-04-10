---
title: Bestätigung für Cancel-Session
description: Verwenden Sie die Bestätigung für Cancel-Session Paket, um die Cancel-Session Anforderung des Clients zu bestätigen. Der Server sendet die Bestätigung, nachdem alle der Uploadsitzung zugeordneten Ressourcen freigegeben wurden.
ms.assetid: 670d061e-ab73-4aa8-85ba-2c9693794235
keywords:
- Bestätigung für Cancel-Session Bits
topic_type:
- apiref
api_name:
- Ack for Cancel-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b85ff937b720a69ee2722cef2f02b25273ea58d
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "104039814"
---
# <a name="ack-for-cancel-session"></a>Bestätigung für Cancel-Session

Verwenden Sie das Paket **ACK for Cancel-Session** , um die [**Abbruch Sitzungs**](cancel-session.md) Anforderung des Clients zu bestätigen. Der Server sendet die Bestätigung, nachdem alle der Uploadsitzung zugeordneten Ressourcen freigegeben wurden.

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
BITS-Session-Id: {guid}
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a>Header

<dl> <dt>

<span id="reason-code"></span><span id="REASON-CODE"></span>Grund: Code
</dt> <dd>

Ersetzen Sie Reason-Code durch den HTTP-Ursachen Code. Legen Sie z. b. Reason-Code auf 200 fest, wenn Erfolg. Eine Liste der http-Ursachen Codes finden Sie unter [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).

</dd> <dt>

<span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>Ursache: Beschreibung
</dt> <dd>

Ersetzen Sie Reason-Description durch die http-Beschreibung, die dem Ursachen Code zugeordnet ist. Legen Sie beispielsweise Reason-Description auf OK fest, wenn der Grund Code 200 ist.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>Bits-Pakettyp
</dt> <dd>

Identifiziert dieses Antwortpaket als ACK-Paket.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>Bits-Session-ID
</dt> <dd>

Zeichen folgen-GUID, die die Sitzung für den Client identifiziert. Ersetzen Sie {GUID} durch die Sitzungs-ID, die der Client im Anforderungspaket der [**Abbruch Sitzung**](cancel-session.md) gesendet hat. Wenn Sie die Sitzungs-ID nicht erkennen, legen Sie den Bits-Error-Code-Header auf BG \_ E \_ Session \_ nicht \_ gefunden fest.

</dd> <dt>

<span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Inhalts Länge
</dt> <dd>

Ersetzen Sie length durch die Anzahl der Bytes, die im Text der Antwort enthalten sind. Erforderlich, auch wenn der Text der Antwort keinen Inhalt enthält.

</dd> <dt>

<span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>Bits-Fehler Code
</dt> <dd>

Ersetzen Sie Error-Code durch eine hexadezimale Zahl, die einen HRESULT-Wert darstellt, der einem serverseitigen Fehler zugeordnet ist. Schließen Sie diesen Header nur ein, wenn Reason-Code nicht 200 oder 201 ist.

</dd> <dt>

<span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>Bits-Fehler-Kontext
</dt> <dd>

Ersetzen Sie Error-Context durch eine hexadezimale Zahl, die den Kontext darstellt, in dem der Fehler aufgetreten ist. Geben Sie die hexadezimale Zahl für [**BG_ERROR_CONTEXT_REMOTE_FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) an, wenn der Server den Fehler generiert hat. Andernfalls geben Sie die hexadezimale Zahl für eine **BG- \_ Fehler \_ Kontext- \_ Remote \_ Anwendung** (0x7) an, wenn der Fehler von der Anwendung generiert wurde, an die die Uploaddatei weitergeleitet wird. Fügen Sie diesen Header nur ein, wenn der Grund Code nicht 200 oder 201 ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der BITS-Client sendet das [**Cancel-Session**](cancel-session.md) -Paket erneut, wenn der Grund Code im Bereich von 500 bis 599 liegt, es sei denn, der Bits-Error-Code-Header ist mit dem Wert "BG \_ E Session" vorhanden \_ \_ \_ . Der Client versucht nicht, die Ursachen Codes 100 bis 499 zu wiederholen.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Bestätigung für Close-Session**](ack-for-close-session.md)
</dt> <dt>

[**Abbrechen-Sitzung**](cancel-session.md)
</dt> </dl>

 

 




