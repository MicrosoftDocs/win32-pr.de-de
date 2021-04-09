---
title: Text Speicher
description: Text Speicher
ms.assetid: c827999a-0b74-4e5d-901e-4c2fa1d74929
keywords:
- Text Dienst Framework (TSF), Text Speicher
- TSF (Text Dienst Framework), Text Speicher
- TSF-aktivierte Anwendungen, Text Speicher
- Text Speicher
- Text Services-Framework (TSF), Zeichen Position der Anwendung (ACP)
- TSF (Text Dienst Framework), Zeichen Position der Anwendung (ACP)
- TSF-aktivierte Anwendungen, Anwendungs Zeichen Position (ACP)
- Zeichen Position der Anwendung (ACP)
- ACP (Position des Anwendungs Zeichens)
- Text Dienst Framework (TSF), Anker
- TSF (Text Dienst Framework), Anker
- TSF-aktivierte Anwendungen, Anker
- Anker
- Text Dienst Framework (TSF), Dokument Sperren
- TSF (Text Dienst Framework), Dokument Sperren
- TSF-aktivierte Anwendungen, Dokument Sperren
- Dokument Sperren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1234f71fa799cf911ff7ede89915068f69417a00
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039180"
---
# <a name="text-stores"></a><span data-ttu-id="eddfb-120">Text Speicher</span><span class="sxs-lookup"><span data-stu-id="eddfb-120">Text Stores</span></span>

## <a name="application-character-position-acp"></a><span data-ttu-id="eddfb-121">Zeichen Position der Anwendung (ACP)</span><span class="sxs-lookup"><span data-stu-id="eddfb-121">Application Character Position (ACP)</span></span>

<span data-ttu-id="eddfb-122">Eine ACP ist die Position eines Zeichens oder von Zeichen in einem Textstream, der als die Anzahl der Zeichen vom Anfang des Textstreams ausgedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="eddfb-122">An ACP is the location of a character, or characters, in a text stream that is expressed as the number of characters from the start of the text stream.</span></span> <span data-ttu-id="eddfb-123">Da das ACP-Modell Null basiert, weist das erste Zeichen in einem Textstream eine ACP von 0 (null) auf.</span><span class="sxs-lookup"><span data-stu-id="eddfb-123">Because the ACP model is zero-based, the first character in a text stream has an ACP of zero.</span></span> <span data-ttu-id="eddfb-124">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="eddfb-124">For example:</span></span>


```C++
Text Stream  H | e | l | l | o |   | W | o | r | l | d
ACP          0   1   2   3   4   5   6   7   8   9   10
```



<span data-ttu-id="eddfb-125">Ein Text Speicher implementiert ein Objekt, das die [ITextStoreACP-](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) Schnittstelle unterstützt, wodurch der Textstream in einer ACP ausgedrückt werden kann.</span><span class="sxs-lookup"><span data-stu-id="eddfb-125">A text store implements an object that supports the [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) interface, which enables the text stream to be expressed in an ACP.</span></span> <span data-ttu-id="eddfb-126">Die **ITextStoreACP-** Schnittstellen Methoden verwenden den ACP-Bereich des Textstreams, um den Text zu ändern.</span><span class="sxs-lookup"><span data-stu-id="eddfb-126">The **ITextStoreACP** interface methods use the ACP range of the text stream to modify the text.</span></span>

## <a name="anchor-based-applications"></a><span data-ttu-id="eddfb-127">Anchor-Based Anwendungen</span><span class="sxs-lookup"><span data-stu-id="eddfb-127">Anchor-Based Applications</span></span>

<span data-ttu-id="eddfb-128">Der Manager verwendet die ACP-basierten Methoden, um Text zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="eddfb-128">The manager uses the ACP-based methods natively to manipulate text.</span></span> <span data-ttu-id="eddfb-129">Ein Anker basierter Ansatz ist jedoch für [Microsoft-Active Accessibility](../winauto/microsoft-active-accessibility.md) Clients verfügbar, die [Anker](ranges.md)unterstützen, wobei der Manager die itextstoreanchor-Methode und die [itextstoreanchorsink](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchorsink) -Methode verwendet, um die [ITextStoreACP-](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) Methode und die [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) -Methode zu umschließen. [](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor)</span><span class="sxs-lookup"><span data-stu-id="eddfb-129">However, an anchor-based approach is available for [Microsoft Active Accessibility](../winauto/microsoft-active-accessibility.md) clients that support [anchors](ranges.md), whereby the manager uses [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) and [ITextStoreAnchorSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchorsink) methods to wrap the [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) and [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) methods.</span></span>

## <a name="document-access-control"></a><span data-ttu-id="eddfb-130">Dokument Access Control</span><span class="sxs-lookup"><span data-stu-id="eddfb-130">Document Access Control</span></span>

<span data-ttu-id="eddfb-131">Der Text Speicher steuert den Zugriff auf den Textstream mithilfe von [Dokument Sperren](document-locks.md).</span><span class="sxs-lookup"><span data-stu-id="eddfb-131">The text store controls access to the text stream by using [document locks](document-locks.md).</span></span> <span data-ttu-id="eddfb-132">Um den Text Speicher zu lesen oder zu ändern, muss der Manager zuerst eine Benachrichtigungs Senke installieren, die die [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) -Schnittstelle unterstützt, indem Sie die [ITextStoreACP:: AdviseSink-](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-advisesink) Methode aufrufen und einen Zeiger an eine Benachrichtigungs Senke übergibt.</span><span class="sxs-lookup"><span data-stu-id="eddfb-132">To read or modify the text store, the manager must first install an advise sink that supports the [ITextStoreACPSink](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink) interface by calling the [ITextStoreACP::AdviseSink](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-advisesink) method and passing a pointer to an advise sink.</span></span> <span data-ttu-id="eddfb-133">Die Benachrichtigungs Senke ermöglicht dem Manager das Abrufen von Dokument Sperren im Text Speicher und das Empfangen von Benachrichtigungen, wenn der Text Speicher von einem anderen als dem Vorgesetzten geändert wird, z. b. Benutzereingaben durch die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="eddfb-133">The advise sink enables the manager to obtain a document locks on the text store and receive notifications when the text store is modified by something other than the manager, such as user input through the application.</span></span> <span data-ttu-id="eddfb-134">Empfehlung-senken werden weiter unten in diesem Thema erläutert.</span><span class="sxs-lookup"><span data-stu-id="eddfb-134">Advise sinks are discussed later in this topic.</span></span>

## <a name="how-to-initialize-the-text-store"></a><span data-ttu-id="eddfb-135">Initialisieren des Text Stores</span><span class="sxs-lookup"><span data-stu-id="eddfb-135">How To Initialize the Text Store</span></span>

<span data-ttu-id="eddfb-136">Eine Anwendung initialisiert einen Text Speicher, indem die folgenden Schritte ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="eddfb-136">An application initializes a text store by completing the following steps:</span></span>

1.  <span data-ttu-id="eddfb-137">Erstellen Sie ein Thread-Manager-Objekt auf Grundlage der [ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) -Schnittstelle, indem Sie die [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion mit einem Zeiger auf ein Thread-Manager-Objekt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="eddfb-137">Create a thread manager object based on the [ITfThreadMgr](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr) interface by calling the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function with a pointer to a thread manager object.</span></span> <span data-ttu-id="eddfb-138">Im folgenden finden Sie ein Codebeispiel für die Implementierung eines Thread-Manager-Objekts.</span><span class="sxs-lookup"><span data-stu-id="eddfb-138">The following is a code example of implementing a thread manager object.</span></span>
    ```C++
    hr = CoCreateInstance (CLSID_TF_ThreadMgr, NULL, CLSCTX_INPROC_SERVER, 
                            IID_ITfThreadMgr, (void**)&pThreadMgr);
    ```

    

2.  <span data-ttu-id="eddfb-139">Aktivieren Sie das Thread-Manager-Objekt, indem Sie die [ITfThreadMgr:: Aktivierungs](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="eddfb-139">Activate the thread manager object by calling the [ITfThreadMgr::Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate) method.</span></span> <span data-ttu-id="eddfb-140">Diese Methode stellt einen Zeiger auf einen [Client Bezeichner](tfclientid.md) bereit, der zum Erstellen eines Kontext Objekts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="eddfb-140">This method supplies a pointer to a [client identifier](tfclientid.md) used to create a context object.</span></span> <span data-ttu-id="eddfb-141">Der Thread-Manager wird verwendet, um ein Dokument-Manager-Objekt zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="eddfb-141">The thread manager is used to implement a document manager object.</span></span>
3.  <span data-ttu-id="eddfb-142">Erstellen Sie ein Dokument-Manager-Objekt auf der Grundlage der [ITfDocumentMgr](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr) -Schnittstelle, indem Sie die [ITfThreadMgr:: createdocumentmgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr) -Methode mit einem Zeiger auf das Dokument-Manager-Objekt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="eddfb-142">Create a document manager object based on the [ITfDocumentMgr](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr) interface by calling the [ITfThreadMgr::CreateDocumentMgr](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-createdocumentmgr) method with a pointer to the document manager object.</span></span> <span data-ttu-id="eddfb-143">Das Dokument-Manager-Objekt wird verwendet, um ein Kontext Objekt zu implementieren, das der Text Speicher ist.</span><span class="sxs-lookup"><span data-stu-id="eddfb-143">The document manager object is used to implement a context object that is the text store.</span></span>
4.  <span data-ttu-id="eddfb-144">Erstellen Sie ein Kontext Objekt aus dem Dokument-Manager, indem Sie die [ITfDocumentMgr:: CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext) -Methode mit dem Zeiger auf das Text Speicher Objekt und einen Zeiger auf den Client Bezeichner aus der Aktivierung des Thread-Managers aufrufen.</span><span class="sxs-lookup"><span data-stu-id="eddfb-144">Create a context object from the document manager by calling the [ITfDocumentMgr::CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext) method with the pointer to the text store object and a pointer to the client identifier from activating the thread manager.</span></span> <span data-ttu-id="eddfb-145">Im folgenden finden Sie ein Beispiel für die Erstellung eines Kontext Objekts:</span><span class="sxs-lookup"><span data-stu-id="eddfb-145">The following is an example of creating a context object:</span></span>
    ```C++
    hr = pDocumentMgr->CreateContext(m_ClientID, 0, (ITextStoreACP*)this, 
                                    &pContext, pEditCookie);
    ```

    

5.  <span data-ttu-id="eddfb-146">Verschieben Sie das Kontext Objekt mit der [ITF documentmgr::P USH](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-push) -Methode auf den Stapel.</span><span class="sxs-lookup"><span data-stu-id="eddfb-146">Push the context object onto the stack with the [ITfDocumentMgr::Push](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-push) method.</span></span> <span data-ttu-id="eddfb-147">Im folgenden finden Sie ein Beispiel für das Übertragen des Kontext Objekts auf den Stapel:</span><span class="sxs-lookup"><span data-stu-id="eddfb-147">The following is an example of pushing the context object onto the stack:</span></span>
    ```C++
    hr = pDocumentMgr->Push(pContext);
    ```

    

## <a name="how-to-modify-the-text-store"></a><span data-ttu-id="eddfb-148">Vorgehensweise beim Ändern des Text Stores</span><span class="sxs-lookup"><span data-stu-id="eddfb-148">How To Modify the Text Store</span></span>

<span data-ttu-id="eddfb-149">Die **ITfDocumentMgr::P USH** -Methode ruft **ITextStoreACP:: AdviseSink** mit einem Zeiger auf die Schnittstelle für die Benachrichtigungs Senke auf, um eine neue Empfehlung-Senke zu installieren oder eine vorhandene Hinweis Senke zu ändern.</span><span class="sxs-lookup"><span data-stu-id="eddfb-149">The **ITfDocumentMgr::Push** method calls **ITextStoreACP::AdviseSink** with a pointer to the advise sink interface to install a new advise sink or modify an existing advise sink.</span></span> <span data-ttu-id="eddfb-150">Die Benachrichtigungs Senke empfängt Benachrichtigungen, wenn der Text Speicher von einem anderen als dem Vorgesetzten geändert wird, z. b. Benutzereingaben für die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="eddfb-150">The advise sink receives notifications when the text store is modified by something other than the manager, such as user input to the application.</span></span> <span data-ttu-id="eddfb-151">Anwendungen müssen die [itfthreadmgreventsink:: OnSetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgreventsink-onsetfocus) -Methode aufrufen, wenn die Eingabemethode den Fokus erhält.</span><span class="sxs-lookup"><span data-stu-id="eddfb-151">Applications must call the [ITfThreadMgrEventSink::OnSetFocus](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgreventsink-onsetfocus) method when the input method obtains the focus.</span></span> <span data-ttu-id="eddfb-152">Andere Benachrichtigungen an den Thread-Manager werden durch Aufrufen der entsprechenden **ITextStoreACPSink** -Schnittstellen Methoden bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="eddfb-152">Other notifications to the thread manager are provided by calling to the appropriate **ITextStoreACPSink** interface methods.</span></span>

<span data-ttu-id="eddfb-153">Anwendungen sollten jedoch nicht die Methoden der **ITextStoreACPSink** -Schnittstelle als Reaktion auf **ITextStoreACP-** Schnittstellen Methoden aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="eddfb-153">However, applications should not call the **ITextStoreACPSink** interface methods in response to **ITextStoreACP** interface methods.</span></span> <span data-ttu-id="eddfb-154">Anwendungen sollten nur **ITextStoreACPSink** -Schnittstellen Methoden aufzurufen, wenn der Text Speicher von einem anderen als dem Vorgesetzten geändert wird.</span><span class="sxs-lookup"><span data-stu-id="eddfb-154">Applications should only call **ITextStoreACPSink** interface methods when the text store is modified by something other than the manager.</span></span>

<span data-ttu-id="eddfb-155">Der Inhalt des Text Speicher kann mit einem temporären Eingabe Zustand namens [Komposition](compositions.md)geändert werden.</span><span class="sxs-lookup"><span data-stu-id="eddfb-155">The contents of the text store can be modified with a temporary input state called a [composition](compositions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="eddfb-156">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="eddfb-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eddfb-157">Anchors</span><span class="sxs-lookup"><span data-stu-id="eddfb-157">Anchors</span></span>](ranges.md)
</dt> <dt>

[<span data-ttu-id="eddfb-158">Ablage</span><span class="sxs-lookup"><span data-stu-id="eddfb-158">Compositions</span></span>](compositions.md)
</dt> <dt>

[<span data-ttu-id="eddfb-159">Dokument Sperren</span><span class="sxs-lookup"><span data-stu-id="eddfb-159">Document Locks</span></span>](document-locks.md)
</dt> <dt>

[<span data-ttu-id="eddfb-160">ITextStoreACPSink</span><span class="sxs-lookup"><span data-stu-id="eddfb-160">ITextStoreACPSink</span></span>](/windows/desktop/api/Textstor/nn-textstor-itextstoreacpsink)
</dt> <dt>

[<span data-ttu-id="eddfb-161">ITextStoreACP</span><span class="sxs-lookup"><span data-stu-id="eddfb-161">ITextStoreACP</span></span>](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp)
</dt> <dt>

[<span data-ttu-id="eddfb-162">Itextstoreanchor</span><span class="sxs-lookup"><span data-stu-id="eddfb-162">ITextStoreAnchor</span></span>](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor)
</dt> <dt>

[<span data-ttu-id="eddfb-163">Itextstoreanchorsink</span><span class="sxs-lookup"><span data-stu-id="eddfb-163">ITextStoreAnchorSink</span></span>](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchorsink)
</dt> <dt>

[<span data-ttu-id="eddfb-164">ITfDocumentMgr</span><span class="sxs-lookup"><span data-stu-id="eddfb-164">ITfDocumentMgr</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdocumentmgr)
</dt> <dt>

[<span data-ttu-id="eddfb-165">ITfThreadMgr</span><span class="sxs-lookup"><span data-stu-id="eddfb-165">ITfThreadMgr</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfthreadmgr)
</dt> <dt>

[<span data-ttu-id="eddfb-166">Itfthreadmgreventsink:: OnSetFocus</span><span class="sxs-lookup"><span data-stu-id="eddfb-166">ITfThreadMgrEventSink::OnSetFocus</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgreventsink-onsetfocus)
</dt> <dt>

[<span data-ttu-id="eddfb-167">Tfclientid</span><span class="sxs-lookup"><span data-stu-id="eddfb-167">TfClientId</span></span>](tfclientid.md)
</dt> <dt>

[<span data-ttu-id="eddfb-168">Microsoft Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="eddfb-168">Microsoft Active Accessibility</span></span>](../winauto/microsoft-active-accessibility.md)
</dt> </dl>

 

 