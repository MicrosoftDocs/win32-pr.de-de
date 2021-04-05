---
title: Informationen über imediaobject
description: Informationen über imediaobject
ms.assetid: c483f74a-efd8-4a9f-a719-686099755e63
keywords:
- Windows Media Player-Plug-ins, Schnittstellen
- Plug-ins, Schnittstellen
- Plug-Ins für die digitale Signalverarbeitung, Schnittstellen
- DSP-Plug-ins, Schnittstellen
- Schnittstellen, DSP-Plug-ins
- Windows Media Player-Plug-ins, imediaobject-Schnittstelle
- Plug-ins, imediaobject-Schnittstelle
- Plug-Ins für die digitale Signalverarbeitung, imediaobject-Schnittstelle
- DSP-Plug-ins, imediaobject-Schnittstelle
- Imediaobject-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfbbecd749242b67bc5c8f36b3c7a2c0a5fbe461
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708046"
---
# <a name="about-imediaobject"></a><span data-ttu-id="20a12-113">Informationen über imediaobject</span><span class="sxs-lookup"><span data-stu-id="20a12-113">About IMediaObject</span></span>

<span data-ttu-id="20a12-114">Die **imediaobject** -Schnittstelle ist die erforderliche Schnittstelle für DMOS.</span><span class="sxs-lookup"><span data-stu-id="20a12-114">The **IMediaObject** interface is the required interface for DMOs.</span></span> <span data-ttu-id="20a12-115">**Imediaobject** enthält die Methoden, die ein Windows Media Player DSP-Plug-in verwendet, um Daten aus Windows Media Player zu erhalten, die Daten zu verarbeiten und die verarbeiteten Daten an Windows Media Player zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="20a12-115">**IMediaObject** contains the methods that a Windows Media Player DSP plug-in uses to get data from Windows Media Player, to process the data, and to return the processed data to Windows Media Player.</span></span> <span data-ttu-id="20a12-116">Eine umfassende Dokumentation der **imediaobject** -Schnittstelle finden Sie im Abschnitt DirectShow des Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="20a12-116">For complete documentation of the **IMediaObject** interface, see the DirectShow section of the Windows SDK.</span></span>

<span data-ttu-id="20a12-117">Die Methoden von **imediaobject** können wie folgt kategorisiert werden:</span><span class="sxs-lookup"><span data-stu-id="20a12-117">The methods of **IMediaObject** can be categorized as follows:</span></span>

## <a name="methods-that-handle-format-negotiation"></a><span data-ttu-id="20a12-118">Methoden, die die Format Aushandlung behandeln</span><span class="sxs-lookup"><span data-stu-id="20a12-118">Methods that Handle Format Negotiation</span></span>

<span data-ttu-id="20a12-119">Dies sind die Methoden, die von Windows Media Player aufgerufen werden, um Informationen zu den vom Plug-in unterstützten Datenformaten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="20a12-119">These are the methods that Windows Media Player calls to get information about the data formats supported by the plug-in.</span></span> <span data-ttu-id="20a12-120">Diese Methoden umfassen:</span><span class="sxs-lookup"><span data-stu-id="20a12-120">These methods include:</span></span>

-   <span data-ttu-id="20a12-121">**Getinputmaxlatency**</span><span class="sxs-lookup"><span data-stu-id="20a12-121">**GetInputMaxLatency**</span></span>
-   <span data-ttu-id="20a12-122">**Getinputsizone FO**</span><span class="sxs-lookup"><span data-stu-id="20a12-122">**GetInputSizeInfo**</span></span>
-   <span data-ttu-id="20a12-123">**Getinputstreaminfo**</span><span class="sxs-lookup"><span data-stu-id="20a12-123">**GetInputStreamInfo**</span></span>
-   <span data-ttu-id="20a12-124">**Getinputtype**</span><span class="sxs-lookup"><span data-stu-id="20a12-124">**GetInputType**</span></span>
-   <span data-ttu-id="20a12-125">**Getoutputsizone FO**</span><span class="sxs-lookup"><span data-stu-id="20a12-125">**GetOutputSizeInfo**</span></span>
-   <span data-ttu-id="20a12-126">**Getoutputstreaminfo**</span><span class="sxs-lookup"><span data-stu-id="20a12-126">**GetOutputStreamInfo**</span></span>
-   <span data-ttu-id="20a12-127">**Getoutputtype**</span><span class="sxs-lookup"><span data-stu-id="20a12-127">**GetOutputType**</span></span>
-   <span data-ttu-id="20a12-128">**Getstreamcount**</span><span class="sxs-lookup"><span data-stu-id="20a12-128">**GetStreamCount**</span></span>
-   <span data-ttu-id="20a12-129">**"* Tinputmaxlatency"*\*</span><span class="sxs-lookup"><span data-stu-id="20a12-129">**SetInputMaxLatency**</span></span>
-   <span data-ttu-id="20a12-130">**"Ttinputtype"**</span><span class="sxs-lookup"><span data-stu-id="20a12-130">**SetInputType**</span></span>
-   <span data-ttu-id="20a12-131">**Setoutputtype**</span><span class="sxs-lookup"><span data-stu-id="20a12-131">**SetOutputType**</span></span>

<span data-ttu-id="20a12-132">Einige dieser Methoden, wie z. b. **getinputtype** und " **abtinputtype**", verwenden die **DMO- \_ \_ Medientyp** Struktur, um das Format der Daten zu beschreiben, die von einem Stream verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="20a12-132">Several of these methods, such as **GetInputType** and **SetInputType**, use the **DMO\_MEDIA\_TYPE** structure to describe the format of the data used by a stream.</span></span> <span data-ttu-id="20a12-133">Wenn diese Methoden von Windows Media Player aufgerufen werden, wird ein Zeiger auf eine **DMO- \_ \_ Medientyp** Struktur bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="20a12-133">When Windows Media Player calls these methods, it provides a pointer to a **DMO\_MEDIA\_TYPE** structure.</span></span> <span data-ttu-id="20a12-134">Wenn eine Methode wie z. b. " **stinputtype** " die Medientyp Informationen angibt, muss das Plug-in die **DMO- \_ \_ Medientyp** Struktur in eine Member-Variable kopieren und deren Datenmember überprüfen, um den Datentyp zu bestimmen, den Windows Media Player im Eingabepuffer bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="20a12-134">If a method such as **SetInputType** specifies the media type information, the plug-in should copy the **DMO\_MEDIA\_TYPE** structure to a member variable and inspect its data members to determine the type of data that Windows Media Player will provide in the input buffer.</span></span> <span data-ttu-id="20a12-135">Wenn eine Methode, wie z. b. **getinputtype** , die Medientyp Informationen abruft, muss das Plug-in die Adresse der Element Variablen mit der Struktur des **DMO- \_ Medien \_ Typs** in den von Windows Media Player in der Parameterliste bereitgestellten Zeiger kopieren.</span><span class="sxs-lookup"><span data-stu-id="20a12-135">If a method such as **GetInputType** retrieves the media type information, the plug-in should copy the address of the member variable containing the **DMO\_MEDIA\_TYPE** structure to the pointer provided by Windows Media Player in the parameter list.</span></span>

<span data-ttu-id="20a12-136">Windows Media Player verwendet hauptsächlich zwei Member der **DMO \_ - \_ Medientyp** Struktur:</span><span class="sxs-lookup"><span data-stu-id="20a12-136">Windows Media Player mainly uses two members of the **DMO\_MEDIA\_TYPE** structure:</span></span>

-   <span data-ttu-id="20a12-137">**majortype**: eine Globally Unique Identifier (GUID), die die Gesamtkategorie der Medien angibt, z. b. Audiodaten oder Videos.</span><span class="sxs-lookup"><span data-stu-id="20a12-137">**majortype**: A globally unique identifier (GUID) that specifies the overall category of the media, such as audio or video.</span></span>
-   <span data-ttu-id="20a12-138">**Untertyp**: eine GUID, die eine ausführlichere Beschreibung der Medien angibt, z. b. PCM-Audiodaten.</span><span class="sxs-lookup"><span data-stu-id="20a12-138">**subtype**: A GUID that specifies a more detailed description of the media, such as PCM audio.</span></span>

<span data-ttu-id="20a12-139">Diese GUIDs befinden sich im Header "UUIDs. h", der in der Windows SDK enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="20a12-139">These GUIDs can be found in the header named uuids.h, which is included with the Windows SDK.</span></span>

<span data-ttu-id="20a12-140">Methoden wie z. b. **getinputsizeinfo** stellen Informationen für Windows Media Player bereit, wie viel Arbeitsspeicher zum Zuordnen der Verarbeitungs Puffer erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="20a12-140">Methods such as **GetInputSizeInfo** provide information to Windows Media Player about how much memory is required to allocate the processing buffers.</span></span> <span data-ttu-id="20a12-141">Methoden wie **getstreamcount** und **getoutputstreaminfo** stellen Windows-Media Player Informationen über die Anzahl und das Zeichen der Streams bereit, die vom DSP-Plug-in unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="20a12-141">Methods such as **GetStreamCount** and **GetOutputStreamInfo** provide information to Windows Media Player about the number and character of the streams supported by the DSP plug-in.</span></span>

<span data-ttu-id="20a12-142">" **Getinputmaxlatency** " und "\* **tinputmaxlatency** " werden in besonderen Fällen von dmos implementiert.</span><span class="sxs-lookup"><span data-stu-id="20a12-142">**GetInputMaxLatency** and **SetInputMaxLatency** are implemented by DMOs in special cases.</span></span> <span data-ttu-id="20a12-143">Windows Media Player DSP-Plug-Ins müssen E \_ notimpl zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="20a12-143">Windows Media Player DSP plug-ins should return E\_NOTIMPL.</span></span>

## <a name="methods-that-specify-or-retrieve-state-information"></a><span data-ttu-id="20a12-144">Methoden zum angeben oder Abrufen von Zustandsinformationen</span><span class="sxs-lookup"><span data-stu-id="20a12-144">Methods that Specify or Retrieve State Information</span></span>

<span data-ttu-id="20a12-145">Dies sind die Methoden, die von Windows Media Player aufgerufen werden, um Werte im Zusammenhang mit dem aktuellen Status des Plug-ins zu erhalten oder festzulegen.</span><span class="sxs-lookup"><span data-stu-id="20a12-145">These are the methods that Windows Media Player calls to get or set values related to the current state of the plug-in.</span></span> <span data-ttu-id="20a12-146">Diese Methoden umfassen:</span><span class="sxs-lookup"><span data-stu-id="20a12-146">These methods include:</span></span>

-   <span data-ttu-id="20a12-147">**Getinputcurrenttype**</span><span class="sxs-lookup"><span data-stu-id="20a12-147">**GetInputCurrentType**</span></span>
-   <span data-ttu-id="20a12-148">**Getinputstatus**</span><span class="sxs-lookup"><span data-stu-id="20a12-148">**GetInputStatus**</span></span>
-   <span data-ttu-id="20a12-149">**Getoutputcurrenttype**</span><span class="sxs-lookup"><span data-stu-id="20a12-149">**GetOutputCurrentType**</span></span>

<span data-ttu-id="20a12-150">**Getinputcurrenttype** und **getoutputcurrenttype** verwenden die **DMO \_ - \_ Medientyp** Struktur zum Zurückgeben von Informationen an Windows Media Player zu den zuvor festgelegten Medientypen für die Eingabe-und Ausgabestreams.</span><span class="sxs-lookup"><span data-stu-id="20a12-150">**GetInputCurrentType** and **GetOutputCurrentType** use the **DMO\_MEDIA\_TYPE** structure to return information to Windows Media Player about the media types previously set for the input and output streams.</span></span> <span data-ttu-id="20a12-151">**Getinputstatus** gibt ein Flag zurück, das Windows Media Player angibt, ob das DSP-Plug-in Eingabedaten akzeptieren kann.</span><span class="sxs-lookup"><span data-stu-id="20a12-151">**GetInputStatus** returns a flag that tells Windows Media Player whether the DSP plug-in can accept input data.</span></span>

## <a name="methods-that-handle-buffering-and-processing-data"></a><span data-ttu-id="20a12-152">Methoden, die die Pufferung und Verarbeitung von Daten verarbeiten</span><span class="sxs-lookup"><span data-stu-id="20a12-152">Methods that Handle Buffering and Processing Data</span></span>

<span data-ttu-id="20a12-153">Dies sind die Methoden, die von Windows Media Player aufgerufen werden, um die verschiedenen Prozesse zu initiieren, die das Plug-in für die digitale Signalverarbeitung durchführt.</span><span class="sxs-lookup"><span data-stu-id="20a12-153">These are the methods that Windows Media Player calls to initiate the various processes that the plug-in performs to do the digital signal processing.</span></span> <span data-ttu-id="20a12-154">Diese Methoden umfassen:</span><span class="sxs-lookup"><span data-stu-id="20a12-154">These methods include:</span></span>

-   <span data-ttu-id="20a12-155">**"" Zugeordnet**</span><span class="sxs-lookup"><span data-stu-id="20a12-155">**AllocateStreamingResources**</span></span>
-   <span data-ttu-id="20a12-156">**Diskontinuität**</span><span class="sxs-lookup"><span data-stu-id="20a12-156">**Discontinuity**</span></span>
-   <span data-ttu-id="20a12-157">**Leerung**</span><span class="sxs-lookup"><span data-stu-id="20a12-157">**Flush**</span></span>
-   <span data-ttu-id="20a12-158">**Freestreamingresources**</span><span class="sxs-lookup"><span data-stu-id="20a12-158">**FreeStreamingResources**</span></span>
-   <span data-ttu-id="20a12-159">**Sperre**</span><span class="sxs-lookup"><span data-stu-id="20a12-159">**Lock**</span></span>
-   <span data-ttu-id="20a12-160">**ProcessInput**</span><span class="sxs-lookup"><span data-stu-id="20a12-160">**ProcessInput**</span></span>
-   <span data-ttu-id="20a12-161">**ProcessOutput**</span><span class="sxs-lookup"><span data-stu-id="20a12-161">**ProcessOutput**</span></span>

<span data-ttu-id="20a12-162">In Windows Media Player werden **zuordungsoramingresources** und **freestreamingresources** aufgerufen, um dem DSP-Plug-in die Möglichkeit zu geben, zusätzliche Puffer einzurichten oder freizugeben, die das Plug-in möglicherweise für die interne Verarbeitung benötigt.</span><span class="sxs-lookup"><span data-stu-id="20a12-162">Windows Media Player calls **AllocateStreamingResources** and **FreeStreamingResources** to provide the DSP plug-in with an opportunity to set up or release any additional buffers the plug-in may require for internal processing.</span></span>

<span data-ttu-id="20a12-163">Windows Media Player DSP-Plug-Ins müssen die DMO- **Diskontinuitäts** Methode nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="20a12-163">Windows Media Player DSP plug-ins do not need to use the DMO **Discontinuity** method.</span></span>

<span data-ttu-id="20a12-164">Windows Media Player ruft **Flush** auf, um das DSP-Plug-in anzuweisen, alle intern gepufferten Daten zu leeren.</span><span class="sxs-lookup"><span data-stu-id="20a12-164">Windows Media Player calls **Flush** to direct the DSP plug-in to flush all internally buffered data.</span></span> <span data-ttu-id="20a12-165">Das Plug-in sollte alle Verweise auf **imediabuffer** -Schnittstellen freigeben, alle Werte, die den Zeitstempel oder die Stichproben Länge für den Medien Puffer angeben, löschen und alle internen Zustände erneut initialisieren, die vom Inhalt des Mediums "Sample" abhängen.</span><span class="sxs-lookup"><span data-stu-id="20a12-165">The plug-in should release any references to **IMediaBuffer** interfaces, clear any values that specify the time stamp or sample length for the media buffer, and reinitialize any internal states that depend upon the contents of the media sample.</span></span>

<span data-ttu-id="20a12-166">Windows Media Player ruft ProcessInput auf, um einen Zeiger auf eine **imediabuffer** -Schnittstelle an das DSP-Plug-in zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="20a12-166">Windows Media Player calls ProcessInput to pass a pointer to an **IMediaBuffer** interface to the DSP plug-in.</span></span> <span data-ttu-id="20a12-167">Diese Schnittstelle ermöglicht den Zugriff auf den von Windows Media Player zugeordneten Eingabepuffer zum Bereitstellen von Daten für das Plug-in.</span><span class="sxs-lookup"><span data-stu-id="20a12-167">This interface provides access to the input buffer allocated by Windows Media Player to supply data to the plug-in.</span></span> <span data-ttu-id="20a12-168">Windows Media Player anschließend **ProcessOutput** aufrufen, um einen Zeiger auf eine **imediabuffer** -Schnittstelle zu übergeben, die Zugriff auf den von Windows Media Player zugeordneten Ausgabepuffer ermöglicht, um die verarbeiteten Daten aus dem DSP-Plug-in zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="20a12-168">Windows Media Player subsequently calls **ProcessOutput** to pass a pointer to an **IMediaBuffer** interface that provides access to the output buffer allocated by Windows Media Player to receive the processed data from the DSP plug-in.</span></span>

<span data-ttu-id="20a12-169">Die **imediaobject** -Schnittstelle enthält eine Methode mit dem Namen **Lock**.</span><span class="sxs-lookup"><span data-stu-id="20a12-169">The **IMediaObject** interface includes a method named **Lock**.</span></span> <span data-ttu-id="20a12-170">Diese Methode ist dafür konzipiert, eine Sperre für den DMO abzurufen oder freizugeben, damit DMO beim Ausführen mehrerer Vorgänge serialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="20a12-170">This method is designed to acquire or release a lock on the DMO to keep the DMO serialized when performing multiple operations.</span></span> <span data-ttu-id="20a12-171">Die Version von **imediaobject:: Lock** im Assistenten Code überschreibt die ATL-Implementierung von **Lock**.</span><span class="sxs-lookup"><span data-stu-id="20a12-171">The version of **IMediaObject::Lock** in the wizard code overrides the ATL implementation of **Lock**.</span></span> <span data-ttu-id="20a12-172">Da Windows Media Player Aufrufe an die DMO-Schnittstelle eines DSP-Plug-ins serialisiert, gibt die Implementierung von **Lock** einfach S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="20a12-172">Because Windows Media Player serializes calls made to the DMO interface of a DSP plug-in, the implementation of **Lock** simply returns S\_OK.</span></span> <span data-ttu-id="20a12-173">Ausführliche Informationen zum Erstellen eines Multithread-DMO finden Sie im Abschnitt DirectShow des Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="20a12-173">For details about how to create a multithreaded DMO, refer to the DirectShow section of the Windows SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="20a12-174">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="20a12-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20a12-175">**Erforderliche Schnittstellen**</span><span class="sxs-lookup"><span data-stu-id="20a12-175">**Required Interfaces**</span></span>](required-interfaces.md)
</dt> </dl>

 

 




