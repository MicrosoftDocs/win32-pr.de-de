---
description: Präsentations Deskriptoren
ms.assetid: 714c8bda-5ce1-47e2-ba73-9304e26b3129
title: Präsentations Deskriptoren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44f1581e35fe6d875c691efdd5ef5736c1aa5215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356845"
---
# <a name="presentation-descriptors"></a><span data-ttu-id="802ca-103">Präsentations Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="802ca-103">Presentation Descriptors</span></span>

<span data-ttu-id="802ca-104">Eine *Präsentation* ist ein Satz verwandter Mediendaten Ströme, die eine gemeinsame Präsentationszeit haben.</span><span class="sxs-lookup"><span data-stu-id="802ca-104">A *presentation* is a set of related media streams that share a common presentation time.</span></span> <span data-ttu-id="802ca-105">Eine Präsentation kann z. b. aus den Audio-und Videostreams von einem Film bestehen.</span><span class="sxs-lookup"><span data-stu-id="802ca-105">For example, a presentation might consist of the audio and video streams from a movie.</span></span> <span data-ttu-id="802ca-106">Ein *Präsentations Deskriptor* ist ein Objekt, das die Beschreibung einer bestimmten Präsentation enthält.</span><span class="sxs-lookup"><span data-stu-id="802ca-106">A *presentation descriptor* is an object that contains the description of a particular presentation.</span></span> <span data-ttu-id="802ca-107">Präsentations Deskriptoren werden verwendet, um Medienquellen und einige Medien senken zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="802ca-107">Presentation descriptors are used to configure media sources and some media sinks.</span></span>

<span data-ttu-id="802ca-108">Jeder Präsentations Deskriptor enthält eine Liste mit einem oder mehreren Daten *Strom Deskriptoren*.</span><span class="sxs-lookup"><span data-stu-id="802ca-108">Each presentation descriptor contains a list of one or more *stream descriptors*.</span></span> <span data-ttu-id="802ca-109">Diese beschreiben die Datenströme in der Präsentation.</span><span class="sxs-lookup"><span data-stu-id="802ca-109">These describe the streams in the presentation.</span></span> <span data-ttu-id="802ca-110">Datenströme können entweder ausgewählt oder deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="802ca-110">Streams can be either selected or deselected.</span></span> <span data-ttu-id="802ca-111">Nur die ausgewählten Streams führen zu Daten.</span><span class="sxs-lookup"><span data-stu-id="802ca-111">Only the selected streams produce data.</span></span> <span data-ttu-id="802ca-112">Nicht ausgewählte Streams sind nicht aktiv, und es werden keine Daten erzeugt.</span><span class="sxs-lookup"><span data-stu-id="802ca-112">Deselected streams are not active and do not produce any data.</span></span> <span data-ttu-id="802ca-113">Jeder Datenstrom Deskriptor verfügt über einen *Medientyp Handler*, der verwendet wird, um den Medientyp des Streams zu ändern oder den aktuellen Medientyp des Streams zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="802ca-113">Each stream descriptor has a *media type handler*, which is used to change the stream's media type or get the stream's current media type.</span></span> <span data-ttu-id="802ca-114">(Weitere Informationen zu Medientypen finden Sie unter [Medientypen](media-types.md).)</span><span class="sxs-lookup"><span data-stu-id="802ca-114">(For more information about media types, see [Media Types](media-types.md).)</span></span>

<span data-ttu-id="802ca-115">In der folgenden Tabelle werden die primären Schnittstellen angezeigt, die von den einzelnen Objekten verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="802ca-115">The following table shows the primary interfaces that each of these objects exposes.</span></span>



| <span data-ttu-id="802ca-116">Object</span><span class="sxs-lookup"><span data-stu-id="802ca-116">Object</span></span>                  | <span data-ttu-id="802ca-117">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="802ca-117">Interface</span></span>                                                      |
|-------------------------|----------------------------------------------------------------|
| <span data-ttu-id="802ca-118">Präsentations Deskriptor</span><span class="sxs-lookup"><span data-stu-id="802ca-118">Presentation descriptor</span></span> | [<span data-ttu-id="802ca-119">**IMF presentationdescriptor**</span><span class="sxs-lookup"><span data-stu-id="802ca-119">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) |
| <span data-ttu-id="802ca-120">Datenstrom Deskriptor</span><span class="sxs-lookup"><span data-stu-id="802ca-120">Stream descriptor</span></span>       | [<span data-ttu-id="802ca-121">**IMF-Deskriptor**</span><span class="sxs-lookup"><span data-stu-id="802ca-121">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)             |
| <span data-ttu-id="802ca-122">Medientyp Handler</span><span class="sxs-lookup"><span data-stu-id="802ca-122">Media type handler</span></span>      | [<span data-ttu-id="802ca-123">**IMF mediatypeer Handler**</span><span class="sxs-lookup"><span data-stu-id="802ca-123">**IMFMediaTypeHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)             |



 

## <a name="media-source-presentations"></a><span data-ttu-id="802ca-124">Medienquellen Präsentationen</span><span class="sxs-lookup"><span data-stu-id="802ca-124">Media Source Presentations</span></span>

<span data-ttu-id="802ca-125">Jede Medienquelle bietet einen Präsentations Deskriptor, der die Standardkonfiguration für die Quelle beschreibt.</span><span class="sxs-lookup"><span data-stu-id="802ca-125">Every media source provides a presentation descriptor that describes the default configuration for the source.</span></span> <span data-ttu-id="802ca-126">In der Standardkonfiguration ist mindestens ein Stream ausgewählt, und jeder ausgewählte Stream weist einen Medientyp auf.</span><span class="sxs-lookup"><span data-stu-id="802ca-126">In the default configuration, at least one stream is selected, and every selected stream has a media type.</span></span> <span data-ttu-id="802ca-127">Um den Präsentations Deskriptor abzurufen, nennen Sie [**imfmediasource:: foratepresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="802ca-127">To get the presentation descriptor, call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span> <span data-ttu-id="802ca-128">Die-Methode gibt einen [**IMF presentationdescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) -Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="802ca-128">The method returns an [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) pointer.</span></span>

<span data-ttu-id="802ca-129">Sie können den Präsentations Deskriptor der Quelle ändern, um einen anderen Satz von Streams auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="802ca-129">You can modify the source's presentation descriptor to select a different set of streams.</span></span> <span data-ttu-id="802ca-130">Ändern Sie den Präsentations Deskriptor nicht, es sei denn, die Medienquelle wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="802ca-130">Do not modify the presentation descriptor unless the media source is stopped.</span></span> <span data-ttu-id="802ca-131">Die Änderungen werden angewendet, wenn Sie [**imfmediasource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) zum Starten der Quelle aufruft.</span><span class="sxs-lookup"><span data-stu-id="802ca-131">The changes are applied when you call [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) to start the source.</span></span>

<span data-ttu-id="802ca-132">Um die Anzahl der Streams abzurufen, nennen Sie [**imfpresentationdescriptor:: getstreamdescriptorcount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount).</span><span class="sxs-lookup"><span data-stu-id="802ca-132">To get the number of streams, call [**IMFPresentationDescriptor::GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount).</span></span> <span data-ttu-id="802ca-133">Um den Datenstrom Deskriptor für einen Stream abzurufen, nennen Sie [**imfpresentationdescriptor:: getstreamdescriptorbyindex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) , und übergeben Sie den Index des Datenstroms.</span><span class="sxs-lookup"><span data-stu-id="802ca-133">To get the stream descriptor for a stream, call [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) and pass in the index of the stream.</span></span> <span data-ttu-id="802ca-134">Streams werden von 0 (null) indiziert.</span><span class="sxs-lookup"><span data-stu-id="802ca-134">Streams are indexed from zero.</span></span> <span data-ttu-id="802ca-135">Die **getstreamdescriptorbyindex** -Methode gibt einen [**IMF streamdescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) -Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="802ca-135">The **GetStreamDescriptorByIndex** method returns an [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) pointer.</span></span> <span data-ttu-id="802ca-136">Außerdem wird ein boolesches Flag zurückgegeben, das angibt, ob der Stream ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="802ca-136">It also returns a Boolean flag indicating whether the stream is selected.</span></span> <span data-ttu-id="802ca-137">Wenn der Stream ausgewählt ist, erzeugt die Medienquelle Daten für diesen Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="802ca-137">If the stream is selected, the media source produces data for that stream.</span></span> <span data-ttu-id="802ca-138">Andernfalls erzeugt die Quelle keine Daten für diesen Stream.</span><span class="sxs-lookup"><span data-stu-id="802ca-138">Otherwise, the source does not produce any data for that stream.</span></span> <span data-ttu-id="802ca-139">Um einen Stream auszuwählen, wenden Sie [**imfpresentationdescriptor:: selectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) mit dem Index des Streams an.</span><span class="sxs-lookup"><span data-stu-id="802ca-139">To select a stream, call [**IMFPresentationDescriptor::SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) with the index of the stream.</span></span> <span data-ttu-id="802ca-140">Um die Auswahl eines Streams zu deaktivieren, nennen Sie [**imfpresentationdescriptor::D eselectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream).</span><span class="sxs-lookup"><span data-stu-id="802ca-140">To deselect a stream, call [**IMFPresentationDescriptor::DeselectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream).</span></span>

<span data-ttu-id="802ca-141">Der folgende Code zeigt, wie der Präsentations Deskriptor aus einer Medienquelle abgerufen und die Streams aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="802ca-141">The following code shows how to get the presentation descriptor from a media source and enumerate the streams.</span></span>


```C++
HRESULT hr = S_OK;
DWORD cStreams = 0;
BOOL  fSelected = FALSE;

IMFPresentationDescriptor *pPresentation = NULL;
IMFStreamDescriptor *pStreamDesc = NULL;

hr = pSource->CreatePresentationDescriptor(&pPresentation);

if (SUCCEEDED(hr))
{
    hr = pPresentation->GetStreamDescriptorCount(&cStreams);
}

if (SUCCEEDED(hr))
{
    for (DWORD iStream = 0; iStream < cStreams; iStream++)
    {
        hr = pPresentation->GetStreamDescriptorByIndex(
            iStream, &fSelected, &pStreamDesc);

        if (FAILED(hr))
        {
            break;
        }

        /*  Use the stream descriptor. (Not shown.) */

        SAFE_RELEASE(pStreamDesc);
    }
}
SAFE_RELEASE(pPresentation);
SAFE_RELEASE(pStreamDesc);
```



## <a name="media-type-handlers"></a><span data-ttu-id="802ca-142">Medientyp Handler</span><span class="sxs-lookup"><span data-stu-id="802ca-142">Media Type Handlers</span></span>

<span data-ttu-id="802ca-143">Um den Medientyp des Streams zu ändern oder um den aktuellen Medientyp des Streams zu erhalten, verwenden Sie den Medientyp Handler des Stream-Deskriptors.</span><span class="sxs-lookup"><span data-stu-id="802ca-143">To change the stream's media type or to get the stream's current media type, use the stream descriptor's media type handler.</span></span> <span data-ttu-id="802ca-144">Aufrufen von [**imfstreamdescriptor:: getmediatypeer Handler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) zum Abrufen des Medientyp Handlers.</span><span class="sxs-lookup"><span data-stu-id="802ca-144">Call [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) to get the media type handler.</span></span> <span data-ttu-id="802ca-145">Diese Methode gibt einen [**IMF Media**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) Type-Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="802ca-145">This method returns an [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) pointer.</span></span>

<span data-ttu-id="802ca-146">Wenn Sie einfach wissen möchten, welche Art von Daten im Stream ist (z. b. Audiodaten oder Videos), nennen Sie [**imfmediatyphandler:: getmajortype**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype).</span><span class="sxs-lookup"><span data-stu-id="802ca-146">If you simply want to know what kind of data is in the stream, such as audio or video, call [**IMFMediaTypeHandler::GetMajorType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype).</span></span> <span data-ttu-id="802ca-147">Diese Methode gibt die GUID für den Haupt Medientyp zurück.</span><span class="sxs-lookup"><span data-stu-id="802ca-147">This method returns the GUID for the major media type.</span></span> <span data-ttu-id="802ca-148">Beispielsweise verbindet eine Wiedergabe Anwendung in der Regel einen Audiodatenstrom mit dem audiorenderer und einem Videostream mit dem Videorenderer.</span><span class="sxs-lookup"><span data-stu-id="802ca-148">For example, a playback application typically connects an audio stream to the audio renderer and a video stream to the video renderer.</span></span> <span data-ttu-id="802ca-149">Wenn Sie die Medien Sitzung oder das topologielader verwenden, um eine Topologie zu erstellen, ist die GUID des Haupt Typs möglicherweise die einzigen Formatinformationen, die Sie benötigen.</span><span class="sxs-lookup"><span data-stu-id="802ca-149">If you use the Media Session or the topology loader to build a topology, the major type GUID might be the only format information that you need.</span></span>

<span data-ttu-id="802ca-150">Wenn Ihre Anwendung ausführlichere Informationen zum aktuellen Format benötigt, müssen Sie [**imfmediatyphandler:: getcurrentmediatype**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="802ca-150">If your application needs more detailed information about the current format, call [**IMFMediaTypeHandler::GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype).</span></span> <span data-ttu-id="802ca-151">Diese Methode gibt einen Zeiger auf die [**imfmediatype**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) -Schnittstelle des Medientyps zurück.</span><span class="sxs-lookup"><span data-stu-id="802ca-151">This method returns a pointer to the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface of the media type.</span></span> <span data-ttu-id="802ca-152">Verwenden Sie diese Schnittstelle, um die Details des Formats zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="802ca-152">Use this interface to get the details of the format.</span></span>

<span data-ttu-id="802ca-153">Der Medientyp Handler enthält außerdem eine Liste der unterstützten Medientypen für den Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="802ca-153">The media type handler also contains a list of supported media types for the stream.</span></span> <span data-ttu-id="802ca-154">Um die Größe der Liste abzurufen, nennen Sie [**imfmediatypehandler:: getmediatypecount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount).</span><span class="sxs-lookup"><span data-stu-id="802ca-154">To get the size of the list, call [**IMFMediaTypeHandler::GetMediaTypeCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount).</span></span> <span data-ttu-id="802ca-155">Um einen Medientyp aus der Liste abzurufen, nennen Sie [**imfmediatypeer Handler:: getmediatypeer byindex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) mit dem Index des Medientyps.</span><span class="sxs-lookup"><span data-stu-id="802ca-155">To get a media type from the list, call [**IMFMediaTypeHandler::GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) with the index of the media type.</span></span> <span data-ttu-id="802ca-156">Medientypen werden in der ungefähren Reihenfolge der bevorzugte Reihenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="802ca-156">Media types are returned in the approximate order of preference.</span></span> <span data-ttu-id="802ca-157">Für Audioformate werden z. b. höhere Stichproben Raten gegenüber niedrigeren Stichproben Raten bevorzugt.</span><span class="sxs-lookup"><span data-stu-id="802ca-157">For example, for audio formats, higher sample rates are preferred over lower sample rates.</span></span> <span data-ttu-id="802ca-158">Es gibt jedoch keine definitive Regel, die die Reihenfolge bestimmt, sodass Sie Sie einfach als Richtlinie behandeln sollten.</span><span class="sxs-lookup"><span data-stu-id="802ca-158">However, there is no definitive rule that governs the ordering, so you should treat it simply as a guideline.</span></span>

<span data-ttu-id="802ca-159">Die Liste der unterstützten Typen darf nicht alle möglichen Medientypen enthalten, die der Stream unterstützt.</span><span class="sxs-lookup"><span data-stu-id="802ca-159">The list of supported types might not contain every possible media type that the stream supports.</span></span> <span data-ttu-id="802ca-160">Um zu testen, ob ein bestimmter Medientyp unterstützt wird, nennen Sie [**imfmediatypehandler:: ismediatypesupportiert**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-ismediatypesupported).</span><span class="sxs-lookup"><span data-stu-id="802ca-160">To test whether a particular media type is supported, call [**IMFMediaTypeHandler::IsMediaTypeSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-ismediatypesupported).</span></span> <span data-ttu-id="802ca-161">Um den Medientyp festzulegen, müssen Sie [**imfmediatyphandler:: setcurrentmediatype**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="802ca-161">To set the media type, call [**IMFMediaTypeHandler::SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype).</span></span> <span data-ttu-id="802ca-162">Wenn die Methode erfolgreich ausgeführt wird, enthält der Stream Daten, die dem angegebenen Format entsprechen.</span><span class="sxs-lookup"><span data-stu-id="802ca-162">If the method succeeds, the stream will contain data that conforms to the specified format.</span></span> <span data-ttu-id="802ca-163">Die **setcurrentmediatype** -Methode ändert nicht die Liste der bevorzugten Typen.</span><span class="sxs-lookup"><span data-stu-id="802ca-163">The **SetCurrentMediaType** method does not change the list of preferred types.</span></span>

<span data-ttu-id="802ca-164">Der folgende Code zeigt, wie Sie den Medientyp Handler, die bevorzugten Medientypen aufzählen und den Medientyp festlegen.</span><span class="sxs-lookup"><span data-stu-id="802ca-164">The following code shows how to get the media type handler, enumerate the preferred media types, and set the media type.</span></span> <span data-ttu-id="802ca-165">In diesem Beispiel wird davon ausgegangen, dass die Anwendung über einen Algorithmus verfügt, der hier nicht angezeigt wird, um den Medientyp auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="802ca-165">This example assumes that the application has some algorithm, not shown here, for selecting the media type.</span></span> <span data-ttu-id="802ca-166">Die Besonderheiten hängen stark von Ihrer Anwendung ab.</span><span class="sxs-lookup"><span data-stu-id="802ca-166">The specifics will depend greatly on your application.</span></span>


```C++
HRESULT hr = S_OK;
DWORD cTypes = 0;
BOOL  bTypeOK = FALSE;

IMFMediaTypeHandler *pHandler = NULL;
IMFMediaType *pMediaType = NULL;

hr = pStreamDesc->GetMediaTypeHandler(&pHandler);

if (SUCCEEDED(hr))
{
    hr = pHandler->GetMediaTypeCount(&cTypes);
}

if (SUCCEEDED(hr))
{
    for (DWORD iType = 0; iType < cTypes; iType++)
    {   
        hr = pHandler->GetMediaTypeByIndex(iType, &pMediaType);

        if (FAILED(hr))
        {
            break;
        }

        /* Examine the media type. (Not shown.)  */

        /* If this media type is acceptable, set the media type. */

        if (bTypeOK)
        {
            hr = pHandler->SetCurrentMediaType(pMediaType);
            break;
        }

        SAFE_RELEASE(pMediaType);
    }
}    

SAFE_RELEASE(pMediaType);
SAFE_RELEASE(pHandler);
```



## <a name="related-topics"></a><span data-ttu-id="802ca-167">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="802ca-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="802ca-168">Medienquellen</span><span class="sxs-lookup"><span data-stu-id="802ca-168">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="802ca-169">Media Foundation Plattform-APIs</span><span class="sxs-lookup"><span data-stu-id="802ca-169">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 



