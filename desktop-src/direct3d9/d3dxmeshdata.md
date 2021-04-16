---
description: Mesh-Datenstruktur.
ms.assetid: 9164b956-95b7-4bc0-bf7e-feed2e3b4a2b
title: D3DXMESHDATA-Struktur (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESHDATA
api_type:
- HeaderDef
api_location:
- D3dx9anim.h
ms.openlocfilehash: 785284ba1330c957813a099eb6cf1c74521d3c90
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354176"
---
# <a name="d3dxmeshdata-structure"></a><span data-ttu-id="4f9a8-103">D3DXMESHDATA-Struktur</span><span class="sxs-lookup"><span data-stu-id="4f9a8-103">D3DXMESHDATA structure</span></span>

<span data-ttu-id="4f9a8-104">Mesh-Datenstruktur.</span><span class="sxs-lookup"><span data-stu-id="4f9a8-104">Mesh data structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f9a8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f9a8-105">Syntax</span></span>


```C++
typedef struct D3DXMESHDATA {
  D3DXMESHDATATYPE Type;
  union {
    LPD3DXMESH      pMesh;
    LPD3DXPATCHMESH pPatchMesh;
  };
} D3DXMESHDATA, *LPD3DXMESHDATA;
```



## <a name="members"></a><span data-ttu-id="4f9a8-106">Member</span><span class="sxs-lookup"><span data-stu-id="4f9a8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4f9a8-107">**Type**</span><span class="sxs-lookup"><span data-stu-id="4f9a8-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="4f9a8-108">Typ: **[ **D3DXMESHDATATYPE**](./d3dxmeshdatatype.md)**</span><span class="sxs-lookup"><span data-stu-id="4f9a8-108">Type: **[**D3DXMESHDATATYPE**](./d3dxmeshdatatype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4f9a8-109">Definiert den Mesh-Datentyp.</span><span class="sxs-lookup"><span data-stu-id="4f9a8-109">Defines the mesh data type.</span></span> <span data-ttu-id="4f9a8-110">Siehe [**D3DXMESHDATATYPE**](./d3dxmeshdatatype.md).</span><span class="sxs-lookup"><span data-stu-id="4f9a8-110">See [**D3DXMESHDATATYPE**](./d3dxmeshdatatype.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f9a8-111">**pmesh**</span><span class="sxs-lookup"><span data-stu-id="4f9a8-111">**pMesh**</span></span>
</dt> <dd>

<span data-ttu-id="4f9a8-112">Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="4f9a8-112">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4f9a8-113">Zeiger auf ein Mesh.</span><span class="sxs-lookup"><span data-stu-id="4f9a8-113">Pointer to a mesh.</span></span> <span data-ttu-id="4f9a8-114">Siehe [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="4f9a8-114">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f9a8-115">**ppatchmesh**</span><span class="sxs-lookup"><span data-stu-id="4f9a8-115">**pPatchMesh**</span></span>
</dt> <dd>

<span data-ttu-id="4f9a8-116">Typ: **LPD3DXPATCHMESH**</span><span class="sxs-lookup"><span data-stu-id="4f9a8-116">Type: **LPD3DXPATCHMESH**</span></span>

</dd> <dd>

<span data-ttu-id="4f9a8-117">Zeiger auf ein patchmesh.</span><span class="sxs-lookup"><span data-stu-id="4f9a8-117">Pointer to a patch mesh.</span></span> <span data-ttu-id="4f9a8-118">Siehe [**ID3DXPatchMesh**](id3dxpatchmesh.md).</span><span class="sxs-lookup"><span data-stu-id="4f9a8-118">See [**ID3DXPatchMesh**](id3dxpatchmesh.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4f9a8-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f9a8-119">Requirements</span></span>



| <span data-ttu-id="4f9a8-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4f9a8-120">Requirement</span></span> | <span data-ttu-id="4f9a8-121">Wert</span><span class="sxs-lookup"><span data-stu-id="4f9a8-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f9a8-122">Header</span><span class="sxs-lookup"><span data-stu-id="4f9a8-122">Header</span></span><br/> | <dl> <span data-ttu-id="4f9a8-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f9a8-123"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f9a8-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f9a8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f9a8-125">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="4f9a8-125">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="4f9a8-126">**D3DXMESHCONTAINER**</span><span class="sxs-lookup"><span data-stu-id="4f9a8-126">**D3DXMESHCONTAINER**</span></span>](d3dxmeshcontainer.md)
</dt> </dl>

 

 
