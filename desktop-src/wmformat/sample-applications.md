---
title: Beispielanwendungen für das Windows Media-Format-SDK
description: Beispielanwendungen für das Windows Media-Format-SDK
ms.assetid: 037741cb-c5fb-485f-bf62-79b5465abfe4
keywords:
- Windows Media-Format-SDK, Beispielanwendungen
- Digital Rights Management (DRM), Beispielanwendungen
- DRM (Digital Rights Management), Beispielanwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ce7a9baf53c289e9420cf3c226bf21a3c6bd16
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474868"
---
# <a name="windows-media-format-sdk-sample-applications"></a><span data-ttu-id="6511e-106">Beispielanwendungen für das Windows Media-Format-SDK</span><span class="sxs-lookup"><span data-stu-id="6511e-106">Windows Media Format SDK Sample Applications</span></span>

<span data-ttu-id="6511e-107">Der Beispielcode, der mit diesem SDK bereitgestellt wird, ist in Form von Projekten für Microsoft Visual Studio 2005.</span><span class="sxs-lookup"><span data-stu-id="6511e-107">The sample code supplied with this SDK is in the form of projects for Microsoft Visual Studio 2005.</span></span> <span data-ttu-id="6511e-108">Die meisten Beispiele sind in C++, aber managedwmf sdkwrapper und ManagedMetadataEdit erfordern c#.</span><span class="sxs-lookup"><span data-stu-id="6511e-108">Most of the samples are in C++, but ManagedWMFSDKWrapper and ManagedMetadataEdit require C#.</span></span>

<span data-ttu-id="6511e-109">Diese Beispiele können nur verwendet werden, wenn das Windows Media-Format-SDK oder das Windows Player SDK installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="6511e-109">These samples will not work unless the Windows Media Format SDK or the Windows Player SDK has been installed.</span></span>

<span data-ttu-id="6511e-110">Verwendungs Informationen für die einzelnen Beispiele sind in einer readme.txt-Datei in jedem Beispiel Verzeichnis enthalten.</span><span class="sxs-lookup"><span data-stu-id="6511e-110">Usage information for each sample is contained in a readme.txt file in each sample directory.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6511e-111">Samle</span><span class="sxs-lookup"><span data-stu-id="6511e-111">Samle</span></span></th>
<th><span data-ttu-id="6511e-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6511e-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6511e-113">Audioplayer</span><span class="sxs-lookup"><span data-stu-id="6511e-113">AudioPlayer</span></span></td>
<td><span data-ttu-id="6511e-114">Gibt Windows Media-Dateien einschließlich von DRM-geschützten Dateien wieder.</span><span class="sxs-lookup"><span data-stu-id="6511e-114">Plays Windows Media files including DRM-protected files.</span></span> <span data-ttu-id="6511e-115">Sie wird über eine grafische Benutzeroberfläche gesteuert, und die Befehle umfassen abspielen, anhalten, suchen und anhalten.</span><span class="sxs-lookup"><span data-stu-id="6511e-115">It is controlled through a GUI, and commands include Play, Pause, Seek and Stop.</span></span> <span data-ttu-id="6511e-116">Es können lokale Dateien oder Dateien wiedergegeben werden, die aus dem Internet gelesen wurden (einschließlich der Ausgabe im Internet mithilfe des wmvnetwrite-Beispiels).</span><span class="sxs-lookup"><span data-stu-id="6511e-116">It can play local files or files read from the Internet (including those output to the Internet by using the WMVNetWrite sample).</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="6511e-117">Die DRM-Teile dieses Beispiels werden auf x64-basierten Versionen von Windows nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6511e-117">The DRM portions of this sample are not supported on x64-based versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6511e-118">DrmHeader</span><span class="sxs-lookup"><span data-stu-id="6511e-118">DRMHeader</span></span></td>
<td><span data-ttu-id="6511e-119">DrmHeader ist eine Konsolenanwendung, die die <a href="/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor"><strong>iwmdrmeditor</strong></a> -Schnittstelle des Metadaten-Editors zum Lesen von DRM-Attributen von Dateien verwendet, ohne mit der statischen DRM-Bibliothek zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="6511e-119">DRMHeader is a console application that uses the metadata editor's <a href="/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor"><strong>IWMDRMEditor</strong></a> interface to read DRM attributes of files without linking to the DRM static library.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="6511e-120">Dieses Beispiel wird in x64-basierten Versionen von Windows nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6511e-120">This sample is not supported on x64-based versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6511e-121">Drmshow</span><span class="sxs-lookup"><span data-stu-id="6511e-121">DRMShow</span></span></td>
<td><span data-ttu-id="6511e-122">Drmshow ist eine Konsolenanwendung, die zeigt, wie <a href="wmformat-glossary.md"><em>DRM</em></a> -Eigenschaften einer Windows Media-Datei mithilfe der Methode " <strong>iwmdrmreader:: getdrmproperty</strong> " gelesen werden. Dieses Beispiel veranschaulicht die Verwendung der <strong>iwmdrmreader:: getdrmproperty</strong> -Methode und die Eigenschaften, die vom DRM-Reader abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="6511e-122">DRMShow is a console application that shows how to read <a href="wmformat-glossary.md"><em>DRM</em></a> properties of a Windows Media file using the <strong>IWMDRMReader::GetDRMProperty</strong> method.This sample demonstrates the use of the <strong>IWMDRMReader::GetDRMProperty</strong> method and the properties that can be retrieved from the DRM reader.</span></span> <span data-ttu-id="6511e-123">Es wird nicht gezeigt, wie Sie eine Lizenz für DRM-geschützte Inhalte erwerben.</span><span class="sxs-lookup"><span data-stu-id="6511e-123">It does not demonstrate how to acquire a license for DRM-protected content.</span></span> <span data-ttu-id="6511e-124">Für dieses Beispiel ist die DRM-Stub-Bibliothek wmstubdrm. lib erforderlich, um zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6511e-124">This sample requires the DRM stub library WMStubDRM.lib to build.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="6511e-125">Dieses Beispiel wird in x64-basierten Versionen von Windows nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6511e-125">This sample is not supported on x64-based versions of Windows.</span></span>
</blockquote>
<br/> <span data-ttu-id="6511e-126">Wenn Sie wmstubdrm. lib von Microsoft abrufen, wird der Bibliothek eine Anwendungs Sicherheitsstufe zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="6511e-126">When you acquire the WMStubDRM.lib from Microsoft, the library is assigned an application security level.</span></span> <span data-ttu-id="6511e-127">Wenn die Sicherheitsstufe der Bibliothek, die Sie erhalten, nicht ausreichen, um eine geschützte Datei wiederzugeben, wird in diesem Beispiel ein Fehler angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6511e-127">If the security level of the library you receive is not sufficient to play a protected file, this sample will display an error.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6511e-128">Directshowinterop/dscopy</span><span class="sxs-lookup"><span data-stu-id="6511e-128">DirectShowInterop/DSCopy</span></span></td>
<td><span data-ttu-id="6511e-129">Transcodiert eine oder mehrere Dateien in eine ASF-Datei mithilfe des DirectShow WM ASF Writer-Filters.</span><span class="sxs-lookup"><span data-stu-id="6511e-129">Transcodes one or more files to an ASF file using the DirectShow  WM ASF Writer filter.</span></span> <span data-ttu-id="6511e-130">Die Eingabedatei kann jedes komprimierte oder nicht komprimierte Format aufweisen, das von DirectShow unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="6511e-130">The input file may be any compressed or uncompressed format supported by DirectShow.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6511e-131">Directshowinterop/dsplay</span><span class="sxs-lookup"><span data-stu-id="6511e-131">DirectShowInterop/DSPlay</span></span></td>
<td><span data-ttu-id="6511e-132">Dieses Beispiel ist ein interaktiver Audiodatei-Player mit <a href="wmformat-glossary.md"><em>DRM</em></a> -Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="6511e-132">This sample is an interactive audio/video media file player with <a href="wmformat-glossary.md"><em>DRM</em></a> support.</span></span> <span data-ttu-id="6511e-133">Er verwendet den WM-"WM-ASF-Reader"-Filter von DirectShow, um Windows Media-Dateien (ASF, WMA, WMV) ohne DRM-Schutz und Dateien wiederzugeben, die DRM auf der Ebene 100 oder niedriger verwenden.</span><span class="sxs-lookup"><span data-stu-id="6511e-133">It uses DirectShow's WM ASF Reader filter to play Windows Media files (ASF, WMA, WMV) without DRM protection and files which use DRM at a level of 100 or below.</span></span> <span data-ttu-id="6511e-134">Weitere Informationen finden Sie unter readme.txt im Verzeichnis des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="6511e-134">See readme.txt in the sample's directory for more information.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6511e-135">Directshowinterop/dsseekfm</span><span class="sxs-lookup"><span data-stu-id="6511e-135">DirectShowInterop/DSSeekFm</span></span></td>
<td><span data-ttu-id="6511e-136">In diesem Beispiel wird veranschaulicht, wie Sie den DirectShow-WM-,-und-Filter zum Wiedergeben von ASF-Inhalten in einem DirectShow-Filter Diagramm verwenden. Außerdem wird erläutert, wie Sie den Frame suchen, der Unterstützung im Windows Media SDK</span><span class="sxs-lookup"><span data-stu-id="6511e-136">This sample demonstrates how to use the DirectShow WM ASF Reader Filter to play ASF content in a DirectShow filter graph, and also how to use the frame seeking support in the Windows Media Format SDK.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6511e-137">Verwaltet/WMF sdkwrapper</span><span class="sxs-lookup"><span data-stu-id="6511e-137">Managed/WMFSDKWrapper</span></span></td>
<td><span data-ttu-id="6511e-138">Diese verwaltete Assembly dient als Wrapper, der von Beispielen für verwalteten Code für den Zugriff auf einige Metadatenschnittstellen dieses SDK verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6511e-138">This managed assembly serves as a wrapper used by managed-code samples for accessing some metadata interfaces of this SDK.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6511e-139">Verwaltet/MetadataEdit</span><span class="sxs-lookup"><span data-stu-id="6511e-139">Managed/MetadataEdit</span></span></td>
<td><span data-ttu-id="6511e-140">Diese c#-Anwendung kann verwendet werden, um Metadaten aus Windows-Mediendateien anzuzeigen und zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="6511e-140">This C# application can be used to view and edit metadata from Windows Media files.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6511e-141">MetaDataEdit</span><span class="sxs-lookup"><span data-stu-id="6511e-141">MetaDataEdit</span></span></td>
<td><span data-ttu-id="6511e-142">Dies ist eine C++-Version der verwalteten MetadataEdit-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="6511e-142">This is a C++ version of the Managed MetadataEdit application.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6511e-143">"Read FromStream"</span><span class="sxs-lookup"><span data-stu-id="6511e-143">ReadFromStream</span></span></td>
<td><span data-ttu-id="6511e-144">In diesem Beispiel für eine Konsolenanwendung wird gezeigt, wie Daten aus <strong>IStream</strong> mit wmreader gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="6511e-144">This console application sample shows how to read data from <strong>IStream</strong> with WMReader.</span></span> <span data-ttu-id="6511e-145">Die <strong>IStream</strong> -Quelle wurde implementiert, um eine Datei im Windows Media-Format (WMA/WMV/ASF) zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="6511e-145"><strong>IStream</strong> source has been implemented to use a file in Windows Media Format (WMA/WMV/ASF).</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="6511e-146">In diesem Beispiel wird nicht gezeigt, wie die aus wmreader ausgehenden Medien Beispiele verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="6511e-146">This sample does not show how to process the media samples coming out of WMReader.</span></span> <span data-ttu-id="6511e-147">Beispiele zum Verarbeiten von Audiodateien/Videos oder anderen Typen von Medien Beispielen finden Sie in den anderen Beispielen, z.b. Audioplayer, die im Windows Media-Format-SDK enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="6511e-147">For examples on how to process audio/video or other types of media samples, please refer to other samples, for instance AudioPlayer, that are included with the Windows Media Format SDK.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6511e-148">Uncompavitowmv</span><span class="sxs-lookup"><span data-stu-id="6511e-148">UncompAVIToWMV</span></span></td>
<td><span data-ttu-id="6511e-149">In diesem Beispiel für eine Konsolenanwendung wird der erforderliche Code zum Komprimieren einer AVI-Datei in eine WMV-Datei gezeigt.</span><span class="sxs-lookup"><span data-stu-id="6511e-149">This console application sample shows the necessary code to compress an AVI file to a WMV file.</span></span> <span data-ttu-id="6511e-150">Es zeigt, wie Sie Beispiele für Audiodaten und Videostreams aus verschiedenen AVI-Dateien zusammenführen und entweder in ähnliche Streams zusammenführen oder basierend auf dem Quelldaten Strom Profil einen neuen Stream erstellen.</span><span class="sxs-lookup"><span data-stu-id="6511e-150">It shows how to merge samples for audio and video streams from several AVI files and either merge these into similar streams or create a new stream based on the source stream profile.</span></span> <span data-ttu-id="6511e-151">Außerdem wird gezeigt, wie ein beliebiger Stream erstellt, Multipass-Codierung ausgeführt, SMPTE-Zeit Code hinzugefügt und der DRM-Schutz auf Version 1 angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="6511e-151">It also shows how to create an arbitrary stream, do multipass encoding, add SMPTE time code, and apply DRM version 1 protection.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6511e-152">Wmgenprofil/exe</span><span class="sxs-lookup"><span data-stu-id="6511e-152">WMGenProfile/exe</span></span></td>
<td><span data-ttu-id="6511e-153">Dieses Beispiel wurde von Version 7,1 aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="6511e-153">This sample has been updated from the 7.1 release.</span></span> <span data-ttu-id="6511e-154">Es ist jetzt eine MFC-Dialog Feld Anwendung.</span><span class="sxs-lookup"><span data-stu-id="6511e-154">It is now an MFC Dialog application.</span></span> <span data-ttu-id="6511e-155">Das wmgenprofile-Beispiel veranschaulicht die Verwendung der statischen wmgenprofile-Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="6511e-155">WMGenProfile sample demonstrates the use of the WMGenProfile static library.</span></span> <span data-ttu-id="6511e-156">Es dient auch als Tool für die Erstellung von Profilen.</span><span class="sxs-lookup"><span data-stu-id="6511e-156">It also serves as a tool for the creation of profiles.</span></span> <span data-ttu-id="6511e-157">Dieses Tool ist für Entwickler bestimmt, die mit dem Windows Media-Format vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="6511e-157">This tool is meant for developers familiar with the Windows Media Format.</span></span> <span data-ttu-id="6511e-158">Die Benutzeroberfläche wurde nicht für die Benutzeroberfläche getestet und ist nicht als Empfehlung zur Darstellung dieser Informationen für einen Benutzer gedacht.</span><span class="sxs-lookup"><span data-stu-id="6511e-158">The UI has not been tested for user experience and is not meant as a recommendation about how to present this information to a user.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6511e-159">Wmgenprofil/lib</span><span class="sxs-lookup"><span data-stu-id="6511e-159">WMGenProfile/lib</span></span></td>
<td><span data-ttu-id="6511e-160">Das Beispiel für die genprofile-Bibliothek veranschaulicht die Erstellung von Profilen.</span><span class="sxs-lookup"><span data-stu-id="6511e-160">The GenProfile library sample demonstrates the creation of profiles.</span></span> <span data-ttu-id="6511e-161">Es wird gezeigt, wie Medientypen und Streams für verschiedene Streamtypen (Audiodaten, Videos, Skripts, Bilder, Dateiübertragungen und Web) erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6511e-161">It shows how to create media types and streams for various stream types (audio, video, script, image, file transfer, and Web).</span></span> <span data-ttu-id="6511e-162">Es wird nicht gezeigt, wie Sie mit Systemprofilen arbeiten oder Systemprofile in Profile konvertieren, die die Codecs für die Windows Media Audio-und Video 9-Serie angeben.</span><span class="sxs-lookup"><span data-stu-id="6511e-162">It does not demonstrate how to work with system profiles or how to convert system profiles to profiles that specify the Windows Media Audio and Video 9 Series codecs.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6511e-163">Wmprop</span><span class="sxs-lookup"><span data-stu-id="6511e-163">WMProp</span></span></td>
<td><span data-ttu-id="6511e-164">Diese Konsolenanwendung veranschaulicht, wie Attribute mithilfe des Metadateneditor-Objekts und der Profilinformationen des Readers abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="6511e-164">This console application demonstrates how to retrieve attributes by using the metadata editor object and profile information from the reader.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6511e-165">Wmstats</span><span class="sxs-lookup"><span data-stu-id="6511e-165">WMStats</span></span></td>
<td><span data-ttu-id="6511e-166">Diese Konsolenanwendung zeigt Reader-und Writer-Statistiken an.</span><span class="sxs-lookup"><span data-stu-id="6511e-166">This console application displays Reader and Writer statistics.</span></span> <span data-ttu-id="6511e-167">Mehrere Instanzen von wmstats können auch gleichzeitig auf einem Computer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6511e-167">Multiple instances of WMStats can also be used concurrently on one machine.</span></span> <span data-ttu-id="6511e-168">Starten Sie eine Instanz als Server, um den Datenstrom an das Netzwerk zu senden, und führen Sie dann eine zweite Instanz als Client aus, um zu überprüfen, ob der Server ordnungsgemäß Streaming.</span><span class="sxs-lookup"><span data-stu-id="6511e-168">Start one instance as a server to send the stream to the network and then run a second instance as a client to verify that server is streaming correctly.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6511e-169">Wmsynkreader</span><span class="sxs-lookup"><span data-stu-id="6511e-169">WMSyncReader</span></span></td>
<td><span data-ttu-id="6511e-170">In diesem Beispiel für eine Konsolenanwendung wird gezeigt, wie eine Mediendatei mithilfe von <strong>iwmsynanader</strong> gelesen wird, ohne dass ein zusätzlicher Thread erstellt oder Rückrufe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6511e-170">This console application sample shows how to read a media file using <strong>IWMSyncReader</strong> without creating any extra thread or using callbacks.</span></span> <span data-ttu-id="6511e-171">Die folgenden Features werden implementiert: Lesen von komprimierten oder dekomprimierten Beispielen</span><span class="sxs-lookup"><span data-stu-id="6511e-171">The following features are implemented :Reading compressed or decompressed samples</span></span><br/> <span data-ttu-id="6511e-172">Zeitbasierte Suche</span><span class="sxs-lookup"><span data-stu-id="6511e-172">Time-based seeking</span></span><br/> <span data-ttu-id="6511e-173">Frame basiertes suchen</span><span class="sxs-lookup"><span data-stu-id="6511e-173">Frame-based seeking</span></span><br/> <span data-ttu-id="6511e-174">Von <strong>IStream</strong> abgeleitete Quelle</span><span class="sxs-lookup"><span data-stu-id="6511e-174"><strong>IStream</strong> derived source</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6511e-175">Wmvappend</span><span class="sxs-lookup"><span data-stu-id="6511e-175">WMVAppend</span></span></td>
<td><span data-ttu-id="6511e-176">Diese Konsolenanwendung nimmt zwei Windows Media-Dateien für die Eingabe an und versucht, eine Ausgabedatei mit dem Inhalt der ersten, gefolgt von der zweiten, zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6511e-176">This console application takes two Windows Media files for input, and attempts to create an output file with the contents of the first followed by the second.</span></span> <span data-ttu-id="6511e-177">Im Beispiel werden die Profile der beiden Eingabedateien verglichen, um sicherzustellen, dass Sie so ähnlich sind, dass Sie angefügt werden.</span><span class="sxs-lookup"><span data-stu-id="6511e-177">The sample compares the profiles of the two input files to ensure they are similar enough to be appended.</span></span> <span data-ttu-id="6511e-178">Wenn dies nicht der Fall ist, wird eine Fehlermeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6511e-178">If this is not the case, an error message appears.</span></span> <span data-ttu-id="6511e-179">Beispielsweise tritt eine Fehlermeldung auf, wenn eine Datei nur Audiodaten und das zweite eine audiovideodatei ist oder wenn zwei Audiodateien unterschiedliche Bitraten aufweisen. Das Beispiel akzeptiert VBR-Quellen (Variable Bitrate).</span><span class="sxs-lookup"><span data-stu-id="6511e-179">For example, an error message occurs when one file is audio only and the second is an audio-video file, or when two audio files have different bit rates.The sample accepts variable bit rate (VBR) sources.</span></span> <span data-ttu-id="6511e-180">Beim Vergleich der Profile der beiden VBR-Quellen ignoriert das Beispiel die durchschnittliche Bitrate Differenz, da zwei VBR-Streams verschiedene durchschnittliche Bitraten aufweisen, auch wenn Sie mit demselben Profil erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="6511e-180">However, when comparing the profiles of the two VBR sources, the sample ignores the average bit rate difference because two VBR streams will have different average bit rates even if they were created using the same profile.</span></span> <span data-ttu-id="6511e-181">Wmvappend kann die Spitzen Bitrate von nicht eingeschränkten Bitrate-basierten VBR-Streams oder die Qualitätsstufe von Qualitäts basierten VBR-Streams nicht vergleichen, da diese Informationen nicht in den Quelldateien vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="6511e-181">WMVAppend cannot compare the peak bit rate of unconstrained bit-rate-based VBR streams, or the quality level of quality-based VBR streams, because this information does not exist in the source files.</span></span> <span data-ttu-id="6511e-182">Daher liegt es in der Verantwortung des Benutzers, sicherzustellen, dass zwei Quelldateien mit demselben Profil erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6511e-182">It is therefore the user's responsibility to make sure that two source files are created using the same profile.</span></span> <span data-ttu-id="6511e-183">Andernfalls kann ein ungültiger Inhalt erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6511e-183">Otherwise, invalid content can be created.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6511e-184">Wmvcopy</span><span class="sxs-lookup"><span data-stu-id="6511e-184">WMVCopy</span></span></td>
<td><span data-ttu-id="6511e-185">Dieses Beispiel zeigt den Code, der zum Kopieren einer WMV-Datei erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="6511e-185">This sample shows the code necessary to copy a WMV file.</span></span> <span data-ttu-id="6511e-186">Es wird gezeigt, wie komprimierte Beispiele, Lese Header Attribute und Skripts gelesen und geschrieben und Header Attribute geändert werden.</span><span class="sxs-lookup"><span data-stu-id="6511e-186">It shows how to read and write compressed samples, read header attributes and scripts, and modify header attributes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6511e-187">Wmvnetwrite</span><span class="sxs-lookup"><span data-stu-id="6511e-187">WMVNetWrite</span></span></td>
<td><span data-ttu-id="6511e-188">Diese Konsolenanwendung zeigt, wie eine Windows Media-Datei über das Internet gestreamt wird.</span><span class="sxs-lookup"><span data-stu-id="6511e-188">This console application shows how a Windows Media file is streamed across the Internet.</span></span> <span data-ttu-id="6511e-189">Für das Beispiel muss ein Port angegeben werden, und anschließend kann die Datei mit einem Player abgespielt werden.</span><span class="sxs-lookup"><span data-stu-id="6511e-189">The sample requires a port to be specified, and then the file can be played using a player.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6511e-190">Wmvrecompress</span><span class="sxs-lookup"><span data-stu-id="6511e-190">WMVRecompress</span></span></td>
<td><span data-ttu-id="6511e-191">Diese Konsolenanwendung zeigt, wie eine WMV-Datei erneut komprimiert wird.</span><span class="sxs-lookup"><span data-stu-id="6511e-191">This console application shows how to recompress a WMV file.</span></span> <span data-ttu-id="6511e-192">Es veranschaulicht das Lesen von nicht komprimierten Beispielen, das Schreiben von nicht komprimierten Beispielen und das Durchlaufen von Multipass-Codierung, multikanalausgabe und intelligenter Neukomprimierung.</span><span class="sxs-lookup"><span data-stu-id="6511e-192">It demonstrates reading uncompressed samples, writing uncompressed samples, and doing multi-pass encoding, multi-channel output, and smart recompression.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="6511e-193">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6511e-193">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6511e-194">**Informationen zum Windows Media-Format-SDK**</span><span class="sxs-lookup"><span data-stu-id="6511e-194">**About the Windows Media Format SDK**</span></span>](about-the-windows-media-format-sdk.md)
</dt> <dt>

[<span data-ttu-id="6511e-195">**Programmierhandbuch**</span><span class="sxs-lookup"><span data-stu-id="6511e-195">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 





