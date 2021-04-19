---
description: Flags, die zum Angeben der Erstellungs Optionen für ein Mesh verwendet werden.
ms.assetid: 1a5a6b3f-34f4-4338-9ffe-8f95f6f0c385
title: D3DX10_MESH-Enumeration (D3DX10Mesh. h)
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
ms.openlocfilehash: c2387024512a42c0a9e06ac1818b0282121cd0eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361890"
---
# <a name="d3dx10_mesh-enumeration"></a><span data-ttu-id="3e519-103">D3dx10 \_ Mesh-Enumeration</span><span class="sxs-lookup"><span data-stu-id="3e519-103">D3DX10\_MESH enumeration</span></span>

<span data-ttu-id="3e519-104">Flags, die zum Angeben der Erstellungs Optionen für ein Mesh verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3e519-104">Flags used to specify creation options for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e519-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e519-105">Syntax</span></span>


```C++
typedef enum D3DX10_MESH { 
  D3DX10_MESH_32_BIT        = 0x001,
  D3DX10_MESH_GS_ADJACENCY  = 0x004
} D3DX10_MESH, *LPD3DX10_MESH;
```



## <a name="constants"></a><span data-ttu-id="3e519-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="3e519-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3e519-107"><span id="D3DX10_MESH_32_BIT"></span><span id="d3dx10_mesh_32_bit"></span>**D3dx10 \_ Mesh \_ 32- \_ Bit**</span><span class="sxs-lookup"><span data-stu-id="3e519-107"><span id="D3DX10_MESH_32_BIT"></span><span id="d3dx10_mesh_32_bit"></span>**D3DX10\_MESH\_32\_BIT**</span></span>
</dt> <dd>

<span data-ttu-id="3e519-108">Das Mesh verfügt über 32-Bit-Indizes anstelle von 16-Bit-Indizes.</span><span class="sxs-lookup"><span data-stu-id="3e519-108">The mesh has 32-bit indices instead of 16-bit indices.</span></span> <span data-ttu-id="3e519-109">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="3e519-109">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="3e519-110"><span id="D3DX10_MESH_GS_ADJACENCY"></span><span id="d3dx10_mesh_gs_adjacency"></span>**D3dx10 \_ Mesh-Sicherheit \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3e519-110"><span id="D3DX10_MESH_GS_ADJACENCY"></span><span id="d3dx10_mesh_gs_adjacency"></span>**D3DX10\_MESH\_GS\_ADJACENCY**</span></span>
</dt> <dd>

<span data-ttu-id="3e519-111">Signalisiert, dass das Mesh Geometrie-Shader-Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="3e519-111">Signals that the mesh contains geometry shader adjacency data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3e519-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3e519-112">Remarks</span></span>

<span data-ttu-id="3e519-113">Ein 32-Bit-Mesh (D3DXMESH \_ 32 Bit) kann theoretisch (2 ³ ²)-1 Gesichter und Scheitel Punkte unterstützen.</span><span class="sxs-lookup"><span data-stu-id="3e519-113">A 32-bit mesh (D3DXMESH\_32BIT) can theoretically support (2³²)-1 faces and vertices.</span></span> <span data-ttu-id="3e519-114">Das belegen von Speicher für ein Mesh, das auf einem 32-Bit-Betriebssystem groß ist, ist jedoch nicht praktikabel.</span><span class="sxs-lookup"><span data-stu-id="3e519-114">However, allocating memory for a mesh that large on a 32-bit operating system is not practical.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e519-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3e519-115">Requirements</span></span>



| <span data-ttu-id="3e519-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3e519-116">Requirement</span></span> | <span data-ttu-id="3e519-117">Wert</span><span class="sxs-lookup"><span data-stu-id="3e519-117">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e519-118">Header</span><span class="sxs-lookup"><span data-stu-id="3e519-118">Header</span></span><br/> | <dl> <span data-ttu-id="3e519-119"><dt>D3DX10Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e519-119"><dt>D3DX10Mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e519-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e519-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e519-121">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="3e519-121">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




