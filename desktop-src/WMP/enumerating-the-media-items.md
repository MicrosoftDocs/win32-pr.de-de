---
title: Aufzählen der Medienelemente
description: Aufzählen der Medienelemente
ms.assetid: 1819b4c3-57ae-48fc-8a01-b699b5802b64
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
- Synchronisierungswiedergabelisten, Auflisten
- Portable Geräte, Aufzählen
- Enumerationen, Synchronisierungswiedergabelisten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96f6afd6c209f96edd011b6b5829af07583057bd9220c61015d8e8ffa9fe4bfa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650910"
---
# <a name="enumerating-the-media-items"></a>Aufzählen der Medienelemente

Der folgende Code zeigt die Medienelemente an, die in einer einzelnen Wiedergabeliste enthalten sind. Dieser Code wird ausgeführt, wenn der Benutzer im von IDC PLVIEW identifizierten ListView-Steuerelement auf eine Wiedergabeliste \_ klickt.


```C++
STDMETHODIMP CSyncSettings::ShowMedia(long lIndex)
{
    ATLASSERT(m_pMainDlg != NULL);
    ATLASSERT(m_spPlaylist.p);

    HRESULT hr = S_OK;
    long lCount = 0; // Count of items in the playlist.

    LVITEM lvI;
    ZeroMemory(&lvI, sizeof(LVITEM));
    lvI.mask = LVIF_TEXT;

    CComPtr<IWMPMedia> spPlaylist; // Playlist the user selected.
    CComBSTR bstrSourceURL; // The URL of a digital media file.
    CComPtr<IWMPPlaylist> spNewPlaylist; // Temporary playlist that contains media items.
    ULONG ulOnDevice = 0;
    ULONG ulDidNotFit = 0;

    HCURSOR hCursor = LoadCursor(NULL, IDC_WAIT);
    HCURSOR hCursorOld = SetCursor(hCursor);

    ListView_DeleteAllItems(m_hMediaView);

    // Retrieve the playlist the user selected.
    hr = m_spPlaylist->get_item(lIndex, &spPlaylist);
  
    if(SUCCEEDED(hr) && spPlaylist)
    {
         // Retrieve the source URL (the path).
         hr = spPlaylist->get_sourceURL(&bstrSourceURL);
    }

    if(SUCCEEDED(hr) && bstrSourceURL.Length())
    {
        CComPtr<IWMPCore3> spCore3;
        m_spPlayer.QueryInterface(&spCore3);

        // Create a temporary IWMPPlaylist object from the IWMPMedia 
        // playlist object.
        hr = spCore3->newPlaylist(CComBSTR("Temp"), bstrSourceURL, &spNewPlaylist);
    }

    if(SUCCEEDED(hr) && spNewPlaylist)
    {        
        hr = spNewPlaylist->get_count(&lCount);
    }

    // Walk the playlist.
    if(SUCCEEDED(hr) && lCount > 0)
    {
        for(long i = 0; i < lCount; i++)
        {
            CComPtr<IWMPMedia> spMedia;
            CComBSTR bstrMediaName; 
            CComBSTR bstrOnDevice = "???";
            CComBSTR bstrFit = "???";  

            hr = spNewPlaylist->get_item(i, &spMedia);
   
            if(SUCCEEDED(hr) && spMedia)
            {
                // Get the name.
                hr = spMedia->get_name(&bstrMediaName);                
            }

            if(SUCCEEDED(hr) && bstrMediaName.Length())
            {   
                // Show the media name.
                lvI.iItem = ListView_GetItemCount(m_hMediaView);
                lvI.iSubItem = 0;
                lvI.pszText = COLE2T(bstrMediaName);
                ListView_InsertItem(m_hMediaView, &lvI);
                
                // Retrieve the synchronization state information for 
                // the digital media file.
                hr = GetPartnershipSyncState(spMedia, m_lCurrentPSIndex, &ulOnDevice, &ulDidNotFit);
            }

            if(SUCCEEDED(hr))
            {                
                // Test whether the media is on the device.
                if(ulOnDevice == 1)
                {
                    bstrOnDevice = "Yes";
                    bstrFit = "Yes";
                }
                else
                {
                    bstrOnDevice = "No";
                    // 1 means media did not fit, 
                    // 0 means other reason for failure.
                    bstrFit = ulDidNotFit ? "No" : "Yes"; 
                }                 
            }
   
            ListView_SetItemText(m_hMediaView, lvI.iItem, 1, COLE2T(bstrOnDevice)); 
            ListView_SetItemText(m_hMediaView, lvI.iItem, 2, COLE2T(bstrFit));
        }
    } 

    if(SUCCEEDED(hr) && lCount == 0)
    {
        // Empty playlist.
        lvI.iItem = ListView_GetItemCount(m_hMediaView);
        lvI.iSubItem = 0;
        lvI.pszText = COLE2T(CComBSTR("No items to display."));
        ListView_InsertItem(m_hMediaView, &lvI);
    }
    
    SetCursor(hCursorOld);
    return hr;
}
```



Informationen zur Implementierung der GetPartnershipSyncState-Funktion finden Sie unter Bestimmen des [Wiedergabelistensynchronisierungsstatus.](determining-playlist-synchronization-state.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMPMedia-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[**IWMPPlaylist-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)
</dt> <dt>

[**Verwalten von Synchronisierungswiedergabelisten**](managing-synchronization-playlists.md)
</dt> </dl>

 

 




