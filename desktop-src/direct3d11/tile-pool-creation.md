---
title: Erstellung eines Kachelpools
description: Ein Kachel Pool wird mithilfe der ID3D11Device-API von "" erstellt, indem das Flag "D3D11 \_ \_ ressourcenmisc- \_ Kachel \_ Pool" im Fehlerflags-Member der D3D11-Puffer-Debug- \_ \_ Struktur, auf die der pdebug-Parameter verweist, übergeben wird.
ms.assetid: 751A64A6-C9B6-4797-BA1C-B3BEF655DF32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f3b66a9a548d27382f8cbb4e447516beea6eca8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104992734"
---
# <a name="tile-pool-creation"></a><span data-ttu-id="f8be0-103">Erstellung eines Kachelpools</span><span class="sxs-lookup"><span data-stu-id="f8be0-103">Tile pool creation</span></span>

<span data-ttu-id="f8be0-104">Ein Kachel Pool wird über die [**ID3D11Device:: featebuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) -API erstellt, indem das Flag für den [**D3D11- \_ \_ ressourcenmisc- \_ Kachel \_ Pool**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) im **Fehlerflags** -Member der [**D3D11- \_ Puffer- \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) Debug-Struktur, auf die der *PDE SC* -Parameter verweist, übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="f8be0-104">A tile pool is created via the [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) API by passing the [**D3D11\_RESOURCE\_MISC\_TILE\_POOL**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) flag in the **MiscFlags** member of the [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure that the *pDesc* parameter points to.</span></span>

<span data-ttu-id="f8be0-105">Anwendungen können einen oder mehrere Kachel Pools pro Direct3D-Gerät erstellen.</span><span class="sxs-lookup"><span data-stu-id="f8be0-105">Applications can create one or more tile pools per Direct3D device.</span></span> <span data-ttu-id="f8be0-106">Die Gesamtgröße jedes Kachel Pools ist auf die Ressourcen Größenbeschränkung von Direct3D 11 beschränkt, was ungefähr 1/4 des GPU-RAM (Graphics Processing Unit) entspricht.</span><span class="sxs-lookup"><span data-stu-id="f8be0-106">The total size of each tile pool is restricted to Direct3D 11's resource size limit, which is roughly 1/4 of graphics processing unit (GPU) RAM.</span></span>

<span data-ttu-id="f8be0-107">Ein Kachel Pool besteht aus 64 KB-Kacheln, aber das Betriebssystem (Anzeigetreiber) verwaltet den gesamten Pool als eine oder mehrere Zuordnungen hinter den Kulissen – die Aufschlüsselung ist für Anwendungen nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="f8be0-107">A tile pool is made of 64KB tiles, but the operating system (display driver) manages the entire pool as one or more allocations behind the scenes—the breakdown is not visible to applications.</span></span> <span data-ttu-id="f8be0-108">Gekachelte Ressourcen definieren Inhalt, indem Sie auf Kacheln innerhalb eines Kachel Pools zeigen.</span><span class="sxs-lookup"><span data-stu-id="f8be0-108">Tiled resources define content by pointing at tiles within a tile pool.</span></span> <span data-ttu-id="f8be0-109">Wenn Sie die Zuordnung einer Kachel aus einer gekachelten Ressource entordnen, wird die Kachel auf **null** verwiesen.</span><span class="sxs-lookup"><span data-stu-id="f8be0-109">Unmapping a tile from a tiled resource is done by pointing the tile to **NULL**.</span></span> <span data-ttu-id="f8be0-110">Solche nicht zugeordneten Kacheln verfügen über Regeln zum Verhalten von Lese-oder Schreibvorgängen.</span><span class="sxs-lookup"><span data-stu-id="f8be0-110">Such unmapped tiles have rules about the behavior of reads or writes.</span></span> <span data-ttu-id="f8be0-111">Weitere Informationen finden Sie unter [Gefahren Nachverfolgung im Vergleich zu Kachel Pool Ressourcen](hazard-tracking-versus-tile-pool-resources.md).</span><span class="sxs-lookup"><span data-stu-id="f8be0-111">For info, see [Hazard tracking versus tile pool resources](hazard-tracking-versus-tile-pool-resources.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f8be0-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f8be0-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8be0-113">Zuordnungen in einen Kachelpool</span><span class="sxs-lookup"><span data-stu-id="f8be0-113">Mappings are into a tile pool</span></span>](mappings-are-into-a-tile-pool.md)
</dt> </dl>

 

 




