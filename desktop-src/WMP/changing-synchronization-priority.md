---
title: Ändern der Synchronisierungspriorität
description: Ändern der Synchronisierungspriorität
ms.assetid: 992781cb-5018-4b88-aa93-2f8a86468a42
keywords:
- Windows Media Player, Synchronisierungswiedergabelisten
- Windows Media Player Objektmodell, Synchronisierungswiedergabelisten
- Objektmodell, Synchronisierungswiedergabelisten
- Windows Media Player Mobile Wiedergabelisten, Synchronisierungswiedergabelisten
- Windows Media Player ActiveX-Steuerelement, Synchronisierungswiedergabelisten
- Windows Media Player Mobile ActiveX- und Synchronisierungswiedergabelisten
- ActiveX-Steuerelement, Synchronisierungswiedergabelisten
- Wiedergabelisten, Synchronisierung
- Metafile-Wiedergabelisten, Synchronisierung
- Windows Medienmetadatei-Wiedergabelisten, Synchronisierung
- Portable Geräte, Ändern der Prioritäten der Synchronisierungswiedergabeliste
- Synchronisierungswiedergabelisten, Prioritäten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1513679bcde31893cd7c4f456bc0e99404bb5dc66de37976f2053ae1559a4cdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997660"
---
# <a name="changing-synchronization-priority"></a>Ändern der Synchronisierungspriorität

Der folgende Beispielcode gibt einen Prioritätswert für jedes Element im ListView-Steuerelement an, das durch IDC PLVIEW identifiziert \_ wird. Elementen, die mit einem Häkchen markiert sind, wird basierend auf ihrer Reihenfolge in der Liste ein Prioritätswert zugewiesen. Elementen, die nicht überprüft werden, wird der Prioritätswert 0 (null) zugewiesen.


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

[**IWMPMedia-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[**IWMPPlaylist-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)
</dt> <dt>

[**Verwalten von Synchronisierungswiedergabelisten**](managing-synchronization-playlists.md)
</dt> </dl>

 

 




