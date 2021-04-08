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
# <a name="sorting-playlists-by-synchronization-priority"></a>Sortieren von Wiedergabelisten nach Synchronisierungs Priorität

Der folgende Code führt eine einfache Art von Wiedergabelisten aus. Sie können sehen, wie diese Funktion im Beispielcode zum Auflisten von [Synchronisierungs Wiedergabelisten](enumerating-synchronization-playlists.md)verwendet wird. Die Funktion übernimmt die folgenden Parameter:

-   *pwiedergabe*. Der Zeiger auf die zu sortierende Windows-Media Player Wiedergabeliste. Die Medienelemente in der Wiedergabeliste müssen auf andere Wiedergabelisten verweisen, nicht auf einzelne digitale Mediendateien.
-   *bstrausynertribute*. Ein BSTR, das den Namen des Attributs der Synchronisierungs Partnerschaft für das aktuelle Gerät ("Sync01", "Sync02" usw.) enthält.
-   *plselected*. Zeiger auf eine **Long** -Variable, die die Anzahl der Synchronisierungs Wiedergabelisten empfängt.

Die-Funktion überprüft das Attribut der Synchronisierungs Partnerschaft für jedes Medien Element (das eine Wiedergabeliste darstellt) in der Wiedergabeliste, die von *pwiedergabe* angegeben wird. Wenn das Attribut einen Wert ungleich 0 (null) aufweist, verschiebt der Code das Medien Element an den Anfang der Wiedergabeliste und fügt es in der Reihenfolge der Priorität ein.

Anschließend gibt die Funktion die Anzahl der Medienelemente (Synchronisierungs Wiedergabelisten) zurück, die einen Wert ungleich 0 (null) für das Attribut der Synchronisierungs Partnerschaft enthielt.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmpmedia:: getiteminfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo)
</dt> <dt>

[**Iwmpwiedergabe:: get- \_ Element**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-get_item)
</dt> <dt>

[**Iwmpwiedergabe:: muveitem**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-moveitem)
</dt> <dt>

[**Synchronisierungs Wiedergabelisten**](managing-synchronization-playlists.md)
</dt> <dt>

[**Synchronisierungs Attribute**](sync-attributes.md)
</dt> </dl>

 

 




