---
title: Auflisten von Synchronisierungswiedergabelisten
description: Auflisten von Synchronisierungswiedergabelisten
ms.assetid: 830c3ea5-2937-48b5-b89f-ef68a6649ca3
keywords:
- Windows Media Player,Synchronisierungswiedergabelisten
- Windows Media Player-Objektmodell, Synchronisierungswiedergabelisten
- Objektmodell,Synchronisierungswiedergabelisten
- Windows Media Player Mobil, Synchronisierungswiedergabelisten
- Windows Media Player ActiveX,Synchronisierungswiedergabelisten
- Windows Media Player Mobile ActiveX-Steuerelement, Synchronisierungswiedergabelisten
- ActiveX,Synchronisierungswiedergabelisten
- Wiedergabelisten,Synchronisierung
- Metafile-Wiedergabelisten,Synchronisierung
- Windows Wiedergabelisten von Medienmetadateien, Synchronisierung
- Synchronisierungswiedergabelisten,Aufzählen
- Portable Geräte,Aufzählen
- Enumerationen,Synchronisierungswiedergabelisten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55c6da1b91ffb779bc32262584375a7970bb20b2c644d6ee6893eacfea0b0d6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117935147"
---
# <a name="enumerating-synchronization-playlists"></a>Auflisten von Synchronisierungswiedergabelisten

Der folgende Beispielcode erstellt eine Funktion, die ein ListView-Steuerelement mit Wiedergabelisten füllt. Synchronisierungswiedergabelisten werden zuerst angezeigt. Synchronisierungswiedergabelisten für das derzeit ausgewählte Gerät werden mit einem Häkchen markiert und in der Reihenfolge der Synchronisierungspriorität sortiert. Alle anderen Wiedergabelisten sind deaktiviert.

Das ListView-Steuerelement wurde für eine einzelne Auswahl konfiguriert. Die Reihenfolge der Wiedergabelisten im ListView-Steuerelement bestimmt deren Synchronisierungspriorität. Der überprüfte Status einer einzelnen Wiedergabeliste bestimmt, ob es sich um eine Synchronisierungswiedergabeliste für das aktuell ausgewählte Gerät handelt.

Der Parameter *lPSIndex gibt* den Partnerschaftsindex für das derzeit ausgewählte portable Gerät an.


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



Informationen zur Implementierung der SortPlaylist-Funktion finden Sie unter [Sortieren von Wiedergabelisten nach Synchronisierungspriorität.](sorting-playlists-by-synchronization-priority.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMPMedia::getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo)
</dt> <dt>

[**IWMPMediaCollection::getByAttribute**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getbyattribute)
</dt> <dt>

[**Verwalten von Synchronisierungswiedergabelisten**](managing-synchronization-playlists.md)
</dt> <dt>

[**Synchronisierungsattribute**](sync-attributes.md)
</dt> </dl>

 

 




