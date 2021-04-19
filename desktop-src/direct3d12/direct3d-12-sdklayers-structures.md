---
title: Strukturen der Debugschicht
description: Die folgenden Strukturen werden in d3d12sdklayers. h deklariert.
ms.assetid: FE8796A7-98D1-4333-8755-2A47567560B3
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 573d49d34c4432796ebac68ce004f265259b9eb2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342304"
---
# <a name="debug-layer-structures"></a><span data-ttu-id="58d7a-103">Strukturen der Debugschicht</span><span class="sxs-lookup"><span data-stu-id="58d7a-103">Debug Layer Structures</span></span>

<span data-ttu-id="58d7a-104">Die folgenden Strukturen werden in d3d12sdklayers. h deklariert.</span><span class="sxs-lookup"><span data-stu-id="58d7a-104">The following structures are declared in d3d12sdklayers.h.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="58d7a-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="58d7a-105">In this section</span></span>



| <span data-ttu-id="58d7a-106">Thema</span><span class="sxs-lookup"><span data-stu-id="58d7a-106">Topic</span></span>                                                                                                                                      | <span data-ttu-id="58d7a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="58d7a-107">Description</span></span>                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="58d7a-108">**D3D12 \_ Debug- \_ Befehls \_ Liste GPU- \_ \_ basierte \_ Validierungs \_ Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="58d7a-108">**D3D12\_DEBUG\_COMMAND\_LIST\_GPU\_BASED\_VALIDATION\_SETTINGS**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_command_list_gpu_based_validation_settings)<br/> | <span data-ttu-id="58d7a-109">Beschreibt die von GPU-Based Validierung verwendeten Befehlslisten Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="58d7a-109">Describes per-command-list settings used by GPU-Based Validation.</span></span> <br/>                                                        |
| [<span data-ttu-id="58d7a-110">**D3D12 \_ Debuggen von \_ \_ GPU-basierten Überprüfungs \_ \_ \_ Einstellungen für Geräte**</span><span class="sxs-lookup"><span data-stu-id="58d7a-110">**D3D12\_DEBUG\_DEVICE\_GPU\_BASED\_VALIDATION\_SETTINGS**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_device_gpu_based_validation_settings)<br/>              | <span data-ttu-id="58d7a-111">Beschreibt die Einstellungen, die von GPU-Based Validierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="58d7a-111">Describes settings used by GPU-Based Validation.</span></span> <br/>                                                                         |
| [<span data-ttu-id="58d7a-112">**D3D12 \_ \_ \_ \_ \_ Leistungs \_ Faktor für die GPU-Verlangsamung des debuggeräts**</span><span class="sxs-lookup"><span data-stu-id="58d7a-112">**D3D12\_DEBUG\_DEVICE\_GPU\_SLOWDOWN\_PERFORMANCE\_FACTOR**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_device_gpu_slowdown_performance_factor)<br/>          | <span data-ttu-id="58d7a-113">Beschreibt den Umfang der künstlichen Verlangsamung, die vom Debuggerät zum Simulieren von Grafikadaptern mit geringerer Leistung eingefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="58d7a-113">Describes the amount of artificial slowdown inserted by the debug device to simulate lower-performance graphics adapters.</span></span><br/> |
| [<span data-ttu-id="58d7a-114">**D3D12 \_ Info \_ Queue \_ Filter**</span><span class="sxs-lookup"><span data-stu-id="58d7a-114">**D3D12\_INFO\_QUEUE\_FILTER**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_info_queue_filter)<br/>                                                                   | <span data-ttu-id="58d7a-115">Debugmeldungs Filter; enthält eine Liste von Nachrichten Typen, die zugelassen oder verweigert werden.</span><span class="sxs-lookup"><span data-stu-id="58d7a-115">Debug message filter; contains a lists of message types to allow or deny.</span></span><br/>                                                 |
| [<span data-ttu-id="58d7a-116">**D3D12 \_ Info \_ Queue \_ Filter \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="58d7a-116">**D3D12\_INFO\_QUEUE\_FILTER\_DESC**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_info_queue_filter_desc)<br/>                                                        | <span data-ttu-id="58d7a-117">Hiermit werden bestimmte Nachrichten Typen zum Durchlaufen eines Filters zugelassen oder verweigert.</span><span class="sxs-lookup"><span data-stu-id="58d7a-117">Allow or deny certain types of messages to pass through a filter.</span></span><br/>                                                         |
| [<span data-ttu-id="58d7a-118">**D3D12- \_ Meldung**</span><span class="sxs-lookup"><span data-stu-id="58d7a-118">**D3D12\_MESSAGE**</span></span>](/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_message)<br/>                                                                                         | <span data-ttu-id="58d7a-119">Eine Debugmeldung in der Informations Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="58d7a-119">A debug message in the Information Queue.</span></span><br/>                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="58d7a-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="58d7a-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58d7a-121">Einrichtung der Direct3D 12-Programmierungsumgebung</span><span class="sxs-lookup"><span data-stu-id="58d7a-121">Direct3D 12 Programming Environment Setup</span></span>](directx-12-programming-environment-set-up.md)
</dt> <dt>

[<span data-ttu-id="58d7a-122">Referenz der Debugschicht</span><span class="sxs-lookup"><span data-stu-id="58d7a-122">Debug Layer Reference</span></span>](direct3d-12-sdklayers-reference.md)
</dt> <dt>

[<span data-ttu-id="58d7a-123">Referenz für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="58d7a-123">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>

 

 





