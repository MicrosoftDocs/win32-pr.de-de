---
title: Gefahrennachverfolgung im Vergleich mit den Kachelpoolressourcen
description: Bei nicht gekachelten Ressourcen kann Direct3D bestimmte Gefahren Bedingungen während des Renderings verhindern, aber da die gefährverfolgung auf Kachel Ebene für gekachelte Ressourcen erfolgen würde, kann das Nachverfolgen von Gefährdungs Zuständen beim Rendern von gekachelten Ressourcen zu teuer sein.
ms.assetid: 4106BAB9-3E0C-48F1-B7E2-565A65DBC78F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c75dcd11cb5e49f165105bd932854e36b37308cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388033"
---
# <a name="hazard-tracking-versus-tile-pool-resources"></a><span data-ttu-id="33a94-103">Gefahrennachverfolgung im Vergleich mit den Kachelpoolressourcen</span><span class="sxs-lookup"><span data-stu-id="33a94-103">Hazard tracking versus tile pool resources</span></span>

<span data-ttu-id="33a94-104">Bei nicht gekachelten Ressourcen kann Direct3D bestimmte Gefahren Bedingungen während des Renderings verhindern, aber da die gefährverfolgung auf Kachel Ebene für gekachelte Ressourcen erfolgen würde, kann das Nachverfolgen von Gefährdungs Zuständen beim Rendern von gekachelten Ressourcen zu teuer sein.</span><span class="sxs-lookup"><span data-stu-id="33a94-104">For non-tiled resources, Direct3D can prevent certain hazard conditions during rendering, but because hazard tracking would be at a tile level for tiled resources, tracking hazard conditions during rendering of tiled resources might be too expensive.</span></span>

<span data-ttu-id="33a94-105">Beispielsweise lässt die Runtime für nicht gekachelte Ressourcen nicht zu, dass eine angegebene untergeordnete Quelle als Eingabe (z. b. eine shaderresourceview) und als Ausgabe (z. b. eine rendertargetview) gleichzeitig gebunden wird.</span><span class="sxs-lookup"><span data-stu-id="33a94-105">For example, for non-tiled resources, the runtime doesn't allow any given SubResource to be bound as an input (such as a ShaderResourceView) and as an output (such as a RenderTargetView) at the same time.</span></span> <span data-ttu-id="33a94-106">Wenn ein solcher Fall auftritt, wird die Bindung der Eingabe von der Laufzeit entbindet.</span><span class="sxs-lookup"><span data-stu-id="33a94-106">If such a case is encountered, the runtime unbinds the input.</span></span> <span data-ttu-id="33a94-107">Dieser Überwachungs Aufwand in der Laufzeit ist kostengünstig und wird auf der Ebene der untergeordneten Quelle erreicht.</span><span class="sxs-lookup"><span data-stu-id="33a94-107">This tracking overhead in the runtime is cheap and is done at the SubResource level.</span></span> <span data-ttu-id="33a94-108">Einer der Vorteile dieses nach Verfolgungs Aufwands besteht darin, die Wahrscheinlichkeit von Anwendungen zu minimieren, abhängig von der Reihenfolge der Hardware-Shader-Ausführung.</span><span class="sxs-lookup"><span data-stu-id="33a94-108">One of the benefits of this tracking overhead is to minimize the chances of applications accidentally depending on hardware shader execution order.</span></span> <span data-ttu-id="33a94-109">Die Ausführungsreihenfolge der Hardware-Shader kann variieren, wenn Sie nicht auf einer bestimmten GPU (Graphics Processing Unit) und dann auf unterschiedlichen GPUs verteilt ist.</span><span class="sxs-lookup"><span data-stu-id="33a94-109">Hardware shader execution order can vary if not on a given graphics processing unit (GPU), then certainly across different GPUs.</span></span>

<span data-ttu-id="33a94-110">Die Nachverfolgung, wie Ressourcen gebunden werden, kann für gekachelte Ressourcen zu teuer sein, da die Nachverfolgung auf Kachel Ebene erfolgt.</span><span class="sxs-lookup"><span data-stu-id="33a94-110">Tracking how resources are bound might be too expensive for tiled resources because tracking is at a tile level.</span></span> <span data-ttu-id="33a94-111">Es ergeben sich neue Probleme, z. b. das Überprüfen von versuchen, eine rendertargetview zu rendertargetview zu rendieren, und eine Kachel, die mehreren Bereichen in der</span><span class="sxs-lookup"><span data-stu-id="33a94-111">New issues arise such as possibly validating away attempts to render to an RenderTargetView with one tile mapped to multiple areas in the surface simultaneously.</span></span> <span data-ttu-id="33a94-112">Wenn sich herausstellt, dass die Nachverfolgung pro Kachel für die Laufzeit zu teuer ist, ist dies im Idealfall zumindest eine Option in der debugschicht.</span><span class="sxs-lookup"><span data-stu-id="33a94-112">If it turns out this per-tile hazard tracking is too expensive for the runtime, ideally this would at least be an option in the debug layer.</span></span>

<span data-ttu-id="33a94-113">Eine Anwendung muss den Anzeigetreiber Benachrichtigen, wenn Sie einen Schreib-oder Lesevorgang für eine gekachelte Ressource ausgegeben hat, die auf den Kachel Pool Speicher verweist, auf den auch von separaten gekachelten Ressourcen in anstehenden Lese-oder Schreibvorgängen verwiesen wird, bevor die folgenden Vorgänge beginnen können.</span><span class="sxs-lookup"><span data-stu-id="33a94-113">An application must inform the display driver when it has issued a write or read operation to a tiled resource that references tile pool memory that will also be referenced by separate tiled resources in upcoming read or write operations that it is expecting the first operation to complete before the following operations can begin.</span></span> <span data-ttu-id="33a94-114">Weitere Informationen zu dieser Bedingung finden Sie unter [**ID3D11DeviceContext2:: tiledresourcebarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) -Hinweise.</span><span class="sxs-lookup"><span data-stu-id="33a94-114">For more info about this condition, see [**ID3D11DeviceContext2::TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) remarks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="33a94-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="33a94-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33a94-116">Zuordnungen in einen Kachelpool</span><span class="sxs-lookup"><span data-stu-id="33a94-116">Mappings are into a tile pool</span></span>](mappings-are-into-a-tile-pool.md)
</dt> </dl>

 

 




