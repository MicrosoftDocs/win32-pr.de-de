---
title: Bestätigung für Ping
description: Verwenden Sie die Bestätigung für das Ping-Paket, um die Ping-Anforderung des Clients zu bestätigen.
ms.assetid: 2e288564-d06f-4b45-b0c0-7aab1897da40
keywords:
- Bestätigung für pingbits
topic_type:
- apiref
api_name:
- Ack for Ping
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5a3ca765c8bd7758f19abe396ad0449a5895d8e
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "103949206"
---
# <a name="ack-for-ping"></a>Bestätigung für Ping

Verwenden Sie die Bestätigung **für das Ping** -Paket, um die [**ping**](ping.md) -Anforderung des Clients zu bestätigen.

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
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

[**Ping**](ping.md)
</dt> </dl>

 

 




