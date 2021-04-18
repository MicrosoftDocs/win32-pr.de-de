---
description: Stellt Ereignisse für Microsoft Windows HTTP-Dienste (WinHTTP) bereit.
ms.assetid: 0721d7f9-2e84-41a9-be52-89c8d638eb90
title: Iwinhttprequestevents-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequestEvents
api_type:
- COM
api_location:
- HttpRequest.idl
ms.openlocfilehash: 3cdd0bf10c0d4bd75351ddaab6e88ce7182850fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350865"
---
# <a name="iwinhttprequestevents-interface"></a><span data-ttu-id="79884-103">Iwinhttprequestevents-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="79884-103">IWinHttpRequestEvents interface</span></span>

<span data-ttu-id="79884-104">Die **iwinhttprequestevents** -Schnittstelle stellt Ereignisse für [Microsoft Windows HTTP-Dienste (WinHTTP)](about-winhttp.md)bereit.</span><span class="sxs-lookup"><span data-stu-id="79884-104">The **IWinHttpRequestEvents** interface provides events for [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md).</span></span> <span data-ttu-id="79884-105">Es werden nur Ereignis Methoden verwendet.</span><span class="sxs-lookup"><span data-stu-id="79884-105">It uses only event methods.</span></span>

## <a name="members"></a><span data-ttu-id="79884-106">Member</span><span class="sxs-lookup"><span data-stu-id="79884-106">Members</span></span>

<span data-ttu-id="79884-107">Die **iwinhttprequestevents** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="79884-107">The **IWinHttpRequestEvents** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="79884-108">**Iwinhttprequestevents** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="79884-108">**IWinHttpRequestEvents** also has these types of members:</span></span>

-   [<span data-ttu-id="79884-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="79884-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="79884-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="79884-110">Methods</span></span>

<span data-ttu-id="79884-111">Die **iwinhttprequestevents** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="79884-111">The **IWinHttpRequestEvents** interface has these methods.</span></span>



| <span data-ttu-id="79884-112">Methode</span><span class="sxs-lookup"><span data-stu-id="79884-112">Method</span></span>                                                                           | <span data-ttu-id="79884-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="79884-113">Description</span></span>                                                          |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="79884-114">**OnError**</span><span class="sxs-lookup"><span data-stu-id="79884-114">**OnError**</span></span>](iwinhttprequestevents-onerror.md)                                 | <span data-ttu-id="79884-115">Tritt auf, wenn in der Anwendung ein Laufzeitfehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="79884-115">Occurs when there is a run-time error in the application.</span></span><br/> |
| [<span data-ttu-id="79884-116">**Onresponondataavailable**</span><span class="sxs-lookup"><span data-stu-id="79884-116">**OnResponseDataAvailable**</span></span>](iwinhttprequestevents-onresponsedataavailable.md) | <span data-ttu-id="79884-117">Tritt auf, wenn Daten aus der Antwort verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="79884-117">Occurs when data is available from the response.</span></span><br/>          |
| [<span data-ttu-id="79884-118">**Onresponendabgeschlossen**</span><span class="sxs-lookup"><span data-stu-id="79884-118">**OnResponseFinished**</span></span>](iwinhttprequestevents-onresponsefinished.md)           | <span data-ttu-id="79884-119">Tritt auf, wenn die Antwortdaten fertig sind.</span><span class="sxs-lookup"><span data-stu-id="79884-119">Occurs when the response data is complete.</span></span><br/>                |
| [<span data-ttu-id="79884-120">**Onresponse-Start**</span><span class="sxs-lookup"><span data-stu-id="79884-120">**OnResponseStart**</span></span>](iwinhttprequestevents-onresponsestart.md)                 | <span data-ttu-id="79884-121">Tritt auf, wenn die Antwortdaten empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="79884-121">Occurs when the response data starts to be received.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="79884-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="79884-122">Remarks</span></span>

<span data-ttu-id="79884-123">Im folgenden Verfahren wird beschrieben, wie Sie sich für Benachrichtigungen registrieren.</span><span class="sxs-lookup"><span data-stu-id="79884-123">The following procedure describes how to register for notifications.</span></span>

1.  <span data-ttu-id="79884-124">Rufen Sie eine [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) -Schnittstelle ab, indem Sie **QueryInterface** für ein [**iwinhttprequest**](iwinhttprequest-interface.md) -Objekt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="79884-124">Get an [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) interface by calling **QueryInterface** on an [**IWinHttpRequest**](iwinhttprequest-interface.md) object.</span></span>
2.  <span data-ttu-id="79884-125">Rufen Sie [FindConnectionPoint](/windows/win32/api/ocidl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint) für die zurückgegebene Schnittstelle auf, und übergeben Sie **IID \_ iwinhttprequestevents** an *riid*.</span><span class="sxs-lookup"><span data-stu-id="79884-125">Call [FindConnectionPoint](/windows/win32/api/ocidl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint) on the returned interface and pass **IID\_IWinHttpRequestEvents** to *riid*.</span></span>
3.  <span data-ttu-id="79884-126">Rufen Sie die [Empfehlung](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) auf dem zurückgegebenen Verbindungspunkt auf, und übergeben Sie einen Zeiger auf eine **IUnknown** -Schnittstelle für ein Objekt, das **iwinhttprequestevents** zu *Punk* implementiert.</span><span class="sxs-lookup"><span data-stu-id="79884-126">Call [Advise](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) on the returned connection point and pass a pointer to an **IUnknown** interface on an object that implements **IWinHttpRequestEvents** to *pUnk*.</span></span>

<span data-ttu-id="79884-127">Benachrichtigungen können beendet werden, indem Sie [Unrat](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-unadvise) für den Verbindungspunkt aufrufen, der in Schritt 2 zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="79884-127">Notifications can be terminated by calling [Unadvise](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-unadvise) on the connection point returned in step 2.</span></span>

<span data-ttu-id="79884-128">Informationen zum Anzeigen von Code, der für com-Benachrichtigungen registriert wird, finden Sie im Abschnitt Client des Artikels [com-Verbindungspunkte](/archive/msdn-magazine/2007/september/clr-inside-out-com-connection-points) .</span><span class="sxs-lookup"><span data-stu-id="79884-128">To view some code that registers for COM notifications, see the Client section of the [COM Connection Points](/archive/msdn-magazine/2007/september/clr-inside-out-com-connection-points) article.</span></span>

> [!Note]  
> <span data-ttu-id="79884-129">Informationen zu Windows XP und Windows 2000 finden Sie im Abschnitt [Lauf Zeitanforderungen](winhttp-start-page.md) auf der WinHTTP-Start Seite.</span><span class="sxs-lookup"><span data-stu-id="79884-129">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="79884-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79884-130">Requirements</span></span>



| <span data-ttu-id="79884-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="79884-131">Requirement</span></span> | <span data-ttu-id="79884-132">Wert</span><span class="sxs-lookup"><span data-stu-id="79884-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="79884-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="79884-133">Minimum supported client</span></span><br/> | <span data-ttu-id="79884-134">Windows XP, Windows 2000 Professional mit SP3 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="79884-134">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="79884-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="79884-135">Minimum supported server</span></span><br/> | <span data-ttu-id="79884-136">Windows Server 2003, Windows 2000-Server mit \[ nur SP3-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="79884-136">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="79884-137">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="79884-137">Redistributable</span></span><br/>          | <span data-ttu-id="79884-138">WinHTTP 5,0 und Internet Explorer 5,01 oder höher unter Windows XP und Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="79884-138">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="79884-139">IDL</span><span class="sxs-lookup"><span data-stu-id="79884-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="79884-140"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="79884-140"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79884-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79884-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79884-142">**Iwinhttprequest**</span><span class="sxs-lookup"><span data-stu-id="79884-142">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="79884-143">WinHTTP-Versionen</span><span class="sxs-lookup"><span data-stu-id="79884-143">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

