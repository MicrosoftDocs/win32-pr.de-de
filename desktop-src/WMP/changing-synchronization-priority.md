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
# <a name="changing-synchronization-priority"></a>Ändern der Synchronisierungs Priorität

Der folgende Beispielcode gibt einen Prioritätswert für jedes Element im ListView-Steuerelement an, das von IDC \_ plview identifiziert wird. Elemente, die mit einem Häkchen gekennzeichnet sind, wird basierend auf ihrer Reihenfolge in der Liste ein Prioritätswert zugewiesen. Elementen, die nicht aktiviert sind, wird ein Prioritätswert von 0 (null) zugewiesen.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmpmedia-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[**Iwmpwiedergabe-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)
</dt> <dt>

[**Synchronisierungs Wiedergabelisten**](managing-synchronization-playlists.md)
</dt> </dl>

 

 




