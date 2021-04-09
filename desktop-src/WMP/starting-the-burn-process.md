---
title: Der Verbrennungsprozess wird gestartet.
description: Der Verbrennungsprozess wird gestartet.
ms.assetid: 91442bd2-1a68-465c-b865-63d309f33d55
keywords:
- Windows Media Player, CD-brennen
- Windows Media Player-Objektmodell, CD-brennen
- Objektmodell, CD-brennen
- Windows Media Player ActiveX-Steuerelement, CD-brennen
- ActiveX-Steuerelement, CD-brennen
- Windows Media Player Mobile ActiveX-Steuerelement, CD-brennen
- Windows Media Player Mobile, CD-brennen
- CD-brennen, Startvorgang zum Brennen
- Brennen von CDs, Starten des Brennvorgangs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4a35f473eebe35bffd48ac802dcfe79082689de
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103948446"
---
# <a name="starting-the-burn-process"></a><span data-ttu-id="39990-112">Der Verbrennungsprozess wird gestartet.</span><span class="sxs-lookup"><span data-stu-id="39990-112">Starting the Burn Process</span></span>

<span data-ttu-id="39990-113">Bevor Sie beginnen können, müssen Sie eine Wiedergabeliste zum Brennen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="39990-113">Before burning can begin, you must assign a playlist to be burned.</span></span> <span data-ttu-id="39990-114">Verwenden Sie [iwmpcdromburn::p UT \_ burnwiedergabe](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnplaylist) , um eine Wiedergabeliste zum Brennen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="39990-114">Use [IWMPCdromBurn::put\_burnPlaylist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnplaylist) to specify a playlist for burning.</span></span>


```C++
HRESULT CMainDlg::PutPlaylist (void)
{
    // Specify the burn playlist.   
    HRESULT hr = m_spCdromBurn->put_burnPlaylist(m_spPlaylist);

    // Update the status information.
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromBurn->refreshStatus();
    }

    return hr;
}

```



<span data-ttu-id="39990-115">Weitere Informationen zum Verwenden von Wiedergabelisten finden Sie unter [iwmpwiedergabe](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist).</span><span class="sxs-lookup"><span data-stu-id="39990-115">For information about using playlists, see [IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist).</span></span>

<span data-ttu-id="39990-116">Um den Brennvorgang zu starten, nennen Sie [iwmpcdromburn:: startburn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-startburn).</span><span class="sxs-lookup"><span data-stu-id="39990-116">To start the burning operation, call [IWMPCdromBurn::startBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-startburn).</span></span>


```C++
// Start burning.
hr = m_spCdromBurn->startBurn();

```



<span data-ttu-id="39990-117">Sie können den Brennvorgang beenden, indem Sie [iwmpcdromburn:: stopburn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-stopburn)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="39990-117">You can stop the burning operation by calling [IWMPCdromBurn::stopBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-stopburn).</span></span>


```C++
// Stop burning.
hr = m_spCdromBurn->stopBurn();

```



## <a name="related-topics"></a><span data-ttu-id="39990-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="39990-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39990-119">**Brennen einer CD**</span><span class="sxs-lookup"><span data-stu-id="39990-119">**Burning a CD**</span></span>](burning-a-cd.md)
</dt> <dt>

[<span data-ttu-id="39990-120">**Abrufen der Schnittstelle zum Brennen von CDs**</span><span class="sxs-lookup"><span data-stu-id="39990-120">**Retrieving the CD Burning Interface**</span></span>](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[<span data-ttu-id="39990-121">**Löschen einer erneut beschreibbaren CD**</span><span class="sxs-lookup"><span data-stu-id="39990-121">**Erasing a Rewritable CD**</span></span>](erasing-a-rewritable-cd.md)
</dt> <dt>

[<span data-ttu-id="39990-122">**Abrufen des Laufwerks und des Festplatten Status**</span><span class="sxs-lookup"><span data-stu-id="39990-122">**Retrieving the Drive and Disc Status**</span></span>](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[<span data-ttu-id="39990-123">**Abrufen des Verbrauchs Status**</span><span class="sxs-lookup"><span data-stu-id="39990-123">**Retrieving the Burn Status**</span></span>](retrieving-the-burn-status.md)
</dt> </dl>

 

 




