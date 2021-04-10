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
# <a name="retrieving-the-burn-status"></a><span data-ttu-id="03266-112">Abrufen des Verbrauchs Status</span><span class="sxs-lookup"><span data-stu-id="03266-112">Retrieving the Burn Status</span></span>

<span data-ttu-id="03266-113">Im folgenden Codebeispiel werden die folgenden Dialogfeld Steuerelemente definiert:</span><span class="sxs-lookup"><span data-stu-id="03266-113">In the code example that follows, the following dialog controls are defined:</span></span>



| <span data-ttu-id="03266-114">Steuerungs-ID</span><span class="sxs-lookup"><span data-stu-id="03266-114">Control ID</span></span>           | <span data-ttu-id="03266-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="03266-115">Description</span></span>                                                                    |
|----------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="03266-116">IDC- \_ Verbrauchs \_ Status</span><span class="sxs-lookup"><span data-stu-id="03266-116">IDC\_BURN\_STATE</span></span>     | <span data-ttu-id="03266-117">Statischer Text, der den Zustand des CD-Brennvorgangs darstellt.</span><span class="sxs-lookup"><span data-stu-id="03266-117">Static text that represents the state of the CD burning operation.</span></span>             |
| <span data-ttu-id="03266-118">IDC \_ -Status</span><span class="sxs-lookup"><span data-stu-id="03266-118">IDC\_PROGRESS</span></span>        | <span data-ttu-id="03266-119">Statusanzeige mit einem Bereich von 0 bis 100, der den gesamten Durchsatz darstellt.</span><span class="sxs-lookup"><span data-stu-id="03266-119">Progress bar with a range of 0 to 100 that represents the total burn progress.</span></span> |
| <span data-ttu-id="03266-120">IDC- \_ Fortschritts \_ Text</span><span class="sxs-lookup"><span data-stu-id="03266-120">IDC\_PROGRESS\_TEXT</span></span>  | <span data-ttu-id="03266-121">Statischer Text, der den gesamten Verbrennungs Fortschritt als Zahl zwischen 0 und 100 darstellt.</span><span class="sxs-lookup"><span data-stu-id="03266-121">Static text that represents the total burn progress as a number from 0 to 100.</span></span> |
| <span data-ttu-id="03266-122">\_Verfügbare IDC- \_ Zeit</span><span class="sxs-lookup"><span data-stu-id="03266-122">IDC\_AVAILABLE\_TIME</span></span> | <span data-ttu-id="03266-123">Statischer Text zum Anzeigen der auf der CD verfügbaren Zeit (in Sekunden).</span><span class="sxs-lookup"><span data-stu-id="03266-123">Static text to display the time available on the CD, in seconds.</span></span>               |
| <span data-ttu-id="03266-124">IDC- \_ freier \_ Speicherplatz</span><span class="sxs-lookup"><span data-stu-id="03266-124">IDC\_FREE\_SPACE</span></span>     | <span data-ttu-id="03266-125">Statischer Text, um den freien Speicherplatz auf der CD in Bytes anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="03266-125">Static text to display the free space on the CD, in bytes.</span></span>                     |
| <span data-ttu-id="03266-126">IDC- \_ Gesamt \_ Speicherplatz</span><span class="sxs-lookup"><span data-stu-id="03266-126">IDC\_TOTAL\_SPACE</span></span>    | <span data-ttu-id="03266-127">Statischer Text zum Anzeigen der Gesamtkapazität der CD in Bytes.</span><span class="sxs-lookup"><span data-stu-id="03266-127">Static text to display the total capacity of the CD, in bytes.</span></span>                 |



 

<span data-ttu-id="03266-128">Sie können den Fortschritt des Brennvorgangs überwachen, indem Sie in regelmäßigen Abständen [iwmpcdromburn:: get \_ burnprogress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnprogress) aufrufen, während die CD gebrannt wird.</span><span class="sxs-lookup"><span data-stu-id="03266-128">You can monitor the progress of the burning operation by periodically calling [IWMPCdromBurn::get\_burnProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnprogress) while the CD is being burned.</span></span> <span data-ttu-id="03266-129">Diese Methode ruft einen Statuswert für den gesamten Brennvorgang ab.</span><span class="sxs-lookup"><span data-stu-id="03266-129">This method retrieves a progress value for the entire burning operation.</span></span> <span data-ttu-id="03266-130">Der abgerufene Wert ist eine Zahl, die den Prozentsatz der abgeschlossenen Verbrennung (von 0 bis 100) darstellt.</span><span class="sxs-lookup"><span data-stu-id="03266-130">The value retrieved is a number that represents the percentage of burning completed, from 0 to 100.</span></span>


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



<span data-ttu-id="03266-131">Sie können den aktuellen Status des Brennvorgangs abrufen, indem Sie [iwmpcdromburn:: get \_ burnstate](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnstate)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="03266-131">You can get the current state of the burning operation by calling [IWMPCdromBurn::get\_burnState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnstate).</span></span> <span data-ttu-id="03266-132">Diese Methode ruft eine Enumeration ab, die den aktuellen Vorgang angibt, der ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="03266-132">This method retrieves an enumeration specifying the current operation being performed.</span></span>


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



<span data-ttu-id="03266-133">Rufen Sie zum Abrufen der Anzahl von Sekunden, die die CD enthalten kann, [iwmpcdromburn:: getiteminfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-getiteminfo) mit "availabletime" als ersten Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="03266-133">To retrieve the number of seconds of audio the CD can hold, call [IWMPCdromBurn::getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-getiteminfo) with "AvailableTime" as the first parameter.</span></span> <span data-ttu-id="03266-134">Der Wert, der von dieser Funktion abgerufen wird, wird durch eine Zeichenfolge dargestellt.</span><span class="sxs-lookup"><span data-stu-id="03266-134">The value retrieved by this function is represented by a string.</span></span>


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



<span data-ttu-id="03266-135">Um die Menge des freien Speicherplatzes auf einem Laufwerk abzurufen, rufen Sie **iwmpcdromburn:: getiteminfo** mit "FreeSpace" als ersten Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="03266-135">To retrieve the amount of free space on a disc, call **IWMPCdromBurn::getItemInfo** with "FreeSpace" as the first parameter.</span></span> <span data-ttu-id="03266-136">Der Wert, der von dieser Funktion abgerufen wird, ist eine Zeichenfolge, die die Anzahl der auf der Festplatte verfügbaren freien Bytes darstellt.</span><span class="sxs-lookup"><span data-stu-id="03266-136">The value retrieved by this function is a string that represents the number of free bytes available on the disc.</span></span>


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



<span data-ttu-id="03266-137">Rufen Sie zum Abrufen der Gesamtkapazität eines Datenträgers **iwmpcdromburn:: getiteminfo** mit "totalspace" als ersten Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="03266-137">To retrieve the total capacity of a disc, call **IWMPCdromBurn::getItemInfo** with "TotalSpace" as the first parameter.</span></span> <span data-ttu-id="03266-138">Der Wert, der von dieser Funktion abgerufen wird, ist eine Zeichenfolge, die der Gesamtzahl der Bytes auf der Festplatte entspricht.</span><span class="sxs-lookup"><span data-stu-id="03266-138">The value retrieved by this function is a string that corresponds to the total number of bytes on the disc.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="03266-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="03266-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03266-140">**Brennen einer CD**</span><span class="sxs-lookup"><span data-stu-id="03266-140">**Burning a CD**</span></span>](burning-a-cd.md)
</dt> <dt>

[<span data-ttu-id="03266-141">**Abrufen der Schnittstelle zum Brennen von CDs**</span><span class="sxs-lookup"><span data-stu-id="03266-141">**Retrieving the CD Burning Interface**</span></span>](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[<span data-ttu-id="03266-142">**Der Verbrennungsprozess wird gestartet.**</span><span class="sxs-lookup"><span data-stu-id="03266-142">**Starting the Burn Process**</span></span>](starting-the-burn-process.md)
</dt> <dt>

[<span data-ttu-id="03266-143">**Löschen einer erneut beschreibbaren CD**</span><span class="sxs-lookup"><span data-stu-id="03266-143">**Erasing a Rewritable CD**</span></span>](erasing-a-rewritable-cd.md)
</dt> <dt>

[<span data-ttu-id="03266-144">**Abrufen des Laufwerks und des Festplatten Status**</span><span class="sxs-lookup"><span data-stu-id="03266-144">**Retrieving the Drive and Disc Status**</span></span>](retrieving-the-drive-and-disc-status.md)
</dt> </dl>

 

 




