---
title: Arbeiten mit Ausgabe Schutz Ebenen
description: Arbeiten mit Ausgabe Schutz Ebenen
ms.assetid: ec5982cd-0b87-4081-98e2-ab2d102a36d8
keywords:
- Windows Media-Format-SDK, Ausgabe Schutz Ebenen (OPL)
- Windows Media-Format-SDK, Schutz Ebenen
- Advanced Systems Format (ASF), Ausgabe Schutz Ebenen (OPL)
- ASF (Advanced Systems Format), Ausgabe Schutz Ebenen (OPL)
- Advanced Systems Format (ASF), Schutz Ebenen
- ASF (Advanced Systems Format), Schutz Ebenen
- Advanced Systems Format (ASF), mehrere Lizenzen
- ASF (Advanced Systems Format), mehrere Lizenzen
- Digital Rights Management (DRM), Ausgabe Schutz Ebenen (OPL)
- DRM (Digital Rights Management), Ausgabe Schutz Ebenen (OPL)
- Digital Rights Management (DRM), Schutz Ebenen
- DRM (Digital Rights Management), Schutz Ebenen
- Digital Rights Management (DRM), Auswerten von Ausgabe Schutz Ebenen (OPL)
- DRM (Digital Rights Management), Auswerten von Ausgabe Schutz Ebenen (OPL)
- Digital Rights Management (DRM), mehrere Lizenzen
- DRM (Digital Rights Management), mehrere Lizenzen
- Ausgabe Schutz Ebenen (OPL)
- OPL (Ausgabe Schutz Ebenen)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aab7023cc8285e5f3993aac69c57deca9675d9dd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314219"
---
# <a name="working-with-output-protection-levels"></a><span data-ttu-id="824f1-121">Arbeiten mit Ausgabe Schutz Ebenen</span><span class="sxs-lookup"><span data-stu-id="824f1-121">Working with Output Protection Levels</span></span>

<span data-ttu-id="824f1-122">Lizenzen, die mithilfe des Windows Media Rights Manager 10 SDK erstellt wurden, können Aktions Einschränkungen mithilfe von "Output Protection Levels (opls)" angeben.</span><span class="sxs-lookup"><span data-stu-id="824f1-122">Licenses created by using the Windows Media Rights Manager 10 SDK can specify action restrictions using output protection levels (OPLs).</span></span> <span data-ttu-id="824f1-123">Opls ermöglichen einem Lizenz Ersteller, einige Aktionen nur auf Geräten mit bestimmten Technologien zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="824f1-123">OPLs enable a license creator to allow some actions only on devices with specific technologies.</span></span> <span data-ttu-id="824f1-124">Die Verwendung von opls hat den Vorteil, dass Sie mehr Flexibilität bei der Erstellung von Lizenz Einschränkungen als in früheren Versionen erhalten.</span><span class="sxs-lookup"><span data-stu-id="824f1-124">The benefits of using OPLs is that you get more flexibility in creating license restrictions than previous versions.</span></span> <span data-ttu-id="824f1-125">Außerdem sind opls erweiterbar, um zukünftige Technologien zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="824f1-125">In addition, OPLs are expandable to accommodate future technologies.</span></span> <span data-ttu-id="824f1-126">Sie können solche Lizenzen in Ihren Anwendungen unterstützen, indem Sie die Methoden der [**IWMDRMReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2) -Schnittstelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="824f1-126">You can support such licenses in your applications by using the methods of the [**IWMDRMReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2) interface.</span></span>

<span data-ttu-id="824f1-127">Um Dateien zu lesen, die durch eine Lizenz geschützt sind, die opls angibt, müssen Sie die OPL auf die gewünschte Aktion überprüfen.</span><span class="sxs-lookup"><span data-stu-id="824f1-127">To read files that are protected by a license that specifies OPLs, you must check the OPL for the desired action.</span></span> <span data-ttu-id="824f1-128">Die von Ihrer Anwendung verwendete Ausgabe Technologie muss von der OPL in der Lizenz zugelassen werden.</span><span class="sxs-lookup"><span data-stu-id="824f1-128">The output technology your application is using must be allowed by the OPL in the license.</span></span> <span data-ttu-id="824f1-129">Beispielsweise erfordern einige Lizenzen für geschütztes Audiomaterial, dass Sie einen sicheren Audiopfad für die Wiedergabe verwenden.</span><span class="sxs-lookup"><span data-stu-id="824f1-129">For example, some licenses for protected audio may require that you use secure audio path to play it.</span></span>

## <a name="configuring-the-reader-to-evaluate-output-protection-levels"></a><span data-ttu-id="824f1-130">Konfigurieren des Readers zum Auswerten von Ausgabe Schutz Ebenen</span><span class="sxs-lookup"><span data-stu-id="824f1-130">Configuring the Reader to Evaluate Output Protection Levels</span></span>

<span data-ttu-id="824f1-131">Bevor Sie opls auf Dateien prüfen können, die im Reader geladen wurden, müssen Sie die [**IWMDRMReader2:: setevaluateoutputlevellicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-setevaluateoutputlevellicenses) -Methode aufrufen und dabei **true** für den *fevaluate* -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="824f1-131">Before you can check OPLs for files loaded in the reader, you must call the [**IWMDRMReader2::SetEvaluateOutputLevelLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-setevaluateoutputlevellicenses) method, passing **TRUE** for the *fEvaluate* parameter.</span></span> <span data-ttu-id="824f1-132">Wenn Sie diese Methode nicht aufzurufen, sind Lizenzen, die opls erfordern, für Ihre Anwendung nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="824f1-132">If you do not call this method, licenses that require OPLs are not visible to your application.</span></span>

## <a name="evaluating-copy-output-protection-levels"></a><span data-ttu-id="824f1-133">Auswerten von Schutz Ebenen für die Kopier Ausgabe</span><span class="sxs-lookup"><span data-stu-id="824f1-133">Evaluating Copy Output Protection Levels</span></span>

<span data-ttu-id="824f1-134">Zum Abrufen von Ausgabe Schutz Ebenen für die Kopier Aktion müssen Sie die [**IWMDRMReader2:: getcopyoutputlevels**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getcopyoutputlevels) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="824f1-134">To get output protection levels for the copy action, call the [**IWMDRMReader2::GetCopyOutputLevels**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getcopyoutputlevels) method.</span></span> <span data-ttu-id="824f1-135">Die Daten, die Sie vom-Befehl empfangen, werden in einer [**DRM- \_ \_ kopieropl**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_copy_opl) -Struktur gespeichert.</span><span class="sxs-lookup"><span data-stu-id="824f1-135">The data you receive from the call is stored in a [**DRM\_COPY\_OPL**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_copy_opl) structure.</span></span> <span data-ttu-id="824f1-136">Die-Struktur enthält eine grundlegende Ausgabe Schutz Ebene, die die minimale Ausgabe Ebene für die Kopier Aktion in der Lizenz angibt.</span><span class="sxs-lookup"><span data-stu-id="824f1-136">The structure contains a base output protection level, which specifies the minimum output level for the copy action in the license.</span></span> <span data-ttu-id="824f1-137">Die DRM \_ \_ -OPL-Struktur enthält jedoch auch zwei Listen mit Technologie bezeichgern: eine für zulässige Technologien, die mit einer niedrigeren OPL als der Basis bewertet werden, und eine für Technologien, die gleich oder höher als die Basis-OPL bewertet werden, aber durch die Lizenz eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="824f1-137">However, the DRM\_COPY\_OPL structure also contains two lists of technology identifiers: one for allowed technologies that are rated at a lower OPL than the base, and one for technologies that are rated equal to or higher than the base OPL but that are restricted by the license.</span></span> <span data-ttu-id="824f1-138">Sie müssen die Einschlüsse und Ausschlüsse überprüfen, um sicherzustellen, dass die von Ihrer Anwendung verwendete Technologie von der Lizenz zugelassen wird.</span><span class="sxs-lookup"><span data-stu-id="824f1-138">You must check the inclusions and exclusions to ensure that the technology your application is using is allowed by the license.</span></span>

## <a name="evaluating-play-output-protection-levels"></a><span data-ttu-id="824f1-139">Auswerten von Wiedergabe-Ausgabe Schutz Ebenen</span><span class="sxs-lookup"><span data-stu-id="824f1-139">Evaluating Play Output Protection Levels</span></span>

<span data-ttu-id="824f1-140">Zum Abrufen von Ausgabe Schutz Ebenen für die Wiedergabe Aktion müssen Sie die [**IWMDRMReader2:: getplayoutputlevels**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getplayoutputlevels) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="824f1-140">To get output protection levels for the play action, call the [**IWMDRMReader2::GetPlayOutputLevels**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getplayoutputlevels) method.</span></span> <span data-ttu-id="824f1-141">Die Daten, die Sie vom-Befehl empfangen, werden in einer [**DRM- \_ Wiedergabe- \_ OPL**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_play_opl) -Struktur gespeichert.</span><span class="sxs-lookup"><span data-stu-id="824f1-141">The data you receive from the call is stored in a [**DRM\_PLAY\_OPL**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_play_opl) structure.</span></span> <span data-ttu-id="824f1-142">Die-Struktur enthält mehrere andere-Strukturen.</span><span class="sxs-lookup"><span data-stu-id="824f1-142">The structure contains several other structures.</span></span> <span data-ttu-id="824f1-143">Die grundlegenden Ausgabe Schutz Ebenen für die Wiedergabe Aktion werden in einer [**DRM- \_ minimalen \_ Ausgabe \_ Schutz \_ Ebenen**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_minimum_output_protection_levels) -Struktur (dem **minopl** -Member von **DRM \_ Play \_ OPL**) gespeichert, der die minimale OPL definiert, die für die Wiedergabe von Inhalten in einer Vielzahl von Formaten erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="824f1-143">The base output protection levels for the play action are stored in a [**DRM\_MINIMUM\_OUTPUT\_PROTECTION\_LEVELS**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_minimum_output_protection_levels) structure (the **minOPL** member of **DRM\_PLAY\_OPL**), which defines the minimum OPL required to play content in a variety of formats.</span></span> <span data-ttu-id="824f1-144">Sie müssen das-Element auf den Typ der Ausgabeformate überprüfen, die Ihre Anwendung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="824f1-144">You must check the member for the type of output formats that your application delivers.</span></span>

<span data-ttu-id="824f1-145">Die **DRM- \_ Wiedergabe- \_ OPL** -Struktur definiert zwei Arten von Einschränkungen: erforderliche Abtast Stichproben und zulässige Video-Ausgabe Schutz Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="824f1-145">The **DRM\_PLAY\_OPL** structure defines two kinds of restrictions: required down-sampling and allowed video output protection identifiers.</span></span>

<span data-ttu-id="824f1-146">Die erforderliche Downsampling ist als eine Liste von Ausgabe Technologie bezeichaten definiert (das **opliddownsample** -Element von **DRM \_ Play \_ OPL**), die den Inhalt für die Wiedergabe nur dann empfangen kann, wenn der Inhalt zuerst mit einer niedrigeren Bitrate abgetastet wird.</span><span class="sxs-lookup"><span data-stu-id="824f1-146">Required down-sampling is defined as a list of output technology identifiers (the **oplIdDownsample** member of **DRM\_PLAY\_OPL**) that, if used, can receive the content for playback only if the content is first down-sampled to a lower bit rate.</span></span>

<span data-ttu-id="824f1-147">Zulässige Grafik-Ausgabebezeichner werden als Liste von Videoausgabe Technologien definiert, die jeweils Konfigurationsinformationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="824f1-147">Allowed video output protection identifiers are defined as a list of video output technologies with configuration information for each.</span></span>

## <a name="handling-multiple-licenses"></a><span data-ttu-id="824f1-148">Verarbeiten mehrerer Lizenzen</span><span class="sxs-lookup"><span data-stu-id="824f1-148">Handling Multiple Licenses</span></span>

<span data-ttu-id="824f1-149">Einigen Dateien sind möglicherweise mehrere Lizenzen im lokalen Lizenz Speicher zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="824f1-149">Some files may have multiple licenses associated with them in the local license store.</span></span> <span data-ttu-id="824f1-150">Wenn Sie opls für eine Datei auswerten, die Sie lesen, können Sie durch Aufrufen der [**IWMDRMReader2:: trynextlicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-trynextlicense) -Methode nach zusätzlichen Lizenzen suchen.</span><span class="sxs-lookup"><span data-stu-id="824f1-150">When you evaluate OPLs for a file that you are reading, you can check for additional licenses by calling the [**IWMDRMReader2::TryNextLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-trynextlicense) method.</span></span> <span data-ttu-id="824f1-151">Sie sollten die Lizenzen weiterhin testen, bis Sie eine gefunden haben, die die durchzuführende Aktion zulässt, oder bis "trynextlicense" DRM \_ S false zurückgibt \_ . Dies deutet darauf hin, dass keine Lizenzen mehr vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="824f1-151">You should continue trying licenses until you find one that allows the action you want to perform or until TryNextLicense returns DRM\_S\_FALSE, which indicates that there are no more licenses.</span></span>

<span data-ttu-id="824f1-152">In einigen Fällen kann eine Datei über eine zugehörige Lizenz verfügen, die eine OPL erfordert, die von der Anwendung nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="824f1-152">In some cases, a file might have an associated license that requires an OPL that your application cannot support.</span></span> <span data-ttu-id="824f1-153">In einem solchen Fall ist es wichtig, eine Überprüfung auf weitere Lizenzen durchzuführen, da möglicherweise eine Lizenz vorhanden ist, die keine opls angibt.</span><span class="sxs-lookup"><span data-stu-id="824f1-153">In such a case it is important to check for additional licenses because a license may exist that does not specify OPLs.</span></span>

<span data-ttu-id="824f1-154">**Hinweis** DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="824f1-154">**Note** DRM is not supported by the x64-based version of this SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="824f1-155">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="824f1-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="824f1-156">**Aktivieren DRM-Unterstützung**</span><span class="sxs-lookup"><span data-stu-id="824f1-156">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="824f1-157">**IWMDRMReader2-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="824f1-157">**IWMDRMReader2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2)
</dt> </dl>

 

 




