---
title: Dokument Sperren
description: Dokument Sperren
ms.assetid: 3c623c44-b0d3-4b03-8de9-25f1062b5726
keywords:
- Text Dienst Framework (TSF), Dokument Sperren
- TSF (Text Dienst Framework), Dokument Sperren
- TSF-aktivierte Anwendungen, Dokument Sperren
- Dokument Sperren
- Text Services-Framework (TSF), Zeichen Position der Anwendung (ACP)
- TSF (Text Dienst Framework), Zeichen Position der Anwendung (ACP)
- TSF-aktivierte Anwendungen, Anwendungs Zeichen Position (ACP)
- Zeichen Position der Anwendung (ACP)
- ACP (Position des Anwendungs Zeichens)
- Text Dienst Framework (TSF), Anker
- TSF (Text Dienst Framework), Anker
- TSF-aktivierte Anwendungen, Anker
- Anker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 438e22d7c77a45d798dfd6d5d7c43eaafa3e09c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206513"
---
# <a name="document-locks"></a><span data-ttu-id="cc5ff-116">Dokument Sperren</span><span class="sxs-lookup"><span data-stu-id="cc5ff-116">Document Locks</span></span>

## <a name="the-document-lock-protocol"></a><span data-ttu-id="cc5ff-117">Das Dokument Sperrprotokoll</span><span class="sxs-lookup"><span data-stu-id="cc5ff-117">The Document Lock Protocol</span></span>

<span data-ttu-id="cc5ff-118">Um eine Dokument Sperre für ACP-basierte Anwendungen anzufordern, ruft der TSF-Manager [ITextStoreACP:: RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock)auf.</span><span class="sxs-lookup"><span data-stu-id="cc5ff-118">To request a document lock for ACP-based applications, the TSF manager calls [ITextStoreACP::RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock).</span></span> <span data-ttu-id="cc5ff-119">Bei Anker basierten Anwendungen ruft der TSF-Manager [itextstoreanchor:: RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock)auf.</span><span class="sxs-lookup"><span data-stu-id="cc5ff-119">For anchor-based applications, the TSF manager calls [ITextStoreAnchor::RequestLock](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock).</span></span> <span data-ttu-id="cc5ff-120">Die Anwendung gewährt die Dokument Sperre durch Aufrufen von [ITextStoreACPSink:: onlockgewährten](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted) (ACP-basierte Anwendungen) oder [itextstoreanchorsink:: onlockgewährten](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted) (Anker basierte Anwendungen) in **RequestLock**.</span><span class="sxs-lookup"><span data-stu-id="cc5ff-120">The application grants the document lock by calling [ITextStoreACPSink::OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted) (ACP-based applications) or [ITextStoreAnchorSink::OnLockGranted](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted) (anchor-based applications) inside of **RequestLock**.</span></span> <span data-ttu-id="cc5ff-121">Die Sperre ist nur während des **onlockgewährten** -Aufrufes zulässig.</span><span class="sxs-lookup"><span data-stu-id="cc5ff-121">The lock is only valid during the **OnLockGranted** call.</span></span> <span data-ttu-id="cc5ff-122">Wenn **onlockgewährte** zurückgibt, gilt das Dokument als entsperrt.</span><span class="sxs-lookup"><span data-stu-id="cc5ff-122">When **OnLockGranted** returns, the document is considered unlocked.</span></span>

## <a name="types-of-document-locks"></a><span data-ttu-id="cc5ff-123">Typen von Dokument Sperren</span><span class="sxs-lookup"><span data-stu-id="cc5ff-123">Types of Document Locks</span></span>

<span data-ttu-id="cc5ff-124">Es gibt zwei Arten von Dokument Sperren: schreibgeschützt und Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="cc5ff-124">There are two types of document locks, read-only and read/write.</span></span> <span data-ttu-id="cc5ff-125">Eine schreibgeschützte Sperre ermöglicht dem Manager, den Text zu lesen, kann aber keinen Text ändern oder einfügen.</span><span class="sxs-lookup"><span data-stu-id="cc5ff-125">A read-only lock enables the manager to read the text, but it cannot modify or insert text.</span></span> <span data-ttu-id="cc5ff-126">Eine Lese-/Schreibsperre ermöglicht dem Manager das Lesen, ändern und Einfügen von Text.</span><span class="sxs-lookup"><span data-stu-id="cc5ff-126">A read/write lock enables the manager to read, modify, and insert text.</span></span> <span data-ttu-id="cc5ff-127">Eine schreibgeschützte Sperre wird angefordert, indem TS \_ LF- \_ Lesevorgänge in *dwFlags* angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cc5ff-127">A read-only lock is requested by specifying TS\_LF\_READ in *dwFlags*.</span></span> <span data-ttu-id="cc5ff-128">Eine Lese-/Schreibsperre wird angefordert, indem TS LF-Lese \_ \_ Vorgang in *dwFlags* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cc5ff-128">A read/write lock is requested by specifying TS\_LF\_READWRITE in *dwFlags*.</span></span>

## <a name="asynchronous-and-synchronous-requests"></a><span data-ttu-id="cc5ff-129">Asynchrone und synchrone Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cc5ff-129">Asynchronous and Synchronous Requests</span></span>

<span data-ttu-id="cc5ff-130">Eine Sperranforderung kann entweder synchron oder asynchron sein.</span><span class="sxs-lookup"><span data-stu-id="cc5ff-130">A lock request can be either synchronous or asynchronous.</span></span> <span data-ttu-id="cc5ff-131">Der Manager fordert eine synchrone Sperre mit dem TS \_ LF- \_ synchronisierungsflag in *dwFlags* an.</span><span class="sxs-lookup"><span data-stu-id="cc5ff-131">The manager requests a synchronous lock by using the TS\_LF\_SYNC flag in *dwFlags*.</span></span> <span data-ttu-id="cc5ff-132">Wenn dieses Flag nicht vorhanden ist, ist die Anforderung asynchron.</span><span class="sxs-lookup"><span data-stu-id="cc5ff-132">If this flag is not present, the request is asynchronous.</span></span>

## <a name="granting-the-lock"></a><span data-ttu-id="cc5ff-133">Erteilen der Sperre</span><span class="sxs-lookup"><span data-stu-id="cc5ff-133">Granting the Lock</span></span>

<span data-ttu-id="cc5ff-134">Wenn **RequestLock** aufgerufen wird, muss die Anwendung ermitteln, ob das Dokument zurzeit gesperrt ist.</span><span class="sxs-lookup"><span data-stu-id="cc5ff-134">When **RequestLock** is called, the application must determine if the document is currently locked.</span></span> <span data-ttu-id="cc5ff-135">Wenn das Dokument nicht gesperrt ist und kein anderer Grund zum Verweigern der Sperre vorhanden ist, sollte die Anwendung *phrSession* auf OK festlegen \_ und s OK zurückgeben \_ .</span><span class="sxs-lookup"><span data-stu-id="cc5ff-135">If the document is not locked, and no other reason to deny the lock exists, the application should set *phrSession* to S\_OK and return S\_OK.</span></span>

<span data-ttu-id="cc5ff-136">Wenn das Dokument gesperrt ist und die Sperranforderung synchron ist, sollte die Anwendung *phrSession* auf "TS \_ E \_ synchron" festlegen und "S OK" zurückgeben \_ .</span><span class="sxs-lookup"><span data-stu-id="cc5ff-136">If the document is locked and the lock request is synchronous, the application should set *phrSession* to TS\_E\_SYNCHRONOUS and return S\_OK.</span></span> <span data-ttu-id="cc5ff-137">Dies weist darauf hin, dass eine synchrone Anforderung nicht erteilt werden kann.</span><span class="sxs-lookup"><span data-stu-id="cc5ff-137">This indicates that a synchronous request cannot be granted.</span></span>

<span data-ttu-id="cc5ff-138">Wenn das Dokument gesperrt ist und die Sperranforderung asynchron ist, sollte die Anwendung die Anforderung in die Warteschlange stellen, *phrSession* auf "TS \_ S \_ Async" festlegen und "S OK" zurückgeben \_ .</span><span class="sxs-lookup"><span data-stu-id="cc5ff-138">If the document is locked and the lock request is asynchronous, the application should queue the request, set *phrSession* to TS\_S\_ASYNC and return S\_OK.</span></span> <span data-ttu-id="cc5ff-139">Wenn das Dokument verfügbar wird, sollte die Anwendung die Anforderung aus der Warteschlange entfernen und **onlockgewährte** abrufen.</span><span class="sxs-lookup"><span data-stu-id="cc5ff-139">When the document becomes available, the application should remove the request from the queue and call **OnLockGranted**.</span></span> <span data-ttu-id="cc5ff-140">Diese Warteschlange von Sperr Anforderungen ist optional. Es gibt ein Szenario, das von einer Anwendung unterstützt werden muss.</span><span class="sxs-lookup"><span data-stu-id="cc5ff-140">This queuing of lock requests is optional; there is one scenario that an application must support.</span></span> <span data-ttu-id="cc5ff-141">Wenn das Dokument über eine schreibgeschützte Sperre verfügt, lautet die neue Sperranforderung Lese-/Schreibzugriff, und die Anforderung ist asynchron, die Anwendung wurde in **onlockgewährten** aufgerufen, was zu einem Wiedereinstiegs Aufruf von **RequestLock** geführt hat.</span><span class="sxs-lookup"><span data-stu-id="cc5ff-141">If the document has a read-only lock, the new lock request is read/write and the request is asynchronous, the application has called into **OnLockGranted** , which has caused a reentrant call to **RequestLock**.</span></span> <span data-ttu-id="cc5ff-142">Die Anwendung sollte *phrSession* auf "TS \_ S \_ Async" festlegen und "S OK" zurückgeben \_ .</span><span class="sxs-lookup"><span data-stu-id="cc5ff-142">The application should set *phrSession* to TS\_S\_ASYNC and return S\_OK.</span></span> <span data-ttu-id="cc5ff-143">Nachdem der Aufruf von **onlockgewährte zurückgegeben** wurde, sollte die Anwendung die upgradeanforderung verarbeiten, indem Sie **onlockgewährten** erneut mit "TS LF-Lesevorgang" aufruft \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="cc5ff-143">After the call to **OnLockGranted** returns, the application should process the upgrade request by calling **OnLockGranted** again with TS\_LF\_READWRITE.</span></span>

## <a name="lock-enforcement"></a><span data-ttu-id="cc5ff-144">Sperr Erzwingung</span><span class="sxs-lookup"><span data-stu-id="cc5ff-144">Lock Enforcement</span></span>

<span data-ttu-id="cc5ff-145">Die Anwendung muss sicherstellen, dass der richtige Sperrentyp vorhanden ist, bevor der Zugriff auf das Dokument zugelassen wird.</span><span class="sxs-lookup"><span data-stu-id="cc5ff-145">The application must ensure that the proper type of lock exists before allowing access to the document.</span></span> <span data-ttu-id="cc5ff-146">Die Anwendung sollte z. b. überprüfen, ob ein Dokument mindestens eine schreibgeschützte Sperre aufweist, bevor das Fortsetzen von [ITextStoreACP:: gettext](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-gettext) oder [itextstoreanchor:: gettext](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext) zugelassen wird.</span><span class="sxs-lookup"><span data-stu-id="cc5ff-146">For example, the application should verify that a document has at least a read-only lock before allowing [ITextStoreACP::GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-gettext) or [ITextStoreAnchor::GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext) to proceed.</span></span> <span data-ttu-id="cc5ff-147">Wenn die richtige Sperre nicht vorhanden ist, sollte die Anwendung TF \_ E \_ NOLOCK zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="cc5ff-147">If the proper lock does not exist, the application should return TF\_E\_NOLOCK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cc5ff-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cc5ff-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc5ff-149">Text Speicher</span><span class="sxs-lookup"><span data-stu-id="cc5ff-149">Text Stores</span></span>](text-stores.md)
</dt> <dt>

[<span data-ttu-id="cc5ff-150">ITextStoreACP:: RequestLock</span><span class="sxs-lookup"><span data-stu-id="cc5ff-150">ITextStoreACP::RequestLock</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock)
</dt> <dt>

[<span data-ttu-id="cc5ff-151">ITextStoreACPSink:: onlockgewährten</span><span class="sxs-lookup"><span data-stu-id="cc5ff-151">ITextStoreACPSink::OnLockGranted</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted)
</dt> <dt>

[<span data-ttu-id="cc5ff-152">ITextStoreACP:: gettext</span><span class="sxs-lookup"><span data-stu-id="cc5ff-152">ITextStoreACP::GetText</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-gettext)
</dt> <dt>

[<span data-ttu-id="cc5ff-153">Itextstoreanchor:: RequestLock</span><span class="sxs-lookup"><span data-stu-id="cc5ff-153">ITextStoreAnchor::RequestLock</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock)
</dt> <dt>

[<span data-ttu-id="cc5ff-154">Itextstoreanchorsink:: onlockgewährten</span><span class="sxs-lookup"><span data-stu-id="cc5ff-154">ITextStoreAnchorSink::OnLockGranted</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted)
</dt> <dt>

[<span data-ttu-id="cc5ff-155">Itextstoreanchor:: gettext</span><span class="sxs-lookup"><span data-stu-id="cc5ff-155">ITextStoreAnchor::GetText</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext)
</dt> </dl>

 

 




