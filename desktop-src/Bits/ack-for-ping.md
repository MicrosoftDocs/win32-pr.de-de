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
# <a name="ack-for-ping"></a><span data-ttu-id="95dcc-104">Bestätigung für Ping</span><span class="sxs-lookup"><span data-stu-id="95dcc-104">Ack for Ping</span></span>

<span data-ttu-id="95dcc-105">Verwenden Sie die Bestätigung **für das Ping** -Paket, um die [**ping**](ping.md) -Anforderung des Clients zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="95dcc-105">Use the **Ack for Ping** packet to acknowledge the client's [**Ping**](ping.md) request.</span></span>

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a><span data-ttu-id="95dcc-106">Header</span><span class="sxs-lookup"><span data-stu-id="95dcc-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="95dcc-107"><span id="reason-code"></span><span id="REASON-CODE"></span>Grund: Code</span><span class="sxs-lookup"><span data-stu-id="95dcc-107"><span id="reason-code"></span><span id="REASON-CODE"></span>reason-code</span></span>
</dt> <dd>

<span data-ttu-id="95dcc-108">Ersetzen Sie Reason-Code durch den HTTP-Ursachen Code.</span><span class="sxs-lookup"><span data-stu-id="95dcc-108">Replace reason-code with the HTTP reason code.</span></span> <span data-ttu-id="95dcc-109">Legen Sie z. b. Reason-Code auf 200 fest, wenn Erfolg.</span><span class="sxs-lookup"><span data-stu-id="95dcc-109">For example, set reason-code to 200 if success.</span></span> <span data-ttu-id="95dcc-110">Eine Liste der http-Ursachen Codes finden Sie unter [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="95dcc-110">For a list of HTTP reason codes, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>

</dd> <dt>

<span data-ttu-id="95dcc-111"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>Ursache: Beschreibung</span><span class="sxs-lookup"><span data-stu-id="95dcc-111"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>reason-description</span></span>
</dt> <dd>

<span data-ttu-id="95dcc-112">Ersetzen Sie Reason-Description durch die http-Beschreibung, die dem Ursachen Code zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="95dcc-112">Replace reason-description with the HTTP description associated with the reason code.</span></span> <span data-ttu-id="95dcc-113">Legen Sie beispielsweise Reason-Description auf OK fest, wenn der Grund Code 200 ist.</span><span class="sxs-lookup"><span data-stu-id="95dcc-113">For example, set reason-description to OK if reason-code is 200.</span></span>

</dd> <dt>

<span data-ttu-id="95dcc-114"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>Bits-Pakettyp</span><span class="sxs-lookup"><span data-stu-id="95dcc-114"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="95dcc-115">Identifiziert dieses Antwortpaket als ACK-Paket.</span><span class="sxs-lookup"><span data-stu-id="95dcc-115">Identifies this response packet as an Ack packet.</span></span>

</dd> <dt>

<span data-ttu-id="95dcc-116"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Inhalts Länge</span><span class="sxs-lookup"><span data-stu-id="95dcc-116"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length</span></span>
</dt> <dd>

<span data-ttu-id="95dcc-117">Ersetzen Sie length durch die Anzahl der Bytes, die im Text der Antwort enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="95dcc-117">Replace length with the number of bytes included in the body of the response.</span></span> <span data-ttu-id="95dcc-118">Erforderlich, auch wenn der Text der Antwort keinen Inhalt enthält.</span><span class="sxs-lookup"><span data-stu-id="95dcc-118">Required even if the body of the response does not include content.</span></span>

</dd> <dt>

<span data-ttu-id="95dcc-119"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>Bits-Fehler Code</span><span class="sxs-lookup"><span data-stu-id="95dcc-119"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code</span></span>
</dt> <dd>

<span data-ttu-id="95dcc-120">Ersetzen Sie Error-Code durch eine hexadezimale Zahl, die einen HRESULT-Wert darstellt, der einem serverseitigen Fehler zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="95dcc-120">Replace error-code with a hexadecimal number that represents an HRESULT value associated with a server-side error.</span></span> <span data-ttu-id="95dcc-121">Fügen Sie diesen Header nur ein, wenn Reason-Code nicht 200 oder 201 ist.</span><span class="sxs-lookup"><span data-stu-id="95dcc-121">Include this header only if reason-code is not 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="95dcc-122"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>Bits-Fehler-Kontext</span><span class="sxs-lookup"><span data-stu-id="95dcc-122"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-Context</span></span>
</dt> <dd>

<span data-ttu-id="95dcc-123">Ersetzen Sie Error-Context durch eine hexadezimale Zahl, die den Kontext darstellt, in dem der Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="95dcc-123">Replace error-context with a hexadecimal number that represents the context in which the error occurred.</span></span> <span data-ttu-id="95dcc-124">Geben Sie die hexadezimale Zahl der [**\_ \_ \_ Remote \_ Datei des BG-Fehler Kontexts**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) an, wenn der Server den Fehler generiert hat.</span><span class="sxs-lookup"><span data-stu-id="95dcc-124">Specify the hexadecimal number for [**BG\_ERROR\_CONTEXT\_REMOTE\_FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) if the server generated the error.</span></span> <span data-ttu-id="95dcc-125">Andernfalls geben Sie die hexadezimale Zahl für eine **BG- \_ Fehler \_ Kontext- \_ Remote \_ Anwendung** (0x7) an, wenn der Fehler von der Anwendung generiert wurde, an die die Uploaddatei weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="95dcc-125">Otherwise, specify the hexadecimal number for **BG\_ERROR\_CONTEXT\_REMOTE\_APPLICATION** (0x7) if the error was generated by the application to which the upload file is passed.</span></span> <span data-ttu-id="95dcc-126">Fügen Sie diesen Header nur ein, wenn der Grund Code nicht 200 oder 201 ist.</span><span class="sxs-lookup"><span data-stu-id="95dcc-126">Include this header only if the reason-code is not 200 or 201.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="95dcc-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95dcc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95dcc-128">**Ping**</span><span class="sxs-lookup"><span data-stu-id="95dcc-128">**Ping**</span></span>](ping.md)
</dt> </dl>

 

 




