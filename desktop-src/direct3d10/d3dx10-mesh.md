---
description: 'D3DX10_MESH-Enumeration: Flags, die zum Angeben von Erstellungsoptionen für ein Gitternetz verwendet werden.'
ms.assetid: 1a5a6b3f-34f4-4338-9ffe-8f95f6f0c385
title: D3DX10_MESH-Enumeration (D3DX10Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_MESH
api_type:
- HeaderDef
api_location:
- D3DX10Mesh.h
ms.openlocfilehash: 2659783b0443396508465f9498eec86950f825bc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105438"
---
# <a name="d3dx10_mesh-enumeration"></a><span data-ttu-id="0292e-103">D3DX10 \_ MESH-Enumeration</span><span class="sxs-lookup"><span data-stu-id="0292e-103">D3DX10\_MESH enumeration</span></span>

<span data-ttu-id="0292e-104">Flags, die zum Angeben von Erstellungsoptionen für ein Gitternetz verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0292e-104">Flags used to specify creation options for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="0292e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0292e-105">Syntax</span></span>


```C++
typedef enum D3DX10_MESH { 
  D3DX10_MESH_32_BIT        = 0x001,
  D3DX10_MESH_GS_ADJACENCY  = 0x004
} D3DX10_MESH, *LPD3DX10_MESH;
```



## <a name="constants"></a><span data-ttu-id="0292e-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="0292e-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0292e-107"><span id="D3DX10_MESH_32_BIT"></span><span id="d3dx10_mesh_32_bit"></span>**D3DX10 \_ MESH \_ 32 \_ BIT**</span><span class="sxs-lookup"><span data-stu-id="0292e-107"><span id="D3DX10_MESH_32_BIT"></span><span id="d3dx10_mesh_32_bit"></span>**D3DX10\_MESH\_32\_BIT**</span></span>
</dt> <dd>

<span data-ttu-id="0292e-108">Das Gitternetz verfügt über 32-Bit-Indizes anstelle von 16-Bit-Indizes.</span><span class="sxs-lookup"><span data-stu-id="0292e-108">The mesh has 32-bit indices instead of 16-bit indices.</span></span> <span data-ttu-id="0292e-109">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="0292e-109">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="0292e-110"><span id="D3DX10_MESH_GS_ADJACENCY"></span><span id="d3dx10_mesh_gs_adjacency"></span>**D3DX10 \_ MESH \_ GS \_ ADJAZ**</span><span class="sxs-lookup"><span data-stu-id="0292e-110"><span id="D3DX10_MESH_GS_ADJACENCY"></span><span id="d3dx10_mesh_gs_adjacency"></span>**D3DX10\_MESH\_GS\_ADJACENCY**</span></span>
</dt> <dd>

<span data-ttu-id="0292e-111">Signalisiert, dass das Gitternetz Geometrie-Shader-Adjazenzdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="0292e-111">Signals that the mesh contains geometry shader adjacency data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0292e-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0292e-112">Remarks</span></span>

<span data-ttu-id="0292e-113">Ein 32-Bit-Gitternetz (D3DXMESH \_ 32BIT) kann theoretisch (2)-1 Gesichter und Scheitelpunkte unterstützen.</span><span class="sxs-lookup"><span data-stu-id="0292e-113">A 32-bit mesh (D3DXMESH\_32BIT) can theoretically support (2³²)-1 faces and vertices.</span></span> <span data-ttu-id="0292e-114">Die Zuweisung von Arbeitsspeicher für ein Gitternetz, das auf einem 32-Bit-Betriebssystem groß ist, ist jedoch nicht praktikabel.</span><span class="sxs-lookup"><span data-stu-id="0292e-114">However, allocating memory for a mesh that large on a 32-bit operating system is not practical.</span></span>

## <a name="requirements"></a><span data-ttu-id="0292e-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0292e-115">Requirements</span></span>



| <span data-ttu-id="0292e-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0292e-116">Requirement</span></span> | <span data-ttu-id="0292e-117">Wert</span><span class="sxs-lookup"><span data-stu-id="0292e-117">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0292e-118">Header</span><span class="sxs-lookup"><span data-stu-id="0292e-118">Header</span></span><br/> | <dl> <span data-ttu-id="0292e-119"><dt>D3DX10Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="0292e-119"><dt>D3DX10Mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0292e-120">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0292e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0292e-121">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="0292e-121">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




