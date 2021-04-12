---
title: Features, die im SDK der Windows Media-Serie 9 hinzugefügt werden
description: Features, die im SDK der Windows Media-Serie 9 hinzugefügt werden
ms.assetid: 73c4da27-a456-4845-a35b-edb75aa3f953
keywords:
- Windows Media-Format-SDK, Features
- Windows Media-Format-SDK, neue Funktionen
- SDK für den Windows Media-Format, synchrone Reader
- Windows Media-Format-SDK, Frame basierte Indizierung
- Windows Media-Format-SDK, SMPTE-Zeit Codes
- Windows Media-Format-SDK, DirectShow-Filter
- Windows Media-Format-SDK, DRM-Schreibfunktion
- Windows Media-Format-SDK, Datei senken
- Windows Media-Format-SDK, DirectX-Video Beschleunigung (DXVA)
- Windows Media-Format-SDK, Multichannel-Audiodatei
- Windows Media-Format-SDK, Wasserzeichen
- Windows Media-Format-SDK, Unterstützung mehrerer Sprachen
- Windows Media-Format-SDK, Geräte Konformitäts Vorlagen
- Windows Media-Format-SDK, Codec-Enumerationen
- Windows Media-Format-SDK, gegenseitiger Ausschluss
- Windows Media-Format-SDK, mehrfache Bitrate (MBR)
- Windows Media-Format-SDK, Transcoding mit intelligenter Neukomprimierung
- Windows Media-Format-SDK, intelligente Neukomprimierung
- SDK für Windows Media-Format, Neukomprimierung
- SDK für Windows Media-Format, Metadaten
- Windows Media-Format-SDK, dynamisches Pixel Seitenverhältnis
- Windows Media-Format-SDK, Text Ströme mit Zeilen Sprung
- Windows Media-Format-SDK, Two-Pass-Codierung
- Windows Media-Format-SDK, wmstub. lib
- synchrone Leser, Informationen zu
- Frame basierte Indizierung
- SMPTE-Zeit Codes, Informationen zu
- DirectShow-Filter
- Datei senken, Erweiterungen
- Multichannel-Audioinformationen, Informationen zu
- Wasserzeichen, Info
- Codecs, Enumerationen
- gegenseitiger Ausschluss, Informationen
- Digital Rights Management (DRM), Schreiben von Funktionen
- DRM (Digital Rights Management), Schreiben von Funktionen
- DirectX-Video Beschleunigung (DXVA), Informationen zu
- DXVA (DirectX-Video Beschleunigung), Informationen zu
- Advanced Systems Format (ASF), Unterstützung mehrerer Sprachen
- ASF (Advanced Systems Format), Unterstützung mehrerer Sprachen
- mehrfache Bitrate (MBR), Informationen zu
- MBR (mehrfache Bitrate), Informationen zu
- Transcodierung mit intelligenter Neukomprimierung
- intelligente Neukomprimierung
- Neukomprimierung
- Metadaten, Windows Media-Format-SDK
- Verhältnis des dynamischen Pixel Aspekts
- Videodaten Ströme mit Zeilen Sprung
- zwei-Pass-Codierung, Informationen
- '2: Codierung, Informationen'
- Wmstub. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adca7e39c89220c2c8c4cac6af354eefb77257aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206820"
---
# <a name="features-added-in-the-windows-media-format-9-series-sdk"></a><span data-ttu-id="0d5a4-153">Features, die im SDK der Windows Media-Serie 9 hinzugefügt werden</span><span class="sxs-lookup"><span data-stu-id="0d5a4-153">Features Added in the Windows Media Format 9 Series SDK</span></span>

<span data-ttu-id="0d5a4-154">Das Windows Media Format 9 Series SDK hat viele Verbesserungen und Features eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-154">The Windows Media Format 9 Series SDK introduced many improvements and features.</span></span> <span data-ttu-id="0d5a4-155">Dieser Abschnitt bietet eine Übersicht über die Features, die Benutzer bei der Migration von einer früheren Version des SDK nutzen.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-155">This section provides an overview of those features for the benefit of users migrating from an earlier version of the SDK.</span></span>

## <a name="synchronous-reading"></a><span data-ttu-id="0d5a4-156">Synchrones lesen</span><span class="sxs-lookup"><span data-stu-id="0d5a4-156">Synchronous Reading</span></span>

<span data-ttu-id="0d5a4-157">Sie können ASF-Dateien mit synchronen Aufrufen lesen.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-157">You can read ASF files with synchronous calls.</span></span> <span data-ttu-id="0d5a4-158">Beim synchronen Lesen einer Datei können Sie die Einstellungen des Readers beim Lesen ändern.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-158">When reading a file synchronously, you can change the settings of the reader while it is reading.</span></span> <span data-ttu-id="0d5a4-159">Die synchronen Lesevorgänge des SDK bieten keine Unterstützung für das Lesen von Dateien über das Internet, aber Sie können die Standard-COM-Schnittstelle **IStream** verwenden, um aus benutzerdefinierten Quellen zu lesen.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-159">The synchronous reading operations of the SDK do not provide support for reading files over the Internet, but you can use the standard COM interface, **IStream**, to read from custom sources.</span></span>

## <a name="frame-based-indexing"></a><span data-ttu-id="0d5a4-160">Frame basierte Indizierung</span><span class="sxs-lookup"><span data-stu-id="0d5a4-160">Frame-based Indexing</span></span>

<span data-ttu-id="0d5a4-161">Sie können ASF-Dateien auf der Grundlage von Video Frames indizieren.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-161">You can index ASF files based on video frames.</span></span> <span data-ttu-id="0d5a4-162">Sowohl der Reader als auch der synchrone Reader können einen Frame eines Videodaten Stroms suchen und die anderen Streams mit diesem Frame synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-162">Both the reader and the synchronous reader can seek to a frame of a video stream and synchronize the other streams to that frame.</span></span>

## <a name="indexing-and-seeking-with-smpte-time-code"></a><span data-ttu-id="0d5a4-163">Indizierung und Suche mit SMPTE-Zeit Code</span><span class="sxs-lookup"><span data-stu-id="0d5a4-163">Indexing and Seeking with SMPTE Time Code</span></span>

<span data-ttu-id="0d5a4-164">Mit dem Windows Media-Format-SDK können Sie SMPTE-Zeit Codes in ASF-Dateien speichern.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-164">The Windows Media Format SDK enables you to store SMPTE time codes in ASF files.</span></span> <span data-ttu-id="0d5a4-165">Dateien können mithilfe von SMPTE-Zeit Code indiziert werden, und sowohl der asynchrone Reader als auch der synchrone Reader können nach SMPTE-Zeit Code Indexeinträgen suchen.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-165">Files can be indexed by SMPTE time code, and both the asynchronous reader and synchronous reader can seek to SMPTE time code index entries.</span></span>

## <a name="directshow-filters"></a><span data-ttu-id="0d5a4-166">DirectShow-Filter</span><span class="sxs-lookup"><span data-stu-id="0d5a4-166">DirectShow Filters</span></span>

<span data-ttu-id="0d5a4-167">Das Windows Media-Format SDK enthält zwei Microsoft DirectShow-® Filter, mit denen DirectShow-basierte Anwendungen die Möglichkeit haben, ASF-Dateien zu lesen und zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-167">The Windows Media Format SDK includes two Microsoft DirectShow® filters that enable DirectShow-based applications to read and write ASF files.</span></span> <span data-ttu-id="0d5a4-168">Mithilfe von DirectShow können Anwendungen auch Daten von audiovideogeräten erfassen und Daten aus verschiedenen Formaten dekomprimieren, bevor Sie Sie als Windows Media-basierte Inhalte neu codieren.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-168">DirectShow also enables applications to capture data from audio-video devices and decompress data from a variety of formats before re-encoding it as Windows Media-based content.</span></span>

## <a name="enhanced-profiles"></a><span data-ttu-id="0d5a4-169">Erweiterte profile</span><span class="sxs-lookup"><span data-stu-id="0d5a4-169">Enhanced Profiles</span></span>

<span data-ttu-id="0d5a4-170">Profile können Informationen zur Bandbreiten Freigabe und Informationen zur streampriorisierung enthalten.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-170">Profiles can contain bandwidth sharing information and stream prioritization information.</span></span> <span data-ttu-id="0d5a4-171">Mit der Bandbreiten Freigabe können Sie angeben, dass für zwei oder mehr Datenströme unabhängig von den einzelnen Bitraten niemals mehr als eine angegebene Bandbreite verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-171">Bandwidth sharing enables you to specify that two or more streams, regardless of their individual bit rates, will never use more than a specified amount of bandwidth.</span></span> <span data-ttu-id="0d5a4-172">Die Bandbreiten Freigabe von Daten in einem Profil ist nur eine Informations Meldung. Sie wird von keiner Logik im SDK erzwungen.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-172">The bandwidth sharing data in a profile is purely informational; it is not enforced by any logic in the SDK.</span></span> <span data-ttu-id="0d5a4-173">Mithilfe der streampriorisierung können Sie eine Prioritäts Priorität für die Datenströme in einem Profil angeben.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-173">Stream prioritization enables you to specify an order of priority for the streams in a profile.</span></span> <span data-ttu-id="0d5a4-174">Wenn bei der Wiedergabe nicht genügend Bandbreite vorhanden ist, um die Datei ordnungsgemäß zu streamen, können Datenströme mit niedrigster Priorität ignoriert werden, um die Leistung zu verbessern</span><span class="sxs-lookup"><span data-stu-id="0d5a4-174">If there is not enough bandwidth at playback to stream the file properly, the lowest priority streams can be ignored in order to improve performance.</span></span>

## <a name="drm-writing-capability"></a><span data-ttu-id="0d5a4-175">DRM-Schreibfunktion</span><span class="sxs-lookup"><span data-stu-id="0d5a4-175">DRM Writing Capability</span></span>

<span data-ttu-id="0d5a4-176">Zusätzlich zu der vorhandenen Unterstützung für DRM-Lesevorgänge hat das Windows Media Format 9-Serie-SDK Unterstützung für das Schreiben von ASF-Dateien mit DRM-Version 1 oder DRM-Schutz Version 7 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-176">In addition to the existing DRM-reading support, the Windows Media Format 9 Series SDK added support for writing ASF files with either DRM version 1 or DRM version 7 protection.</span></span> <span data-ttu-id="0d5a4-177">Diese neue Funktion ermöglicht "Live DRM-Szenarien", wie z. b. Pay-per-View-Webcasting von Live Sportveranstaltungen oder Konzerten.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-177">This new capability enables "Live DRM" scenarios such as pay-per-view webcasting of live sporting events or concerts.</span></span>

## <a name="enhanced-file-sink"></a><span data-ttu-id="0d5a4-178">Erweiterte Datei Senke</span><span class="sxs-lookup"><span data-stu-id="0d5a4-178">Enhanced File Sink</span></span>

<span data-ttu-id="0d5a4-179">Der 9-Serienversion des SDK wurden mehrere neue dateisenke-Funktionen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-179">Several new file sink capabilities were added to the 9 Series version of the SDK.</span></span> <span data-ttu-id="0d5a4-180">Sie können die Datei Senke so konfigurieren, dass die automatische Indizierung neu erstellter ASF-Dateien deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-180">You can configure the file sink to disable automatic indexing of newly created ASF files.</span></span> <span data-ttu-id="0d5a4-181">Sie haben auch die Möglichkeit, Sie für nicht gepufferte Eingaben und Ausgaben zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-181">You also have the option to configure it for unbuffered input and output.</span></span>

## <a name="directx-video-acceleration"></a><span data-ttu-id="0d5a4-182">DirectX-Video Beschleunigung</span><span class="sxs-lookup"><span data-stu-id="0d5a4-182">DirectX Video Acceleration</span></span>

<span data-ttu-id="0d5a4-183">Bei DirectX Video Acceleration (DXVA) handelt es sich um eine Technologie, die die Wiedergabe von Videos mit hoher Bitrate (DVD-Qualität oder besser) auf weniger leistungsfähigen Computern mit DXVA-fähigen Grafikkarten ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-183">DirectX Video Acceleration (DXVA) is a technology that enables playback of high-bit-rate video (DVD quality or better) on less powerful machines with DXVA-enabled graphics cards.</span></span> <span data-ttu-id="0d5a4-184">Sie können das Reader-Objekt dieses SDK verwenden, um die DirectX-Video Beschleunigung bei der Wiedergabe von ASF-Dateien zu aktivieren, wenn die Hardware dies unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-184">You can use the reader object of this SDK to enable DirectX Video Acceleration, if the hardware supports it, when playing ASF files.</span></span>

## <a name="multichannel-audio"></a><span data-ttu-id="0d5a4-185">Multichannel-Audiodatei</span><span class="sxs-lookup"><span data-stu-id="0d5a4-185">Multichannel Audio</span></span>

<span data-ttu-id="0d5a4-186">Sie können Multichannel-audiocode codieren und wiedergeben.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-186">You can encode and play multichannel audio.</span></span> <span data-ttu-id="0d5a4-187">Der Windows Media Audio 9 Professional-Codec unterstützt Formate mit 6 Kanälen und acht Kanälen sowie eine Stereo-High-Definition.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-187">The Windows Media Audio 9 Professional codec supports formats with 6 channels and 8 channels as well as high definition stereo.</span></span>

## <a name="watermarking"></a><span data-ttu-id="0d5a4-188">Grenzwerte</span><span class="sxs-lookup"><span data-stu-id="0d5a4-188">Watermarking</span></span>

<span data-ttu-id="0d5a4-189">Sie können ASF-Dateien mit digitalen Wasserzeichen für die Sicherheit codieren.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-189">You can encode ASF files with digital watermarks for security.</span></span> <span data-ttu-id="0d5a4-190">Alle Wasserzeichen Systeme unterscheiden sich in ihrem Ansatz, aber alle Betten die Identifizierung in codierten Inhalt ein.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-190">All watermarking systems are different in their approach, but all embed identification into encoded content.</span></span> <span data-ttu-id="0d5a4-191">Das Wasserzeichen wird mithilfe spezieller DirectX® Media Objects (DMOs) von Drittanbietern ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-191">Watermarking is performed using special third-party DirectX® media objects (DMOs).</span></span>

## <a name="support-for-multiple-languages-in-asf-files"></a><span data-ttu-id="0d5a4-192">Unterstützung für mehrere Sprachen in ASF-Dateien</span><span class="sxs-lookup"><span data-stu-id="0d5a4-192">Support for Multiple Languages in ASF files</span></span>

<span data-ttu-id="0d5a4-193">Sie können mehrere Sprachen in ASF-Dateien sowohl in Streams als auch in Metadaten unterstützen.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-193">You can support multiple languages in ASF files, both in streams and in metadata.</span></span> <span data-ttu-id="0d5a4-194">Beispielsweise können Sie eine Videodatei mit Audiodatenströmen in verschiedenen Sprachen erstellen.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-194">For example, you can create a video file with audio streams in several languages.</span></span> <span data-ttu-id="0d5a4-195">Bei der Wiedergabe kann der Benutzer auswählen, welche Sprache verwendet werden soll, oder die Anwendung kann die Systeminformationen auf dem wiedergegebenen Computer Abfragen und automatisch eine Sprache auswählen.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-195">At playback, the user can select which language to use, or your application can query the system information on the playing computer and select a language automatically.</span></span> <span data-ttu-id="0d5a4-196">Metadatenattribute können auch mehrmals eingegeben werden, mit den Werten in verschiedenen Sprachen.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-196">Metadata attributes can also be entered multiple times, with the values in different languages.</span></span>

## <a name="device-conformance-templates"></a><span data-ttu-id="0d5a4-197">Geräte Konformitäts Vorlagen</span><span class="sxs-lookup"><span data-stu-id="0d5a4-197">Device Conformance Templates</span></span>

<span data-ttu-id="0d5a4-198">Zur Unterstützung bei der Ausrichtung von Inhalten auf bestimmte Client Geräte unterstützen die Windows Media-Codecs nun Geräte Konformitäts Vorlagen.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-198">To assist in targeting content to specific client devices, the Windows Media codecs now support device conformance templates.</span></span> <span data-ttu-id="0d5a4-199">Jede Vorlage enthält einen definierten Bereich von Einstellungen und Codec-Funktionen, die für Medien verwendet werden sollen, die für eine bestimmte Platt Form Plattform gedacht sind.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-199">Each template contains a defined range of settings and codec features that should be used for media intended for a particular category of platforms.</span></span> <span data-ttu-id="0d5a4-200">System Profile werden in den neuesten Versionen der Windows Media-Codecs nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-200">System profiles are no longer supported with the latest versions of the Windows Media codecs.</span></span> <span data-ttu-id="0d5a4-201">Alle Profile müssen Ihren Anforderungen entsprechend angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-201">All profiles must be customized to suit your needs.</span></span> <span data-ttu-id="0d5a4-202">Sie können Geräte Konformitäts Vorlagen verwenden, um Sie beim Entwerfen von Profilen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-202">You can use device conformance templates to assist you in designing your profiles.</span></span>

## <a name="expanded-codec-enumeration"></a><span data-ttu-id="0d5a4-203">Erweiterte Codec-Enumeration</span><span class="sxs-lookup"><span data-stu-id="0d5a4-203">Expanded Codec Enumeration</span></span>

<span data-ttu-id="0d5a4-204">Das Profil-Manager-Objekt kann die Windows Media Audio und Video Codecs nach unterstützten Formaten Abfragen.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-204">The profile manager object can query the Windows Media Audio and Video codecs for supported formats.</span></span> <span data-ttu-id="0d5a4-205">Sie können Parameter für die abgerufenen Formate festlegen.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-205">You can set parameters for the formats retrieved.</span></span> <span data-ttu-id="0d5a4-206">Beispielsweise können Sie alle Qualitäts basierten Variablen Bitrate-Formate abrufen, die vom Windows Media Audio 9-Codec unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-206">For example, you can retrieve all the quality-based variable bit rate formats supported by the Windows Media Audio 9 codec.</span></span>

## <a name="improved-mutual-exclusion"></a><span data-ttu-id="0d5a4-207">Verbesserter gegenseitiger Ausschluss</span><span class="sxs-lookup"><span data-stu-id="0d5a4-207">Improved Mutual Exclusion</span></span>

<span data-ttu-id="0d5a4-208">Sie können benannte Datensätze erstellen, die mehrere Datenströme innerhalb eines gegenseitigen Ausschluss Objekts enthalten.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-208">You can create named records containing multiple streams within a mutual exclusion object.</span></span> <span data-ttu-id="0d5a4-209">Sie können auch Objekte für die gegenseitige Ausschluss benennen, um Sie leichter zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-209">You can also name mutual exclusion objects to make them easier to identify.</span></span> <span data-ttu-id="0d5a4-210">Dies ermöglicht Ihnen das Erstellen von Ebenen des gegenseitigen Ausschlusses.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-210">This enables you to create layers of mutual exclusion.</span></span> <span data-ttu-id="0d5a4-211">Eine Datei kann z. b. Datenströme enthalten, die sich nach Bitrate und Sprache gegenseitig ausschließen.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-211">For example, a file can contain streams that are mutually exclusive by bit rate and by language.</span></span> <span data-ttu-id="0d5a4-212">Der sprachbasierte gegenseitige Ausschluss umfasst Gruppen von Streams, jede Gruppe, die aus Streams in derselben Sprache besteht, aber sich gegenseitig von der Bitrate ausschließen.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-212">The language-based mutual exclusion would involve groups of streams, each group consisting of streams in the same language but mutually exclusive by bit rate.</span></span>

## <a name="expanded-multiple-bit-rate-support"></a><span data-ttu-id="0d5a4-213">Erweiterte Unterstützung für mehrere Bitraten</span><span class="sxs-lookup"><span data-stu-id="0d5a4-213">Expanded Multiple Bit Rate Support</span></span>

<span data-ttu-id="0d5a4-214">Die Unterstützung gegenseitiger Ausschluss ist für MBR-Audiodaten (Multiple Bitrate) und für Videos mit unterschiedlichen Bildgrößen enthalten.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-214">Mutual exclusion support is included for multiple bit rate (MBR) audio and for video with streams of varying image sizes.</span></span>

## <a name="attributes-for-streams"></a><span data-ttu-id="0d5a4-215">Attribute für Streams</span><span class="sxs-lookup"><span data-stu-id="0d5a4-215">Attributes for Streams</span></span>

<span data-ttu-id="0d5a4-216">Sie können einzelnen Streams in ASF-Dateien Attribute zuweisen.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-216">You can assign attributes to individual streams in ASF files.</span></span> <span data-ttu-id="0d5a4-217">Sie müssen weiterhin Attribute auf Dateiebene für MP3-Dateien verwenden.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-217">You must still use file-level attributes for MP3 files.</span></span> <span data-ttu-id="0d5a4-218">Diese Funktion fügt dem SDK keine Methoden hinzu, aber die vorhandenen Methoden akzeptieren jetzt streamnummern außer 0 (null).</span><span class="sxs-lookup"><span data-stu-id="0d5a4-218">This feature does not add any methods to the SDK, but the existing methods will now accept stream numbers other than zero.</span></span>

## <a name="transcoding-with-smart-recompression"></a><span data-ttu-id="0d5a4-219">Transcoding mit intelligenter Neukomprimierung</span><span class="sxs-lookup"><span data-stu-id="0d5a4-219">Transcoding with Smart Recompression</span></span>

<span data-ttu-id="0d5a4-220">Die intelligente Neukomprimierung ermöglicht es Ihnen, Windows Media-Audiodateien von einer hohen Bitrate in eine niedrigere Bitrate zu transcodieren, die eine bessere Qualität als zuvor erreicht hat.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-220">Smart recompression allows you to transcode Windows Media audio files from a high bit rate to a lower bit rate with better quality than previously achievable.</span></span>

## <a name="expanded-metadata-support"></a><span data-ttu-id="0d5a4-221">Erweiterte Metadatenunterstützung</span><span class="sxs-lookup"><span data-stu-id="0d5a4-221">Expanded Metadata Support</span></span>

<span data-ttu-id="0d5a4-222">Das Windows Media-Format SDK bietet die folgenden neuen Metadatenfeatures:</span><span class="sxs-lookup"><span data-stu-id="0d5a4-222">The Windows Media Format SDK provides the following new metadata features:</span></span>

-   <span data-ttu-id="0d5a4-223">Index basierte Metadatentags, die mehrere Tags mit dem gleichen Namen ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-223">Index-based metadata tags, enabling multiple tags with the same name.</span></span>
-   <span data-ttu-id="0d5a4-224">Möglichkeit zum Lesen von DRM-Header Attributen ohne wmstubdrm. lib-Datei.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-224">Ability to read DRM header attributes without a WMStubDRM.lib file.</span></span>
-   <span data-ttu-id="0d5a4-225">Attribute mit mehr als 64 Kilobyte zugeordneten Daten.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-225">Attributes with more than 64 kilobytes of associated data.</span></span>
-   <span data-ttu-id="0d5a4-226">Attribute in mehreren Sprachen.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-226">Attributes in multiple languages.</span></span>
-   <span data-ttu-id="0d5a4-227">Dutzende von neuen vordefinierten Attributen.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-227">Dozens of new predefined attributes.</span></span>

## <a name="dynamic-pixel-aspect-ratio"></a><span data-ttu-id="0d5a4-228">Verhältnis des dynamischen Pixel Aspekts</span><span class="sxs-lookup"><span data-stu-id="0d5a4-228">Dynamic Pixel Aspect Ratio</span></span>

<span data-ttu-id="0d5a4-229">Videostreams, die aus verschiedenen Inhaltstypen bestehen, können durch die Identifizierung des Pixel Seitenverhältnisses der unterschiedlichen Stichproben im Stream untersucht werden.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-229">Video streams that are composed of various types of content can be accommodated by identifying the pixel aspect ratio of the disparate samples in the stream.</span></span> <span data-ttu-id="0d5a4-230">Dadurch kann die Spiele Anwendung eine bessere Wiedergabe solcher Inhalte bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-230">This enables the playing application to provide better playback of such content.</span></span>

## <a name="interlaced-video-streams"></a><span data-ttu-id="0d5a4-231">Video Datenströme mit Zeilen Sprung</span><span class="sxs-lookup"><span data-stu-id="0d5a4-231">Interlaced Video Streams</span></span>

<span data-ttu-id="0d5a4-232">In früheren Versionen des SDK für den Windows Media-Format haben Sie die Möglichkeit bereitgestellt, Zeilen Sprung Inhalte in einen Videodaten Strom mit progressivem Scannen [*zu codieren*](wmformat-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="0d5a4-232">Previous versions of the Windows Media Format SDK have provided the ability to encode [*interlaced*](wmformat-glossary.md) content into a progressive-scan video stream.</span></span> <span data-ttu-id="0d5a4-233">Beginnend mit dem Windows Media Format 9-Reihe-SDK können Sie Zeilen Sprung Video codieren, während das Zeilen Sprung Format beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-233">Starting with the Windows Media Format 9 Series SDK, you can encode interlaced video while preserving its interlaced format.</span></span> <span data-ttu-id="0d5a4-234">Dies kann zu einer verbesserten Wiedergabe führen, insbesondere auf Zeilen Sprung Geräten, z. b. Fernseh Sets.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-234">This can result in improved playback, particularly on interlaced devices, such as television sets.</span></span>

## <a name="two-pass-encoding"></a><span data-ttu-id="0d5a4-235">Two-Pass Codierung</span><span class="sxs-lookup"><span data-stu-id="0d5a4-235">Two-Pass Encoding</span></span>

<span data-ttu-id="0d5a4-236">Die neuen Windows Media-Codecs ermöglichen die zwei-Pass-Codierung.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-236">The new Windows Media codecs enable two-pass encoding.</span></span> <span data-ttu-id="0d5a4-237">Inhalt, der in zwei Durchläufen codiert ist, kann eine höhere Qualität ausgeben</span><span class="sxs-lookup"><span data-stu-id="0d5a4-237">Content encoded in two passes can achieve higher quality output.</span></span>

## <a name="new-speech-codec"></a><span data-ttu-id="0d5a4-238">Neuer Sprachcodec</span><span class="sxs-lookup"><span data-stu-id="0d5a4-238">New Speech Codec</span></span>

<span data-ttu-id="0d5a4-239">Dieses SDK enthält den neuen Windows Media Audio 9-Sprachcodec, der für die Codierung der menschlichen Stimme bei niedriger Bitrate optimiert ist.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-239">This SDK includes the new Windows Media Audio 9 Voice codec which is optimized for encoding the human voice while using a low bit rate.</span></span> <span data-ttu-id="0d5a4-240">Dieser Codec bietet auch eine bessere Leistung für gemischte Musikinhalte.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-240">This codec also provides superior performance for mixed music-voice content.</span></span>

## <a name="accessible-video-frame-duration"></a><span data-ttu-id="0d5a4-241">Barrierefreie Video Frame Dauer</span><span class="sxs-lookup"><span data-stu-id="0d5a4-241">Accessible Video Frame Duration</span></span>

<span data-ttu-id="0d5a4-242">Sie können das Writer-Objekt dieses SDK zum Bereitstellen der Dauer von Video Frames für den Reader bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-242">You can have the writer object of this SDK provide the duration of video frames to the reader.</span></span>

## <a name="streaming-html"></a><span data-ttu-id="0d5a4-243">Streaming-HTML</span><span class="sxs-lookup"><span data-stu-id="0d5a4-243">Streaming HTML</span></span>

<span data-ttu-id="0d5a4-244">Mit der vorherigen Version dieses SDK konnten Sie einen Skript Befehl verwenden, um Ihrer Anwendung das Öffnen einer Webseite zu signalisieren.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-244">With previous version of this SDK, you were able to use a script command to signal your application to open a Web page.</span></span> <span data-ttu-id="0d5a4-245">Beginnend mit dem Windows Media Format 9-Reihe-SDK können Sie die Komponenten von Webseiten in ihren ASF-Dateien speichern, um sicherzustellen, dass es keine Verzögerung bei Präsentationen gibt.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-245">Starting with the Windows Media Format 9 Series SDK, you can store the components of Web pages in your ASF files, to ensure that there is no lag in presentations.</span></span>

## <a name="wmstublib-no-longer-required-for-build-environment"></a><span data-ttu-id="0d5a4-246">"Wmstub. lib" ist für die Buildumgebung nicht mehr erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-246">WMStub.lib no longer required for build environment</span></span>

<span data-ttu-id="0d5a4-247">Die buildumgebungseinstellungen für das SDK für Windows Media-Format wurden beginnend mit dem SDK für Windows Media-Serie 9 geändert.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-247">The build-environment settings for the Windows Media Format SDK changed starting with the Windows Media Format 9 Series SDK.</span></span> <span data-ttu-id="0d5a4-248">Sie müssen wmstub. lib nicht mehr für Anwendungen einschließen, die dieses SDK verwenden.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-248">You no longer need to include WMStub.lib for applications using this SDK.</span></span> <span data-ttu-id="0d5a4-249">Allerdings müssen DRM-fähige Anwendungen weiterhin einen separaten Lizenzvertrag abrufen und Signieren und eine eindeutige statische Bibliothek von Microsoft erhalten.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-249">However, DRM-enabled applications still must obtain and sign a separate license agreement, and obtain a unique static library from Microsoft.</span></span> <span data-ttu-id="0d5a4-250">Kontaktieren Sie, wmla@microsoft.com um weitere Informationen zur DRM-Bibliothek und zum Lizenzvertrag zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0d5a4-250">Contact wmla@microsoft.com for more information about the DRM library and license agreement.</span></span> <span data-ttu-id="0d5a4-251">Weitere Informationen zum Aufbau von Projekten mit diesem SDK finden Sie unter [Bibliotheksdateien und Compilereinstellungen](library-files-and-compiler-settings.md).</span><span class="sxs-lookup"><span data-stu-id="0d5a4-251">For more information about building projects with this SDK, see [Library Files and Compiler Settings](library-files-and-compiler-settings.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d5a4-252">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0d5a4-252">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d5a4-253">**Informationen zum Windows Media-Format-SDK**</span><span class="sxs-lookup"><span data-stu-id="0d5a4-253">**About the Windows Media Format SDK**</span></span>](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




