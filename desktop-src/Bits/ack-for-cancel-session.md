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
# <a name="ack-for-cancel-session"></a><span data-ttu-id="c2fa7-105">Bestätigung für Cancel-Session</span><span class="sxs-lookup"><span data-stu-id="c2fa7-105">Ack for Cancel-Session</span></span>

<span data-ttu-id="c2fa7-106">Verwenden Sie das Paket **ACK for Cancel-Session** , um die [**Abbruch Sitzungs**](cancel-session.md) Anforderung des Clients zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="c2fa7-106">Use the **Ack for Cancel-Session** packet to acknowledge the client's [**Cancel-Session**](cancel-session.md) request.</span></span> <span data-ttu-id="c2fa7-107">Der Server sendet die Bestätigung, nachdem alle der Uploadsitzung zugeordneten Ressourcen freigegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="c2fa7-107">The server sends the acknowledgment after releasing all resources associated with the upload session.</span></span>

``` syntax
reason-code reason-description
BITS-Packet-Type: Ack
BITS-Session-Id: {guid}
Content-Length: length
BITS-Error-Code: error-code
BITS-Error-Context: error-context
```

## <a name="headers"></a><span data-ttu-id="c2fa7-108">Header</span><span class="sxs-lookup"><span data-stu-id="c2fa7-108">Headers</span></span>

<dl> <dt>

<span data-ttu-id="c2fa7-109"><span id="reason-code"></span><span id="REASON-CODE"></span>Grund: Code</span><span class="sxs-lookup"><span data-stu-id="c2fa7-109"><span id="reason-code"></span><span id="REASON-CODE"></span>reason-code</span></span>
</dt> <dd>

<span data-ttu-id="c2fa7-110">Ersetzen Sie Reason-Code durch den HTTP-Ursachen Code.</span><span class="sxs-lookup"><span data-stu-id="c2fa7-110">Replace reason-code with the HTTP reason code.</span></span> <span data-ttu-id="c2fa7-111">Legen Sie z. b. Reason-Code auf 200 fest, wenn Erfolg.</span><span class="sxs-lookup"><span data-stu-id="c2fa7-111">For example, set reason-code to 200 if success.</span></span> <span data-ttu-id="c2fa7-112">Eine Liste der http-Ursachen Codes finden Sie unter [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="c2fa7-112">For a list of HTTP reason codes, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>

</dd> <dt>

<span data-ttu-id="c2fa7-113"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>Ursache: Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2fa7-113"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>reason-description</span></span>
</dt> <dd>

<span data-ttu-id="c2fa7-114">Ersetzen Sie Reason-Description durch die http-Beschreibung, die dem Ursachen Code zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c2fa7-114">Replace reason-description with the HTTP description associated with the reason code.</span></span> <span data-ttu-id="c2fa7-115">Legen Sie beispielsweise Reason-Description auf OK fest, wenn der Grund Code 200 ist.</span><span class="sxs-lookup"><span data-stu-id="c2fa7-115">For example, set reason-description to OK if reason-code is 200.</span></span>

</dd> <dt>

<span data-ttu-id="c2fa7-116"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>Bits-Pakettyp</span><span class="sxs-lookup"><span data-stu-id="c2fa7-116"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="c2fa7-117">Identifiziert dieses Antwortpaket als ACK-Paket.</span><span class="sxs-lookup"><span data-stu-id="c2fa7-117">Identifies this response packet as an Ack packet.</span></span>

</dd> <dt>

<span data-ttu-id="c2fa7-118"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>Bits-Session-ID</span><span class="sxs-lookup"><span data-stu-id="c2fa7-118"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="c2fa7-119">Zeichen folgen-GUID, die die Sitzung für den Client identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c2fa7-119">String GUID that identifies the session to the client.</span></span> <span data-ttu-id="c2fa7-120">Ersetzen Sie {GUID} durch die Sitzungs-ID, die der Client im Anforderungspaket der [**Abbruch Sitzung**](cancel-session.md) gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="c2fa7-120">Replace {guid} with the session identifier that the client sent in the [**Cancel-Session**](cancel-session.md) request packet.</span></span> <span data-ttu-id="c2fa7-121">Wenn Sie die Sitzungs-ID nicht erkennen, legen Sie den Bits-Error-Code-Header auf BG \_ E \_ Session \_ nicht \_ gefunden fest.</span><span class="sxs-lookup"><span data-stu-id="c2fa7-121">If you do not recognize the session identifier, set the BITS-Error-Code header to BG\_E\_SESSION\_NOT\_FOUND.</span></span>

</dd> <dt>

<span data-ttu-id="c2fa7-122"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Inhalts Länge</span><span class="sxs-lookup"><span data-stu-id="c2fa7-122"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length</span></span>
</dt> <dd>

<span data-ttu-id="c2fa7-123">Ersetzen Sie length durch die Anzahl der Bytes, die im Text der Antwort enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c2fa7-123">Replace length with the number of bytes included in the body of the response.</span></span> <span data-ttu-id="c2fa7-124">Erforderlich, auch wenn der Text der Antwort keinen Inhalt enthält.</span><span class="sxs-lookup"><span data-stu-id="c2fa7-124">Required even if the body of the response does not include content.</span></span>

</dd> <dt>

<span data-ttu-id="c2fa7-125"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>Bits-Fehler Code</span><span class="sxs-lookup"><span data-stu-id="c2fa7-125"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code</span></span>
</dt> <dd>

<span data-ttu-id="c2fa7-126">Ersetzen Sie Error-Code durch eine hexadezimale Zahl, die einen HRESULT-Wert darstellt, der einem serverseitigen Fehler zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c2fa7-126">Replace error-code with a hexadecimal number that represents an HRESULT value associated with a server-side error.</span></span> <span data-ttu-id="c2fa7-127">Schließen Sie diesen Header nur ein, wenn Reason-Code nicht 200 oder 201 ist.</span><span class="sxs-lookup"><span data-stu-id="c2fa7-127">Only include this header if reason-code is not 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="c2fa7-128"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>Bits-Fehler-Kontext</span><span class="sxs-lookup"><span data-stu-id="c2fa7-128"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-Context</span></span>
</dt> <dd>

<span data-ttu-id="c2fa7-129">Ersetzen Sie Error-Context durch eine hexadezimale Zahl, die den Kontext darstellt, in dem der Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="c2fa7-129">Replace error-context with a hexadecimal number that represents the context in which the error occurred.</span></span> <span data-ttu-id="c2fa7-130">Geben Sie die hexadezimale Zahl für [**BG_ERROR_CONTEXT_REMOTE_FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) an, wenn der Server den Fehler generiert hat.</span><span class="sxs-lookup"><span data-stu-id="c2fa7-130">Specify the hexadecimal number for [**BG_ERROR_CONTEXT_REMOTE_FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) if the server generated the error.</span></span> <span data-ttu-id="c2fa7-131">Andernfalls geben Sie die hexadezimale Zahl für eine **BG- \_ Fehler \_ Kontext- \_ Remote \_ Anwendung** (0x7) an, wenn der Fehler von der Anwendung generiert wurde, an die die Uploaddatei weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="c2fa7-131">Otherwise, specify the hexadecimal number for **BG\_ERROR\_CONTEXT\_REMOTE\_APPLICATION** (0x7) if the error was generated by the application to which the upload file is passed.</span></span> <span data-ttu-id="c2fa7-132">Fügen Sie diesen Header nur ein, wenn der Grund Code nicht 200 oder 201 ist.</span><span class="sxs-lookup"><span data-stu-id="c2fa7-132">Include this header only if the reason-code is not 200 or 201.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c2fa7-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2fa7-133">Remarks</span></span>

<span data-ttu-id="c2fa7-134">Der BITS-Client sendet das [**Cancel-Session**](cancel-session.md) -Paket erneut, wenn der Grund Code im Bereich von 500 bis 599 liegt, es sei denn, der Bits-Error-Code-Header ist mit dem Wert "BG \_ E Session" vorhanden \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c2fa7-134">The BITS client resends the [**Cancel-Session**](cancel-session.md) packet if the reason-code is in the range from 500 through 599, unless the BITS-Error-Code header is present with a value of BG\_E\_SESSION\_NOT\_FOUND.</span></span> <span data-ttu-id="c2fa7-135">Der Client versucht nicht, die Ursachen Codes 100 bis 499 zu wiederholen.</span><span class="sxs-lookup"><span data-stu-id="c2fa7-135">The client will not retry for reason codes 100 through 499.</span></span>

## <a name="see-also"></a><span data-ttu-id="c2fa7-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2fa7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2fa7-137">**Bestätigung für Close-Session**</span><span class="sxs-lookup"><span data-stu-id="c2fa7-137">**Ack for Close-Session**</span></span>](ack-for-close-session.md)
</dt> <dt>

[<span data-ttu-id="c2fa7-138">**Abbrechen-Sitzung**</span><span class="sxs-lookup"><span data-stu-id="c2fa7-138">**Cancel-Session**</span></span>](cancel-session.md)
</dt> </dl>

 

 




