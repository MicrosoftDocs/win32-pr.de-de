---
description: Der Prozentsatz der Zeit, die Daten im Treiber verarbeitet. Mithilfe dieser Statistiken können Fälle identifiziert werden, in denen der Treiber auf andere Ressourcen wartet.
ms.assetid: 2c613349-61eb-44aa-aa7b-3161dd1fc95e
title: D3DDEVINFO_D3D9INTERFACETIMINGS-Struktur (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9INTERFACETIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: dfd6303f3682e29090db41fa83b38fc67f99121e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354357"
---
# <a name="d3ddevinfo_d3d9interfacetimings-structure"></a><span data-ttu-id="c28b2-104">D3DDEVINFO \_ D3D9INTERFACETIMINGS-Struktur</span><span class="sxs-lookup"><span data-stu-id="c28b2-104">D3DDEVINFO\_D3D9INTERFACETIMINGS structure</span></span>

<span data-ttu-id="c28b2-105">Der Prozentsatz der Zeit, die Daten im Treiber verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="c28b2-105">Percent of time processing data in the driver.</span></span> <span data-ttu-id="c28b2-106">Mithilfe dieser Statistiken können Fälle identifiziert werden, in denen der Treiber auf andere Ressourcen wartet.</span><span class="sxs-lookup"><span data-stu-id="c28b2-106">These statistics may help identify cases when the driver is waiting for other resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="c28b2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c28b2-107">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_D3D9INTERFACETIMINGS {
  FLOAT WaitingForGPUToUseApplicationResourceTimePercent;
  FLOAT WaitingForGPUToAcceptMoreCommandsTimePercent;
  FLOAT WaitingForGPUToStayWithinLatencyTimePercent;
  FLOAT WaitingForGPUExclusiveResourceTimePercent;
  FLOAT WaitingForGPUOtherTimePercent;
} D3DDEVINFO_D3D9INTERFACETIMINGS, *LPD3DDEVINFO_D3D9INTERFACETIMINGS;
```



## <a name="members"></a><span data-ttu-id="c28b2-108">Member</span><span class="sxs-lookup"><span data-stu-id="c28b2-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c28b2-109">**Waitingforgputougenapplicationresourcetimeprozent**</span><span class="sxs-lookup"><span data-stu-id="c28b2-109">**WaitingForGPUToUseApplicationResourceTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="c28b2-110">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c28b2-110">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c28b2-111">Der Prozentsatz der Zeit, die der Treiber auf die Beendigung der GPU mithilfe einer gesperrten Ressource gewartet hat (und [D3DLOCK \_ donotwait](d3dlock.md) nicht angegeben wurde).</span><span class="sxs-lookup"><span data-stu-id="c28b2-111">Percentage of time the driver spent waiting for the GPU to finish using a locked resource (and [D3DLOCK\_DONOTWAIT](d3dlock.md) wasn't specified).</span></span>

</dd> <dt>

<span data-ttu-id="c28b2-112">**Waitingforgputoakzeptmorecommandstimeprozent**</span><span class="sxs-lookup"><span data-stu-id="c28b2-112">**WaitingForGPUToAcceptMoreCommandsTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="c28b2-113">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c28b2-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c28b2-114">Der Prozentsatz der Zeit, die der Treiber auf die Verarbeitung einiger Befehle durch die GPU gewartet hat, bevor der Treiber mehr senden konnte.</span><span class="sxs-lookup"><span data-stu-id="c28b2-114">Percentage of time the driver spent waiting for the GPU to finish processing some commands before the driver could send more.</span></span> <span data-ttu-id="c28b2-115">Dies gibt an, dass der Treiber nicht mehr genügend Platz zum Senden von Befehlen an die GPU hat.</span><span class="sxs-lookup"><span data-stu-id="c28b2-115">This indicates the driver has run out of room to send commands to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="c28b2-116">**Waitingforgputostaywithinlatencytimeprozent**</span><span class="sxs-lookup"><span data-stu-id="c28b2-116">**WaitingForGPUToStayWithinLatencyTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="c28b2-117">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c28b2-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c28b2-118">Der Prozentsatz der Zeit, die der Treiber gewartet hat, bis die GPU-Latenz auf weniger als drei renderingframes reduziert wurde.</span><span class="sxs-lookup"><span data-stu-id="c28b2-118">Percentage of time the driver spent waiting for the GPU latency to reduce to less than three rendering frames.</span></span>

<span data-ttu-id="c28b2-119">Wenn eine Anwendung GPU-begrenzt ist, muss der Treiber die CPU so lange einstellen, bis die GPU innerhalb von drei Frames erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="c28b2-119">If an application is GPU-limited, the driver must stall the CPU until the GPU gets within three frames.</span></span> <span data-ttu-id="c28b2-120">Dadurch wird verhindert, dass eine Anwendung eine große Anzahl von renderingaufrufen in die Warteschlange eingereiht, was die Wartezeit zwischen dem Zeitpunkt, zu dem der Benutzer neue Daten eingibt, und dem Zeitpunkt, zu dem der Benutzer die Ergebnisse dieser Eingabe sieht</span><span class="sxs-lookup"><span data-stu-id="c28b2-120">This prevents an application from queuing up many seconds' worth of rendering calls which may dramatically increase the latency between when the user inputs new data and when the user sees the results of that input.</span></span> <span data-ttu-id="c28b2-121">Im Allgemeinen kann der Treiber überprüfen, wie oft der [**vorhandene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) aufgerufen wird, um zu verhindern, dass mehr als drei Frames der Rendering-Arbeit in die Warteschlange eingereiht werden.</span><span class="sxs-lookup"><span data-stu-id="c28b2-121">In general, the driver can track the number of times [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) is called to prevent queuing up more than three frames of rendering work.</span></span>

</dd> <dt>

<span data-ttu-id="c28b2-122">**Waitingforgpuexclusiveresourcetimeprozent**</span><span class="sxs-lookup"><span data-stu-id="c28b2-122">**WaitingForGPUExclusiveResourceTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="c28b2-123">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c28b2-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c28b2-124">Der Prozentsatz der Zeit, die der Treiber auf eine Ressource gewartet hat, die nicht Pipeline (parallel betrieben) werden kann.</span><span class="sxs-lookup"><span data-stu-id="c28b2-124">Percentage of time the driver spent waiting for a resource that cannot be pipelined (that is operated in parallel).</span></span> <span data-ttu-id="c28b2-125">Eine Anwendung kann aus Leistungsgründen die Verwendung einer Ressource ohne Pipelines vermeiden.</span><span class="sxs-lookup"><span data-stu-id="c28b2-125">An application may want to avoid using a non-pipelined resource for performance reasons.</span></span>

</dd> <dt>

<span data-ttu-id="c28b2-126">**Waitingforgpuothertimeprozent**</span><span class="sxs-lookup"><span data-stu-id="c28b2-126">**WaitingForGPUOtherTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="c28b2-127">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c28b2-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c28b2-128">Der Prozentsatz der Zeit, die der Treiber auf die Verarbeitung anderer GPU gewartet hat.</span><span class="sxs-lookup"><span data-stu-id="c28b2-128">Percentage of time the driver spent waiting for other GPU processing.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c28b2-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c28b2-129">Remarks</span></span>

<span data-ttu-id="c28b2-130">Diese Metriken helfen, zu bestimmen, wann ein Treiber wartet und worauf er wartet.</span><span class="sxs-lookup"><span data-stu-id="c28b2-130">These metrics help identify when a driver is waiting and what it is waiting for.</span></span> <span data-ttu-id="c28b2-131">Hohe Prozentsätze sind nicht notwendigerweise ein Problem.</span><span class="sxs-lookup"><span data-stu-id="c28b2-131">High percentages are not necessarily a problem.</span></span>

<span data-ttu-id="c28b2-132">Diese systemweiten Metriken können oder nicht implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="c28b2-132">These system-global metrics may or may not be implemented.</span></span> <span data-ttu-id="c28b2-133">Abhängig von der jeweiligen Hardware unterstützen diese Metriken möglicherweise nicht mehrere Abfragen gleichzeitig.</span><span class="sxs-lookup"><span data-stu-id="c28b2-133">Depending on the specific hardware, these metrics may not support multiple queries simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="c28b2-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c28b2-134">Requirements</span></span>



| <span data-ttu-id="c28b2-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c28b2-135">Requirement</span></span> | <span data-ttu-id="c28b2-136">Wert</span><span class="sxs-lookup"><span data-stu-id="c28b2-136">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c28b2-137">Header</span><span class="sxs-lookup"><span data-stu-id="c28b2-137">Header</span></span><br/> | <dl> <span data-ttu-id="c28b2-138"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="c28b2-138"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c28b2-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c28b2-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c28b2-140">Direct3D-Strukturen</span><span class="sxs-lookup"><span data-stu-id="c28b2-140">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="c28b2-141">**GetData**</span><span class="sxs-lookup"><span data-stu-id="c28b2-141">**GetData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
