---
title: SRV-verhalten bei nicht zugeordneten Kacheln
description: Das Verhalten von Lesevorgängen in der Shader-Ressourcen Ansicht (SRV), die nicht zugeordnete Kacheln einschließen, hängt von der Hardwareunterstützung ab.
ms.assetid: 9B720BEE-AB0C-4B75-92AD-3F382A107D48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e086a4db869c3204fc560e64002ba04e8bd8ba9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206228"
---
# <a name="srv-behavior-with-non-mapped-tiles"></a><span data-ttu-id="af2a2-103">SRV-verhalten bei nicht zugeordneten Kacheln</span><span class="sxs-lookup"><span data-stu-id="af2a2-103">SRV behavior with non-mapped tiles</span></span>

<span data-ttu-id="af2a2-104">Das Verhalten von Lesevorgängen in der Shader-Ressourcen Ansicht (SRV), die nicht zugeordnete Kacheln einschließen, hängt von der Hardwareunterstützung ab.</span><span class="sxs-lookup"><span data-stu-id="af2a2-104">Behavior of shader resource view (SRV) reads that involve non-mapped tiles depends on the level of hardware support.</span></span> <span data-ttu-id="af2a2-105">Eine Aufschlüsselung der Anforderungen finden Sie unter Read-Behavior für [Kachel Ressourcen-Funktionsebenen](tiled-resources-features-tiers.md).</span><span class="sxs-lookup"><span data-stu-id="af2a2-105">For a breakdown of requirements, see read behavior for [Tiled resources features tiers](tiled-resources-features-tiers.md).</span></span> <span data-ttu-id="af2a2-106">In diesem Abschnitt wird das ideale Verhalten zusammengefasst, das für [Ebene 2](tier-2.md) erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="af2a2-106">This section summarizes the ideal behavior, which [Tier 2](tier-2.md) requires.</span></span>

<span data-ttu-id="af2a2-107">Stellen Sie sich einen Textur Filter Vorgang vor, der aus einer Gruppe von texeln in einem SRV liest.</span><span class="sxs-lookup"><span data-stu-id="af2a2-107">Consider a texture filter operation that reads from a set of texels in an SRV.</span></span> <span data-ttu-id="af2a2-108">Texels, die auf nicht zugeordnete Kacheln fallen, tragen in alle nicht fehlenden Komponenten des Formats (und die Standardeinstellung für fehlende Komponenten) in den gesamten Filter Vorgang neben den Beiträgen aus zugeordneten texeln den Wert 0 (null) ein.</span><span class="sxs-lookup"><span data-stu-id="af2a2-108">Texels that fall on non-mapped tiles contribute 0 in all non-missing components of the format (and the default for missing components) into the overall filter operation alongside contributions from mapped texels.</span></span> <span data-ttu-id="af2a2-109">Die texeln werden alle gewichtet und kombiniert, unabhängig davon, ob die Daten von zugeordneten oder nicht zugeordneten Kacheln stammen.</span><span class="sxs-lookup"><span data-stu-id="af2a2-109">The texels are all weighted and combined together independent of whether the data came from mapped or non-mapped tiles.</span></span>

<span data-ttu-id="af2a2-110">Die Hardware der ersten Ebene der Ebene [2](tier-2.md) erfüllt diese Spezifikations Anforderung nicht und gibt das 0 (null) mit den Standardwerten zurück, die vorher als Gesamt Filterergebnis bezeichnet werden, wenn texeln (mit einer Gewichtung ungleich null) auf nicht zugeordnete Kacheln fallen.</span><span class="sxs-lookup"><span data-stu-id="af2a2-110">Some first generation [Tier 2](tier-2.md) level hardware does not meet this spec requirement and returns the 0 with defaults described preceding as the overall filter result if any texels (with nonzero weight) fall on non-mapped tiles.</span></span> <span data-ttu-id="af2a2-111">Es ist nicht zulässig, dass andere Hardware die Anforderung erhält, alle texeln (ungleich 0) in den Filter einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="af2a2-111">No other hardware will be allowed to miss the requirement to include all (nonzero weight) texels in the filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="af2a2-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="af2a2-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af2a2-113">Pipeline Zugriff auf gekachelte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="af2a2-113">Pipeline access to tiled resources</span></span>](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




