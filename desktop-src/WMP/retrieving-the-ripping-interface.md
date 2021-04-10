---
title: Abrufen der Rippingschnittstelle
description: Abrufen der Rippingschnittstelle
ms.assetid: 760610eb-e356-4b50-b865-53557ba9b815
keywords:
- Windows Media Player, CD-einreißen
- Windows Media Player-Objektmodell, CD-einreißen
- Objektmodell, CD-einreißen
- Windows Media Player ActiveX-Steuerelement, CD-einreißen
- ActiveX-Steuerelement, CD-einreißen
- Windows Media Player Mobile ActiveX-Steuerelement, CD-einreißen
- Windows Media Player Mobile, CD-einreißen
- CD-Ripping, iwmpcdromrip-Schnittstelle
- einreißen CDs, iwmpcdromrip-Schnittstelle
- Iwmpcdromrip-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 903fa285404700e35363a94239c79706e7af0e34
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "103858076"
---
# <a name="retrieving-the-ripping-interface"></a><span data-ttu-id="e7383-113">Abrufen der Rippingschnittstelle</span><span class="sxs-lookup"><span data-stu-id="e7383-113">Retrieving the Ripping Interface</span></span>

<span data-ttu-id="e7383-114">Um die CD-Laufwerke auf dem Computer des Benutzers aufzulisten, verwenden Sie die **iwmpcdromcollection** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e7383-114">To enumerate the CD drives on the user's computer, use the **IWMPCdromCollection** interface.</span></span> <span data-ttu-id="e7383-115">Rufen Sie einen Zeiger auf diese Schnittstelle ab, indem [Sie iwmpcore:: get \_ cdromcollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e7383-115">Retrieve a pointer to this interface by calling [IWMPCore::get\_cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection).</span></span>

<span data-ttu-id="e7383-116">Mithilfe der [get \_ count](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-get_count) -und [Item](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-item) -Methoden können Sie die Auflistung durchlaufen, um eine [iwmpcdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) -Schnittstelle für jedes CD-Laufwerk auf dem Computer des Benutzers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e7383-116">By using the [get\_count](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-get_count) and [item](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-item) methods, you can iterate the collection to retrieve an [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) interface for each CD drive on the user's computer.</span></span>

<span data-ttu-id="e7383-117">Die **iwmpcdrom** -Schnittstelle stellt ein einzelnes CD-Laufwerk dar.</span><span class="sxs-lookup"><span data-stu-id="e7383-117">The **IWMPCdrom** interface represents an individual CD drive.</span></span> <span data-ttu-id="e7383-118">Bevor Sie mit dem Einreißen einer CD beginnen, müssen Sie zuerst **QueryInterface** über einen **iwmpcdrom** -Zeiger aufrufen, um die [iwmpcdromrip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) -Schnittstelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e7383-118">Before you begin ripping a CD, you must first call **QueryInterface** through an **IWMPCdrom** pointer to retrieve the [IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) interface.</span></span>

<span data-ttu-id="e7383-119">Im folgenden Codebeispiel wird veranschaulicht, wie Sie eine Schnittstelle zum einreißen einer CD von einem bestimmten Laufwerk abrufen:</span><span class="sxs-lookup"><span data-stu-id="e7383-119">The following code example demonstrates how to retrieve an interface for ripping a CD from a specific drive:</span></span>


```C++
HRESULT CMainDlg::GetCdromDriveCount (long &lDriveCount)
{
    HRESULT hr = m_spPlayer->get_cdromCollection(&m_spCdromCollection);

    // Get the number of CDROM drives.
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromCollection->get_count(&lDriveCount);
    }

    return hr;
}

// lIndex refers to the index of the current drive,
// which must be less than the value retrieved by
// GetCdromDriveCount above.
HRESULT CMainDlg::GetCdromRipInterface (long lIndex)
{
    // Get the IWMPCdrom interface.
    m_spCdrom.Release();
    HRESULT hr = m_spCdromCollection->item(lIndex, &m_spCdrom);
    if (SUCCEEDED(hr))
    {
        // Get the IWMPCdromRip interface.
        m_spCdromRip.Release();
        hr = m_spCdrom->QueryInterface(&m_spCdromRip);
    }

    return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="e7383-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e7383-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7383-121">**Ripping einer CD**</span><span class="sxs-lookup"><span data-stu-id="e7383-121">**Ripping a CD**</span></span>](ripping-a-cd.md)
</dt> <dt>

[<span data-ttu-id="e7383-122">**Der RIP-Prozess wird gestartet.**</span><span class="sxs-lookup"><span data-stu-id="e7383-122">**Starting the Rip Process**</span></span>](starting-the-rip-process.md)
</dt> <dt>

[<span data-ttu-id="e7383-123">**Abrufen des Status "RIP"**</span><span class="sxs-lookup"><span data-stu-id="e7383-123">**Retrieving the Rip Status**</span></span>](retrieving-the-rip-status.md)
</dt> <dt>

[<span data-ttu-id="e7383-124">**Auswählen von Elementen für das Ripping**</span><span class="sxs-lookup"><span data-stu-id="e7383-124">**Selecting Items for Ripping**</span></span>](selecting-items-for-ripping.md)
</dt> <dt>

[<span data-ttu-id="e7383-125">**Iwmpcdromcollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="e7383-125">**IWMPCdromCollection Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> </dl>

 

 




