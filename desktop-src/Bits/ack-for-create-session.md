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
# <a name="ack-for-create-session"></a><span data-ttu-id="78303-104">Bestätigung für Create-Session</span><span class="sxs-lookup"><span data-stu-id="78303-104">Ack for Create-Session</span></span>

<span data-ttu-id="78303-105">Verwenden Sie das Paket " **ACK for Create-Session** ", um die Anforderung zum [**Erstellen einer Sitzung**](create-session.md) zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="78303-105">Use the **Ack for Create-Session** packet to acknowledge the client's [**Create-Session**](create-session.md) request.</span></span>

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

## <a name="headers"></a><span data-ttu-id="78303-106">Header</span><span class="sxs-lookup"><span data-stu-id="78303-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="78303-107"><span id="reason-code"></span><span id="REASON-CODE"></span>Grund: Code</span><span class="sxs-lookup"><span data-stu-id="78303-107"><span id="reason-code"></span><span id="REASON-CODE"></span>reason-code</span></span>
</dt> <dd>

<span data-ttu-id="78303-108">Ersetzen Sie Reason-Code durch den HTTP-Ursachen Code.</span><span class="sxs-lookup"><span data-stu-id="78303-108">Replace reason-code with the HTTP reason code.</span></span> <span data-ttu-id="78303-109">In der folgenden Tabelle werden die typischen Ursachen Codes für eine Antwort auf eine Anforderung zum [**Erstellen einer Sitzung**](create-session.md) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="78303-109">The following table shows the typical reason codes for a response to a [**Create-Session**](create-session.md) request.</span></span> <span data-ttu-id="78303-110">Eine Liste der http-Ursachen Codes finden Sie unter [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="78303-110">For a list of HTTP reason codes, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>



| <span data-ttu-id="78303-111">Ursachencode</span><span class="sxs-lookup"><span data-stu-id="78303-111">Reason code</span></span>    | <span data-ttu-id="78303-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="78303-112">Description</span></span>                                                                         |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="78303-113">200</span><span class="sxs-lookup"><span data-stu-id="78303-113">200</span></span><br/> | <span data-ttu-id="78303-114">OK.</span><span class="sxs-lookup"><span data-stu-id="78303-114">OK.</span></span> <span data-ttu-id="78303-115">Die Anforderung wurde erfolgreich gesendet.</span><span class="sxs-lookup"><span data-stu-id="78303-115">The request was successful.</span></span><br/>                                          |
| <span data-ttu-id="78303-116">201</span><span class="sxs-lookup"><span data-stu-id="78303-116">201</span></span><br/> | <span data-ttu-id="78303-117">Erstellt.</span><span class="sxs-lookup"><span data-stu-id="78303-117">Created.</span></span> <span data-ttu-id="78303-118">Die Sitzung wurde erstellt.</span><span class="sxs-lookup"><span data-stu-id="78303-118">The session was created.</span></span><br/>                                        |
| <span data-ttu-id="78303-119">403</span><span class="sxs-lookup"><span data-stu-id="78303-119">403</span></span><br/> | <span data-ttu-id="78303-120">Unzulässig.</span><span class="sxs-lookup"><span data-stu-id="78303-120">Forbidden.</span></span> <span data-ttu-id="78303-121">Der Benutzer darf keine Dateien in die angegebene URL hochladen.</span><span class="sxs-lookup"><span data-stu-id="78303-121">The user is not allowed to upload files to the specified URL.</span></span><br/> |
| <span data-ttu-id="78303-122">404</span><span class="sxs-lookup"><span data-stu-id="78303-122">404</span></span><br/> | <span data-ttu-id="78303-123">Nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="78303-123">Not Found.</span></span> <span data-ttu-id="78303-124">Die angegebene URL ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="78303-124">The specified URL does not exist.</span></span><br/>                             |
| <span data-ttu-id="78303-125">409</span><span class="sxs-lookup"><span data-stu-id="78303-125">409</span></span><br/> | <span data-ttu-id="78303-126">Konflikt.</span><span class="sxs-lookup"><span data-stu-id="78303-126">Conflict.</span></span> <span data-ttu-id="78303-127">Die Datei ist auf dem Server vorhanden und kann nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="78303-127">The file exists on the server and cannot be overwritten.</span></span><br/>       |



 

</dd> <dt>

<span data-ttu-id="78303-128"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>Ursache: Beschreibung</span><span class="sxs-lookup"><span data-stu-id="78303-128"><span id="reason-description"></span><span id="REASON-DESCRIPTION"></span>reason-description</span></span>
</dt> <dd>

<span data-ttu-id="78303-129">Ersetzen Sie Reason-Description durch die http-Beschreibung, die dem Ursachen Code zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="78303-129">Replace reason-description with the HTTP description associated with the reason code.</span></span> <span data-ttu-id="78303-130">Legen Sie beispielsweise Reason-Description auf OK fest, wenn der Grund Code 200 ist.</span><span class="sxs-lookup"><span data-stu-id="78303-130">For example, set reason-description to OK if reason-code is 200.</span></span>

</dd> <dt>

<span data-ttu-id="78303-131"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>Bits-Pakettyp</span><span class="sxs-lookup"><span data-stu-id="78303-131"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="78303-132">Identifiziert dieses Antwortpaket als ACK-Paket.</span><span class="sxs-lookup"><span data-stu-id="78303-132">Identifies this response packet as an Ack packet.</span></span>

</dd> <dt>

<span data-ttu-id="78303-133"><span id="BITS-Protocol"></span><span id="bits-protocol"></span><span id="BITS-PROTOCOL"></span>BITS-Protokoll</span><span class="sxs-lookup"><span data-stu-id="78303-133"><span id="BITS-Protocol"></span><span id="bits-protocol"></span><span id="BITS-PROTOCOL"></span>BITS-Protocol</span></span>
</dt> <dd>

<span data-ttu-id="78303-134">Zeichen folgen-GUID, die das Protokoll identifiziert, das der Server für diese Sitzung verwenden möchte.</span><span class="sxs-lookup"><span data-stu-id="78303-134">String GUID that identifies the protocol that the server wants to use for this session.</span></span> <span data-ttu-id="78303-135">Ersetzen Sie {GUID} durch die Protokoll-ID aus der Liste der Protokolle, die der Client in der [**Create-Session-**](create-session.md) Anforderung enthält. der Bits-supported-Protocol-Header enthält die Liste.</span><span class="sxs-lookup"><span data-stu-id="78303-135">Replace {guid} with the protocol identifier from the list of protocols the client includes in the [**Create-Session**](create-session.md) request; the BITS-Supported-Protocol header contains the list.</span></span> <span data-ttu-id="78303-136">Fügen Sie diesen Header nur ein, wenn der Grund Code 200 oder 201 ist.</span><span class="sxs-lookup"><span data-stu-id="78303-136">Include this header only if the reason-code is 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="78303-137"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>Bits-Session-ID</span><span class="sxs-lookup"><span data-stu-id="78303-137"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="78303-138">Zeichen folgen-GUID, die diese Sitzung für den Client identifiziert.</span><span class="sxs-lookup"><span data-stu-id="78303-138">String GUID that identifies this session to the client.</span></span> <span data-ttu-id="78303-139">Ersetzen Sie {GUID} durch die Sitzungs-ID, die der Client in allen nachfolgenden Anforderungs Paketen sendet.</span><span class="sxs-lookup"><span data-stu-id="78303-139">Replace {guid} with the session identifier that the client sends in all subsequent request packets.</span></span>

<span data-ttu-id="78303-140">Bits verwendet eine GUID zum Identifizieren der Sitzung, Sie können jedoch jede beliebige http-Zeichenfolge mit bis zu 100 Zeichen verwenden.</span><span class="sxs-lookup"><span data-stu-id="78303-140">BITS uses a GUID to identify the session, but you can use any HTTP-legal string up to 100 characters.</span></span>

</dd> <dt>

<span data-ttu-id="78303-141"><span id="BITS-Host-Id"></span><span id="bits-host-id"></span><span id="BITS-HOST-ID"></span>Bits-Host-ID</span><span class="sxs-lookup"><span data-stu-id="78303-141"><span id="BITS-Host-Id"></span><span id="bits-host-id"></span><span id="BITS-HOST-ID"></span>BITS-Host-Id</span></span>
</dt> <dd>

<span data-ttu-id="78303-142">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="78303-142">Optional.</span></span> <span data-ttu-id="78303-143">Fügen Sie diesen Header nur ein, wenn die [BITS-IIS-Erweiterungs Eigenschaft](bits-iis-extension-properties.md), bitshostid, festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="78303-143">Include this header only if the [BITS IIS extension property](bits-iis-extension-properties.md), BITSHostId, is set.</span></span> <span data-ttu-id="78303-144">Ersetzen Sie publichostname durch den Servernamen oder die IP-Adresse aus der bitshostid-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="78303-144">Replace PublicHostName with the server name or IP address from the BITSHostId property.</span></span>

<span data-ttu-id="78303-145">Der Client muss den Serverteil der Remote-URL für alle nachfolgenden Pakete ersetzen.</span><span class="sxs-lookup"><span data-stu-id="78303-145">The client must replace the server portion of the remote-URL on all subsequent packets.</span></span> <span data-ttu-id="78303-146">Wenn der Client diesen Hostnamen für nachfolgende Pakete nicht angibt, wird der Auftrag möglicherweise erneut auf einem anderen Server in der Farm gestartet, wobei eine partielle Uploaddatei auf dem vorherigen Server belassen wird.</span><span class="sxs-lookup"><span data-stu-id="78303-146">If the client does not specify this host name on subsequent packets, it is possible that the job will begin again on another server in the farm, leaving a partial upload file on the previous server.</span></span>

</dd> <dt>

<span data-ttu-id="78303-147"><span id="BITS-Host-Id-Fallback-Timeout"></span><span id="bits-host-id-fallback-timeout"></span><span id="BITS-HOST-ID-FALLBACK-TIMEOUT"></span>Bits-Host-ID-Fallback-Timeout</span><span class="sxs-lookup"><span data-stu-id="78303-147"><span id="BITS-Host-Id-Fallback-Timeout"></span><span id="bits-host-id-fallback-timeout"></span><span id="BITS-HOST-ID-FALLBACK-TIMEOUT"></span>BITS-Host-Id-Fallback-Timeout</span></span>
</dt> <dd>

<span data-ttu-id="78303-148">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="78303-148">Optional.</span></span> <span data-ttu-id="78303-149">Fügen Sie diesen Header nur ein, wenn der Bits-Host-ID-Header angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="78303-149">Include this header only if the BITS-Host-Id header is specified.</span></span> <span data-ttu-id="78303-150">Ersetzen Sie Timeout durch den Timeout Wert aus der bitshostidfallbacktimeout-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="78303-150">Replace Timeout with the time-out value from the BITSHostIdFallbackTimeout property.</span></span> <span data-ttu-id="78303-151">Die bitshostidfallbacktimeout-Eigenschaft ist eine der [BITS-IIS-Erweiterungs Eigenschaften](bits-iis-extension-properties.md).</span><span class="sxs-lookup"><span data-stu-id="78303-151">The BITSHostIdFallbackTimeout property is one of the [BITS IIS extension properties](bits-iis-extension-properties.md).</span></span>

<span data-ttu-id="78303-152">Der Client verwendet den Timeout Zeitraum, um zu bestimmen, wie lange versucht wird, erneut eine Verbindung mit dem im Bits-Host-ID-Header angegebenen Servernamen herzustellen, bevor auf den Hostnamen zurückgegriffen wird, der im Remote Dateinamen des Auftrags angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="78303-152">The client uses the time-out period to determine how long it tries to reconnect to the server name specified in the BITS-Host-Id header before reverting to the host name specified in the remote file name of the job.</span></span> <span data-ttu-id="78303-153">Der Timer beginnt, wenn Bits keine Verbindung mit dem Bits-Host-ID-Server herstellen kann.</span><span class="sxs-lookup"><span data-stu-id="78303-153">The timer begins when BITS is unable to connect to the BITS-Host-Id server.</span></span> <span data-ttu-id="78303-154">Der Zeitgeber wird zurückgesetzt, wenn eine Verbindung mit dem Server wieder hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="78303-154">The timer is reset when a connection to the server is restored.</span></span> <span data-ttu-id="78303-155">Wenn kein Timeout Wert angegeben wird, wird der im Remote Dateinamen angegebene Hostname nie vom Client wieder hergestellt.</span><span class="sxs-lookup"><span data-stu-id="78303-155">If a time-out period is not specified, the client never reverts to the host name specified in the remote file name.</span></span>

</dd> <dt>

<span data-ttu-id="78303-156"><span id="Accept-Encoding"></span><span id="accept-encoding"></span><span id="ACCEPT-ENCODING"></span>Accept-Encoding</span><span class="sxs-lookup"><span data-stu-id="78303-156"><span id="Accept-Encoding"></span><span id="accept-encoding"></span><span id="ACCEPT-ENCODING"></span>Accept-Encoding</span></span>
</dt> <dd>

<span data-ttu-id="78303-157">Identifiziert das Codierungsschema, das in den an den Server gesendeten Fragmenten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="78303-157">Identifies the encoding scheme to use on the fragments sent to the server.</span></span> <span data-ttu-id="78303-158">Das fragmentpaket enthält das codierte Fragment im Text des Pakets.</span><span class="sxs-lookup"><span data-stu-id="78303-158">The Fragment packet contains the encoded fragment in the body of the packet.</span></span> <span data-ttu-id="78303-159">Der BITS-Server erfordert die Identitäts Codierung (Klartext).</span><span class="sxs-lookup"><span data-stu-id="78303-159">The BITS server requires Identity encoding (plaintext).</span></span> <span data-ttu-id="78303-160">Fügen Sie diesen Header nur ein, wenn der Grund Code 200 oder 201 ist.</span><span class="sxs-lookup"><span data-stu-id="78303-160">Include this header only if the Reason-code is 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="78303-161"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Inhalts Länge</span><span class="sxs-lookup"><span data-stu-id="78303-161"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length</span></span>
</dt> <dd>

<span data-ttu-id="78303-162">Ersetzen Sie length durch die Anzahl der Bytes, die im Text der Antwort enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="78303-162">Replace length with the number of bytes included in the body of the response.</span></span> <span data-ttu-id="78303-163">Erforderlich, auch wenn der Text der Antwort keinen Inhalt enthält.</span><span class="sxs-lookup"><span data-stu-id="78303-163">Required even if the body of the response does not include content.</span></span>

</dd> <dt>

<span data-ttu-id="78303-164"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>Bits-Fehler Code</span><span class="sxs-lookup"><span data-stu-id="78303-164"><span id="BITS-Error-Code"></span><span id="bits-error-code"></span><span id="BITS-ERROR-CODE"></span>BITS-Error-Code</span></span>
</dt> <dd>

<span data-ttu-id="78303-165">Ersetzen Sie Error-Code durch eine hexadezimale Zahl, die einen HRESULT-Wert darstellt, der einem serverseitigen Fehler zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="78303-165">Replace error-code with a hexadecimal number that represents an HRESULT value associated with a server-side error.</span></span> <span data-ttu-id="78303-166">Fügen Sie diesen Header nur ein, wenn Reason-Code nicht 200 oder 201 ist.</span><span class="sxs-lookup"><span data-stu-id="78303-166">Include this header only if reason-code is not 200 or 201.</span></span>

</dd> <dt>

<span data-ttu-id="78303-167"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>Bits-Fehler-Kontext</span><span class="sxs-lookup"><span data-stu-id="78303-167"><span id="BITS-Error-Context"></span><span id="bits-error-context"></span><span id="BITS-ERROR-CONTEXT"></span>BITS-Error-Context</span></span>
</dt> <dd>

<span data-ttu-id="78303-168">Ersetzen Sie Error-Context durch eine hexadezimale Zahl, die den Kontext darstellt, in dem der Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="78303-168">Replace error-context with a hexadecimal number that represents the context in which the error occurred.</span></span> <span data-ttu-id="78303-169">Geben Sie die hexadezimale Zahl der [**\_ \_ \_ Remote \_ Datei des BG-Fehler Kontexts**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) an, wenn der Server den Fehler generiert hat.</span><span class="sxs-lookup"><span data-stu-id="78303-169">Specify the hexadecimal number for [**BG\_ERROR\_CONTEXT\_REMOTE\_FILE**](/windows/win32/api/bits/ne-bits-bg_error_context) (0x5) if the server generated the error.</span></span> <span data-ttu-id="78303-170">Andernfalls geben Sie die hexadezimale Zahl für eine **BG- \_ Fehler \_ Kontext- \_ Remote \_ Anwendung** (0x7) an, wenn der Fehler von der Anwendung generiert wurde, an die die Uploaddatei weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="78303-170">Otherwise, specify the hexadecimal number for **BG\_ERROR\_CONTEXT\_REMOTE\_APPLICATION** (0x7) if the error was generated by the application to which the upload file is passed.</span></span> <span data-ttu-id="78303-171">Fügen Sie diesen Header nur ein, wenn der Grund Code nicht 200 oder 201 ist.</span><span class="sxs-lookup"><span data-stu-id="78303-171">Include this header only if the reason-code is not 200 or 201.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="78303-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78303-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78303-173">**Create-Session**</span><span class="sxs-lookup"><span data-stu-id="78303-173">**Create-Session**</span></span>](create-session.md)
</dt> </dl>

 

 





