---
title: Brennen einer CD
description: Brennen einer CD
ms.assetid: df55479e-d8a7-443d-bf2c-c988bfd0b1be
keywords:
- Windows Media Player, CD-brennen
- Windows Media Player-Objektmodell, CD-brennen
- Objektmodell, CD-brennen
- Windows Media Player ActiveX-Steuerelement, CD-brennen
- ActiveX-Steuerelement, CD-brennen
- Windows Media Player Mobile ActiveX-Steuerelement, CD-brennen
- Windows Media Player Mobile, CD-brennen
- CD-brennen, Informationen zu
- Brennen von CDs, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 007b7808ff375ab0673592d0d016f8e713321d1a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104101274"
---
# <a name="burning-a-cd"></a><span data-ttu-id="136a7-112">Brennen einer CD</span><span class="sxs-lookup"><span data-stu-id="136a7-112">Burning a CD</span></span>

<span data-ttu-id="136a7-113">In diesem Abschnitt wird beschrieben, wie Sie die [iwmpcdromburn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) -Schnittstelle verwenden, um Musik auf eine CD zu brennen.</span><span class="sxs-lookup"><span data-stu-id="136a7-113">This section describes how to use the [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) interface to burn music to a CD.</span></span> <span data-ttu-id="136a7-114">Die **iwmpcdromburn** -Schnittstelle bietet Funktionen zum Brennen von Wiedergabelisten auf CDs als Daten-und Audiospuren sowie zum Löschen von CD-RWs.</span><span class="sxs-lookup"><span data-stu-id="136a7-114">The **IWMPCdromBurn** interface provides functionality for burning playlists to CDs as either data or audio tracks, as well as erasing CD-RWs.</span></span>

<span data-ttu-id="136a7-115">Code Verwendung</span><span class="sxs-lookup"><span data-stu-id="136a7-115">Code Usage</span></span>

<span data-ttu-id="136a7-116">Die Codebeispiele in diesem Abschnitt verwenden Active Template Library (ATL)-Klassen, wie z. b. **CComPtr**.</span><span class="sxs-lookup"><span data-stu-id="136a7-116">The code examples in this section use Active Template Library (ATL) classes, such as **CComPtr**.</span></span>

<span data-ttu-id="136a7-117">Enthaltene Header</span><span class="sxs-lookup"><span data-stu-id="136a7-117">Included Headers</span></span>

<span data-ttu-id="136a7-118">Um den Code in diesem Abschnitt zu verwenden, schließen Sie die folgenden Header ein:</span><span class="sxs-lookup"><span data-stu-id="136a7-118">To use the code in this section, include the following headers:</span></span>


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"

```



<span data-ttu-id="136a7-119">Schnittstellen Zeiger</span><span class="sxs-lookup"><span data-stu-id="136a7-119">Interface Pointers</span></span>

<span data-ttu-id="136a7-120">Die Schnittstellen für Windows-Media Player werden in den folgenden Element Variablen gespeichert:</span><span class="sxs-lookup"><span data-stu-id="136a7-120">The interfaces for Windows Media Player are stored in the following member variables:</span></span>


```C++
// Player interface.
CComPtr<IWMPPlayer>             m_spPlayer;

// CDROM interfaces.
CComPtr<IWMPCdromCollection>    m_spCdromCollection;
CComPtr<IWMPCdrom>              m_spCdrom;
CComPtr<IWMPCdromBurn>          m_spCdromBurn;
CComPtr<IWMPPlaylist>           m_spPlaylist;

```



<span data-ttu-id="136a7-121">In den folgenden Themen wird die Verwendung der CD-brennen-API beschrieben.</span><span class="sxs-lookup"><span data-stu-id="136a7-121">The following topics describe how to use the CD burning API.</span></span>

-   [<span data-ttu-id="136a7-122">Abrufen der Schnittstelle zum Brennen von CDs</span><span class="sxs-lookup"><span data-stu-id="136a7-122">Retrieving the CD Burning Interface</span></span>](retrieving-the-cd-burning-interface.md)
-   [<span data-ttu-id="136a7-123">Der Verbrennungsprozess wird gestartet.</span><span class="sxs-lookup"><span data-stu-id="136a7-123">Starting the Burn Process</span></span>](starting-the-burn-process.md)
-   [<span data-ttu-id="136a7-124">Löschen einer erneut beschreibbaren CD</span><span class="sxs-lookup"><span data-stu-id="136a7-124">Erasing a Rewritable CD</span></span>](erasing-a-rewritable-cd.md)
-   [<span data-ttu-id="136a7-125">Abrufen des Laufwerks und des Festplatten Status</span><span class="sxs-lookup"><span data-stu-id="136a7-125">Retrieving the Drive and Disc Status</span></span>](retrieving-the-drive-and-disc-status.md)
-   [<span data-ttu-id="136a7-126">Abrufen des Verbrauchs Status</span><span class="sxs-lookup"><span data-stu-id="136a7-126">Retrieving the Burn Status</span></span>](retrieving-the-burn-status.md)

## <a name="related-topics"></a><span data-ttu-id="136a7-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="136a7-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="136a7-128">**Player-Steuerelement Handbuch**</span><span class="sxs-lookup"><span data-stu-id="136a7-128">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




