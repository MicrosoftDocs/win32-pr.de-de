---
description: D3DXSHPRTSPLITMESHVERTDATA-Struktur
ms.assetid: 8799a680-bf5f-42cc-91aa-1a6aed164ca5
title: D3DXSHPRTSPLITMESHVERTDATA-Struktur (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTSPLITMESHVERTDATA
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 55424929a3d415fc1b89f7a1af53be849cf90185
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762024"
---
# <a name="d3dxshprtsplitmeshvertdata-structure"></a><span data-ttu-id="2eced-103">D3DXSHPRTSPLITMESHVERTDATA-Struktur</span><span class="sxs-lookup"><span data-stu-id="2eced-103">D3DXSHPRTSPLITMESHVERTDATA structure</span></span>

## <a name="syntax"></a><span data-ttu-id="2eced-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2eced-104">Syntax</span></span>


```C++
typedef struct D3DXSHPRTSPLITMESHVERTDATA {
  UINT uVertRemap;
  UINT uSubCluster;
  UINT ucVertStatus;
} D3DXSHPRTSPLITMESHVERTDATA, *LPD3DXSHPRTSPLITMESHVERTDATA;
```



## <a name="members"></a><span data-ttu-id="2eced-105">Member</span><span class="sxs-lookup"><span data-stu-id="2eced-105">Members</span></span>

<dl> <dt>

<span data-ttu-id="2eced-106">**uvertremap**</span><span class="sxs-lookup"><span data-stu-id="2eced-106">**uVertRemap**</span></span>
</dt> <dd>

<span data-ttu-id="2eced-107">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2eced-107">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2eced-108">Scheitelpunkt im ursprünglichen Mesh, dies entspricht.</span><span class="sxs-lookup"><span data-stu-id="2eced-108">Vertex in original mesh this corresponds to.</span></span>

</dd> <dt>

<span data-ttu-id="2eced-109">**usubcluster**</span><span class="sxs-lookup"><span data-stu-id="2eced-109">**uSubCluster**</span></span>
</dt> <dd>

<span data-ttu-id="2eced-110">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2eced-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2eced-111">Cluster Index relativ zum Supercluster.</span><span class="sxs-lookup"><span data-stu-id="2eced-111">Cluster index, relative to the supercluster.</span></span>

</dd> <dt>

<span data-ttu-id="2eced-112">**ucvertstatus**</span><span class="sxs-lookup"><span data-stu-id="2eced-112">**ucVertStatus**</span></span>
</dt> <dd>

<span data-ttu-id="2eced-113">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2eced-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2eced-114">1, wenn der Scheitelpunkt gültige Daten aufweist, 0 (null), wenn er "Full" ist.</span><span class="sxs-lookup"><span data-stu-id="2eced-114">1 if vertex has valid data, 0 if it is "full".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2eced-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2eced-115">Remarks</span></span>

<span data-ttu-id="2eced-116">In [**D3DXSHPRTCompSplitMeshSC**](d3dxshprtcompsplitmeshsc.md)zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="2eced-116">Allocated in [**D3DXSHPRTCompSplitMeshSC**](d3dxshprtcompsplitmeshsc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2eced-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2eced-117">Requirements</span></span>



| <span data-ttu-id="2eced-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2eced-118">Requirement</span></span> | <span data-ttu-id="2eced-119">Wert</span><span class="sxs-lookup"><span data-stu-id="2eced-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2eced-120">Header</span><span class="sxs-lookup"><span data-stu-id="2eced-120">Header</span></span><br/> | <dl> <span data-ttu-id="2eced-121"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="2eced-121"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2eced-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2eced-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2eced-123">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="2eced-123">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
