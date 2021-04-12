---
title: Windows Media Player Bits-Auftrags Konvention
description: Windows Media Player können digitale Medienelemente automatisch herunterladen und der Bibliothek hinzufügen, wenn Sie Background Intelligent Transfer Service (Bits) verwenden.
ms.assetid: 643faba7-9af2-4292-8d92-e321d7690a5b
keywords:
- Windows Media Player Online Stores, Background Intelligent Transfer Service (Bits)
- Online Stores, Background Intelligent Transfer Service (Bits)
- Typ 2 Online Stores, Background Intelligent Transfer Service (Bits)
- Intelligenter Hintergrundübertragungsdienst (Background Intelligent Transfer Service, BITS)
- Bits (Background Intelligent Transfer Service)
- Windows Media Player Online Stores, Bits-Auftrags Konvention
- Online Stores, Bits-Auftrags Konvention
- Typ 2 Online Stores, Bits-Auftrags Konvention
- Bits-Auftrags Konvention
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85278593ce151f46370ca491ccac8e1645f9bb70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104209321"
---
# <a name="windows-media-player-bits-job-convention"></a><span data-ttu-id="74c95-112">Windows Media Player Bits-Auftrags Konvention</span><span class="sxs-lookup"><span data-stu-id="74c95-112">Windows Media Player BITS Job Convention</span></span>

<span data-ttu-id="74c95-113">Windows Media Player können digitale Medienelemente automatisch herunterladen und der Bibliothek hinzufügen, wenn Sie [Background Intelligent Transfer Service (Bits)](/windows/desktop/Bits/background-intelligent-transfer-service-portal)verwenden.</span><span class="sxs-lookup"><span data-stu-id="74c95-113">Windows Media Player can automatically download and add digital media items to the library if you use [Background Intelligent Transfer Service (BITS)](/windows/desktop/Bits/background-intelligent-transfer-service-portal).</span></span> <span data-ttu-id="74c95-114">Um dieses Feature nutzen zu können, müssen Sie den Auftrag der Bits-Übertragungs Warteschlange hinzufügen und **ibackgroundcopyjob:: setDescription** aufrufen, indem Sie eine Beschreibungs Zeichenfolge mit dem richtigen Format angeben.</span><span class="sxs-lookup"><span data-stu-id="74c95-114">To take advantage of this feature, you must add your job to the BITS transfer queue and call **IBackgroundCopyJob::SetDescription**, providing a description string that uses the correct format.</span></span>

> [!Note]  
> <span data-ttu-id="74c95-115">In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores</span><span class="sxs-lookup"><span data-stu-id="74c95-115">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="74c95-116">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="74c95-116">Use of this functionality outside the context of an online store is not supported.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="74c95-117">Syntax</span><span class="sxs-lookup"><span data-stu-id="74c95-117">Syntax</span></span>

``` syntax
::WMP_JOB:1:serviceId:Provider:AlbumArtist:AlbumTitle:TrackNumber:Title:Duration:Rating
```

## <a name="parameters"></a><span data-ttu-id="74c95-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="74c95-118">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74c95-119"><span id="serviceId"></span><span id="serviceid"></span><span id="SERVICEID"></span>*serviceId*</span><span class="sxs-lookup"><span data-stu-id="74c95-119"><span id="serviceId"></span><span id="serviceid"></span><span id="SERVICEID"></span>*serviceId*</span></span>
</dt> <dd>

<span data-ttu-id="74c95-120">Ein zufällig generierter 32-Bit-Wert, der von Windows Media Player verwendet wird, um den Dienst zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="74c95-120">A randomly generated 32-bit value that Windows Media Player uses to identify the service.</span></span>

</dd> <dt>

<span data-ttu-id="74c95-121"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>*Ab*</span><span class="sxs-lookup"><span data-stu-id="74c95-121"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>*Provider*</span></span>
</dt> <dd>

<span data-ttu-id="74c95-122">Der Anbietername.</span><span class="sxs-lookup"><span data-stu-id="74c95-122">The provider name.</span></span> <span data-ttu-id="74c95-123">Dieser Wert muss mit einem gültigen Namen für den Onlinespeicher Schlüssel identisch sein.</span><span class="sxs-lookup"><span data-stu-id="74c95-123">This value must match a valid online store key name.</span></span>

</dd> <dt>

<span data-ttu-id="74c95-124"><span id="AlbumArtist"></span><span id="albumartist"></span><span id="ALBUMARTIST"></span>*Albumartist*</span><span class="sxs-lookup"><span data-stu-id="74c95-124"><span id="AlbumArtist"></span><span id="albumartist"></span><span id="ALBUMARTIST"></span>*AlbumArtist*</span></span>
</dt> <dd>

<span data-ttu-id="74c95-125">Der Name des primären Künstlers für das Album.</span><span class="sxs-lookup"><span data-stu-id="74c95-125">The name of the primary artist for the album.</span></span>

</dd> <dt>

<span data-ttu-id="74c95-126"><span id="AlbumTitle"></span><span id="albumtitle"></span><span id="ALBUMTITLE"></span>*Albumtitle*</span><span class="sxs-lookup"><span data-stu-id="74c95-126"><span id="AlbumTitle"></span><span id="albumtitle"></span><span id="ALBUMTITLE"></span>*AlbumTitle*</span></span>
</dt> <dd>

<span data-ttu-id="74c95-127">Der Titel des Albums.</span><span class="sxs-lookup"><span data-stu-id="74c95-127">The title of the album.</span></span>

</dd> <dt>

<span data-ttu-id="74c95-128"><span id="TrackNumber"></span><span id="tracknumber"></span><span id="TRACKNUMBER"></span>*Tracknumber*</span><span class="sxs-lookup"><span data-stu-id="74c95-128"><span id="TrackNumber"></span><span id="tracknumber"></span><span id="TRACKNUMBER"></span>*TrackNumber*</span></span>
</dt> <dd>

<span data-ttu-id="74c95-129">Die CD-Nachverfolgung.</span><span class="sxs-lookup"><span data-stu-id="74c95-129">The CD track number.</span></span>

</dd> <dt>

<span data-ttu-id="74c95-130"><span id="Title"></span><span id="title"></span><span id="TITLE"></span>*Tel*</span><span class="sxs-lookup"><span data-stu-id="74c95-130"><span id="Title"></span><span id="title"></span><span id="TITLE"></span>*Title*</span></span>
</dt> <dd>

<span data-ttu-id="74c95-131">Der Titel des Inhalts.</span><span class="sxs-lookup"><span data-stu-id="74c95-131">The title of the content.</span></span>

</dd> <dt>

<span data-ttu-id="74c95-132"><span id="Duration"></span><span id="duration"></span><span id="DURATION"></span>*Auf*</span><span class="sxs-lookup"><span data-stu-id="74c95-132"><span id="Duration"></span><span id="duration"></span><span id="DURATION"></span>*Duration*</span></span>
</dt> <dd>

<span data-ttu-id="74c95-133">Die Dauer des Inhalts.</span><span class="sxs-lookup"><span data-stu-id="74c95-133">The duration of the content.</span></span>

</dd> <dt>

<span data-ttu-id="74c95-134"><span id="Rating"></span><span id="rating"></span><span id="RATING"></span>*Leistung*</span><span class="sxs-lookup"><span data-stu-id="74c95-134"><span id="Rating"></span><span id="rating"></span><span id="RATING"></span>*Rating*</span></span>
</dt> <dd>

<span data-ttu-id="74c95-135">Die Bewertung für den Inhalt.</span><span class="sxs-lookup"><span data-stu-id="74c95-135">The rating for the content.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="74c95-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="74c95-136">Remarks</span></span>

<span data-ttu-id="74c95-137">Wenn Windows Media Player 10 oder höher Bits zum Herunterladen von Inhalten verwendet, listet es die Aufträge in der Übertragungs Warteschlange auf und überprüft die Beschreibungs Zeichenfolge für jeden Auftrag.</span><span class="sxs-lookup"><span data-stu-id="74c95-137">When Windows Media Player 10 or later uses BITS to download content, it enumerates the jobs in the transfer queue and inspects the description string for each job.</span></span> <span data-ttu-id="74c95-138">Wenn die Beschreibungs Zeichenfolge mit der erwarteten Konvention übereinstimmt, lädt Windows Media Player den Inhalt herunter.</span><span class="sxs-lookup"><span data-stu-id="74c95-138">If the description string matches the expected convention, Windows Media Player downloads the content.</span></span>

<span data-ttu-id="74c95-139">Sie müssen für jeden Bits-Auftrag nur eine digitale Mediendatei hinzufügen, die heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="74c95-139">You must add only one digital media file for download to each BITS job.</span></span>

<span data-ttu-id="74c95-140">Nachdem Sie einen BITS-Auftrag mithilfe dieser Konvention gestartet haben, müssen Sie Windows Media Player den Auftrag Fertigstellen lassen.</span><span class="sxs-lookup"><span data-stu-id="74c95-140">After you start a BITS job using this convention, you must let Windows Media Player complete the job.</span></span> <span data-ttu-id="74c95-141">Windows Media Player entfernt auch den Auftrag aus der Bits-Warteschlange, verschiebt die heruntergeladene Datei an den Speicherort, an dem die aufgeladene Musik gespeichert wird, und fügt die heruntergeladene Datei der Bibliothek hinzu.</span><span class="sxs-lookup"><span data-stu-id="74c95-141">Windows Media Player will also remove the job from the BITS queue, move the downloaded file to the location where ripped music is saved, and add the downloaded file to the library.</span></span>

<span data-ttu-id="74c95-142">Der *serviceid-* Parameter muss einen 32-Bit-Wert ungleich 0 (null) enthalten.</span><span class="sxs-lookup"><span data-stu-id="74c95-142">The *serviceId* parameter must contain a nonzero 32-bit value.</span></span> <span data-ttu-id="74c95-143">Es wird empfohlen, dass Sie die Funktion " [**cryptgenrandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) " verwenden, um diesen Wert zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="74c95-143">We recommend that you use the function [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) to create this value.</span></span>

<span data-ttu-id="74c95-144">Der Dateiname, den Sie mit dem *localname* -Parameter von **ibackgroundcopyjob:: AddFile** angeben, muss die Dateinamenerweiterung. WMA,. WMV,. MP3 oder. ASF aufweisen.</span><span class="sxs-lookup"><span data-stu-id="74c95-144">The file name you specify using the *localName* parameter of **IBackgroundCopyJob::AddFile** must have a .wma, .wmv, .mp3, or .asf file name extension.</span></span>

<span data-ttu-id="74c95-145">Die übrigen Parameter sind so konzipiert, dass Sie Metadatenwerte enthalten, die sich auf den Inhalt beziehen</span><span class="sxs-lookup"><span data-stu-id="74c95-145">The remaining parameters are designed to contain metadata values related to the content.</span></span> <span data-ttu-id="74c95-146">Sie können diese Werte von der Webseite für den Online Shop abrufen, indem Sie die Datei " **Downloader. getiteminfo**" verwenden.</span><span class="sxs-lookup"><span data-stu-id="74c95-146">You can retrieve these values from your online store webpage by using **DownloadItem.getItemInfo**.</span></span> <span data-ttu-id="74c95-147">Sie können die korrekte Download Auflistung abrufen, indem Sie **Downloadmanager. getdownloadcollection** aufrufen und *serviceid* als *CollectionId* -Parameter bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="74c95-147">You can retrieve the correct download collection by calling **DownloadManager.getDownloadCollection** and providing *serviceId* as the *collectionId* parameter.</span></span>

<span data-ttu-id="74c95-148">Windows Media Player überprüft die Bits-Warteschlange in regelmäßigen Abständen, während der Spieler ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="74c95-148">Windows Media Player inspects the BITS queue periodically while the Player is running.</span></span> <span data-ttu-id="74c95-149">Um sicherzustellen, dass Windows Media Player die Bits-Warteschlange auf Download Aufträge überprüft, sollten Sie einen Wert im folgenden Registrierungs Unterschlüssel erstellen:</span><span class="sxs-lookup"><span data-stu-id="74c95-149">To ensure that Windows Media Player checks the BITS queue for download jobs, you should create a value in the following registry subkey:</span></span>

<span data-ttu-id="74c95-150">**HKEY \_ Current \_ User \\ Software \\ Microsoft \\ Media Player \\ Services**</span><span class="sxs-lookup"><span data-stu-id="74c95-150">**HKEY\_CURRENT\_USER\\Software\\Microsoft\\MediaPlayer\\Services**</span></span>

<span data-ttu-id="74c95-151">Der Wert sollte wie folgt erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="74c95-151">The value should be created as follows.</span></span>



| <span data-ttu-id="74c95-152">Name</span><span class="sxs-lookup"><span data-stu-id="74c95-152">Name</span></span>                | <span data-ttu-id="74c95-153">type</span><span class="sxs-lookup"><span data-stu-id="74c95-153">Type</span></span>      | <span data-ttu-id="74c95-154">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="74c95-154">Description</span></span>                                                                                                                                                                                                          |
|---------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74c95-155">**Aktuerfrischendes Download**</span><span class="sxs-lookup"><span data-stu-id="74c95-155">**RefreshDownload**</span></span> | <span data-ttu-id="74c95-156">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="74c95-156">**DWORD**</span></span> | <span data-ttu-id="74c95-157">Gibt an, ob Windows Media Player die Bits-Warteschlange auf Download Aufträge prüfen soll.</span><span class="sxs-lookup"><span data-stu-id="74c95-157">Specifies whether Windows Media Player should inspect the BITS queue for download jobs.</span></span> <span data-ttu-id="74c95-158">Wenn der Wert 0 (null) ist, wird der Spieler die Bits-Warteschlange nicht untersuchen.</span><span class="sxs-lookup"><span data-stu-id="74c95-158">If the value is zero, the Player will not inspect the BITS queue.</span></span> <span data-ttu-id="74c95-159">Der Player muss die Warteschlange untersuchen, wenn der Wert ungleich 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="74c95-159">The Player must inspect the queue if the value is nonzero.</span></span> |



 

<span data-ttu-id="74c95-160">Mit der folgenden alternativen Syntax können Sie BITS-Aufträge hinzufügen, die von Windows Media Player nicht ausgeführt werden, für die jedoch lediglich Statusinformationen angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="74c95-160">You can use the following alternate syntax to add BITS jobs that Windows Media Player does not complete, but for which it simply shows status information:</span></span>

``` syntax
::WMP_STATUS:1:serviceId:Provider:AlbumArtist:AlbumTitle:TrackNumber:Title:Duration:Rating
```

<span data-ttu-id="74c95-161">Wenn Sie die obige Syntax verwenden, müssen Sie Code schreiben, um den Bits-Download abzuschließen, den Inhalt auf dem Computer des Benutzers zu organisieren und den Inhalt bei Bedarf der Bibliothek hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="74c95-161">When you use the preceding syntax, you must write code to complete the BITS download, organize the content on the user's computer, and add the content to the library, if desired.</span></span>

## <a name="related-topics"></a><span data-ttu-id="74c95-162">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="74c95-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74c95-163">Cryptgenrandom verwendet</span><span class="sxs-lookup"><span data-stu-id="74c95-163">CryptGenRandom</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom)
</dt> <dt>

[<span data-ttu-id="74c95-164">**Download Element. getiteminfo**</span><span class="sxs-lookup"><span data-stu-id="74c95-164">**DownloadItem.getItemInfo**</span></span>](downloaditem-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="74c95-165">**Download Manager. getdownloadcollection**</span><span class="sxs-lookup"><span data-stu-id="74c95-165">**DownloadManager.getDownloadCollection**</span></span>](downloadmanager-getdownloadcollection.md)
</dt> <dt>

[<span data-ttu-id="74c95-166">**Referenz für Typ 2-Onlineshops**</span><span class="sxs-lookup"><span data-stu-id="74c95-166">**Reference for Type 2 Online Stores**</span></span>](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 