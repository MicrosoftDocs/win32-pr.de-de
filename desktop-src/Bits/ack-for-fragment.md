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
# <a name="ack-for-fragment"></a><span data-ttu-id="54e4a-104">Bestätigung für Fragment</span><span class="sxs-lookup"><span data-stu-id="54e4a-104">Ack for Fragment</span></span>

<span data-ttu-id="54e4a-105">Verwenden Sie das **ACK for Fragment** -Paket, um die [**fragmentanforderung**](fragment.md) des Clients zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="54e4a-105">Use the **Ack for Fragment** packet to acknowledge the client's [**Fragment**](fragment.md) request.</span></span>

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

## <a name="headers"></a><span data-ttu-id="54e4a-106">Header</span><span class="sxs-lookup"><span data-stu-id="54e4a-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="54e4a-107"><span id="reason-code"></span><span id="REASON-CODE"></span>Grund: Code</span><span class="sxs-lookup"><span data-stu-id="54e4a-107"><span id="reason-code"></span><span id="REASON-CODE"></span>reason-code</span></span>
</dt> <dd>

<span data-ttu-id="54e4a-108">Ersetzen Sie Reason-Code durch einen HTTP-Ursachen Code.</span><span class="sxs-lookup"><span data-stu-id="54e4a-108">Replace reason-code with an HTTP reason code.</span></span> <span data-ttu-id="54e4a-109">In der folgenden Tabelle sind die typischen Ursachen Codes für eine Antwort auf eine [**fragmentanforderung**](fragment.md) aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="54e4a-109">The following table shows the typical reason codes for a response to a [**Fragment**](fragment.md) request.</span></span> <span data-ttu-id="54e4a-110">Eine Liste der http-Ursachen Codes finden Sie unter [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="54e4a-110">For a list of HTTP reason codes, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>



| <span data-ttu-id="54e4a-111">Ursachencode</span><span class="sxs-lookup"><span data-stu-id="54e4a-111">Reason code</span></span>    | <span data-ttu-id="54e4a-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="54e4a-112">Description</span></span>                                                                                                            |
|----------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54e4a-113">200</span><span class="sxs-lookup"><span data-stu-id="54e4a-113">200</span></span><br/> | <span data-ttu-id="54e4a-114">OK.</span><span class="sxs-lookup"><span data-stu-id="54e4a-114">OK.</span></span> <span data-ttu-id="54e4a-115">Die Anforderung wurde erfolgreich gesendet.</span><span class="sxs-lookup"><span data-stu-id="54e4a-115">The request was successful.</span></span><br/>                                                                             |
| <span data-ttu-id="54e4a-116">416</span><span class="sxs-lookup"><span data-stu-id="54e4a-116">416</span></span><br/> | <span data-ttu-id="54e4a-117">Bereich-nicht-befriedbar.</span><span class="sxs-lookup"><span data-stu-id="54e4a-117">Range-Not-Satisfiable.</span></span> <span data-ttu-id="54e4a-118">Der Client hat ein Fragment gesendet, dessen Bereich nicht zusammenhängend mit dem vorherigen Fragment ist.</span><span class="sxs-lookup"><span data-stu-id="54e4a-118">The client sent a fragment whose range is not contiguous with the previous fragment.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="54e4a-119"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>Ursache: Beschreibung</span><span class="sxs-lookup"><span data-stu-id="54e4a-119"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>reason-description</span></span>
</dt> <dd>

<span data-ttu-id="54e4a-120">Ersetzen Sie Reason-Description durch die http-Beschreibung, die dem Ursachen Code zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="54e4a-120">Replace reason-description with the HTTP description associated with the reason code.</span></span> <span data-ttu-id="54e4a-121">Legen Sie beispielsweise Reason-Description auf OK fest, wenn der Grund Code 200 ist.</span><span class="sxs-lookup"><span data-stu-id="54e4a-121">For example, set reason-description to OK if reason-code is 200.</span></span>

</dd> <dt>

<span data-ttu-id="54e4a-122"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>Bits-Pakettyp</span><span class="sxs-lookup"><span data-stu-id="54e4a-122"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="54e4a-123">Identifiziert dieses Antwortpaket als ACK-Paket.</span><span class="sxs-lookup"><span data-stu-id="54e4a-123">Identifies this response packet as an Ack packet.</span></span>

</dd> <dt>

<span data-ttu-id="54e4a-124"><span id="BITS-Received-Content-Range"></span><span id="bits-received-content-range"></span><span id="BITS-RECEIVED-CONTENT-RANGE"></span>Bits-empfangen-Content-Range</span><span class="sxs-lookup"><span data-stu-id="54e4a-124"><span id="BITS-Received-Content-Range"></span><span id="bits-received-content-range"></span><span id="BITS-RECEIVED-CONTENT-RANGE"></span>BITS-Received-Content-Range</span></span>
</dt> <dd>

<span data-ttu-id="54e4a-125">NULL basierter Offset zum nächsten Byte, den der Server vom Client erwartet.</span><span class="sxs-lookup"><span data-stu-id="54e4a-125">Zero-based offset to the next byte the server expects the client to send.</span></span> <span data-ttu-id="54e4a-126">Wenn das Fragment z. b. den Bereich 128 212 enthielt, legen Sie Bereich auf 213 fest.</span><span class="sxs-lookup"><span data-stu-id="54e4a-126">For example, if the fragment contained the range 128 212, you would set range to 213.</span></span>

</dd> <dt>

<span data-ttu-id="54e4a-127"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>Bits-Session-ID</span><span class="sxs-lookup"><span data-stu-id="54e4a-127"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="54e4a-128">Zeichen folgen-GUID, die die Sitzung für den Client identifiziert.</span><span class="sxs-lookup"><span data-stu-id="54e4a-128">String GUID that identifies the session to the client.</span></span> <span data-ttu-id="54e4a-129">Ersetzen Sie {GUID} durch den Sitzungs Bezeichner, den der Client im [**fragmentanforderungs**](fragment.md) Paket gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="54e4a-129">Replace {guid} with the session identifier that the client sent in the [**Fragment**](fragment.md) request packet.</span></span> <span data-ttu-id="54e4a-130">Wenn Sie die Sitzungs-ID nicht erkennen, legen Sie den Bits-Error-Code-Header auf BG \_ E \_ Session \_ nicht \_ gefunden fest.</span><span class="sxs-lookup"><span data-stu-id="54e4a-130">If you do not recognize the session identifier, set the BITS-Error-Code header to BG\_E\_SESSION\_NOT\_FOUND.</span></span>

</dd> <dt>

<span data-ttu-id="54e4a-131"><span id="BITS-Reply-URL"></span><span id="bits-reply-url"></span><span id="BITS-REPLY-URL"></span>Bits-Antwort-URL</span><span class="sxs-lookup"><span data-stu-id="54e4a-131"><span id="BITS-Reply-URL"></span><span id="bits-reply-url"></span><span id="BITS-REPLY-URL"></span>BITS-Reply-URL</span></span>
</dt> <dd>

<span data-ttu-id="54e4a-132">Enthält die URL zu den Antwortdaten eines Upload-Antwort-Auftrags.</span><span class="sxs-lookup"><span data-stu-id="54e4a-132">Contains the URL to the reply data of an upload-reply job.</span></span> <span data-ttu-id="54e4a-133">Fügen Sie diesen Header in die endgültige fragmentantwort ein, nachdem der Upload abgeschlossen ist, und Sie erhalten ggf. eine Antwort von der Serveranwendung.</span><span class="sxs-lookup"><span data-stu-id="54e4a-133">Include this header in the final fragment response after the upload is complete and you receive a response from the server application, if applicable.</span></span>

<span data-ttu-id="54e4a-134">Verwenden Sie den Content-Range-Header aus der fragmentanforderung, um zu bestimmen, ob der Upload fertiggestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="54e4a-134">Use the Content-Range header from the Fragment request to determine whether the upload is complete.</span></span> <span data-ttu-id="54e4a-135">Der Upload ist abgeschlossen, wenn der Ende Offset des Bereichs Werts dem Wert der Gesamtlänge minus 1 entspricht.</span><span class="sxs-lookup"><span data-stu-id="54e4a-135">The upload is complete if the end offset of the range value equals the total-length value minus one.</span></span>

<span data-ttu-id="54e4a-136">Der BITS-Server sendet die Uploaddatei an die Serveranwendung, nachdem er den Abschluss des Uploads festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="54e4a-136">The BITS server posts the upload file to the server application after it determines the upload is complete.</span></span> <span data-ttu-id="54e4a-137">Die Serveranwendung verarbeitet die Datei und generiert die Antwort.</span><span class="sxs-lookup"><span data-stu-id="54e4a-137">The server application processes the file and generates the reply.</span></span> <span data-ttu-id="54e4a-138">Der BITS-Server legt den Wert von Bits-Reply-URL auf die URL der Antwortdatei von der Serveranwendung fest.</span><span class="sxs-lookup"><span data-stu-id="54e4a-138">The BITS server sets the value of BITS-Reply-URL to the URL of the reply file from the server application.</span></span>

</dd> <dt>

<span data-ttu-id="54e4a-139"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Inhalts Länge</span><span class="sxs-lookup"><span data-stu-id="54e4a-139"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length</span></span>
</dt> <dd>

<span data-ttu-id="54e4a-140">Ersetzen Sie length durch die Anzahl der Bytes, die im Text der Antwort enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="54e4a-140">Replace length with the number of bytes included in the body of the response.</span></span> <span data-ttu-id="54e4a-141">Content-length ist erforderlich, auch wenn der Text der Antwort keinen Inhalt enthält.</span><span class="sxs-lookup"><span data-stu-id="54e4a-141">Content-Length is required, even if the body of the response does not include content.</span></span>

</dd> <dt>

<span data-ttu-id="54e4a-142"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>Bits-Fehler Code</span><span class="sxs-lookup"><span data-stu-id="54e4a-142"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code</span></span>
</dt> <dd>

<span data-ttu-id="54e4a-143">Ersetzen Sie Error-Code durch eine hexadezimale Zahl, die einen HRESULT-Wert darstellt, der einem serverseitigen Fehler zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="54e4a-143">Replace error-code with a hexadecimal number that represents an HRESULT value associated with a server-side error.</span></span> <span data-ttu-id="54e4a-144">Schließen Sie diesen Header nur ein, wenn Reason-Code nicht 200 oder 201 ist.</span><span class="sxs-lookup"><span data-stu-id="54e4a-144">Only include this header if reason-code is not 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="54e4a-145"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>Bits-Fehler-Kontext</span><span class="sxs-lookup"><span data-stu-id="54e4a-145"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-Context</span></span>
</dt> <dd>

<span data-ttu-id="54e4a-146">Ersetzen Sie Error-Context durch eine hexadezimale Zahl, die den Kontext darstellt, in dem der Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="54e4a-146">Replace error-context with a hexadecimal number that represents the context in which the error occurred.</span></span> <span data-ttu-id="54e4a-147">Geben Sie die hexadezimale Zahl der [**\_ \_ \_ Remote \_ Datei des BG-Fehler Kontexts**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) an, wenn der Server den Fehler generiert hat.</span><span class="sxs-lookup"><span data-stu-id="54e4a-147">Specify the hexadecimal number for [**BG\_ERROR\_CONTEXT\_REMOTE\_FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) if the server generated the error.</span></span> <span data-ttu-id="54e4a-148">Andernfalls geben Sie die hexadezimale Zahl für eine **BG- \_ Fehler \_ Kontext- \_ Remote \_ Anwendung** (0x7) an, wenn der Fehler von der Anwendung generiert wurde, an die die Uploaddatei weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="54e4a-148">Otherwise, specify the hexadecimal number for **BG\_ERROR\_CONTEXT\_REMOTE\_APPLICATION** (0x7) if the error was generated by the application to which the upload file is passed.</span></span> <span data-ttu-id="54e4a-149">Fügen Sie diesen Header nur ein, wenn der Grund Code nicht 200 oder 201 ist.</span><span class="sxs-lookup"><span data-stu-id="54e4a-149">Include this header only if the reason-code is not 200 or 201.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="54e4a-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54e4a-150">Remarks</span></span>

<span data-ttu-id="54e4a-151">Wenn die Sitzung für einen Upload-Antwort-Auftrag gilt, kann es zu einer Verzögerung kommen, bevor der Client die endgültige Bestätigung **für die fragmentantwort** erhält.</span><span class="sxs-lookup"><span data-stu-id="54e4a-151">If the session is for an upload-reply job, there may be a delay before the client receives the final **Ack for Fragment** response.</span></span> <span data-ttu-id="54e4a-152">Die Länge der Verzögerung hängt von der Zeitspanne ab, die die Serveranwendung (auf die der Server die Uploaddatei sendet) benötigt, um die Antwort zu generieren.</span><span class="sxs-lookup"><span data-stu-id="54e4a-152">The length of the delay depends on the amount of time the server application (application to which the server posts the upload file) takes to generate the reply.</span></span>

## <a name="see-also"></a><span data-ttu-id="54e4a-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54e4a-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54e4a-154">**Create-Session**</span><span class="sxs-lookup"><span data-stu-id="54e4a-154">**Create-Session**</span></span>](create-session.md)
</dt> <dt>

[<span data-ttu-id="54e4a-155">**Fragment**</span><span class="sxs-lookup"><span data-stu-id="54e4a-155">**Fragment**</span></span>](fragment.md)
</dt> </dl>

 

 





