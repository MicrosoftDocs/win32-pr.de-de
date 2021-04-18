---
title: Status der Wiedergabelisten Synchronisierung
description: Status der Wiedergabelisten Synchronisierung
ms.assetid: 634b659b-c3ae-4957-b17e-18fd92e915be
keywords:
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
- Portable Geräte, bestimmen des Status der Synchronisierungs Wiedergabe
- Synchronisierungs Wiedergabelisten, Synchronisierungs Status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9758cfbb73c698a40d6d4f48e645e57750d8a332
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106337207"
---
# <a name="determining-playlist-synchronization-state"></a><span data-ttu-id="b526a-115">Status der Wiedergabelisten Synchronisierung</span><span class="sxs-lookup"><span data-stu-id="b526a-115">Determining Playlist Synchronization State</span></span>

<span data-ttu-id="b526a-116">Windows Media Player 10 oder höher verwendet das **SyncState** -Attribut, um Informationen darüber zu erhalten, ob eine bestimmte digitale Mediendatei auf ein tragbares Gerät kopiert wurde, und im Falle eines Fehlers, ob das Kopieren fehlgeschlagen ist, da das Gerät nicht über genügend Arbeitsspeicher verfügt.</span><span class="sxs-lookup"><span data-stu-id="b526a-116">Windows Media Player 10 or later uses the **SyncState** attribute to contain information about whether a particular digital media file has been copied to a portable device and, in the case of a failure, whether copying failed because the device did not have enough memory.</span></span>

<span data-ttu-id="b526a-117">Im folgenden Beispielcode wird eine Funktion erstellt, die diese Informationen aus einer digitalen Mediendatei abruft.</span><span class="sxs-lookup"><span data-stu-id="b526a-117">The following example code creates a function that retrieves this information from a digital media file.</span></span> <span data-ttu-id="b526a-118">Die Funktion übernimmt die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="b526a-118">The function takes the following parameters:</span></span>

-   <span data-ttu-id="b526a-119">*pmedia*.</span><span class="sxs-lookup"><span data-stu-id="b526a-119">*pMedia*.</span></span> <span data-ttu-id="b526a-120">Zeiger auf eine **iwmpmedia** -Schnittstelle, die die zu überprüfende digitale Mediendatei darstellt.</span><span class="sxs-lookup"><span data-stu-id="b526a-120">Pointer to an **IWMPMedia** interface that represents the digital media file to inspect.</span></span>
-   <span data-ttu-id="b526a-121">*lpsindex*:</span><span class="sxs-lookup"><span data-stu-id="b526a-121">*lPsIndex*.</span></span> <span data-ttu-id="b526a-122">Der Partnerschafts Index des aktuellen Geräts.</span><span class="sxs-lookup"><span data-stu-id="b526a-122">Partnership index of the current device.</span></span>
-   <span data-ttu-id="b526a-123">*pulondevice*.</span><span class="sxs-lookup"><span data-stu-id="b526a-123">*pulOnDevice*.</span></span> <span data-ttu-id="b526a-124">Zeiger auf eine **Long** -Variable, die den Wert empfängt, der angibt, ob die digitale Mediendatei auf das Gerät kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="b526a-124">Pointer to a **long** variable that receives the value indicating whether the digital media file has been copied to the device.</span></span>
-   <span data-ttu-id="b526a-125">*puldidnotfit*.</span><span class="sxs-lookup"><span data-stu-id="b526a-125">*pulDidNotFit*.</span></span> <span data-ttu-id="b526a-126">Zeiger auf eine **Long** -Variable, die den Wert empfängt, der angibt, ob der Kopiervorgang fehlgeschlagen ist, da das Gerät nicht über genügend Arbeitsspeicher verfügt.</span><span class="sxs-lookup"><span data-stu-id="b526a-126">Pointer to a **long** variable that receives the value indicating whether the copy operation failed because the device did not have enough memory.</span></span>

<span data-ttu-id="b526a-127">Die im **SyncState** -Attribut enthaltenen Informationen werden bitweise codiert.</span><span class="sxs-lookup"><span data-stu-id="b526a-127">The information contained in the **SyncState** attribute is encoded in a bitwise fashion.</span></span> <span data-ttu-id="b526a-128">Sie können sehen, wie diese Funktion im Beispielcode zum Auflisten [der Medienelemente](enumerating-the-media-items.md)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b526a-128">You can see how this function is used in the example code in [Enumerating the Media Items](enumerating-the-media-items.md).</span></span>


```C++
STDMETHODIMP CSyncSettings::GetPartnershipSyncState(IWMPMedia* pMedia, long lPsIndex, ULONG *pulOnDevice, ULONG *pulDidNotFit)
{
    ATLASSERT(pMedia); 
    ATLASSERT(lPsIndex > 0 && 
              lPsIndex < 17);
    ATLASSERT(pulOnDevice);
    ATLASSERT(pulDidNotFit);
  
    CComVariant varSyncStateVal;   
    CComPtr<IWMPMedia> spMedia(pMedia); 
    CComPtr<IWMPMedia3> spMedia3;     
    HRESULT hr = spMedia.QueryInterface(&spMedia3); 
    ULONG ulSyncState = 0; // Stores the ulVal member of varSyncStateVal. 
    ULONG lLSB = 0; // Represents least significant bit: Did the media fail to copy because it would not fit?
    ULONG lMSB = 0; // Represents most significant bit: Is the media on the device?

    // Calculate the bit shift required to isolate the partnership bit 
    // pair from the SyncState attribute.
    const int iRshift = (lPsIndex - 1) * 2;

    if(SUCCEEDED(hr) && spMedia3)
    {       
        hr = spMedia3->getItemInfoByType(CComBSTR("SyncState"), CComBSTR(""), 0, &varSyncStateVal);
    }

    if(SUCCEEDED(hr) && varSyncStateVal.vt == VT_UI4)
    {   
        // Get the value.
        ulSyncState = varSyncStateVal.ulVal;

        // Shift the bit pair to the rightmost position.
        ulSyncState >>= iRshift; 

        // Mask the rightmost bit pair.
        ulSyncState &= 3;

        // Get the LSB         
        lLSB = ulSyncState & ~2; // Sets the 2E1 bit to zero. 

        // Get the MSB
        ulSyncState >>= 1;
        lMSB = ulSyncState;       
    }

    // Return the bits.
    *pulOnDevice = lMSB;
    *pulDidNotFit = lLSB;

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="b526a-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b526a-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b526a-130">**Iwmpmedia-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b526a-130">**IWMPMedia Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[<span data-ttu-id="b526a-131">**IWMPMedia3:: getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="b526a-131">**IWMPMedia3::getItemInfoByType**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia3-getiteminfobytype)
</dt> <dt>

[<span data-ttu-id="b526a-132">**Synchronisierungs Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="b526a-132">**Managing Synchronization Playlists**</span></span>](managing-synchronization-playlists.md)
</dt> <dt>

[<span data-ttu-id="b526a-133">**SyncState-Attribut**</span><span class="sxs-lookup"><span data-stu-id="b526a-133">**SyncState Attribute**</span></span>](syncstate-attribute.md)
</dt> </dl>

 

 




