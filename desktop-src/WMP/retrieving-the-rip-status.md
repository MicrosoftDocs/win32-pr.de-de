---
title: Abrufen des Status "RIP"
description: Abrufen des Status "RIP"
ms.assetid: 9907bfdd-eae7-4ca2-b488-5a6ad11416f5
keywords:
- Windows Media Player, CD-einreißen
- Windows Media Player-Objektmodell, CD-einreißen
- Objektmodell, CD-einreißen
- Windows Media Player ActiveX-Steuerelement, CD-einreißen
- ActiveX-Steuerelement, CD-einreißen
- Windows Media Player Mobile ActiveX-Steuerelement, CD-einreißen
- Windows Media Player Mobile, CD-einreißen
- CD-Ripping, Abrufen des RIP-Status
- einreißen CDs, Abrufen des RIP-Status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be1fce1a46f9cc2d8477cabcc12a3a1b5bd159d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038596"
---
# <a name="retrieving-the-rip-status"></a>Abrufen des Status "RIP"

Sie können den Fortschritt des einreißen-Vorgangs überwachen, indem Sie in regelmäßigen Abständen [iwmpcdromrip:: get \_ ripprogress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripprogress)aufrufen. Diese Methode ruft einen Statuswert für den gesamten einreißen-Vorgang ab. Der abgerufene Wert ist eine Zahl, die den Prozentsatz des abgeschlossenen einreißen darstellt (von 0 bis 100).

Der Statuswert stellt den abgeschlossenen Prozentsatz des gesamten rippingprozesses dar. Verwenden Sie zum Bestimmen des Status einer bestimmten Spur [iwmpmedia:: getiteminfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo) mit "ripprogress" als Attribut Name. Um den Index des aktuell ausgetauppten Titels zu ermitteln, nennen Sie **iwmpwiedergabe:: getiteminfo** mit "currentriptrackindex" als Attribut Name.

Sie können den Status des einreißen-Vorgangs überwachen, indem Sie in regelmäßigen Abständen [iwmpcdromrip:: get \_ ripstate](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripstate)aufrufen. Diese Methode ruft einen [wmpripstate](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate) -Enumerationswert ab, der angibt, ob der Vorgang gerade ausgeführt wird oder beendet wurde. Sie können auch den Status des rippingvorgangs überwachen, indem Sie das [IWMPEvents3:: cdromripstatechange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripstatechange) -Ereignis behandeln. (Weitere Informationen finden Sie [unter Handling Events in C++](handling-events-in-c.md).) Achten Sie darauf, den **iwmpcdromrip** -Zeiger (bereitgestellt durch das-Ereignis) mit dem Zeiger zu vergleichen, der den einreißen-Vorgang darstellt, um sicherzustellen, dass das Ereignis durch den Vorgang ausgelöst wurde.

Der folgende Beispielcode zeigt, wie diese Funktionen verwendet werden, um den Status eines einreißen-Vorgangs abzurufen.

Die folgenden Dialogfeld Steuerelemente sind für das Codebeispiel definiert.



| Steuerungs-ID                   | BESCHREIBUNG                                                                                                        |
|------------------------------|--------------------------------------------------------------------------------------------------------------------|
| IDC \_ Current \_ Track          | Statischer Text, der den Index des lauflaufs darstellt                                         |
| Status Text für IDC-nach \_ Verfolgung \_ \_   | Statischer Text, der den Status der Nachverfolgung darstellt, die momentan als Prozentsatz ausgeführt wird.                      |
| IDC-Status \_ \_ Verfolgung         | Statusanzeige mit einem Bereich von 0 bis 100, der den Status der aktuell ausgeführten Spur als Prozentsatz darstellt. |
| IDC- \_ Gesamt \_ Fortschritts \_ Text | Statischer Text, der den Status des gesamten rippingprozesses als Prozentsatz darstellt.                             |
| IDC-Status \_ \_ insgesamt       | Statusanzeige mit einem Bereich von 0 bis 100, der den Status des gesamten rippingprozesses als Prozentsatz darstellt.        |
| IDC- \_ RIP- \_ Zustand              | Statischer Text, der den derzeit ausgeführten Vorgang anzeigt ("Ripping", "beendet" oder "unknown")             |



 


```C++
HRESULT CMainDlg::UpdateStatus (void)
{
    // bstrItemName and bstrVal are used for getItemInfo.
    CComBSTR bstrItemName;
    CComBSTR bstrVal;

    // Get the current track index.
    HRESULT hr = bstrItemName.Append("CurrentRipTrackIndex");
    if (SUCCEEDED(hr))
    {
        hr = m_spPlaylist->getItemInfo(bstrItemName, &bstrVal);
    }

    // Update the dialog text with the track number.
    if (SUCCEEDED(hr))
    {
        SetDlgItemTextW(IDC_CURRENT_TRACK, bstrVal.m_str);
    }

    // Get an IWMPMedia interface from the Playlist.
    CComPtr<IWMPMedia> spMedia;
    if (SUCCEEDED(hr))
    {
        long lIndex = _wtol(bstrVal.m_str);
        hr = m_spPlaylist->get_item(lIndex, &spMedia);
    }

    // Update the current track progress bar and progress text.
    if (SUCCEEDED(hr))
    {
        bstrItemName.Empty();
        hr = bstrItemName.Append("RipProgress");
    }
    if (SUCCEEDED(hr))
    {
        hr = spMedia->getItemInfo(bstrItemName, &bstrVal);
    }

    if (SUCCEEDED(hr))
    {
        // Update the text corresponding to the percentage.
        SetDlgItemTextW(IDC_TRACK_PROGRESS_TEXT, bstrVal.m_str);

        // Obtain a numerical value from the progress string.
        long lTrackPosition = _wtol(bstrVal.m_str);

        // Update the progress bar showing the percentage.
        SendMessage(GetDlgItem(IDC_PROGRESS_TRACK),
            PBM_SETPOS, lTrackPosition, 0);
    }

    // Update the total progress bar and progress text.
    long lTotalPosition = 0;
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromRip->get_ripProgress(&lTotalPosition);
    }
    if (SUCCEEDED(hr))
    {
        // Update the text corresponding to the percentage.
        SetDlgItemInt(IDC_OVERALL_PROGRESS_TEXT, lTotalPosition);

        // Update the progress bar showing the percentage.
        SendMessage(GetDlgItem(IDC_PROGRESS_OVERALL),
            PBM_SETPOS, lTotalPosition, 0);
    }

    // Update the ripping state.
    CComBSTR bstrState;
    WMPRipState wmprs = wmprsUnknown;
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromRip->get_ripState(&wmprs);
    }
    if (SUCCEEDED(hr))
    {
        switch (wmprs)
        {
            case wmprsUnknown:
            default:
                hr = bstrState.Append("Unknown");
                break;
            case wmprsRipping:
                hr = bstrState.Append("Ripping");
                break;
            case wmprsStopped:
                hr = bstrState.Append("Stopped");
                break;
        }
    }
    if (SUCCEEDED(hr))
    {
        SetDlgItemTextW(IDC_RIP_STATE, bstrState.m_str);
    }

    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Ripping einer CD**](ripping-a-cd.md)
</dt> <dt>

[**Abrufen der Rippingschnittstelle**](retrieving-the-ripping-interface.md)
</dt> <dt>

[**Der RIP-Prozess wird gestartet.**](starting-the-rip-process.md)
</dt> <dt>

[**Auswählen von Elementen für das Ripping**](selecting-items-for-ripping.md)
</dt> </dl>

 

 




