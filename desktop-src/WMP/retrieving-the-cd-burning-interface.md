---
title: Abrufen der Schnittstelle zum Brennen von CDs
description: Abrufen der Schnittstelle zum Brennen von CDs
ms.assetid: d52f7b27-a327-4656-8dc2-0b075264d295
keywords:
- Windows Media Player, CD-brennen
- Windows Media Player-Objektmodell, CD-brennen
- Objektmodell, CD-brennen
- Windows Media Player ActiveX-Steuerelement, CD-brennen
- ActiveX-Steuerelement, CD-brennen
- Windows Media Player Mobile ActiveX-Steuerelement, CD-brennen
- Windows Media Player Mobile, CD-brennen
- CD-brennen, Abrufen der iwmpcdromcollection-Schnittstelle
- Brennen von CDs, Abrufen der iwmpcdromcollection-Schnittstelle
- Iwmpcdromcollection-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b63763f9dd99bbaf88ae099edb53ba072cd1a25e
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104038671"
---
# <a name="retrieving-the-cd-burning-interface"></a><span data-ttu-id="4232b-113">Abrufen der Schnittstelle zum Brennen von CDs</span><span class="sxs-lookup"><span data-stu-id="4232b-113">Retrieving the CD Burning Interface</span></span>

<span data-ttu-id="4232b-114">Um die CD-Laufwerke auf dem Computer des Benutzers aufzulisten, verwenden Sie die **iwmpcdromcollection** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="4232b-114">To enumerate the CD drives on the user's computer, use the **IWMPCdromCollection** interface.</span></span> <span data-ttu-id="4232b-115">Sie rufen einen Zeiger auf diese Schnittstelle ab, indem Sie [iwmpcore:: get \_ cdromcollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4232b-115">You retrieve a pointer to this interface by calling [IWMPCore::get\_cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection).</span></span>

<span data-ttu-id="4232b-116">Mithilfe der **get \_ count** -und **Item** -Methoden können Sie die Auflistung durchlaufen, um einen [iwmpcdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) -Schnittstellen Zeiger für jedes CD-Laufwerk auf dem Computer des Benutzers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4232b-116">By using the **get\_count** and **item** methods, you can iterate the collection to retrieve an [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) interface pointer for each CD drive on the user's computer.</span></span>

<span data-ttu-id="4232b-117">Die **iwmpcdrom** -Schnittstelle stellt ein einzelnes CD-Laufwerk dar.</span><span class="sxs-lookup"><span data-stu-id="4232b-117">The **IWMPCdrom** interface represents an individual CD drive.</span></span> <span data-ttu-id="4232b-118">Bevor Sie mit dem Brennen einer CD beginnen, müssen Sie zuerst **QueryInterface** über einen **iwmpcdrom** -Zeiger aufrufen, um einen Zeiger auf die [iwmpcdromburn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) -Schnittstelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4232b-118">Before you begin burning a CD, you must first call **QueryInterface** through an **IWMPCdrom** pointer to retrieve a pointer to the [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) interface.</span></span>

<span data-ttu-id="4232b-119">Im folgenden Codebeispiel wird veranschaulicht, wie Sie eine Schnittstelle zum Brennen einer CD auf einem bestimmten Laufwerk abrufen:</span><span class="sxs-lookup"><span data-stu-id="4232b-119">The following code example demonstrates how to retrieve an interface for burning a CD to a specific drive:</span></span>


```C++
HRESULT CMainDlg::GetCdromDriveCount (long &lDriveCount)
{
    hr = m_spPlayer->get_cdromCollection(&m_spCdromCollection);

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
HRESULT CMainDlg::GetCdromBurnInterface (long lIndex)
{
    // Get the IWMPCdrom interface.
    m_spCdrom.Release();
    HRESULT hr = m_spCdromCollection->item(lIndex, &m_spCdrom);
    if (SUCCEEDED(hr))
    {
        // Get the IWMPCdromBurn interface.
        m_spCdromBurn.Release();
        hr = m_spCdrom->QueryInterface(&m_spCdromBurn);
    }

    return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="4232b-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4232b-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4232b-121">**Brennen einer CD**</span><span class="sxs-lookup"><span data-stu-id="4232b-121">**Burning a CD**</span></span>](burning-a-cd.md)
</dt> <dt>

[<span data-ttu-id="4232b-122">**Der Verbrennungsprozess wird gestartet.**</span><span class="sxs-lookup"><span data-stu-id="4232b-122">**Starting the Burn Process**</span></span>](starting-the-burn-process.md)
</dt> <dt>

[<span data-ttu-id="4232b-123">**Löschen einer erneut beschreibbaren CD**</span><span class="sxs-lookup"><span data-stu-id="4232b-123">**Erasing a Rewritable CD**</span></span>](erasing-a-rewritable-cd.md)
</dt> <dt>

[<span data-ttu-id="4232b-124">**Abrufen des Laufwerks und des Festplatten Status**</span><span class="sxs-lookup"><span data-stu-id="4232b-124">**Retrieving the Drive and Disc Status**</span></span>](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[<span data-ttu-id="4232b-125">**Abrufen des Verbrauchs Status**</span><span class="sxs-lookup"><span data-stu-id="4232b-125">**Retrieving the Burn Status**</span></span>](retrieving-the-burn-status.md)
</dt> <dt>

[<span data-ttu-id="4232b-126">**Iwmpcdromcollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="4232b-126">**IWMPCdromCollection Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> </dl>

 

 




