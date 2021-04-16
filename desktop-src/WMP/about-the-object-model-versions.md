---
title: Informationen zu Objektmodellversionen
description: Informationen zu Objektmodellversionen
ms.assetid: 20bb1681-9079-4f8c-bb5e-5c98e3bdc76a
keywords:
- Windows Media Player, Versionen
- Windows Media Player-Objektmodell, Versionen
- Objektmodell, Versionen
- Windows Media Player ActiveX-Steuerelement, Versionen für das Objektmodell
- ActiveX-Steuerelement, Versionen für das Objektmodell
- Windows Media Player Mobile ActiveX-Steuerelement, Versionen für das Objektmodell
- Windows Media Player Mobile, Versionen für das Objektmodell
- Versionen von Windows Media Player, Objektmodell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59886f5750b6fc42112f73d6bb6e05e8d013ffdc
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/21/2020
ms.locfileid: "104390045"
---
# <a name="about-the-object-model-versions"></a><span data-ttu-id="94fcd-111">Informationen zu Objektmodellversionen</span><span class="sxs-lookup"><span data-stu-id="94fcd-111">About the Object Model Versions</span></span>

<span data-ttu-id="94fcd-112">In Windows Media Player 7,0 wurde ein neues Objektmodell eingeführt.</span><span class="sxs-lookup"><span data-stu-id="94fcd-112">Windows Media Player 7.0 introduced a new object model.</span></span> <span data-ttu-id="94fcd-113">Dieses Objektmodell wurde mit Windows Media Player 7,1, Windows Media Player für Windows XP, Windows Media Player 9-Serie, Windows Media Player 10, Windows Media Player 11 und Windows Media Player 12 erweitert.</span><span class="sxs-lookup"><span data-stu-id="94fcd-113">This object model has been extended with Windows Media Player 7.1, Windows Media Player for Windows XP, Windows Media Player 9 Series, Windows Media Player 10, Windows Media Player 11, and Windows Media Player 12.</span></span> <span data-ttu-id="94fcd-114">Jedes Thema in der Objektmodell Referenz enthält einen Anforderungs Abschnitt, der die Mindestanforderungen für die jeweilige Eigenschaft, Methode oder das jeweilige Ereignis beschreibt.</span><span class="sxs-lookup"><span data-stu-id="94fcd-114">Each topic in the Object Model Reference includes a Requirements section that details the minimum requirement for the individual property, method, or event.</span></span> <span data-ttu-id="94fcd-115">In der folgenden Liste werden die neuen Objekte, Methoden, Eigenschaften und Ereignisse erläutert, die seit Version 7,0 für jede Version hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="94fcd-115">The following lists detail the new objects, methods, properties, and events that have been added for each version since version 7.0.</span></span> <span data-ttu-id="94fcd-116">Diese Listen enthalten auch neue C++-Schnittstellen, Methoden und Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="94fcd-116">These lists also include new C++ interfaces, methods, and events.</span></span>

<span data-ttu-id="94fcd-117">Wenn eine neue oder aktualisierte Schnittstelle auch als Objekt verfügbar gemacht wird, wird nur das Objekt aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="94fcd-117">Where a new or updated interface is also exposed as an object, only the object is listed.</span></span> <span data-ttu-id="94fcd-118">Informationen zum Auffinden der-Schnittstelle finden Sie in der [Objektmodell Referenz für C++](object-model-reference-for-c.md).</span><span class="sxs-lookup"><span data-stu-id="94fcd-118">To locate the interface, refer to the [Object Model Reference for C++](object-model-reference-for-c.md).</span></span> <span data-ttu-id="94fcd-119">Normalerweise müssen Sie dem Objektnamen lediglich das iwmp-Präfix hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="94fcd-119">Usually, you will simply need to add the IWMP prefix to the object name.</span></span> <span data-ttu-id="94fcd-120">Wenn eine neue Schnittstelle eine vorhandene erweitert, müssen Sie möglicherweise nach der aktuellen Versionsnummer suchen.</span><span class="sxs-lookup"><span data-stu-id="94fcd-120">If a new interface extends an existing one, you may need to look for the latest version number.</span></span> <span data-ttu-id="94fcd-121">Beispielsweise wurden in der Windows Media Player 9-Reihe neue Eigenschaften und Methoden eingeführt, die im [**Settings**](settings-object.md) -Objekt verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="94fcd-121">For example, Windows Media Player 9 Series introduced new properties and methods available from the [**Settings**](settings-object.md) object.</span></span> <span data-ttu-id="94fcd-122">In C++ sind diese über die [**IWMPSettings2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings2) -Schnittstelle verfügbar, die [**iwmpsettings**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings)erweitert.</span><span class="sxs-lookup"><span data-stu-id="94fcd-122">In C++, these are available through the [**IWMPSettings2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings2) interface, which extends [**IWMPSettings**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings).</span></span>

## <a name="added-for-windows-media-player-71"></a><span data-ttu-id="94fcd-123">Für Windows Media Player 7,1 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="94fcd-123">Added for Windows Media Player 7.1</span></span>

-   [<span data-ttu-id="94fcd-124">**Player. stretchdefit (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="94fcd-124">**Player.stretchToFit Property**</span></span>](player-stretchtofit.md)

## <a name="added-for-windows-media-player-for-windows-xp"></a><span data-ttu-id="94fcd-125">Für Windows-Media Player für Windows XP hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="94fcd-125">Added for Windows Media Player for Windows XP</span></span>

-   [<span data-ttu-id="94fcd-126">**Controls. Step-Methode**</span><span class="sxs-lookup"><span data-stu-id="94fcd-126">**Controls.step Method**</span></span>](controls-step.md)
-   [<span data-ttu-id="94fcd-127">**DVD-Objekt**</span><span class="sxs-lookup"><span data-stu-id="94fcd-127">**DVD Object**</span></span>](dvd-object.md)
-   [<span data-ttu-id="94fcd-128">**Media. Error (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="94fcd-128">**Media.error Property**</span></span>](media-error.md)
-   [<span data-ttu-id="94fcd-129">**Player. domainchange-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="94fcd-129">**Player.DomainChange Event**</span></span>](player-player-domainchange.md)
-   [<span data-ttu-id="94fcd-130">**Player. MediaError-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="94fcd-130">**Player.MediaError Event**</span></span>](player-player-mediaerror.md)
-   [<span data-ttu-id="94fcd-131">**Player. openplaylistswitch-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="94fcd-131">**Player.OpenPlaylistSwitch Event**</span></span>](player-player-openplaylistswitch.md)
-   [<span data-ttu-id="94fcd-132">**Player. windowlessvideo (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="94fcd-132">**Player.windowlessVideo Property**</span></span>](player-windowlessvideo.md)

## <a name="added-for-windows-media-player-9-series"></a><span data-ttu-id="94fcd-133">Für Windows Media Player 9-Reihe hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="94fcd-133">Added for Windows Media Player 9 Series</span></span>

-   [<span data-ttu-id="94fcd-134">**Closedcaption. getsamilangid-Methode**</span><span class="sxs-lookup"><span data-stu-id="94fcd-134">**ClosedCaption.getSAMILangID Method**</span></span>](closedcaption-getsamilangid.md)
-   [<span data-ttu-id="94fcd-135">**Closedcaption. getsamilangname-Methode**</span><span class="sxs-lookup"><span data-stu-id="94fcd-135">**ClosedCaption.getSAMILangName Method**</span></span>](closedcaption-getsamilangname.md)
-   [<span data-ttu-id="94fcd-136">**Closedcaption. getsamistylename-Methode**</span><span class="sxs-lookup"><span data-stu-id="94fcd-136">**ClosedCaption.getSAMIStyleName Method**</span></span>](closedcaption-getsamistylename.md)
-   [<span data-ttu-id="94fcd-137">**Closedcaption. samilangcount (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="94fcd-137">**ClosedCaption.SAMILangCount Property**</span></span>](closedcaption-samilangcount.md)
-   [<span data-ttu-id="94fcd-138">**Closedcaption. samistylecount (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="94fcd-138">**ClosedCaption.SAMIStyleCount Property**</span></span>](closedcaption-samistylecount.md)
-   [<span data-ttu-id="94fcd-139">**Controls. audiolanguagecount (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="94fcd-139">**Controls.audioLanguageCount Property**</span></span>](controls-audiolanguagecount.md)
-   [<span data-ttu-id="94fcd-140">**Controls. currentaudiolanguage (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="94fcd-140">**Controls.currentAudioLanguage Property**</span></span>](controls-currentaudiolanguage.md)
-   [<span data-ttu-id="94fcd-141">**Controls. currentaudiolanguageindex (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="94fcd-141">**Controls.currentAudioLanguageIndex Property**</span></span>](controls-currentaudiolanguageindex.md)
-   [<span data-ttu-id="94fcd-142">**Controls. currentPositionTimecode-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="94fcd-142">**Controls.currentPositionTimecode Property**</span></span>](controls-currentpositiontimecode.md)
-   [<span data-ttu-id="94fcd-143">**Controls. getaudiolanguagedescription-Methode**</span><span class="sxs-lookup"><span data-stu-id="94fcd-143">**Controls.getAudioLanguageDescription Method**</span></span>](controls-getaudiolanguagedescription.md)
-   [<span data-ttu-id="94fcd-144">**Controls. getaudiolanguageid-Methode**</span><span class="sxs-lookup"><span data-stu-id="94fcd-144">**Controls.getAudioLanguageID Method**</span></span>](controls-getaudiolanguageid.md)
-   [<span data-ttu-id="94fcd-145">**Controls. getlanguagename-Methode**</span><span class="sxs-lookup"><span data-stu-id="94fcd-145">**Controls.getLanguageName Method**</span></span>](controls-getlanguagename.md)
-   [<span data-ttu-id="94fcd-146">**ErrorItem. Condition (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="94fcd-146">**ErrorItem.condition Property**</span></span>](erroritem-condition.md)
-   [<span data-ttu-id="94fcd-147">**Extern. appcolorlight (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="94fcd-147">**External.appColorLight Property**</span></span>](external-appcolorlight.md)
-   [<span data-ttu-id="94fcd-148">**Externes. oncolorchange-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="94fcd-148">**External.OnColorChange Event**</span></span>](external-oncolorchange-event.md)
-   [<span data-ttu-id="94fcd-149">**Extern. Version (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="94fcd-149">**External.version Property**</span></span>](external-version.md)
-   [<span data-ttu-id="94fcd-150">**Iwmpevents::P layerdockedstatechange-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="94fcd-150">**IWMPEvents::PlayerDockedStateChange Event**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerdockedstatechange)
-   [<span data-ttu-id="94fcd-151">**Iwmpevents::P layerreconnect-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="94fcd-151">**IWMPEvents::PlayerReconnect Event**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerreconnect)
-   [<span data-ttu-id="94fcd-152">**Iwmpevents:: switchedto Control-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="94fcd-152">**IWMPEvents::SwitchedToControl Event**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtocontrol)
-   [<span data-ttu-id="94fcd-153">**Iwmpevents:: switchedtoplayerapplication-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="94fcd-153">**IWMPEvents::SwitchedToPlayerApplication Event**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtoplayerapplication)
-   [<span data-ttu-id="94fcd-154">**Iwmpplayerservices-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="94fcd-154">**IWMPPlayerServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)
-   [<span data-ttu-id="94fcd-155">**Iwmpremotemediaservices-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="94fcd-155">**IWMPRemoteMediaServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)
-   [<span data-ttu-id="94fcd-156">**Iwmpskinmanager-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="94fcd-156">**IWMPSkinManager Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpskinmanager)
-   [<span data-ttu-id="94fcd-157">**Media. getattributezähltbytype-Methode**</span><span class="sxs-lookup"><span data-stu-id="94fcd-157">**Media.getAttributeCountByType Method**</span></span>](media-getattributecountbytype.md)
-   [<span data-ttu-id="94fcd-158">**Media. getItemInfoByType-Methode**</span><span class="sxs-lookup"><span data-stu-id="94fcd-158">**Media.getItemInfoByType Method**</span></span>](media-getiteminfobytype.md)
-   [<span data-ttu-id="94fcd-159">**MetadataPicture-Objekt**</span><span class="sxs-lookup"><span data-stu-id="94fcd-159">**MetadataPicture Object**</span></span>](metadatapicture-object.md)
-   [<span data-ttu-id="94fcd-160">**MetadataText-Objekt**</span><span class="sxs-lookup"><span data-stu-id="94fcd-160">**MetadataText Object**</span></span>](metadatatext-object.md)
-   [<span data-ttu-id="94fcd-161">**Player. audiolanguagechange-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="94fcd-161">**Player.AudioLanguageChange Event**</span></span>](player-player-audiolanguagechange.md)
-   [<span data-ttu-id="94fcd-162">**Player. IsRemote-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="94fcd-162">**Player.isRemote Property**</span></span>](player-isremote.md)
-   [<span data-ttu-id="94fcd-163">**Player. mediacollectionattributestringchanged-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="94fcd-163">**Player.MediaCollectionAttributeStringChanged Event**</span></span>](player-player-mediacollectionattributestringchanged.md)
-   [<span data-ttu-id="94fcd-164">**Player. newmedia-Methode**</span><span class="sxs-lookup"><span data-stu-id="94fcd-164">**Player.newMedia Method**</span></span>](player-newmedia.md)
-   [<span data-ttu-id="94fcd-165">**Player. newwiedergabe-Methode**</span><span class="sxs-lookup"><span data-stu-id="94fcd-165">**Player.newPlaylist Method**</span></span>](player-newplaylist.md)
-   [<span data-ttu-id="94fcd-166">**Player. openplayer-Methode**</span><span class="sxs-lookup"><span data-stu-id="94fcd-166">**Player.openPlayer Method**</span></span>](player-openplayer.md)
-   [<span data-ttu-id="94fcd-167">**Player. playerapplication (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="94fcd-167">**Player.playerApplication Property**</span></span>](player-playerapplication.md)
-   [<span data-ttu-id="94fcd-168">**Player. statusChange-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="94fcd-168">**Player.StatusChange Event**</span></span>](player-player-statuschange.md)
-   [<span data-ttu-id="94fcd-169">**Playerapplication-Objekt**</span><span class="sxs-lookup"><span data-stu-id="94fcd-169">**PlayerApplication Object**</span></span>](playerapplication-object.md)
-   [<span data-ttu-id="94fcd-170">**Settings. defaultaudiolanguage (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="94fcd-170">**Settings.defaultAudioLanguage Property**</span></span>](settings-defaultaudiolanguage.md)
-   [<span data-ttu-id="94fcd-171">**Settings. mediaaccessrights (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="94fcd-171">**Settings.mediaAccessRights Property**</span></span>](settings-mediaaccessrights.md)
-   [<span data-ttu-id="94fcd-172">**Settings. requestmediaaccessrights-Methode**</span><span class="sxs-lookup"><span data-stu-id="94fcd-172">**Settings.requestMediaAccessRights Method**</span></span>](settings-requestmediaaccessrights.md)

## <a name="added-for-windows-media-player-10"></a><span data-ttu-id="94fcd-173">Für Windows Media Player 10 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="94fcd-173">Added for Windows Media Player 10</span></span>

-   [<span data-ttu-id="94fcd-174">**Iwmpgraphcreation-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="94fcd-174">**IWMPGraphCreation Interface**</span></span>](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpgraphcreation)
-   [<span data-ttu-id="94fcd-175">**IWMPPlayerServices2-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="94fcd-175">**IWMPPlayerServices2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices2)
-   [<span data-ttu-id="94fcd-176">**Iwmpsyncdevice-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="94fcd-176">**IWMPSyncDevice Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
-   [<span data-ttu-id="94fcd-177">**Iwmpsyncservices-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="94fcd-177">**IWMPSyncServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)
-   [<span data-ttu-id="94fcd-178">**Wmpdevicestatus-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="94fcd-178">**WMPDeviceStatus Enumeration**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus)
-   [<span data-ttu-id="94fcd-179">**Wmpsyncstate-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="94fcd-179">**WMPSyncState Enumeration**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpsyncstate)

## <a name="added-for-windows-media-player-11"></a><span data-ttu-id="94fcd-180">Für Windows Media Player 11 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="94fcd-180">Added for Windows Media Player 11</span></span>

-   [<span data-ttu-id="94fcd-181">**Iwmpcdromburn-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="94fcd-181">**IWMPCdromBurn Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)
-   [<span data-ttu-id="94fcd-182">**Iwmpcdromburn-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="94fcd-182">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
-   [<span data-ttu-id="94fcd-183">**Iwmpcdromrip-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="94fcd-183">**IWMPCdromRip Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)
-   [<span data-ttu-id="94fcd-184">**Iwmpcdromrip-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="94fcd-184">**IWMPCdromRip Interface (VB and C#)**</span></span>](iwmpcdromrip--vb-and-c.md)
-   [<span data-ttu-id="94fcd-185">**IWMPEvents3-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="94fcd-185">**IWMPEvents3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)
-   [<span data-ttu-id="94fcd-186">**Iwmpfoldermonitorservices-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="94fcd-186">**IWMPFolderMonitorServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
-   [<span data-ttu-id="94fcd-187">**Iwmplibrary-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="94fcd-187">**IWMPLibrary Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)
-   [<span data-ttu-id="94fcd-188">**Iwmplibrary-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="94fcd-188">**IWMPLibrary Interface (VB and C#)**</span></span>](iwmplibrary--vb-and-c.md)
-   [<span data-ttu-id="94fcd-189">**Iwmplibraryservices-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="94fcd-189">**IWMPLibraryServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)
-   [<span data-ttu-id="94fcd-190">**Iwmplibraryservices-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="94fcd-190">**IWMPLibraryServices Interface (VB and C#)**</span></span>](iwmplibraryservices--vb-and-c.md)
-   [<span data-ttu-id="94fcd-191">**Iwmplibrarysharingservices-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="94fcd-191">**IWMPLibrarySharingServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrarysharingservices)
-   [<span data-ttu-id="94fcd-192">**IWMPMediaCollection2-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="94fcd-192">**IWMPMediaCollection2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2)
-   [<span data-ttu-id="94fcd-193">**IWMPMediaCollection2-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="94fcd-193">**IWMPMediaCollection2 Interface (VB and C#)**</span></span>](iwmpmediacollection2--vb-and-c.md)
-   [<span data-ttu-id="94fcd-194">**Iwmpquery-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="94fcd-194">**IWMPQuery Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)
-   [<span data-ttu-id="94fcd-195">**Iwmpquery-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="94fcd-195">**IWMPQuery Interface (VB and C#)**</span></span>](iwmpquery--vb-and-c.md)
-   [<span data-ttu-id="94fcd-196">**Iwmprenderconfig-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="94fcd-196">**IWMPRenderConfig Interface**</span></span>](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmprenderconfig)
-   [<span data-ttu-id="94fcd-197">**IWMPStringCollection2-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="94fcd-197">**IWMPStringCollection2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2)
-   [<span data-ttu-id="94fcd-198">**IWMPStringCollection2-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="94fcd-198">**IWMPStringCollection2 Interface (VB and C#)**</span></span>](iwmpstringcollection2--vb-and-c.md)
-   [<span data-ttu-id="94fcd-199">**IWMPSyncDevice2-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="94fcd-199">**IWMPSyncDevice2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice2)
-   [<span data-ttu-id="94fcd-200">**Iwmpvideorenderconfig-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="94fcd-200">**IWMPVideoRenderConfig Interface**</span></span>](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpvideorenderconfig)
-   [<span data-ttu-id="94fcd-201">**Query-Objekt**</span><span class="sxs-lookup"><span data-stu-id="94fcd-201">**Query Object**</span></span>](query-object.md)
-   [<span data-ttu-id="94fcd-202">**Wmpburnformat-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="94fcd-202">**WMPBurnFormat Enumeration**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnformat)
-   [<span data-ttu-id="94fcd-203">**Wmpburnstate-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="94fcd-203">**WMPBurnState Enumeration**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
-   [<span data-ttu-id="94fcd-204">**Wmplibrarytype-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="94fcd-204">**WMPLibraryType Enumeration**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
-   [<span data-ttu-id="94fcd-205">**Wmpripstate-Enumeration**</span><span class="sxs-lookup"><span data-stu-id="94fcd-205">**WMPRipState Enumeration**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate)

## <a name="added-for-windows-media-player-12"></a><span data-ttu-id="94fcd-206">Für Windows Media Player 12 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="94fcd-206">Added for Windows Media Player 12</span></span>

-   [<span data-ttu-id="94fcd-207">**Iwmpaudiorenderconfig-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="94fcd-207">**IWMPAudioRenderConfig Interface**</span></span>](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpaudiorenderconfig)
-   [<span data-ttu-id="94fcd-208">**IWMPEvents4-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="94fcd-208">**IWMPEvents4 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
-   [<span data-ttu-id="94fcd-209">**IWMPLibrary2-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="94fcd-209">**IWMPLibrary2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary2)
-   [<span data-ttu-id="94fcd-210">**IWMPSyncDevice3-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="94fcd-210">**IWMPSyncDevice3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice3)

## <a name="related-topics"></a><span data-ttu-id="94fcd-211">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="94fcd-211">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94fcd-212">**Informationen zum Player-Objektmodell**</span><span class="sxs-lookup"><span data-stu-id="94fcd-212">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> <dt>

[<span data-ttu-id="94fcd-213">**Objektmodell Referenz für die Skripterstellung**</span><span class="sxs-lookup"><span data-stu-id="94fcd-213">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




