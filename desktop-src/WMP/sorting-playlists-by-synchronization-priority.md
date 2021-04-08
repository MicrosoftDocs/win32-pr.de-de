---
title: Sortieren von Wiedergabelisten nach Synchronisierungs Priorität
description: Sortieren von Wiedergabelisten nach Synchronisierungs Priorität
ms.assetid: 0f7f1ed3-0639-47bf-bf8e-52ae0a1d7ab2
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
- Portable Geräte, Sortieren von Synchronisierungs Wiedergabelisten
- Synchronisierungs Wiedergabelisten, Sortieren
- Synchronisierungs Wiedergabelisten, Prioritäten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90624e8e1cab715e8a26e33f40a444d53ab35def
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103858019"
---
# <a name="sorting-playlists-by-synchronization-priority"></a><span data-ttu-id="19369-116">Sortieren von Wiedergabelisten nach Synchronisierungs Priorität</span><span class="sxs-lookup"><span data-stu-id="19369-116">Sorting Playlists by Synchronization Priority</span></span>

<span data-ttu-id="19369-117">Der folgende Code führt eine einfache Art von Wiedergabelisten aus.</span><span class="sxs-lookup"><span data-stu-id="19369-117">The following code performs a simple sort of playlists.</span></span> <span data-ttu-id="19369-118">Sie können sehen, wie diese Funktion im Beispielcode zum Auflisten von [Synchronisierungs Wiedergabelisten](enumerating-synchronization-playlists.md)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="19369-118">You can see how this function is used in the example code in [Enumerating Synchronization Playlists](enumerating-synchronization-playlists.md).</span></span> <span data-ttu-id="19369-119">Die Funktion übernimmt die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="19369-119">The function takes the following parameters:</span></span>

-   <span data-ttu-id="19369-120">*pwiedergabe*.</span><span class="sxs-lookup"><span data-stu-id="19369-120">*pPlaylist*.</span></span> <span data-ttu-id="19369-121">Der Zeiger auf die zu sortierende Windows-Media Player Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="19369-121">The pointer to the Windows Media Player playlist to sort.</span></span> <span data-ttu-id="19369-122">Die Medienelemente in der Wiedergabeliste müssen auf andere Wiedergabelisten verweisen, nicht auf einzelne digitale Mediendateien.</span><span class="sxs-lookup"><span data-stu-id="19369-122">The media items in the playlist must point to other playlists, not individual digital media files.</span></span>
-   <span data-ttu-id="19369-123">*bstrausynertribute*.</span><span class="sxs-lookup"><span data-stu-id="19369-123">*bstrSyncAttribute*.</span></span> <span data-ttu-id="19369-124">Ein BSTR, das den Namen des Attributs der Synchronisierungs Partnerschaft für das aktuelle Gerät ("Sync01", "Sync02" usw.) enthält.</span><span class="sxs-lookup"><span data-stu-id="19369-124">A BSTR containing the name of the synchronization partnership attribute for the current device ("Sync01", "Sync02", and so on).</span></span>
-   <span data-ttu-id="19369-125">*plselected*.</span><span class="sxs-lookup"><span data-stu-id="19369-125">*plSelected*.</span></span> <span data-ttu-id="19369-126">Zeiger auf eine **Long** -Variable, die die Anzahl der Synchronisierungs Wiedergabelisten empfängt.</span><span class="sxs-lookup"><span data-stu-id="19369-126">Pointer to a **long** variable that receives the count of synchronization playlists.</span></span>

<span data-ttu-id="19369-127">Die-Funktion überprüft das Attribut der Synchronisierungs Partnerschaft für jedes Medien Element (das eine Wiedergabeliste darstellt) in der Wiedergabeliste, die von *pwiedergabe* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="19369-127">The function inspects the synchronization partnership attribute for each media item (representing a playlist) in the playlist specified by *pPlaylist*.</span></span> <span data-ttu-id="19369-128">Wenn das Attribut einen Wert ungleich 0 (null) aufweist, verschiebt der Code das Medien Element an den Anfang der Wiedergabeliste und fügt es in der Reihenfolge der Priorität ein.</span><span class="sxs-lookup"><span data-stu-id="19369-128">If the attribute has a nonzero value, the code moves the media item to the beginning of the playlist and inserts it in priority order.</span></span>

<span data-ttu-id="19369-129">Anschließend gibt die Funktion die Anzahl der Medienelemente (Synchronisierungs Wiedergabelisten) zurück, die einen Wert ungleich 0 (null) für das Attribut der Synchronisierungs Partnerschaft enthielt.</span><span class="sxs-lookup"><span data-stu-id="19369-129">When finished, the function returns the count of media items (synchronization playlists) that had a nonzero value for the synchronization partnership attribute.</span></span>


```C++
STDMETHODIMP CSyncSettings::SortPlaylist(IWMPPlaylist *pPlaylist, BSTR bstrSyncAttribute, long *plSelected)
{
    HRESULT hr = S_OK;
    long lSyncItemCount = 0;

    ATLASSERT (pPlaylist);
    ATLASSERT (plSelected);

    // Local copies of the parameters.
    CComPtr<IWMPPlaylist> spPlaylist(pPlaylist);
    CComBSTR bstrAttribute(bstrSyncAttribute);

    ATLASSERT (bstrAttribute.Length());

    // Get the count of playlist media items.
    long lCount = 0;
    spPlaylist->get_count(&lCount);

    // Walk the playlist.
    for(long i = 0; i < lCount; i++)
    {
        CComPtr<IWMPMedia> spMedia;                 
        CComBSTR bstrVal;            
        long lPriority = 0;
        
        hr = spPlaylist->get_item(i, &spMedia);

        if(SUCCEEDED(hr) && spMedia)
        {      
            // Get the sync priority value as a string.
            hr = spMedia->getItemInfo(bstrAttribute, &bstrVal);
        }

        if(SUCCEEDED(hr) && spMedia)
        {
            // Convert sync priority to a long number.
            lPriority = _wtol(bstrVal);
        }

        // Sort the playlist.
        // Only move the current item if it has a
        // sync priority value.
        if(lPriority > 0)
        {
            lSyncItemCount++;

            // Walk down the list and insert the item
            // in ascending order.
            for(long j = 0; j < lCount; j++)
            {
                CComPtr<IWMPMedia> spMediaCompare;
                CComBSTR bstrValCompare;
                long lPriorityTest = 0;

                hr = spPlaylist->get_item(j, &spMediaCompare);

                if(SUCCEEDED(hr) && spMediaCompare.p)
                {
                    hr = spMediaCompare->getItemInfo(bstrAttribute, &bstrValCompare);
                }
                if(SUCCEEDED(hr) && spMediaCompare.p)
                {
                    lPriorityTest = _wtol(bstrValCompare);
                    
                    if(lPriority <= lPriorityTest || 
                        0 == lPriorityTest)
                    {
                        hr = spPlaylist->moveItem(i, j);
                        break;                            
                    }                        
                } 
            } // for j                       
        } // if(lPriority > 0)          
    } // for i  
  
    // Return the sync item count.
    *plSelected = lSyncItemCount;

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="19369-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="19369-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19369-131">**Iwmpmedia:: getiteminfo**</span><span class="sxs-lookup"><span data-stu-id="19369-131">**IWMPMedia::getItemInfo**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo)
</dt> <dt>

[<span data-ttu-id="19369-132">**Iwmpwiedergabe:: get- \_ Element**</span><span class="sxs-lookup"><span data-stu-id="19369-132">**IWMPPlaylist::get\_item**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-get_item)
</dt> <dt>

[<span data-ttu-id="19369-133">**Iwmpwiedergabe:: muveitem**</span><span class="sxs-lookup"><span data-stu-id="19369-133">**IWMPPlaylist::moveItem**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-moveitem)
</dt> <dt>

[<span data-ttu-id="19369-134">**Synchronisierungs Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="19369-134">**Managing Synchronization Playlists**</span></span>](managing-synchronization-playlists.md)
</dt> <dt>

[<span data-ttu-id="19369-135">**Synchronisierungs Attribute**</span><span class="sxs-lookup"><span data-stu-id="19369-135">**Sync Attributes**</span></span>](sync-attributes.md)
</dt> </dl>

 

 




