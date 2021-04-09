---
description: In diesem Thema wird das MPEG-1 Media Source SDK-Beispiel ausführlich erläutert.
ms.assetid: d392f30c-c963-4eb3-add2-1bb986919c0b
title: 'Fallstudie: MPEG-1-Medienquelle'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87e1f72cc6ae6df119439bdae1942732bf8d2fa2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104050678"
---
# <a name="case-study-mpeg-1-media-source"></a><span data-ttu-id="681a0-103">Fallstudie: MPEG-1-Medienquelle</span><span class="sxs-lookup"><span data-stu-id="681a0-103">Case Study: MPEG-1 Media Source</span></span>

<span data-ttu-id="681a0-104">In Microsoft Media Foundation wird das Objekt, das Mediendaten in die Daten Pipeline einführt, als *Medienquelle* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="681a0-104">In Microsoft Media Foundation, the object that introduces media data into the data pipeline is called a *media source*.</span></span> <span data-ttu-id="681a0-105">In diesem Thema wird das [MPEG-1 Media Source](mpeg1source-sample.md) SDK-Beispiel ausführlich erläutert.</span><span class="sxs-lookup"><span data-stu-id="681a0-105">This topic takes an in-depth look at the [MPEG-1 Media Source](mpeg1source-sample.md) SDK Sample.</span></span>

-   [<span data-ttu-id="681a0-106">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="681a0-106">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="681a0-107">C++-Klassen, die in der MPEG-1-Quelle verwendet werden</span><span class="sxs-lookup"><span data-stu-id="681a0-107">C++ Classes Used in the MPEG-1 Source</span></span>](#c-classes-used-in-the-mpeg-1-source)
-   [<span data-ttu-id="681a0-108">Byte Datenstrom-Handler</span><span class="sxs-lookup"><span data-stu-id="681a0-108">Byte-Stream Handler</span></span>](#byte-stream-handler)
-   [<span data-ttu-id="681a0-109">Präsentations Deskriptor</span><span class="sxs-lookup"><span data-stu-id="681a0-109">Presentation Descriptor</span></span>](#presentation-descriptor)
-   [<span data-ttu-id="681a0-110">Streamingzustände</span><span class="sxs-lookup"><span data-stu-id="681a0-110">Streaming States</span></span>](#streaming-states)
    -   [<span data-ttu-id="681a0-111">Starten</span><span class="sxs-lookup"><span data-stu-id="681a0-111">Start</span></span>](#start)
    -   [<span data-ttu-id="681a0-112">Anhalten</span><span class="sxs-lookup"><span data-stu-id="681a0-112">Pause</span></span>](#pause)
    -   [<span data-ttu-id="681a0-113">Beenden</span><span class="sxs-lookup"><span data-stu-id="681a0-113">Stop</span></span>](#stop)
-   [<span data-ttu-id="681a0-114">Beispiel Anforderungen</span><span class="sxs-lookup"><span data-stu-id="681a0-114">Sample Requests</span></span>](#sample-requests)
-   [<span data-ttu-id="681a0-115">Ende des Streams</span><span class="sxs-lookup"><span data-stu-id="681a0-115">End of Stream</span></span>](#end-of-stream)
-   [<span data-ttu-id="681a0-116">Asynchrone Vorgänge</span><span class="sxs-lookup"><span data-stu-id="681a0-116">Asynchronous Operations</span></span>](#asynchronous-operations)
    -   [<span data-ttu-id="681a0-117">Vorgangs Warteschlange</span><span class="sxs-lookup"><span data-stu-id="681a0-117">Operation Queue</span></span>](#operation-queue)
-   [<span data-ttu-id="681a0-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="681a0-118">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="681a0-119">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="681a0-119">Prerequisites</span></span>

<span data-ttu-id="681a0-120">Bevor Sie dieses Thema lesen, sollten Sie sich mit den folgenden Media Foundation Konzepten vertraut machen:</span><span class="sxs-lookup"><span data-stu-id="681a0-120">Before reading this topic you should understand the following Media Foundation concepts:</span></span>

-   [<span data-ttu-id="681a0-121">Medienquellen-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="681a0-121">Media Source Object Model</span></span>](media-source-object-model.md)
-   <span data-ttu-id="681a0-122">[Asynchrone Rückruf Methoden](asynchronous-callback-methods.md).</span><span class="sxs-lookup"><span data-stu-id="681a0-122">[Asynchronous Callback Methods](asynchronous-callback-methods.md).</span></span>
-   [<span data-ttu-id="681a0-123">Arbeits Warteschlangen</span><span class="sxs-lookup"><span data-stu-id="681a0-123">Work Queues</span></span>](work-queues.md)
-   [<span data-ttu-id="681a0-124">Medienereignis Generatoren</span><span class="sxs-lookup"><span data-stu-id="681a0-124">Media Event Generators</span></span>](media-event-generators.md)
-   [<span data-ttu-id="681a0-125">Medien Puffer</span><span class="sxs-lookup"><span data-stu-id="681a0-125">Media Buffers</span></span>](media-buffers.md)
-   [<span data-ttu-id="681a0-126">Medien Beispiele</span><span class="sxs-lookup"><span data-stu-id="681a0-126">Media Samples</span></span>](media-samples.md)
-   [<span data-ttu-id="681a0-127">Medientypen</span><span class="sxs-lookup"><span data-stu-id="681a0-127">Media Types</span></span>](media-types.md)

<span data-ttu-id="681a0-128">Außerdem sollten Sie ein grundlegendes Verständnis der Media Foundation Architektur haben, insbesondere der Rolle von Medienquellen in der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="681a0-128">You should also have a basic understanding of the Media Foundation architecture, particularly the role of media sources in the pipeline.</span></span> <span data-ttu-id="681a0-129">(Weitere Informationen finden Sie unter [Medienquellen](media-sources.md).)</span><span class="sxs-lookup"><span data-stu-id="681a0-129">(For more information, see [Media Sources](media-sources.md).)</span></span>

<span data-ttu-id="681a0-130">Außerdem sollten Sie das Thema [Schreiben einer benutzerdefinierten Medienquelle](writing-a-custom-media-source.md)lesen, die eine allgemeinere Übersicht über die hier beschriebenen Schritte bietet.</span><span class="sxs-lookup"><span data-stu-id="681a0-130">In addition, you may want to read the topic [Writing a Custom Media Source](writing-a-custom-media-source.md), which gives a more general overview of the steps described here.</span></span>

<span data-ttu-id="681a0-131">In diesem Thema wird nicht der gesamte Code aus dem SDK-Beispiel reproduziert, da das Beispiel ziemlich groß ist.</span><span class="sxs-lookup"><span data-stu-id="681a0-131">This topic does not reproduce all of the code from the SDK sample, because the sample is fairly large.</span></span>

## <a name="c-classes-used-in-the-mpeg-1-source"></a><span data-ttu-id="681a0-132">C++-Klassen, die in der MPEG-1-Quelle verwendet werden</span><span class="sxs-lookup"><span data-stu-id="681a0-132">C++ Classes Used in the MPEG-1 Source</span></span>

<span data-ttu-id="681a0-133">Die Beispiel-MPEG-1-Quelle wird mit den folgenden C++-Klassen implementiert:</span><span class="sxs-lookup"><span data-stu-id="681a0-133">The sample MPEG-1 source is implemented with the following C++ classes:</span></span>

-   <span data-ttu-id="681a0-134">`MPEG1ByteStreamHandler`.</span><span class="sxs-lookup"><span data-stu-id="681a0-134">`MPEG1ByteStreamHandler`.</span></span> <span data-ttu-id="681a0-135">Implementiert den bytestreamhandler für die Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="681a0-135">Implements the byte-stream handler for the media source.</span></span> <span data-ttu-id="681a0-136">Bei einem Bytestream erstellt der bytestreamhandler eine Instanz der Quelle.</span><span class="sxs-lookup"><span data-stu-id="681a0-136">Given a byte stream, the byte-stream handler creates an instance of the source.</span></span>
-   <span data-ttu-id="681a0-137">`MPEG1Source`.</span><span class="sxs-lookup"><span data-stu-id="681a0-137">`MPEG1Source`.</span></span> <span data-ttu-id="681a0-138">Implementiert die Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="681a0-138">Implements the media source.</span></span>
-   <span data-ttu-id="681a0-139">`MPEG1Stream`.</span><span class="sxs-lookup"><span data-stu-id="681a0-139">`MPEG1Stream`.</span></span> <span data-ttu-id="681a0-140">Implementiert die Medienstrom Objekte.</span><span class="sxs-lookup"><span data-stu-id="681a0-140">Implements the media stream objects.</span></span> <span data-ttu-id="681a0-141">Die Medienquelle erstellt ein `MPEG1Stream` -Objekt für jeden Audiostream oder Videostream im MPEG-1-Bitstream.</span><span class="sxs-lookup"><span data-stu-id="681a0-141">The media source creates one `MPEG1Stream` object for every audio or video stream in the MPEG-1 bitstream.</span></span>
-   <span data-ttu-id="681a0-142">`Parser`.</span><span class="sxs-lookup"><span data-stu-id="681a0-142">`Parser`.</span></span> <span data-ttu-id="681a0-143">Analysiert den MPEG-1-Bitstream.</span><span class="sxs-lookup"><span data-stu-id="681a0-143">Parses the MPEG-1 bitstream.</span></span> <span data-ttu-id="681a0-144">In den meisten Fällen sind die Details dieser Klasse für die Media Foundation-APIs nicht relevant.</span><span class="sxs-lookup"><span data-stu-id="681a0-144">For the most part, the details of this class are not relevant to the Media Foundation APIs.</span></span>
-   <span data-ttu-id="681a0-145">SourceOP, opqueue: diese beiden Klassen verwalten asynchrone Vorgänge in der Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="681a0-145">SourceOp, OpQueue: These two classes manage asynchronous operations in the media source.</span></span> <span data-ttu-id="681a0-146">(Siehe [asynchrone Vorgänge](#asynchronous-operations)).</span><span class="sxs-lookup"><span data-stu-id="681a0-146">(See [Asynchronous Operations](#asynchronous-operations)).</span></span>

<span data-ttu-id="681a0-147">Weitere verschiedene Hilfsklassen werden weiter unten in diesem Thema beschrieben.</span><span class="sxs-lookup"><span data-stu-id="681a0-147">Other miscellaneous helper classes are described later in the topic.</span></span>

## <a name="byte-stream-handler"></a><span data-ttu-id="681a0-148">Byte-Stream Handler</span><span class="sxs-lookup"><span data-stu-id="681a0-148">Byte-Stream Handler</span></span>

<span data-ttu-id="681a0-149">Der *Byte Datenstrom* Handler ist das Objekt, das die Medienquelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="681a0-149">The *byte-stream* handler is the object that creates the media source.</span></span> <span data-ttu-id="681a0-150">Der Byte Datenstrom Handler wird vom quellresolver erstellt. Anwendungen interagieren nicht direkt mit dem Byte Datenstrom-Handler.</span><span class="sxs-lookup"><span data-stu-id="681a0-150">The byte-stream handler is created by the source resolver; applications do not interact directly with the byte-stream handler.</span></span> <span data-ttu-id="681a0-151">Der quellresolver ermittelt den bytestreamhandler, indem er sich in der Registrierung ansieht.</span><span class="sxs-lookup"><span data-stu-id="681a0-151">The source resolver discovers the byte-stream handler by looking in the registry.</span></span> <span data-ttu-id="681a0-152">Der Handler wird durch die Dateinamenerweiterung oder den MIME-Typ registriert.</span><span class="sxs-lookup"><span data-stu-id="681a0-152">Handler are registered by file name extension or MIME type.</span></span> <span data-ttu-id="681a0-153">Bei der MPEG-1-Quelle wird der Byte Datenstrom Handler für die Dateinamenerweiterung ". mpg" registriert.</span><span class="sxs-lookup"><span data-stu-id="681a0-153">For the MPEG-1 source, the byte-stream handler is registered for the ".mpg" file name extension.</span></span>

> [!Note]  
> <span data-ttu-id="681a0-154">Wenn Sie benutzerdefinierte URL-Schemas unterstützen möchten, können Sie auch einen *Schema Handler* schreiben.</span><span class="sxs-lookup"><span data-stu-id="681a0-154">If you want to support custom URL schemes, you can also write a *scheme handler*.</span></span> <span data-ttu-id="681a0-155">Die MPEG-1-Quelle ist für lokale Dateien konzipiert, und Media Foundation stellt bereits einen Schema Handler für "file://"-URLs bereit.</span><span class="sxs-lookup"><span data-stu-id="681a0-155">The MPEG-1 source is designed for local files, and Media Foundation already provides a scheme handler for "file://" URLs.</span></span>

 

<span data-ttu-id="681a0-156">Der Byte Datenstrom Handler implementiert die [**IMF bytestreamhandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="681a0-156">The byte-stream handler implements the [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) interface.</span></span> <span data-ttu-id="681a0-157">Diese Schnittstelle verfügt über zwei wichtige Methoden, die implementiert werden müssen:</span><span class="sxs-lookup"><span data-stu-id="681a0-157">This interface has two most important methods that must be implemented:</span></span>

-   <span data-ttu-id="681a0-158">[**Beginkreateobject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject).</span><span class="sxs-lookup"><span data-stu-id="681a0-158">[**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject).</span></span> <span data-ttu-id="681a0-159">Startet einen asynchronen Vorgang, um die Medienquelle zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="681a0-159">Starts an asynchronous operation to create the media source.</span></span>
-   <span data-ttu-id="681a0-160">[**Endkreateobject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject).</span><span class="sxs-lookup"><span data-stu-id="681a0-160">[**EndCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject).</span></span> <span data-ttu-id="681a0-161">Schließt den asynchronen-Aufrufvorgang ab.</span><span class="sxs-lookup"><span data-stu-id="681a0-161">Completes the asynchronous call.</span></span>

<span data-ttu-id="681a0-162">Zwei andere Methoden sind optional und werden im SDK-Beispiel nicht implementiert:</span><span class="sxs-lookup"><span data-stu-id="681a0-162">Two other methods are optional and not implemented in the SDK sample:</span></span>

-   <span data-ttu-id="681a0-163">[**Cancelobjectcreation**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation).</span><span class="sxs-lookup"><span data-stu-id="681a0-163">[**CancelObjectCreation**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation).</span></span> <span data-ttu-id="681a0-164">Bricht die [**beginkreateobject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) -Methode ab.</span><span class="sxs-lookup"><span data-stu-id="681a0-164">Cancels the [**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) method.</span></span> <span data-ttu-id="681a0-165">Diese Methode ist nützlich für eine Netzwerkquelle, bei der beim Start eine hohe Latenz auftreten kann.</span><span class="sxs-lookup"><span data-stu-id="681a0-165">This method is useful for a network source that might have a high latency at startup.</span></span>
-   <span data-ttu-id="681a0-166">[**Getmaxnummeriofbytesrequirements dforresolution**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-getmaxnumberofbytesrequiredforresolution).</span><span class="sxs-lookup"><span data-stu-id="681a0-166">[**GetMaxNumberOfBytesRequiredForResolution**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-getmaxnumberofbytesrequiredforresolution).</span></span> <span data-ttu-id="681a0-167">Ruft die maximale Anzahl von Bytes ab, die der Handler aus dem Quelldaten Strom liest.</span><span class="sxs-lookup"><span data-stu-id="681a0-167">Gets the maximum number of bytes that the handler will read from the source stream.</span></span> <span data-ttu-id="681a0-168">Implementieren Sie diese Methode, wenn Sie wissen, wie viel Daten der Byte Strom Handler vor der Erstellung der Medienquelle haben kann.</span><span class="sxs-lookup"><span data-stu-id="681a0-168">Implement this method if you know how much data the byte-stream handler before it can create the media source.</span></span> <span data-ttu-id="681a0-169">Andernfalls geben Sie einfach **E \_ notimpl** zurück.</span><span class="sxs-lookup"><span data-stu-id="681a0-169">Otherwise, simply return **E\_NOTIMPL**.</span></span>

<span data-ttu-id="681a0-170">Hier ist die Implementierung der [**beginkreateobject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) -Methode:</span><span class="sxs-lookup"><span data-stu-id="681a0-170">Here is the implementation of the [**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) method:</span></span>


```C++
HRESULT MPEG1ByteStreamHandler::BeginCreateObject(
        /* [in] */ IMFByteStream *pByteStream,
        /* [in] */ LPCWSTR pwszURL,
        /* [in] */ DWORD dwFlags,
        /* [in] */ IPropertyStore *pProps,
        /* [out] */ IUnknown **ppIUnknownCancelCookie,  // Can be NULL
        /* [in] */ IMFAsyncCallback *pCallback,
        /* [in] */ IUnknown *punkState                  // Can be NULL
        )
{
    if (pByteStream == NULL)
    {
        return E_POINTER;
    }

    if (pCallback == NULL)
    {
        return E_POINTER;
    }

    if ((dwFlags & MF_RESOLUTION_MEDIASOURCE) == 0)
    {
        return E_INVALIDARG;
    }

    HRESULT hr = S_OK;

    IMFAsyncResult *pResult = NULL;
    MPEG1Source    *pSource = NULL;

    // Create an instance of the media source.
    hr = MPEG1Source::CreateInstance(&pSource);

    // Create a result object for the caller's async callback.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateAsyncResult(NULL, pCallback, punkState, &pResult);
    }

    // Start opening the source. This is an async operation.
    // When it completes, the source will invoke our callback
    // and then we will invoke the caller's callback.
    if (SUCCEEDED(hr))
    {
        hr = pSource->BeginOpen(pByteStream, this, NULL);
    }

    if (SUCCEEDED(hr))
    {
        if (ppIUnknownCancelCookie)
        {
            *ppIUnknownCancelCookie = NULL;
        }

        m_pSource = pSource;
        m_pSource->AddRef();

        m_pResult = pResult;
        m_pResult->AddRef();
    }

// cleanup
    SafeRelease(&pSource);
    SafeRelease(&pResult);
    return hr;
}
```



<span data-ttu-id="681a0-171">Die-Methode führt die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="681a0-171">The method performs the following steps:</span></span>

1.  <span data-ttu-id="681a0-172">Erstellt eine neue Instanz eines `MPEG1Source`-Objekts.</span><span class="sxs-lookup"><span data-stu-id="681a0-172">Creates a new instance of the `MPEG1Source` object.</span></span>
2.  <span data-ttu-id="681a0-173">Erstellen Sie ein asynchrones Ergebnis Objekt.</span><span class="sxs-lookup"><span data-stu-id="681a0-173">Create an asynchronous result object.</span></span> <span data-ttu-id="681a0-174">Dieses Objekt wird später verwendet, um die Rückruf Methode des Quell Resolvers aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="681a0-174">This object is used later to invoke the source resolver's callback method.</span></span>
3.  <span data-ttu-id="681a0-175">Ruft `MPEG1Source::BeginOpen` auf, eine asynchrone Methode, die in der-Klasse definiert ist `MPEG1Source` .</span><span class="sxs-lookup"><span data-stu-id="681a0-175">Calls `MPEG1Source::BeginOpen`, an asynchronous method defined in the `MPEG1Source` class.</span></span>
4.  <span data-ttu-id="681a0-176">Legt *ppiunknowncancelcookie* auf **null** fest, um den Aufrufer darüber zu informieren, dass [**cancelobjectcreation**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation) nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="681a0-176">Sets *ppIUnknownCancelCookie* to **NULL**, which informs the caller that [**CancelObjectCreation**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation) is not supported.</span></span>

<span data-ttu-id="681a0-177">`MPEG1Source::BeginOpen`Mit der-Methode wird der Bytestream gelesen und das-Objekt initialisiert `MPEG1Source` .</span><span class="sxs-lookup"><span data-stu-id="681a0-177">The `MPEG1Source::BeginOpen` method does the actual work of reading the byte stream and initializing the `MPEG1Source` object.</span></span> <span data-ttu-id="681a0-178">Diese Methode ist nicht Teil der öffentlichen API.</span><span class="sxs-lookup"><span data-stu-id="681a0-178">This method is not part of the public API.</span></span> <span data-ttu-id="681a0-179">Sie können beliebige Mechanismen zwischen dem Handler und der Medienquelle definieren, die Ihren Anforderungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="681a0-179">You can define any mechanism between the handler and the media source that suits your needs.</span></span> <span data-ttu-id="681a0-180">Wenn Sie den größten Teil der Logik in die Medienquelle einfügen, bleibt der Byte Strom Handler relativ einfach.</span><span class="sxs-lookup"><span data-stu-id="681a0-180">Putting most of the logic into the media source keeps the byte-stream handler relatively simple.</span></span>

<span data-ttu-id="681a0-181">`BeginOpen`Führt die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="681a0-181">Briefly, `BeginOpen` does the following:</span></span>

1.  <span data-ttu-id="681a0-182">Ruft [**imfbytestream:: getFeatures**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) auf, um zu überprüfen, ob der quellbytestream sowohl lesbar als auch suchbar ist.</span><span class="sxs-lookup"><span data-stu-id="681a0-182">Calls [**IMFByteStream::GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) to verify that the source byte stream is both readable and seekable.</span></span>
2.  <span data-ttu-id="681a0-183">Ruft [**imfbytestream:: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) auf, um eine asynchrone e/a-Anforderung zu starten.</span><span class="sxs-lookup"><span data-stu-id="681a0-183">Calls [**IMFByteStream::BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) to start an asynchronous I/O request.</span></span>

<span data-ttu-id="681a0-184">Der Rest der Initialisierung erfolgt asynchron.</span><span class="sxs-lookup"><span data-stu-id="681a0-184">The rest of the initialization occurs asynchronously.</span></span> <span data-ttu-id="681a0-185">Die Medienquelle liest genügend Daten aus dem Stream, um die MPEG-1-Sequenz Header zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="681a0-185">The media source reads enough data from the stream to parse the MPEG-1 sequence headers.</span></span> <span data-ttu-id="681a0-186">Anschließend wird ein *Präsentations Deskriptor* erstellt, bei dem es sich um das Objekt handelt, das zum Beschreiben der Audiodaten und Videostreams in der Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="681a0-186">Then it creates a *presentation descriptor*, which is the object used to describe the audio and video streams in the file.</span></span> <span data-ttu-id="681a0-187">(Weitere Informationen finden Sie unter [Präsentations Deskriptor](#presentation-descriptor).) Wenn der `BeginOpen` Vorgang abgeschlossen ist, ruft der Byte Datenstrom Handler die Rückruf Methode des Quell Resolvers auf.</span><span class="sxs-lookup"><span data-stu-id="681a0-187">(For more information, see [Presentation Descriptor](#presentation-descriptor).) When the `BeginOpen` operation completes, the byte-stream handler invokes the source resolver's callback method.</span></span> <span data-ttu-id="681a0-188">An diesem Punkt ruft der Quell Konflikt Löser [**IMF bytestreamhandler:: endkreateobject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject)auf.</span><span class="sxs-lookup"><span data-stu-id="681a0-188">At that point, the source resolver calls [**IMFByteStreamHandler::EndCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject).</span></span> <span data-ttu-id="681a0-189">Die **endkreateobject** -Methode gibt den Status des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="681a0-189">The **EndCreateObject** method returns the status of the operation.</span></span>


```C++
HRESULT MPEG1ByteStreamHandler::EndCreateObject(
        /* [in] */ IMFAsyncResult *pResult,
        /* [out] */ MF_OBJECT_TYPE *pObjectType,
        /* [out] */ IUnknown **ppObject)
{
    if (pResult == NULL || pObjectType == NULL || ppObject == NULL)
    {
        return E_POINTER;
    }

    HRESULT hr = S_OK;

    *pObjectType = MF_OBJECT_INVALID;
    *ppObject = NULL;

    hr = pResult->GetStatus();

    if (SUCCEEDED(hr))
    {
        *pObjectType = MF_OBJECT_MEDIASOURCE;

        assert(m_pSource != NULL);

        hr = m_pSource->QueryInterface(IID_PPV_ARGS(ppObject));
    }

    SafeRelease(&m_pSource);
    SafeRelease(&m_pResult);
    return hr;
}
```



<span data-ttu-id="681a0-190">Wenn während dieses Vorgangs ein Fehler auftritt, wird der Rückruf mit einem Fehlerstatus Code aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="681a0-190">If an error occurs at any time during this process, the callback is invoked with an error status code.</span></span>

## <a name="presentation-descriptor"></a><span data-ttu-id="681a0-191">Präsentations Deskriptor</span><span class="sxs-lookup"><span data-stu-id="681a0-191">Presentation Descriptor</span></span>

<span data-ttu-id="681a0-192">Der Präsentations Deskriptor beschreibt den Inhalt der MPEG-1-Datei, einschließlich der folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="681a0-192">The presentation descriptor describes the contents of the MPEG-1 file, including the following information:</span></span>

-   <span data-ttu-id="681a0-193">Die Anzahl der Streams.</span><span class="sxs-lookup"><span data-stu-id="681a0-193">The number of the streams.</span></span>
-   <span data-ttu-id="681a0-194">Das Format der einzelnen Datenströme.</span><span class="sxs-lookup"><span data-stu-id="681a0-194">The format of each stream.</span></span>
-   <span data-ttu-id="681a0-195">Datenstrom Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="681a0-195">Stream identifiers.</span></span>
-   <span data-ttu-id="681a0-196">Der Auswahl Status der einzelnen Datenströme (ausgewählt oder deaktiviert).</span><span class="sxs-lookup"><span data-stu-id="681a0-196">The selection status of each stream (selected or deselected).</span></span>

<span data-ttu-id="681a0-197">Im Hinblick auf die Media Foundation Architektur enthält der Präsentations Deskriptor einen oder mehrere *streamdeskriptoren*.</span><span class="sxs-lookup"><span data-stu-id="681a0-197">In terms of the Media Foundation architecture, the presentation descriptor contains one or more *stream descriptors*.</span></span> <span data-ttu-id="681a0-198">Jeder Datenstrom Deskriptor enthält einen *Medientyp Handler*, mit dem Medientypen im Stream abgerufen oder festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="681a0-198">Each stream descriptor contains a *media type handler*, which is used to get or set media types on the stream.</span></span> <span data-ttu-id="681a0-199">Media Foundation stellt Aktien Implementierungen für den Präsentations Deskriptor und den Datenstrom Deskriptor bereit. Diese sind für die meisten Medienquellen geeignet.</span><span class="sxs-lookup"><span data-stu-id="681a0-199">Media Foundation provides stock implementations for the presentation descriptor and stream descriptor; these are suitable for most media sources.</span></span>

<span data-ttu-id="681a0-200">Um einen Präsentations Deskriptor zu erstellen, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="681a0-200">To create a presentation descriptor, perform the following steps:</span></span>

1.  <span data-ttu-id="681a0-201">Für jeden Stream:</span><span class="sxs-lookup"><span data-stu-id="681a0-201">For each stream:</span></span>
    1.  <span data-ttu-id="681a0-202">Geben Sie eine Datenstrom-ID und ein Array möglicher Medientypen an.</span><span class="sxs-lookup"><span data-stu-id="681a0-202">Provide a stream ID and an array of possible media types.</span></span> <span data-ttu-id="681a0-203">Wenn der Stream mehr als einen Medientyp unterstützt, ordnen Sie die Liste der Medientypen ggf. nach Belieben zu.</span><span class="sxs-lookup"><span data-stu-id="681a0-203">If the stream supports more than one media type, order the list of media types by preference, if any.</span></span> <span data-ttu-id="681a0-204">(Geben Sie zuerst den optimalen Typ und den am wenigsten optimalen Typ an.)</span><span class="sxs-lookup"><span data-stu-id="681a0-204">(Put the optimal type first, and the least optimal type last.)</span></span>
    2.  <span data-ttu-id="681a0-205">Rufen Sie [**mfkreatestreamdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatestreamdescriptor) auf, um den Datenstrom Deskriptor zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="681a0-205">Call [**MFCreateStreamDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatestreamdescriptor) to create the stream descriptor.</span></span>
    3.  <span data-ttu-id="681a0-206">Aufrufen von [**imfstreamdescriptor:: getmediatypeer Handler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) für den neu erstellten streamdeskriptor.</span><span class="sxs-lookup"><span data-stu-id="681a0-206">Call [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) on the newly created stream descriptor.</span></span>
    4.  <span data-ttu-id="681a0-207">Um das Standardformat für den Stream festzulegen, können Sie [**imfmediatypeer Handler:: setcurrentmediatype**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="681a0-207">Call [**IMFMediaTypeHandler::SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) to set the default format for the stream.</span></span> <span data-ttu-id="681a0-208">Wenn mehr als ein Medientyp vorhanden ist, sollten Sie in der Regel den ersten Typ in der Liste festlegen.</span><span class="sxs-lookup"><span data-stu-id="681a0-208">If there is more than one media type, you should generally set the first type in the list.</span></span>
2.  <span data-ttu-id="681a0-209">Aufrufen von [**mfkreatepresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) und übergeben des Arrays von streamdeskriptorzeigern.</span><span class="sxs-lookup"><span data-stu-id="681a0-209">Call [**MFCreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) and pass in the array of stream descriptor pointers.</span></span>
3.  <span data-ttu-id="681a0-210">Für jeden Stream wird [**imfpresentationdescriptor:: selectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) oder [**deselectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream) aufgerufen, um den Standardauswahl Status festzulegen.</span><span class="sxs-lookup"><span data-stu-id="681a0-210">For each stream, call [**IMFPresentationDescriptor::SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) or [**DeselectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream) to set the default selection state.</span></span> <span data-ttu-id="681a0-211">Wenn mehr als ein Datenstrom desselben Typs (Audiodatei oder Video) vorhanden ist, sollte standardmäßig nur eine ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="681a0-211">If there is more than one stream of the same type (audio or video), only one should be selected by default.</span></span>

<span data-ttu-id="681a0-212">Das- `MPEG1Source` Objekt erstellt den Präsentations Deskriptor in der- `InitPresentationDescriptor` Methode:</span><span class="sxs-lookup"><span data-stu-id="681a0-212">The `MPEG1Source` object creates the presentation descriptor in its `InitPresentationDescriptor` method:</span></span>


```C++
HRESULT MPEG1Source::InitPresentationDescriptor()
{
    HRESULT hr = S_OK;
    DWORD cStreams = 0;

    assert(m_pPresentationDescriptor == NULL);
    assert(m_state == STATE_OPENING);

    if (m_pHeader == NULL)
    {
        return E_FAIL;
    }

    // Get the number of streams, as declared in the MPEG-1 header, skipping
    // any streams with an unsupported format.
    for (DWORD i = 0; i < m_pHeader->cStreams; i++)
    {
        if (IsStreamTypeSupported(m_pHeader->streams[i].type))
        {
            cStreams++;
        }
    }

    // How many streams do we actually have?
    if (cStreams > m_streams.GetCount())
    {
        // Keep reading data until we have seen a packet for each stream.
        return S_OK;
    }

    // We should never create a stream we don't support.
    assert(cStreams == m_streams.GetCount());

    // Ready to create the presentation descriptor.

    // Create an array of IMFStreamDescriptor pointers.
    IMFStreamDescriptor **ppSD =
            new (std::nothrow) IMFStreamDescriptor*[cStreams];

    if (ppSD == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    ZeroMemory(ppSD, cStreams * sizeof(IMFStreamDescriptor*));

    // Fill the array by getting the stream descriptors from the streams.
    for (DWORD i = 0; i < cStreams; i++)
    {
        hr = m_streams[i]->GetStreamDescriptor(&ppSD[i]);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Create the presentation descriptor.
    hr = MFCreatePresentationDescriptor(cStreams, ppSD,
        &m_pPresentationDescriptor);

    if (FAILED(hr))
    {
        goto done;
    }

    // Select the first video stream (if any).
    for (DWORD i = 0; i < cStreams; i++)
    {
        GUID majorType = GUID_NULL;

        hr = GetStreamMajorType(ppSD[i], &majorType);
        if (FAILED(hr))
        {
            goto done;
        }

        if (majorType == MFMediaType_Video)
        {
            hr = m_pPresentationDescriptor->SelectStream(i);
            if (FAILED(hr))
            {
                goto done;
            }
            break;
        }
    }

    // Switch state from "opening" to stopped.
    m_state = STATE_STOPPED;

    // Invoke the async callback to complete the BeginOpen operation.
    hr = CompleteOpen(S_OK);

done:
    // clean up:
    if (ppSD)
    {
        for (DWORD i = 0; i < cStreams; i++)
        {
            SafeRelease(&ppSD[i]);
        }
        delete [] ppSD;
    }
    return hr;
}
```



<span data-ttu-id="681a0-213">Die Anwendung ruft den Präsentations Deskriptor durch Aufrufen von [**imfmediasource:: createpresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor)ab.</span><span class="sxs-lookup"><span data-stu-id="681a0-213">The application gets the presentation descriptor by calling [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span> <span data-ttu-id="681a0-214">Diese Methode erstellt eine flache Kopie des Präsentations Deskriptors, indem [**imfpresentationdescriptor:: Clone**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-clone)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="681a0-214">This method creates a shallow copy of the presentation descriptor by calling [**IMFPresentationDescriptor::Clone**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-clone).</span></span> <span data-ttu-id="681a0-215">(Die Kopie enthält Zeiger auf die ursprünglichen streamdeskriptoren.) Die Anwendung kann den präsentationdeskriptor verwenden, um den Medientyp festzulegen, einen Stream auszuwählen oder einen Stream zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="681a0-215">(The copy contains pointers to the original stream descriptors.) The application can use the presentation descriptor to set the media type, select a stream, or deselect a stream.</span></span>

<span data-ttu-id="681a0-216">Optional können Präsentations Deskriptoren und streamdeskriptoren Attribute enthalten, die zusätzliche Informationen über die Quelle enthalten.</span><span class="sxs-lookup"><span data-stu-id="681a0-216">Optionally, presentation descriptors and stream descriptors can contain attributes that give additional information about the source.</span></span> <span data-ttu-id="681a0-217">Eine Liste solcher Attribute finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="681a0-217">For a list such attributes, see the following topics:</span></span>

-   [<span data-ttu-id="681a0-218">Präsentations deskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="681a0-218">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
-   [<span data-ttu-id="681a0-219">Streamdeskriptorattribute</span><span class="sxs-lookup"><span data-stu-id="681a0-219">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)

<span data-ttu-id="681a0-220">Ein Attribut verdient besondere Erwähnung: das [**MF \_ PD \_ Duration**](mf-pd-duration-attribute.md) -Attribut enthält die Gesamtdauer der Quelle.</span><span class="sxs-lookup"><span data-stu-id="681a0-220">One attribute deserves special mention: The [**MF\_PD\_DURATION**](mf-pd-duration-attribute.md) attribute contains the total duration of the source.</span></span> <span data-ttu-id="681a0-221">Legen Sie dieses Attribut fest, wenn Sie die Dauer im Voraus kennen. die Dauer kann z. b. in den Datei Headern angegeben werden, abhängig vom Dateiformat.</span><span class="sxs-lookup"><span data-stu-id="681a0-221">Set this attribute if you know the duration up front; for example, the duration might be specified in the file headers, depending on the file format.</span></span> <span data-ttu-id="681a0-222">Die Anwendung kann diesen Wert anzeigen oder verwenden, um eine Statusanzeige oder eine Suchleiste festzulegen.</span><span class="sxs-lookup"><span data-stu-id="681a0-222">The application might display this value, or use it to set a progress bar or seek bar.</span></span>

## <a name="streaming-states"></a><span data-ttu-id="681a0-223">Streamingzustände</span><span class="sxs-lookup"><span data-stu-id="681a0-223">Streaming States</span></span>

<span data-ttu-id="681a0-224">Eine Medienquelle definiert die folgenden Zustände:</span><span class="sxs-lookup"><span data-stu-id="681a0-224">A media source defines the following states:</span></span>



| <span data-ttu-id="681a0-225">State</span><span class="sxs-lookup"><span data-stu-id="681a0-225">State</span></span>    | <span data-ttu-id="681a0-226">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="681a0-226">Description</span></span>                                                                                                     |
|----------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="681a0-227">Gestartet</span><span class="sxs-lookup"><span data-stu-id="681a0-227">Started</span></span>  | <span data-ttu-id="681a0-228">Die Quelle akzeptiert und verarbeitet Beispiel Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="681a0-228">The source accepts and processes sample requests.</span></span>                                                               |
| <span data-ttu-id="681a0-229">Angehalten</span><span class="sxs-lookup"><span data-stu-id="681a0-229">Paused</span></span>   | <span data-ttu-id="681a0-230">Die Quelle akzeptiert Beispiel Anforderungen, verarbeitet sie aber nicht.</span><span class="sxs-lookup"><span data-stu-id="681a0-230">The source accepts sample requests, but does not process them.</span></span> <span data-ttu-id="681a0-231">Anforderungen werden in die Warteschlange eingereiht, bis die Quelle gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="681a0-231">Requests are queued until the source is started.</span></span> |
| <span data-ttu-id="681a0-232">Beendet.</span><span class="sxs-lookup"><span data-stu-id="681a0-232">Stopped.</span></span> | <span data-ttu-id="681a0-233">Die Quelle lehnt Beispiel Anforderungen ab.</span><span class="sxs-lookup"><span data-stu-id="681a0-233">The source rejects sample requests.</span></span>                                                                             |



 

### <a name="start"></a><span data-ttu-id="681a0-234">Start</span><span class="sxs-lookup"><span data-stu-id="681a0-234">Start</span></span>

<span data-ttu-id="681a0-235">Die [**imfmediasource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) -Methode startet die Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="681a0-235">The [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method starts the media source.</span></span> <span data-ttu-id="681a0-236">Hierfür werden die folgenden Parameter verwendet:</span><span class="sxs-lookup"><span data-stu-id="681a0-236">It takes the following parameters:</span></span>

-   <span data-ttu-id="681a0-237">Ein Präsentations Deskriptor.</span><span class="sxs-lookup"><span data-stu-id="681a0-237">A presentation descriptor.</span></span>
-   <span data-ttu-id="681a0-238">Eine Zeitformat-GUID.</span><span class="sxs-lookup"><span data-stu-id="681a0-238">A time-format GUID.</span></span>
-   <span data-ttu-id="681a0-239">Eine Startposition.</span><span class="sxs-lookup"><span data-stu-id="681a0-239">A start position.</span></span>

<span data-ttu-id="681a0-240">Die Anwendung muss den Präsentations Deskriptor abrufen, indem [**createpresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) für die Quelle aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="681a0-240">The application must obtain the presentation descriptor by calling [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) on the source.</span></span> <span data-ttu-id="681a0-241">Es ist kein definierter Mechanismus zum Validieren eines Präsentations Deskriptors vorhanden.</span><span class="sxs-lookup"><span data-stu-id="681a0-241">There is no defined mechanism for validating a presentation descriptor.</span></span> <span data-ttu-id="681a0-242">Wenn die Anwendung den falschen Präsentations Deskriptor angibt, sind die Ergebnisse nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="681a0-242">If the application specifies the wrong presentation descriptor, the results are undefined.</span></span>

<span data-ttu-id="681a0-243">Die Zeitformat-GUID gibt an, wie die Anfangsposition interpretiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="681a0-243">The time-format GUID specifies how to interpret the starting position.</span></span> <span data-ttu-id="681a0-244">Das Standardformat ist 100-Nanosecond (NS)-Einheiten, die durch GUID NULL angegeben werden \_ .</span><span class="sxs-lookup"><span data-stu-id="681a0-244">The standard format is 100-nanosecond (ns) units, indicated by GUID\_NULL.</span></span> <span data-ttu-id="681a0-245">Jede Medienquelle muss 100-ns-Einheiten unterstützen.</span><span class="sxs-lookup"><span data-stu-id="681a0-245">Every media source must support 100-ns units.</span></span> <span data-ttu-id="681a0-246">Optional kann eine Quelle auch andere Zeiteinheiten unterstützen, z. b. Frame Nummer oder Zeit Code.</span><span class="sxs-lookup"><span data-stu-id="681a0-246">Optionally, a source can support other units of time, such as frame number or time code.</span></span> <span data-ttu-id="681a0-247">Es gibt jedoch keine Standardmethode, um eine Medienquelle nach der Liste der unterstützten Zeitformate abzufragen.</span><span class="sxs-lookup"><span data-stu-id="681a0-247">However, there is no standard way to query a media source for the list of time formats it supports.</span></span>

<span data-ttu-id="681a0-248">Die Startposition wird als **PROPVARIANT** angegeben und ermöglicht je nach Zeitformat unterschiedliche Datentypen.</span><span class="sxs-lookup"><span data-stu-id="681a0-248">The start position is given as a **PROPVARIANT**, allowing for different data types depending on the time format.</span></span> <span data-ttu-id="681a0-249">Bei 100-ns ist der **PROPVARIANT** -Typ entweder **VT \_ I8** oder **VT \_ empty**.</span><span class="sxs-lookup"><span data-stu-id="681a0-249">For 100-ns, the **PROPVARIANT** type is either **VT\_I8** or **VT\_EMPTY**.</span></span> <span data-ttu-id="681a0-250">Wenn **VT \_ I8**, enthält die **PROPVARIANT** die Startposition in 100-ns-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="681a0-250">If **VT\_I8**, the **PROPVARIANT** contains the start position in 100-ns units.</span></span> <span data-ttu-id="681a0-251">Der Wert **VT \_ empty** hat die besondere Bedeutung "Start an der aktuellen Position".</span><span class="sxs-lookup"><span data-stu-id="681a0-251">The value **VT\_EMPTY** has the special meaning "start at the current position."</span></span>

<span data-ttu-id="681a0-252">Implementieren Sie die [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) -Methode wie folgt:</span><span class="sxs-lookup"><span data-stu-id="681a0-252">Implement the [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method as follows:</span></span>

1.  <span data-ttu-id="681a0-253">Parameter und Status überprüfen:</span><span class="sxs-lookup"><span data-stu-id="681a0-253">Validate parameters and state:</span></span>
    -   <span data-ttu-id="681a0-254">Suchen Sie nach **null** -Parametern.</span><span class="sxs-lookup"><span data-stu-id="681a0-254">Check for **NULL** parameters.</span></span>
    -   <span data-ttu-id="681a0-255">Überprüfen Sie die Zeitformat-GUID.</span><span class="sxs-lookup"><span data-stu-id="681a0-255">Check the time-format GUID.</span></span> <span data-ttu-id="681a0-256">Wenn der Wert ungültig ist, wird das von **MF \_ E \_ nicht unterstützte \_ Zeit \_ Format** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="681a0-256">If the value is invalid, return **MF\_E\_UNSUPPORTED\_TIME\_FORMAT**.</span></span>
    -   <span data-ttu-id="681a0-257">Überprüfen Sie den Datentyp von **PROPVARIANT** , der die Anfangsposition enthält.</span><span class="sxs-lookup"><span data-stu-id="681a0-257">Check the data type of the **PROPVARIANT** that holds the start position.</span></span>
    -   <span data-ttu-id="681a0-258">Überprüfen Sie die Startposition.</span><span class="sxs-lookup"><span data-stu-id="681a0-258">Validate the start position.</span></span> <span data-ttu-id="681a0-259">Wenn ungültig, wird " **MF \_ E \_ invalidrequest**" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="681a0-259">If invalid, return **MF\_E\_INVALIDREQUEST**.</span></span>
    -   <span data-ttu-id="681a0-260">Wenn die Quelle heruntergefahren wurde, wird das **\_ \_ Herunterfahren von MF E** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="681a0-260">If the source has been shut down, return **MF\_E\_SHUTDOWN**.</span></span>
2.  <span data-ttu-id="681a0-261">Wenn in Schritt 1 kein Fehler auftritt, stellen Sie einen asynchronen Vorgang in die Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="681a0-261">If no error occurs in step 1, queue an asynchronous operation.</span></span> <span data-ttu-id="681a0-262">Alles nach diesem Schritt tritt in einem Arbeitswarteschlangen-Thread auf.</span><span class="sxs-lookup"><span data-stu-id="681a0-262">Everything after this step occurs on a work-queue thread.</span></span>
3.  <span data-ttu-id="681a0-263">Für jeden Stream:</span><span class="sxs-lookup"><span data-stu-id="681a0-263">For each stream:</span></span>
    1.  <span data-ttu-id="681a0-264">Überprüfen Sie, ob der Stream bereits aus einer vorherigen [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) Anforderung aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="681a0-264">Check if the stream is already active from a previous [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) request.</span></span>
    2.  <span data-ttu-id="681a0-265">Aufrufen von [**imfpresentationdescriptor:: getstreamdescriptorbyindex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) , um zu überprüfen, ob die Anwendung den Stream ausgewählt oder deaktiviert hat.</span><span class="sxs-lookup"><span data-stu-id="681a0-265">Call [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) to check whether the application selected or deselected the stream.</span></span>
    3.  <span data-ttu-id="681a0-266">Wenn ein zuvor ausgewählter Stream jetzt deaktiviert ist, leeren Sie alle nicht übermittelten Beispiele für diesen Stream.</span><span class="sxs-lookup"><span data-stu-id="681a0-266">If a previously selected stream is now deselected, flush any undelivered samples for that stream.</span></span>
    4.  <span data-ttu-id="681a0-267">Wenn der Stream aktiv ist, sendet die Medienquelle (nicht der Stream) eines der folgenden Ereignisse:</span><span class="sxs-lookup"><span data-stu-id="681a0-267">If the stream is active, the media source (not the stream) sends one of the following events:</span></span>
        -   <span data-ttu-id="681a0-268">Er sendet [meupdatedstream](meupdatedstream.md) , wenn der Stream zuvor aktiv war.</span><span class="sxs-lookup"><span data-stu-id="681a0-268">It sends [MEUpdatedStream](meupdatedstream.md) if the stream was previously active.</span></span>
        -   <span data-ttu-id="681a0-269">Andernfalls wird [menewstream](menewstream.md)gesendet.</span><span class="sxs-lookup"><span data-stu-id="681a0-269">Otherwise, it sends [MENewStream](menewstream.md).</span></span>

        <span data-ttu-id="681a0-270">Bei beiden Ereignissen handelt es sich bei den Ereignisdaten um den [**IMF Media Stream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) -Zeiger für den Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="681a0-270">For both events, the event data is the [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) pointer for the stream.</span></span>
    5.  <span data-ttu-id="681a0-271">Wenn die Quelle vom angehaltenen Zustand neu gestartet wird, sind möglicherweise ausstehende Beispiel Anforderungen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="681a0-271">If the source is restarting from the paused state, there might be pending sample requests.</span></span> <span data-ttu-id="681a0-272">Wenn dies der Fall ist, übermitteln Sie diese jetzt.</span><span class="sxs-lookup"><span data-stu-id="681a0-272">If so, deliver these now.</span></span>
    6.  <span data-ttu-id="681a0-273">Wenn die Quelle eine neue Position sucht, sendet jedes Stream-Objekt ein [mestreamseeked](mestreamseeked.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="681a0-273">If the source is seeking to a new position, each stream object sends an [MEStreamSeeked](mestreamseeked.md) event.</span></span> <span data-ttu-id="681a0-274">Andernfalls sendet jeder Stream ein [mestreamstarted](mestreamstarted.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="681a0-274">Otherwise, each stream sends an [MEStreamStarted](mestreamstarted.md) event.</span></span>
4.  <span data-ttu-id="681a0-275">Wenn die Quelle eine neue Position sucht, sendet die Medienquelle ein [mesourceseeked](mesourceseeked.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="681a0-275">If the source is seeking to a new position, the media source sends an [MESourceSeeked](mesourceseeked.md) event.</span></span> <span data-ttu-id="681a0-276">Andernfalls wird ein [mesourcestarted](mesourcestarted.md) -Ereignis gesendet.</span><span class="sxs-lookup"><span data-stu-id="681a0-276">Otherwise, it sends an [MESourceStarted](mesourcestarted.md) event.</span></span>

<span data-ttu-id="681a0-277">Wenn zu einem beliebigen Zeitpunkt nach Schritt 2 ein Fehler auftritt, sendet die Quelle ein [mesourcestarted](mesourcestarted.md) -Ereignis mit einem Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="681a0-277">If an error occurs at any time after step 2, the source sends an [MESourceStarted](mesourcestarted.md) event with an error code.</span></span> <span data-ttu-id="681a0-278">Dadurch wird die Anwendung benachrichtigt, dass die [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) Methode asynchron fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="681a0-278">This alerts the application that the [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method failed asynchronously.</span></span>

<span data-ttu-id="681a0-279">Der folgende Code zeigt die Schritte 1 – 2:</span><span class="sxs-lookup"><span data-stu-id="681a0-279">The following code shows steps 1–2:</span></span>


```C++
HRESULT MPEG1Source::Start(
        IMFPresentationDescriptor* pPresentationDescriptor,
        const GUID* pguidTimeFormat,
        const PROPVARIANT* pvarStartPos
    )
{

    HRESULT hr = S_OK;
    SourceOp *pAsyncOp = NULL;

    // Check parameters.

    // Start position and presentation descriptor cannot be NULL.
    if (pvarStartPos == NULL || pPresentationDescriptor == NULL)
    {
        return E_INVALIDARG;
    }

    // Check the time format.
    if ((pguidTimeFormat != NULL) && (*pguidTimeFormat != GUID_NULL))
    {
        // Unrecognized time format GUID.
        return MF_E_UNSUPPORTED_TIME_FORMAT;
    }

    // Check the data type of the start position.
    if ((pvarStartPos->vt != VT_I8) && (pvarStartPos->vt != VT_EMPTY))
    {
        return MF_E_UNSUPPORTED_TIME_FORMAT;
    }

    EnterCriticalSection(&m_critSec);

    // Check if this is a seek request. This sample does not support seeking.

    if (pvarStartPos->vt == VT_I8)
    {
        // If the current state is STOPPED, then position 0 is valid.
        // Otherwise, the start position must be VT_EMPTY (current position).

        if ((m_state != STATE_STOPPED) || (pvarStartPos->hVal.QuadPart != 0))
        {
            hr = MF_E_INVALIDREQUEST;
            goto done;
        }
    }

    // Fail if the source is shut down.
    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    // Fail if the source was not initialized yet.
    hr = IsInitialized();
    if (FAILED(hr))
    {
        goto done;
    }

    // Perform a basic check on the caller's presentation descriptor.
    hr = ValidatePresentationDescriptor(pPresentationDescriptor);
    if (FAILED(hr))
    {
        goto done;
    }

    // The operation looks OK. Complete the operation asynchronously.
    hr = SourceOp::CreateStartOp(pPresentationDescriptor, &pAsyncOp);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAsyncOp->SetData(*pvarStartPos);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = QueueOperation(pAsyncOp);

done:
    SafeRelease(&pAsyncOp);
    LeaveCriticalSection(&m_critSec);
    return hr;
}
```



<span data-ttu-id="681a0-280">Die restlichen Schritte werden im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="681a0-280">The remaining steps are shown in the next example:</span></span>


```C++
HRESULT MPEG1Source::DoStart(StartOp *pOp)
{
    assert(pOp->Op() == SourceOp::OP_START);

    IMFPresentationDescriptor *pPD = NULL;
    IMFMediaEvent  *pEvent = NULL;

    HRESULT     hr = S_OK;
    LONGLONG    llStartOffset = 0;
    BOOL        bRestartFromCurrentPosition = FALSE;
    BOOL        bSentEvents = FALSE;

    hr = BeginAsyncOp(pOp);

    // Get the presentation descriptor from the SourceOp object.
    // This is the PD that the caller passed into the Start() method.
    // The PD has already been validated.
    if (SUCCEEDED(hr))
    {
        hr = pOp->GetPresentationDescriptor(&pPD);
    }

    // Because this sample does not support seeking, the start
    // position must be 0 (from stopped) or "current position."

    // If the sample supported seeking, we would need to get the
    // start position from the PROPVARIANT data contained in pOp.

    if (SUCCEEDED(hr))
    {
        // Select/deselect streams, based on what the caller set in the PD.
        // This method also sends the MENewStream/MEUpdatedStream events.
        hr = SelectStreams(pPD, pOp->Data());
    }

    if (SUCCEEDED(hr))
    {
        m_state = STATE_STARTED;

        // Queue the "started" event. The event data is the start position.
        hr = m_pEventQueue->QueueEventParamVar(
            MESourceStarted,
            GUID_NULL,
            S_OK,
            &pOp->Data()
            );
    }

    if (FAILED(hr))
    {
        // Failure. Send the error code to the application.

        // Note: It's possible that QueueEvent itself failed, in which case it
        // is likely to fail again. But there is no good way to recover in
        // that case.

        (void)m_pEventQueue->QueueEventParamVar(
            MESourceStarted, GUID_NULL, hr, NULL);
    }

    CompleteAsyncOp(pOp);

    SafeRelease(&pEvent);
    SafeRelease(&pPD);
    return hr;
}
```



### <a name="pause"></a><span data-ttu-id="681a0-281">Anhalten</span><span class="sxs-lookup"><span data-stu-id="681a0-281">Pause</span></span>

<span data-ttu-id="681a0-282">Die [**imfmediasource::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) -Methode hält die Medienquelle an.</span><span class="sxs-lookup"><span data-stu-id="681a0-282">The [**IMFMediaSource::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) method pauses the media source.</span></span> <span data-ttu-id="681a0-283">Implementieren Sie diese Methode wie folgt:</span><span class="sxs-lookup"><span data-stu-id="681a0-283">Implement this method as follows:</span></span>

1.  <span data-ttu-id="681a0-284">Einen asynchronen Vorgang in die Warteschlange stellen.</span><span class="sxs-lookup"><span data-stu-id="681a0-284">Queue an asynchronous operation.</span></span>
2.  <span data-ttu-id="681a0-285">Jeder aktive Stream sendet ein [mestreampaused](mestreampaused.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="681a0-285">Each active stream sends an [MEStreamPaused](mestreampaused.md) event.</span></span>
3.  <span data-ttu-id="681a0-286">Die Medienquelle sendet ein [mesourcepaused](mesourcepaused.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="681a0-286">The media source sends an [MESourcePaused](mesourcepaused.md) event.</span></span>

<span data-ttu-id="681a0-287">Bei angehaltenen Warteschlangen werden die Quell-in die Warteschlange eingereiht</span><span class="sxs-lookup"><span data-stu-id="681a0-287">While paused, the source queues sample requests without processing them.</span></span> <span data-ttu-id="681a0-288">(Siehe [Beispiel Anforderungen](#sample-requests).)</span><span class="sxs-lookup"><span data-stu-id="681a0-288">(See [Sample Requests](#sample-requests).)</span></span>

### <a name="stop"></a><span data-ttu-id="681a0-289">Stop</span><span class="sxs-lookup"><span data-stu-id="681a0-289">Stop</span></span>

<span data-ttu-id="681a0-290">Die [**imfmediasource:: Stopp**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) -Methode beendet die Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="681a0-290">The [**IMFMediaSource::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) method stops the media source.</span></span> <span data-ttu-id="681a0-291">Implementieren Sie diese Methode wie folgt:</span><span class="sxs-lookup"><span data-stu-id="681a0-291">Implement this method as follows:</span></span>

1.  <span data-ttu-id="681a0-292">Einen asynchronen Vorgang in die Warteschlange stellen.</span><span class="sxs-lookup"><span data-stu-id="681a0-292">Queue an asynchronous operation.</span></span>
2.  <span data-ttu-id="681a0-293">Jeder aktive Stream sendet ein [mestreambeendeten](mestreamstopped.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="681a0-293">Each active stream sends an [MEStreamStopped](mestreamstopped.md) event.</span></span>
3.  <span data-ttu-id="681a0-294">Löschen Sie alle Beispiele und Beispiel Anforderungen in der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="681a0-294">Clear all queued samples and sample requests.</span></span>
4.  <span data-ttu-id="681a0-295">Die Medienquelle sendet ein [mesourcestpt](mesourcestopped.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="681a0-295">The media source sends an [MESourceStopped](mesourcestopped.md) event.</span></span>

<span data-ttu-id="681a0-296">Obwohl die Quelle beendet ist, lehnt sie alle Anforderungen für Stichproben ab.</span><span class="sxs-lookup"><span data-stu-id="681a0-296">While stopped, the source rejects all requests for samples.</span></span>

<span data-ttu-id="681a0-297">Wenn die Quelle beendet wird, während eine e/a-Anforderung ausgeführt wird, kann die e/a-Anforderung abgeschlossen werden, nachdem die Quelle in den Zustand "beendet" wechselt.</span><span class="sxs-lookup"><span data-stu-id="681a0-297">If the source is stopped while an I/O request is in progress, the I/O request might complete after the source enters the stopped state.</span></span> <span data-ttu-id="681a0-298">In diesem Fall sollte die Quelle das Ergebnis dieser e/a-Anforderung verwerfen.</span><span class="sxs-lookup"><span data-stu-id="681a0-298">In that case, the source should discard the result of that I/O request.</span></span>

## <a name="sample-requests"></a><span data-ttu-id="681a0-299">Beispielanforderungen</span><span class="sxs-lookup"><span data-stu-id="681a0-299">Sample Requests</span></span>

<span data-ttu-id="681a0-300">Media Foundation ein *Pull* -Modell verwenden, bei dem die Pipeline Stichproben aus der Medienquelle anfordert.</span><span class="sxs-lookup"><span data-stu-id="681a0-300">Media Foundation use a *pull* model, in which the pipeline requests samples from the media source.</span></span> <span data-ttu-id="681a0-301">Dies unterscheidet sich von dem von DirectShow verwendeten Modell, in dem die Quellen "Push"-Beispiele verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="681a0-301">This differs from the model used by DirectShow, in which the sources "pushes" samples.</span></span>

<span data-ttu-id="681a0-302">Um ein neues Beispiel anzufordern, ruft die Media Foundation Pipeline [**imfmediastream:: requestsample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample)auf.</span><span class="sxs-lookup"><span data-stu-id="681a0-302">To request a new sample, the Media Foundation pipeline calls [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample).</span></span> <span data-ttu-id="681a0-303">Diese Methode nimmt einen **IUnknown** -Zeiger an, der ein *Tokenobjekt* darstellt.</span><span class="sxs-lookup"><span data-stu-id="681a0-303">This method takes an **IUnknown** pointer that represents a *token* object.</span></span> <span data-ttu-id="681a0-304">Die Implementierung des Tokenobjekts liegt dem Aufrufer. Er bietet dem Aufrufer einfach die Möglichkeit, Beispiel Anforderungen zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="681a0-304">The implementation of the token object is up to the caller; it simply provides a way for the caller to track sample requests.</span></span> <span data-ttu-id="681a0-305">Der tokenparameter kann auch **null** sein.</span><span class="sxs-lookup"><span data-stu-id="681a0-305">The token parameter can also be **NULL**.</span></span>

<span data-ttu-id="681a0-306">Angenommen, die Quelle verwendet asynchrone e/a-Anforderungen zum Lesen von Daten, wird die Beispiel Generierung nicht mit Beispiel Anforderungen synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="681a0-306">Assuming the source uses asynchronous I/O requests to read data, sample generation will not be synchronized with sample requests.</span></span> <span data-ttu-id="681a0-307">Zum Synchronisieren von Beispiel Anforderungen mit der Beispiel Generierung führt eine Medienquelle Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="681a0-307">To synchronize sample requests with sample generation, a media source does the following:</span></span>

1.  <span data-ttu-id="681a0-308">Anforderungs Token werden in einer Warteschlange abgelegt.</span><span class="sxs-lookup"><span data-stu-id="681a0-308">Request tokens are placed on a queue.</span></span>
2.  <span data-ttu-id="681a0-309">Wenn Beispiele generiert werden, werden Sie in einer zweiten Warteschlange platziert.</span><span class="sxs-lookup"><span data-stu-id="681a0-309">As samples are generated, they are placed on a second queue.</span></span>
3.  <span data-ttu-id="681a0-310">Die Medienquelle schließt eine Beispiel Anforderung ab, indem ein Anforderungs Token aus der ersten Warteschlange und ein Beispiel aus der zweiten Warteschlange abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="681a0-310">The media source completes a sample request by pulling a request token from the first queue and a sample from the second queue.</span></span>
4.  <span data-ttu-id="681a0-311">Die Medienquelle sendet ein memediasample-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="681a0-311">The media source sends an MEMediaSample event.</span></span> <span data-ttu-id="681a0-312">Das Ereignis enthält einen Zeiger auf das Beispiel, und das Beispiel enthält einen Zeiger auf das Token.</span><span class="sxs-lookup"><span data-stu-id="681a0-312">The event contains a pointer to the sample, and the sample contains a pointer to the token.</span></span>

<span data-ttu-id="681a0-313">Das folgende Diagramm zeigt die Beziehung zwischen dem [memediasample](memediasample.md) -Ereignis, dem Beispiel und dem Anforderungs Token.</span><span class="sxs-lookup"><span data-stu-id="681a0-313">The following diagram shows the relationship between the [MEMediaSample](memediasample.md) event, the sample, and the request token.</span></span>

![das Diagramm zeigt "memediasample" und eine Beispiel Warteschlange, die auf imfsample verweist. imfsample und die Anforderungs Warteschlange zeigen auf IUnknown.](images/mediasourceimpl01.png)

<span data-ttu-id="681a0-315">Die Beispiel-MPEG-1-Quelle implementiert diesen Prozess wie folgt:</span><span class="sxs-lookup"><span data-stu-id="681a0-315">The example MPEG-1 source implements this process as follows:</span></span>

1.  <span data-ttu-id="681a0-316">Die [**requestsample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) -Methode stellt die Anforderung in eine FIFO-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="681a0-316">The [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method puts the request on a FIFO queue.</span></span>
2.  <span data-ttu-id="681a0-317">Wenn e/a-Anforderungen abgeschlossen sind, erstellt die Medienquelle neue Beispiele und versetzt Sie in eine zweite FIFO-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="681a0-317">As I/O requests are completed, the media source creates new samples and puts them on a second FIFO queue.</span></span> <span data-ttu-id="681a0-318">(Diese Warteschlange verfügt über eine maximale Größe, um zu verhindern, dass die Quelle zu weit vorangeht.)</span><span class="sxs-lookup"><span data-stu-id="681a0-318">(This queue has a maximum size, to prevent the source from reading too far ahead.)</span></span>
3.  <span data-ttu-id="681a0-319">Wenn beide Warteschlangen mindestens ein Element (eine Anforderung und ein Beispiel) enthalten, vervollständigt die Medienquelle die erste Anforderung aus der Anforderungs Warteschlange, indem das erste Beispiel aus der Beispiel Warteschlange gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="681a0-319">Whenever both of these queues have at least one item (one request and one sample), the media source completes the first request from the request queue by sending out the first sample from the sample queue.</span></span>
4.  <span data-ttu-id="681a0-320">Um ein Beispiel zu liefern, sendet das Stream-Objekt (nicht das Quell Objekt) ein [memediasample](memediasample.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="681a0-320">To deliver a sample, the stream object (not the source object) sends an [MEMediaSample](memediasample.md) event.</span></span>
    -   <span data-ttu-id="681a0-321">Die Ereignisdaten sind ein Zeiger auf die [**imfsample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Schnittstelle des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="681a0-321">The event data is a pointer to the sample's [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface.</span></span>
    -   <span data-ttu-id="681a0-322">Wenn die Anforderung ein Token enthielt, fügen Sie das Token an das Beispiel an, indem Sie das [**mfsampleextension- \_ tokenattribut**](mfsampleextension-token-attribute.md) für das Beispiel festlegen.</span><span class="sxs-lookup"><span data-stu-id="681a0-322">If the request included a token, attach the token to the sample by setting the [**MFSampleExtension\_Token**](mfsampleextension-token-attribute.md) attribute on the sample.</span></span>

<span data-ttu-id="681a0-323">Zu diesem Zeitpunkt gibt es drei Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="681a0-323">At this point, there are three possibilities:</span></span>

-   <span data-ttu-id="681a0-324">Es gibt ein weiteres Beispiel in der Beispiel Warteschlange, aber keine übereinstimmende Anforderung.</span><span class="sxs-lookup"><span data-stu-id="681a0-324">There is another sample in the sample queue, but no matching request.</span></span>
-   <span data-ttu-id="681a0-325">Es gibt eine Anforderung, aber keine Stichprobe.</span><span class="sxs-lookup"><span data-stu-id="681a0-325">There is a request, but no sample.</span></span>
-   <span data-ttu-id="681a0-326">Beide Warteschlangen sind leer. Es sind keine Beispiele und keine Anforderungen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="681a0-326">Both queues are empty; there are no samples and no requests.</span></span>

<span data-ttu-id="681a0-327">Wenn die Beispiel Warteschlange leer ist, überprüft die Quelle das Ende des Streams (siehe das [Ende des Streams](#end-of-stream)).</span><span class="sxs-lookup"><span data-stu-id="681a0-327">If the sample queue is empty, the source checks for the end of the stream (see [End of Stream](#end-of-stream)).</span></span> <span data-ttu-id="681a0-328">Andernfalls wird eine weitere e/a-Anforderung für Daten gestartet.</span><span class="sxs-lookup"><span data-stu-id="681a0-328">Otherwise, it starts another I/O request for data.</span></span> <span data-ttu-id="681a0-329">Wenn während dieses Vorgangs ein Fehler auftritt, sendet der Stream ein [meerror](meerror.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="681a0-329">If any error occurs during this process, the stream sends an [MEError](meerror.md) event.</span></span>

<span data-ttu-id="681a0-330">Der folgende Code implementiert die [**IMF Mediastream:: requestsample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) -Methode:</span><span class="sxs-lookup"><span data-stu-id="681a0-330">The following code implements the [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method:</span></span>


```C++
HRESULT MPEG1Stream::RequestSample(IUnknown* pToken)
{
    HRESULT hr = S_OK;
    IMFMediaSource *pSource = NULL;

    // Hold the media source object's critical section.
    SourceLock lock(m_pSource);

    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    if (m_state == STATE_STOPPED)
    {
        hr = MF_E_INVALIDREQUEST;
        goto done;
    }

    if (!m_bActive)
    {
        // If the stream is not active, it should not get sample requests.
        hr = MF_E_INVALIDREQUEST;
        goto done;
    }

    if (m_bEOS && m_Samples.IsEmpty())
    {
        // This stream has already reached the end of the stream, and the
        // sample queue is empty.
        hr = MF_E_END_OF_STREAM;
        goto done;
    }

    hr = m_Requests.InsertBack(pToken);
    if (FAILED(hr))
    {
        goto done;
    }

    // Dispatch the request.
    hr = DispatchSamples();
    if (FAILED(hr))
    {
        goto done;
    }

done:
    if (FAILED(hr) && (m_state != STATE_SHUTDOWN))
    {
        // An error occurred. Send an MEError even from the source,
        // unless the source is already shut down.
        hr = m_pSource->QueueEvent(MEError, GUID_NULL, hr, NULL);
    }
    return hr;
}
```



<span data-ttu-id="681a0-331">Die `DispatchSamples` -Methode ruft Beispiele aus der Beispiel Warteschlange ab, gleicht Sie mit ausstehenden Beispiel Anforderungen und Warteschlangen [memediasample](memediasample.md) -Ereignissen ab:</span><span class="sxs-lookup"><span data-stu-id="681a0-331">The `DispatchSamples` method pulls samples from the sample queue, matches them with pending sample requests, and queues [MEMediaSample](memediasample.md) events:</span></span>


```C++
HRESULT MPEG1Stream::DispatchSamples()
{
    HRESULT hr = S_OK;
    BOOL bNeedData = FALSE;
    BOOL bEOS = FALSE;

    SourceLock lock(m_pSource);

    // An I/O request can complete after the source is paused, stopped, or
    // shut down. Do not deliver samples unless the source is running.
    if (m_state != STATE_STARTED)
    {
        return S_OK;
    }

    IMFSample *pSample = NULL;
    IUnknown  *pToken = NULL;

    // Deliver as many samples as we can.
    while (!m_Samples.IsEmpty() && !m_Requests.IsEmpty())
    {
        // Pull the next sample from the queue.
        hr = m_Samples.RemoveFront(&pSample);
        if (FAILED(hr))
        {
            goto done;
        }

        // Pull the next request token from the queue. Tokens can be NULL.
        hr = m_Requests.RemoveFront(&pToken);
        if (FAILED(hr))
        {
            goto done;
        }

        if (pToken)
        {
            // Set the token on the sample.
            hr = pSample->SetUnknown(MFSampleExtension_Token, pToken);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        // Send an MEMediaSample event with the sample.
        hr = m_pEventQueue->QueueEventParamUnk(
            MEMediaSample, GUID_NULL, S_OK, pSample);

        if (FAILED(hr))
        {
            goto done;
        }

        SafeRelease(&pSample);
        SafeRelease(&pToken);
    }

    if (m_Samples.IsEmpty() && m_bEOS)
    {
        // The sample queue is empty AND we have reached the end of the source
        // stream. Notify the pipeline by sending the end-of-stream event.

        hr = m_pEventQueue->QueueEventParamVar(
            MEEndOfStream, GUID_NULL, S_OK, NULL);

        if (FAILED(hr))
        {
            goto done;
        }

        // Notify the source. It will send the end-of-presentation event.
        hr = m_pSource->QueueAsyncOperation(SourceOp::OP_END_OF_STREAM);
        if (FAILED(hr))
        {
            goto done;
        }
    }
    else if (NeedsData())
    {
        // The sample queue is empty; the request queue is not empty; and we
        // have not reached the end of the stream. Ask for more data.
        hr = m_pSource->QueueAsyncOperation(SourceOp::OP_REQUEST_DATA);
        if (FAILED(hr))
        {
            goto done;
        }
    }

done:
    if (FAILED(hr) && (m_state != STATE_SHUTDOWN))
    {
        // An error occurred. Send an MEError even from the source,
        // unless the source is already shut down.
        m_pSource->QueueEvent(MEError, GUID_NULL, hr, NULL);
    }

    SafeRelease(&pSample);
    SafeRelease(&pToken);
    return S_OK;
}
```



<span data-ttu-id="681a0-332">Die- `DispatchSamples` Methode wird in den folgenden Situationen aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="681a0-332">The `DispatchSamples` method is called in the following circumstances:</span></span>

-   <span data-ttu-id="681a0-333">Innerhalb der [**requestsample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) -Methode.</span><span class="sxs-lookup"><span data-stu-id="681a0-333">Inside the [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method.</span></span>
-   <span data-ttu-id="681a0-334">Wenn die Medienquelle vom angehaltenen Zustand neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="681a0-334">When the media source restarts from the paused state.</span></span>
-   <span data-ttu-id="681a0-335">Wenn eine e/a-Anforderung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="681a0-335">When an I/O request completes.</span></span>

## <a name="end-of-stream"></a><span data-ttu-id="681a0-336">Ende des Streams</span><span class="sxs-lookup"><span data-stu-id="681a0-336">End of Stream</span></span>

<span data-ttu-id="681a0-337">Wenn ein Stream keine weiteren Daten enthält und alle Beispiele für diesen Stream übermittelt wurden, sendet die Streamobjekte ein [meendof Stream](meendofstream.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="681a0-337">When a stream has no more data, and all of the samples for that stream have been delivered, the stream objects sends an [MEEndOfStream](meendofstream.md) event.</span></span>

<span data-ttu-id="681a0-338">Wenn alle aktiven Streams abgeschlossen sind, sendet die Medienquelle ein [meendof Presentation](meendofpresentation.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="681a0-338">When all of the active streams are done, the media source sends an [MEEndOfPresentation](meendofpresentation.md) event.</span></span>

## <a name="asynchronous-operations"></a><span data-ttu-id="681a0-339">Asynchrone Vorgänge</span><span class="sxs-lookup"><span data-stu-id="681a0-339">Asynchronous Operations</span></span>

<span data-ttu-id="681a0-340">Der vielleicht schwierigste Teil beim Schreiben einer Medienquelle ist das Verständnis des Media Foundation asynchronen Modells.</span><span class="sxs-lookup"><span data-stu-id="681a0-340">Perhaps the hardest part of writing a media source is understanding the Media Foundation asynchronous model.</span></span>

<span data-ttu-id="681a0-341">Alle Methoden in einer Medienquelle, die das Streaming steuern, sind asynchron.</span><span class="sxs-lookup"><span data-stu-id="681a0-341">All of the methods on a media source that control streaming are asynchronous.</span></span> <span data-ttu-id="681a0-342">In jedem Fall führt die-Methode eine anfängliche Validierung aus, z. b. das Überprüfen von Parametern.</span><span class="sxs-lookup"><span data-stu-id="681a0-342">In each case, the method does some initial validation, such as checking parameters.</span></span> <span data-ttu-id="681a0-343">Die Quelle sendet dann den Rest der Arbeit an eine Arbeits Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="681a0-343">The source then dispatches the rest of the work to a work queue.</span></span> <span data-ttu-id="681a0-344">Nachdem der Vorgang abgeschlossen ist, sendet die Medienquelle ein Ereignis zurück an den Aufrufer über die [**imfmediaeventgenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) -Schnittstelle der Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="681a0-344">After the operation completes, the media source sends an event back to the caller, through the media source's [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="681a0-345">Daher ist es wichtig, dass Sie die Arbeits Warteschlangen verstehen.</span><span class="sxs-lookup"><span data-stu-id="681a0-345">It is therefore important to understand work queues.</span></span>

<span data-ttu-id="681a0-346">Wenn Sie ein Element in einer Arbeits Warteschlange platzieren möchten, können Sie entweder [**mfputworkitem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) oder [**mfputworkitemex**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex)abrufen.</span><span class="sxs-lookup"><span data-stu-id="681a0-346">To put an item on a work queue, you can call either [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) or [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex).</span></span> <span data-ttu-id="681a0-347">Die MPEG-1-Quelle verwendet " **mfputworkitem**", aber die beiden Funktionen führen dasselbe aus.</span><span class="sxs-lookup"><span data-stu-id="681a0-347">The MPEG-1 source happens to use **MFPutWorkItem**, but the two functions do the same thing.</span></span> <span data-ttu-id="681a0-348">Die **mfputworkitem** -Funktion übernimmt die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="681a0-348">The **MFPutWorkItem** function takes the following parameters:</span></span>

-   <span data-ttu-id="681a0-349">Ein **DWORD** -Wert, der die Arbeits Warteschlange identifiziert.</span><span class="sxs-lookup"><span data-stu-id="681a0-349">A **DWORD** value that identifies the work queue.</span></span> <span data-ttu-id="681a0-350">Sie können eine private Arbeits Warteschlange erstellen oder den **mfasync- \_ Rückruf \_ Warteschlangen- \_ Standard** verwenden.</span><span class="sxs-lookup"><span data-stu-id="681a0-350">You can create a private work queue or use **MFASYNC\_CALLBACK\_QUEUE\_STANDARD**.</span></span>
-   <span data-ttu-id="681a0-351">Ein Zeiger auf die [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="681a0-351">A pointer to the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span> <span data-ttu-id="681a0-352">Diese Rückruf Schnittstelle wird aufgerufen, um die Arbeit auszuführen.</span><span class="sxs-lookup"><span data-stu-id="681a0-352">This callback interface is invoked to perform the work.</span></span>
-   <span data-ttu-id="681a0-353">Ein optionales Zustands Objekt, das **IUnknown** implementieren muss.</span><span class="sxs-lookup"><span data-stu-id="681a0-353">An optional state object, which must implement **IUnknown**.</span></span>

<span data-ttu-id="681a0-354">Die Arbeits Warteschlange wird von mindestens einem Arbeitsthread gewartet, der fortlaufend das nächste Arbeits Element aus der Warteschlange abruft und die [**imfasynccallback:: Aufrufen**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) -Methode der Rückruf Schnittstelle aufruft.</span><span class="sxs-lookup"><span data-stu-id="681a0-354">The work queue is serviced by one or more worker threads that continuously pull the next work item from the queue and invoke the [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method of the callback interface.</span></span>

<span data-ttu-id="681a0-355">Es ist nicht garantiert, dass Arbeitselemente in derselben Reihenfolge ausgeführt werden, in der Sie Sie in der Warteschlange ablegen.</span><span class="sxs-lookup"><span data-stu-id="681a0-355">Work items are not guaranteed to execute in the same order that you put them on the queue.</span></span> <span data-ttu-id="681a0-356">Beachten Sie, dass mehr als ein Thread dieselbe Arbeits Warteschlange verarbeiten kann. Daher können [**Aufruf**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) Aufrufe überlappen oder nicht in der richtigen Reihenfolge auftreten.</span><span class="sxs-lookup"><span data-stu-id="681a0-356">Remember that more than one thread can service the same work queue, so [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) calls can overlap or occur out of order.</span></span> <span data-ttu-id="681a0-357">Daher liegt es an der Medienquelle, den korrekten internen Zustand beizubehalten, indem Arbeits Warteschlangen Elemente in der richtigen Reihenfolge übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="681a0-357">Therefore, it is up to the media source to maintain the correct internal state, by submitting work queue items in the right order.</span></span> <span data-ttu-id="681a0-358">Erst wenn der vorherige Vorgang beendet ist, startet die Quelle den nächsten Vorgang.</span><span class="sxs-lookup"><span data-stu-id="681a0-358">Only when the previous operation is complete does the source start the next operation.</span></span>

<span data-ttu-id="681a0-359">Zur Darstellung von ausstehenden Vorgängen definiert die MPEG-1-Quelle eine Klasse mit dem Namen `SourceOp` :</span><span class="sxs-lookup"><span data-stu-id="681a0-359">To represent pending operations, the MPEG-1 source defines a class named `SourceOp`:</span></span>


```C++
// Represents a request for an asynchronous operation.

class SourceOp : public IUnknown
{
public:

    enum Operation
    {
        OP_START,
        OP_PAUSE,
        OP_STOP,
        OP_REQUEST_DATA,
        OP_END_OF_STREAM
    };

    static HRESULT CreateOp(Operation op, SourceOp **ppOp);
    static HRESULT CreateStartOp(IMFPresentationDescriptor *pPD, SourceOp **ppOp);

    // IUnknown
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    SourceOp(Operation op);
    virtual ~SourceOp();

    HRESULT SetData(const PROPVARIANT& var);

    Operation Op() const { return m_op; }
    const PROPVARIANT& Data() { return m_data;}

protected:
    long        m_cRef;     // Reference count.
    Operation   m_op;
    PROPVARIANT m_data;     // Data for the operation.
};
```



<span data-ttu-id="681a0-360">Die- `Operation` Enumeration identifiziert den ausstehenden Vorgang.</span><span class="sxs-lookup"><span data-stu-id="681a0-360">The `Operation` enumeration identifies which operation is pending.</span></span> <span data-ttu-id="681a0-361">Die-Klasse enthält auch eine **PROPVARIANT** , um alle zusätzlichen Daten für den Vorgang zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="681a0-361">The class also contains a **PROPVARIANT** to convey any additional data for the operation.</span></span>

### <a name="operation-queue"></a><span data-ttu-id="681a0-362">Vorgangs Warteschlange</span><span class="sxs-lookup"><span data-stu-id="681a0-362">Operation Queue</span></span>

<span data-ttu-id="681a0-363">Zum Serialisieren von Vorgängen verwaltet die Medienquelle eine Warteschlange von `SourceOp` Objekten.</span><span class="sxs-lookup"><span data-stu-id="681a0-363">To serialize operations, the media source maintains a queue of `SourceOp` objects.</span></span> <span data-ttu-id="681a0-364">Er verwendet eine Hilfsklasse, um die Warteschlange zu verwalten:</span><span class="sxs-lookup"><span data-stu-id="681a0-364">It uses a helper class to manage the queue:</span></span>


```C++
template <class OP_TYPE>
class OpQueue : public IUnknown
{
public:

    typedef ComPtrList<OP_TYPE>   OpList;

    HRESULT QueueOperation(OP_TYPE *pOp);

protected:

    HRESULT ProcessQueue();
    HRESULT ProcessQueueAsync(IMFAsyncResult *pResult);

    virtual HRESULT DispatchOperation(OP_TYPE *pOp) = 0;
    virtual HRESULT ValidateOperation(OP_TYPE *pOp) = 0;

    OpQueue(CRITICAL_SECTION& critsec)
        : m_OnProcessQueue(this, &OpQueue::ProcessQueueAsync),
          m_critsec(critsec)
    {
    }

    virtual ~OpQueue()
    {
    }

protected:
    OpList                  m_OpQueue;         // Queue of operations.
    CRITICAL_SECTION&       m_critsec;         // Protects the queue state.
    AsyncCallback<OpQueue>  m_OnProcessQueue;  // ProcessQueueAsync callback.
};
```



<span data-ttu-id="681a0-365">Die- `OpQueue` Klasse ist so konzipiert, dass Sie von der Komponente geerbt wird, die asynchrone Arbeitsaufgaben ausführt.</span><span class="sxs-lookup"><span data-stu-id="681a0-365">The `OpQueue` class is designed to be inherited by the component that performs asynchronous work items.</span></span> <span data-ttu-id="681a0-366">Der *\_ typvorlagen Parameter op* ist der Objekttyp, der zum Darstellen von Arbeits Elementen in der Warteschlange verwendet wird – in diesem Fall ist der *op- \_ Typ* `SourceOp` .</span><span class="sxs-lookup"><span data-stu-id="681a0-366">The *OP\_TYPE* template parameter is the object type used to represent work items in the queue—in this case, *OP\_TYPE* will be `SourceOp`.</span></span> <span data-ttu-id="681a0-367">Die- `OpQueue` Klasse implementiert die folgenden Methoden:</span><span class="sxs-lookup"><span data-stu-id="681a0-367">The `OpQueue` class implements the following methods:</span></span>

-   <span data-ttu-id="681a0-368">`QueueOperation` Fügt ein neues Element in die Warteschlange ein.</span><span class="sxs-lookup"><span data-stu-id="681a0-368">`QueueOperation` puts a new item on the queue.</span></span>
-   <span data-ttu-id="681a0-369">`ProcessQueue` sendet den nächsten Vorgang aus der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="681a0-369">`ProcessQueue` dispatches the next operation from the queue.</span></span> <span data-ttu-id="681a0-370">Diese Methode ist asynchron.</span><span class="sxs-lookup"><span data-stu-id="681a0-370">This method is asynchronous.</span></span>
-   <span data-ttu-id="681a0-371">`ProcessQueueAsync` schließt die asynchrone- `ProcessQueue` Methode ab.</span><span class="sxs-lookup"><span data-stu-id="681a0-371">`ProcessQueueAsync` completes the asynchronous `ProcessQueue` method.</span></span>

<span data-ttu-id="681a0-372">Zwei weitere Methoden müssen von der abgeleiteten Klasse implementiert werden:</span><span class="sxs-lookup"><span data-stu-id="681a0-372">Another two methods must be implemented by the derived class:</span></span>

-   <span data-ttu-id="681a0-373">`ValidateOperation` überprüft, ob ein angegebener Vorgang aufgrund des aktuellen Status der Medienquelle gültig ist.</span><span class="sxs-lookup"><span data-stu-id="681a0-373">`ValidateOperation` checks whether it is valid to perform a specified operation, given the current state of the media source.</span></span>
-   <span data-ttu-id="681a0-374">`DispatchOperation` führt die asynchrone Arbeitsaufgabe aus.</span><span class="sxs-lookup"><span data-stu-id="681a0-374">`DispatchOperation` carries out the asynchronous work item.</span></span>

<span data-ttu-id="681a0-375">Die Vorgangs Warteschlange wird wie folgt verwendet:</span><span class="sxs-lookup"><span data-stu-id="681a0-375">The operation queue is used as follows:</span></span>

1.  <span data-ttu-id="681a0-376">Die Media Foundation Pipeline Ruft eine asynchrone Methode für die Medienquelle auf, z. b. [**imfmediasource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span><span class="sxs-lookup"><span data-stu-id="681a0-376">The Media Foundation pipeline calls an asynchronous method on the media source, such as [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span></span>
2.  <span data-ttu-id="681a0-377">Die asynchrone-Methode ruft `QueueOperation` auf, wodurch der [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) Vorgang in die Warteschlange versetzt und `ProcessQueue` (in Form eines- `SourceOp` Objekts) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="681a0-377">The asynchronous method calls `QueueOperation`, which puts the [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) operation on the queue and calls `ProcessQueue` (in the form of a `SourceOp` object).</span></span>
3.  <span data-ttu-id="681a0-378">`ProcessQueue` Ruft das [**mfputworkitem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem)-Element auf.</span><span class="sxs-lookup"><span data-stu-id="681a0-378">`ProcessQueue` calls [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem).</span></span>
4.  <span data-ttu-id="681a0-379">Der Arbeits Warteschlangen Thread ruft auf `ProcessQueueAsync` .</span><span class="sxs-lookup"><span data-stu-id="681a0-379">The work-queue thread calls `ProcessQueueAsync`.</span></span>
5.  <span data-ttu-id="681a0-380">Die `ProcessQueueAsync` -Methode ruft `ValidateOperation` und auf `DispatchOperation` .</span><span class="sxs-lookup"><span data-stu-id="681a0-380">The `ProcessQueueAsync` method calls `ValidateOperation` and `DispatchOperation`.</span></span>

<span data-ttu-id="681a0-381">Der folgende Code fügt einen neuen Vorgang für die MPEG-1-Quelle in die Warteschlange ein:</span><span class="sxs-lookup"><span data-stu-id="681a0-381">The following code queues a new operation on the MPEG-1 source:</span></span>


```C++
template <class OP_TYPE>
HRESULT OpQueue<OP_TYPE>::QueueOperation(OP_TYPE *pOp)
{
    HRESULT hr = S_OK;

    EnterCriticalSection(&m_critsec);

    hr = m_OpQueue.InsertBack(pOp);
    if (SUCCEEDED(hr))
    {
        hr = ProcessQueue();
    }

    LeaveCriticalSection(&m_critsec);
    return hr;
}
```



<span data-ttu-id="681a0-382">Der folgende Code verarbeitet die Warteschlange:</span><span class="sxs-lookup"><span data-stu-id="681a0-382">The following code processes the queue:</span></span>


```C++
template <class OP_TYPE>
HRESULT OpQueue<OP_TYPE>::ProcessQueue()
{
    HRESULT hr = S_OK;
    if (m_OpQueue.GetCount() > 0)
    {
        hr = MFPutWorkItem(
            MFASYNC_CALLBACK_QUEUE_STANDARD,    // Use the standard work queue.
            &m_OnProcessQueue,                  // Callback method.
            NULL                                // State object.
            );
    }
    return hr;
}
```



<span data-ttu-id="681a0-383">Die `ValidateOperation` -Methode überprüft, ob die MPEG-1-Quelle den nächsten Vorgang in der Warteschlange senden kann.</span><span class="sxs-lookup"><span data-stu-id="681a0-383">The `ValidateOperation` method checks whether the MPEG-1 source can dispatch the next operation in the queue.</span></span> <span data-ttu-id="681a0-384">Wenn ein anderer Vorgang ausgeführt wird, wird von `ValidateOperation` **MF \_ E \_ notakzeptierte** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="681a0-384">If another operation is in progress, `ValidateOperation` returns **MF\_E\_NOTACCEPTING**.</span></span> <span data-ttu-id="681a0-385">Dadurch wird sichergestellt, dass `DispatchOperation` nicht aufgerufen wird, während ein anderer Vorgang aussteht.</span><span class="sxs-lookup"><span data-stu-id="681a0-385">This ensures that `DispatchOperation` is not called while there is another operation pending.</span></span>


```C++
HRESULT MPEG1Source::ValidateOperation(SourceOp *pOp)
{
    if (m_pCurrentOp != NULL)
    {
        return MF_E_NOTACCEPTING;
    }
    return S_OK;
}
```



<span data-ttu-id="681a0-386">Die DispatchOperation-Methode schaltet den Vorgangstyp ein:</span><span class="sxs-lookup"><span data-stu-id="681a0-386">The DispatchOperation method switches on the operation type:</span></span>


```C++
//-------------------------------------------------------------------
// DispatchOperation
//
// Performs the asynchronous operation indicated by pOp.
//
// NOTE:
// This method implements the pure-virtual OpQueue::DispatchOperation
// method. It is always called from a work-queue thread.
//-------------------------------------------------------------------

HRESULT MPEG1Source::DispatchOperation(SourceOp *pOp)
{
    EnterCriticalSection(&m_critSec);

    HRESULT hr = S_OK;

    if (m_state == STATE_SHUTDOWN)
    {
        LeaveCriticalSection(&m_critSec);

        return S_OK; // Already shut down, ignore the request.
    }

    switch (pOp->Op())
    {

    // IMFMediaSource methods:

    case SourceOp::OP_START:
        hr = DoStart((StartOp*)pOp);
        break;

    case SourceOp::OP_STOP:
        hr = DoStop(pOp);
        break;

    case SourceOp::OP_PAUSE:
        hr = DoPause(pOp);
        break;

    // Operations requested by the streams:

    case SourceOp::OP_REQUEST_DATA:
        hr = OnStreamRequestSample(pOp);
        break;

    case SourceOp::OP_END_OF_STREAM:
        hr = OnEndOfStream(pOp);
        break;

    default:
        hr = E_UNEXPECTED;
    }

    if (FAILED(hr))
    {
        StreamingError(hr);
    }

    LeaveCriticalSection(&m_critSec);
    return hr;
}
```



<span data-ttu-id="681a0-387">Zusammenfassung:</span><span class="sxs-lookup"><span data-stu-id="681a0-387">To summarize:</span></span>

1.  <span data-ttu-id="681a0-388">Die Pipeline Ruft eine asynchrone Methode auf, z. b. [**imfmediasource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span><span class="sxs-lookup"><span data-stu-id="681a0-388">The pipeline calls an asynchronous method, such as [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).</span></span>
2.  <span data-ttu-id="681a0-389">Die asynchrone-Methode ruft `OpQueue::QueueOperation` auf und übergibt einen Zeiger auf ein- `SourceOp` Objekt.</span><span class="sxs-lookup"><span data-stu-id="681a0-389">The asynchronous method calls `OpQueue::QueueOperation`, passing in a pointer to a `SourceOp` object.</span></span>
3.  <span data-ttu-id="681a0-390">`QueueOperation`Mit der-Methode wird der-Vorgang in der Warteschlangen-Warteschlange von *m \_* angezeigt `OpQueue::ProcessQueue` .</span><span class="sxs-lookup"><span data-stu-id="681a0-390">The `QueueOperation` method puts the operation on the *m\_OpQueue* queue and calls `OpQueue::ProcessQueue`.</span></span>
4.  <span data-ttu-id="681a0-391">Die- `ProcessQueue` Methode ruft das [**mfputworkitem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem)-Element auf.</span><span class="sxs-lookup"><span data-stu-id="681a0-391">The `ProcessQueue` method calls [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem).</span></span> <span data-ttu-id="681a0-392">An diesem Punkt geschieht alles in einem Media Foundation Arbeits Warteschlangen Thread.</span><span class="sxs-lookup"><span data-stu-id="681a0-392">From this point, everything happens on a Media Foundation work-queue thread.</span></span> <span data-ttu-id="681a0-393">Die asynchrone Methode kehrt zum Aufrufer zurück.</span><span class="sxs-lookup"><span data-stu-id="681a0-393">The asynchronous method returns to the caller.</span></span>
5.  <span data-ttu-id="681a0-394">Der Arbeits Warteschlangen Thread ruft die- `OpQueue::ProcessQueueAsync` Methode auf.</span><span class="sxs-lookup"><span data-stu-id="681a0-394">The work-queue thread calls the `OpQueue::ProcessQueueAsync` method.</span></span>
6.  <span data-ttu-id="681a0-395">Die `ProcessQueueAsync` Methode ruft `MPEG1Source:ValidateOperation` auf, um den Vorgang zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="681a0-395">The `ProcessQueueAsync` method calls `MPEG1Source:ValidateOperation` to validate the operation.</span></span>
7.  <span data-ttu-id="681a0-396">Die- `ProcessQueueAsync` Methode ruft `MPEG1Source::DispatchOperation` auf, um den Vorgang zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="681a0-396">The `ProcessQueueAsync` method calls `MPEG1Source::DispatchOperation` to process the operation.</span></span>

<span data-ttu-id="681a0-397">Dieser Entwurf bietet mehrere Vorteile:</span><span class="sxs-lookup"><span data-stu-id="681a0-397">There are several benefits to this design:</span></span>

-   <span data-ttu-id="681a0-398">Methoden sind asynchron, sodass Sie den Thread der aufrufenden Anwendung nicht blockieren.</span><span class="sxs-lookup"><span data-stu-id="681a0-398">Methods are asynchronous, so they do not block the calling application's thread.</span></span>
-   <span data-ttu-id="681a0-399">Vorgänge werden an einen Media Foundation Arbeits Warteschlangen Thread gesendet, der von Pipeline Komponenten gemeinsam genutzt wird.</span><span class="sxs-lookup"><span data-stu-id="681a0-399">Operations are dispatched on a Media Foundation work-queue thread, which is shared among pipeline components.</span></span> <span data-ttu-id="681a0-400">Daher erstellt die Medienquelle keinen eigenen Thread und verringert so die Gesamtzahl der erstellten Threads.</span><span class="sxs-lookup"><span data-stu-id="681a0-400">Therefore, the media source does not create its own thread, reducing the total number of threads that are created.</span></span>
-   <span data-ttu-id="681a0-401">Die Medienquelle wird nicht blockiert, während auf den Abschluss des Vorgangs gewartet wird.</span><span class="sxs-lookup"><span data-stu-id="681a0-401">The media source does not block while waiting for operations to complete.</span></span> <span data-ttu-id="681a0-402">Dadurch wird die Wahrscheinlichkeit verringert, dass eine Medienquelle versehentlich einen Deadlock auslöst und den Kontextwechsel reduziert.</span><span class="sxs-lookup"><span data-stu-id="681a0-402">This reduces the chance that a media source will accidentally cause a deadlock, and helps to reduce context switching.</span></span>
-   <span data-ttu-id="681a0-403">Die Medienquelle kann asynchrone e/a-Vorgänge verwenden, um die Quelldatei zu lesen (durch Aufrufen von [**imfbytestream:: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread)).</span><span class="sxs-lookup"><span data-stu-id="681a0-403">The media source can use asynchronous I/O to read the source file (by calling [**IMFByteStream::BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread)).</span></span> <span data-ttu-id="681a0-404">Die Medienquelle muss beim Warten auf den Abschluss einer e/a-Routine nicht blockiert werden.</span><span class="sxs-lookup"><span data-stu-id="681a0-404">The media source does not need to block while waiting for I/O routine complete.</span></span>

<span data-ttu-id="681a0-405">Wenn Sie das im SDK-Beispiel gezeigte Muster befolgen, können Sie sich auf bestimmte Details der Medienquelle konzentrieren.</span><span class="sxs-lookup"><span data-stu-id="681a0-405">If you follow the pattern shown in the SDK sample, you can focus on the particular details of your media source.</span></span>

## <a name="related-topics"></a><span data-ttu-id="681a0-406">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="681a0-406">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="681a0-407">Medienquellen</span><span class="sxs-lookup"><span data-stu-id="681a0-407">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="681a0-408">Schreiben einer benutzerdefinierten Medienquelle</span><span class="sxs-lookup"><span data-stu-id="681a0-408">Writing a Custom Media Source</span></span>](writing-a-custom-media-source.md)
</dt> </dl>

 

 



