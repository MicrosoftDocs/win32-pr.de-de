---
title: Abrufen des Verbrauchs Status
description: Abrufen des Verbrauchs Status
ms.assetid: 63b6525d-00be-4c68-8473-3bc1a58fde15
keywords:
- Windows Media Player, CD-brennen
- Windows Media Player-Objektmodell, CD-brennen
- Objektmodell, CD-brennen
- Windows Media Player ActiveX-Steuerelement, CD-brennen
- ActiveX-Steuerelement, CD-brennen
- Windows Media Player Mobile ActiveX-Steuerelement, CD-brennen
- Windows Media Player Mobile, CD-brennen
- CD-brennen, Abrufen des Verbrauchs Status
- Brennen von CDs, Abrufen des Verbrauchs Status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9b9ab1d865b728c3a23b9b77f45ab022226605
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103948449"
---
# <a name="retrieving-the-burn-status"></a>Abrufen des Verbrauchs Status

Im folgenden Codebeispiel werden die folgenden Dialogfeld Steuerelemente definiert:



| Steuerungs-ID           | BESCHREIBUNG                                                                    |
|----------------------|--------------------------------------------------------------------------------|
| IDC- \_ Verbrauchs \_ Status     | Statischer Text, der den Zustand des CD-Brennvorgangs darstellt.             |
| IDC \_ -Status        | Statusanzeige mit einem Bereich von 0 bis 100, der den gesamten Durchsatz darstellt. |
| IDC- \_ Fortschritts \_ Text  | Statischer Text, der den gesamten Verbrennungs Fortschritt als Zahl zwischen 0 und 100 darstellt. |
| \_Verfügbare IDC- \_ Zeit | Statischer Text zum Anzeigen der auf der CD verfügbaren Zeit (in Sekunden).               |
| IDC- \_ freier \_ Speicherplatz     | Statischer Text, um den freien Speicherplatz auf der CD in Bytes anzuzeigen.                     |
| IDC- \_ Gesamt \_ Speicherplatz    | Statischer Text zum Anzeigen der Gesamtkapazität der CD in Bytes.                 |



 

Sie können den Fortschritt des Brennvorgangs überwachen, indem Sie in regelmäßigen Abständen [iwmpcdromburn:: get \_ burnprogress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnprogress) aufrufen, während die CD gebrannt wird. Diese Methode ruft einen Statuswert für den gesamten Brennvorgang ab. Der abgerufene Wert ist eine Zahl, die den Prozentsatz der abgeschlossenen Verbrennung (von 0 bis 100) darstellt.


```C++
// Update the progress bar IDC_PROGRESS
// and the corresponding text string IDC_PROGRESS_TEXT.
long lProgress = 0;
hr = m_spCdromBurn->get_burnProgress(&lProgress);
if (SUCCEEDED(hr))
{
    SendMessage(GetDlgItem(IDC_PROGRESS),
        PBM_SETPOS, lProgress, 0);
    SetDlgItemInt(IDC_PROGRESS_TEXT, lProgress);
}

```



Sie können den aktuellen Status des Brennvorgangs abrufen, indem Sie [iwmpcdromburn:: get \_ burnstate](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnstate)aufrufen. Diese Methode ruft eine Enumeration ab, die den aktuellen Vorgang angibt, der ausgeführt wird.


```C++
// Retrieve the burn state.
WMPBurnState wmpbs = wmpbsUnknown;
HRESULT hr = m_spCdromBurn->get_burnState(&wmpbs);

if (SUCCEEDED(hr))
{
    // Set the burn state string.
    CComBSTR bstrState;
    switch (wmpbs)
    {
        case wmpbsUnknown:
        default:
            hr = bstrState.Append("Unknown state.");
            break;
        case wmpbsBusy:
            hr = bstrState.Append("Windows Media Player is Busy.");
            break;
        case wmpbsReady:
            hr = bstrState.Append("Ready to begin burning.");
            break;
        case wmpbsWaitingForDisc:
            hr = bstrState.Append("Waiting for disc.");
            break;
        case wmpbsRefreshStatusPending:
            hr = bstrState.Append("The burn playlist has changed.");
            m_spCdromBurn->refreshStatus();
            break;
        case wmpbsPreparingToBurn:
            hr = bstrState.Append("Preparing to burn the CD.");
            break;
        case wmpbsBurning:
            hr = bstrState.Append("The CD is being burned.");
            break;
        case wmpbsStopped:
            hr = bstrState.Append("The burning operation is stopped.");
            break;
        case wmpbsErasing:
            hr = bstrState.Append("Erasing the CD.");
            break;
    }
    if (SUCCEEDED(hr))
    {
        SetDlgItemTextW(IDC_BURN_STATE, bstrState.m_str);
    }
}

```



Rufen Sie zum Abrufen der Anzahl von Sekunden, die die CD enthalten kann, [iwmpcdromburn:: getiteminfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-getiteminfo) mit "availabletime" als ersten Parameter auf. Der Wert, der von dieser Funktion abgerufen wird, wird durch eine Zeichenfolge dargestellt.


```C++
// Set "AvailableTime" string
CComBSTR bstrTime;
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("AvailableTime");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->getItemInfo(bstrItem, &bstrTime);
}
if (SUCCEEDED(hr))
{
    hr = bstrTime.Append(" seconds");
}
if (SUCCEEDED(hr))
{
    SetDlgItemTextW(IDC_AVAILABLE_TIME, bstrTime.m_str);
}

```



Um die Menge des freien Speicherplatzes auf einem Laufwerk abzurufen, rufen Sie **iwmpcdromburn:: getiteminfo** mit "FreeSpace" als ersten Parameter auf. Der Wert, der von dieser Funktion abgerufen wird, ist eine Zeichenfolge, die die Anzahl der auf der Festplatte verfügbaren freien Bytes darstellt.


```C++
// Set "FreeSpace" string
CComBSTR bstrFreeSpace;
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("FreeSpace");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->getItemInfo(bstrItem, &bstrFreeSpace);
}
if (SUCCEEDED(hr))
{
    hr = bstrFreeSpace.Append(" bytes");
}
if (SUCCEEDED(hr))
{
    SetDlgItemTextW(IDC_FREE_SPACE, bstrFreeSpace.m_str);
}

```



Rufen Sie zum Abrufen der Gesamtkapazität eines Datenträgers **iwmpcdromburn:: getiteminfo** mit "totalspace" als ersten Parameter auf. Der Wert, der von dieser Funktion abgerufen wird, ist eine Zeichenfolge, die der Gesamtzahl der Bytes auf der Festplatte entspricht.


```C++
// Set "TotalSpace" string.
CComBSTR bstrTotalSpace;
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("TotalSpace");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->getItemInfo(bstrItem, &bstrTotalSpace);
}
if (SUCCEEDED(hr))
{
    hr = bstrTotalSpace.Append(" bytes");
}
if (SUCCEEDED(hr))
{
    SetDlgItemTextW(IDC_TOTAL_SPACE, bstrTotalSpace.m_str);
}

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Brennen einer CD**](burning-a-cd.md)
</dt> <dt>

[**Abrufen der Schnittstelle zum Brennen von CDs**](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[**Der Verbrennungsprozess wird gestartet.**](starting-the-burn-process.md)
</dt> <dt>

[**Löschen einer erneut beschreibbaren CD**](erasing-a-rewritable-cd.md)
</dt> <dt>

[**Abrufen des Laufwerks und des Festplatten Status**](retrieving-the-drive-and-disc-status.md)
</dt> </dl>

 

 




