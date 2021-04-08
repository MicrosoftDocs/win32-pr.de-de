---
title: Ripping einer CD
description: Ripping einer CD
ms.assetid: f5c1b5bf-d616-48cb-8690-e0237c56e402
keywords:
- Windows Media Player, CD-einreißen
- Windows Media Player-Objektmodell, CD-einreißen
- Objektmodell, CD-einreißen
- Windows Media Player ActiveX-Steuerelement, CD-einreißen
- ActiveX-Steuerelement, CD-einreißen
- Windows Media Player Mobile ActiveX-Steuerelement, CD-einreißen
- Windows Media Player Mobile, CD-einreißen
- CD-Ripping, Info
- einreißen CDs, Info
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 767734b3449fd0a64b31c8f351406bbf9f6c805b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856572"
---
# <a name="ripping-a-cd"></a><span data-ttu-id="e0dc4-112">Ripping einer CD</span><span class="sxs-lookup"><span data-stu-id="e0dc4-112">Ripping a CD</span></span>

<span data-ttu-id="e0dc4-113">Es gibt zwei Möglichkeiten, eine CD mit dem Windows Media Player-Steuerelement zu zerreißen.</span><span class="sxs-lookup"><span data-stu-id="e0dc4-113">There are two ways to rip a CD by using the Windows Media Player control.</span></span> <span data-ttu-id="e0dc4-114">Windows Media Player 9 kann CDs mithilfe von **iwmpplayerservices:: settaskpane** zerreißen.</span><span class="sxs-lookup"><span data-stu-id="e0dc4-114">Windows Media Player 9 can rip CDs by using **IWMPPlayerServices::setTaskPane**.</span></span> <span data-ttu-id="e0dc4-115">Windows Media Player 11 führt die **iwmpcdromrip** -Schnittstelle für das einreißen von CDs ein.</span><span class="sxs-lookup"><span data-stu-id="e0dc4-115">Windows Media Player 11 introduces the **IWMPCdromRip** interface for ripping CDs.</span></span> <span data-ttu-id="e0dc4-116">Diese Schnittstelle bietet mehr Funktionalität als **iwmpplayerservices:: settaskpane**, und es wird empfohlen, dass Sie **iwmpcdromrip** verwenden, wenn es verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="e0dc4-116">This interface provides more functionality than **IWMPPlayerServices::setTaskPane**, and it is recommended that you use **IWMPCdromRip** if it is available.</span></span>

<span data-ttu-id="e0dc4-117">In den folgenden Abschnitten wird beschrieben, wie Sie eine CD mithilfe von Windows Media Player zerreißen.</span><span class="sxs-lookup"><span data-stu-id="e0dc4-117">The following sections describe how to rip a CD by using Windows Media Player.</span></span>

-   [<span data-ttu-id="e0dc4-118">Ripping mithilfe der iwmpcdromrip-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="e0dc4-118">Ripping by Using the IWMPCdromRip Interface</span></span>](ripping-by-using-the-iwmpcdromrip-interface.md)
-   [<span data-ttu-id="e0dc4-119">Ripping mithilfe von iwmpplayerservices:: settaskpane</span><span class="sxs-lookup"><span data-stu-id="e0dc4-119">Ripping by Using IWMPPlayerServices::setTaskPane</span></span>](ripping-by-using-iwmpplayerservices--settaskpane.md)

## <a name="related-topics"></a><span data-ttu-id="e0dc4-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e0dc4-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0dc4-121">**Player-Steuerelement Handbuch**</span><span class="sxs-lookup"><span data-stu-id="e0dc4-121">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




