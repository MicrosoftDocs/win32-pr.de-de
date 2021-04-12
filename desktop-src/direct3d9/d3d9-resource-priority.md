---
description: Konstanten, die verwendet werden, um die Priorität einer Ressource in SetPriority festzulegen.
ms.assetid: 98886349-883f-41c3-870b-e4a639977760
title: D3D9_RESOURCE_PRIORITY (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3D9_RESOURCE_PRIORITY_MINIMUM
- D3D9_RESOURCE_PRIORITY_LOW
- D3D9_RESOURCE_PRIORITY_NORMAL
- D3D9_RESOURCE_PRIORITY_HIGH
- D3D9_RESOURCE_PRIORITY_MAXIMUM
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 1ae5a54c7645db63b1023c3571f8181f4ee2daec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219465"
---
# <a name="d3d9_resource_priority"></a><span data-ttu-id="9847b-103">D3d9- \_ Ressourcen \_ Priorität</span><span class="sxs-lookup"><span data-stu-id="9847b-103">D3D9\_RESOURCE\_PRIORITY</span></span>

<span data-ttu-id="9847b-104">Konstanten, die verwendet werden, um die Priorität einer Ressource in [**SetPriority**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority)festzulegen.</span><span class="sxs-lookup"><span data-stu-id="9847b-104">Constants used to set the priority of a resource in [**SetPriority**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority).</span></span>



| <span data-ttu-id="9847b-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="9847b-105">Constant/value</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="9847b-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9847b-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3D9_RESOURCE_PRIORITY_MINIMUM"></span><span id="d3d9_resource_priority_minimum"></span><dl> <span data-ttu-id="9847b-107"><dt>**D3d9 \_ \_ \_ Minimale Ressourcen Priorität**</dt> <dt>0x28000000</dt></span><span class="sxs-lookup"><span data-stu-id="9847b-107"><dt>**D3D9\_RESOURCE\_PRIORITY\_MINIMUM**</dt> <dt>0x28000000</dt></span></span> </dl> | <span data-ttu-id="9847b-108">Die Ressource hat die niedrigste mögliche Priorität.</span><span class="sxs-lookup"><span data-stu-id="9847b-108">The resource has the lowest priority possible.</span></span> <span data-ttu-id="9847b-109">Diese Konstante markiert die Ressource als nicht verwendet und zum Entfernen.</span><span class="sxs-lookup"><span data-stu-id="9847b-109">This constant marks the resource as unused and for eviction.</span></span> <span data-ttu-id="9847b-110">Die Ressource sollte entfernt werden, sobald eine andere Ressource den von der Ressource belegten Speicherplatz benötigt.</span><span class="sxs-lookup"><span data-stu-id="9847b-110">The resource should be evicted as soon as another resource requires the memory space that the resource occupies.</span></span><br/>                                                                                                                                                                                                              |
| <span id="D3D9_RESOURCE_PRIORITY_LOW"></span><span id="d3d9_resource_priority_low"></span><dl> <span data-ttu-id="9847b-111"><dt>**D3d9 \_ Ressourcen \_ Priorität \_ niedrig**</dt> <dt>0x50.000.000</dt></span><span class="sxs-lookup"><span data-stu-id="9847b-111"><dt>**D3D9\_RESOURCE\_PRIORITY\_LOW**</dt> <dt>0x50000000</dt></span></span> </dl>             | <span data-ttu-id="9847b-112">Die Ressource wird mit niedriger Priorität geplant.</span><span class="sxs-lookup"><span data-stu-id="9847b-112">The resource is scheduled with low priority.</span></span> <span data-ttu-id="9847b-113">Die Platzierung der Ressource ist nicht wichtig, und das Betriebssystem führt nur wenig Arbeit aus, um einen Speicherort für die Ressource zu finden.</span><span class="sxs-lookup"><span data-stu-id="9847b-113">The placement of the resource is not critical, and the operating system performs minimal work to find a location for the resource.</span></span> <span data-ttu-id="9847b-114">Durch das Markieren einer Ressource mit niedriger Priorität können andere kritische Ressourcen den schnelleren Arbeitsspeicher belegen.</span><span class="sxs-lookup"><span data-stu-id="9847b-114">Marking a resource as low priority allows other more critical resources to occupy the faster memory.</span></span><br/>                                                                                                                                                      |
| <span id="D3D9_RESOURCE_PRIORITY_NORMAL"></span><span id="d3d9_resource_priority_normal"></span><dl> <span data-ttu-id="9847b-115"><dt>**D3d9 \_ Ressourcen \_ Priorität \_ Normal**</dt> <dt>0x78000000</dt></span><span class="sxs-lookup"><span data-stu-id="9847b-115"><dt>**D3D9\_RESOURCE\_PRIORITY\_NORMAL**</dt> <dt>0x78000000</dt></span></span> </dl>    | <span data-ttu-id="9847b-116">Die Ressource wird mit normaler Priorität geplant.</span><span class="sxs-lookup"><span data-stu-id="9847b-116">The resource is scheduled with normal priority.</span></span> <span data-ttu-id="9847b-117">Die Platzierung der Ressource ist wichtig für die Leistung, aber Sie ist nicht entscheidend.</span><span class="sxs-lookup"><span data-stu-id="9847b-117">The placement of the resource is important for performance, but it is not critical.</span></span> <span data-ttu-id="9847b-118">Das Betriebssystem sollte versuchen, die Ressource, die als normal gekennzeichnet ist, am bevorzugten Speicherort der Ressource anstatt an eine Ressource mit niedriger Priorität zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="9847b-118">The operating system should try to place the resource that is marked as normal in the resource's preferred location instead of a low-priority resource.</span></span> <span data-ttu-id="9847b-119">In der Regel werden Texturen als normal gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="9847b-119">Typically, textures are marked as normal.</span></span><br/>                                                                                                     |
| <span id="D3D9_RESOURCE_PRIORITY_HIGH"></span><span id="d3d9_resource_priority_high"></span><dl> <span data-ttu-id="9847b-120"><dt>**D3d9 \_ Ressourcen \_ Priorität \_ hoch**</dt> <dt>0xA0000000</dt></span><span class="sxs-lookup"><span data-stu-id="9847b-120"><dt>**D3D9\_RESOURCE\_PRIORITY\_HIGH**</dt> <dt>0xa0000000</dt></span></span> </dl>          | <span data-ttu-id="9847b-121">Die Ressource wird mit hoher Priorität geplant.</span><span class="sxs-lookup"><span data-stu-id="9847b-121">The resource is scheduled with high priority.</span></span> <span data-ttu-id="9847b-122">Die Platzierung der Ressource ist wichtig für die Leistung.</span><span class="sxs-lookup"><span data-stu-id="9847b-122">The placement of the resource is critical for performance.</span></span> <span data-ttu-id="9847b-123">Das Betriebssystem versucht immer, die Ressource, die im bevorzugten Speicherort der Ressource als hoch gekennzeichnet ist, anstelle einer Ressource mit niedriger Priorität oder normaler Priorität zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="9847b-123">The operating system always tries to place the resource that is marked as high in the resource's preferred location instead of a low-priority or normal-priority resource.</span></span> <span data-ttu-id="9847b-124">In der Regel werden Renderziele als hoch markiert.</span><span class="sxs-lookup"><span data-stu-id="9847b-124">Typically, render targets are marked as high.</span></span><br/>                                                                                                         |
| <span id="D3D9_RESOURCE_PRIORITY_MAXIMUM"></span><span id="d3d9_resource_priority_maximum"></span><dl> <span data-ttu-id="9847b-125"><dt>**D3d9 \_ \_ \_ Maximale Ressourcen Priorität**</dt> <dt>0xc8000000</dt></span><span class="sxs-lookup"><span data-stu-id="9847b-125"><dt>**D3D9\_RESOURCE\_PRIORITY\_MAXIMUM**</dt> <dt>0xc8000000</dt></span></span> </dl> | <span data-ttu-id="9847b-126">Die Ressource hat die maximal mögliche Priorität.</span><span class="sxs-lookup"><span data-stu-id="9847b-126">The resource has the maximum priority possible.</span></span> <span data-ttu-id="9847b-127">Diese Konstante markiert die Priorität der Ressource als vorläufig.</span><span class="sxs-lookup"><span data-stu-id="9847b-127">This constant marks the priority of the resource as soft-pinned.</span></span> <span data-ttu-id="9847b-128">Eine vorläufig fixierte Ressource wird nur dann aus dem Arbeitsspeicher entfernt, wenn es keine andere Möglichkeit gibt, die Arbeitsspeicher Anforderung eines DMA-Puffers zu beheben.</span><span class="sxs-lookup"><span data-stu-id="9847b-128">A soft-pinned resource is evicted from memory only if there is no other way of resolving the memory requirement of a DMA buffer.</span></span> <span data-ttu-id="9847b-129">Das Betriebssystem versucht, einen DMA-Puffer auf seine Mindestgröße aufzuteilen und alle anderen Ressourcen, die nicht fixiert und nicht vorläufig fixiert werden, zu entfernen, bevor eine vorläufig fixierte Ressource entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="9847b-129">The operating system attempts to split a DMA buffer to its minimum size and evict all other resources that are not pinned and not soft-pinned before it evicts a soft-pinned resource.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="9847b-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9847b-130">Remarks</span></span>

<span data-ttu-id="9847b-131">Werte, die nicht den maximalen Wert für die **d3d9- \_ Ressourcen \_ Priorität \_** und die **Maximale d3d9- \_ Ressourcen \_ Priorität \_** haben, werden vom Planer als Hinweise behandelt.</span><span class="sxs-lookup"><span data-stu-id="9847b-131">Values other than **D3D9\_RESOURCE\_PRIORITY\_MINIMUM** and **D3D9\_RESOURCE\_PRIORITY\_MAXIMUM** are treated as hints by the scheduler.</span></span>

<span data-ttu-id="9847b-132">Sie können andere Prioritätsstufen als die zuvor in diesem Thema definierten Werte verwenden.</span><span class="sxs-lookup"><span data-stu-id="9847b-132">You can use priority levels other than the values defined earlier in this topic.</span></span> <span data-ttu-id="9847b-133">Wenn Sie z. b. eine Ressource mit der Prioritätsstufe 0x78000001 markieren, wird angegeben, dass die Ressourcen Priorität etwas über dem normalen Wert liegt.</span><span class="sxs-lookup"><span data-stu-id="9847b-133">For example, marking a resource with a priority level of 0x78000001 indicates that the resource priority is slightly above normal.</span></span>

## <a name="requirements"></a><span data-ttu-id="9847b-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9847b-134">Requirements</span></span>



| <span data-ttu-id="9847b-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9847b-135">Requirement</span></span> | <span data-ttu-id="9847b-136">Wert</span><span class="sxs-lookup"><span data-stu-id="9847b-136">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9847b-137">Header</span><span class="sxs-lookup"><span data-stu-id="9847b-137">Header</span></span><br/> | <dl> <span data-ttu-id="9847b-138"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="9847b-138"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9847b-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9847b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9847b-140">Direct3D-Konstanten</span><span class="sxs-lookup"><span data-stu-id="9847b-140">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
