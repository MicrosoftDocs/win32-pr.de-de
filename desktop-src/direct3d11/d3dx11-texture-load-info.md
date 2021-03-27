---
title: D3DX11_TEXTURE_LOAD_INFO-Struktur (D3DX11tex. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Beschreibt Parameter, mit denen eine Textur aus einer anderen Textur geladen wird.
ms.assetid: 2fe24752-d1bc-4666-bf0f-cc397394da56
keywords:
- D3DX11_TEXTURE_LOAD_INFO Struktur Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_TEXTURE_LOAD_INFO
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ca893908f854b6b127d783af25cc2fb9bc5df6a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996058"
---
# <a name="d3dx11_texture_load_info-structure"></a><span data-ttu-id="795a6-105">Bibliothek d3dx11 \_ Textur \_ Lade- \_ Informationsstruktur</span><span class="sxs-lookup"><span data-stu-id="795a6-105">D3DX11\_TEXTURE\_LOAD\_INFO structure</span></span>

> [!Note]  
> <span data-ttu-id="795a6-106">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="795a6-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="795a6-107">Beschreibt Parameter, mit denen eine Textur aus einer anderen Textur geladen wird.</span><span class="sxs-lookup"><span data-stu-id="795a6-107">Describes parameters used to load a texture from another texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="795a6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="795a6-108">Syntax</span></span>


```C++
typedef struct _D3DX11_TEXTURE_LOAD_INFO {
  D3D11_BOX *pSrcBox;
  D3D11_BOX *pDstBox;
  UINT      SrcFirstMip;
  UINT      DstFirstMip;
  UINT      NumMips;
  UINT      SrcFirstElement;
  UINT      DstFirstElement;
  UINT      NumElements;
  UINT      Filter;
  UINT      MipFilter;
} D3DX11_TEXTURE_LOAD_INFO;
```



## <a name="members"></a><span data-ttu-id="795a6-109">Member</span><span class="sxs-lookup"><span data-stu-id="795a6-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="795a6-110">**psrcbox**</span><span class="sxs-lookup"><span data-stu-id="795a6-110">**pSrcBox**</span></span>
</dt> <dd>

<span data-ttu-id="795a6-111">Typ: **[ **D3D11 \_ Box**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***</span><span class="sxs-lookup"><span data-stu-id="795a6-111">Type: **[**D3D11\_BOX**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***</span></span>

</dd> <dd>

<span data-ttu-id="795a6-112">Quell Textur Feld (siehe [**D3D11 \_ Box**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)).</span><span class="sxs-lookup"><span data-stu-id="795a6-112">Source texture box (see [**D3D11\_BOX**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)).</span></span>

</dd> <dt>

<span data-ttu-id="795a6-113">**pdstbox**</span><span class="sxs-lookup"><span data-stu-id="795a6-113">**pDstBox**</span></span>
</dt> <dd>

<span data-ttu-id="795a6-114">Typ: **[ **D3D11 \_ Box**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***</span><span class="sxs-lookup"><span data-stu-id="795a6-114">Type: **[**D3D11\_BOX**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)\***</span></span>

</dd> <dd>

<span data-ttu-id="795a6-115">Ziel Textur Feld (siehe [**D3D11 \_ Box**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)).</span><span class="sxs-lookup"><span data-stu-id="795a6-115">Destination texture box (see [**D3D11\_BOX**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_box)).</span></span>

</dd> <dt>

<span data-ttu-id="795a6-116">**Srcfirstmip**</span><span class="sxs-lookup"><span data-stu-id="795a6-116">**SrcFirstMip**</span></span>
</dt> <dd>

<span data-ttu-id="795a6-117">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="795a6-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="795a6-118">MipMap-Ebene der Quell Textur. Weitere Informationen finden Sie unter [**D3D11CalcSubresource**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource) .</span><span class="sxs-lookup"><span data-stu-id="795a6-118">Source texture mipmap level, see [**D3D11CalcSubresource**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource) for more detail.</span></span>

</dd> <dt>

<span data-ttu-id="795a6-119">**Dstfirstmip**</span><span class="sxs-lookup"><span data-stu-id="795a6-119">**DstFirstMip**</span></span>
</dt> <dd>

<span data-ttu-id="795a6-120">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="795a6-120">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="795a6-121">Die MipMap-Ebene der Ziel Textur. weitere Details finden Sie unter [**D3D11CalcSubresource**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource) .</span><span class="sxs-lookup"><span data-stu-id="795a6-121">Destination texture mipmap level, see [**D3D11CalcSubresource**](/windows/desktop/api/D3D11/nf-d3d11-d3d11calcsubresource) for more detail.</span></span>

</dd> <dt>

<span data-ttu-id="795a6-122">**Nummips**</span><span class="sxs-lookup"><span data-stu-id="795a6-122">**NumMips**</span></span>
</dt> <dd>

<span data-ttu-id="795a6-123">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="795a6-123">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="795a6-124">Anzahl von MipMap-Ebenen in der Quell Textur.</span><span class="sxs-lookup"><span data-stu-id="795a6-124">Number of mipmap levels in the source texture.</span></span>

</dd> <dt>

<span data-ttu-id="795a6-125">**Srcfirstelement**</span><span class="sxs-lookup"><span data-stu-id="795a6-125">**SrcFirstElement**</span></span>
</dt> <dd>

<span data-ttu-id="795a6-126">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="795a6-126">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="795a6-127">Erstes Element der Quell Textur.</span><span class="sxs-lookup"><span data-stu-id="795a6-127">First element of the source texture.</span></span>

</dd> <dt>

<span data-ttu-id="795a6-128">**Dstfirstelement**</span><span class="sxs-lookup"><span data-stu-id="795a6-128">**DstFirstElement**</span></span>
</dt> <dd>

<span data-ttu-id="795a6-129">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="795a6-129">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="795a6-130">Erstes Element der Ziel Textur.</span><span class="sxs-lookup"><span data-stu-id="795a6-130">First element of the destination texture.</span></span>

</dd> <dt>

<span data-ttu-id="795a6-131">**NumElements**</span><span class="sxs-lookup"><span data-stu-id="795a6-131">**NumElements**</span></span>
</dt> <dd>

<span data-ttu-id="795a6-132">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="795a6-132">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="795a6-133">Anzahl der zu ladenden Elemente.</span><span class="sxs-lookup"><span data-stu-id="795a6-133">Number of elements to load.</span></span>

</dd> <dt>

<span data-ttu-id="795a6-134">**Filter**</span><span class="sxs-lookup"><span data-stu-id="795a6-134">**Filter**</span></span>
</dt> <dd>

<span data-ttu-id="795a6-135">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="795a6-135">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="795a6-136">Filteroptionen während der erneuten Stichprobenentnahme (siehe [**Bibliothek d3dx11 \_ Filter \_ Flag**](d3dx11-filter-flag.md)).</span><span class="sxs-lookup"><span data-stu-id="795a6-136">Filtering options during resampling (see [**D3DX11\_FILTER\_FLAG**](d3dx11-filter-flag.md)).</span></span>

</dd> <dt>

<span data-ttu-id="795a6-137">**MipFilter**</span><span class="sxs-lookup"><span data-stu-id="795a6-137">**MipFilter**</span></span>
</dt> <dd>

<span data-ttu-id="795a6-138">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="795a6-138">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="795a6-139">Filteroptionen beim Erzeugen von Mip-Ebenen (siehe [**Bibliothek d3dx11 \_ Filter \_ Flag**](d3dx11-filter-flag.md)).</span><span class="sxs-lookup"><span data-stu-id="795a6-139">Filtering options when generating mip levels (see [**D3DX11\_FILTER\_FLAG**](d3dx11-filter-flag.md)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="795a6-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="795a6-140">Remarks</span></span>

<span data-ttu-id="795a6-141">Diese Struktur wird in einem [**D3DX11LoadTextureFromTexture**](d3dx11loadtexturefromtexture.md)-aufrufswert verwendet.</span><span class="sxs-lookup"><span data-stu-id="795a6-141">This structure is used in a call to [**D3DX11LoadTextureFromTexture**](d3dx11loadtexturefromtexture.md).</span></span>

<span data-ttu-id="795a6-142">Die Standardwerte lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="795a6-142">The default values are:</span></span>


```
    pSrcBox = NULL;
    pDstBox = NULL;
    SrcFirstMip = 0;
    DstFirstMip = 0;
    NumMips = D3DX11_DEFAULT;
    SrcFirstElement = 0;
    DstFirstElement = 0;
    NumElements = D3DX11_DEFAULT;
    Filter = D3DX11_DEFAULT;
    MipFilter = D3DX11_DEFAULT;
```



## <a name="requirements"></a><span data-ttu-id="795a6-143">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="795a6-143">Requirements</span></span>



| <span data-ttu-id="795a6-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="795a6-144">Requirement</span></span> | <span data-ttu-id="795a6-145">Wert</span><span class="sxs-lookup"><span data-stu-id="795a6-145">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="795a6-146">Header</span><span class="sxs-lookup"><span data-stu-id="795a6-146">Header</span></span><br/> | <dl> <span data-ttu-id="795a6-147"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="795a6-147"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="795a6-148">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="795a6-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="795a6-149">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="795a6-149">D3DX Structures</span></span>](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

