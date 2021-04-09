---
title: Löschen einer erneut beschreibbaren CD
description: Löschen einer erneut beschreibbaren CD
ms.assetid: 272fdd2b-c174-4bde-b05e-839d547532a6
keywords:
- Windows Media Player, CD-brennen
- Windows Media Player-Objektmodell, CD-brennen
- Objektmodell, CD-brennen
- Windows Media Player ActiveX-Steuerelement, CD-brennen
- ActiveX-Steuerelement, CD-brennen
- Windows Media Player Mobile ActiveX-Steuerelement, CD-brennen
- Windows Media Player Mobile, CD-brennen
- CD-brennen, Löschen von rebeschreib baren CDs
- Brennen von CDs, Löschen von rebeschreib baren CDs
- Löschen von wieder beschreibbaren CDs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7025b7cd70c86c0b832aa792e50a8a2c64e7f45
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038556"
---
# <a name="erasing-a-rewritable-cd"></a><span data-ttu-id="b5b74-113">Löschen einer erneut beschreibbaren CD</span><span class="sxs-lookup"><span data-stu-id="b5b74-113">Erasing a Rewritable CD</span></span>

<span data-ttu-id="b5b74-114">Die [iwmpcdromburn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) -Schnittstelle stellt eine Methode zum Löschen von CD-RW-CDs bereit.</span><span class="sxs-lookup"><span data-stu-id="b5b74-114">The [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) interface provides a method for erasing CD-RW discs.</span></span> <span data-ttu-id="b5b74-115">Bevor Sie eine CD löschen, müssen Sie zunächst sicherstellen, dass der Vorgang unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="b5b74-115">Before erasing a CD, you must first ensure that the operation is supported.</span></span> <span data-ttu-id="b5b74-116">Weitere Informationen finden Sie unter [Abrufen des Laufwerks und des Festplatten Status](retrieving-the-drive-and-disc-status.md).</span><span class="sxs-lookup"><span data-stu-id="b5b74-116">For more information, see [Retrieving the Drive and Disc Status](retrieving-the-drive-and-disc-status.md).</span></span>

<span data-ttu-id="b5b74-117">Um mit dem Löschen des Inhalts einer erneut beschreibbaren CD zu beginnen, nennen Sie [iwmpcdromburn:: Erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase).</span><span class="sxs-lookup"><span data-stu-id="b5b74-117">To begin erasing the contents of a rewritable CD, call [IWMPCdromBurn::erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase).</span></span>


```C++

    HRESULT hr = m_spCdromBurn->erase();
    

```



## <a name="related-topics"></a><span data-ttu-id="b5b74-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b5b74-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5b74-119">**Brennen einer CD**</span><span class="sxs-lookup"><span data-stu-id="b5b74-119">**Burning a CD**</span></span>](burning-a-cd.md)
</dt> <dt>

[<span data-ttu-id="b5b74-120">**Abrufen der Schnittstelle zum Brennen von CDs**</span><span class="sxs-lookup"><span data-stu-id="b5b74-120">**Retrieving the CD Burning Interface**</span></span>](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[<span data-ttu-id="b5b74-121">**Der Verbrennungsprozess wird gestartet.**</span><span class="sxs-lookup"><span data-stu-id="b5b74-121">**Starting the Burn Process**</span></span>](starting-the-burn-process.md)
</dt> <dt>

[<span data-ttu-id="b5b74-122">**Abrufen des Laufwerks und des Festplatten Status**</span><span class="sxs-lookup"><span data-stu-id="b5b74-122">**Retrieving the Drive and Disc Status**</span></span>](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[<span data-ttu-id="b5b74-123">**Abrufen des Verbrauchs Status**</span><span class="sxs-lookup"><span data-stu-id="b5b74-123">**Retrieving the Burn Status**</span></span>](retrieving-the-burn-status.md)
</dt> </dl>

 

 




