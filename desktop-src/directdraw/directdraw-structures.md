---
title: DirectDraw-Strukturen
description: Dieser Abschnitt enthält Informationen zu den folgenden in DirectDraw verwendeten Strukturen.
ms.assetid: 36424B41-B179-414A-ACFF-E63DA7B27043
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52cf24c71da3f022833c6ecf9843e996df2c514b
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "106340743"
---
# <a name="directdraw-structures"></a><span data-ttu-id="69e96-103">DirectDraw-Strukturen</span><span class="sxs-lookup"><span data-stu-id="69e96-103">DirectDraw Structures</span></span>

<span data-ttu-id="69e96-104">Dieser Abschnitt enthält Informationen zu den folgenden Strukturen, die mit DirectDraw verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="69e96-104">This section contains information about the following structures used with DirectDraw:</span></span>

-   [<span data-ttu-id="69e96-105">**Ddbltbatch**</span><span class="sxs-lookup"><span data-stu-id="69e96-105">**DDBLTBATCH**</span></span>](/windows/desktop/api/Ddraw/ns-ddraw-ddbltbatch)
-   [<span data-ttu-id="69e96-106">**Ddbltfx**</span><span class="sxs-lookup"><span data-stu-id="69e96-106">**DDBLTFX**</span></span>](/windows/desktop/api/Ddraw/ns-ddraw-ddbltfx)
-   [<span data-ttu-id="69e96-107">**Ddcaps**</span><span class="sxs-lookup"><span data-stu-id="69e96-107">**DDCAPS**</span></span>](/windows/desktop/api/Ddraw/ns-ddraw-ddcaps_dx3)
-   [<span data-ttu-id="69e96-108">**Ddcolorcontrol**</span><span class="sxs-lookup"><span data-stu-id="69e96-108">**DDCOLORCONTROL**</span></span>](/windows/win32/api/ddraw/nn-ddraw-idirectdrawcolorcontrol)
-   [<span data-ttu-id="69e96-109">**Ddcolorkey**</span><span class="sxs-lookup"><span data-stu-id="69e96-109">**DDCOLORKEY**</span></span>](/windows/desktop/api/Ddraw/ns-ddraw-ddcolorkey)
-   [<span data-ttu-id="69e96-110">**DDDEVICEIDENTIFIER2**</span><span class="sxs-lookup"><span data-stu-id="69e96-110">**DDDEVICEIDENTIFIER2**</span></span>](/windows/win32/api/ddraw/ns-ddraw-dddeviceidentifier2)
-   [<span data-ttu-id="69e96-111">**Ddgammaramp**</span><span class="sxs-lookup"><span data-stu-id="69e96-111">**DDGAMMARAMP**</span></span>](/windows/desktop/api/Ddraw/ns-ddraw-ddgammaramp)
-   [<span data-ttu-id="69e96-112">**Ddoverlayfx**</span><span class="sxs-lookup"><span data-stu-id="69e96-112">**DDOVERLAYFX**</span></span>](/windows/desktop/api/Ddraw/ns-ddraw-ddoverlayfx)
-   [<span data-ttu-id="69e96-113">**Ddpixelformat**</span><span class="sxs-lookup"><span data-stu-id="69e96-113">**DDPIXELFORMAT**</span></span>](/windows/desktop/api/Ddraw/ns-ddraw-ddpixelformat)
-   <span data-ttu-id="69e96-114">[**DDSCAPS**](/previous-versions/ms783271(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="69e96-114">[**DDSCAPS**](/previous-versions/ms783271(v=vs.85))</span></span>
-   <span data-ttu-id="69e96-115">[**DDSCAPS2**](/previous-versions/bb943980(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="69e96-115">[**DDSCAPS2**](/previous-versions/bb943980(v=vs.85))</span></span>
-   <span data-ttu-id="69e96-116">[**Ddsurfacede SC**](/previous-versions/ms783272(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="69e96-116">[**DDSURFACEDESC**](/previous-versions/ms783272(v=vs.85))</span></span>
-   <span data-ttu-id="69e96-117">[**DDSURFACEDESC2**](/previous-versions/bb943981(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="69e96-117">[**DDSURFACEDESC2**](/previous-versions/bb943981(v=vs.85))</span></span>

> [!Note]  
> <span data-ttu-id="69e96-118">Sie sollten den Arbeitsspeicher für jede DirectX-Struktur mit 0 initialisieren, bevor Sie die-Struktur verwenden.</span><span class="sxs-lookup"><span data-stu-id="69e96-118">You should initialize the memory for each DirectX structure to 0 before you use the structure.</span></span> <span data-ttu-id="69e96-119">Außerdem sollten Sie für alle Strukturen, die ein **dwSize** -Element enthalten, den-Member auf die Größe der-Struktur in Bytes festlegen, bevor die-Struktur verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="69e96-119">In addition, for all structures that contain a **dwSize** member, you should set the member to the size of the structure, in bytes, before the structure is used.</span></span> <span data-ttu-id="69e96-120">Im folgenden Beispiel werden diese Aufgaben für eine gemeinsame Struktur, [**ddcaps**](/windows/desktop/api/Ddraw/ns-ddraw-ddcaps_dx3), ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="69e96-120">The following example performs these tasks on a common structure, [**DDCAPS**](/windows/desktop/api/Ddraw/ns-ddraw-ddcaps_dx3):</span></span>

 


```
DDCAPS ddcaps; // You cannot use this yet.
 
ZeroMemory(&ddcaps, sizeof(DDCAPS));
ddcaps.dwSize = sizeof(DDCAPS);
 
// Now you can use the structure.
.
.
```



 

 




