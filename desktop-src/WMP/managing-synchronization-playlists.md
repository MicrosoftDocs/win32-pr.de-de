---
title: Verwalten von Synchronisierungswiedergabelisten
description: Verwalten von Synchronisierungswiedergabelisten
ms.assetid: 5891ada0-37a6-4256-9885-8aa9dbe98b7c
keywords:
- Windows Media Player,portable Geräte
- Windows Media Player Objektmodell, portable Geräte
- Objektmodell, portable Geräte
- Windows Media Player ActiveX,portable Geräte
- ActiveX,portable Geräte
- Windows Media Player Mobile ActiveX Steuerung, portable Geräte
- Windows Media Player Mobile, portable Geräte
- Portable Geräte,Verwalten von Synchronisierungswiedergabelisten
- Gerätesynchronisierung,Wiedergabelisten
- Synchronisieren von Geräten, Wiedergabelisten
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
- Synchronisierungswiedergabelisten,Verwalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10253d7f08c618d62079ccc1767fdaf85560861eae68d39cd897e7959eaffcad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996370"
---
# <a name="managing-synchronization-playlists"></a>Verwalten von Synchronisierungswiedergabelisten

Windows Media Player 10 oder höher verwendet Wiedergabelisten, um digitale Mediendateien mit portablen Geräten zu synchronisieren. In diesem Abschnitt wird erläutert, wie Sie mit Synchronisierungswiedergabelisten arbeiten.

Der Beispielcode in diesem Abschnitt verwendet zwei ListView-Steuerelemente, um Informationen anzuzeigen. Das erste ListView-Steuerelement (IDC PLVIEW) zeigt alle Wiedergabelisten in der \_ Windows Media Player-Bibliothek an, und Synchronisierungswiedergabelisten werden zuerst angezeigt. Synchronisierungswiedergabelisten für das derzeit ausgewählte Gerät werden mit einem Häkchen markiert und in der Reihenfolge der Synchronisierungspriorität sortiert. Alle anderen Wiedergabelisten sind deaktiviert. Das ListView-Steuerelement wurde für eine einzelne Auswahl konfiguriert. Die Reihenfolge der Wiedergabelisten im ListView-Steuerelement bestimmt deren Synchronisierungspriorität. Der überprüfte Status einer einzelnen Wiedergabeliste bestimmt, ob es sich um eine Synchronisierungswiedergabeliste für das aktuell ausgewählte Gerät handelt.

Das zweite ListView-Steuerelement (IDC \_ MEDIAVIEW) zeigt die Medienelemente in der ausgewählten Wiedergabeliste an. Zwei zusätzliche Spalten zeigen Text an, der angibt, ob die digitale Mediendatei auf das Gerät kopiert wurde und ob bei einem Fehler ein Fehler beim Kopieren auft war, weil die digitale Mediendatei nicht passte.

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



Das folgende Array von Zeichenfolgen enthält die Namen der Synchronisierungsattribute, die in den Beispielen verwendet werden:


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



Die folgende Membervariable enthält eine Wiedergabeliste, die alle Wiedergabelisten in der Windows Media Player enthält. Jede Wiedergabeliste wird als Medienelement dargestellt.


```C++
CComPtr<IWMPPlaylist> m_spPlaylist;
```



Die folgenden Abschnitte enthalten Beispielcode:

-   [Auflisten von Synchronisierungswiedergabelisten](enumerating-synchronization-playlists.md)
-   [Sortieren von Wiedergabelisten nach Synchronisierungspriorität](sorting-playlists-by-synchronization-priority.md)
-   [Aufzählen der Medienelemente](enumerating-the-media-items.md)
-   [Bestimmen des Wiedergabelistensynchronisierungsstatus](determining-playlist-synchronization-state.md)
-   [Ändern der Synchronisierungspriorität](changing-synchronization-priority.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Arbeiten mit portablen Geräten**](working-with-portable-devices.md)
</dt> </dl>

 

 




