---
description: Die iwinhttprequest-Schnittstelle stellt alle nichtereignis Methoden für Microsoft Windows HTTP-Dienste (WinHTTP) bereit.
ms.assetid: 6417b3b5-b74a-4c7b-acf9-87e2e814a4df
title: Iwinhttprequest-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 77ebc8947ad36d2dc9efba121cdd6da2d6de359b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216328"
---
# <a name="iwinhttprequest-interface"></a><span data-ttu-id="8747c-103">Iwinhttprequest-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="8747c-103">IWinHttpRequest interface</span></span>

<span data-ttu-id="8747c-104">Die **iwinhttprequest** -Schnittstelle stellt alle nichtereignis Methoden für [Microsoft Windows HTTP-Dienste (WinHTTP)](about-winhttp.md)bereit.</span><span class="sxs-lookup"><span data-stu-id="8747c-104">The **IWinHttpRequest** interface provides all of the nonevent methods for [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md).</span></span>

## <a name="members"></a><span data-ttu-id="8747c-105">Member</span><span class="sxs-lookup"><span data-stu-id="8747c-105">Members</span></span>

<span data-ttu-id="8747c-106">Die **iwinhttprequest** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="8747c-106">The **IWinHttpRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8747c-107">**Iwinhttprequest** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="8747c-107">**IWinHttpRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="8747c-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="8747c-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="8747c-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8747c-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8747c-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="8747c-110">Methods</span></span>

<span data-ttu-id="8747c-111">Die **iwinhttprequest** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="8747c-111">The **IWinHttpRequest** interface has these methods.</span></span>



| <span data-ttu-id="8747c-112">Methode</span><span class="sxs-lookup"><span data-stu-id="8747c-112">Method</span></span>                                                                 | <span data-ttu-id="8747c-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8747c-113">Description</span></span>                                                                                                                             |
|:-----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8747c-114">**Abbruch**</span><span class="sxs-lookup"><span data-stu-id="8747c-114">**Abort**</span></span>](iwinhttprequest-abort.md)                                 | <span data-ttu-id="8747c-115">Bricht eine [WinHTTP](about-winhttp.md) [**Send**](iwinhttprequest-send.md) -Methode ab.</span><span class="sxs-lookup"><span data-stu-id="8747c-115">Aborts a [WinHTTP](about-winhttp.md) [**Send**](iwinhttprequest-send.md) method.</span></span><br/>                                           |
| [<span data-ttu-id="8747c-116">**Getallresponcheaders**</span><span class="sxs-lookup"><span data-stu-id="8747c-116">**GetAllResponseHeaders**</span></span>](iwinhttprequest-getallresponseheaders.md) | <span data-ttu-id="8747c-117">Ruft alle HTTP-Antwortheader ab.</span><span class="sxs-lookup"><span data-stu-id="8747c-117">Retrieves all HTTP response headers.</span></span><br/>                                                                                         |
| [<span data-ttu-id="8747c-118">**Getresponsheader**</span><span class="sxs-lookup"><span data-stu-id="8747c-118">**GetResponseHeader**</span></span>](iwinhttprequest-getresponseheader.md)         | <span data-ttu-id="8747c-119">Ruft die HTTP-Antwortheader ab.</span><span class="sxs-lookup"><span data-stu-id="8747c-119">Retrieves the HTTP response headers.</span></span><br/>                                                                                         |
| [<span data-ttu-id="8747c-120">**Eren**</span><span class="sxs-lookup"><span data-stu-id="8747c-120">**Open**</span></span>](iwinhttprequest-open.md)                                   | <span data-ttu-id="8747c-121">Öffnet eine HTTP-Verbindung mit einer HTTP-Ressource.</span><span class="sxs-lookup"><span data-stu-id="8747c-121">Opens an HTTP connection to an HTTP resource.</span></span><br/>                                                                                |
| [<span data-ttu-id="8747c-122">**Senden**</span><span class="sxs-lookup"><span data-stu-id="8747c-122">**Send**</span></span>](iwinhttprequest-send.md)                                   | <span data-ttu-id="8747c-123">Sendet eine HTTP-Anforderung an einen HTTP-Server.</span><span class="sxs-lookup"><span data-stu-id="8747c-123">Sends an HTTP request to an HTTP server.</span></span><br/>                                                                                     |
| [<span data-ttu-id="8747c-124">**"Abtautologonpolicy"**</span><span class="sxs-lookup"><span data-stu-id="8747c-124">**SetAutoLogonPolicy**</span></span>](iwinhttprequest-setautologonpolicy.md)       | <span data-ttu-id="8747c-125">Legt die aktuelle [Richtlinie für die automatische Anmeldung](authentication-in-winhttp.md)fest.</span><span class="sxs-lookup"><span data-stu-id="8747c-125">Sets the current [Automatic Logon Policy](authentication-in-winhttp.md).</span></span><br/>                             |
| [<span data-ttu-id="8747c-126">**Setclientcertificate**</span><span class="sxs-lookup"><span data-stu-id="8747c-126">**SetClientCertificate**</span></span>](iwinhttprequest-setclientcertificate.md)   | <span data-ttu-id="8747c-127">Wählt ein Client Zertifikat aus, das an einen HTTPS-Server (Secure Hypertext Transfer Protocol) gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8747c-127">Selects a client certificate to send to a Secure Hypertext Transfer Protocol (HTTPS) server.</span></span><br/>                                 |
| [<span data-ttu-id="8747c-128">**SetCredentials**</span><span class="sxs-lookup"><span data-stu-id="8747c-128">**SetCredentials**</span></span>](iwinhttprequest-setcredentials.md)               | <span data-ttu-id="8747c-129">Legt Anmelde Informationen für die Verwendung mit einem HTTP-Server fest, entweder einen Proxy Server oder einen ursprünglichen Server.</span><span class="sxs-lookup"><span data-stu-id="8747c-129">Sets credentials to be used with an HTTP server, either a proxy server or an originating server.</span></span><br/>                             |
| [<span data-ttu-id="8747c-130">**SetProxy**</span><span class="sxs-lookup"><span data-stu-id="8747c-130">**SetProxy**</span></span>](iwinhttprequest-setproxy.md)                           | <span data-ttu-id="8747c-131">Legt Proxy Server Informationen fest.</span><span class="sxs-lookup"><span data-stu-id="8747c-131">Sets proxy server information.</span></span><br/>                                                                                               |
| [<span data-ttu-id="8747c-132">**"Ltrequestheader"**</span><span class="sxs-lookup"><span data-stu-id="8747c-132">**SetRequestHeader**</span></span>](iwinhttprequest-setrequestheader.md)           | <span data-ttu-id="8747c-133">Fügt einen HTTP-Anforderungs Header hinzu, ändert oder löscht ihn.</span><span class="sxs-lookup"><span data-stu-id="8747c-133">Adds, changes, or deletes an HTTP request header.</span></span><br/>                                                                            |
| [<span data-ttu-id="8747c-134">**Settimeouts**</span><span class="sxs-lookup"><span data-stu-id="8747c-134">**SetTimeouts**</span></span>](iwinhttprequest-settimeouts.md)                     | <span data-ttu-id="8747c-135">Gibt die einzelnen Timeout Komponenten eines Sende-/Empfangsvorgangs in Millisekunden an.</span><span class="sxs-lookup"><span data-stu-id="8747c-135">Specifies the individual time-out components of a send/receive operation, in milliseconds.</span></span><br/>                                   |
| [<span data-ttu-id="8747c-136">**WaitForResponse**</span><span class="sxs-lookup"><span data-stu-id="8747c-136">**WaitForResponse**</span></span>](iwinhttprequest-waitforresponse.md)             | <span data-ttu-id="8747c-137">Wartet auf den Abschluss einer asynchronen [**Sende**](iwinhttprequest-send.md) Methode (mit optionalem Timeout Wert) in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="8747c-137">Waits for an asynchronous [**Send**](iwinhttprequest-send.md) method to complete, with optional time-out value, in seconds.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8747c-138">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8747c-138">Properties</span></span>

<span data-ttu-id="8747c-139">Die **iwinhttprequest** -Schnittstelle verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8747c-139">The **IWinHttpRequest** interface has these properties.</span></span>



| <span data-ttu-id="8747c-140">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8747c-140">Property</span></span>                                                            | <span data-ttu-id="8747c-141">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="8747c-141">Access type</span></span>           | <span data-ttu-id="8747c-142">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8747c-142">Description</span></span>                                                           |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="8747c-143">**Option**</span><span class="sxs-lookup"><span data-stu-id="8747c-143">**Option**</span></span>](iwinhttprequest-option.md)<br/>                 | <span data-ttu-id="8747c-144">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8747c-144">Read/write</span></span><br/> | <span data-ttu-id="8747c-145">Ein WinHTTP-Optionswert.</span><span class="sxs-lookup"><span data-stu-id="8747c-145">A WinHTTP option value.</span></span><br/>                                    |
| [<span data-ttu-id="8747c-146">**Response Body**</span><span class="sxs-lookup"><span data-stu-id="8747c-146">**ResponseBody**</span></span>](iwinhttprequest-responsebody.md)<br/>     | <span data-ttu-id="8747c-147">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8747c-147">Read-only</span></span><br/>  | <span data-ttu-id="8747c-148">Der Antwort Entitäts Text als Array nicht signierter bytes.</span><span class="sxs-lookup"><span data-stu-id="8747c-148">The response entity body as an array of unsigned bytes.</span></span><br/>    |
| [<span data-ttu-id="8747c-149">**ResponseStream**</span><span class="sxs-lookup"><span data-stu-id="8747c-149">**ResponseStream**</span></span>](iwinhttprequest-responsestream.md)<br/> | <span data-ttu-id="8747c-150">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8747c-150">Read-only</span></span><br/>  | <span data-ttu-id="8747c-151">Der Antwort Entitäts Text als [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span><span class="sxs-lookup"><span data-stu-id="8747c-151">The response entity body as an [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span></span><br/> |
| [<span data-ttu-id="8747c-152">**Response Text**</span><span class="sxs-lookup"><span data-stu-id="8747c-152">**ResponseText**</span></span>](iwinhttprequest-responsetext.md)<br/>     | <span data-ttu-id="8747c-153">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8747c-153">Read-only</span></span><br/>  | <span data-ttu-id="8747c-154">Der Antwort Entitäts Text.</span><span class="sxs-lookup"><span data-stu-id="8747c-154">The response entity body.</span></span><br/>                                  |
| [<span data-ttu-id="8747c-155">**Status**</span><span class="sxs-lookup"><span data-stu-id="8747c-155">**Status**</span></span>](iwinhttprequest-status.md)<br/>                 | <span data-ttu-id="8747c-156">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8747c-156">Read-only</span></span><br/>  | <span data-ttu-id="8747c-157">Der HTTP-Statuscode der letzten Antwort.</span><span class="sxs-lookup"><span data-stu-id="8747c-157">The HTTP status code from the last response.</span></span><br/>               |
| [<span data-ttu-id="8747c-158">**StatusText**</span><span class="sxs-lookup"><span data-stu-id="8747c-158">**StatusText**</span></span>](iwinhttprequest-statustext.md)<br/>         | <span data-ttu-id="8747c-159">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8747c-159">Read-only</span></span><br/>  | <span data-ttu-id="8747c-160">Der HTTP-Status Text.</span><span class="sxs-lookup"><span data-stu-id="8747c-160">The HTTP status text.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="8747c-161">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8747c-161">Remarks</span></span>

<span data-ttu-id="8747c-162">Die in HttpRequest. idl definierte **iwinhttprequest** -Schnittstelle wird von einer Klasse mit der ID **CLSID \_ WinHttpRequest** implementiert.</span><span class="sxs-lookup"><span data-stu-id="8747c-162">The **IWinHttpRequest** interface defined in httprequest.idl is implemented by a class with id of **CLSID\_WinHttpRequest**.</span></span> <span data-ttu-id="8747c-163">Eine Anwendung ruft diese Schnittstelle durch Aufrufen von [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) mit der Klassen-ID **CLSID \_ WinHttpRequest** und der Schnittstellen-ID **\_ IID iwinhttprequest** ab.</span><span class="sxs-lookup"><span data-stu-id="8747c-163">An application obtain this interface by calling [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) with a class id of **CLSID\_WinHttpRequest** and an interface id of **IID\_IWinHttpRequest**.</span></span>

> [!Note]  
> <span data-ttu-id="8747c-164">Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Lauf Zeitanforderungen](winhttp-start-page.md) auf der WinHTTP-Startseite.</span><span class="sxs-lookup"><span data-stu-id="8747c-164">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8747c-165">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8747c-165">Requirements</span></span>



| <span data-ttu-id="8747c-166">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8747c-166">Requirement</span></span> | <span data-ttu-id="8747c-167">Wert</span><span class="sxs-lookup"><span data-stu-id="8747c-167">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="8747c-168">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8747c-168">Minimum supported client</span></span><br/> | <span data-ttu-id="8747c-169">Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8747c-169">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="8747c-170">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8747c-170">Minimum supported server</span></span><br/> | <span data-ttu-id="8747c-171">Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8747c-171">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="8747c-172">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="8747c-172">Redistributable</span></span><br/>          | <span data-ttu-id="8747c-173">WinHTTP 5,0 und Internet Explorer 5,01 oder höher unter Windows XP und Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="8747c-173">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="8747c-174">IDL</span><span class="sxs-lookup"><span data-stu-id="8747c-174">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8747c-175"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8747c-175"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="8747c-176">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8747c-176">Library</span></span><br/>                  | <dl> <span data-ttu-id="8747c-177"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8747c-177"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="8747c-178">DLL</span><span class="sxs-lookup"><span data-stu-id="8747c-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8747c-179"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8747c-179"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8747c-180">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8747c-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8747c-181">**Iwinhttprequestevents**</span><span class="sxs-lookup"><span data-stu-id="8747c-181">**IWinHttpRequestEvents**</span></span>](iwinhttprequestevents-interface.md)
</dt> <dt>

[<span data-ttu-id="8747c-182">WinHTTP-Versionen</span><span class="sxs-lookup"><span data-stu-id="8747c-182">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

