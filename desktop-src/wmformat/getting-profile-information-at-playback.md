---
title: Erhalten von Profilinformationen bei der Wiedergabe
description: Erhalten von Profilinformationen bei der Wiedergabe
ms.assetid: 4ea6c063-fd53-4b5e-ac01-9e2790322ace
keywords:
- Windows Media-Format-SDK, profile
- Advanced Systems Format (ASF), profile
- ASF (Advanced Systems Format), profile
- Advanced Systems Format (ASF), gegenseitiger Ausschluss
- ASF (Advanced Systems Format), gegenseitiger Ausschluss
- Advanced Systems Format (ASF), Bandbreiten Freigabe
- ASF (Advanced Systems Format), Bandbreiten Freigabe
- Streams, erhalten von Profilinformationen bei der Wiedergabe
- Profile, erhalten von Informationen bei der Wiedergabe
- gegenseitiger Ausschluss, erhalten von Profilinformationen bei der Wiedergabe
- Bandbreiten Freigabe, erhalten von Profilinformationen bei der Wiedergabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a5c7083f7bf9e986e8a23ba2c78dfe4404942a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104101278"
---
# <a name="getting-profile-information-at-playback"></a><span data-ttu-id="ddb72-114">Erhalten von Profilinformationen bei der Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="ddb72-114">Getting Profile Information at Playback</span></span>

<span data-ttu-id="ddb72-115">Informationen aus dem Profil, das zum Erstellen einer Datei verwendet wird, werden im Header Abschnitt der Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ddb72-115">Information from the profile used to create a file is stored in the header section of the file.</span></span> <span data-ttu-id="ddb72-116">Beide Reader-Objekte können über den Dateiheader auf die Profilinformationen zugreifen.</span><span class="sxs-lookup"><span data-stu-id="ddb72-116">Both reader objects can access the profile information from the file header.</span></span> <span data-ttu-id="ddb72-117">Es gibt mehrere Gründe, warum Sie auf die Profildaten des Readers zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="ddb72-117">There are several reasons why you might want to access profile data from the reader.</span></span> <span data-ttu-id="ddb72-118">In den meisten Fällen müssen Sie Informationen zu Streams, gegenseitigen Ausschluss Objekten und Bandbreiten Freigabe Objekten abrufen.</span><span class="sxs-lookup"><span data-stu-id="ddb72-118">Most commonly, you will need to retrieve information about streams, mutual exclusion objects, and bandwidth sharing objects.</span></span>

<span data-ttu-id="ddb72-119">Sowohl das asynchrone Reader-Objekt als auch das synchrone Reader-Objekt können für die [**iwmprofile**](iwmprofile.md) -Schnittstelle abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="ddb72-119">Both the asynchronous reader object and the synchronous reader object can be queried for the [**IWMProfile**](iwmprofile.md) interface.</span></span> <span data-ttu-id="ddb72-120">Keine Änderungen an den Profilinformationen können Auswirkungen auf die Datei im Reader haben.</span><span class="sxs-lookup"><span data-stu-id="ddb72-120">No changes made to the profile information can have any affect on the file in the reader.</span></span> <span data-ttu-id="ddb72-121">Weitere Informationen zum Zugreifen auf Profilinformationen finden Sie unter [Arbeiten mit Profilen](working-with-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="ddb72-121">For more information about accessing profile information, see [Working with Profiles](working-with-profiles.md).</span></span>

## <a name="stream-information"></a><span data-ttu-id="ddb72-122">Streaminformationen</span><span class="sxs-lookup"><span data-stu-id="ddb72-122">Stream Information</span></span>

<span data-ttu-id="ddb72-123">Manchmal ist es wichtig zu wissen, wie ein Stream konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="ddb72-123">It is sometimes important to know how a stream is configured.</span></span> <span data-ttu-id="ddb72-124">Wenn Sie Medien Eigenschaften von einem der Reader-Objekte abrufen, werden die Eigenschaften der Ausgaben abgerufen.</span><span class="sxs-lookup"><span data-stu-id="ddb72-124">When you retrieve media properties from the either of the reader objects, you get the properties of the outputs.</span></span> <span data-ttu-id="ddb72-125">Ausgabe Eigenschaften beschreiben, wie die unkomprimierten Daten aus einem Stream vom Reader übermittelt werden, nicht wie der Stream innerhalb der ASF-Datei konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="ddb72-125">Output properties describe how the uncompressed data from a stream is going to be delivered by the reader, not how the stream is configured within the ASF file.</span></span>

<span data-ttu-id="ddb72-126">Wenn Sie nicht komprimierte streambeispiele von einem der Reader-Objekte empfangen, müssen Sie die Profilinformationen verwenden, um das Format der komprimierten Daten zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="ddb72-126">When receiving uncompressed stream samples from either reader object, you must use the profile information to identify the format of the compressed data.</span></span> <span data-ttu-id="ddb72-127">Dies ist besonders wichtig, wenn Sie den komprimierten Stream in eine andere ASF-Datei schreiben möchten.</span><span class="sxs-lookup"><span data-stu-id="ddb72-127">This is particularly important if you are going to write the compressed stream to another ASF file.</span></span>

<span data-ttu-id="ddb72-128">Sie müssen auch auf streaminformationen zugreifen, wenn Sie eine intelligente Neukomprimierung verwenden, um einen Audiostream in eine niedrigere Bitrate zu transcodieren.</span><span class="sxs-lookup"><span data-stu-id="ddb72-128">You also need to access stream information when using smart recompression to transcode an audio stream to a lower bit rate.</span></span>

<span data-ttu-id="ddb72-129">Möglicherweise möchten Sie ermitteln, ob ein Datenstrom mithilfe von VBR-Codierung (Variable Bitrate) geschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="ddb72-129">You may want to determine whether a stream was written using variable bit rate (VBR) encoding.</span></span> <span data-ttu-id="ddb72-130">Es ist nicht möglich, auf VBR-Informationen von der **iwmprofile** -Schnittstelle eines Reader-Objekts zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="ddb72-130">You cannot access any VBR information from the **IWMProfile** interface of either reader object.</span></span> <span data-ttu-id="ddb72-131">Dies liegt daran, dass die VBR-Informationen nach der Codierung nicht in der Datei gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="ddb72-131">This is because the VBR information is not stored in the file after encoding.</span></span> <span data-ttu-id="ddb72-132">Sie können mithilfe der VBR-Codierung ermitteln, ob ein Stream erstellt wurde, indem Sie einen Zeiger auf die [**iwmheaderinfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) -Schnittstelle des Reader-Objekts erhalten und [**iwmheaderinfo:: getattributebyname**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ddb72-132">You can determine whether a stream was created using VBR encoding by obtaining a pointer to the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface of the reader object and calling [**IWMHeaderInfo::GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).</span></span> <span data-ttu-id="ddb72-133">Sie müssen die Datenstrom Nummer angeben und g \_ wszisvbr als Attributnamen übergeben.</span><span class="sxs-lookup"><span data-stu-id="ddb72-133">You must specify the stream number and pass g\_wszIsVBR as the attribute name.</span></span>

## <a name="mutual-exclusion-information"></a><span data-ttu-id="ddb72-134">Informationen zum gegenseitigen Ausschluss</span><span class="sxs-lookup"><span data-stu-id="ddb72-134">Mutual Exclusion Information</span></span>

<span data-ttu-id="ddb72-135">Wenn Sie eine Leseanwendung erstellen möchten, die den gegenseitigen Ausschluss verwendet, sollten Sie auf die Informationen zu allen gegenseitigen Ausschluss Objekten im Profil zugreifen.</span><span class="sxs-lookup"><span data-stu-id="ddb72-135">If you want to create a reading application that uses mutual exclusion, you will want to access the information about any mutual exclusion objects included in the profile.</span></span> <span data-ttu-id="ddb72-136">Für alle gegenseitigen Ausschluss Typen außer der Bitrate ist die Leseanwendung für jeden erforderlichen Datenstrom Wechsel verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="ddb72-136">For all mutual exclusion types except bit rate, the reading application is responsible for any stream switching that is required.</span></span> <span data-ttu-id="ddb72-137">Um Streams zu wechseln, müssen Sie wissen, welche Streams welche Datenströme haben.</span><span class="sxs-lookup"><span data-stu-id="ddb72-137">To switch streams, you need to know which streams are which.</span></span>

## <a name="bandwidth-sharing-information"></a><span data-ttu-id="ddb72-138">Informationen zur Bandbreiten Freigabe</span><span class="sxs-lookup"><span data-stu-id="ddb72-138">Bandwidth Sharing Information</span></span>

<span data-ttu-id="ddb72-139">Bandbreiten Freigabe Objekte, die in einem Profil enthalten sind, sind nur zu Informationszwecken enthalten.</span><span class="sxs-lookup"><span data-stu-id="ddb72-139">Bandwidth sharing objects that are included in a profile are included only for informational purposes.</span></span> <span data-ttu-id="ddb72-140">Weder das Writer-Objekt noch eines der Reader-Objekte führt eine Aktion aus, die durch die Bandbreiten Freigabe von Daten verursacht wird.</span><span class="sxs-lookup"><span data-stu-id="ddb72-140">Neither the writer object nor either of the reader objects takes any action as a result of bandwidth sharing data.</span></span> <span data-ttu-id="ddb72-141">Wenn Sie die Bandbreiten Freigabe in der Leseanwendung verwenden möchten, müssen Sie auf die Informationen zur Bandbreiten Freigabe aus den Profildaten zugreifen.</span><span class="sxs-lookup"><span data-stu-id="ddb72-141">If you want to use bandwidth sharing in your reading application, you must access the bandwidth sharing information from the profile data.</span></span>

> [!Note]  
> <span data-ttu-id="ddb72-142">Nicht alle Informationen aus dem Profil, das zum Erstellen einer Datei verwendet wird, sind im Dateiheader vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ddb72-142">Not all of the information from the profile used to create a file is present in the file header.</span></span> <span data-ttu-id="ddb72-143">Als allgemeine Regel werden Daten, die nur zum Zeitpunkt der Codierung verwendet werden, nicht in der Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ddb72-143">As a general rule, data that is used only at the time of encoding is not persisted in the file.</span></span> <span data-ttu-id="ddb72-144">Dies schließt Eingabeeinstellungen ein, die mithilfe der [**IWMWriterAdvanced2:: setinputsetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) -Methode festgelegt wurden, sowie Eigenschaften, die mithilfe der [**iwmpropertyvault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) -Methode festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="ddb72-144">This includes input settings that were set using the [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) method, as well as properties set using the [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) method.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ddb72-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ddb72-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ddb72-146">**Iwmprofile-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ddb72-146">**IWMProfile Interface**</span></span>](iwmprofile.md)
</dt> <dt>

[<span data-ttu-id="ddb72-147">**Lesen von ASF-Dateien**</span><span class="sxs-lookup"><span data-stu-id="ddb72-147">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> </dl>

 

 




