---
description: D3DXSHPRTSPLITMESHCLUSTERDATA-Struktur
ms.assetid: 6a53420c-06bc-4f52-ac2e-5adda5e34cb2
title: D3DXSHPRTSPLITMESHCLUSTERDATA-Struktur (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTSPLITMESHCLUSTERDATA
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: e7b1bc23606dbf08f5a924860e12c9c09d719287
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365080"
---
# <a name="d3dxshprtsplitmeshclusterdata-structure"></a><span data-ttu-id="e48ec-103">D3DXSHPRTSPLITMESHCLUSTERDATA-Struktur</span><span class="sxs-lookup"><span data-stu-id="e48ec-103">D3DXSHPRTSPLITMESHCLUSTERDATA structure</span></span>

## <a name="syntax"></a><span data-ttu-id="e48ec-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e48ec-104">Syntax</span></span>


```C++
typedef struct D3DXSHPRTSPLITMESHCLUSTERDATA {
  UINT uVertStart;
  UINT uVertLength;
  UINT uFaceStart;
  UINT uFaceLength;
  UINT uClusterStart;
  UINT uClusterLength;
} D3DXSHPRTSPLITMESHCLUSTERDATA, *LPD3DXSHPRTSPLITMESHCLUSTERDATA;
```



## <a name="members"></a><span data-ttu-id="e48ec-105">Member</span><span class="sxs-lookup"><span data-stu-id="e48ec-105">Members</span></span>

<dl> <dt>

<span data-ttu-id="e48ec-106">**uvertstart**</span><span class="sxs-lookup"><span data-stu-id="e48ec-106">**uVertStart**</span></span>
</dt> <dd>

<span data-ttu-id="e48ec-107">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e48ec-107">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e48ec-108">Ursprünglicher Scheitelpunkt in neu zugeordnete Scheitelpunkt Arrays.</span><span class="sxs-lookup"><span data-stu-id="e48ec-108">Initial vertex into remapped vertex array.</span></span>

</dd> <dt>

<span data-ttu-id="e48ec-109">**uvertlength**</span><span class="sxs-lookup"><span data-stu-id="e48ec-109">**uVertLength**</span></span>
</dt> <dd>

<span data-ttu-id="e48ec-110">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e48ec-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e48ec-111">Anzahl der Scheitel Punkte in diesem Supercluster.</span><span class="sxs-lookup"><span data-stu-id="e48ec-111">Number of vertices in this supercluster.</span></span>

</dd> <dt>

<span data-ttu-id="e48ec-112">**ufakestart**</span><span class="sxs-lookup"><span data-stu-id="e48ec-112">**uFaceStart**</span></span>
</dt> <dd>

<span data-ttu-id="e48ec-113">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e48ec-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e48ec-114">Ursprünglicher Index in Flächen Array.</span><span class="sxs-lookup"><span data-stu-id="e48ec-114">Initial index into face array.</span></span>

</dd> <dt>

<span data-ttu-id="e48ec-115">**ufakelength**</span><span class="sxs-lookup"><span data-stu-id="e48ec-115">**uFaceLength**</span></span>
</dt> <dd>

<span data-ttu-id="e48ec-116">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e48ec-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e48ec-117">Anzahl der Gesichter in diesem Supercluster.</span><span class="sxs-lookup"><span data-stu-id="e48ec-117">Number of faces in this supercluster.</span></span>

</dd> <dt>

<span data-ttu-id="e48ec-118">**uclusterstart**</span><span class="sxs-lookup"><span data-stu-id="e48ec-118">**uClusterStart**</span></span>
</dt> <dd>

<span data-ttu-id="e48ec-119">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e48ec-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e48ec-120">Ursprünglicher Index in Cluster Array.</span><span class="sxs-lookup"><span data-stu-id="e48ec-120">Initial index into cluster array.</span></span>

</dd> <dt>

<span data-ttu-id="e48ec-121">**uclusterlength**</span><span class="sxs-lookup"><span data-stu-id="e48ec-121">**uClusterLength**</span></span>
</dt> <dd>

<span data-ttu-id="e48ec-122">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e48ec-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e48ec-123">Anzahl der Cluster in diesem Supercluster-Array.</span><span class="sxs-lookup"><span data-stu-id="e48ec-123">Number of clusters in this supercluster array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e48ec-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e48ec-124">Requirements</span></span>



| <span data-ttu-id="e48ec-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e48ec-125">Requirement</span></span> | <span data-ttu-id="e48ec-126">Wert</span><span class="sxs-lookup"><span data-stu-id="e48ec-126">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e48ec-127">Header</span><span class="sxs-lookup"><span data-stu-id="e48ec-127">Header</span></span><br/> | <dl> <span data-ttu-id="e48ec-128"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e48ec-128"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e48ec-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e48ec-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e48ec-130">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="e48ec-130">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="e48ec-131">**D3DXSHPRTCompSplitMeshSC**</span><span class="sxs-lookup"><span data-stu-id="e48ec-131">**D3DXSHPRTCompSplitMeshSC**</span></span>](d3dxshprtcompsplitmeshsc.md)
</dt> </dl>

 

 
