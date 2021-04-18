---
title: Der RIP-Prozess wird gestartet.
description: Der RIP-Prozess wird gestartet.
ms.assetid: 82ffc114-ddad-41be-af80-6c1bd29cb0d4
keywords:
- Windows Media Player, CD-einreißen
- Windows Media Player-Objektmodell, CD-einreißen
- Objektmodell, CD-einreißen
- Windows Media Player ActiveX-Steuerelement, CD-einreißen
- ActiveX-Steuerelement, CD-einreißen
- Windows Media Player Mobile ActiveX-Steuerelement, CD-einreißen
- Windows Media Player Mobile, CD-einreißen
- CD-Ripping, Starten des RIP-Prozesses
- einreißen CDs, Starten des RIP-Prozesses
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2107b053abf8747d7add8fcedc26a2386ae5fd84
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106338241"
---
# <a name="starting-the-rip-process"></a><span data-ttu-id="795f0-112">Der RIP-Prozess wird gestartet.</span><span class="sxs-lookup"><span data-stu-id="795f0-112">Starting the Rip Process</span></span>

<span data-ttu-id="795f0-113">Nachdem Sie die rippingschnittstelle wie im vorherigen Abschnitt erläutert abgerufen haben, starten Sie den einreißen-Prozess, indem Sie [iwmpcdromrip:: startrip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-startrip)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="795f0-113">After you have retrieved the ripping interface as explained in the previous section, start the ripping process by calling [IWMPCdromRip::startRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-startrip).</span></span>


```C++
// Start ripping.
HRESULT hr = m_spCdromRip->startRip();

```



<span data-ttu-id="795f0-114">Sie können den einreißen-Vorgang beenden, indem Sie [iwmpcdromrip:: stoprip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-stoprip)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="795f0-114">You can stop the ripping operation by calling [IWMPCdromRip::stopRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-stoprip).</span></span>


```C++
// Stop ripping.
HRESULT hr = m_spCdromRip->stopRip();

```



## <a name="related-topics"></a><span data-ttu-id="795f0-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="795f0-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="795f0-116">**Ripping einer CD**</span><span class="sxs-lookup"><span data-stu-id="795f0-116">**Ripping a CD**</span></span>](ripping-a-cd.md)
</dt> <dt>

[<span data-ttu-id="795f0-117">**Abrufen der Rippingschnittstelle**</span><span class="sxs-lookup"><span data-stu-id="795f0-117">**Retrieving the Ripping Interface**</span></span>](retrieving-the-ripping-interface.md)
</dt> <dt>

[<span data-ttu-id="795f0-118">**Abrufen des Status "RIP"**</span><span class="sxs-lookup"><span data-stu-id="795f0-118">**Retrieving the Rip Status**</span></span>](retrieving-the-rip-status.md)
</dt> <dt>

[<span data-ttu-id="795f0-119">**Auswählen von Elementen für das Ripping**</span><span class="sxs-lookup"><span data-stu-id="795f0-119">**Selecting Items for Ripping**</span></span>](selecting-items-for-ripping.md)
</dt> </dl>

 

 




