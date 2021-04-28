---
description: 'D3DXMESH-Enumeration: Flags, die zum Angeben von Erstellungsoptionen für ein Gitternetz verwendet werden.'
ms.assetid: c94e19ab-8024-4a28-9d1a-6d57707c3a52
title: D3DXMESH-Enumeration (D3dx9mesh.h)
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
ms.openlocfilehash: a312c2618960691184182039afe38acc8947eb6a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098098"
---
# <a name="d3dxmesh-enumeration"></a><span data-ttu-id="d1bb8-103">D3DXMESH-Enumeration</span><span class="sxs-lookup"><span data-stu-id="d1bb8-103">D3DXMESH enumeration</span></span>

<span data-ttu-id="d1bb8-104">Flags, die zum Angeben von Erstellungsoptionen für ein Gitternetz verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d1bb8-104">Flags used to specify creation options for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1bb8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1bb8-105">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="d1bb8-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="d1bb8-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d1bb8-107"><span id="D3DXMESH_32BIT"></span><span id="d3dxmesh_32bit"></span>**D3DXMESH \_ 32 BIT**</span><span class="sxs-lookup"><span data-stu-id="d1bb8-107"><span id="D3DXMESH_32BIT"></span><span id="d3dxmesh_32bit"></span>**D3DXMESH\_32BIT**</span></span>
</dt> <dd>

<span data-ttu-id="d1bb8-108">Das Gitternetz verfügt über 32-Bit-Indizes anstelle von 16-Bit-Indizes.</span><span class="sxs-lookup"><span data-stu-id="d1bb8-108">The mesh has 32-bit indices instead of 16-bit indices.</span></span> <span data-ttu-id="d1bb8-109">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="d1bb8-109">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="d1bb8-110"><span id="D3DXMESH_DONOTCLIP"></span><span id="d3dxmesh_donotclip"></span>**D3DXMESH \_ DONOTCLIP**</span><span class="sxs-lookup"><span data-stu-id="d1bb8-110"><span id="D3DXMESH_DONOTCLIP"></span><span id="d3dxmesh_donotclip"></span>**D3DXMESH\_DONOTCLIP**</span></span>
</dt> <dd>

<span data-ttu-id="d1bb8-111">Verwenden Sie das [**D3DUSAGE \_ DONOTCLIP-Verwendungsflag**](d3dusage.md) für Scheitelpunkt- und Indexpuffer.</span><span class="sxs-lookup"><span data-stu-id="d1bb8-111">Use the [**D3DUSAGE\_DONOTCLIP**](d3dusage.md) usage flag for vertex and index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="d1bb8-112"><span id="D3DXMESH_POINTS"></span><span id="d3dxmesh_points"></span>**D3DXMESH-PUNKTE \_**</span><span class="sxs-lookup"><span data-stu-id="d1bb8-112"><span id="D3DXMESH_POINTS"></span><span id="d3dxmesh_points"></span>**D3DXMESH\_POINTS**</span></span>
</dt> <dd>

<span data-ttu-id="d1bb8-113">Verwenden Sie das [**D3DUSAGE \_ POINTS-Verwendungsflag**](d3dusage.md) für Scheitelpunkt- und Indexpuffer.</span><span class="sxs-lookup"><span data-stu-id="d1bb8-113">Use the [**D3DUSAGE\_POINTS**](d3dusage.md) usage flag for vertex and index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="d1bb8-114"><span id="D3DXMESH_RTPATCHES"></span><span id="d3dxmesh_rtpatches"></span>**D3DXMESH \_ RTPATCHES**</span><span class="sxs-lookup"><span data-stu-id="d1bb8-114"><span id="D3DXMESH_RTPATCHES"></span><span id="d3dxmesh_rtpatches"></span>**D3DXMESH\_RTPATCHES**</span></span>
</dt> <dd>

<span data-ttu-id="d1bb8-115">Verwenden Sie das [**D3DUSAGE \_ RTPATCHES-Verwendungsflag**](d3dusage.md) für Scheitelpunkt- und Indexpuffer.</span><span class="sxs-lookup"><span data-stu-id="d1bb8-115">Use the [**D3DUSAGE\_RTPATCHES**](d3dusage.md) usage flag for vertex and index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="d1bb8-116"><span id="D3DXMESH_NPATCHES"></span><span id="d3dxmesh_npatches"></span>**\_D3DXMESH-NPATCHES**</span><span class="sxs-lookup"><span data-stu-id="d1bb8-116"><span id="D3DXMESH_NPATCHES"></span><span id="d3dxmesh_npatches"></span>**D3DXMESH\_NPATCHES**</span></span>
</dt> <dd>

<span data-ttu-id="d1bb8-117">Wenn Sie dieses Flag angeben, werden der Scheitelpunkt und der Indexpuffer des Gitternetzes mit dem [**\_ NPATCHES-Flag D3DUSAGE**](d3dusage.md) erstellt.</span><span class="sxs-lookup"><span data-stu-id="d1bb8-117">Specifying this flag causes the vertex and index buffer of the mesh to be created with [**D3DUSAGE\_NPATCHES**](d3dusage.md) flag.</span></span> <span data-ttu-id="d1bb8-118">Dies ist erforderlich, wenn das Gittermodellobjekt mithilfe der N-Patch-Erweiterung mit Direct3D gerendert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d1bb8-118">This is required if the mesh object is to be rendered using N-patch enhancement using Direct3D.</span></span>

</dd> <dt>

<span data-ttu-id="d1bb8-119"><span id="D3DXMESH_VB_SYSTEMMEM"></span><span id="d3dxmesh_vb_systemmem"></span>**D3DXMESH \_ VB \_ SYSTEMMEM**</span><span class="sxs-lookup"><span data-stu-id="d1bb8-119"><span id="D3DXMESH_VB_SYSTEMMEM"></span><span id="d3dxmesh_vb_systemmem"></span>**D3DXMESH\_VB\_SYSTEMMEM**</span></span>
</dt> <dd>

<span data-ttu-id="d1bb8-120">Verwenden Sie das [**D3DPOOL \_ SYSTEMMEM-Verwendungsflag**](./d3dpool.md) für Scheitelpunktpuffer.</span><span class="sxs-lookup"><span data-stu-id="d1bb8-120">Use the [**D3DPOOL\_SYSTEMMEM**](./d3dpool.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="d1bb8-121"><span id="D3DXMESH_VB_MANAGED"></span><span id="d3dxmesh_vb_managed"></span>**D3DXMESH \_ VB \_ VERWALTET**</span><span class="sxs-lookup"><span data-stu-id="d1bb8-121"><span id="D3DXMESH_VB_MANAGED"></span><span id="d3dxmesh_vb_managed"></span>**D3DXMESH\_VB\_MANAGED**</span></span>
</dt> <dd>

<span data-ttu-id="d1bb8-122">Verwenden Sie das [**D3DPOOL \_ MANAGED-Verwendungsflag**](./d3dpool.md) für Scheitelpunktpuffer.</span><span class="sxs-lookup"><span data-stu-id="d1bb8-122">Use the [**D3DPOOL\_MANAGED**](./d3dpool.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="d1bb8-123"><span id="D3DXMESH_VB_WRITEONLY"></span><span id="d3dxmesh_vb_writeonly"></span>**D3DXMESH \_ VB \_ WRITEONLY**</span><span class="sxs-lookup"><span data-stu-id="d1bb8-123"><span id="D3DXMESH_VB_WRITEONLY"></span><span id="d3dxmesh_vb_writeonly"></span>**D3DXMESH\_VB\_WRITEONLY**</span></span>
</dt> <dd>

<span data-ttu-id="d1bb8-124">Verwenden Sie [**das D3DUSAGE \_ WRITEONLY-Verwendungsflag**](d3dusage.md) für Scheitelpunktpuffer.</span><span class="sxs-lookup"><span data-stu-id="d1bb8-124">Use the [**D3DUSAGE\_WRITEONLY**](d3dusage.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="d1bb8-125"><span id="D3DXMESH_VB_DYNAMIC"></span><span id="d3dxmesh_vb_dynamic"></span>**D3DXMESH \_ VB \_ DYNAMIC**</span><span class="sxs-lookup"><span data-stu-id="d1bb8-125"><span id="D3DXMESH_VB_DYNAMIC"></span><span id="d3dxmesh_vb_dynamic"></span>**D3DXMESH\_VB\_DYNAMIC**</span></span>
</dt> <dd>

<span data-ttu-id="d1bb8-126">Verwenden Sie [**das D3DUSAGE DYNAMIC-Verwendungsflag \_**](d3dusage.md) für Scheitelpunktpuffer.</span><span class="sxs-lookup"><span data-stu-id="d1bb8-126">Use the [**D3DUSAGE\_DYNAMIC**](d3dusage.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="d1bb8-127"><span id="D3DXMESH_VB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_vb_softwareprocessing"></span>**D3DXMESH \_ VB \_ SOFTWAREPROCESSING**</span><span class="sxs-lookup"><span data-stu-id="d1bb8-127"><span id="D3DXMESH_VB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_vb_softwareprocessing"></span>**D3DXMESH\_VB\_SOFTWAREPROCESSING**</span></span>
</dt> <dd>

<span data-ttu-id="d1bb8-128">Verwenden Sie [**das D3DUSAGE \_ SOFTWAREPROCESSING-Verwendungsflag**](d3dusage.md) für Scheitelpunktpuffer.</span><span class="sxs-lookup"><span data-stu-id="d1bb8-128">Use the [**D3DUSAGE\_SOFTWAREPROCESSING**](d3dusage.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="d1bb8-129"><span id="D3DXMESH_IB_SYSTEMMEM"></span><span id="d3dxmesh_ib_systemmem"></span>**D3DXMESH \_ IB \_ SYSTEMMEM**</span><span class="sxs-lookup"><span data-stu-id="d1bb8-129"><span id="D3DXMESH_IB_SYSTEMMEM"></span><span id="d3dxmesh_ib_systemmem"></span>**D3DXMESH\_IB\_SYSTEMMEM**</span></span>
</dt> <dd>

<span data-ttu-id="d1bb8-130">Verwenden Sie [**das D3DPOOL \_ SYSTEMMEM-Verwendungsflag**](./d3dpool.md) für Indexpuffer.</span><span class="sxs-lookup"><span data-stu-id="d1bb8-130">Use the [**D3DPOOL\_SYSTEMMEM**](./d3dpool.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="d1bb8-131"><span id="D3DXMESH_IB_MANAGED"></span><span id="d3dxmesh_ib_managed"></span>**D3DXMESH \_ IB \_ MANAGED**</span><span class="sxs-lookup"><span data-stu-id="d1bb8-131"><span id="D3DXMESH_IB_MANAGED"></span><span id="d3dxmesh_ib_managed"></span>**D3DXMESH\_IB\_MANAGED**</span></span>
</dt> <dd>

<span data-ttu-id="d1bb8-132">Verwenden Sie [**das D3DPOOL \_ MANAGED-Verwendungsflag**](./d3dpool.md) für Indexpuffer.</span><span class="sxs-lookup"><span data-stu-id="d1bb8-132">Use the [**D3DPOOL\_MANAGED**](./d3dpool.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="d1bb8-133"><span id="D3DXMESH_IB_WRITEONLY"></span><span id="d3dxmesh_ib_writeonly"></span>**D3DXMESH \_ IB \_ WRITEONLY**</span><span class="sxs-lookup"><span data-stu-id="d1bb8-133"><span id="D3DXMESH_IB_WRITEONLY"></span><span id="d3dxmesh_ib_writeonly"></span>**D3DXMESH\_IB\_WRITEONLY**</span></span>
</dt> <dd>

<span data-ttu-id="d1bb8-134">Verwenden Sie [**das D3DUSAGE \_ WRITEONLY-Verwendungsflag**](d3dusage.md) für Indexpuffer.</span><span class="sxs-lookup"><span data-stu-id="d1bb8-134">Use the [**D3DUSAGE\_WRITEONLY**](d3dusage.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="d1bb8-135"><span id="D3DXMESH_IB_DYNAMIC"></span><span id="d3dxmesh_ib_dynamic"></span>**D3DXMESH \_ IB \_ DYNAMIC**</span><span class="sxs-lookup"><span data-stu-id="d1bb8-135"><span id="D3DXMESH_IB_DYNAMIC"></span><span id="d3dxmesh_ib_dynamic"></span>**D3DXMESH\_IB\_DYNAMIC**</span></span>
</dt> <dd>

<span data-ttu-id="d1bb8-136">Verwenden Sie [**das D3DUSAGE \_ DYNAMIC-Verwendungsflag**](d3dusage.md) für Indexpuffer.</span><span class="sxs-lookup"><span data-stu-id="d1bb8-136">Use the [**D3DUSAGE\_DYNAMIC**](d3dusage.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="d1bb8-137"><span id="D3DXMESH_IB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_ib_softwareprocessing"></span>**D3DXMESH \_ IB \_ SOFTWAREPROCESSING**</span><span class="sxs-lookup"><span data-stu-id="d1bb8-137"><span id="D3DXMESH_IB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_ib_softwareprocessing"></span>**D3DXMESH\_IB\_SOFTWAREPROCESSING**</span></span>
</dt> <dd>

<span data-ttu-id="d1bb8-138">Verwenden Sie [**das D3DUSAGE \_ SOFTWAREPROCESSING-Verwendungsflag**](d3dusage.md) für Indexpuffer.</span><span class="sxs-lookup"><span data-stu-id="d1bb8-138">Use the [**D3DUSAGE\_SOFTWAREPROCESSING**](d3dusage.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="d1bb8-139"><span id="D3DXMESH_VB_SHARE"></span><span id="d3dxmesh_vb_share"></span>**D3DXMESH \_ \_ VB-FREIGABE**</span><span class="sxs-lookup"><span data-stu-id="d1bb8-139"><span id="D3DXMESH_VB_SHARE"></span><span id="d3dxmesh_vb_share"></span>**D3DXMESH\_VB\_SHARE**</span></span>
</dt> <dd>

<span data-ttu-id="d1bb8-140">Erzwingt, dass die geklonten Gitternetze Scheitelpunktpuffer freigeben.</span><span class="sxs-lookup"><span data-stu-id="d1bb8-140">Forces the cloned meshes to share vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="d1bb8-141"><span id="D3DXMESH_USEHWONLY"></span><span id="d3dxmesh_usehwonly"></span>**D3DXMESH \_ USEHWONLY**</span><span class="sxs-lookup"><span data-stu-id="d1bb8-141"><span id="D3DXMESH_USEHWONLY"></span><span id="d3dxmesh_usehwonly"></span>**D3DXMESH\_USEHWONLY**</span></span>
</dt> <dd>

<span data-ttu-id="d1bb8-142">Verwenden Sie nur die Hardwareverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="d1bb8-142">Use hardware processing only.</span></span> <span data-ttu-id="d1bb8-143">Bei Geräten im gemischten Modus wird dieses Flag dazu führen, dass das System Hardware verwendet (sofern dies in der Hardware unterstützt wird) oder standardmäßig die Softwareverarbeitung verwendet.</span><span class="sxs-lookup"><span data-stu-id="d1bb8-143">For mixed-mode device, this flag will cause the system to use hardware (if supported in hardware) or will default to software processing.</span></span>

</dd> <dt>

<span data-ttu-id="d1bb8-144"><span id="D3DXMESH_SYSTEMMEM"></span><span id="d3dxmesh_systemmem"></span>**D3DXMESH \_ SYSTEMMEM**</span><span class="sxs-lookup"><span data-stu-id="d1bb8-144"><span id="D3DXMESH_SYSTEMMEM"></span><span id="d3dxmesh_systemmem"></span>**D3DXMESH\_SYSTEMMEM**</span></span>
</dt> <dd>

<span data-ttu-id="d1bb8-145">Entspricht der Angabe von D3DXMESH \_ VB \_ SYSTEMMEM und D3DXMESH \_ IB \_ SYSTEMMEM.</span><span class="sxs-lookup"><span data-stu-id="d1bb8-145">Equivalent to specifying both D3DXMESH\_VB\_SYSTEMMEM and D3DXMESH\_IB\_SYSTEMMEM.</span></span>

</dd> <dt>

<span data-ttu-id="d1bb8-146"><span id="D3DXMESH_MANAGED"></span><span id="d3dxmesh_managed"></span>**D3DXMESH \_ VERWALTET**</span><span class="sxs-lookup"><span data-stu-id="d1bb8-146"><span id="D3DXMESH_MANAGED"></span><span id="d3dxmesh_managed"></span>**D3DXMESH\_MANAGED**</span></span>
</dt> <dd>

<span data-ttu-id="d1bb8-147">Entspricht der Angabe von D3DXMESH \_ VB \_ MANAGED und D3DXMESH \_ IB \_ MANAGED.</span><span class="sxs-lookup"><span data-stu-id="d1bb8-147">Equivalent to specifying both D3DXMESH\_VB\_MANAGED and D3DXMESH\_IB\_MANAGED.</span></span>

</dd> <dt>

<span data-ttu-id="d1bb8-148"><span id="D3DXMESH_WRITEONLY"></span><span id="d3dxmesh_writeonly"></span>**D3DXMESH \_ WRITEONLY**</span><span class="sxs-lookup"><span data-stu-id="d1bb8-148"><span id="D3DXMESH_WRITEONLY"></span><span id="d3dxmesh_writeonly"></span>**D3DXMESH\_WRITEONLY**</span></span>
</dt> <dd>

<span data-ttu-id="d1bb8-149">Entspricht der Angabe von D3DXMESH \_ VB \_ WRITEONLY und D3DXMESH \_ IB \_ WRITEONLY.</span><span class="sxs-lookup"><span data-stu-id="d1bb8-149">Equivalent to specifying both D3DXMESH\_VB\_WRITEONLY and D3DXMESH\_IB\_WRITEONLY.</span></span>

</dd> <dt>

<span data-ttu-id="d1bb8-150"><span id="D3DXMESH_DYNAMIC"></span><span id="d3dxmesh_dynamic"></span>**D3DXMESH \_ DYNAMIC**</span><span class="sxs-lookup"><span data-stu-id="d1bb8-150"><span id="D3DXMESH_DYNAMIC"></span><span id="d3dxmesh_dynamic"></span>**D3DXMESH\_DYNAMIC**</span></span>
</dt> <dd>

<span data-ttu-id="d1bb8-151">Entspricht der Angabe von D3DXMESH \_ VB \_ DYNAMIC und D3DXMESH \_ IB \_ DYNAMIC.</span><span class="sxs-lookup"><span data-stu-id="d1bb8-151">Equivalent to specifying both D3DXMESH\_VB\_DYNAMIC and D3DXMESH\_IB\_DYNAMIC.</span></span>

</dd> <dt>

<span data-ttu-id="d1bb8-152"><span id="D3DXMESH_SOFTWAREPROCESSING"></span><span id="d3dxmesh_softwareprocessing"></span>**D3DXMESH \_ SOFTWAREPROCESSING**</span><span class="sxs-lookup"><span data-stu-id="d1bb8-152"><span id="D3DXMESH_SOFTWAREPROCESSING"></span><span id="d3dxmesh_softwareprocessing"></span>**D3DXMESH\_SOFTWAREPROCESSING**</span></span>
</dt> <dd>

<span data-ttu-id="d1bb8-153">Entspricht der Angabe von D3DXMESH \_ VB \_ SOFTWAREPROCESSING und D3DXMESH \_ IB \_ SOFTWAREPROCESSING.</span><span class="sxs-lookup"><span data-stu-id="d1bb8-153">Equivalent to specifying both D3DXMESH\_VB\_SOFTWAREPROCESSING and D3DXMESH\_IB\_SOFTWAREPROCESSING.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1bb8-154">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d1bb8-154">Remarks</span></span>

<span data-ttu-id="d1bb8-155">Ein 32-Bit-Gitternetz (D3DXMESH \_ 32BIT) kann theoretisch (2^32)-1 Gesichter und Scheitelpunkte unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d1bb8-155">A 32-bit mesh (D3DXMESH\_32BIT) can theoretically support (2^32)-1 faces and vertices.</span></span> <span data-ttu-id="d1bb8-156">Die Zuweisung von Arbeitsspeicher für ein Gitternetz, das auf einem 32-Bit-Betriebssystem groß ist, ist jedoch nicht praktikabel.</span><span class="sxs-lookup"><span data-stu-id="d1bb8-156">However, allocating memory for a mesh that large on a 32-bit operating system is not practical.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1bb8-157">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d1bb8-157">Requirements</span></span>



| <span data-ttu-id="d1bb8-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d1bb8-158">Requirement</span></span> | <span data-ttu-id="d1bb8-159">Wert</span><span class="sxs-lookup"><span data-stu-id="d1bb8-159">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1bb8-160">Header</span><span class="sxs-lookup"><span data-stu-id="d1bb8-160">Header</span></span><br/> | <dl> <span data-ttu-id="d1bb8-161"><dt>D3dx9mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="d1bb8-161"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1bb8-162">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d1bb8-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1bb8-163">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="d1bb8-163">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
