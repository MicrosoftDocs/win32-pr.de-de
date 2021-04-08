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
# <a name="retrieving-the-rip-status"></a><span data-ttu-id="c8c11-112">Abrufen des Status "RIP"</span><span class="sxs-lookup"><span data-stu-id="c8c11-112">Retrieving the Rip Status</span></span>

<span data-ttu-id="c8c11-113">Sie können den Fortschritt des einreißen-Vorgangs überwachen, indem Sie in regelmäßigen Abständen [iwmpcdromrip:: get \_ ripprogress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripprogress)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c8c11-113">You can monitor the progress of the ripping operation by periodically calling [IWMPCdromRip::get\_ripProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripprogress).</span></span> <span data-ttu-id="c8c11-114">Diese Methode ruft einen Statuswert für den gesamten einreißen-Vorgang ab.</span><span class="sxs-lookup"><span data-stu-id="c8c11-114">This method retrieves a progress value for the entire ripping operation.</span></span> <span data-ttu-id="c8c11-115">Der abgerufene Wert ist eine Zahl, die den Prozentsatz des abgeschlossenen einreißen darstellt (von 0 bis 100).</span><span class="sxs-lookup"><span data-stu-id="c8c11-115">The value retrieved is a number that represents the percentage of ripping completed, from 0 to 100.</span></span>

<span data-ttu-id="c8c11-116">Der Statuswert stellt den abgeschlossenen Prozentsatz des gesamten rippingprozesses dar.</span><span class="sxs-lookup"><span data-stu-id="c8c11-116">The progress value represents the completed percentage of the entire ripping process.</span></span> <span data-ttu-id="c8c11-117">Verwenden Sie zum Bestimmen des Status einer bestimmten Spur [iwmpmedia:: getiteminfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo) mit "ripprogress" als Attribut Name.</span><span class="sxs-lookup"><span data-stu-id="c8c11-117">To determine the progress of a specific track, use [IWMPMedia::getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo) with "RipProgress" as the attribute name.</span></span> <span data-ttu-id="c8c11-118">Um den Index des aktuell ausgetauppten Titels zu ermitteln, nennen Sie **iwmpwiedergabe:: getiteminfo** mit "currentriptrackindex" als Attribut Name.</span><span class="sxs-lookup"><span data-stu-id="c8c11-118">To determine the index of the track currently being ripped, call **IWMPPlaylist::getItemInfo** with "CurrentRipTrackIndex" as the attribute name.</span></span>

<span data-ttu-id="c8c11-119">Sie können den Status des einreißen-Vorgangs überwachen, indem Sie in regelmäßigen Abständen [iwmpcdromrip:: get \_ ripstate](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripstate)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c8c11-119">You can monitor the state of the ripping operation by periodically calling [IWMPCdromRip::get\_ripState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripstate).</span></span> <span data-ttu-id="c8c11-120">Diese Methode ruft einen [wmpripstate](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate) -Enumerationswert ab, der angibt, ob der Vorgang gerade ausgeführt wird oder beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c8c11-120">This method retrieves a [WMPRipState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate) enumeration value that indicates whether the operation is in progress or stopped.</span></span> <span data-ttu-id="c8c11-121">Sie können auch den Status des rippingvorgangs überwachen, indem Sie das [IWMPEvents3:: cdromripstatechange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripstatechange) -Ereignis behandeln.</span><span class="sxs-lookup"><span data-stu-id="c8c11-121">You can also monitor the state of the ripping operation by handling the [IWMPEvents3::CdromRipStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripstatechange) event.</span></span> <span data-ttu-id="c8c11-122">(Weitere Informationen finden Sie [unter Handling Events in C++](handling-events-in-c.md).) Achten Sie darauf, den **iwmpcdromrip** -Zeiger (bereitgestellt durch das-Ereignis) mit dem Zeiger zu vergleichen, der den einreißen-Vorgang darstellt, um sicherzustellen, dass das Ereignis durch den Vorgang ausgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="c8c11-122">(See [Handling Events in C++](handling-events-in-c.md).) Be careful to compare the **IWMPCdromRip** pointer (provided by the event) to the pointer that represents your ripping operation, to ensure that the event was raised by your operation.</span></span>

<span data-ttu-id="c8c11-123">Der folgende Beispielcode zeigt, wie diese Funktionen verwendet werden, um den Status eines einreißen-Vorgangs abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c8c11-123">The following example code shows how to use these functions to retrieve the status of a ripping operation.</span></span>

<span data-ttu-id="c8c11-124">Die folgenden Dialogfeld Steuerelemente sind für das Codebeispiel definiert.</span><span class="sxs-lookup"><span data-stu-id="c8c11-124">The following dialog controls are defined for the code example.</span></span>



| <span data-ttu-id="c8c11-125">Steuerungs-ID</span><span class="sxs-lookup"><span data-stu-id="c8c11-125">Control ID</span></span>                   | <span data-ttu-id="c8c11-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c8c11-126">Description</span></span>                                                                                                        |
|------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8c11-127">IDC \_ Current \_ Track</span><span class="sxs-lookup"><span data-stu-id="c8c11-127">IDC\_CURRENT\_TRACK</span></span>          | <span data-ttu-id="c8c11-128">Statischer Text, der den Index des lauflaufs darstellt</span><span class="sxs-lookup"><span data-stu-id="c8c11-128">Static text that represents the index of the track currently being ripped.</span></span>                                         |
| <span data-ttu-id="c8c11-129">Status Text für IDC-nach \_ Verfolgung \_ \_</span><span class="sxs-lookup"><span data-stu-id="c8c11-129">IDC\_TRACK\_PROGRESS\_TEXT</span></span>   | <span data-ttu-id="c8c11-130">Statischer Text, der den Status der Nachverfolgung darstellt, die momentan als Prozentsatz ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c8c11-130">Static text that represents the progress of the track currently being ripped as a percentage.</span></span>                      |
| <span data-ttu-id="c8c11-131">IDC-Status \_ \_ Verfolgung</span><span class="sxs-lookup"><span data-stu-id="c8c11-131">IDC\_PROGRESS\_TRACK</span></span>         | <span data-ttu-id="c8c11-132">Statusanzeige mit einem Bereich von 0 bis 100, der den Status der aktuell ausgeführten Spur als Prozentsatz darstellt.</span><span class="sxs-lookup"><span data-stu-id="c8c11-132">Progress bar with range 0 to 100 that represents the progress of the track currently being ripped as a percentage.</span></span> |
| <span data-ttu-id="c8c11-133">IDC- \_ Gesamt \_ Fortschritts \_ Text</span><span class="sxs-lookup"><span data-stu-id="c8c11-133">IDC\_OVERALL\_PROGRESS\_TEXT</span></span> | <span data-ttu-id="c8c11-134">Statischer Text, der den Status des gesamten rippingprozesses als Prozentsatz darstellt.</span><span class="sxs-lookup"><span data-stu-id="c8c11-134">Static text that represents the progress of the total ripping process as a percentage.</span></span>                             |
| <span data-ttu-id="c8c11-135">IDC-Status \_ \_ insgesamt</span><span class="sxs-lookup"><span data-stu-id="c8c11-135">IDC\_PROGRESS\_OVERALL</span></span>       | <span data-ttu-id="c8c11-136">Statusanzeige mit einem Bereich von 0 bis 100, der den Status des gesamten rippingprozesses als Prozentsatz darstellt.</span><span class="sxs-lookup"><span data-stu-id="c8c11-136">Progress bar with range 0 to 100 that represents the progress of the total ripping process as a percentage.</span></span>        |
| <span data-ttu-id="c8c11-137">IDC- \_ RIP- \_ Zustand</span><span class="sxs-lookup"><span data-stu-id="c8c11-137">IDC\_RIP\_STATE</span></span>              | <span data-ttu-id="c8c11-138">Statischer Text, der den derzeit ausgeführten Vorgang anzeigt ("Ripping", "beendet" oder "unknown")</span><span class="sxs-lookup"><span data-stu-id="c8c11-138">Static text that displays the operation currently being performed ("Ripping", "Stopped", or "Unknown")</span></span>             |



 


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



## <a name="related-topics"></a><span data-ttu-id="c8c11-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c8c11-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8c11-140">**Ripping einer CD**</span><span class="sxs-lookup"><span data-stu-id="c8c11-140">**Ripping a CD**</span></span>](ripping-a-cd.md)
</dt> <dt>

[<span data-ttu-id="c8c11-141">**Abrufen der Rippingschnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c8c11-141">**Retrieving the Ripping Interface**</span></span>](retrieving-the-ripping-interface.md)
</dt> <dt>

[<span data-ttu-id="c8c11-142">**Der RIP-Prozess wird gestartet.**</span><span class="sxs-lookup"><span data-stu-id="c8c11-142">**Starting the Rip Process**</span></span>](starting-the-rip-process.md)
</dt> <dt>

[<span data-ttu-id="c8c11-143">**Auswählen von Elementen für das Ripping**</span><span class="sxs-lookup"><span data-stu-id="c8c11-143">**Selecting Items for Ripping**</span></span>](selecting-items-for-ripping.md)
</dt> </dl>

 

 




