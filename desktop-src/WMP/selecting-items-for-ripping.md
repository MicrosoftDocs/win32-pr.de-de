---
title: Auswählen von Elementen für Das Auswählen
description: Auswählen von Elementen für Das Auswählen
ms.assetid: 94bc765a-8318-4715-82e0-e7a9b93e99e0
keywords:
- Windows Media Player, CD-Umarbeitung
- Windows Media Player-Objektmodell, CD-Endering
- Objektmodell, CD-Endering
- Windows Media Player ActiveX-Steuerelement, CD-Platte
- ActiveX-Steuerelement, CD-Platte
- Windows Media Player Mobile ActiveX-Steuerelement, CD-Platte
- Windows Media Player Mobil, CD-Platte
- CD-Umschalten, Auswählen von Elementen
- CDs auswählen, Elemente auswählen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea677028fab6b3c39466e916bd8bb59ea8cee4d370730c096cbb98978f4abc49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119646650"
---
# <a name="selecting-items-for-ripping"></a>Auswählen von Elementen für Das Auswählen

Manchmal möchte ein Benutzer nicht jede Spur auf einer CD berennen. Windows Media Player stellt eine Schnittstelle bereit, mit der angegeben werden kann, welche Spuren für die Löschung ausgewählt werden. In einer CD-Anwendung gibt es in der Regel eine Benutzeroberfläche, über die der Benutzer Kontrollkästchen in einer Liste von Spuren auf der CD aktivieren kann.

Einige Spuren sind möglicherweise nicht standardmäßig für die Löschung ausgewählt. Wenn sich eine Spur bereits in der bibliothek Windows Media Player befindet, wird sie nicht automatisch für die Suche ausgewählt. Im zweiten Codebeispiel in diesem Abschnitt wird veranschaulicht, wie der Standardwert umgangen und manuell eine Spur für die Suche ausgewählt wird, wenn er bereits ausgereift wurde.

Im folgenden Codebeispiel wird veranschaulicht, wie ermittelt wird, ob eine Spur für die Löschung ausgewählt ist:


```C++
HRESULT CMainDlg::IsTrackSelected(long lIndex, bool &bSelected)
{
    // The track is selected unless the
    // "SelectedForRip" attribute is true.
    bSelected = true;

    // bstrItemName and bstrVal are used for getItemInfo.
    CComBSTR bstrItemName;
    CComBSTR bstrVal;

    // Get an IWMPMedia from the Playlist.
    CComPtr<IWMPMedia> spMedia;
    HRESULT hr = m_spPlaylist->get_item(lIndex, &spMedia);

    // Check whether it is selected for ripping.
    if (SUCCEEDED(hr))
    {
        hr = bstrItemName.Append("SelectedForRip");
    }
    if (SUCCEEDED(hr))
    {
        hr = spMedia->getItemInfo(
            bstrItemName,
            &bstrVal);
    }
    if (SUCCEEDED(hr))
    {
        // If getItemInfo("SelectedForRip") is not "True"
        // then the track is not selected.
        if (wcscmp(bstrVal.m_str, L"True"))
            bSelected = false;
    }

    return hr;
}

```



Im folgenden Codebeispiel wird veranschaulicht, wie sie angeben, ob eine Spur für die Löschung ausgewählt wird.


```C++
HRESULT CMainDlg::SelectTrack (long lIndex, bool bSelected)
{
    // bstrItemName and bstrVal are used for setItemInfo.
    CComBSTR bstrItemName;
    CComBSTR bstrVal;

    // Get an IWMPMedia from the Playlist.
    CComPtr<IWMPMedia> spMedia;
    HRESULT hr = m_spPlaylist->get_item(lIndex, &spMedia);

    // Select the track for ripping.
    if (SUCCEEDED(hr))
    {
        hr = bstrItemName.Append("SelectedForRip");
    }
    if (SUCCEEDED(hr))
    {
        if (bSelected)
        {
            hr = bstrVal.Append("True");
        }
        else
        {
            hr = bstrVal.Append("False");
        }
    }
    if (SUCCEEDED(hr))
    {
        hr = spMedia->setItemInfo(
            bstrItemName,
            bstrVal);
    }

    return hr;
}

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Bearbeitung einer CD**](ripping-a-cd.md)
</dt> <dt>

[**Abrufen der Rippingschnittstelle**](retrieving-the-ripping-interface.md)
</dt> <dt>

[**Starten des Abzockprozesses**](starting-the-rip-process.md)
</dt> <dt>

[**Abrufen des Reifegrads**](retrieving-the-rip-status.md)
</dt> </dl>

 

 




