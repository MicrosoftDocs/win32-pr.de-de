---
title: Abrufen des Reißstatus
description: Abrufen des Reißstatus
ms.assetid: 9907bfdd-eae7-4ca2-b488-5a6ad11416f5
keywords:
- Windows Media Player,CD-Ening
- Windows Media Player-Objektmodell,CD-Bebauung
- Objektmodell,CD-Überbauung
- Windows Media Player ActiveX-Steuerelement,CD-2016
- ActiveX,CD-Steuerung
- Windows Media Player Mobile ActiveX-Steuerelement, CD-2016
- Windows Media Player Mobil, CD-10
- CD-Leiste, Abrufen des Reißstatus
- Abrufen von CDs, Abrufen des Reißstatus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3210fa9e0db5f9260989d7bebb3650770cec7626892bc20546a6b602fb98955
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118570191"
---
# <a name="retrieving-the-rip-status"></a>Abrufen des Reißstatus

Sie können den Fortschritt des Wischvorgang überwachen, indem Sie [regelmäßig IWMPCiererRip::get \_ ripProgress aufrufen.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripprogress) Diese Methode ruft einen Statuswert für den gesamten Besendungsvorgang ab. Der abgerufene Wert ist eine Zahl, die den Prozentsatz der abgeschlossenen 0 bis 100-100-Werte darstellt.

Der Statuswert stellt den abgeschlossenen Prozentsatz des gesamten Vorgangs dar. Um den Fortschritt einer bestimmten Spur zu bestimmen, verwenden Sie [IWMPMedia::getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo) mit "RipProgress" als Attributnamen. Rufen Sie ZUM Ermitteln des Index der gerade gezeichneten Spur **IWMPPlaylist::getItemInfo** mit "CurrentRipTrackIndex" als Attributnamen auf.

Sie können den Zustand des Wischvorgang überwachen, indem Sie [regelmäßig IWMPCiererRip::get \_ ripState aufrufen.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripstate) Diese Methode ruft einen [WMPRipState-Enumerationswert](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate) ab, der angibt, ob der Vorgang durchgeführt oder beendet wird. Sie können auch den Status des Vorgangs überwachen, indem Sie das [IWMPEvents3::CiererRipStateChange-Ereignis](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripstatechange) behandeln. (Weitere Informationen [finden Sie unter Behandeln von Ereignissen in C++.)](handling-events-in-c.md) Achten Sie darauf, den **IWMPCiererRip-Zeiger** (bereitgestellt vom -Ereignis) mit dem Zeiger zu vergleichen, der Ihren Beschningsvorgang darstellt, um sicherzustellen, dass das Ereignis von Ihrem Vorgang ausgelöst wurde.

Der folgende Beispielcode zeigt, wie sie diese Funktionen verwenden, um den Status eines belässenden Vorgangs abzurufen.

Die folgenden Dialogsteuerelemente werden für das Codebeispiel definiert.



| Steuerungs-ID                   | Beschreibung                                                                                                        |
|------------------------------|--------------------------------------------------------------------------------------------------------------------|
| IDC \_ CURRENT \_ TRACK          | Statischer Text, der den Index der Gerade überhingten Spur darstellt.                                         |
| IDC \_ TRACK \_ PROGRESS \_ TEXT   | Statischer Text, der den Fortschritt der Spur darstellt, die derzeit als Prozentsatz ge nachverfolgt wird.                      |
| IDC \_ PROGRESS \_ TRACK         | Statusleiste mit einem Bereich von 0 bis 100, der den Fortschritt der gerade als Prozentsatz geerbte Spur darstellt. |
| TEXT ZUM \_ GESAMTFORTSCHRITT \_ DES IDC \_ | Statischer Text, der den Fortschritt des gesamten Vorgangs als Prozentsatz darstellt.                             |
| GESAMTER \_ \_ IDC-FORTSCHRITT       | Statusleiste mit einem Bereich von 0 bis 100, der den Fortschritt des gesamten Belässungsprozesses als Prozentsatz darstellt.        |
| IDC \_ \_ RIP-STATUS              | Statischer Text, der den gerade ausgeführten Vorgang anzeigt ("Besendung", "Beendet" oder "Unbekannt")             |



 


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

[**Erstellen einer CD**](ripping-a-cd.md)
</dt> <dt>

[**Abrufen der Rippingschnittstelle**](retrieving-the-ripping-interface.md)
</dt> <dt>

[**Starten des Reißprozesses**](starting-the-rip-process.md)
</dt> <dt>

[**Auswählen von Elementen für "Besendung"**](selecting-items-for-ripping.md)
</dt> </dl>

 

 




