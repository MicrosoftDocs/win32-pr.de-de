---
Description: Dieses Thema enthält Informationen zur Verwendung des WinHTTP WinHttpRequest com-Objekts mit Skriptsprachen.
ms.assetid: 0bbbf3dc-84b8-41d8-8627-e3d80ddcb783
title: WinHttpRequest-Objekt
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/22/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- WinHttpRequest
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 907e94a731b2ec150a331347480c461d0d0fa319
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364971"
---
# <a name="winhttprequest-object"></a><span data-ttu-id="86c33-103">WinHttpRequest-Objekt</span><span class="sxs-lookup"><span data-stu-id="86c33-103">WinHttpRequest object</span></span>

<span data-ttu-id="86c33-104">Dieses Thema enthält Informationen zur Verwendung des WinHTTP **WinHttpRequest** com-Objekts mit Skriptsprachen.</span><span class="sxs-lookup"><span data-stu-id="86c33-104">This topic provides information about using the WinHTTP **WinHttpRequest** COM object with scripting languages.</span></span> <span data-ttu-id="86c33-105">Weitere Informationen, einschließlich der C++-API (WinHTTP), finden Sie unter [Informationen zu WinHTTP](about-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="86c33-105">For more information, including the C++ API (WinHTTP) please see [About WinHTTP](about-winhttp.md).</span></span> <span data-ttu-id="86c33-106">Einen Vergleich dieser Schnittstellen finden Sie unter [Auswählen einer WinHTTP-Schnittstelle](choosing-a-winhttp-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="86c33-106">See [Choosing a WinHTTP Interface](choosing-a-winhttp-interface.md) for a comparison of these interfaces.</span></span>

## <a name="example"></a><span data-ttu-id="86c33-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="86c33-107">Example</span></span>

```javascript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
```

```cpp
 IWinHttpRequest *  pIWinHttpRequest = NULL;
 \\..
    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1", &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid, NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IWinHttpRequest,
                              (void **)&pIWinHttpRequest);
    }
```

<span data-ttu-id="86c33-108">Code Beispiele, die von der [iwinhttprequest:: Status-Eigenschaft](iwinhttprequest-status.md)übernommen werden.</span><span class="sxs-lookup"><span data-stu-id="86c33-108">Code examples taken from [IWinHttpRequest::Status property](iwinhttprequest-status.md).</span></span>



## <a name="members"></a><span data-ttu-id="86c33-109">Member</span><span class="sxs-lookup"><span data-stu-id="86c33-109">Members</span></span>

<span data-ttu-id="86c33-110">Das **WinHttpRequest** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="86c33-110">The **WinHttpRequest** object has these types of members:</span></span>

-   [<span data-ttu-id="86c33-111">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="86c33-111">Events</span></span>](#events)
-   [<span data-ttu-id="86c33-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="86c33-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="86c33-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="86c33-113">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="86c33-114">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="86c33-114">Events</span></span>

<span data-ttu-id="86c33-115">Das **WinHttpRequest** -Objekt enthält diese Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="86c33-115">The **WinHttpRequest** object has these events.</span></span>



| <span data-ttu-id="86c33-116">Ereignis</span><span class="sxs-lookup"><span data-stu-id="86c33-116">Event</span></span>                                                                            | <span data-ttu-id="86c33-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="86c33-117">Description</span></span>                                                          |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="86c33-118">**OnError**</span><span class="sxs-lookup"><span data-stu-id="86c33-118">**OnError**</span></span>](iwinhttprequestevents-onerror.md)                                 | <span data-ttu-id="86c33-119">Tritt auf, wenn in der Anwendung ein Laufzeitfehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="86c33-119">Occurs when there is a run-time error in the application.</span></span><br/> |
| [<span data-ttu-id="86c33-120">**Onresponondataavailable**</span><span class="sxs-lookup"><span data-stu-id="86c33-120">**OnResponseDataAvailable**</span></span>](iwinhttprequestevents-onresponsedataavailable.md) | <span data-ttu-id="86c33-121">Tritt auf, wenn Daten aus der Antwort verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="86c33-121">Occurs when data is available from the response.</span></span><br/>          |
| [<span data-ttu-id="86c33-122">**Onresponendabgeschlossen**</span><span class="sxs-lookup"><span data-stu-id="86c33-122">**OnResponseFinished**</span></span>](iwinhttprequestevents-onresponsefinished.md)           | <span data-ttu-id="86c33-123">Tritt auf, wenn die Antwortdaten fertig sind.</span><span class="sxs-lookup"><span data-stu-id="86c33-123">Occurs when the response data is complete.</span></span><br/>                |
| [<span data-ttu-id="86c33-124">**Onresponse-Start**</span><span class="sxs-lookup"><span data-stu-id="86c33-124">**OnResponseStart**</span></span>](iwinhttprequestevents-onresponsestart.md)                 | <span data-ttu-id="86c33-125">Tritt auf, wenn die Antwortdaten empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="86c33-125">Occurs when the response data starts to be received.</span></span><br/>      |



 

### <a name="methods"></a><span data-ttu-id="86c33-126">Methoden</span><span class="sxs-lookup"><span data-stu-id="86c33-126">Methods</span></span>

<span data-ttu-id="86c33-127">Das **WinHttpRequest** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="86c33-127">The **WinHttpRequest** object has these methods.</span></span>



| <span data-ttu-id="86c33-128">Methode</span><span class="sxs-lookup"><span data-stu-id="86c33-128">Method</span></span>                                                                 | <span data-ttu-id="86c33-129">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="86c33-129">Description</span></span>                                                                                                                                                |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="86c33-130">**Abbruch**</span><span class="sxs-lookup"><span data-stu-id="86c33-130">**Abort**</span></span>](iwinhttprequest-abort.md)                                 | <span data-ttu-id="86c33-131">Bricht eine [WinHTTP](about-winhttp.md) [**Send**](iwinhttprequest-send.md) -Methode ab.</span><span class="sxs-lookup"><span data-stu-id="86c33-131">Aborts a [WinHTTP](about-winhttp.md) [**Send**](iwinhttprequest-send.md) method.</span></span><br/>                                                              |
| [<span data-ttu-id="86c33-132">**Getallresponcheaders**</span><span class="sxs-lookup"><span data-stu-id="86c33-132">**GetAllResponseHeaders**</span></span>](iwinhttprequest-getallresponseheaders.md) | <span data-ttu-id="86c33-133">Ruft alle HTTP-Antwortheader ab.</span><span class="sxs-lookup"><span data-stu-id="86c33-133">Retrieves all HTTP response headers.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="86c33-134">**Getresponsheader**</span><span class="sxs-lookup"><span data-stu-id="86c33-134">**GetResponseHeader**</span></span>](iwinhttprequest-getresponseheader.md)         | <span data-ttu-id="86c33-135">Ruft die HTTP-Antwortheader ab.</span><span class="sxs-lookup"><span data-stu-id="86c33-135">Retrieves the HTTP response headers.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="86c33-136">**Eren**</span><span class="sxs-lookup"><span data-stu-id="86c33-136">**Open**</span></span>](iwinhttprequest-open.md)                                   | <span data-ttu-id="86c33-137">Öffnet eine HTTP-Verbindung mit einer HTTP-Ressource.</span><span class="sxs-lookup"><span data-stu-id="86c33-137">Opens an HTTP connection to an HTTP resource.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="86c33-138">**Senden**</span><span class="sxs-lookup"><span data-stu-id="86c33-138">**Send**</span></span>](iwinhttprequest-send.md)                                   | <span data-ttu-id="86c33-139">Sendet eine HTTP-Anforderung an einen HTTP-Server.</span><span class="sxs-lookup"><span data-stu-id="86c33-139">Sends an HTTP request to an HTTP server.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="86c33-140">**"Abtautologonpolicy"**</span><span class="sxs-lookup"><span data-stu-id="86c33-140">**SetAutoLogonPolicy**</span></span>](iwinhttprequest-setautologonpolicy.md)       | <span data-ttu-id="86c33-141">Legt die aktuelle [Richtlinie für die automatische Anmeldung](authentication-in-winhttp.md)fest.</span><span class="sxs-lookup"><span data-stu-id="86c33-141">Sets the current [Automatic Logon Policy](authentication-in-winhttp.md).</span></span><br/>                                                |
| [<span data-ttu-id="86c33-142">**Setclientcertificate**</span><span class="sxs-lookup"><span data-stu-id="86c33-142">**SetClientCertificate**</span></span>](iwinhttprequest-setclientcertificate.md)   | <span data-ttu-id="86c33-143">Wählt ein Client Zertifikat aus, das an einen HTTPS-Server (Secure Hypertext Transfer Protocol) gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="86c33-143">Selects a client certificate to send to a Secure Hypertext Transfer Protocol (HTTPS) server.</span></span><br/>                                                    |
| [<span data-ttu-id="86c33-144">**SetCredentials**</span><span class="sxs-lookup"><span data-stu-id="86c33-144">**SetCredentials**</span></span>](iwinhttprequest-setcredentials.md)               | <span data-ttu-id="86c33-145">Legt Anmelde Informationen fest, die mit einem HTTP-Server entweder als Ursprung oder als Proxy Server verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="86c33-145">Sets credentials to be used with an HTTP server either an origin or a proxy server.</span></span><br/>                                                             |
| [<span data-ttu-id="86c33-146">**SetProxy**</span><span class="sxs-lookup"><span data-stu-id="86c33-146">**SetProxy**</span></span>](iwinhttprequest-setproxy.md)                           | <span data-ttu-id="86c33-147">Legt Proxy Server Informationen fest.</span><span class="sxs-lookup"><span data-stu-id="86c33-147">Sets proxy server information.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="86c33-148">**"Ltrequestheader"**</span><span class="sxs-lookup"><span data-stu-id="86c33-148">**SetRequestHeader**</span></span>](iwinhttprequest-setrequestheader.md)           | <span data-ttu-id="86c33-149">Fügt einen HTTP-Anforderungs Header hinzu, ändert oder löscht ihn.</span><span class="sxs-lookup"><span data-stu-id="86c33-149">Adds, changes, or deletes an HTTP request header.</span></span><br/>                                                                                               |
| [<span data-ttu-id="86c33-150">**Settimeouts**</span><span class="sxs-lookup"><span data-stu-id="86c33-150">**SetTimeouts**</span></span>](iwinhttprequest-settimeouts.md)                     | <span data-ttu-id="86c33-151">Gibt die einzelnen Timeout Komponenten eines Sende-/empfangvorgangs in Millisekunden an.</span><span class="sxs-lookup"><span data-stu-id="86c33-151">Specifies, in milliseconds, the individual time-out components of a send/receive operation.</span></span><br/>                                                     |
| [<span data-ttu-id="86c33-152">**WaitForResponse**</span><span class="sxs-lookup"><span data-stu-id="86c33-152">**WaitForResponse**</span></span>](iwinhttprequest-waitforresponse.md)             | <span data-ttu-id="86c33-153">Gibt die Wartezeit (in Sekunden) für die Ausführung einer asynchronen [**Sende**](iwinhttprequest-send.md) Methode mit optionalem Timeout Wert an.</span><span class="sxs-lookup"><span data-stu-id="86c33-153">Specifies the wait time, in seconds, for an asynchronous [**Send**](iwinhttprequest-send.md) method to complete, with optional time-out value.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="86c33-154">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="86c33-154">Properties</span></span>

<span data-ttu-id="86c33-155">Das **WinHttpRequest** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="86c33-155">The **WinHttpRequest** object has these properties.</span></span>



| <span data-ttu-id="86c33-156">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="86c33-156">Property</span></span>                                                            | <span data-ttu-id="86c33-157">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="86c33-157">Access type</span></span>           | <span data-ttu-id="86c33-158">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="86c33-158">Description</span></span>                                                                     |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="86c33-159">**Option**</span><span class="sxs-lookup"><span data-stu-id="86c33-159">**Option**</span></span>](iwinhttprequest-option.md)<br/>                 | <span data-ttu-id="86c33-160">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="86c33-160">Read/write</span></span><br/> | <span data-ttu-id="86c33-161">Legt einen WinHTTP-Optionswert fest oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="86c33-161">Sets or retrieves a WinHTTP option value.</span></span><br/>                            |
| [<span data-ttu-id="86c33-162">**Response Body**</span><span class="sxs-lookup"><span data-stu-id="86c33-162">**ResponseBody**</span></span>](iwinhttprequest-responsebody.md)<br/>     | <span data-ttu-id="86c33-163">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="86c33-163">Read-only</span></span><br/>  | <span data-ttu-id="86c33-164">Ruft den Entitäts Text der Antwort als Array nicht signierter Bytes ab.</span><span class="sxs-lookup"><span data-stu-id="86c33-164">Retrieves the response entity body as an array of unsigned bytes.</span></span><br/>    |
| [<span data-ttu-id="86c33-165">**ResponseStream**</span><span class="sxs-lookup"><span data-stu-id="86c33-165">**ResponseStream**</span></span>](iwinhttprequest-responsestream.md)<br/> | <span data-ttu-id="86c33-166">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="86c33-166">Read-only</span></span><br/>  | <span data-ttu-id="86c33-167">Ruft den Entitäts Text der Antwort als [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)ab.</span><span class="sxs-lookup"><span data-stu-id="86c33-167">Retrieves the response entity body as an [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span></span><br/> |
| [<span data-ttu-id="86c33-168">**Response Text**</span><span class="sxs-lookup"><span data-stu-id="86c33-168">**ResponseText**</span></span>](iwinhttprequest-responsetext.md)<br/>     | <span data-ttu-id="86c33-169">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="86c33-169">Read-only</span></span><br/>  | <span data-ttu-id="86c33-170">Ruft den Text der Antwort Entität als Text ab.</span><span class="sxs-lookup"><span data-stu-id="86c33-170">Retrieves the response entity body as text.</span></span><br/>                          |
| [<span data-ttu-id="86c33-171">**Status**</span><span class="sxs-lookup"><span data-stu-id="86c33-171">**Status**</span></span>](iwinhttprequest-status.md)<br/>                 | <span data-ttu-id="86c33-172">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="86c33-172">Read-only</span></span><br/>  | <span data-ttu-id="86c33-173">Ruft den HTTP-Statuscode von der letzten Antwort ab.</span><span class="sxs-lookup"><span data-stu-id="86c33-173">Retrieves the HTTP status code from the last response.</span></span><br/>               |
| [<span data-ttu-id="86c33-174">**StatusText**</span><span class="sxs-lookup"><span data-stu-id="86c33-174">**StatusText**</span></span>](iwinhttprequest-statustext.md)<br/>         | <span data-ttu-id="86c33-175">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="86c33-175">Read-only</span></span><br/>  | <span data-ttu-id="86c33-176">Ruft den HTTP-Status Text ab.</span><span class="sxs-lookup"><span data-stu-id="86c33-176">Retrieves HTTP status text.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="86c33-177">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="86c33-177">Remarks</span></span>

<span data-ttu-id="86c33-178">Das **WinHttpRequest** -Objekt verwendet die [**IErrorInfo**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ierrorinfo) -Schnittstelle zum Bereitstellen von Fehler Daten.</span><span class="sxs-lookup"><span data-stu-id="86c33-178">The **WinHttpRequest** object uses the [**IErrorInfo**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ierrorinfo) interface to provide error data.</span></span> <span data-ttu-id="86c33-179">Eine Beschreibung und ein numerischer Fehlerwert können mit dem [Err](/previous-versions//sbf5ze0e(v=vs.85)) -Objekt in Microsoft Visual Basic Scripting Edition (VBScript) und dem [Error](https://msdn.microsoft.com/library/dww52sbt.aspx) -Objekt in Microsoft JScript abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="86c33-179">A description and numerical error value can be obtained with the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object in Microsoft Visual Basic Scripting Edition (VBScript), and the [Error](https://msdn.microsoft.com/library/dww52sbt.aspx) object in Microsoft JScript.</span></span> <span data-ttu-id="86c33-180">Die unteren 16 Bits einer Fehlernummer entsprechen den Werten, die in [**Fehlermeldungen**](error-messages.md)gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="86c33-180">The lower 16 bits of an error number correspond to the values found in [**Error Messages**](error-messages.md).</span></span>

> [!Note]  
> <span data-ttu-id="86c33-181">Informationen zu Windows XP und Windows 2000 finden Sie unter [Lauf Zeitanforderungen](winhttp-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="86c33-181">For Windows XP and Windows 2000, see [Run-Time Requirements](winhttp-start-page.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="86c33-182">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="86c33-182">Requirements</span></span>



| <span data-ttu-id="86c33-183">Anforderung</span><span class="sxs-lookup"><span data-stu-id="86c33-183">Requirement</span></span> | <span data-ttu-id="86c33-184">Wert</span><span class="sxs-lookup"><span data-stu-id="86c33-184">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="86c33-185">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="86c33-185">Minimum supported client</span></span><br/> | <span data-ttu-id="86c33-186">Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="86c33-186">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="86c33-187">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="86c33-187">Minimum supported server</span></span><br/> | <span data-ttu-id="86c33-188">Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="86c33-188">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="86c33-189">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="86c33-189">Redistributable</span></span><br/>          | <span data-ttu-id="86c33-190">WinHTTP 5,0 und Internet Explorer 5,01 oder höher unter Windows XP und Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="86c33-190">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="86c33-191">IDL</span><span class="sxs-lookup"><span data-stu-id="86c33-191">IDL</span></span><br/>                      | <dl> <span data-ttu-id="86c33-192"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="86c33-192"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="86c33-193">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="86c33-193">Library</span></span><br/>                  | <dl> <span data-ttu-id="86c33-194"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="86c33-194"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="86c33-195">DLL</span><span class="sxs-lookup"><span data-stu-id="86c33-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86c33-196"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86c33-196"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="86c33-197">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="86c33-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86c33-198">WinHTTP-Versionen</span><span class="sxs-lookup"><span data-stu-id="86c33-198">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

