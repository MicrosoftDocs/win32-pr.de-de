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
# <a name="managing-synchronization-playlists"></a>Synchronisierungs Wiedergabelisten

Windows Media Player 10 oder höher verwendet Wiedergabelisten, um digitale Mediendateien mit tragbaren Geräten zu synchronisieren. In diesem Abschnitt wird erläutert, wie Synchronisierungs Wiedergabelisten verwendet werden.

Der Beispielcode in diesem Abschnitt verwendet zwei ListView-Steuerelemente, um Informationen anzuzeigen. Das erste ListView-Steuerelement (IDC \_ plview) zeigt alle Wiedergabelisten in der Windows Media Player-Bibliothek an, wobei zuerst Synchronisierungs Wiedergabelisten angezeigt werden. Synchronisierungs Wiedergabelisten für das aktuell ausgewählte Gerät sind mit einem Häkchen gekennzeichnet und sind in der Reihenfolge der Synchronisierungs Priorität sortiert. Alle anderen Wiedergabelisten werden deaktiviert. Das ListView-Steuerelement wurde für die einfache Auswahl konfiguriert. Die Reihenfolge der Wiedergabelisten im ListView-Steuerelement bestimmt Ihre Synchronisierungs Priorität. Der aktivierte Zustand einer einzelnen Wiedergabeliste bestimmt, ob es sich um eine Synchronisierungs Wiedergabeliste für das aktuell ausgewählte Gerät handelt.

Das zweite ListView-Steuerelement (IDC \_ MediaView) zeigt die Medienelemente in der ausgewählten Wiedergabeliste an. In zwei zusätzlichen Spalten wird Text angezeigt, der angibt, ob die digitale Mediendatei auf das Gerät kopiert wurde, und im Fall eines Fehlers, ob der Kopiervorgang fehlgeschlagen ist, da die digitale Mediendatei nicht passt.

Der folgende Beispielcode zeigt, wie die ListView-Steuerelemente initialisiert werden:


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



Das folgende Array von Zeichen folgen enthält die Namen der Synchronisierungs Attribute, die in den Beispielen verwendet werden:


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



Die folgende Member-Variable enthält eine Wiedergabeliste, die alle Wiedergabelisten in der Windows Media Player-Bibliothek enthält. Jede Wiedergabeliste wird als Medien Element dargestellt.


```C++
CComPtr<IWMPPlaylist> m_spPlaylist;
```



Die folgenden Abschnitte enthalten Beispielcode:

-   [Auflisten von Synchronisierungs Wiedergabelisten](enumerating-synchronization-playlists.md)
-   [Sortieren von Wiedergabelisten nach Synchronisierungs Priorität](sorting-playlists-by-synchronization-priority.md)
-   [Auflisten der Medienelemente](enumerating-the-media-items.md)
-   [Status der Wiedergabelisten Synchronisierung](determining-playlist-synchronization-state.md)
-   [Ändern der Synchronisierungs Priorität](changing-synchronization-priority.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Arbeiten mit tragbaren Geräten**](working-with-portable-devices.md)
</dt> </dl>

 

 




