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
# <a name="selecting-items-for-ripping"></a><span data-ttu-id="8d0cb-112">Auswählen von Elementen für das Ripping</span><span class="sxs-lookup"><span data-stu-id="8d0cb-112">Selecting Items for Ripping</span></span>

<span data-ttu-id="8d0cb-113">Manchmal möchte ein Benutzer nicht jede Spur auf einer CD zerreißen.</span><span class="sxs-lookup"><span data-stu-id="8d0cb-113">Sometimes a user does not want to rip every track on a CD.</span></span> <span data-ttu-id="8d0cb-114">Windows Media Player stellt eine Schnittstelle bereit, mit der angegeben wird, welche Spuren zum Ripping ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="8d0cb-114">Windows Media Player provides an interface for specifying which tracks are selected for ripping.</span></span> <span data-ttu-id="8d0cb-115">In der Regel gibt es in einer CD-einreißen-Anwendung eine Benutzeroberfläche, über die der Benutzer Kontrollkästchen in einer Liste der Titel auf der CD auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="8d0cb-115">Typically in a CD ripping application there is a user interface that lets the user select check boxes in a list of tracks on the CD.</span></span>

<span data-ttu-id="8d0cb-116">Einige Spuren werden möglicherweise nicht standardmäßig für das einreißen ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="8d0cb-116">Some tracks might not be selected for ripping by default.</span></span> <span data-ttu-id="8d0cb-117">Wenn ein Track bereits in der Windows Media Player-Bibliothek vorhanden ist, wird er nicht automatisch für das Ripping ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="8d0cb-117">If a track is already in the Windows Media Player library, it will not be automatically selected for ripping.</span></span> <span data-ttu-id="8d0cb-118">Im zweiten Codebeispiel in diesem Abschnitt wird veranschaulicht, wie der Standardwert umgangen und manuell eine Spur für das einreißen ausgewählt wird, wenn er bereits in den Code gerissen wurde.</span><span class="sxs-lookup"><span data-stu-id="8d0cb-118">The second code example in this section demonstrates how to bypass the default value and manually select a track for ripping if it has already been ripped.</span></span>

<span data-ttu-id="8d0cb-119">Im folgenden Codebeispiel wird veranschaulicht, wie Sie bestimmen können, ob ein Track für das Ripping ausgewählt ist:</span><span class="sxs-lookup"><span data-stu-id="8d0cb-119">The following code example demonstrates how to determine whether a track is selected for ripping:</span></span>


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



<span data-ttu-id="8d0cb-120">Im folgenden Codebeispiel wird veranschaulicht, wie angegeben wird, ob ein Track für das Ripping ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="8d0cb-120">The following code example demonstrates how to specify whether a track is selected for ripping.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="8d0cb-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8d0cb-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d0cb-122">**Ripping einer CD**</span><span class="sxs-lookup"><span data-stu-id="8d0cb-122">**Ripping a CD**</span></span>](ripping-a-cd.md)
</dt> <dt>

[<span data-ttu-id="8d0cb-123">**Abrufen der Rippingschnittstelle**</span><span class="sxs-lookup"><span data-stu-id="8d0cb-123">**Retrieving the Ripping Interface**</span></span>](retrieving-the-ripping-interface.md)
</dt> <dt>

[<span data-ttu-id="8d0cb-124">**Der RIP-Prozess wird gestartet.**</span><span class="sxs-lookup"><span data-stu-id="8d0cb-124">**Starting the Rip Process**</span></span>](starting-the-rip-process.md)
</dt> <dt>

[<span data-ttu-id="8d0cb-125">**Abrufen des Status "RIP"**</span><span class="sxs-lookup"><span data-stu-id="8d0cb-125">**Retrieving the Rip Status**</span></span>](retrieving-the-rip-status.md)
</dt> </dl>

 

 




