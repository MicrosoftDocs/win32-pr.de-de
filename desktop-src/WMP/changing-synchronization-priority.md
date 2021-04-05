---
title: Ändern der Synchronisierungs Priorität
description: Ändern der Synchronisierungs Priorität
ms.assetid: 992781cb-5018-4b88-aa93-2f8a86468a42
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
- Portable Geräte, Ändern der Prioritäten der Synchronisierungs Wiedergabeliste
- Synchronisierungs Wiedergabelisten, Prioritäten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 327f211282e2e3b35c21dce721a17f99dcb6583d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723608"
---
# <a name="changing-synchronization-priority"></a><span data-ttu-id="bdbb3-115">Ändern der Synchronisierungs Priorität</span><span class="sxs-lookup"><span data-stu-id="bdbb3-115">Changing Synchronization Priority</span></span>

<span data-ttu-id="bdbb3-116">Der folgende Beispielcode gibt einen Prioritätswert für jedes Element im ListView-Steuerelement an, das von IDC \_ plview identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="bdbb3-116">The following example code specifies a priority value for each item in the ListView control identified by IDC\_PLVIEW.</span></span> <span data-ttu-id="bdbb3-117">Elemente, die mit einem Häkchen gekennzeichnet sind, wird basierend auf ihrer Reihenfolge in der Liste ein Prioritätswert zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="bdbb3-117">Items that are marked with a check mark are assigned a priority value based on their order in the list.</span></span> <span data-ttu-id="bdbb3-118">Elementen, die nicht aktiviert sind, wird ein Prioritätswert von 0 (null) zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="bdbb3-118">Items that are not checked are assigned a priority value of zero.</span></span>


```C++
void CSyncSettings::SetPriorities()
{
    ATLASSERT(m_spPlaylist.p);
    
    long lCount = 0;
    CComBSTR bstrAttribute(g_szSyncAttributeNames[m_lCurrentPSIndex]); 
    long lPriorityCount = 0; // Tracks the next priority value to be assigned.
    long lNewPriority = 0; // Contains the new priority value for the playlist.

    HRESULT hr = m_spPlaylist->get_count(&lCount);

    if(SUCCEEDED(hr) && lCount > 0)
    {
        HCURSOR hCursor = LoadCursor(NULL, IDC_WAIT);
        HCURSOR hCursorOld = SetCursor(hCursor);

        // Walk the list.
        for(long i = 0; i < lCount; i++)
        {
            CComPtr<IWMPMedia> spMedia;
            BOOL bChecked = ListView_GetCheckState(m_hPlView, i);

            if(TRUE == bChecked)
            {
                // Assign a priority value.
                lNewPriority = ++lPriorityCount;
            }
            else
            {
                // Not a sync playlist.
                lNewPriority = 0;
            }

            // Set the attribute on the playlist.
            hr = m_spPlaylist->get_item(i, &spMedia);

            if(SUCCEEDED(hr))
            {     
                WCHAR buffer[30];
                _ltow(lNewPriority, buffer, 10);
                CComBSTR bstrPriority(buffer);
                hr = spMedia->setItemInfo(bstrAttribute, bstrPriority);
            }
        }
        SetCursor(hCursorOld);
    }       
}
```



## <a name="related-topics"></a><span data-ttu-id="bdbb3-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bdbb3-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdbb3-120">**Iwmpmedia-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="bdbb3-120">**IWMPMedia Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[<span data-ttu-id="bdbb3-121">**Iwmpwiedergabe-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="bdbb3-121">**IWMPPlaylist Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)
</dt> <dt>

[<span data-ttu-id="bdbb3-122">**Synchronisierungs Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="bdbb3-122">**Managing Synchronization Playlists**</span></span>](managing-synchronization-playlists.md)
</dt> </dl>

 

 




