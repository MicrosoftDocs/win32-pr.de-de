---
title: Auflisten der Medienelemente
description: Auflisten der Medienelemente
ms.assetid: 1819b4c3-57ae-48fc-8a01-b699b5802b64
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
ms.openlocfilehash: e8e07148ed6978355056febfb2ad920e4b1380a3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106338243"
---
# <a name="enumerating-the-media-items"></a>Auflisten der Medienelemente

Der folgende Code zeigt die Medienelemente an, die in einer einzelnen Wiedergabeliste enthalten sind. Dieser Code wird ausgeführt, wenn der Benutzer auf eine Wiedergabeliste im ListView-Steuerelement klickt, das von IDC \_ plview identifiziert wird.


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



Informationen zur Implementierung der getpartnershipsyncstate-Funktion finden Sie unter [bestimmen des Synchronisierungs Status der Wiedergabeliste](determining-playlist-synchronization-state.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmpmedia-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[**Iwmpwiedergabe-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)
</dt> <dt>

[**Synchronisierungs Wiedergabelisten**](managing-synchronization-playlists.md)
</dt> </dl>

 

 




