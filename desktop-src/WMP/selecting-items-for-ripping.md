---
title: Auswählen von Elementen für das Ripping
description: Auswählen von Elementen für das Ripping
ms.assetid: 94bc765a-8318-4715-82e0-e7a9b93e99e0
keywords:
- Windows Media Player, CD-einreißen
- Windows Media Player-Objektmodell, CD-einreißen
- Objektmodell, CD-einreißen
- Windows Media Player ActiveX-Steuerelement, CD-einreißen
- ActiveX-Steuerelement, CD-einreißen
- Windows Media Player Mobile ActiveX-Steuerelement, CD-einreißen
- Windows Media Player Mobile, CD-einreißen
- CD-Ripping, auswählen von Elementen
- einreißen CDs, auswählen von Elementen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfc18ded43b609be6c7ac1f16833b0c8a33505ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947849"
---
# <a name="selecting-items-for-ripping"></a>Auswählen von Elementen für das Ripping

Manchmal möchte ein Benutzer nicht jede Spur auf einer CD zerreißen. Windows Media Player stellt eine Schnittstelle bereit, mit der angegeben wird, welche Spuren zum Ripping ausgewählt werden. In der Regel gibt es in einer CD-einreißen-Anwendung eine Benutzeroberfläche, über die der Benutzer Kontrollkästchen in einer Liste der Titel auf der CD auswählen kann.

Einige Spuren werden möglicherweise nicht standardmäßig für das einreißen ausgewählt. Wenn ein Track bereits in der Windows Media Player-Bibliothek vorhanden ist, wird er nicht automatisch für das Ripping ausgewählt. Im zweiten Codebeispiel in diesem Abschnitt wird veranschaulicht, wie der Standardwert umgangen und manuell eine Spur für das einreißen ausgewählt wird, wenn er bereits in den Code gerissen wurde.

Im folgenden Codebeispiel wird veranschaulicht, wie Sie bestimmen können, ob ein Track für das Ripping ausgewählt ist:


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



Im folgenden Codebeispiel wird veranschaulicht, wie angegeben wird, ob ein Track für das Ripping ausgewählt ist.


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

[**Ripping einer CD**](ripping-a-cd.md)
</dt> <dt>

[**Abrufen der Rippingschnittstelle**](retrieving-the-ripping-interface.md)
</dt> <dt>

[**Der RIP-Prozess wird gestartet.**](starting-the-rip-process.md)
</dt> <dt>

[**Abrufen des Status "RIP"**](retrieving-the-rip-status.md)
</dt> </dl>

 

 




