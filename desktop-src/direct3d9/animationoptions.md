---
description: Ermöglicht es Ihnen, Animations Optionen festzulegen.
ms.assetid: 727b4d87-4164-4915-b158-d21fe7d1b729
title: AnimationOptions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7bd3c5df8081523ccef2a802e631454fadaeeae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127129"
---
# <a name="animationoptions"></a><span data-ttu-id="c7ceb-103">AnimationOptions</span><span class="sxs-lookup"><span data-stu-id="c7ceb-103">AnimationOptions</span></span>

<span data-ttu-id="c7ceb-104">Ermöglicht es Ihnen, Animations Optionen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="c7ceb-104">Enables you to set animation options.</span></span>

``` syntax
template AnimationOptions
{
    < E2BF56C0-840F-11cf-8F52-0040333594A3 >
    DWORD openclosed;
    DWORD positionquality;
} 
```

<span data-ttu-id="c7ceb-105">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="c7ceb-105">Where:</span></span>

-   <span data-ttu-id="c7ceb-106">openclosed: Verwenden Sie 0 für eine geschlossene Animation oder 1 für eine geöffnete Animation.</span><span class="sxs-lookup"><span data-stu-id="c7ceb-106">openclosed - Use 0 for a closed animation, or 1 for an open animation.</span></span> <span data-ttu-id="c7ceb-107">Standardmäßig wird eine Animation geschlossen.</span><span class="sxs-lookup"><span data-stu-id="c7ceb-107">By default, an animation is closed.</span></span>
-   <span data-ttu-id="c7ceb-108">positionquality: legt die Positions Qualität für beliebige Positions Schlüssel fest.</span><span class="sxs-lookup"><span data-stu-id="c7ceb-108">positionquality - Set the position quality for any position keys specified.</span></span> <span data-ttu-id="c7ceb-109">Verwenden Sie 0 für Spline-Positionen oder 1 für lineare Positionen.</span><span class="sxs-lookup"><span data-stu-id="c7ceb-109">Use 0 for spline positions or 1 for linear positions.</span></span>

## <a name="see-also"></a><span data-ttu-id="c7ceb-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7ceb-110">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7ceb-111">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="c7ceb-111">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



