---
title: Ack for Close-Session
description: Verwenden Sie das Ack for Close-Session-Paket, um die Anforderung des Clients Close-Session bestätigen. Der Server sendet die Bestätigung nach der Freigabe aller Ressourcen, die der Uploadsitzung zugeordnet sind.
ms.assetid: 9d4b658a-8b41-4678-b996-f2174784cdd6
keywords:
- Ack für Close-Session BITS
topic_type:
- apiref
api_name:
- Ack for Close-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 289f2cfc2ca9f1e879e0aa592af28d86ae433f6e06d007aa71e00581baba2af5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835413"
---
# <a name="ack-for-close-session"></a>Ack for Close-Session

Verwenden Sie **das Ack for Close-Session-Paket,** um die [**Close-Session-Anforderung**](close-session.md) des Clients zu bestätigen. Der Server sendet die Bestätigung nach der Freigabe aller Ressourcen, die der Uploadsitzung zugeordnet sind.

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

<span id="reason-code"></span><span id="REASON-CODE"></span>reason-code
</dt> <dd>

Ersetzen Sie reason-code durch den HTTP-Grundcode. Legen Sie z. B. reason-code bei Erfolg auf 200 fest. Eine Liste der HTTP-Grundcodes finden Sie unter [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).

</dd> <dt>

<span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>reason-description
</dt> <dd>

Ersetzen Sie reason-description durch die HTTP-Beschreibung, die dem Grundcode zugeordnet ist. Legen Sie beispielsweise reason-description auf OK fest, wenn reason-code 200 ist.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type
</dt> <dd>

Identifiziert dieses Antwortpaket als Ack-Paket.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id
</dt> <dd>

Zeichenfolgen-GUID, die die Sitzung mit dem Client identifiziert. Ersetzen Sie {guid} durch den Sitzungsbezeichner, den der Client im [**Close-Session-Anforderungspaket**](close-session.md) gesendet hat. Wenn Sie den Sitzungsbezeichner nicht erkennen, legen Sie den BITS-Error-Code-Header auf BG \_ E SESSION NOT FOUND \_ \_ \_ fest.

</dd> <dt>

<span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length
</dt> <dd>

Ersetzen Sie length durch die Anzahl der Bytes, die im Text der Antwort enthalten sind. Content-Length ist erforderlich, auch wenn der Text der Antwort keinen Inhalt enthält.

</dd> <dt>

<span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Fehlercode
</dt> <dd>

Ersetzen Sie error-code durch eine Hexadezimalzahl, die einen HRESULT-Wert darstellt, der einem serverseitigen Fehler zugeordnet ist. Schließen Sie diesen Header nur ein, wenn reason-code nicht 200 oder 201 ist.

</dd> <dt>

<span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-Context
</dt> <dd>

Ersetzen Sie error-context durch eine Hexadezimalzahl, die den Kontext darstellt, in dem der Fehler aufgetreten ist. Geben Sie die Hexadezimalzahl für [**BG ERROR CONTEXT REMOTE \_ \_ \_ \_ FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) an, wenn der Server den Fehler generiert hat. Geben Sie andernfalls die Hexadezimalzahl für **BG ERROR CONTEXT REMOTE \_ \_ \_ \_ APPLICATION** (0x7) an, wenn der Fehler von der Anwendung generiert wurde, an die die Uploaddatei übergeben wird. Schließen Sie diesen Header nur ein, wenn der Grundcode nicht 200 oder 201 ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der BITS-Client gibt das [**Close-Session-Paket**](close-session.md) erneut zurück, wenn der Grundcode im Bereich von 500 bis 599 liegt, es sei denn, der BITS-Error-Code-Header ist mit dem Wert BG \_ E SESSION NOT FOUND \_ \_ \_ vorhanden. Der Client wird den Grundcode 100 bis 499 nicht wiederholen.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Ack für Cancel-Session**](ack-for-cancel-session.md)
</dt> <dt>

[**Close-Session**](close-session.md)
</dt> </dl>

 

 




