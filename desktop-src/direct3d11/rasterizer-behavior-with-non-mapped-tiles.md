---
title: Rasterizerverhalten bei nicht zugeordneten Kacheln
description: In diesem Abschnitt wird das Verhalten des Rasterizers mit nicht zugeordneten Kacheln beschrieben.
ms.assetid: 3477A621-7051-4585-AB58-523EE64CDC5C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54230321f4286b92a3444e3f74167ee7b8711c3f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104992814"
---
# <a name="rasterizer-behavior-with-non-mapped-tiles"></a><span data-ttu-id="bfd72-103">Rasterizerverhalten bei nicht zugeordneten Kacheln</span><span class="sxs-lookup"><span data-stu-id="bfd72-103">Rasterizer behavior with non-mapped tiles</span></span>

<span data-ttu-id="bfd72-104">In diesem Abschnitt wird das Verhalten des Rasterizers mit nicht zugeordneten Kacheln beschrieben.</span><span class="sxs-lookup"><span data-stu-id="bfd72-104">This section describes rasterizer behavior with non-mapped tiles.</span></span>

## <a name="depthstencilview"></a><span data-ttu-id="bfd72-105">Depthstencilview</span><span class="sxs-lookup"><span data-stu-id="bfd72-105">DepthStencilView</span></span>

<span data-ttu-id="bfd72-106">Das Verhalten von Lese-und Schreibvorgängen in der tiefen Schablone ist abhängig von der Hardwareunterstützung.</span><span class="sxs-lookup"><span data-stu-id="bfd72-106">Behavior of depth stencil view (DSV) reads and writes depends on the level of hardware support.</span></span> <span data-ttu-id="bfd72-107">Eine Aufschlüsselung der Anforderungen finden Sie unter Allgemeines Lese-und Schreibverhalten für die [Features der gekachelten Ressourcen](tiled-resources-features-tiers.md).</span><span class="sxs-lookup"><span data-stu-id="bfd72-107">For a breakdown of requirements, see overall read and write behavior for [Tiled resources features tiers](tiled-resources-features-tiers.md).</span></span>

<span data-ttu-id="bfd72-108">Hier ist das ideale Verhalten:</span><span class="sxs-lookup"><span data-stu-id="bfd72-108">Here is the ideal behavior:</span></span>

<span data-ttu-id="bfd72-109">Wenn eine Kachel nicht in der depthstencilview zugeordnet ist, ist der Rückgabewert aus der Lesetiefe 0 (null), der dann in alle Vorgänge eingefügt wird, die für den Wert der tiefen Lesevorgänge konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="bfd72-109">If a tile isn't mapped in the DepthStencilView, the return value from reading depth is 0, which is then fed into whatever operations are configured for the depth read value.</span></span> <span data-ttu-id="bfd72-110">Schreibvorgänge in die Kachel "fehlende tiefe" werden gelöscht.</span><span class="sxs-lookup"><span data-stu-id="bfd72-110">Writes to the missing depth tile are dropped.</span></span> <span data-ttu-id="bfd72-111">Diese ideale Definition für die Schreib Behandlung ist für [Ebene 2](tier-2.md)nicht erforderlich. Schreibvorgänge in nicht zugeordnete Kacheln können in einem Cache landen, den nachfolgende Lesevorgänge aufnehmen können.</span><span class="sxs-lookup"><span data-stu-id="bfd72-111">This ideal definition for write handling is not required by [Tier 2](tier-2.md); writes to non-mapped tiles can end up in a cache that subsequent reads could pick up.</span></span>

## <a name="rendertargetview"></a><span data-ttu-id="bfd72-112">Rendertargetview</span><span class="sxs-lookup"><span data-stu-id="bfd72-112">RenderTargetView</span></span>

<span data-ttu-id="bfd72-113">Das Verhalten von Lese-und Schreibvorgängen der renderzielansicht (RTV) hängt von der Hardwareunterstützung ab.</span><span class="sxs-lookup"><span data-stu-id="bfd72-113">Behavior of render target view (RTV) reads and writes depends on the level of hardware support.</span></span> <span data-ttu-id="bfd72-114">Eine Aufschlüsselung der Anforderungen finden Sie unter Allgemeines Lese-und Schreibverhalten für die [Features der gekachelten Ressourcen](tiled-resources-features-tiers.md).</span><span class="sxs-lookup"><span data-stu-id="bfd72-114">For a breakdown of requirements, see overall read and write behavior for [Tiled resources features tiers](tiled-resources-features-tiers.md).</span></span>

<span data-ttu-id="bfd72-115">Bei allen Implementierungen können unterschiedliche, gleichzeitig gebundene rtvs (und DSV) verschiedene Bereiche zugeordnet werden, die nicht zugeordnet sind und unterschiedliche Größen Oberflächen Formate aufweisen können (Dies bedeutet verschiedene Kachel Formen).</span><span class="sxs-lookup"><span data-stu-id="bfd72-115">On all implementations, different RTVs (and DSV) bound simultaneously can have different areas mapped versus non-mapped and can have different sized surface formats (which means different tile shapes).</span></span>

<span data-ttu-id="bfd72-116">Hier ist das ideale Verhalten:</span><span class="sxs-lookup"><span data-stu-id="bfd72-116">Here is the ideal behavior:</span></span>

<span data-ttu-id="bfd72-117">Lesevorgänge aus rtvs geben 0 in fehlenden Kacheln zurück, und Schreibvorgänge werden gelöscht.</span><span class="sxs-lookup"><span data-stu-id="bfd72-117">Reads from RTVs return 0 in missing tiles and writes are dropped.</span></span> <span data-ttu-id="bfd72-118">Diese ideale Definition für die Schreib Behandlung ist für [Ebene 2](tier-2.md)nicht erforderlich. Schreibvorgänge in nicht zugeordnete Kacheln können in einem Cache landen, den nachfolgende Lesevorgänge aufnehmen können.</span><span class="sxs-lookup"><span data-stu-id="bfd72-118">This ideal definition for write handling is not required by [Tier 2](tier-2.md); writes to non-mapped tiles can end up in a cache that subsequent reads could pick up.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bfd72-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bfd72-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bfd72-120">Pipeline Zugriff auf gekachelte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bfd72-120">Pipeline access to tiled resources</span></span>](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




