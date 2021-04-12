---
description: Flags, die zum Angeben der Erstellungs Optionen für ein Mesh verwendet werden.
ms.assetid: c94e19ab-8024-4a28-9d1a-6d57707c3a52
title: D3DXMESH-Enumeration (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESH
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 602eb38f2113b54ee02477faf3bdd15a6a924abc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354186"
---
# <a name="d3dxmesh-enumeration"></a><span data-ttu-id="fb838-103">D3DXMESH-Enumeration</span><span class="sxs-lookup"><span data-stu-id="fb838-103">D3DXMESH enumeration</span></span>

<span data-ttu-id="fb838-104">Flags, die zum Angeben der Erstellungs Optionen für ein Mesh verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fb838-104">Flags used to specify creation options for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb838-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb838-105">Syntax</span></span>


```C++
typedef enum D3DXMESH { 
  D3DXMESH_32BIT                  = 0x001,
  D3DXMESH_DONOTCLIP              = 0x002,
  D3DXMESH_POINTS                 = 0x004,
  D3DXMESH_RTPATCHES              = 0x008,
  D3DXMESH_NPATCHES               = 0x4000,
  D3DXMESH_VB_SYSTEMMEM           = 0x010,
  D3DXMESH_VB_MANAGED             = 0x020,
  D3DXMESH_VB_WRITEONLY           = 0x040,
  D3DXMESH_VB_DYNAMIC             = 0x080,
  D3DXMESH_VB_SOFTWAREPROCESSING  = 0x8000,
  D3DXMESH_IB_SYSTEMMEM           = 0x100,
  D3DXMESH_IB_MANAGED             = 0x200,
  D3DXMESH_IB_WRITEONLY           = 0x400,
  D3DXMESH_IB_DYNAMIC             = 0x800,
  D3DXMESH_IB_SOFTWAREPROCESSING  = 0x10000,
  D3DXMESH_VB_SHARE               = 0x1000,
  D3DXMESH_USEHWONLY              = 0x2000,
  D3DXMESH_SYSTEMMEM              = 0x110,
  D3DXMESH_MANAGED                = 0x220,
  D3DXMESH_WRITEONLY              = 0x440,
  D3DXMESH_DYNAMIC                = 0x880,
  D3DXMESH_SOFTWAREPROCESSING     = 0x18000
} D3DXMESH, *LPD3DXMESH;
```



## <a name="constants"></a><span data-ttu-id="fb838-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="fb838-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="fb838-107"><span id="D3DXMESH_32BIT"></span><span id="d3dxmesh_32bit"></span>**D3DXMESH \_ 32-Bit**</span><span class="sxs-lookup"><span data-stu-id="fb838-107"><span id="D3DXMESH_32BIT"></span><span id="d3dxmesh_32bit"></span>**D3DXMESH\_32BIT**</span></span>
</dt> <dd>

<span data-ttu-id="fb838-108">Das Mesh verfügt über 32-Bit-Indizes anstelle von 16-Bit-Indizes.</span><span class="sxs-lookup"><span data-stu-id="fb838-108">The mesh has 32-bit indices instead of 16-bit indices.</span></span> <span data-ttu-id="fb838-109">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="fb838-109">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="fb838-110"><span id="D3DXMESH_DONOTCLIP"></span><span id="d3dxmesh_donotclip"></span>**D3DXMESH \_ DoNotClip**</span><span class="sxs-lookup"><span data-stu-id="fb838-110"><span id="D3DXMESH_DONOTCLIP"></span><span id="d3dxmesh_donotclip"></span>**D3DXMESH\_DONOTCLIP**</span></span>
</dt> <dd>

<span data-ttu-id="fb838-111">Verwenden Sie das [**D3DUSAGE \_ DoNotClip**](d3dusage.md) -nutzungsflag für Scheitelpunkt-und Index Puffer.</span><span class="sxs-lookup"><span data-stu-id="fb838-111">Use the [**D3DUSAGE\_DONOTCLIP**](d3dusage.md) usage flag for vertex and index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="fb838-112"><span id="D3DXMESH_POINTS"></span><span id="d3dxmesh_points"></span>**D3DXMESH \_ Punkte**</span><span class="sxs-lookup"><span data-stu-id="fb838-112"><span id="D3DXMESH_POINTS"></span><span id="d3dxmesh_points"></span>**D3DXMESH\_POINTS**</span></span>
</dt> <dd>

<span data-ttu-id="fb838-113">Verwenden Sie das Usage-Flag [**D3DUSAGE \_ Points**](d3dusage.md) für Scheitelpunkt-und Index Puffer.</span><span class="sxs-lookup"><span data-stu-id="fb838-113">Use the [**D3DUSAGE\_POINTS**](d3dusage.md) usage flag for vertex and index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="fb838-114"><span id="D3DXMESH_RTPATCHES"></span><span id="d3dxmesh_rtpatches"></span>**D3DXMESH \_ rtpatches**</span><span class="sxs-lookup"><span data-stu-id="fb838-114"><span id="D3DXMESH_RTPATCHES"></span><span id="d3dxmesh_rtpatches"></span>**D3DXMESH\_RTPATCHES**</span></span>
</dt> <dd>

<span data-ttu-id="fb838-115">Verwenden Sie das [**D3DUSAGE \_ rtpatches**](d3dusage.md) Usage-Flag für Scheitelpunkt-und Index Puffer.</span><span class="sxs-lookup"><span data-stu-id="fb838-115">Use the [**D3DUSAGE\_RTPATCHES**](d3dusage.md) usage flag for vertex and index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="fb838-116"><span id="D3DXMESH_NPATCHES"></span><span id="d3dxmesh_npatches"></span>**D3DXMESH \_ npatches**</span><span class="sxs-lookup"><span data-stu-id="fb838-116"><span id="D3DXMESH_NPATCHES"></span><span id="d3dxmesh_npatches"></span>**D3DXMESH\_NPATCHES**</span></span>
</dt> <dd>

<span data-ttu-id="fb838-117">Die Angabe dieses Flags bewirkt, dass der Scheitelpunkt und der Index Puffer des Mesh mit dem [**D3DUSAGE \_ npatches**](d3dusage.md) -Flag erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="fb838-117">Specifying this flag causes the vertex and index buffer of the mesh to be created with [**D3DUSAGE\_NPATCHES**](d3dusage.md) flag.</span></span> <span data-ttu-id="fb838-118">Dies ist erforderlich, wenn das Mesh-Objekt mit der N-patcherweiterung mithilfe von Direct3D gerendert werden soll.</span><span class="sxs-lookup"><span data-stu-id="fb838-118">This is required if the mesh object is to be rendered using N-patch enhancement using Direct3D.</span></span>

</dd> <dt>

<span data-ttu-id="fb838-119"><span id="D3DXMESH_VB_SYSTEMMEM"></span><span id="d3dxmesh_vb_systemmem"></span>**D3DXMESH \_ vb \_ SystemMem**</span><span class="sxs-lookup"><span data-stu-id="fb838-119"><span id="D3DXMESH_VB_SYSTEMMEM"></span><span id="d3dxmesh_vb_systemmem"></span>**D3DXMESH\_VB\_SYSTEMMEM**</span></span>
</dt> <dd>

<span data-ttu-id="fb838-120">Verwenden Sie das [**D3DPOOL \_ SystemMem**](./d3dpool.md) -nutzungsflag für Scheitelpunkt Puffer.</span><span class="sxs-lookup"><span data-stu-id="fb838-120">Use the [**D3DPOOL\_SYSTEMMEM**](./d3dpool.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="fb838-121"><span id="D3DXMESH_VB_MANAGED"></span><span id="d3dxmesh_vb_managed"></span>**D3DXMESH \_ vb \_ verwaltet**</span><span class="sxs-lookup"><span data-stu-id="fb838-121"><span id="D3DXMESH_VB_MANAGED"></span><span id="d3dxmesh_vb_managed"></span>**D3DXMESH\_VB\_MANAGED**</span></span>
</dt> <dd>

<span data-ttu-id="fb838-122">Verwenden Sie das [**D3DPOOL \_ Managed**](./d3dpool.md) Usage-Flag für Scheitelpunkt Puffer.</span><span class="sxs-lookup"><span data-stu-id="fb838-122">Use the [**D3DPOOL\_MANAGED**](./d3dpool.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="fb838-123"><span id="D3DXMESH_VB_WRITEONLY"></span><span id="d3dxmesh_vb_writeonly"></span>**D3DXMESH \_ vb \_ schreibgeschützt**</span><span class="sxs-lookup"><span data-stu-id="fb838-123"><span id="D3DXMESH_VB_WRITEONLY"></span><span id="d3dxmesh_vb_writeonly"></span>**D3DXMESH\_VB\_WRITEONLY**</span></span>
</dt> <dd>

<span data-ttu-id="fb838-124">Verwenden Sie das [**D3DUSAGE \_ Write**](d3dusage.md) -use-Flag für Scheitel Punkte.</span><span class="sxs-lookup"><span data-stu-id="fb838-124">Use the [**D3DUSAGE\_WRITEONLY**](d3dusage.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="fb838-125"><span id="D3DXMESH_VB_DYNAMIC"></span><span id="d3dxmesh_vb_dynamic"></span>**D3DXMESH \_ vb \_ dynamisch**</span><span class="sxs-lookup"><span data-stu-id="fb838-125"><span id="D3DXMESH_VB_DYNAMIC"></span><span id="d3dxmesh_vb_dynamic"></span>**D3DXMESH\_VB\_DYNAMIC**</span></span>
</dt> <dd>

<span data-ttu-id="fb838-126">Verwenden Sie das [**D3DUSAGE \_ Dynamic**](d3dusage.md) Usage-Flag für Scheitelpunkt Puffer.</span><span class="sxs-lookup"><span data-stu-id="fb838-126">Use the [**D3DUSAGE\_DYNAMIC**](d3dusage.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="fb838-127"><span id="D3DXMESH_VB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_vb_softwareprocessing"></span>**D3DXMESH \_ vb- \_ softwareprocessing**</span><span class="sxs-lookup"><span data-stu-id="fb838-127"><span id="D3DXMESH_VB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_vb_softwareprocessing"></span>**D3DXMESH\_VB\_SOFTWAREPROCESSING**</span></span>
</dt> <dd>

<span data-ttu-id="fb838-128">Verwenden Sie das [**D3DUSAGE \_ softwareprocessing**](d3dusage.md) -nutzungsflag für Scheitelpunkt Puffer.</span><span class="sxs-lookup"><span data-stu-id="fb838-128">Use the [**D3DUSAGE\_SOFTWAREPROCESSING**](d3dusage.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="fb838-129"><span id="D3DXMESH_IB_SYSTEMMEM"></span><span id="d3dxmesh_ib_systemmem"></span>**D3DXMESH \_ IB-System Arbeitsspeicher \_**</span><span class="sxs-lookup"><span data-stu-id="fb838-129"><span id="D3DXMESH_IB_SYSTEMMEM"></span><span id="d3dxmesh_ib_systemmem"></span>**D3DXMESH\_IB\_SYSTEMMEM**</span></span>
</dt> <dd>

<span data-ttu-id="fb838-130">Verwenden Sie das [**D3DPOOL \_ SystemMem**](./d3dpool.md) -nutzungsflag für Index Puffer.</span><span class="sxs-lookup"><span data-stu-id="fb838-130">Use the [**D3DPOOL\_SYSTEMMEM**](./d3dpool.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="fb838-131"><span id="D3DXMESH_IB_MANAGED"></span><span id="d3dxmesh_ib_managed"></span>**D3DXMESH \_ IB \_ verwaltet**</span><span class="sxs-lookup"><span data-stu-id="fb838-131"><span id="D3DXMESH_IB_MANAGED"></span><span id="d3dxmesh_ib_managed"></span>**D3DXMESH\_IB\_MANAGED**</span></span>
</dt> <dd>

<span data-ttu-id="fb838-132">Verwenden Sie das [**D3DPOOL \_ Managed**](./d3dpool.md) Usage-Flag für Index Puffer.</span><span class="sxs-lookup"><span data-stu-id="fb838-132">Use the [**D3DPOOL\_MANAGED**](./d3dpool.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="fb838-133"><span id="D3DXMESH_IB_WRITEONLY"></span><span id="d3dxmesh_ib_writeonly"></span>**D3DXMESH \_ IB \_ schreibgeschützt**</span><span class="sxs-lookup"><span data-stu-id="fb838-133"><span id="D3DXMESH_IB_WRITEONLY"></span><span id="d3dxmesh_ib_writeonly"></span>**D3DXMESH\_IB\_WRITEONLY**</span></span>
</dt> <dd>

<span data-ttu-id="fb838-134">Verwenden Sie das [**D3DUSAGE \_ Write**](d3dusage.md) -use-Flag für Index Puffer.</span><span class="sxs-lookup"><span data-stu-id="fb838-134">Use the [**D3DUSAGE\_WRITEONLY**](d3dusage.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="fb838-135"><span id="D3DXMESH_IB_DYNAMIC"></span><span id="d3dxmesh_ib_dynamic"></span>**D3DXMESH \_ IB \_ dynamisch**</span><span class="sxs-lookup"><span data-stu-id="fb838-135"><span id="D3DXMESH_IB_DYNAMIC"></span><span id="d3dxmesh_ib_dynamic"></span>**D3DXMESH\_IB\_DYNAMIC**</span></span>
</dt> <dd>

<span data-ttu-id="fb838-136">Verwenden Sie das [**D3DUSAGE \_ Dynamic**](d3dusage.md) Usage-Flag für Index Puffer.</span><span class="sxs-lookup"><span data-stu-id="fb838-136">Use the [**D3DUSAGE\_DYNAMIC**](d3dusage.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="fb838-137"><span id="D3DXMESH_IB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_ib_softwareprocessing"></span>**D3DXMESH \_ IB- \_ softwareprocessing**</span><span class="sxs-lookup"><span data-stu-id="fb838-137"><span id="D3DXMESH_IB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_ib_softwareprocessing"></span>**D3DXMESH\_IB\_SOFTWAREPROCESSING**</span></span>
</dt> <dd>

<span data-ttu-id="fb838-138">Verwenden Sie das [**D3DUSAGE \_ softwareprocessing**](d3dusage.md) -nutzungsflag für Index Puffer.</span><span class="sxs-lookup"><span data-stu-id="fb838-138">Use the [**D3DUSAGE\_SOFTWAREPROCESSING**](d3dusage.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="fb838-139"><span id="D3DXMESH_VB_SHARE"></span><span id="d3dxmesh_vb_share"></span>**D3DXMESH \_ vb- \_ Freigabe**</span><span class="sxs-lookup"><span data-stu-id="fb838-139"><span id="D3DXMESH_VB_SHARE"></span><span id="d3dxmesh_vb_share"></span>**D3DXMESH\_VB\_SHARE**</span></span>
</dt> <dd>

<span data-ttu-id="fb838-140">Erzwingt, dass die geklonten Netzen Vertex-Puffer freigeben.</span><span class="sxs-lookup"><span data-stu-id="fb838-140">Forces the cloned meshes to share vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="fb838-141"><span id="D3DXMESH_USEHWONLY"></span><span id="d3dxmesh_usehwonly"></span>**D3DXMESH \_ usehweinzierl**</span><span class="sxs-lookup"><span data-stu-id="fb838-141"><span id="D3DXMESH_USEHWONLY"></span><span id="d3dxmesh_usehwonly"></span>**D3DXMESH\_USEHWONLY**</span></span>
</dt> <dd>

<span data-ttu-id="fb838-142">Verwenden Sie nur die Hardware Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="fb838-142">Use hardware processing only.</span></span> <span data-ttu-id="fb838-143">Bei Geräten mit gemischtem Modus bewirkt dieses Flag, dass das System Hardware verwendet (wenn es in der Hardware unterstützt wird) oder die Software Verarbeitung standardmäßig verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fb838-143">For mixed-mode device, this flag will cause the system to use hardware (if supported in hardware) or will default to software processing.</span></span>

</dd> <dt>

<span data-ttu-id="fb838-144"><span id="D3DXMESH_SYSTEMMEM"></span><span id="d3dxmesh_systemmem"></span>**D3DXMESH \_ SystemMem**</span><span class="sxs-lookup"><span data-stu-id="fb838-144"><span id="D3DXMESH_SYSTEMMEM"></span><span id="d3dxmesh_systemmem"></span>**D3DXMESH\_SYSTEMMEM**</span></span>
</dt> <dd>

<span data-ttu-id="fb838-145">Entspricht der Angabe von D3DXMESH \_ vb \_ SystemMem und D3DXMESH \_ IB \_ SystemMem.</span><span class="sxs-lookup"><span data-stu-id="fb838-145">Equivalent to specifying both D3DXMESH\_VB\_SYSTEMMEM and D3DXMESH\_IB\_SYSTEMMEM.</span></span>

</dd> <dt>

<span data-ttu-id="fb838-146"><span id="D3DXMESH_MANAGED"></span><span id="d3dxmesh_managed"></span>**D3DXMESH \_ verwaltet**</span><span class="sxs-lookup"><span data-stu-id="fb838-146"><span id="D3DXMESH_MANAGED"></span><span id="d3dxmesh_managed"></span>**D3DXMESH\_MANAGED**</span></span>
</dt> <dd>

<span data-ttu-id="fb838-147">Entspricht der Angabe von D3DXMESH \_ vb \_ Managed und D3DXMESH \_ IB \_ Managed.</span><span class="sxs-lookup"><span data-stu-id="fb838-147">Equivalent to specifying both D3DXMESH\_VB\_MANAGED and D3DXMESH\_IB\_MANAGED.</span></span>

</dd> <dt>

<span data-ttu-id="fb838-148"><span id="D3DXMESH_WRITEONLY"></span><span id="d3dxmesh_writeonly"></span>**D3DXMESH \_ schreiben**</span><span class="sxs-lookup"><span data-stu-id="fb838-148"><span id="D3DXMESH_WRITEONLY"></span><span id="d3dxmesh_writeonly"></span>**D3DXMESH\_WRITEONLY**</span></span>
</dt> <dd>

<span data-ttu-id="fb838-149">Entspricht der Angabe von D3DXMESH \_ vb \_ Write-only und D3DXMESH \_ IB \_ Write.</span><span class="sxs-lookup"><span data-stu-id="fb838-149">Equivalent to specifying both D3DXMESH\_VB\_WRITEONLY and D3DXMESH\_IB\_WRITEONLY.</span></span>

</dd> <dt>

<span data-ttu-id="fb838-150"><span id="D3DXMESH_DYNAMIC"></span><span id="d3dxmesh_dynamic"></span>**D3DXMESH \_ dynamisch**</span><span class="sxs-lookup"><span data-stu-id="fb838-150"><span id="D3DXMESH_DYNAMIC"></span><span id="d3dxmesh_dynamic"></span>**D3DXMESH\_DYNAMIC**</span></span>
</dt> <dd>

<span data-ttu-id="fb838-151">Äquivalent zum Angeben von D3DXMESH \_ vb \_ Dynamic und D3DXMESH \_ IB \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="fb838-151">Equivalent to specifying both D3DXMESH\_VB\_DYNAMIC and D3DXMESH\_IB\_DYNAMIC.</span></span>

</dd> <dt>

<span data-ttu-id="fb838-152"><span id="D3DXMESH_SOFTWAREPROCESSING"></span><span id="d3dxmesh_softwareprocessing"></span>**D3DXMESH \_ softwareprocessing**</span><span class="sxs-lookup"><span data-stu-id="fb838-152"><span id="D3DXMESH_SOFTWAREPROCESSING"></span><span id="d3dxmesh_softwareprocessing"></span>**D3DXMESH\_SOFTWAREPROCESSING**</span></span>
</dt> <dd>

<span data-ttu-id="fb838-153">Entspricht der Angabe von D3DXMESH \_ vb \_ softwareprocessing und D3DXMESH \_ IB \_ Software processing.</span><span class="sxs-lookup"><span data-stu-id="fb838-153">Equivalent to specifying both D3DXMESH\_VB\_SOFTWAREPROCESSING and D3DXMESH\_IB\_SOFTWAREPROCESSING.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fb838-154">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb838-154">Remarks</span></span>

<span data-ttu-id="fb838-155">Ein 32-Bit-Mesh (D3DXMESH \_ 32bit) kann theoretisch (2 ^ 32)-1 Gesichter und Scheitel Punkte unterstützen.</span><span class="sxs-lookup"><span data-stu-id="fb838-155">A 32-bit mesh (D3DXMESH\_32BIT) can theoretically support (2^32)-1 faces and vertices.</span></span> <span data-ttu-id="fb838-156">Das belegen von Speicher für ein Mesh, das auf einem 32-Bit-Betriebssystem groß ist, ist jedoch nicht praktikabel.</span><span class="sxs-lookup"><span data-stu-id="fb838-156">However, allocating memory for a mesh that large on a 32-bit operating system is not practical.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb838-157">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb838-157">Requirements</span></span>



| <span data-ttu-id="fb838-158">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fb838-158">Requirement</span></span> | <span data-ttu-id="fb838-159">Wert</span><span class="sxs-lookup"><span data-stu-id="fb838-159">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb838-160">Header</span><span class="sxs-lookup"><span data-stu-id="fb838-160">Header</span></span><br/> | <dl> <span data-ttu-id="fb838-161"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb838-161"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb838-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb838-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb838-163">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="fb838-163">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
