---
title: Ripping mithilfe der iwmpcdromrip-Schnittstelle
description: Ripping mithilfe der iwmpcdromrip-Schnittstelle
ms.assetid: 7622072e-82e1-4e31-ad80-ddc3473b5841
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
ms.openlocfilehash: 4fcf2e959d10385365075bb20e1c04c2d796ad2e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103858023"
---
# <a name="ripping-by-using-the-iwmpcdromrip-interface"></a><span data-ttu-id="bbedd-113">Ripping mithilfe der iwmpcdromrip-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="bbedd-113">Ripping by Using the IWMPCdromRip Interface</span></span>

<span data-ttu-id="bbedd-114">In diesem Abschnitt wird beschrieben, wie Sie die [iwmpcdromrip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) -Schnittstelle verwenden, um Musik von einer CD zu zerreißen.</span><span class="sxs-lookup"><span data-stu-id="bbedd-114">This section describes how to use the [IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) interface to rip music from a CD.</span></span>

<span data-ttu-id="bbedd-115">Das einreißen einer CD mithilfe der **iwmpcdromrip** -Schnittstelle hat die gleiche Wirkung wie das einreißen von Musik mithilfe der Windows Media Player-Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="bbedd-115">Ripping a CD by using the **IWMPCdromRip** interface has the same effect as ripping music by using the Windows Media Player user interface.</span></span> <span data-ttu-id="bbedd-116">Ausgerigter Inhalt wird der Bibliothek automatisch entsprechend den Einstellungen des Benutzers hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bbedd-116">Ripped content is automatically added to the library according to the user's preferences.</span></span> <span data-ttu-id="bbedd-117">Weitere Informationen zum CD-Ripping finden Sie unter "Ripping Music from CDs" in der Windows Media Player-Hilfe.</span><span class="sxs-lookup"><span data-stu-id="bbedd-117">For more information about CD ripping, see "Ripping music from CDs" in Windows Media Player Help.</span></span>

<span data-ttu-id="bbedd-118">Die Codebeispiele in diesem Abschnitt verwenden Active Template Library (ATL)-Klassen, wie z. b. **CComPtr**.</span><span class="sxs-lookup"><span data-stu-id="bbedd-118">The code examples in this section use Active Template Library (ATL) classes, such as **CComPtr**.</span></span>

## <a name="included-headers"></a><span data-ttu-id="bbedd-119">Enthaltene Header</span><span class="sxs-lookup"><span data-stu-id="bbedd-119">Included Headers</span></span>

<span data-ttu-id="bbedd-120">Um den Code in diesem Abschnitt zu verwenden, schließen Sie die folgenden Header ein:</span><span class="sxs-lookup"><span data-stu-id="bbedd-120">To use the code in this section, include the following headers:</span></span>


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"

```



## <a name="interface-pointers"></a><span data-ttu-id="bbedd-121">Schnittstellen Zeiger</span><span class="sxs-lookup"><span data-stu-id="bbedd-121">Interface Pointers</span></span>

<span data-ttu-id="bbedd-122">Die Schnittstellen für Windows-Media Player werden in den folgenden Element Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="bbedd-122">The interfaces for Windows Media Player are stored in the following member variables.</span></span>


```C++
// Player interface.
CComPtr<IWMPPlayer>             m_spPlayer;

// CDROM interfaces.
CComPtr<IWMPCdromCollection>    m_spCdromCollection;
CComPtr<IWMPCdrom>              m_spCdrom;
CComPtr<IWMPCdromRip>           m_spCdromRip;
CComPtr<IWMPPlaylist>           m_spPlaylist;

```



<span data-ttu-id="bbedd-123">In den folgenden Abschnitten wird die Verwendung der iwmpcdromrip-Schnittstelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="bbedd-123">The Following Sections Describe How to Use the IWMPCdromRip Interface</span></span>

-   [<span data-ttu-id="bbedd-124">Abrufen der Rippingschnittstelle</span><span class="sxs-lookup"><span data-stu-id="bbedd-124">Retrieving the Ripping Interface</span></span>](retrieving-the-ripping-interface.md)
-   [<span data-ttu-id="bbedd-125">Der RIP-Prozess wird gestartet.</span><span class="sxs-lookup"><span data-stu-id="bbedd-125">Starting the Rip Process</span></span>](starting-the-rip-process.md)
-   [<span data-ttu-id="bbedd-126">Abrufen des Status "RIP"</span><span class="sxs-lookup"><span data-stu-id="bbedd-126">Retrieving the Rip Status</span></span>](retrieving-the-rip-status.md)
-   [<span data-ttu-id="bbedd-127">Auswählen von Elementen für das Ripping</span><span class="sxs-lookup"><span data-stu-id="bbedd-127">Selecting Items for Ripping</span></span>](selecting-items-for-ripping.md)

 

 




