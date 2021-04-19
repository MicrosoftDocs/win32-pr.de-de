---
description: Die TAPI- \_ linienproxyrequest-Nachricht übermittelt eine Anforderung an einen registrierten Proxy Funktions Handler.
ms.assetid: 7f33de55-2482-4558-bd86-ee2ac1e31269
title: LINE_PROXYREQUEST Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d536e85a9c773626bb5aacc4745d9d82817fe3c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373758"
---
# <a name="line_proxyrequest-message"></a><span data-ttu-id="bc803-103">Zeile \_ proxyrequest-Nachricht</span><span class="sxs-lookup"><span data-stu-id="bc803-103">LINE\_PROXYREQUEST message</span></span>

<span data-ttu-id="bc803-104">Die TAPI **- \_ linienproxyrequest** -Nachricht übermittelt eine Anforderung an einen registrierten Proxy Funktions Handler.</span><span class="sxs-lookup"><span data-stu-id="bc803-104">The TAPI **LINE\_PROXYREQUEST** message delivers a request to a registered proxy function handler.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="bc803-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc803-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc803-106">*hdevice*</span><span class="sxs-lookup"><span data-stu-id="bc803-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="bc803-107">Das Handle der Anwendung für das liniengerät, auf dem sich der Agentstatus geändert hat.</span><span class="sxs-lookup"><span data-stu-id="bc803-107">The application's handle to the line device on which the agent status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="bc803-108">*dwcallbackinstance*</span><span class="sxs-lookup"><span data-stu-id="bc803-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="bc803-109">Die beim Öffnen der Zeile des Aufrufs angegebene Rückruf Instanz.</span><span class="sxs-lookup"><span data-stu-id="bc803-109">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="bc803-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="bc803-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="bc803-111">Zeiger auf eine [**lineproxyrequest**](/windows/desktop/api/Tapi/ns-tapi-lineproxyrequest) -Struktur, die die Anforderung enthält, die von der proxyhandleranwendung verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="bc803-111">Pointer to a [**LINEPROXYREQUEST**](/windows/desktop/api/Tapi/ns-tapi-lineproxyrequest) structure containing the request to be processed by the proxy handler application.</span></span>

</dd> <dt>

<span data-ttu-id="bc803-112">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="bc803-112">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="bc803-113">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="bc803-113">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="bc803-114">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="bc803-114">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="bc803-115">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="bc803-115">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc803-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bc803-116">Return value</span></span>

<span data-ttu-id="bc803-117">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="bc803-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc803-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc803-118">Remarks</span></span>

<span data-ttu-id="bc803-119">Die **Zeile \_ proxyrequest** -Nachricht wird nur an die erste Anwendung gesendet, die für die Verarbeitung von Proxy Anforderungen des übermittelten Typs registriert ist.</span><span class="sxs-lookup"><span data-stu-id="bc803-119">The **LINE\_PROXYREQUEST** message is sent only to the first application that registered to handle proxy requests of the type being delivered.</span></span>

<span data-ttu-id="bc803-120">Die Anwendung sollte die im Proxy Puffer enthaltene Anforderung verarbeiten und [**lineproxyresponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) anrufen, um Daten zurückzugeben oder Ergebnisse zu liefern.</span><span class="sxs-lookup"><span data-stu-id="bc803-120">The application should process the request contained in the proxy buffer and call [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) to return data or deliver results.</span></span> <span data-ttu-id="bc803-121">Die Verarbeitung der Anforderung sollte nur im Kontext der TAPI-Rückruffunktion der Anwendung erfolgen, wenn Sie sofort ausgeführt werden kann, ohne auf eine Antwort von einer anderen Entität zu warten.</span><span class="sxs-lookup"><span data-stu-id="bc803-121">Processing of the request should be done within the context of the application's TAPI callback function only if it can be performed immediately, without waiting for response from any other entity.</span></span> <span data-ttu-id="bc803-122">Wenn die Anwendung mit anderen Entitäten kommunizieren muss (z. b. ein Dienstanbieter zur Handhabung der PBX-basierten ACD oder eines beliebigen anderen System Dienstanbieters, der zu Blockierungen führen kann), sollte die Anforderung in der Anwendung in die Warteschlange eingereiht werden, und die Rückruffunktion wird beendet, um zu vermeiden, dass weitere TAPI-Nachrichten von der Anwendung verzögert werden</span><span class="sxs-lookup"><span data-stu-id="bc803-122">If the application needs to communicate with other entities (for example, a service provider to handle PBX-based ACD, or any other system service which might result in blocking), then the request should be queued within the application and the callback function exited to avoid delaying the receipt of further TAPI messages by the application.</span></span>

<span data-ttu-id="bc803-123">Zum Zeitpunkt, an dem die **Zeile \_ proxyrequest** an den Proxy Handler übermittelt wird, hat TAPI bereits ein positives Ergebnis der *dwrequestid-* Funktion an die ursprüngliche Anwendung zurückgegeben und die Blockierung des aufrufenden Threads aufgehoben, um die Ausführung fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="bc803-123">At the time the **LINE\_PROXYREQUEST** is delivered to the proxy handler, TAPI has already returned a positive *dwRequestID* function result to the original application and unblocked the calling thread to continue execution.</span></span> <span data-ttu-id="bc803-124">Die Anwendung wartet auf eine [**Zeilen \_ Antwort**](line-reply.md) Nachricht, die automatisch generiert wird, wenn die Proxy Handler-Anwendung [**lineproxyresponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse)aufruft.</span><span class="sxs-lookup"><span data-stu-id="bc803-124">The application is awaiting a [**LINE\_REPLY**](line-reply.md) message, which is automatically generated when the proxy handler application calls [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse).</span></span>

<span data-ttu-id="bc803-125">Die Anwendung darf den Speicher, auf den von *lpproxyrequest* verwiesen wird, nicht freigeben.</span><span class="sxs-lookup"><span data-stu-id="bc803-125">The application shall not free the memory pointed to by *lpProxyRequest*.</span></span> <span data-ttu-id="bc803-126">TAPI gibt den Arbeitsspeicher während der Ausführung von [**lineproxyresponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse)frei.</span><span class="sxs-lookup"><span data-stu-id="bc803-126">TAPI frees the memory during the execution of [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse).</span></span> <span data-ttu-id="bc803-127">Die Anwendung kann [**lineproxyresponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) für jede **Zeile \_ proxyrequest** -Nachricht genau einmal aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="bc803-127">The application can call [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) exactly once for each **LINE\_PROXYREQUEST** message.</span></span>

<span data-ttu-id="bc803-128">Wenn die Anwendung eine Nachricht [**zum \_ Schließen**](line-close.md) der Nachricht empfängt, während Sie ausstehende Proxy Anforderungen hat, sollte Sie [**lineproxyresponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) für jede ausstehende Anforderung abrufen und einen entsprechenden *dwresult* -Wert übergeben (z \_ . b. lineerr operationfailed).</span><span class="sxs-lookup"><span data-stu-id="bc803-128">If the application receives a [**LINE\_CLOSE**](line-close.md) message while it has pending proxy requests, it should call [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) for each pending request, passing in an appropriate *dwResult* value (such as LINEERR\_OPERATIONFAILED).</span></span>

## <a name="requirements"></a><span data-ttu-id="bc803-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc803-129">Requirements</span></span>



| <span data-ttu-id="bc803-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc803-130">Requirement</span></span> | <span data-ttu-id="bc803-131">Wert</span><span class="sxs-lookup"><span data-stu-id="bc803-131">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="bc803-132">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="bc803-132">TAPI version</span></span><br/> | <span data-ttu-id="bc803-133">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="bc803-133">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="bc803-134">Header</span><span class="sxs-lookup"><span data-stu-id="bc803-134">Header</span></span><br/>       | <dl> <span data-ttu-id="bc803-135"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc803-135"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc803-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc803-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc803-137">**Zeilen \_ Schließen**</span><span class="sxs-lookup"><span data-stu-id="bc803-137">**LINE\_CLOSE**</span></span>](line-close.md)
</dt> <dt>

[<span data-ttu-id="bc803-138">**Zeilen \_ Antwort**</span><span class="sxs-lookup"><span data-stu-id="bc803-138">**LINE\_REPLY**</span></span>](line-reply.md)
</dt> <dt>

[<span data-ttu-id="bc803-139">**Lineproxyrequest**</span><span class="sxs-lookup"><span data-stu-id="bc803-139">**LINEPROXYREQUEST**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineproxyrequest)
</dt> <dt>

[<span data-ttu-id="bc803-140">**lineproxyresponse**</span><span class="sxs-lookup"><span data-stu-id="bc803-140">**lineProxyResponse**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse)
</dt> </dl>

 

 




