---
title: Vorgänge für Kachelpools
description: In diesem Abschnitt werden Vorgänge aufgelistet, die Sie für Kachel Pools ausführen können.
ms.assetid: 69CF182B-9161-43B7-89A5-0468E1BBD6B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a6c9ec58e6c9197f107f47cd7fe3513f43030c0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104209252"
---
# <a name="operations-available-on-tile-pools"></a><span data-ttu-id="259bc-103">Vorgänge für Kachelpools</span><span class="sxs-lookup"><span data-stu-id="259bc-103">Operations available on tile pools</span></span>

<span data-ttu-id="259bc-104">In diesem Abschnitt werden Vorgänge aufgelistet, die Sie für Kachel Pools ausführen können.</span><span class="sxs-lookup"><span data-stu-id="259bc-104">This section lists operations that you can perform on tile pools.</span></span>

-   <span data-ttu-id="259bc-105">Die Lebensdauer von Kachel Pools funktioniert wie jede andere Direct3D-Ressource, die durch die Verweis Zählung unterstützt wird, einschließlich der Nachverfolgung von Zuordnungen aus gekachelten Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="259bc-105">The lifetime of tile pools works like any other Direct3D Resource, backed by reference counting, including in this case tracking of mappings from tiled resources.</span></span> <span data-ttu-id="259bc-106">Wenn die Anwendung nicht mehr auf einen Kachel Pool verweist und alle Kachel Zuordnungen zum Arbeitsspeicher verschwunden sind und der GPU-Zugriff (Graphics Processing Unit) abgeschlossen ist, hebt das Betriebssystem die Zuordnung des Kachel Pools auf.</span><span class="sxs-lookup"><span data-stu-id="259bc-106">When the application no longer references a tile pool and any tile mappings to the memory are gone and graphics processing unit (GPU) accesses completed, the operating system will deallocate the tile pool.</span></span>
-   <span data-ttu-id="259bc-107">APIs, die sich auf die Freigabe und Synchronisierung von Oberflächen beziehen, funktionieren für Kachel Pools (aber nicht direkt auf Kacheln).</span><span class="sxs-lookup"><span data-stu-id="259bc-107">APIs related to surface sharing and synchronization work for tile pools (but not directly on tiled resources).</span></span> <span data-ttu-id="259bc-108">Ähnlich wie das Verhalten für angebotene Kachel Pools werden Direct3D-Befehle, die auf gekachelte Ressourcen zugreifen, die auf einen Kachel Pool zeigen, gelöscht, wenn der Kachel Pool freigegeben wurde und zurzeit von einem anderen Gerät und Prozess abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="259bc-108">Similar to the behavior for offered tile pools, Direct3D commands that access tiled resources that point to a tile pool are dropped if the tile pool has been shared and is currently acquired by another device and process.</span></span>
-   <span data-ttu-id="259bc-109">[**ID3D11DeviceContext2:: resizetilepool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) -Vorgang</span><span class="sxs-lookup"><span data-stu-id="259bc-109">[**ID3D11DeviceContext2::ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) operation</span></span>
-   <span data-ttu-id="259bc-110">[**IDXGIDevice2:: offerresources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources) -und [**reclaimresources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) -Vorgänge: Diese APIs für die vorübergehende Bereitstellen von Speicher für das System arbeiten für den gesamten Kachel Pool (und sind für einzelne gekachelte Ressourcen nicht verfügbar).</span><span class="sxs-lookup"><span data-stu-id="259bc-110">[**IDXGIDevice2::OfferResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources) and [**ReclaimResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) operations - These APIs for yielding memory temporarily to the system operate on the entire tile pool (and aren't available for individual tiled resources).</span></span> <span data-ttu-id="259bc-111">Wenn eine gekachelte Ressource auf eine Kachel in einem angebotenen Kachel Pool zeigt, verhält sich die Kachel Ressource so, als ob Sie angeboten wird (z. b. wenn die Laufzeit Befehle löscht, die auf diese Kachel verweisen).</span><span class="sxs-lookup"><span data-stu-id="259bc-111">If a tiled resource points to a tile in an offered tile pool, the tiled resource behaves as if it is offered (for example, the runtime drops commands that reference it).</span></span>

<span data-ttu-id="259bc-112">Daten können nicht direkt in den und aus dem Arbeitsspeicher des Kachel Pools kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="259bc-112">Data can't be copied to and from tile pool memory directly.</span></span> <span data-ttu-id="259bc-113">Der Zugriff auf den Arbeitsspeicher erfolgt immer über gekachelte Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="259bc-113">Accesses to the memory are always done through tiled resources.</span></span>

## <a name="related-topics"></a><span data-ttu-id="259bc-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="259bc-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="259bc-115">Erstellen von Kachel Ressourcen</span><span class="sxs-lookup"><span data-stu-id="259bc-115">Creating tiled resources</span></span>](creating-tiled-resources.md)
</dt> </dl>

 

 