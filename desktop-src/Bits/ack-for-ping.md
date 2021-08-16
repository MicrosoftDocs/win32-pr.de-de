---
title: Ack für Ping
description: Verwenden Sie den Ack für das Ping-Paket, um die Ping-Anforderung des Clients zu bestätigen.
ms.assetid: 2e288564-d06f-4b45-b0c0-7aab1897da40
keywords:
- Ack für Ping BITS
topic_type:
- apiref
api_name:
- Ack for Ping
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09f31850599331027f3f8135a42dac8c8ea54519c04291d42fb06b5c7b8735fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835180"
---
# <a name="ack-for-ping"></a>Ack für Ping

Verwenden Sie den **Ack für das Ping-Paket,** um die [**Ping-Anforderung**](ping.md) des Clients zu bestätigen.

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
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

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Pingen**](ping.md)
</dt> </dl>

 

 




