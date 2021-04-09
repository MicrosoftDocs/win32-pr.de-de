---
title: Unterstützung mehrerer Sprachen
description: Unterstützung mehrerer Sprachen
ms.assetid: b0061de4-d725-455f-9d9b-5bd0dbe8ff53
keywords:
- Windows Media-Format-SDK, Unterstützung für mehrere Sprachen
- Windows Media-Format-SDK, Unterstützung mehrerer Sprachen
- Windows Media-Format-SDK, Sprachunterstützung
- Advanced Systems Format (ASF), Unterstützung für mehrere Sprachen
- ASF (Advanced Systems Format), Unterstützung mehrerer Sprachen
- Advanced Systems Format (ASF), Unterstützung mehrerer Sprachen
- ASF (Advanced Systems Format), Unterstützung mehrerer Sprachen
- Advanced Systems Format (ASF), Sprachunterstützung
- ASF (Advanced Systems Format), Sprachunterstützung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc070bda1cc25c6b7fd0fa583a8ac63a55fa603
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "103948508"
---
# <a name="to-support-multiple-languages"></a><span data-ttu-id="95101-112">Unterstützung mehrerer Sprachen</span><span class="sxs-lookup"><span data-stu-id="95101-112">To Support Multiple Languages</span></span>

<span data-ttu-id="95101-113">Sie können mehrere Sprachen in Streams und Metadaten unterstützen.</span><span class="sxs-lookup"><span data-stu-id="95101-113">You can support multiple languages both in streams and in metadata.</span></span> <span data-ttu-id="95101-114">Der Kern der Unterstützung mehrerer Sprachen im Windows Media-Format-SDK ist die [**iwmlanguagelist**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) -Schnittstelle, die eine Liste der unterstützten Sprachen verwaltet.</span><span class="sxs-lookup"><span data-stu-id="95101-114">The core of multiple language support in the Windows Media Format SDK is the [**IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) interface, which maintains a list of the languages supported.</span></span> <span data-ttu-id="95101-115">Die Sprachliste gibt jeder unterstützten Sprache einen Index, der in verschiedenen Objekten im SDK verwendet wird, wenn mehrere Sprachen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="95101-115">The language list gives each supported language an index, which is used in various objects in the SDK when dealing with the multiple languages.</span></span>

<span data-ttu-id="95101-116">Die [**iwmlanguagelist:: AddLanguageByRFC1766String**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-addlanguagebyrfc1766string) -Methode fügt der Liste eine Sprache hinzu.</span><span class="sxs-lookup"><span data-stu-id="95101-116">The [**IWMLanguageList::AddLanguageByRFC1766String**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-addlanguagebyrfc1766string) method adds a language to the list.</span></span> <span data-ttu-id="95101-117">Sie können die Sprachen, die sich bereits in der Liste befinden, ermitteln, indem Sie die Gesamtzahl der Sprachen mit [**iwmlanguagelist:: getlanguagecount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagecount) abrufen und dann die Sprachen, die [**iwmlanguagelist:: getlanguagedetails**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagedetails) aufrufen, durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="95101-117">You can identify the languages already in the list by obtaining the total number of languages with [**IWMLanguageList::GetLanguageCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagecount) and then looping through the languages calling [**IWMLanguageList::GetLanguageDetails**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagedetails) for each.</span></span> <span data-ttu-id="95101-118">Der sprach Index ist NULL basiert.</span><span class="sxs-lookup"><span data-stu-id="95101-118">The language index is zero based.</span></span>

## <a name="to-configure-mutual-exclusion-by-language"></a><span data-ttu-id="95101-119">So konfigurieren Sie den gegenseitigen Ausschluss nach Sprache</span><span class="sxs-lookup"><span data-stu-id="95101-119">To Configure Mutual Exclusion by Language</span></span>

<span data-ttu-id="95101-120">Das Konfigurieren eines einfachen gegenseitigen Ausschluss Objekts nach Sprache ist sehr einfach.</span><span class="sxs-lookup"><span data-stu-id="95101-120">Configuring a simple mutual exclusion object by language is very simple.</span></span> <span data-ttu-id="95101-121">Jeder Stream ist nun einer Sprache zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="95101-121">Each stream is now associated with a language.</span></span> <span data-ttu-id="95101-122">Die einem Stream zugeordnete Sprache kann mithilfe von [**IWMStreamConfig3:: setLanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig3-setlanguage)festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="95101-122">The language associated with a stream can be set using [**IWMStreamConfig3::SetLanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig3-setlanguage).</span></span> <span data-ttu-id="95101-123">Nachdem alle sich gegenseitig ausschließenden Streams konfiguriert wurden, erstellen Sie einfach ein gegenseitiges Ausschluss Objekt, wie es bei jedem anderen Typ der Fall wäre.</span><span class="sxs-lookup"><span data-stu-id="95101-123">After all of the mutually exclusive streams are configured, simply create a mutual exclusion object as you would for any other type.</span></span> <span data-ttu-id="95101-124">Rufen Sie dann [**iwmmutualexclusion:: settype**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) auf, und übergeben Sie die CLSID- \_ wmmutex- \_ Sprache für den-Typ.</span><span class="sxs-lookup"><span data-stu-id="95101-124">Then call [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) passing CLSID\_WMMUTEX\_Language for the type.</span></span>

<span data-ttu-id="95101-125">Datenströme, die sich gegenseitig ausschließen, werden komplizierter, wenn die exklusiven Streams auch durch die Bitrate gegenseitig ausschließen.</span><span class="sxs-lookup"><span data-stu-id="95101-125">Streams that are mutually exclusive by language become more complicated when the exclusive streams are also mutually exclusive by bit rate.</span></span> <span data-ttu-id="95101-126">In diesem Fall müssen Sie die folgenden Schritte ausführen, um sich gegenseitig ausschließende Datensätze zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="95101-126">In this case you must use mutually exclusive records, by performing the following steps:</span></span>

1.  <span data-ttu-id="95101-127">Erstellen Sie ein gegenseitiges Ausschluss Objekt für die Streams unterschiedlicher Bitraten in jeder Sprache.</span><span class="sxs-lookup"><span data-stu-id="95101-127">Create a mutual exclusion object for the streams of differing bit rates in each language.</span></span> <span data-ttu-id="95101-128">Weitere Informationen zum Erstellen eines gegenseitigen Ausschluss Objekts per Bitrate finden [Sie unter Verwenden des gegenseitigen Ausschlusses mehrerer Bitrate](using-multiple-bit-rate-mutual-exclusion.md).</span><span class="sxs-lookup"><span data-stu-id="95101-128">For more information about creating a mutual exclusion object by bit rate, see [Using Multiple Bit Rate Mutual Exclusion](using-multiple-bit-rate-mutual-exclusion.md).</span></span>
2.  <span data-ttu-id="95101-129">Erstellen Sie ein gegenseitiges Ausschluss Objekt.</span><span class="sxs-lookup"><span data-stu-id="95101-129">Create a mutual exclusion object.</span></span> <span data-ttu-id="95101-130">Rufen Sie [**iwmmutualexclusion:: settype**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) auf, und übergeben Sie die CLSID- \_ wmmutex- \_ Sprache, um die Exklusivität nach Sprache anzugeben.</span><span class="sxs-lookup"><span data-stu-id="95101-130">Call [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) and pass CLSID\_WMMUTEX\_Language to specify exclusivity by language.</span></span>
3.  <span data-ttu-id="95101-131">Rufen Sie einen Zeiger auf die [**IWMMutualExclusion2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2) -Schnittstelle des gegenseitigen Ausschluss Objekts ab, das in Schritt 2 durch Aufrufen der **QueryInterface** -Methode von [**iwmmutualexclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="95101-131">Obtain a pointer to the [**IWMMutualExclusion2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2) interface of the mutual exclusion object created in step 2 by calling the **QueryInterface** method of [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion).</span></span>
4.  <span data-ttu-id="95101-132">Rufen Sie die [**IWMMutualExclusion2:: addRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addrecord) -Methode einmal für jede Sprache auf, um Stream-Datensätze zu erstellen, die sich gegenseitig ausschließen.</span><span class="sxs-lookup"><span data-stu-id="95101-132">Call the [**IWMMutualExclusion2::AddRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addrecord) method once for each language, to create stream records that will be mutually exclusive.</span></span>
5.  <span data-ttu-id="95101-133">Fügen Sie für jeden Datensatz, der in Schritt 4 erstellt wurde, die Streams der entsprechenden Sprache mit Aufrufen von [**IWMMutualExclusion2:: addstreamforrecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addstreamforrecord)hinzu.</span><span class="sxs-lookup"><span data-stu-id="95101-133">For each record created in step 4, add the streams of the appropriate language with calls to [**IWMMutualExclusion2::AddStreamForRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addstreamforrecord).</span></span>

## <a name="to-read-files-with-multiple-languages"></a><span data-ttu-id="95101-134">So lesen Sie Dateien mit mehreren Sprachen</span><span class="sxs-lookup"><span data-stu-id="95101-134">To Read Files with Multiple Languages</span></span>

<span data-ttu-id="95101-135">Das Reader-Objekt stellt Methoden bereit, um die verfügbaren Sprachen von Streams in einer Datei zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="95101-135">The reader object provides methods to identify the available languages of streams in a file.</span></span> <span data-ttu-id="95101-136">Sie können die Anzahl der unterstützten Sprachen für eine Ausgabe abrufen, indem Sie [**IWMReaderAdvanced4:: getlanguagecount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguagecount)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="95101-136">You can retrieve the number of supported languages for an output by calling [**IWMReaderAdvanced4::GetLanguageCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguagecount).</span></span> <span data-ttu-id="95101-137">Anschließend können Sie Details zu jeder Sprache mit Aufrufen von [**IWMReaderAdvanced4:: GetLanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguage)abrufen.</span><span class="sxs-lookup"><span data-stu-id="95101-137">You can then retrieve details about each language with calls to [**IWMReaderAdvanced4::GetLanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguage).</span></span>

<span data-ttu-id="95101-138">Sie können die zu Wiedergabe Ende Sprache angeben, indem Sie den Index dieser Sprache mit einem Aufrufen von [**IWMReaderAdvanced2:: setoutputsetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting)an den Reader übergeben.</span><span class="sxs-lookup"><span data-stu-id="95101-138">You can specify the language to play by passing the index of that language to the reader with a call to [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting).</span></span> <span data-ttu-id="95101-139">Dadurch wird die angegebene Sprache ausgewählt, während die automatische Datenstrom Auswahl für alle anderen gegenseitigen Ausschluss Objekte in der Datei beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="95101-139">This will select the specified language while maintaining automatic stream selection for any other mutual exclusion objects in the file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="95101-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="95101-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95101-141">**Erweiterte Themen**</span><span class="sxs-lookup"><span data-stu-id="95101-141">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> <dt>

[<span data-ttu-id="95101-142">**Iwmlanguagelist-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="95101-142">**IWMLanguageList Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist)
</dt> <dt>

[<span data-ttu-id="95101-143">**Iwmmutualexclusion-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="95101-143">**IWMMutualExclusion Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)
</dt> <dt>

[<span data-ttu-id="95101-144">**IWMMutualExclusion2-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="95101-144">**IWMMutualExclusion2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2)
</dt> <dt>

[<span data-ttu-id="95101-145">**IWMReaderAdvanced2-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="95101-145">**IWMReaderAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[<span data-ttu-id="95101-146">**IWMReaderAdvanced4-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="95101-146">**IWMReaderAdvanced4 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)
</dt> <dt>

[<span data-ttu-id="95101-147">**IWMStreamConfig3-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="95101-147">**IWMStreamConfig3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3)
</dt> </dl>

 

 




