---
description: Beschreibt Parameter, mit denen eine Textur aus einer anderen Textur geladen wird.
ms.assetid: dee693ce-afa7-479b-a76a-00816e30d5cf
title: D3DX10_TEXTURE_LOAD_INFO-Struktur (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_TEXTURE_LOAD_INFO
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: d3a689bb2104ee4cb419eb1483619d1fcf71d7e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355206"
---
# <a name="d3dx10_texture_load_info-structure"></a><span data-ttu-id="088db-103">D3dx10 \_ Textur \_ Lade- \_ Informationsstruktur</span><span class="sxs-lookup"><span data-stu-id="088db-103">D3DX10\_TEXTURE\_LOAD\_INFO structure</span></span>

<span data-ttu-id="088db-104">Beschreibt Parameter, mit denen eine Textur aus einer anderen Textur geladen wird.</span><span class="sxs-lookup"><span data-stu-id="088db-104">Describes parameters used to load a texture from another texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="088db-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="088db-105">Syntax</span></span>


```C++
typedef struct _D3DX10_TEXTURE_LOAD_INFO {
  D3D10_BOX *pSrcBox;
  D3D10_BOX *pDstBox;
  UINT      SrcFirstMip;
  UINT      DstFirstMip;
  UINT      NumMips;
  UINT      SrcFirstElement;
  UINT      DstFirstElement;
  UINT      NumElements;
  UINT      Filter;
  UINT      MipFilter;
} D3DX10_TEXTURE_LOAD_INFO;
```



## <a name="members"></a><span data-ttu-id="088db-106">Member</span><span class="sxs-lookup"><span data-stu-id="088db-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="088db-107">**psrcbox**</span><span class="sxs-lookup"><span data-stu-id="088db-107">**pSrcBox**</span></span>
</dt> <dd>

<span data-ttu-id="088db-108">Typ: **[ **d3d10 \_ Box**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***</span><span class="sxs-lookup"><span data-stu-id="088db-108">Type: **[**D3D10\_BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***</span></span>

</dd> <dd>

<span data-ttu-id="088db-109">Quell Textur Feld (siehe [**d3d10 \_ Box**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)).</span><span class="sxs-lookup"><span data-stu-id="088db-109">Source texture box (see [**D3D10\_BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)).</span></span>

</dd> <dt>

<span data-ttu-id="088db-110">**pdstbox**</span><span class="sxs-lookup"><span data-stu-id="088db-110">**pDstBox**</span></span>
</dt> <dd>

<span data-ttu-id="088db-111">Typ: **[ **d3d10 \_ Box**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***</span><span class="sxs-lookup"><span data-stu-id="088db-111">Type: **[**D3D10\_BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)\***</span></span>

</dd> <dd>

<span data-ttu-id="088db-112">Ziel Textur Feld (siehe [**d3d10 \_ Box**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)).</span><span class="sxs-lookup"><span data-stu-id="088db-112">Destination texture box (see [**D3D10\_BOX**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_box)).</span></span>

</dd> <dt>

<span data-ttu-id="088db-113">**Srcfirstmip**</span><span class="sxs-lookup"><span data-stu-id="088db-113">**SrcFirstMip**</span></span>
</dt> <dd>

<span data-ttu-id="088db-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="088db-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="088db-115">MipMap-Ebene der Quell Textur. Weitere Informationen finden Sie unter [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) .</span><span class="sxs-lookup"><span data-stu-id="088db-115">Source texture mipmap level, see [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) for more detail.</span></span>

</dd> <dt>

<span data-ttu-id="088db-116">**Dstfirstmip**</span><span class="sxs-lookup"><span data-stu-id="088db-116">**DstFirstMip**</span></span>
</dt> <dd>

<span data-ttu-id="088db-117">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="088db-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="088db-118">Die MipMap-Ebene der Ziel Textur. weitere Details finden Sie unter [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) .</span><span class="sxs-lookup"><span data-stu-id="088db-118">Destination texture mipmap level, see [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource) for more detail.</span></span>

</dd> <dt>

<span data-ttu-id="088db-119">**Nummips**</span><span class="sxs-lookup"><span data-stu-id="088db-119">**NumMips**</span></span>
</dt> <dd>

<span data-ttu-id="088db-120">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="088db-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="088db-121">Anzahl von MipMap-Ebenen in der Quell Textur.</span><span class="sxs-lookup"><span data-stu-id="088db-121">Number of mipmap levels in the source texture.</span></span>

</dd> <dt>

<span data-ttu-id="088db-122">**Srcfirstelement**</span><span class="sxs-lookup"><span data-stu-id="088db-122">**SrcFirstElement**</span></span>
</dt> <dd>

<span data-ttu-id="088db-123">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="088db-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="088db-124">Erstes Element der Quell Textur.</span><span class="sxs-lookup"><span data-stu-id="088db-124">First element of the source texture.</span></span>

</dd> <dt>

<span data-ttu-id="088db-125">**Dstfirstelement**</span><span class="sxs-lookup"><span data-stu-id="088db-125">**DstFirstElement**</span></span>
</dt> <dd>

<span data-ttu-id="088db-126">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="088db-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="088db-127">Erstes Element der Ziel Textur.</span><span class="sxs-lookup"><span data-stu-id="088db-127">First element of the destination texture.</span></span>

</dd> <dt>

<span data-ttu-id="088db-128">**NumElements**</span><span class="sxs-lookup"><span data-stu-id="088db-128">**NumElements**</span></span>
</dt> <dd>

<span data-ttu-id="088db-129">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="088db-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="088db-130">Anzahl der zu ladenden Elemente.</span><span class="sxs-lookup"><span data-stu-id="088db-130">Number of elements to load.</span></span>

</dd> <dt>

<span data-ttu-id="088db-131">**Filter**</span><span class="sxs-lookup"><span data-stu-id="088db-131">**Filter**</span></span>
</dt> <dd>

<span data-ttu-id="088db-132">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="088db-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="088db-133">Filteroptionen während der erneuten Stichprobenentnahme (siehe [**d3dx10 \_ Filter \_ Flag**](d3dx10-filter-flag.md)).</span><span class="sxs-lookup"><span data-stu-id="088db-133">Filtering options during resampling (see [**D3DX10\_FILTER\_FLAG**](d3dx10-filter-flag.md)).</span></span>

</dd> <dt>

<span data-ttu-id="088db-134">**MipFilter**</span><span class="sxs-lookup"><span data-stu-id="088db-134">**MipFilter**</span></span>
</dt> <dd>

<span data-ttu-id="088db-135">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="088db-135">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="088db-136">Filteroptionen beim Erzeugen von Mip-Ebenen (siehe [**d3dx10 \_ Filter \_ Flag**](d3dx10-filter-flag.md)).</span><span class="sxs-lookup"><span data-stu-id="088db-136">Filtering options when generating mip levels (see [**D3DX10\_FILTER\_FLAG**](d3dx10-filter-flag.md)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="088db-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="088db-137">Remarks</span></span>

<span data-ttu-id="088db-138">Diese Struktur wird in einem [**D3DX10LoadTextureFromTexture**](d3dx10loadtexturefromtexture.md)-aufrufswert verwendet.</span><span class="sxs-lookup"><span data-stu-id="088db-138">This structure is used in a call to [**D3DX10LoadTextureFromTexture**](d3dx10loadtexturefromtexture.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="088db-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="088db-139">Requirements</span></span>



| <span data-ttu-id="088db-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="088db-140">Requirement</span></span> | <span data-ttu-id="088db-141">Wert</span><span class="sxs-lookup"><span data-stu-id="088db-141">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="088db-142">Header</span><span class="sxs-lookup"><span data-stu-id="088db-142">Header</span></span><br/> | <dl> <span data-ttu-id="088db-143"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="088db-143"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="088db-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="088db-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="088db-145">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="088db-145">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
