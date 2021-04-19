---
description: Verwaltete Vertex-Puffer-oder Index Puffer Ressourcen können nicht als dynamisch deklariert werden, indem D3DUSAGE \_ Dynamic zum Erstellungs Zeitpunkt angegeben wird.
ms.assetid: 440d9d94-3a56-4b34-a5e3-1b4712b078fc
title: Application-Managed Ressourcen und Zuordnungs Strategien (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4f5ce23cac4bf46b8580a31d7c6d71fdc3de15
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343584"
---
# <a name="application-managed-resources-and-allocation-strategies-direct3d-9"></a><span data-ttu-id="f191c-103">Application-Managed Ressourcen und Zuordnungs Strategien (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f191c-103">Application-Managed Resources and Allocation Strategies (Direct3D 9)</span></span>

<span data-ttu-id="f191c-104">Verwaltete Vertex-Puffer-oder Index Puffer Ressourcen können nicht als dynamisch deklariert werden, indem D3DUSAGE \_ Dynamic zum Erstellungs Zeitpunkt angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f191c-104">Managed vertex-buffer or index-buffer resources cannot be declared dynamic by specifying D3DUSAGE\_DYNAMIC at creation time.</span></span> <span data-ttu-id="f191c-105">Dies erfordert eine zusätzliche Kopie für jede Änderung am Inhalt des Vertexpuffers.</span><span class="sxs-lookup"><span data-stu-id="f191c-105">This would require an additional copy for every modification to the vertex buffer contents.</span></span> <span data-ttu-id="f191c-106">Dynamische Scheitelpunkt Puffer sind zum Rendern dynamischer Geometrie und aus Daten, die aus dem Binär Raum partitionierte Strukturen oder anderen sichtbaren Datenstrukturen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f191c-106">Dynamic vertex buffers are intended for rendering dynamic geometry and data pulled in from binary space partitioned trees or other visibility data structures.</span></span> <span data-ttu-id="f191c-107">Dies kann erreicht werden, indem Puffer im gewünschten Format vorab zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="f191c-107">This can be accomplished by pre-allocating buffers of the desired format.</span></span> <span data-ttu-id="f191c-108">Diese Ressourcen werden dann zur Unterstützung von Anwendungsanforderungen durch einen Ressourcen-Manager innerhalb der Anwendung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="f191c-108">These resources are then parceled out to support application needs by a resource manager within the application.</span></span> <span data-ttu-id="f191c-109">Die Gesamtanzahl dynamischer Scheitelpunkt Puffer ist klein, weil eine Anwendung gleichzeitig nur ein paar unterschiedliche Scheitel Punkte verwendet, und weil ein anderer Scheitelpunkt Puffer nur für eindeutige Schritte erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="f191c-109">The total number of dynamic vertex buffers is small because an application will use simultaneously only a few different vertex strides and because a different vertex buffer is required only for unique strides.</span></span> <span data-ttu-id="f191c-110">Wenn Sie dynamische Ressourcen auf diese Weise verwalten, stellen Sie sicher, dass die Leistung der Anwendung durch hoch frequente Anforderungen an die Ressourcen nicht erheblich beeinträchtigt wird.</span><span class="sxs-lookup"><span data-stu-id="f191c-110">When managing dynamic resources in this way, ensure that high-frequency demands on the resources do not significantly decrease the application's performance.</span></span>

<span data-ttu-id="f191c-111">Wenn Sie Ressourcen verwenden, die von Direct3D und Anwendungen verwaltet werden, sollten Sie von der Anwendung verwaltete Ressourcen im D3DPOOL \_ -Standard Speicher zuordnen, bevor Sie von Direct3D verwaltete Ressourcen erstellen.</span><span class="sxs-lookup"><span data-stu-id="f191c-111">When using resources managed by both Direct3D and applications, allocate application-managed resources in D3DPOOL\_DEFAULT memory prior to creating Direct3D-managed resources.</span></span> <span data-ttu-id="f191c-112">Dadurch kann der Speicher-Manager eine genaue Anzahl von verfügbarem Arbeitsspeicher beibehalten.</span><span class="sxs-lookup"><span data-stu-id="f191c-112">This enables the memory manager to maintain an accurate count of available memory.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f191c-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f191c-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f191c-114">Direct3D-Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f191c-114">Direct3D Resources</span></span>](direct3d-resources.md)
</dt> </dl>

 

 



