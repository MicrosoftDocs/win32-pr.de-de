---
title: UAV-Leistungsindikatoren
description: Sie können die UAV-Leistungsindikatoren (unsortierter Zugriffs Ansicht) verwenden, um einen atomaren 32-Bit-Zähler mit einer nicht geordneten Zugriffs Ansicht (UAV) zuzuordnen.
ms.assetid: 0B77E238-E8CF-466B-9188-3DE96AF97F42
ms.localizationpriority: high
ms.topic: article
ms.date: 02/10/2020
ms.openlocfilehash: 94bc1492e3b984d96c76788430d2e63c0672ca76
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "104548673"
---
# <a name="uav-counters"></a><span data-ttu-id="279d9-103">UAV-Leistungsindikatoren</span><span class="sxs-lookup"><span data-stu-id="279d9-103">UAV Counters</span></span>
<span data-ttu-id="279d9-104">Sie können die UAV-Leistungsindikatoren (unsortierter Zugriffs Ansicht) verwenden, um einen atomaren 32-Bit-Zähler mit einer nicht geordneten Zugriffs Ansicht (UAV) zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="279d9-104">You can use unordered-access-view (UAV) counters to associate a 32-bit atomic counter with an unordered-access-view (UAV).</span></span>

## <a name="differences-in-uav-counters-from-direct3d-11-to-direct3d-12"></a><span data-ttu-id="279d9-105">Unterschiede bei UAV-Indikatoren von Direct3D 11 bis Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="279d9-105">Differences in UAV counters from Direct3D 11 to Direct3D 12</span></span>
<span data-ttu-id="279d9-106">Für den Zugriff auf die UAV-Indikatoren verwenden Direct3D 12 apps und Direct3D 11-apps die gleichen High-Level-Shader-Funktionen (HLSL).</span><span class="sxs-lookup"><span data-stu-id="279d9-106">Direct3D 12 apps and Direct3D 11 apps both use the same high-level shader language (HLSL) shader functions to access the UAV counters.</span></span>

-   <span data-ttu-id="279d9-107">**Incrementcounter**</span><span class="sxs-lookup"><span data-stu-id="279d9-107">**IncrementCounter**</span></span>
-   <span data-ttu-id="279d9-108">**Dekrementcounter**</span><span class="sxs-lookup"><span data-stu-id="279d9-108">**DecrementCounter**</span></span>
-   <span data-ttu-id="279d9-109">**Append**</span><span class="sxs-lookup"><span data-stu-id="279d9-109">**Append**</span></span>
-   <span data-ttu-id="279d9-110">**Nutzen**</span><span class="sxs-lookup"><span data-stu-id="279d9-110">**Consume**</span></span>

### <a name="direct3d-12"></a><span data-ttu-id="279d9-111">Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="279d9-111">Direct3D 12</span></span>
<span data-ttu-id="279d9-112">In Direct3D 12 werden die 32-Bit-Werte von der Anwendung zugeordnet, sodass die 32-Bit-Werte wie jede andere Direct3D 12-Ressource entweder von der CPU oder der GPU gelesen und geschrieben werden können.</span><span class="sxs-lookup"><span data-stu-id="279d9-112">In Direct3D 12, the 32-bit values are allocated by the application, so the 32-bit values can be read and written by either the CPU or the GPU, just like any other Direct3D 12 resource.</span></span>

### <a name="direct3d-11"></a><span data-ttu-id="279d9-113">Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="279d9-113">Direct3D 11</span></span>
<span data-ttu-id="279d9-114">Außerhalb der Shader müssen Sie mit Direct3D 11 API-Methoden aufrufen, um auf die Indikatoren zuzugreifen (z. b. [Verknüpfung id3d11devicecontext aus:: copystructurecount](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-copystructurecount)).</span><span class="sxs-lookup"><span data-stu-id="279d9-114">Outside of the shaders, with Direct3D 11 you need to call API methods in order to access the counters (for example, [ID3D11DeviceContext::CopyStructureCount](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-copystructurecount)).</span></span>

## <a name="using-uav-counters"></a><span data-ttu-id="279d9-115">Verwenden von UAV-Leistungsindikatoren</span><span class="sxs-lookup"><span data-stu-id="279d9-115">Using UAV counters</span></span>
<span data-ttu-id="279d9-116">Ihre APP ist dafür verantwortlich, 32 Bits Speicher für UAV-Indikatoren zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="279d9-116">Your app is responsible for allocating 32-bits of storage for UAV counters.</span></span> <span data-ttu-id="279d9-117">Dieser Speicher kann in einer anderen Ressource zugewiesen werden als der, der Daten enthält, auf die über die UAV zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="279d9-117">This storage can be allocated in a different resource as the one that contains data accessible via the UAV.</span></span>

<span data-ttu-id="279d9-118">Weitere Informationen finden Sie unter " [**kreateunorderedaccessview**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)", [**D3D12 \_ buffer \_ UAV \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags) und [**D3D12 \_ buffer \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_uav).</span><span class="sxs-lookup"><span data-stu-id="279d9-118">Refer to [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview), [**D3D12\_BUFFER\_UAV\_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags) and [**D3D12\_BUFFER\_UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_uav).</span></span>

<span data-ttu-id="279d9-119">Wenn " *pcounterresource* " im Aufrufen von " [**anateunorderedaccessview**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)" angegeben wird, ist der UAV ein Indikator zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="279d9-119">If *pCounterResource* is specified in the call to [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview), then there is a counter associated with the UAV.</span></span> <span data-ttu-id="279d9-120">In diesem Fall:</span><span class="sxs-lookup"><span data-stu-id="279d9-120">In this case:</span></span>

-   <span data-ttu-id="279d9-121">*Structurebytestride* muss größer als 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="279d9-121">*StructureByteStride* must be greater than zero</span></span>
-   <span data-ttu-id="279d9-122">Das Format muss im DXGI- \_ Format unbekannt sein. \_</span><span class="sxs-lookup"><span data-stu-id="279d9-122">Format must be DXGI\_FORMAT\_UNKNOWN</span></span>
-   <span data-ttu-id="279d9-123">Das RAW-Flag darf nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="279d9-123">The RAW flag must not be set</span></span>
-   <span data-ttu-id="279d9-124">Beide Ressourcen müssen Puffer sein.</span><span class="sxs-lookup"><span data-stu-id="279d9-124">Both of the resources must be buffers</span></span>
-   <span data-ttu-id="279d9-125">*Counteroffset-Bytes* muss ein Vielfaches von 4 Bytes sein.</span><span class="sxs-lookup"><span data-stu-id="279d9-125">*CounterOffsetInBytes* must be a multiple of 4 bytes</span></span>
-   <span data-ttu-id="279d9-126">*Counteroffmentinbytes* muss innerhalb des Bereichs der Indikator Ressource liegen.</span><span class="sxs-lookup"><span data-stu-id="279d9-126">*CounterOffsetInBytes* must be within the range of the counter resource</span></span>
-   <span data-ttu-id="279d9-127">*pdebug* darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="279d9-127">*pDesc* cannot be NULL</span></span>
-   <span data-ttu-id="279d9-128">die *präquelle* darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="279d9-128">*pResource* cannot be NULL</span></span>

<span data-ttu-id="279d9-129">Beachten Sie auch die folgenden Anwendungsfälle:</span><span class="sxs-lookup"><span data-stu-id="279d9-129">And note the following use cases:</span></span>

-   <span data-ttu-id="279d9-130">Wenn " *pcounterresource* " nicht angegeben wird, muss " *counteroffset tinbytes* " den Wert "0" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="279d9-130">If *pCounterResource* is not specified, then *CounterOffsetInBytes* must be 0.</span></span>
-   <span data-ttu-id="279d9-131">Wenn das RAW-Flag festgelegt ist, muss das Format das DXGI \_ -Format R32 aufweisen, \_ \_ und die UAV-Ressource muss ein Puffer sein.</span><span class="sxs-lookup"><span data-stu-id="279d9-131">If the RAW flag is set then the format must be DXGI\_FORMAT\_R32\_TYPELESS and the UAV resource must be a buffer.</span></span>
-   <span data-ttu-id="279d9-132">Wenn *pcounterresource* nicht festgelegt ist, muss *counteroffsetinbytes* den Wert 0 aufweisen.</span><span class="sxs-lookup"><span data-stu-id="279d9-132">If *pCounterResource* is not set, then *CounterOffsetInBytes* must be 0.</span></span>
-   <span data-ttu-id="279d9-133">Wenn das RAW-Flag nicht festgelegt ist und *structurebytestride* = 0 ist, muss das Format ein gültiges UAV-Format aufweisen.</span><span class="sxs-lookup"><span data-stu-id="279d9-133">If the RAW flag is not set and *StructureByteStride* = 0, then the format must be a valid UAV format.</span></span>

<span data-ttu-id="279d9-134">Direct3D 12 entfernt den Unterschied zwischen angefügenden und gegen-UAVs (obwohl der Unterschied in HLSL-Bytecode noch vorhanden ist).</span><span class="sxs-lookup"><span data-stu-id="279d9-134">Direct3D 12 removes the distinction between append and counter UAVs (although the distinction still exists in HLSL bytecode).</span></span>

<span data-ttu-id="279d9-135">Die Core-Laufzeit überprüft diese Einschränkungen in der Datei " [**" von "**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview)".</span><span class="sxs-lookup"><span data-stu-id="279d9-135">The core runtime will validate these restrictions inside of [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview).</span></span>

<span data-ttu-id="279d9-136">Beim Zeichnen/verteilen muss die Counter-Ressource den Status [**D3D12 \_ Resource \_ State \_ unsortierter \_ Zugriff**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)aufweisen.</span><span class="sxs-lookup"><span data-stu-id="279d9-136">During Draw/Dispatch, the counter resource must be in the state [**D3D12\_RESOURCE\_STATE\_UNORDERED\_ACCESS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states).</span></span> <span data-ttu-id="279d9-137">Außerdem ist es innerhalb eines einzelnen Draw/Dispatch-Aufrufes nicht möglich, dass eine Anwendung über zwei separate UAV-Indikatoren auf denselben Speicherort mit 32-Bit-Speicher zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="279d9-137">Also, within a single Draw/Dispatch call, it is invalid for an application to access the same 32-bit memory location via two separate UAV counters.</span></span> <span data-ttu-id="279d9-138">Die debugschicht gibt Fehler aus, wenn eine dieser Funktionen erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="279d9-138">The debug layer will issue errors if either of these is detected.</span></span>

<span data-ttu-id="279d9-139">Es gibt keine "Set-Methode" oder "copystructurecount"-Methoden, da Apps einfach Daten direkt in den und aus dem Zählerwert kopieren können.</span><span class="sxs-lookup"><span data-stu-id="279d9-139">There are no "SetUnorderedAccessViewCounterValue" or "CopyStructureCount" methods because apps can simply copy data to and from the counter value directly.</span></span>

<span data-ttu-id="279d9-140">Dynamische Indizierung von UAVs mit Leistungsindikatoren wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="279d9-140">Dynamic indexing of UAVs with counters is supported.</span></span>

<span data-ttu-id="279d9-141">Wenn ein Shader versucht, auf den-Wert einer UAV zuzugreifen, der nicht über einen zugeordneten-Wert verfügt, wird von der debugschicht eine Warnung ausgegeben, und es tritt ein GPU-Seiten Fehler auf, der bewirkt, dass das Gerät der apps entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="279d9-141">If a shader attempts to access the counter of a UAV that does not have an associated counter, then the debug layer will issue a warning, and a GPU page fault will occur causing the apps’s device to be removed.</span></span>

<span data-ttu-id="279d9-142">UAV-Indikatoren werden in allen Heap Typen unterstützt (Standard, Upload, Read Back).</span><span class="sxs-lookup"><span data-stu-id="279d9-142">UAV counters are supported in all heap types (default, upload, readback).</span></span>

## <a name="related-topics"></a><span data-ttu-id="279d9-143">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="279d9-143">Related topics</span></span>

* [<span data-ttu-id="279d9-144">Zähler und Abfragen</span><span class="sxs-lookup"><span data-stu-id="279d9-144">Counters and queries</span></span>](counters-and-queries.md)