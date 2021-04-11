---
title: Im Windows Media 9,5 SDK hinzugefügte Features
description: Im Windows Media 9,5 SDK hinzugefügte Features
ms.assetid: 1525132c-8aa1-42bb-9552-41531fb83055
keywords:
- Windows Media-Format-SDK, Features
- Windows Media-Format-SDK, neue Funktionen
- Windows Media-Format-SDK, Schnittstelle für anwendungsspezifische Verarbeitung
- Windows Media-Format-SDK, DirectX-Video Beschleunigung (DXVA)
- Windows Media-Format-SDK, iwmplayerhook-Schnittstelle
- Iwmplayerhook
- Windows Media-Format-SDK, x64-basierte Versionen von Windows
- Windows Media-Format-SDK, Windows Media Video Bildcodec
- Windows Media-Format-SDK, Audiocodecs
- Windows Media-Format-SDK, DRM 10 für Netzwerkgeräte
- Windows Media-Format-SDK, DRM-Lizenzen
- Windows Media-Format-SDK, Advanced Profile Codec
- Windows Media-Format-SDK, digitales Microsoft/Philips Digital Interconnect-Format (S/PDIF)
- Windows Media-Format-SDK, Low-Delay-Formate
- Windows Media-Format-SDK, ungefähre Suchmodus
- Windows Media-Format-SDK, Brennen von Wiedergabelisten
- Windows Media-Format-SDK, Unterstützung mehrerer Sprachen
- Windows Media-Format-SDK, Windows Media Device Manager SDK
- Windows Media-Format-SDK, Codec-Schnittstellen
- Codecs, Windows Media Video Abbild
- Digital Rights Management (DRM), Netzwerkgeräte sicheres Übertragungsprotokoll
- DRM (Digital Rights Management), Netzwerkgeräte (Secure Transfer Protocol)
- Digital Rights Management (DRM), Lizenzen
- DRM (Digital Rights Management), Lizenzen
- Codecs, Advanced Profile Codec
- Digitales Interconnect-Format (S/PDIF) für Sony/Philips, übertragen oder übertragen mithilfe von
- S/PDIF (digitales Interconnect-Format von Sony/Philips), übertragen oder übertragen mithilfe von
- ungefähre Suchmodus
- Metadaten, Unterstützung mehrerer Sprachen
- Windows Media Device Manager SDK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e58c9816ef80325422ee365b952842727b5004e
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104101302"
---
# <a name="features-added-in-the-windows-media-95-sdk"></a><span data-ttu-id="3820d-133">Im Windows Media 9,5 SDK hinzugefügte Features</span><span class="sxs-lookup"><span data-stu-id="3820d-133">Features Added in the Windows Media 9.5 SDK</span></span>

<span data-ttu-id="3820d-134">Im Windows Media-Format 9,5 SDK wurden neue Funktionen eingeführt, um die Sicherheit und Flexibilität von Inhalten zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="3820d-134">The Windows Media Format 9.5 SDK introduced new features to provide enhanced content security and flexibility.</span></span> <span data-ttu-id="3820d-135">Die folgenden Änderungen wurden seit der Veröffentlichung der 9-Serie an dem SDK vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="3820d-135">The following changes were made to the SDK since the 9 Series release.</span></span>

## <a name="new-interface-for-application-specific-processing-during-directx-video-acceleration"></a><span data-ttu-id="3820d-136">Neue Schnittstelle für die anwendungsspezifische Verarbeitung während der DirectX-Video Beschleunigung</span><span class="sxs-lookup"><span data-stu-id="3820d-136">New Interface for Application-specific Processing During DirectX Video Acceleration</span></span>

<span data-ttu-id="3820d-137">Player Anwendungen, die die DirectX-Video Beschleunigung unterstützen, können jetzt die [**iwmplayerhook**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmplayerhook) -Schnittstelle implementieren, um die anwendungsspezifische Verarbeitung während der DirectX-VA-Decodierung</span><span class="sxs-lookup"><span data-stu-id="3820d-137">Player applications that support DirectX Video Acceleration can now implement the [**IWMPlayerHook**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmplayerhook) interface to perform application-specific processing during DirectX VA decoding.</span></span> <span data-ttu-id="3820d-138">Der Reader Ruft die [**iwmplayerhook::P redecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmplayerhook-predecode) -Rückruf Methode auf, bevor komprimierte Videobeispiele zum Decodieren an den Videoprozessor übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="3820d-138">The reader calls the [**IWMPLayerHook::PreDecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmplayerhook-predecode) callback method before passing compressed video samples to the video processor for decoding.</span></span>

> [!Note]  
> <span data-ttu-id="3820d-139">Um die **iwmplayerhook** -Schnittstelle und die zugehörige [**IWMReaderAdvanced5**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced5) -Schnittstelle zu verwenden, muss die Update Nummer 888656 im Windows Media-Format-SDK installiert sein.</span><span class="sxs-lookup"><span data-stu-id="3820d-139">To use the **IWMPlayerHook** interface and the associated [**IWMReaderAdvanced5**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced5) interface, you must have update number 888656 installed in the Windows Media Format SDK.</span></span> <span data-ttu-id="3820d-140">Sie können das Update von der [Microsoft-Website](https://support.microsoft.com/?id=888656)herunterladen.</span><span class="sxs-lookup"><span data-stu-id="3820d-140">You can download the update from the [Microsoft Web site](https://support.microsoft.com/?id=888656).</span></span>

 

## <a name="windows-media-format-sdk-version-for-x64-based-versions-of-windows"></a><span data-ttu-id="3820d-141">Windows Media-Format-SDK-Version für x64-basierte Versionen von Windows</span><span class="sxs-lookup"><span data-stu-id="3820d-141">Windows Media Format SDK version for x64-based versions of Windows</span></span>

<span data-ttu-id="3820d-142">Eine x64-basierte Version des SDK für Windows Media-Format ist verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3820d-142">An x64-based version of the Windows Media Format SDK is available.</span></span> <span data-ttu-id="3820d-143">Diese Dokumentation gilt sowohl für die 32-Bit-Versionen als auch für die x64-basierte Version des SDK.</span><span class="sxs-lookup"><span data-stu-id="3820d-143">This documentation applies to both the 32-bit versions and the x64-based version of the SDK.</span></span> <span data-ttu-id="3820d-144">Allerdings wird Digital Rights Management (DRM) im x64-basierten Windows Media-Format-SDK nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3820d-144">However, digital rights management (DRM) is not supported in the x64-based Windows Media Format SDK.</span></span>

## <a name="new-version-of-the-windows-media-video-image-codec"></a><span data-ttu-id="3820d-145">Neue Version des Windows Media Video Abbild Codecs</span><span class="sxs-lookup"><span data-stu-id="3820d-145">New Version of the Windows Media Video Image Codec</span></span>

<span data-ttu-id="3820d-146">Mit dem Windows Media Video 9-Abbild v2-Codec werden die Beispiel Geometrie Berechnungen zum Schwenken und Zoomen vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="3820d-146">The Windows Media Video 9 Image v2 codec simplifies the sample geometry calculations for panning and zooming.</span></span> <span data-ttu-id="3820d-147">Der neue Codec unterstützt auch mehrere komplexe Übergänge zwischen Bildern.</span><span class="sxs-lookup"><span data-stu-id="3820d-147">The new codec also supports several complex transitions between images.</span></span>

## <a name="new-version-of-the-windows-media-audio-codecs"></a><span data-ttu-id="3820d-148">Neue Version der Windows Media Audio Codecs</span><span class="sxs-lookup"><span data-stu-id="3820d-148">New Version of the Windows Media Audio Codecs</span></span>

<span data-ttu-id="3820d-149">Das Windows Media-Format 9,5 SDK umfasst die folgenden aktualisierten Audiocodecs:</span><span class="sxs-lookup"><span data-stu-id="3820d-149">The Windows Media Format 9.5 SDK includes the following updated audio codecs:</span></span>

-   <span data-ttu-id="3820d-150">Windows Media Audio 9,1</span><span class="sxs-lookup"><span data-stu-id="3820d-150">Windows Media Audio 9.1</span></span>
-   <span data-ttu-id="3820d-151">Windows Media Audio 9,1 Professional</span><span class="sxs-lookup"><span data-stu-id="3820d-151">Windows Media Audio 9.1 Professional</span></span>
-   <span data-ttu-id="3820d-152">Windows Media Audio 9,1 verlustfreie</span><span class="sxs-lookup"><span data-stu-id="3820d-152">Windows Media Audio 9.1 Lossless</span></span>

## <a name="windows-media-drm-10-for-network-devices-protocol-support"></a><span data-ttu-id="3820d-153">Unterstützung für Protokoll Unterstützung für Windows Media DRM 10 für Netzwerkgeräte</span><span class="sxs-lookup"><span data-stu-id="3820d-153">Windows Media DRM 10 for Network Devices Protocol Support</span></span>

<span data-ttu-id="3820d-154">Das Windows Media-Format 9,5 SDK unterstützt das sichere Übertragungsprotokoll von Windows Media DRM 10 für Netzwerkgeräte.</span><span class="sxs-lookup"><span data-stu-id="3820d-154">The Windows Media Format 9.5 SDK supports the new Windows Media DRM 10 for Network Devices secure transfer protocol.</span></span> <span data-ttu-id="3820d-155">Dieses Protokoll kann verwendet werden, um verschlüsselte Inhalte über ein lokales Netzwerk an ein Wiedergabe Gerät zu streamen, z. b. einen Video Empfänger, der sich auf der obersten Ebene befindet.</span><span class="sxs-lookup"><span data-stu-id="3820d-155">This protocol can be used to stream encrypted content over a local network to a playback device, such as a set-top video receiver.</span></span>

<span data-ttu-id="3820d-156">Die meisten der Prozeduren, die zum Implementieren der Unterstützung für Windows Media DRM 10 für Netzwerkgeräte verwendet werden, müssen von der Anwendung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3820d-156">Most of the procedures used to implement support for Windows Media DRM 10 for Network Devices must be performed by the application.</span></span> <span data-ttu-id="3820d-157">Sie können jedoch die Methoden des Windows Media Format SDK verwenden, um die folgenden Funktionen bereitzustellen:</span><span class="sxs-lookup"><span data-stu-id="3820d-157">However, you can use methods of the Windows Media Format SDK to provide the following functionality:</span></span>

-   <span data-ttu-id="3820d-158">Warten Sie eine Datenbank von Geräten, einschließlich derjenigen, die für Windows Media DRM 10 für Netzwerkgeräte aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="3820d-158">Maintain a database of devices, including those that are enabled for Windows Media DRM 10 for Network Devices.</span></span>
-   <span data-ttu-id="3820d-159">Überprüfen Sie die Geräte, um sicherzustellen, dass Sie ausreichend für den Client im Netzwerk für sicheres Streaming ausreichend sind.</span><span class="sxs-lookup"><span data-stu-id="3820d-159">Validate devices to ensure that they are "near" enough to the client on the network for secure streaming.</span></span>
-   <span data-ttu-id="3820d-160">Konvertieren von DRM-geschützten Dateien in Windows Media DRM 10 für Netzwerkgeräte Ströme.</span><span class="sxs-lookup"><span data-stu-id="3820d-160">Convert DRM-protected files to Windows Media DRM 10 for Network Devices streams.</span></span>
-   <span data-ttu-id="3820d-161">Schreiben von Dateien mithilfe zuvor verschlüsselter Daten.</span><span class="sxs-lookup"><span data-stu-id="3820d-161">Write files using previously encrypted data.</span></span>

## <a name="support-for-new-drm-licenses"></a><span data-ttu-id="3820d-162">Unterstützung für neue DRM-Lizenzen</span><span class="sxs-lookup"><span data-stu-id="3820d-162">Support for New DRM Licenses</span></span>

<span data-ttu-id="3820d-163">Neue Lizenzen, die mithilfe des Windows Media Rights Manager SDK erstellt wurden, verwenden Ausgabe Schutz Ebenen (opls), um Rechte und Einschränkungen für das Abspielen und Kopieren von Inhalten anzugeben.</span><span class="sxs-lookup"><span data-stu-id="3820d-163">New licenses created by using the Windows Media Rights Manager SDK use Output Protection Levels (OPLs) to specify rights and restrictions for playing and copying content.</span></span> <span data-ttu-id="3820d-164">Das SDK für den Windows Media-Format unterstützt das Lesen der opls aus einer Lizenz.</span><span class="sxs-lookup"><span data-stu-id="3820d-164">The Windows Media Format SDK provides support for reading the OPLs from a license.</span></span>

## <a name="new-video-codec"></a><span data-ttu-id="3820d-165">Neuer Videocodec</span><span class="sxs-lookup"><span data-stu-id="3820d-165">New Video Codec</span></span>

<span data-ttu-id="3820d-166">Die Windows Media Video 9 Advanced Profile Codec basiert auf der hohen Qualität des Windows Media Video 9-Codecs und fügt gleichzeitig Unterstützung für die Zeilen Sprung Codierung hinzu.</span><span class="sxs-lookup"><span data-stu-id="3820d-166">The Windows Media Video 9 Advanced Profile codec builds on the high quality of the Windows Media Video 9 codec while adding support for interlaced encoding.</span></span>

## <a name="spdif-output"></a><span data-ttu-id="3820d-167">S/PDIF-Ausgabe</span><span class="sxs-lookup"><span data-stu-id="3820d-167">S/PDIF Output</span></span>

<span data-ttu-id="3820d-168">Inhalte, die mit einem der Windows Media Audio Professional-Codecs codiert sind, können jetzt mithilfe des digitalen Interconnect-Formats (S/PDIF) von Sony/Philips übertragen oder übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="3820d-168">Content encoded with one of the Windows Media Audio Professional codecs can now be transferred or transmitted using the Sony/Philips Digital Interconnect Format (S/PDIF).</span></span>

## <a name="low-delay-audio"></a><span data-ttu-id="3820d-169">Low-Delay Audiodaten</span><span class="sxs-lookup"><span data-stu-id="3820d-169">Low-Delay Audio</span></span>

<span data-ttu-id="3820d-170">In den Windows Media Audio 9,1-und Windows Media Audio 9,1 Professional-Codecs werden nun jeweils mehrere Low-Delay-Formate unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3820d-170">The Windows Media Audio 9.1 and Windows Media Audio 9.1 Professional codecs now each support several low-delay formats.</span></span> <span data-ttu-id="3820d-171">Diese Formate liefern Audiostreams, die schneller gestartet werden können, wodurch die Latenz bei streamumschalungsszenarien reduziert wird.</span><span class="sxs-lookup"><span data-stu-id="3820d-171">These formats produce audio streams that can be started more quickly, reducing latency in stream-switching scenarios.</span></span> <span data-ttu-id="3820d-172">Die Gesamt Latenz bei Live Übertragungen wird auch durch die Verwendung von Low-Delay-Formaten verbessert.</span><span class="sxs-lookup"><span data-stu-id="3820d-172">Overall latency in live broadcasts is also improved by using low-delay formats.</span></span>

## <a name="approximate-seeking-mode"></a><span data-ttu-id="3820d-173">Ungefähre Suchmodus</span><span class="sxs-lookup"><span data-stu-id="3820d-173">Approximate Seeking Mode</span></span>

<span data-ttu-id="3820d-174">Sie können jetzt eine ungefähre Zeit in einer ASF-Datei mit dem Reader suchen.</span><span class="sxs-lookup"><span data-stu-id="3820d-174">You can now seek to an approximate time in an ASF file with the reader.</span></span> <span data-ttu-id="3820d-175">Dieser Modus verbessert die Leistung bei einer unpräzisen Suche, z. b. Wenn ein Benutzer auf die Suchleiste in Windows Media Player klickt.</span><span class="sxs-lookup"><span data-stu-id="3820d-175">This mode improves performance when performing an imprecise seek, such as when a user clicks the seek bar in Windows Media Player.</span></span> <span data-ttu-id="3820d-176">Die ungefähre Suche gibt das Medien Beispiel für den vorherigen Cleanpoint zurück, anstatt das Beispiel für die genaue Zeit wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="3820d-176">Approximate seeking returns the media sample for the previous cleanpoint instead of reconstructing the sample for the precise time sought.</span></span>

## <a name="playlist-burning"></a><span data-ttu-id="3820d-177">Wiedergabelisten brennen</span><span class="sxs-lookup"><span data-stu-id="3820d-177">Playlist Burning</span></span>

<span data-ttu-id="3820d-178">Windows Media DRM 10 unterstützt die Rechte zum Kopieren von Audiodateien auf Red Book CD als Teil einer Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="3820d-178">Windows Media DRM 10 supports rights for copying audio files to Red Book CD as part of a playlist.</span></span> <span data-ttu-id="3820d-179">Das Windows Media-Format-SDK stellt Methoden bereit, mit denen überprüft werden kann, ob die Dateien in einer Wiedergabeliste kopiert werden dürfen.</span><span class="sxs-lookup"><span data-stu-id="3820d-179">The Windows Media Format SDK provides methods for verifying whether the files in a playlist are allowed to be copied.</span></span>

## <a name="improved-multiple-language-support-for-metadata"></a><span data-ttu-id="3820d-180">Verbesserte Multiple-Language-Unterstützung für Metadaten</span><span class="sxs-lookup"><span data-stu-id="3820d-180">Improved Multiple-Language Support for Metadata</span></span>

<span data-ttu-id="3820d-181">Im Windows Media Format 9-Reihe-SDK wurden alle zu einer Datei hinzugefügten Metadaten einer Sprachliste zugewiesen, der der sprach Bezeichner der Standardsprache zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="3820d-181">In the Windows Media Format 9 Series SDK, all metadata added to a file was assigned to a language list that was given the language identifier of the default language.</span></span> <span data-ttu-id="3820d-182">Dies verursachte Probleme, wenn Inhalts Verteiler in verschiedenen Gebiets Schemas einige Metadaten hinzugefügt haben, da Benutzer im Gebiets Schema des Verteilers nur die wenigen Attribute sehen, die für Ihre Sprache hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="3820d-182">This caused problems when content distributors in different locales added some metadata, because users in the distributor's locale only see the few attributes added for their language.</span></span> <span data-ttu-id="3820d-183">Das Windows Media-Format 9,5 SDK löst dieses Problem, indem es keine Sprachliste erstellt, bis in der Dateiattribute aus zwei Sprachen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="3820d-183">The Windows Media Format 9.5 SDK solves this problem by not creating a language list until there are attributes from two languages present in the file.</span></span> <span data-ttu-id="3820d-184">An diesem Punkt werden alle Metadaten dem Gebiets Schema der zweiten Sprache zugeordnet, das dann zum Standard wird.</span><span class="sxs-lookup"><span data-stu-id="3820d-184">At that point, all of the metadata is associated with the locale of the second language, which then becomes the default.</span></span> <span data-ttu-id="3820d-185">Auf diese Weise kann ein Inhalts Verteiler alle ursprünglichen Metadaten für eine Datei, z. b. Titel und Autor, intakt halten und gleichzeitig einige Attribute hinzufügen, die Ihrem Gebiets Schema entsprechen.</span><span class="sxs-lookup"><span data-stu-id="3820d-185">In this way, a content distributor can keep all of the original metadata for a file, such as title and author, intact while adding some attributes pertinent to their locale.</span></span>

## <a name="windows-media-device-manager-sdk-included-in-installation"></a><span data-ttu-id="3820d-186">Windows Media Device Manager SDK, das in der Installation enthalten ist</span><span class="sxs-lookup"><span data-stu-id="3820d-186">Windows Media Device Manager SDK Included in Installation</span></span>

<span data-ttu-id="3820d-187">Das Installationspaket für das Windows Media-Format 9,5 SDK installiert das Windows Media Device Manager SDK.</span><span class="sxs-lookup"><span data-stu-id="3820d-187">The installation package for the Windows Media Format 9.5 SDK installs the Windows Media Device Manager SDK.</span></span> <span data-ttu-id="3820d-188">Die Dokumentation für das Windows Media Device Manager SDK finden Sie im Ordner "C: \\ wmsdk \\ WMFSDK95 \\ WMDM \\ docs" (Ihr Ordner unterscheidet sich, wenn Sie das Windows Media-Format-SDK nicht im Standardordner installieren).</span><span class="sxs-lookup"><span data-stu-id="3820d-188">The documentation for the Windows Media Device Manager SDK can be found in the C:\\WMSDK\\WMFSDK95\\WMDM\\docs folder (your folder will be different if you do not install the Windows Media Format SDK in the default folder.)</span></span>

## <a name="codec-interface-documentation"></a><span data-ttu-id="3820d-189">Dokumentation zu Codec Interface</span><span class="sxs-lookup"><span data-stu-id="3820d-189">Codec Interface Documentation</span></span>

<span data-ttu-id="3820d-190">Diese Dokumentation enthält Informationen zur Verwendung der Windows Media Audio und der Video Codecs außerhalb des Windows Media SDK.</span><span class="sxs-lookup"><span data-stu-id="3820d-190">This documentation includes information about using the Windows Media Audio and Video codecs outside of the Windows Media Format SDK.</span></span> <span data-ttu-id="3820d-191">Diese Dokumentation wurde ursprünglich als Teil eines Downloads aus dem Microsoft Developer Network veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="3820d-191">This documentation was originally released as part of a download from the Microsoft Developer Network.</span></span> <span data-ttu-id="3820d-192">Die Beispielanwendungen, die die Verwendung der Codec-DMOS direkt veranschaulichen, sind in der Windows Media-Format-SDK-Installation zusammen mit Headern enthalten.</span><span class="sxs-lookup"><span data-stu-id="3820d-192">The sample applications that demonstrate using the codec DMOs directly are included in the Windows Media Format SDK installation along with headers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3820d-193">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3820d-193">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3820d-194">**Informationen zum Windows Media-Format-SDK**</span><span class="sxs-lookup"><span data-stu-id="3820d-194">**About the Windows Media Format SDK**</span></span>](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




