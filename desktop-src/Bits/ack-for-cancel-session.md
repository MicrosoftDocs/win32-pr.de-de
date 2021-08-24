---
title: Ack für Cancel-Session
description: Verwenden Sie Ack für Cancel-Session Paket, um die Cancel-Session Anforderung des Clients zu bestätigen. Der Server sendet die Bestätigung, nachdem alle Ressourcen freigegeben wurden, die der Uploadsitzung zugeordnet sind.
ms.assetid: 670d061e-ab73-4aa8-85ba-2c9693794235
keywords:
- Ack für Cancel-Session BITS
topic_type:
- apiref
api_name:
- Ack for Cancel-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b23de0b23b0b87f559326c37ad61ecd09c38f697f0be48b45e92f5e7389b09fd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588820"
---
# <a name="ack-for-cancel-session"></a>Ack für Cancel-Session

Verwenden Sie den **Ack für das Cancel-Session-Paket,** um die [**Cancel-Session-Anforderung**](cancel-session.md) des Clients zu bestätigen. Der Server sendet die Bestätigung, nachdem alle Ressourcen freigegeben wurden, die der Uploadsitzung zugeordnet sind.

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

Ersetzen Sie reason-code durch den HTTP-Ursachencode. Legen Sie beispielsweise reason-code bei Erfolg auf 200 fest. Eine Liste der HTTP-Ursachencodes finden Sie unter [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).

</dd> <dt>

<span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>Ursachenbeschreibung
</dt> <dd>

Ersetzen Sie reason-description durch die HTTP-Beschreibung, die dem Ursachencode zugeordnet ist. Legen Sie beispielsweise reason-description auf OK fest, wenn reason-code 200 ist.

</dd> <dt>

<span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type
</dt> <dd>

Identifiziert dieses Antwortpaket als Ack-Paket.

</dd> <dt>

<span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Sitzungs-ID
</dt> <dd>

Zeichenfolgen-GUID, die die Sitzung für den Client identifiziert. Ersetzen Sie {guid} durch den Sitzungsbezeichner, den der Client im [**Anforderungspaket Cancel-Session**](cancel-session.md) gesendet hat. Wenn Sie den Sitzungsbezeichner nicht erkennen, legen Sie den HEADER BITS-Error-Code auf BG \_ E SESSION NOT FOUND \_ \_ \_ fest.

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

Ersetzen Sie error-context durch eine Hexadezimalzahl, die den Kontext darstellt, in dem der Fehler aufgetreten ist. Geben Sie die Hexadezimalzahl für [**BG_ERROR_CONTEXT_REMOTE_FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) an, wenn der Server den Fehler generiert hat. Geben Sie andernfalls die Hexadezimalzahl für **BG ERROR CONTEXT REMOTE \_ \_ \_ \_ APPLICATION** (0x7) an, wenn der Fehler von der Anwendung generiert wurde, an die die Uploaddatei übergeben wird. Schließen Sie diesen Header nur ein, wenn der Reason-Code nicht 200 oder 201 ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der BITS-Client gibt das [**Cancel-Session-Paket**](cancel-session.md) erneut zurück, wenn sich der Reason-Code im Bereich von 500 bis 599 befindet, es sei denn, der BITS-Error-Code-Header ist mit dem Wert BG \_ E SESSION NOT FOUND \_ \_ \_ vorhanden. Der Client wird aus den Ursachencodes 100 bis 499 nicht erneut versuchen.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ack for Close-Session**](ack-for-close-session.md)
</dt> <dt>

[**Cancel-Session**](cancel-session.md)
</dt> </dl>

 

 




