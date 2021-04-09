---
title: Abrufen des Laufwerks und des Festplatten Status
description: Abrufen des Laufwerks und des Festplatten Status
ms.assetid: 5e3e6107-d2bc-450c-a86e-5d3ef7b3092a
keywords:
- Windows Media Player, CD-brennen
- Windows Media Player-Objektmodell, CD-brennen
- Objektmodell, CD-brennen
- Windows Media Player ActiveX-Steuerelement, CD-brennen
- ActiveX-Steuerelement, CD-brennen
- Windows Media Player Mobile ActiveX-Steuerelement, CD-brennen
- Windows Media Player Mobile, CD-brennen
- CD-brennen, Abrufen von Laufwerk-und Festplatten Status
- Brennen von CDs, Abrufen von Laufwerks-und Festplatten Status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eab66581c336f642fd53b22f81949847d0a1c89
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103858024"
---
# <a name="retrieving-the-drive-and-disc-status"></a><span data-ttu-id="32699-112">Abrufen des Laufwerks und des Festplatten Status</span><span class="sxs-lookup"><span data-stu-id="32699-112">Retrieving the Drive and Disc Status</span></span>

<span data-ttu-id="32699-113">Vor dem Starten eines CD-Brennvorgangs müssen Sie sicherstellen, dass das ausgewählte CD-ROM-Laufwerk den Vorgang unterstützt, den Sie ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="32699-113">Before starting a CD burning operation, you must ensure that the selected CD-ROM drive supports the operation you want to perform.</span></span> <span data-ttu-id="32699-114">Beispielsweise müssen Sie überprüfen, ob eine CD gelöscht werden kann, bevor Sie [iwmpcdromburn:: Erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="32699-114">For instance, you must check that a CD is capable of being erased before calling [IWMPCdromBurn::erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase).</span></span> <span data-ttu-id="32699-115">Der folgende Code zeigt ein Beispiel für die Verwendung von [iwmpcdromburn:: IsAvailable](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-isavailable) , um zu bestimmen, ob ein Vorgang unterstützt wird:</span><span class="sxs-lookup"><span data-stu-id="32699-115">The following code shows an example of using [IWMPCdromBurn::isAvailable](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-isavailable) to determine whether an operation is supported:</span></span>


```C++
VARIANT_BOOL vbResult;
    
// Check whether this drive can burn CDs.
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("Burn");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->isAvailable(bstrItem, &vbResult);
}
if (SUCCEEDED(hr))
{
    if (VARIANT_TRUE == vbResult)
    {
        // The current drive can burn CDs.
    }
}

```



## <a name="related-topics"></a><span data-ttu-id="32699-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="32699-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32699-117">**Brennen einer CD**</span><span class="sxs-lookup"><span data-stu-id="32699-117">**Burning a CD**</span></span>](burning-a-cd.md)
</dt> <dt>

[<span data-ttu-id="32699-118">**Abrufen der Schnittstelle zum Brennen von CDs**</span><span class="sxs-lookup"><span data-stu-id="32699-118">**Retrieving the CD Burning Interface**</span></span>](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[<span data-ttu-id="32699-119">**Der Verbrennungsprozess wird gestartet.**</span><span class="sxs-lookup"><span data-stu-id="32699-119">**Starting the Burn Process**</span></span>](starting-the-burn-process.md)
</dt> <dt>

[<span data-ttu-id="32699-120">**Löschen einer erneut beschreibbaren CD**</span><span class="sxs-lookup"><span data-stu-id="32699-120">**Erasing a Rewritable CD**</span></span>](erasing-a-rewritable-cd.md)
</dt> <dt>

[<span data-ttu-id="32699-121">**Abrufen des Verbrauchs Status**</span><span class="sxs-lookup"><span data-stu-id="32699-121">**Retrieving the Burn Status**</span></span>](retrieving-the-burn-status.md)
</dt> </dl>

 

 




