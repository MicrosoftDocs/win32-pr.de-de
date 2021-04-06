---
title: Neuerungen in Windows Media Player 12
description: In diesem Thema sind die neuen Features von Windows Media Player 12 aufgeführt.
ms.assetid: 17f76963-c96d-46c9-82c0-3ed2d8a4e892
keywords:
- Windows Media Player, Neuerungen
- Windows Media Player, neue Features
- Software Development Kit (SDK), Windows Media Player 12
- SDK (Software Development Kit), Windows Media Player 12
- Dokumentation, Windows Media Player 12 SDK
- Neuerungen, Windows Media Player 12
- neue Features, Windows Media Player 12
- Schnittstellen, neue Features in Windows Media Player 12
- Attribute, neue Features in Windows Media Player 12
- Metadaten, neue Features in Windows Media Player 12
- Enumerationen, neue Features in Windows Media Player 12
- Flags, neue Features in Windows Media Player 12
- Schnittstellen, veraltet in Windows Media Player 12
- Methoden, veraltet in Windows Media Player 11 und nicht 12
- Versionen von Windows Media Player, neue Features in Version 12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16b21077df1f4a9c11edbfa20032ed473f872a0
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2020
ms.locfileid: "104101371"
---
# <a name="whats-new-in-windows-media-player-12"></a><span data-ttu-id="adf6d-118">Neuerungen in Windows Media Player 12</span><span class="sxs-lookup"><span data-stu-id="adf6d-118">What's New in Windows Media Player 12</span></span>

<span data-ttu-id="adf6d-119">In diesem Thema sind die neuen Features von Windows Media Player 12 aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="adf6d-119">This topic lists features that are new in Windows Media Player 12.</span></span>

## <a name="new-interfaces"></a><span data-ttu-id="adf6d-120">Neue Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="adf6d-120">New Interfaces</span></span>

-   [<span data-ttu-id="adf6d-121">**Iwmpaudiorenderconfig**</span><span class="sxs-lookup"><span data-stu-id="adf6d-121">**IWMPAudioRenderConfig**</span></span>](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpaudiorenderconfig)
-   [<span data-ttu-id="adf6d-122">**IWMPEvents4**</span><span class="sxs-lookup"><span data-stu-id="adf6d-122">**IWMPEvents4**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
-   [<span data-ttu-id="adf6d-123">**IWMPLibrary2**</span><span class="sxs-lookup"><span data-stu-id="adf6d-123">**IWMPLibrary2**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary2)
-   [<span data-ttu-id="adf6d-124">**IWMPSyncDevice3**</span><span class="sxs-lookup"><span data-stu-id="adf6d-124">**IWMPSyncDevice3**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice3)

## <a name="new-attributes"></a><span data-ttu-id="adf6d-125">Neue Attribute</span><span class="sxs-lookup"><span data-stu-id="adf6d-125">New Attributes</span></span>

<span data-ttu-id="adf6d-126">Die folgenden neuen Attribute für Medienelemente sind über die [**iwmpmedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) -und [**IWMPMedia3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia3) -Schnittstellen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="adf6d-126">The following new attributes for media items are available through the [**IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) and [**IWMPMedia3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia3) interfaces.</span></span>

-   [<span data-ttu-id="adf6d-127">**Albumcoverurl**</span><span class="sxs-lookup"><span data-stu-id="adf6d-127">**AlbumCoverURL**</span></span>](wm-albumcoverurl-attribute.md)
-   [<span data-ttu-id="adf6d-128">**Alternative ceurl**</span><span class="sxs-lookup"><span data-stu-id="adf6d-128">**AlternateSourceURL**</span></span>](alternatesourceurl-attribute.md)
-   [<span data-ttu-id="adf6d-129">**Dlnasourceuri**</span><span class="sxs-lookup"><span data-stu-id="adf6d-129">**DLNASourceURI**</span></span>](dlnasourceuri-attribute.md)
-   [<span data-ttu-id="adf6d-130">**Dlnaserverudn**</span><span class="sxs-lookup"><span data-stu-id="adf6d-130">**DLNAServerUDN**</span></span>](dlnaserverudn-attribute.md)
-   [<span data-ttu-id="adf6d-131">**Dtcpiphost**</span><span class="sxs-lookup"><span data-stu-id="adf6d-131">**DTCPIPHost**</span></span>](dtcpiphost-attribute.md)
-   [<span data-ttu-id="adf6d-132">**Dtcpipport**</span><span class="sxs-lookup"><span data-stu-id="adf6d-132">**DTCPIPPort**</span></span>](dtcpipport-attribute.md)
-   [<span data-ttu-id="adf6d-133">**LIBRARYID**</span><span class="sxs-lookup"><span data-stu-id="adf6d-133">**LibraryID**</span></span>](libraryid-attribute.md)
-   [<span data-ttu-id="adf6d-134">**LibraryName**</span><span class="sxs-lookup"><span data-stu-id="adf6d-134">**LibraryName**</span></span>](libraryname-attribute.md)

## <a name="new-device-metadata"></a><span data-ttu-id="adf6d-135">Neue Geräte Metadaten</span><span class="sxs-lookup"><span data-stu-id="adf6d-135">New Device Metadata</span></span>

<span data-ttu-id="adf6d-136">Die folgenden neuen gerätemetadatenelemente können durch Aufrufen von [**iwmpsyncdevice:: getiteminfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-getiteminfo)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="adf6d-136">The following new device metadata items can be retrieved by calling [**IWMPSyncDevice::getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-getiteminfo).</span></span>

-   <span data-ttu-id="adf6d-137">**Backgroundsyncstate**</span><span class="sxs-lookup"><span data-stu-id="adf6d-137">**BackgroundSyncState**</span></span>
-   <span data-ttu-id="adf6d-138">**Skippedfiles**</span><span class="sxs-lookup"><span data-stu-id="adf6d-138">**SkippedFiles**</span></span>
-   <span data-ttu-id="adf6d-139">**SyncFilter**</span><span class="sxs-lookup"><span data-stu-id="adf6d-139">**SyncFilter**</span></span>

<span data-ttu-id="adf6d-140">Die folgenden neuen gerätemetadatenelemente können durch Aufrufen von [**IWMPSyncDevice2:: setiteminfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo)festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="adf6d-140">The following new device metadata items can be set by calling [**IWMPSyncDevice2::setItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo).</span></span>

-   <span data-ttu-id="adf6d-141">**Autosyncdefaultrules**</span><span class="sxs-lookup"><span data-stu-id="adf6d-141">**AutoSyncDefaultRules**</span></span>
-   <span data-ttu-id="adf6d-142">**Backgroundsyncstate**</span><span class="sxs-lookup"><span data-stu-id="adf6d-142">**BackgroundSyncState**</span></span>
-   <span data-ttu-id="adf6d-143">**Includeskippedfiles**</span><span class="sxs-lookup"><span data-stu-id="adf6d-143">**IncludeSkippedFiles**</span></span>
-   <span data-ttu-id="adf6d-144">**SyncFilter**</span><span class="sxs-lookup"><span data-stu-id="adf6d-144">**SyncFilter**</span></span>
-   <span data-ttu-id="adf6d-145">**Synchronisierungs Verbindung**</span><span class="sxs-lookup"><span data-stu-id="adf6d-145">**SyncOnConnect**</span></span>

## <a name="new-enumeration-member"></a><span data-ttu-id="adf6d-146">Neuer Enumerationsmember</span><span class="sxs-lookup"><span data-stu-id="adf6d-146">New Enumeration Member</span></span>

<span data-ttu-id="adf6d-147">Die [**wmpsyncstate**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpsyncstate) -Enumeration weist den folgenden neuen Member auf.</span><span class="sxs-lookup"><span data-stu-id="adf6d-147">The [**WMPSyncState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpsyncstate) enumeration has the following new member.</span></span>

-   <span data-ttu-id="adf6d-148">**wmpssestimating**</span><span class="sxs-lookup"><span data-stu-id="adf6d-148">**wmpssEstimating**</span></span>

## <a name="new-flag"></a><span data-ttu-id="adf6d-149">Neues Flag</span><span class="sxs-lookup"><span data-stu-id="adf6d-149">New Flag</span></span>

<span data-ttu-id="adf6d-150">Die [**iwmpgraphcreation:: getgraphkreationflags**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-getgraphcreationflags) -Methode unterstützt das folgende neue Flag.</span><span class="sxs-lookup"><span data-stu-id="adf6d-150">The [**IWMPGraphCreation::GetGraphCreationFlags**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-getgraphcreationflags) method supports the following new flag.</span></span>

-   <span data-ttu-id="adf6d-151">**wmpgc- \_ Flags \_ verwenden \_ benutzerdefiniertes \_ Diagramm**</span><span class="sxs-lookup"><span data-stu-id="adf6d-151">**WMPGC\_FLAGS\_USE\_CUSTOM\_GRAPH**</span></span>

## <a name="deprecated-interface"></a><span data-ttu-id="adf6d-152">Veraltete Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="adf6d-152">Deprecated Interface</span></span>

<span data-ttu-id="adf6d-153">Die folgende Schnittstelle ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="adf6d-153">The following interface is deprecated.</span></span>

-   [<span data-ttu-id="adf6d-154">**Iwmpfoldermonitorservices**</span><span class="sxs-lookup"><span data-stu-id="adf6d-154">**IWMPFolderMonitorServices**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)

## <a name="methods-that-are-no-longer-deprecated"></a><span data-ttu-id="adf6d-155">Methoden, die nicht mehr als veraltet eingestuft werden</span><span class="sxs-lookup"><span data-stu-id="adf6d-155">Methods That Are No Longer Deprecated</span></span>

<span data-ttu-id="adf6d-156">Die folgenden Methoden wurden im Windows Media Player 11 SDK als veraltet markiert, sind jedoch nicht mehr als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="adf6d-156">The following methods were deprecated in Windows Media Player 11 SDK, but are no longer deprecated.</span></span>

-   [<span data-ttu-id="adf6d-157">**Iwmpgraphcreation:: graphkreationprerender**</span><span class="sxs-lookup"><span data-stu-id="adf6d-157">**IWMPGraphCreation::GraphCreationPreRender**</span></span>](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-graphcreationprerender)
-   [<span data-ttu-id="adf6d-158">**Iwmpgraphcreation:: graphkreationpostranender**</span><span class="sxs-lookup"><span data-stu-id="adf6d-158">**IWMPGraphCreation::GraphCreationPostRender**</span></span>](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-graphcreationpostrender)

## <a name="related-topics"></a><span data-ttu-id="adf6d-159">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="adf6d-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="adf6d-160">Informationen zum Windows Media Player SDK</span><span class="sxs-lookup"><span data-stu-id="adf6d-160">About the Windows Media Player SDK</span></span>](about-the-windows-media-player-sdk.md)
</dt> </dl>

 

 




