---
title: Auflisten von Synchronisierungs Wiedergabelisten
description: Auflisten von Synchronisierungs Wiedergabelisten
ms.assetid: 830c3ea5-2937-48b5-b89f-ef68a6649ca3
keywords:
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
- Synchronisierungs Wiedergabelisten, auflisten
- Portable Geräte, auflisten
- Enumerationen, Synchronisierungs Wiedergabelisten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29679380cec1844e9a790ac4ff047bfa4bf05288
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106339043"
---
# <a name="enumerating-synchronization-playlists"></a><span data-ttu-id="1c217-116">Auflisten von Synchronisierungs Wiedergabelisten</span><span class="sxs-lookup"><span data-stu-id="1c217-116">Enumerating Synchronization Playlists</span></span>

<span data-ttu-id="1c217-117">Im folgenden Beispielcode wird eine Funktion erstellt, die ein ListView-Steuerelement mit Wiedergabelisten füllt.</span><span class="sxs-lookup"><span data-stu-id="1c217-117">The following example code creates a function that fills a ListView control with playlists.</span></span> <span data-ttu-id="1c217-118">Synchronisierungs Wiedergabelisten werden zuerst angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1c217-118">Synchronization playlists appear first.</span></span> <span data-ttu-id="1c217-119">Synchronisierungs Wiedergabelisten für das aktuell ausgewählte Gerät sind mit einem Häkchen gekennzeichnet und sind in der Reihenfolge der Synchronisierungs Priorität sortiert.</span><span class="sxs-lookup"><span data-stu-id="1c217-119">Synchronization playlists for the currently selected device are marked with a check mark and are sorted in synchronization priority order.</span></span> <span data-ttu-id="1c217-120">Alle anderen Wiedergabelisten werden deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="1c217-120">All other playlists are unchecked.</span></span>

<span data-ttu-id="1c217-121">Das ListView-Steuerelement wurde für die einfache Auswahl konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="1c217-121">The ListView control was configured for single selection.</span></span> <span data-ttu-id="1c217-122">Die Reihenfolge der Wiedergabelisten im ListView-Steuerelement bestimmt Ihre Synchronisierungs Priorität.</span><span class="sxs-lookup"><span data-stu-id="1c217-122">The order of playlists in the ListView control determines their synchronization priority.</span></span> <span data-ttu-id="1c217-123">Der aktivierte Zustand einer einzelnen Wiedergabeliste bestimmt, ob es sich um eine Synchronisierungs Wiedergabeliste für das aktuell ausgewählte Gerät handelt.</span><span class="sxs-lookup"><span data-stu-id="1c217-123">The checked state of an individual playlist determines whether it is a synchronization playlist for the currently selected device.</span></span>

<span data-ttu-id="1c217-124">Der Parameter *lpsindex* gibt den Partnerschafts Index für das aktuell ausgewählte portable Gerät an.</span><span class="sxs-lookup"><span data-stu-id="1c217-124">The parameter *lPSIndex* specifies the partnership index for the currently selected portable device.</span></span>


```C++
STDMETHODIMP CSyncSettings::ShowPlaylists(long lPSIndex)
{ 
    HRESULT hr = S_OK; 
    ATLASSERT(m_pMainDlg);
   
    CComPtr<IWMPMediaCollection> spMediaCollection;
    CComPtr<IWMPPlaylist> spPlaylist; // Contains a playlist of all playlists.
    long lSyncItemCount= 0; // Count of items selected for synchronization. 

    ListView_DeleteAllItems(m_hPlView);

    m_spPlaylist.Release();
   
    if(lPSIndex == 0)
    {
        return S_OK;
    } 

    HCURSOR hCursor = LoadCursor(NULL, IDC_WAIT);
    HCURSOR hCursorOld = SetCursor(hCursor);

    if(SUCCEEDED(hr))
    {
        // Retrieve a pointer to IWMPMediaCollection.
        hr = m_spPlayer->get_mediaCollection(&spMediaCollection);
    }

    if(SUCCEEDED(hr) && spMediaCollection)
    {
        // Retrieve a playlist filled with IWMPMedia items.
        // Each IWMPMedia represents an individual playlist 
        // in the library.
        hr = spMediaCollection->getByAttribute(CComBSTR("MediaType"), CComBSTR("playlist"), &spPlaylist);
    }
 
    if(SUCCEEDED(hr) && spPlaylist)
    {  
        // Get the sync attribute name for the current device.
        CComBSTR bstrAttribute(g_szSyncAttributeNames[lPSIndex]);

        // Sort the playlist.
        // lSyncItemCount is the count of synchronization playlists.
        hr = SortPlaylist(spPlaylist, bstrAttribute, &lSyncItemCount);
     
        if(SUCCEEDED(hr))
        {
            m_spPlaylist = spPlaylist;  // Cache the playlist.

            long lCount = 0;
            spPlaylist->get_count(&lCount);
             
            // Fill the ListView control.
            for(long i = 0; i < lCount; i++)
            {
                CComPtr<IWMPMedia> spMedia;
                CComBSTR bstrPlaylistName;
                CComBSTR bstrVal; // Value of the SyncXX attribute.

                // Retrieve a playlist.
                hr = spPlaylist->get_item(i, &spMedia);

                if(SUCCEEDED(hr) && spMedia)
                {
                    // Get the name.
                    hr = spMedia->get_name(&bstrPlaylistName);
                }  
                if(SUCCEEDED(hr) && spMedia)
                {      
                    // Get the SyncXX attribute value.
                    hr = spMedia->getItemInfo(bstrAttribute, &bstrVal);
                }

                if(SUCCEEDED(hr) && bstrPlaylistName.Length())
                {
                    // Insert the item in the ListView control.
                    LVITEM lvI;
                    ZeroMemory(&lvI, sizeof(LVITEM));
                    lvI.mask = LVIF_TEXT; 
                    lvI.lParam = _wtol(bstrVal);
                    lvI.iItem = ListView_GetItemCount(m_hPlView);
                    lvI.pszText = "";
                    ListView_InsertItem(m_hPlView, &lvI);

                    // If this is a sync playlist, mark the check box.
                    if(i < lSyncItemCount)
                    {
                        ListView_SetCheckState(m_hPlView, i, TRUE);
                    }

                    // Display the playlist name.
                    lvI.iSubItem = 1;
                    lvI.pszText = COLE2T(bstrPlaylistName);
                    ListView_SetItem(m_hPlView, &lvI);
                }
            }
        }        
    }

    SetCursor(hCursorOld);
    return hr;
}
```



<span data-ttu-id="1c217-125">Informationen zur Implementierung der sortwiedergabe-Funktion finden Sie unter [Sortieren von Wiedergabelisten nach Synchronisierungs Priorität](sorting-playlists-by-synchronization-priority.md).</span><span class="sxs-lookup"><span data-stu-id="1c217-125">For the implementation of the SortPlaylist function, see [Sorting Playlists by Synchronization Priority](sorting-playlists-by-synchronization-priority.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c217-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1c217-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c217-127">**Iwmpmedia:: getiteminfo**</span><span class="sxs-lookup"><span data-stu-id="1c217-127">**IWMPMedia::getItemInfo**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo)
</dt> <dt>

[<span data-ttu-id="1c217-128">**Iwmpmediacollection:: getbyattribute**</span><span class="sxs-lookup"><span data-stu-id="1c217-128">**IWMPMediaCollection::getByAttribute**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getbyattribute)
</dt> <dt>

[<span data-ttu-id="1c217-129">**Synchronisierungs Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="1c217-129">**Managing Synchronization Playlists**</span></span>](managing-synchronization-playlists.md)
</dt> <dt>

[<span data-ttu-id="1c217-130">**Synchronisierungs Attribute**</span><span class="sxs-lookup"><span data-stu-id="1c217-130">**Sync Attributes**</span></span>](sync-attributes.md)
</dt> </dl>

 

 




