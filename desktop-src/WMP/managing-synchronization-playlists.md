---
title: Synchronisierungs Wiedergabelisten
description: Synchronisierungs Wiedergabelisten
ms.assetid: 5891ada0-37a6-4256-9885-8aa9dbe98b7c
keywords:
- Windows Media Player, portable Geräte
- Windows Media Player-Objektmodell, portable Geräte
- Objektmodell, portable Geräte
- Windows Media Player ActiveX-Steuerelement, portable Geräte
- ActiveX-Steuerelement, portable Geräte
- Windows Media Player Mobile ActiveX-Steuerelement, portable Geräte
- Windows Media Player Mobile, tragbare Geräte
- Portable Geräte, Verwalten von Synchronisierungs Wiedergabelisten
- Geräte Synchronisierung, Wiedergabelisten
- Synchronisieren von Geräten, Wiedergabelisten
- Windows Media Player, Synchronisierungs Wiedergabelisten
- Windows Media Player-Objektmodell, Synchronisierungs Wiedergabelisten
- Objektmodell, Synchronisierungs Wiedergabelisten
- Windows Media Player Mobile, Synchronisierungs Wiedergabelisten
- Windows Media Player ActiveX-Steuerelement, Synchronisierungs Wiedergabelisten
- Windows Media Player Mobile ActiveX-Steuerelement, Synchronisierungs Wiedergabelisten
- ActiveX-Steuerung, Synchronisierungs Wiedergabelisten
- Wiedergabelisten, Synchronisierung
- Metadatei-Wiedergabelisten, Synchronisierung
- Windows Media Metadatei-Wiedergabelisten, Synchronisierung
- Synchronisierungs Wiedergabelisten, verwalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be0fe084918c0b69b827dbb941388246cbd177ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337189"
---
# <a name="managing-synchronization-playlists"></a><span data-ttu-id="51824-124">Synchronisierungs Wiedergabelisten</span><span class="sxs-lookup"><span data-stu-id="51824-124">Managing Synchronization Playlists</span></span>

<span data-ttu-id="51824-125">Windows Media Player 10 oder höher verwendet Wiedergabelisten, um digitale Mediendateien mit tragbaren Geräten zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="51824-125">Windows Media Player 10 or later uses playlists to synchronize digital media files with portable devices.</span></span> <span data-ttu-id="51824-126">In diesem Abschnitt wird erläutert, wie Synchronisierungs Wiedergabelisten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="51824-126">This section explains how to work with synchronization playlists.</span></span>

<span data-ttu-id="51824-127">Der Beispielcode in diesem Abschnitt verwendet zwei ListView-Steuerelemente, um Informationen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="51824-127">The example code in this section uses two ListView controls to display information.</span></span> <span data-ttu-id="51824-128">Das erste ListView-Steuerelement (IDC \_ plview) zeigt alle Wiedergabelisten in der Windows Media Player-Bibliothek an, wobei zuerst Synchronisierungs Wiedergabelisten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="51824-128">The first ListView control (IDC\_PLVIEW) displays all of the playlists in the Windows Media Player library, with synchronization playlists appearing first.</span></span> <span data-ttu-id="51824-129">Synchronisierungs Wiedergabelisten für das aktuell ausgewählte Gerät sind mit einem Häkchen gekennzeichnet und sind in der Reihenfolge der Synchronisierungs Priorität sortiert.</span><span class="sxs-lookup"><span data-stu-id="51824-129">Synchronization playlists for the currently selected device are marked with a check mark and are sorted in synchronization priority order.</span></span> <span data-ttu-id="51824-130">Alle anderen Wiedergabelisten werden deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="51824-130">All other playlists are unchecked.</span></span> <span data-ttu-id="51824-131">Das ListView-Steuerelement wurde für die einfache Auswahl konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="51824-131">The ListView control was configured for single selection.</span></span> <span data-ttu-id="51824-132">Die Reihenfolge der Wiedergabelisten im ListView-Steuerelement bestimmt Ihre Synchronisierungs Priorität.</span><span class="sxs-lookup"><span data-stu-id="51824-132">The order of playlists in the ListView control determines their synchronization priority.</span></span> <span data-ttu-id="51824-133">Der aktivierte Zustand einer einzelnen Wiedergabeliste bestimmt, ob es sich um eine Synchronisierungs Wiedergabeliste für das aktuell ausgewählte Gerät handelt.</span><span class="sxs-lookup"><span data-stu-id="51824-133">The checked state of an individual playlist determines whether it is a synchronization playlist for the currently selected device.</span></span>

<span data-ttu-id="51824-134">Das zweite ListView-Steuerelement (IDC \_ MediaView) zeigt die Medienelemente in der ausgewählten Wiedergabeliste an.</span><span class="sxs-lookup"><span data-stu-id="51824-134">The second ListView control (IDC\_MEDIAVIEW) displays the media items in the selected playlist.</span></span> <span data-ttu-id="51824-135">In zwei zusätzlichen Spalten wird Text angezeigt, der angibt, ob die digitale Mediendatei auf das Gerät kopiert wurde, und im Fall eines Fehlers, ob der Kopiervorgang fehlgeschlagen ist, da die digitale Mediendatei nicht passt.</span><span class="sxs-lookup"><span data-stu-id="51824-135">Two additional columns display text indicating whether the digital media file was copied to the device and, in the case of a failure, whether the copy failed because the digital media file did not fit.</span></span>

<span data-ttu-id="51824-136">Der folgende Beispielcode zeigt, wie die ListView-Steuerelemente initialisiert werden:</span><span class="sxs-lookup"><span data-stu-id="51824-136">The following example code shows how the ListView controls are initialized:</span></span>


```C++
STDMETHODIMP CSyncSettings::InitListView()
{
    m_hPlView = GetDlgItem(IDC_PLVIEW);
    m_hMediaView = GetDlgItem(IDC_MEDIAVIEW); 

    ATLASSERT(m_hPlView);
    ATLASSERT(m_hMediaView);

    // Sync playlist information.
    // Selection highlights all rows.
    // Show checkboxes.
    ListView_SetExtendedListViewStyleEx(m_hPlView, 0, LVS_EX_CHECKBOXES | LVS_EX_FULLROWSELECT);
   
    // Add headers.
    LVCOLUMN lvc;
    ZeroMemory(&lvc, sizeof(LVCOLUMN));
    lvc.mask = LVCF_WIDTH | LVCF_TEXT | LVCF_SUBITEM; 
    lvc.iSubItem = 0;
    
    lvc.pszText = _T("Sync");
    lvc.cx = 40;
    ListView_InsertColumn(m_hPlView, lvc.iSubItem, &lvc);

    lvc.iSubItem++;
    lvc.pszText = _T("Playlist Name");
    lvc.cx = 300;
    ListView_InsertColumn(m_hPlView, lvc.iSubItem, &lvc); 

    // Media information.
    // Selection highlights all rows.
    ListView_SetExtendedListViewStyleEx(m_hMediaView, 0, LVS_EX_FULLROWSELECT);

    // Add headers
    ZeroMemory(&lvc, sizeof(LVCOLUMN));
    lvc.mask = LVCF_WIDTH | LVCF_TEXT | LVCF_SUBITEM; 
    lvc.iSubItem = 0;
    
    lvc.pszText = _T("Media name");
    lvc.cx = 150;
    ListView_InsertColumn(m_hMediaView, lvc.iSubItem, &lvc);

    lvc.iSubItem++;
    lvc.pszText = _T("On Device");
    lvc.cx = 69;
    ListView_InsertColumn(m_hMediaView, lvc.iSubItem, &lvc);  

    lvc.iSubItem++;
    lvc.pszText = _T("Fit?");
    lvc.cx = 40;
    ListView_InsertColumn(m_hMediaView, lvc.iSubItem, &lvc);  
   
    return S_OK;
}
```



<span data-ttu-id="51824-137">Das folgende Array von Zeichen folgen enthält die Namen der Synchronisierungs Attribute, die in den Beispielen verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="51824-137">The following array of strings contains the names of the synchronization attributes used in the examples:</span></span>


```C++
static const TCHAR *g_szSyncAttributeNames[17] = {
        _T("Not used"), // Do not access this one.
        _T("Sync01"),
        _T("Sync02"),
        _T("Sync03"),
        _T("Sync04"),
        _T("Sync05"),
        _T("Sync06"),
        _T("Sync07"),
        _T("Sync08"),
        _T("Sync09"),
        _T("Sync10"),
        _T("Sync11"),
        _T("Sync12"),
        _T("Sync13"),
        _T("Sync14"),
        _T("Sync15"),
        _T("Sync16")};
```



<span data-ttu-id="51824-138">Die folgende Member-Variable enthält eine Wiedergabeliste, die alle Wiedergabelisten in der Windows Media Player-Bibliothek enthält.</span><span class="sxs-lookup"><span data-stu-id="51824-138">The following member variable contains a playlist containing all playlists in the Windows Media Player library.</span></span> <span data-ttu-id="51824-139">Jede Wiedergabeliste wird als Medien Element dargestellt.</span><span class="sxs-lookup"><span data-stu-id="51824-139">Each playlist is represented as a media item.</span></span>


```C++
CComPtr<IWMPPlaylist> m_spPlaylist;
```



<span data-ttu-id="51824-140">Die folgenden Abschnitte enthalten Beispielcode:</span><span class="sxs-lookup"><span data-stu-id="51824-140">The following sections provide example code:</span></span>

-   [<span data-ttu-id="51824-141">Auflisten von Synchronisierungs Wiedergabelisten</span><span class="sxs-lookup"><span data-stu-id="51824-141">Enumerating Synchronization Playlists</span></span>](enumerating-synchronization-playlists.md)
-   [<span data-ttu-id="51824-142">Sortieren von Wiedergabelisten nach Synchronisierungs Priorität</span><span class="sxs-lookup"><span data-stu-id="51824-142">Sorting Playlists by Synchronization Priority</span></span>](sorting-playlists-by-synchronization-priority.md)
-   [<span data-ttu-id="51824-143">Auflisten der Medienelemente</span><span class="sxs-lookup"><span data-stu-id="51824-143">Enumerating the Media Items</span></span>](enumerating-the-media-items.md)
-   [<span data-ttu-id="51824-144">Status der Wiedergabelisten Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="51824-144">Determining Playlist Synchronization State</span></span>](determining-playlist-synchronization-state.md)
-   [<span data-ttu-id="51824-145">Ändern der Synchronisierungs Priorität</span><span class="sxs-lookup"><span data-stu-id="51824-145">Changing Synchronization Priority</span></span>](changing-synchronization-priority.md)

## <a name="related-topics"></a><span data-ttu-id="51824-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="51824-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51824-147">**Arbeiten mit tragbaren Geräten**</span><span class="sxs-lookup"><span data-stu-id="51824-147">**Working with Portable Devices**</span></span>](working-with-portable-devices.md)
</dt> </dl>

 

 




