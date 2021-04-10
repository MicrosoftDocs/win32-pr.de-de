---
description: Gibt an, welche Teile von Mesh-Daten vom Gerät verworfen werden sollen. Wird mit ID3DX10Mesh::D iscard verwendet.
ms.assetid: 8b3c22ab-1337-4a66-ae32-17bd1b73f624
title: D3DX10_MESH_DISCARD_FLAGS-Enumeration (D3DX10Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_MESH_DISCARD_FLAGS
api_type:
- HeaderDef
api_location:
- D3DX10Mesh.h
ms.openlocfilehash: 6640834cf81bfa5e4b6263d3b3cfbb1181bb16c9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961710"
---
# <a name="d3dx10_mesh_discard_flags-enumeration"></a><span data-ttu-id="6d2e6-104">D3dx10 \_ Mesh \_ Verwerfungs \_ Flags-Enumeration</span><span class="sxs-lookup"><span data-stu-id="6d2e6-104">D3DX10\_MESH\_DISCARD\_FLAGS enumeration</span></span>

<span data-ttu-id="6d2e6-105">Gibt an, welche Teile von Mesh-Daten vom Gerät verworfen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6d2e6-105">Specifies which pieces of mesh data to discard from the device.</span></span> <span data-ttu-id="6d2e6-106">Wird mit [**ID3DX10Mesh::D iscard**](id3dx10mesh-discard.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="6d2e6-106">Used with [**ID3DX10Mesh::Discard**](id3dx10mesh-discard.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6d2e6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d2e6-107">Syntax</span></span>


```C++
typedef enum D3DX10_MESH_DISCARD_FLAGS { 
  D3DX10_MESH_DISCARD_ATTRIBUTE_BUFFER  = 0x01,
  D3DX10_MESH_DISCARD_ATTRIBUTE_TABLE   = 0x02,
  D3DX10_MESH_DISCARD_POINTREPS         = 0x04,
  D3DX10_MESH_DISCARD_ADJACENCY         = 0x08,
  D3DX10_MESH_DISCARD_DEVICE_BUFFERS    = 0x10
} D3DX10_MESH_DISCARD_FLAGS, *LPD3DX10_MESH_DISCARD_FLAGS;
```



## <a name="constants"></a><span data-ttu-id="6d2e6-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="6d2e6-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6d2e6-109"><span id="D3DX10_MESH_DISCARD_ATTRIBUTE_BUFFER"></span><span id="d3dx10_mesh_discard_attribute_buffer"></span>**D3dx10 \_ Mesh \_ - \_ Attribut \_ Puffer verwerfen**</span><span class="sxs-lookup"><span data-stu-id="6d2e6-109"><span id="D3DX10_MESH_DISCARD_ATTRIBUTE_BUFFER"></span><span id="d3dx10_mesh_discard_attribute_buffer"></span>**D3DX10\_MESH\_DISCARD\_ATTRIBUTE\_BUFFER**</span></span>
</dt> <dd>

<span data-ttu-id="6d2e6-110">Verwerfen Sie den Attribut Puffer.</span><span class="sxs-lookup"><span data-stu-id="6d2e6-110">Discard the attribute buffer.</span></span>

</dd> <dt>

<span data-ttu-id="6d2e6-111"><span id="D3DX10_MESH_DISCARD_ATTRIBUTE_TABLE"></span><span id="d3dx10_mesh_discard_attribute_table"></span>**D3dx10 \_ Mesh \_ - \_ Attribut \_ Tabelle verwerfen**</span><span class="sxs-lookup"><span data-stu-id="6d2e6-111"><span id="D3DX10_MESH_DISCARD_ATTRIBUTE_TABLE"></span><span id="d3dx10_mesh_discard_attribute_table"></span>**D3DX10\_MESH\_DISCARD\_ATTRIBUTE\_TABLE**</span></span>
</dt> <dd>

<span data-ttu-id="6d2e6-112">Verwerfen Sie die Attribut Tabelle.</span><span class="sxs-lookup"><span data-stu-id="6d2e6-112">Discard the attribute table.</span></span>

</dd> <dt>

<span data-ttu-id="6d2e6-113"><span id="D3DX10_MESH_DISCARD_POINTREPS"></span><span id="d3dx10_mesh_discard_pointreps"></span>**D3dx10- \_ Mesh- \_ \_ pointreps verwerfen**</span><span class="sxs-lookup"><span data-stu-id="6d2e6-113"><span id="D3DX10_MESH_DISCARD_POINTREPS"></span><span id="d3dx10_mesh_discard_pointreps"></span>**D3DX10\_MESH\_DISCARD\_POINTREPS**</span></span>
</dt> <dd>

<span data-ttu-id="6d2e6-114">Verwerfen Sie den Zeiger Mitarbeiter-Puffer.</span><span class="sxs-lookup"><span data-stu-id="6d2e6-114">Discard the pointer reps buffer.</span></span>

</dd> <dt>

<span data-ttu-id="6d2e6-115"><span id="D3DX10_MESH_DISCARD_ADJACENCY"></span><span id="d3dx10_mesh_discard_adjacency"></span>**D3dx10 \_ Mesh- \_ Verwerfungs \_ Fähigkeit**</span><span class="sxs-lookup"><span data-stu-id="6d2e6-115"><span id="D3DX10_MESH_DISCARD_ADJACENCY"></span><span id="d3dx10_mesh_discard_adjacency"></span>**D3DX10\_MESH\_DISCARD\_ADJACENCY**</span></span>
</dt> <dd>

<span data-ttu-id="6d2e6-116">Verwerfen Sie den annähernden Puffer.</span><span class="sxs-lookup"><span data-stu-id="6d2e6-116">Discard the adjacency buffer.</span></span>

</dd> <dt>

<span data-ttu-id="6d2e6-117"><span id="D3DX10_MESH_DISCARD_DEVICE_BUFFERS"></span><span id="d3dx10_mesh_discard_device_buffers"></span>**D3dx10 \_ Mesh \_ - \_ Geräte \_ Puffer verwerfen**</span><span class="sxs-lookup"><span data-stu-id="6d2e6-117"><span id="D3DX10_MESH_DISCARD_DEVICE_BUFFERS"></span><span id="d3dx10_mesh_discard_device_buffers"></span>**D3DX10\_MESH\_DISCARD\_DEVICE\_BUFFERS**</span></span>
</dt> <dd>

<span data-ttu-id="6d2e6-118">Verwerfen Sie die Puffer, die an das Gerät übertragen wurden (mit [**ID3DX10Mesh:: commitcomdevice**](id3dx10mesh-committodevice.md)).</span><span class="sxs-lookup"><span data-stu-id="6d2e6-118">Discard the buffers committed to the device (with [**ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6d2e6-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d2e6-119">Requirements</span></span>



| <span data-ttu-id="6d2e6-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6d2e6-120">Requirement</span></span> | <span data-ttu-id="6d2e6-121">Wert</span><span class="sxs-lookup"><span data-stu-id="6d2e6-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d2e6-122">Header</span><span class="sxs-lookup"><span data-stu-id="6d2e6-122">Header</span></span><br/> | <dl> <span data-ttu-id="6d2e6-123"><dt>D3DX10Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d2e6-123"><dt>D3DX10Mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d2e6-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d2e6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d2e6-125">D3DX-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="6d2e6-125">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




