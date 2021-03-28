---
title: Auf gekachelten Ressourcen verfügbare Vorgänge
description: In diesem Abschnitt werden Vorgänge aufgelistet, die Sie für gekachelte Ressourcen ausführen können.
ms.assetid: 1CF42A18-B6EA-4BA9-BEDE-9A8CC083CBAF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45d051943816502fd0bafb77e67241026f31498
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037386"
---
# <a name="operations-available-on-tiled-resources"></a><span data-ttu-id="c8ebc-103">Auf gekachelten Ressourcen verfügbare Vorgänge</span><span class="sxs-lookup"><span data-stu-id="c8ebc-103">Operations available on tiled resources</span></span>

<span data-ttu-id="c8ebc-104">In diesem Abschnitt werden Vorgänge aufgelistet, die Sie für gekachelte Ressourcen ausführen können.</span><span class="sxs-lookup"><span data-stu-id="c8ebc-104">This section lists operations that you can perform on tiled resources.</span></span>

-   <span data-ttu-id="c8ebc-105">void [**ID3D11DeviceContext2:: updatetilemappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) und [**ID3D11DeviceContext2:: copytilemappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) -Vorgänge: Diese Vorgangs Punkt-Kachel Positionen in einer gekachelten Ressource an Positionen in Kachel Pools oder auf NULL oder auf beides.</span><span class="sxs-lookup"><span data-stu-id="c8ebc-105">void [**ID3D11DeviceContext2::UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) and [**ID3D11DeviceContext2::CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) operations - These operations point tile locations in a tiled resource to locations in tile pools, or to NULL, or to both.</span></span> <span data-ttu-id="c8ebc-106">Diese Vorgänge können eine Zusammenhang lose Teilmenge der Kachel Zeiger aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c8ebc-106">These operations can update a disjoint subset of the tile pointers.</span></span>
-   <span data-ttu-id="c8ebc-107">Copy \* ()-und Update \* ()-Vorgänge: alle APIs, die Daten in eine und aus einer Standard Pool Oberfläche (z. b. [**ID3D11DeviceContext1:: CopySubresourceRegion1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) und [**ID3D11DeviceContext1:: UpdateSubresource1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-updatesubresource1)) kopieren können, funktionieren für gekachelte Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="c8ebc-107">Copy\*() and Update\*() operations - All the APIs that can copy data to and from a default pool surface (for example, [**ID3D11DeviceContext1::CopySubresourceRegion1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) and [**ID3D11DeviceContext1::UpdateSubresource1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-updatesubresource1)) work for tiled resources.</span></span> <span data-ttu-id="c8ebc-108">Beim Lesen von nicht zugeordneten Kacheln wird 0 erzeugt und Schreibvorgänge in nicht zugeordnete Kacheln werden gelöscht.</span><span class="sxs-lookup"><span data-stu-id="c8ebc-108">Reading from unmapped tiles produces 0 and writes to unmapped tiles are dropped.</span></span>
-   <span data-ttu-id="c8ebc-109">[**ID3D11DeviceContext2:: copytiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) und [**ID3D11DeviceContext2:: updatetiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles) -Vorgänge: diese Vorgänge sind zum Kopieren von Kacheln mit 64 KB-Granularität in und aus einer gekachelten Ressource und einer Puffer Ressource in einem kanonischen Speicher Layout vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c8ebc-109">[**ID3D11DeviceContext2::CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) and [**ID3D11DeviceContext2::UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles) operations - These operations exist for copying tiles at 64KB granularity to and from any tiled resource and a buffer resource in a canonical memory layout.</span></span> <span data-ttu-id="c8ebc-110">Der Anzeigetreiber und die Hardware führen alle Arbeitsspeicher, die für die gekachelte Ressource erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="c8ebc-110">The display driver and hardware perform any memory "swizzling" necessary for the tiled resource.</span></span>
-   <span data-ttu-id="c8ebc-111">Direct3D Pipeline Bindungen und Ansichts Erstellungen/-Bindungen, die für nicht-Kachel Ressourcen funktionieren, funktionieren auch für gekachelte Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="c8ebc-111">Direct3D pipeline bindings and view creations / bindings that would work on non-tiled resources work on tiled resources as well.</span></span>

<span data-ttu-id="c8ebc-112">Kachel Steuerelemente sind in sofortigen oder verzögerten Kontexten verfügbar (genau wie Aktualisierungen typischer Ressourcen), und bei der Ausführung wirkt sich dies auf nachfolgende Zugriffe auf die Kacheln aus (nicht zuvor übermittelte Vorgänge).</span><span class="sxs-lookup"><span data-stu-id="c8ebc-112">Tile controls are available on immediate or deferred contexts (just like updates to typical resources) and upon execution impact subsequent accesses to the tiles (not previously submitted operations).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8ebc-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c8ebc-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8ebc-114">Erstellen von Kachel Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c8ebc-114">Creating tiled resources</span></span>](creating-tiled-resources.md)
</dt> </dl>

 

 




