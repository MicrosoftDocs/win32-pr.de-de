---
description: Das umgebende Rechteck aller Monitore ist der virtuelle Bildschirm. Der Desktop deckt den virtuellen Bildschirm anstelle eines einzelnen Monitors ab. Die folgende Abbildung zeigt eine mögliche Anordnung von drei Monitoren.
ms.assetid: 3f84027d-f316-4454-92ad-2d36d10b2ec8
title: Der virtuelle Bildschirm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4550ab0f849b90523842e6cc4e093c238ff11cbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995126"
---
# <a name="the-virtual-screen"></a><span data-ttu-id="ab194-105">Der virtuelle Bildschirm</span><span class="sxs-lookup"><span data-stu-id="ab194-105">The Virtual Screen</span></span>

<span data-ttu-id="ab194-106">Das umgebende Rechteck aller Monitore ist der *virtuelle Bildschirm*.</span><span class="sxs-lookup"><span data-stu-id="ab194-106">The bounding rectangle of all the monitors is the *virtual screen*.</span></span> <span data-ttu-id="ab194-107">Der Desktop deckt den virtuellen Bildschirm anstelle eines einzelnen Monitors ab.</span><span class="sxs-lookup"><span data-stu-id="ab194-107">The desktop covers the virtual screen instead of a single monitor.</span></span> <span data-ttu-id="ab194-108">Die folgende Abbildung zeigt eine mögliche Anordnung von drei Monitoren.</span><span class="sxs-lookup"><span data-stu-id="ab194-108">The following illustration shows a possible arrangement of three monitors.</span></span>

![Abbildung mit drei Feldern, die Monitore darstellen, die in einem Feld angeordnet sind, das den virtuellen Bildschirm darstellt](images/multimon-1.png)

<span data-ttu-id="ab194-110">Der *primäre Monitor* enthält den Ursprung (0,0).</span><span class="sxs-lookup"><span data-stu-id="ab194-110">The *primary monitor* contains the origin (0,0).</span></span> <span data-ttu-id="ab194-111">Dies dient der Kompatibilität mit vorhandenen Anwendungen, die einen Monitor mit einem Ursprung erwarten.</span><span class="sxs-lookup"><span data-stu-id="ab194-111">This is for compatibility with existing applications that expect a monitor with an origin.</span></span> <span data-ttu-id="ab194-112">Der primäre Monitor muss sich jedoch nicht in der oberen linken Ecke des virtuellen Bildschirms befinden.</span><span class="sxs-lookup"><span data-stu-id="ab194-112">However, the primary monitor does not have to be in the upper left of the virtual screen.</span></span> <span data-ttu-id="ab194-113">In Abbildung 1 befindet Sie sich in der Mitte.</span><span class="sxs-lookup"><span data-stu-id="ab194-113">In Figure 1, it is near the center.</span></span> <span data-ttu-id="ab194-114">Wenn sich der primäre Monitor nicht in der oberen linken Ecke des virtuellen Bildschirms befindet, sind Teile des virtuellen Bildschirms mit negativen Koordinaten vorhanden.</span><span class="sxs-lookup"><span data-stu-id="ab194-114">When the primary monitor is not in the upper left of the virtual screen, parts of the virtual screen have negative coordinates.</span></span> <span data-ttu-id="ab194-115">Da die Anordnung von Monitoren vom Benutzer festgelegt wird, sollten alle Anwendungen für die Arbeit mit negativen Koordinaten konzipiert werden.</span><span class="sxs-lookup"><span data-stu-id="ab194-115">Because the arrangement of monitors is set by the user, all applications should be designed to work with negative coordinates.</span></span> <span data-ttu-id="ab194-116">Weitere Informationen finden Sie unter [Überlegungen zu mehreren Monitoren für ältere Programme](multiple-monitor-considerations-for-older-programs.md).</span><span class="sxs-lookup"><span data-stu-id="ab194-116">For more information, see [Multiple Monitor Considerations for Older Programs](multiple-monitor-considerations-for-older-programs.md).</span></span>

<span data-ttu-id="ab194-117">Die Koordinaten des virtuellen Bildschirms werden aufgrund der 16-Bit-Werte, die in vielen vorhandenen Nachrichten enthalten sind, durch einen 16-Bit-Wert mit Vorzeichen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="ab194-117">The coordinates of the virtual screen are represented by a signed 16-bit value because of the 16-bit values contained in many existing messages.</span></span> <span data-ttu-id="ab194-118">Folglich lauten die Begrenzungen des virtuellen Bildschirms wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ab194-118">Thus, the bounds of the virtual screen are:</span></span>

``` syntax
SHORT_MIN    <= rcVirtualScreen.left   <= SHORT_MAX - 1
SHORT_MIN +1 <= rcVirtualScreen.right  <= SHORT_MAX
SHORT_MIN    <= rcVirtualScreen.top    <= SHORT_MAX - 1
SHORT_MIN +1 <= rcVirtualScreen.bottom <= SHORT_MAX
```

 

 



