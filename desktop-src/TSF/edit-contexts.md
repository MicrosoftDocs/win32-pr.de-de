---
title: Kontexte bearbeiten
description: Kontexte bearbeiten
ms.assetid: cf8bbe66-d2ad-49b3-9e7c-246e4ca50149
keywords:
- Text Dienste-Framework (TSF), Bearbeiten von Kontexten
- TSF (Text Dienst Framework), Kontexte bearbeiten
- Text Dienste, Kontexte bearbeiten
- TSF-aktivierte Anwendungen, Kontexte bearbeiten
- Kontexte bearbeiten
- Text Dienste-Framework (TSF), Cookies bearbeiten
- TSF (Text Dienste-Framework), Cookies bearbeiten
- Text Dienste, Cookies bearbeiten
- TSF-aktivierte Anwendungen, Cookies bearbeiten
- Cookies bearbeiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 020ca8713d66d9d14e387381fc21157db8bdedf1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855943"
---
# <a name="edit-contexts"></a><span data-ttu-id="9c98a-113">Kontexte bearbeiten</span><span class="sxs-lookup"><span data-stu-id="9c98a-113">Edit Contexts</span></span>

## <a name="applications"></a><span data-ttu-id="9c98a-114">Anwendungen</span><span class="sxs-lookup"><span data-stu-id="9c98a-114">Applications</span></span>

<span data-ttu-id="9c98a-115">Um einen Bearbeitungs Kontext zu erstellen, ruft eine Anwendung [ITfDocumentMgr:: kreatecontext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext)auf.</span><span class="sxs-lookup"><span data-stu-id="9c98a-115">To create an edit context, an application calls [ITfDocumentMgr::CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext).</span></span>

## <a name="text-services"></a><span data-ttu-id="9c98a-116">Text Dienste</span><span class="sxs-lookup"><span data-stu-id="9c98a-116">Text Services</span></span>

<span data-ttu-id="9c98a-117">Ein Text Dienst verwendet häufig den aktuell aktiven Bearbeitungs Kontext.</span><span class="sxs-lookup"><span data-stu-id="9c98a-117">A text service often uses the currently active edit context.</span></span> <span data-ttu-id="9c98a-118">Der derzeit aktive Bearbeitungs Kontext ist der Bearbeitungs Kontext am oberen Rand des Stapels des aktiven Dokument-Managers.</span><span class="sxs-lookup"><span data-stu-id="9c98a-118">The currently active edit context is the edit context at the top of the stack of the active document manager.</span></span> <span data-ttu-id="9c98a-119">Um den derzeit aktiven Kontext abzurufen, Ruft ein Text Dienst [ITfThreadMgr:: GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus) auf, um den aktiven Dokument-Manager abzurufen. Anschließend wird [ITfDocumentMgr:: GetTop](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-gettop) aufgerufen, um den Bearbeitungs Kontext am oberen Rand des Stapels abzurufen.</span><span class="sxs-lookup"><span data-stu-id="9c98a-119">To obtain the currently active context, a text service calls [ITfThreadMgr::GetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus) to obtain the active document manager and then calls [ITfDocumentMgr::GetTop](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-gettop) to obtain the edit context at the top of the stack.</span></span>

<span data-ttu-id="9c98a-120">In einigen Fällen erfordert ein Text Dienst einen eigenen Bearbeitungs Kontext.</span><span class="sxs-lookup"><span data-stu-id="9c98a-120">In some cases, a text service requires its own edit context.</span></span> <span data-ttu-id="9c98a-121">Um einen Bearbeitungs Kontext zu erstellen, Ruft ein Text Dienst **ITfDocumentMgr:: kreatecontext** auf.</span><span class="sxs-lookup"><span data-stu-id="9c98a-121">To create an edit context, a text service calls **ITfDocumentMgr::CreateContext**.</span></span>

## <a name="edit-cookies"></a><span data-ttu-id="9c98a-122">Cookies bearbeiten</span><span class="sxs-lookup"><span data-stu-id="9c98a-122">Edit Cookies</span></span>

<span data-ttu-id="9c98a-123">Viele Methoden, wie z. b. [itfrange:: SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext), erfordern eine Möglichkeit, einen Bearbeitungs Kontext zu identifizieren, der über eine schreibgeschützte oder Lese-/Schreib-Dokumentsperre verfügt. [](document-locks.md)</span><span class="sxs-lookup"><span data-stu-id="9c98a-123">Many methods, such as [ITfRange::SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext), require a way to identify an edit context that has a read-only or read/write [document lock](document-locks.md).</span></span> <span data-ttu-id="9c98a-124">Eine Dokument Sperre wird durch eine Aushandlung zwischen dem TSF-Manager und der Anwendung abgerufen.</span><span class="sxs-lookup"><span data-stu-id="9c98a-124">A document lock is obtained through a negotiation between the TSF manager and the application.</span></span> <span data-ttu-id="9c98a-125">Ein Text Dienst kann diese Aushandlung nicht direkt ausführen.</span><span class="sxs-lookup"><span data-stu-id="9c98a-125">A text service cannot perform this negotiation directly.</span></span> <span data-ttu-id="9c98a-126">Ein Text Dienst kann nur dann eine Sperre abrufen, indem er eine [Bearbeitungs Sitzung](edit-sessions.md) mit einem bestimmten Kontext und Lese-oder Lese-/Schreibzugriff anfordert.</span><span class="sxs-lookup"><span data-stu-id="9c98a-126">A text service can only obtain a lock by requesting an [edit session](edit-sessions.md) with a specific context and read-only or read/write access.</span></span> <span data-ttu-id="9c98a-127">Wenn die Bearbeitungs Sitzung erteilt wird, wird der Text Dienst mit einem *Bearbeitungs Cookie* bereitgestellt, das den Bearbeitungs Kontext mit dem angeforderten Zugriff identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9c98a-127">When the edit session is granted, the text service is supplied with an *edit cookie* that identifies the edit context with the requested access.</span></span> <span data-ttu-id="9c98a-128">Dieses Cookie wird dann an die-Methode weitergegeben, um den Bearbeitungs Kontext mit dem richtigen Zugriff zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="9c98a-128">This cookie is then passed to the method to identify the edit context with the proper access.</span></span>

<span data-ttu-id="9c98a-129">**ITfDocumentMgr:: kreatecontext** stellt dem Kontext Ersteller außerdem ein Bearbeitungs Cookie zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="9c98a-129">**ITfDocumentMgr::CreateContext** also supplies an edit cookie to the context creator.</span></span> <span data-ttu-id="9c98a-130">Dieses Cookie hat schreibgeschützten Zugriff, und es gibt keine Möglichkeit, die Zugriffsebene zu ändern.</span><span class="sxs-lookup"><span data-stu-id="9c98a-130">This cookie has read-only access and there is no way to modify the access level.</span></span> <span data-ttu-id="9c98a-131">In Wahrheit aushandelt der TSF-Manager keine Dokument Sperre für dieses Bearbeitungs Cookie.</span><span class="sxs-lookup"><span data-stu-id="9c98a-131">In truth, the TSF manager does not negotiate a document lock for this edit cookie.</span></span> <span data-ttu-id="9c98a-132">Das Cookie ist intern als schreibgeschützt gekennzeichnet, aber das Dokument ist eigentlich nicht gesperrt.</span><span class="sxs-lookup"><span data-stu-id="9c98a-132">The cookie is internally marked read-only, but the document is not actually locked.</span></span> <span data-ttu-id="9c98a-133">Wenn der Kontext Ersteller z. b. [ITfContext:: GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) mit dem Bearbeitungs Cookie aufruft, das von **ITfDocumentMgr:: featecontext** zurückgegeben wird, führt dies dazu, dass die Anwendung [ITextStoreACP:: GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection) oder [itextstoreanchor:: GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="9c98a-133">For example, if the context creator calls [ITfContext::GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) with the edit cookie returned by **ITfDocumentMgr::CreateContext** , this results in the application's [ITextStoreACP::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection) or [ITextStoreAnchor::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection) being called.</span></span> <span data-ttu-id="9c98a-134">Vor dem Abrufen der Auswahl wird von der Anwendung bestimmt, ob eine Dokument Sperre vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9c98a-134">Before obtaining the selection, the application will determine if a document lock exists.</span></span> <span data-ttu-id="9c98a-135">Da keine Sperre vorhanden ist, kann die Anwendung mit TS \_ E \_ NOLOCK nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9c98a-135">Because no lock exists, the application will fail with TS\_E\_NOLOCK.</span></span> <span data-ttu-id="9c98a-136">Das heißt, wenn eine Anwendung mit diesem Cookie eine Methode aufruft, die dazu führt, dass eine der aufrufenden Text Speichermethoden der Anwendung aufgerufen wird, muss dieser Fall intern behandelt werden, da die Anwendung nicht tatsächlich über eine Dokument Sperre verfügt.</span><span class="sxs-lookup"><span data-stu-id="9c98a-136">That is, if an application calls a method with this cookie that results in one of the application's text store methods being called, it must handle this case internally because the application will not actually have a document lock.</span></span>

<span data-ttu-id="9c98a-137">Wenn für den Kontext Ersteller ein Bearbeitungs Cookie mit Lese-/Schreibzugriff erforderlich ist, muss eine eigene Bearbeitungs Sitzung eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="9c98a-137">If the context creator requires an edit cookie with read/write access, it must establish its own edit session.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c98a-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9c98a-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c98a-139">ITfContext</span><span class="sxs-lookup"><span data-stu-id="9c98a-139">ITfContext</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfcontext)
</dt> <dt>

[<span data-ttu-id="9c98a-140">ITF documentmgr:: kreatecontext</span><span class="sxs-lookup"><span data-stu-id="9c98a-140">ITfDocumentMgr::CreateContext</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext)
</dt> <dt>

[<span data-ttu-id="9c98a-141">ITfThreadMgr:: GetFocus</span><span class="sxs-lookup"><span data-stu-id="9c98a-141">ITfThreadMgr::GetFocus</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getfocus)
</dt> <dt>

[<span data-ttu-id="9c98a-142">ITF documentmgr:: GetTop</span><span class="sxs-lookup"><span data-stu-id="9c98a-142">ITfDocumentMgr::GetTop</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-gettop)
</dt> <dt>

[<span data-ttu-id="9c98a-143">Itfrange:: SetText</span><span class="sxs-lookup"><span data-stu-id="9c98a-143">ITfRange::SetText</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext)
</dt> <dt>

[<span data-ttu-id="9c98a-144">Dokument Sperren</span><span class="sxs-lookup"><span data-stu-id="9c98a-144">Document Locks</span></span>](document-locks.md)
</dt> <dt>

[<span data-ttu-id="9c98a-145">Bearbeitungssitzungen</span><span class="sxs-lookup"><span data-stu-id="9c98a-145">Edit Sessions</span></span>](edit-sessions.md)
</dt> <dt>

[<span data-ttu-id="9c98a-146">ITF context:: GetSelection</span><span class="sxs-lookup"><span data-stu-id="9c98a-146">ITfContext::GetSelection</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[<span data-ttu-id="9c98a-147">ITextStoreACP:: GetSelection</span><span class="sxs-lookup"><span data-stu-id="9c98a-147">ITextStoreACP::GetSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)
</dt> <dt>

[<span data-ttu-id="9c98a-148">Itextstoreanchor:: GetSelection</span><span class="sxs-lookup"><span data-stu-id="9c98a-148">ITextStoreAnchor::GetSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection)
</dt> </dl>

 

 




