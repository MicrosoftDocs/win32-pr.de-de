---
description: Beschreibt eine Oberfläche.
ms.assetid: fad8ffdb-36e5-4695-b343-e1315357c31a
title: D3DSURFACE_DESC-Struktur (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSURFACE_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 6424bbe9b78532657670bc5cd9ad0705de89a3b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351941"
---
# <a name="d3dsurface_desc-structure"></a><span data-ttu-id="2a83f-103">D3DSURFACE- \_ Struktur</span><span class="sxs-lookup"><span data-stu-id="2a83f-103">D3DSURFACE\_DESC structure</span></span>

<span data-ttu-id="2a83f-104">Beschreibt eine Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="2a83f-104">Describes a surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a83f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a83f-105">Syntax</span></span>


```C++
typedef struct D3DSURFACE_DESC {
  D3DFORMAT           Format;
  D3DRESOURCETYPE     Type;
  DWORD               Usage;
  D3DPOOL             Pool;
  D3DMULTISAMPLE_TYPE MultiSampleType;
  DWORD               MultiSampleQuality;
  UINT                Width;
  UINT                Height;
} D3DSURFACE_DESC, *LPD3DSURFACE_DESC;
```



## <a name="members"></a><span data-ttu-id="2a83f-106">Member</span><span class="sxs-lookup"><span data-stu-id="2a83f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2a83f-107">**Format**</span><span class="sxs-lookup"><span data-stu-id="2a83f-107">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="2a83f-108">Typ: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="2a83f-108">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2a83f-109">Member des [D3DFORMAT](d3dformat.md) -Enumerationstyps, der das Oberflächen Format beschreibt.</span><span class="sxs-lookup"><span data-stu-id="2a83f-109">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the surface format.</span></span>

</dd> <dt>

<span data-ttu-id="2a83f-110">**Type**</span><span class="sxs-lookup"><span data-stu-id="2a83f-110">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="2a83f-111">Typ: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**</span><span class="sxs-lookup"><span data-stu-id="2a83f-111">Type: **[**D3DRESOURCETYPE**](./d3dresourcetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2a83f-112">Member des [**D3DRESOURCETYPE**](./d3dresourcetype.md) -Enumerationstyps, der diese Ressource als Oberfläche identifiziert.</span><span class="sxs-lookup"><span data-stu-id="2a83f-112">Member of the [**D3DRESOURCETYPE**](./d3dresourcetype.md) enumerated type, identifying this resource as a surface.</span></span>

</dd> <dt>

<span data-ttu-id="2a83f-113">**Verwendung**</span><span class="sxs-lookup"><span data-stu-id="2a83f-113">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="2a83f-114">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2a83f-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2a83f-115">Entweder die D3DUSAGE \_ depthstencil-oder D3DUSAGE \_ renderTarget-Werte.</span><span class="sxs-lookup"><span data-stu-id="2a83f-115">Either the D3DUSAGE\_DEPTHSTENCIL or D3DUSAGE\_RENDERTARGET values.</span></span> <span data-ttu-id="2a83f-116">Weitere Informationen finden Sie unter [**D3DUSAGE**](d3dusage.md).</span><span class="sxs-lookup"><span data-stu-id="2a83f-116">For more information, see [**D3DUSAGE**](d3dusage.md).</span></span>

</dd> <dt>

<span data-ttu-id="2a83f-117">**Pool**</span><span class="sxs-lookup"><span data-stu-id="2a83f-117">**Pool**</span></span>
</dt> <dd>

<span data-ttu-id="2a83f-118">Typ: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="2a83f-118">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2a83f-119">Member des [**D3DPOOL**](./d3dpool.md) -Enumerationstyps, der die für diese Oberfläche zugeordnete Arbeitsspeicher Klasse angibt.</span><span class="sxs-lookup"><span data-stu-id="2a83f-119">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, specifying the class of memory allocated for this surface.</span></span>

</dd> <dt>

<span data-ttu-id="2a83f-120">**MultiSampleType**</span><span class="sxs-lookup"><span data-stu-id="2a83f-120">**MultiSampleType**</span></span>
</dt> <dd>

<span data-ttu-id="2a83f-121">Type: **[ **D3DMULTISAMPLE- \_ Typ**](./d3dmultisample-type.md)**</span><span class="sxs-lookup"><span data-stu-id="2a83f-121">Type: **[**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2a83f-122">Member des Typs " [**D3DMULTISAMPLE \_ Type**](./d3dmultisample-type.md) enumerieriert", der die Ebenen der von der-Oberfläche unterstützten vollständigen multisamplinggrad-Auflistung angibt.</span><span class="sxs-lookup"><span data-stu-id="2a83f-122">Member of the [**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md) enumerated type, specifying the levels of full-scene multisampling supported by the surface.</span></span>

</dd> <dt>

<span data-ttu-id="2a83f-123">**Multisamplequality**</span><span class="sxs-lookup"><span data-stu-id="2a83f-123">**MultiSampleQuality**</span></span>
</dt> <dd>

<span data-ttu-id="2a83f-124">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2a83f-124">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2a83f-125">Qualitätsstufe.</span><span class="sxs-lookup"><span data-stu-id="2a83f-125">Quality level.</span></span> <span data-ttu-id="2a83f-126">Der gültige Bereich liegt zwischen 0 (null) und einem niedrigeren Wert als der von " [**checkdevicemultisampletype**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype)" verwendeten pqualitylevels.</span><span class="sxs-lookup"><span data-stu-id="2a83f-126">The valid range is between zero and one less than the level returned by pQualityLevels used by [**CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype).</span></span> <span data-ttu-id="2a83f-127">Wenn Sie einen größeren Wert übergeben, wird der Fehler "D3DERR \_ invalidcall" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2a83f-127">Passing a larger value returns the error, D3DERR\_INVALIDCALL.</span></span> <span data-ttu-id="2a83f-128">Die multisamplequality-Werte von gekoppelten renderzielen, tiefen Schablone-Oberflächen und der Multisample-Typ müssen alle entsprechen.</span><span class="sxs-lookup"><span data-stu-id="2a83f-128">The MultisampleQuality values of paired render targets, depth stencil surfaces and the MultiSample type must all match.</span></span>

</dd> <dt>

<span data-ttu-id="2a83f-129">**Width**</span><span class="sxs-lookup"><span data-stu-id="2a83f-129">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="2a83f-130">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2a83f-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2a83f-131">Breite der Oberfläche in Pixel.</span><span class="sxs-lookup"><span data-stu-id="2a83f-131">Width of the surface, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="2a83f-132">**Height**</span><span class="sxs-lookup"><span data-stu-id="2a83f-132">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="2a83f-133">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2a83f-133">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2a83f-134">Höhe der Oberfläche in Pixel.</span><span class="sxs-lookup"><span data-stu-id="2a83f-134">Height of the surface, in pixels.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2a83f-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a83f-135">Requirements</span></span>



| <span data-ttu-id="2a83f-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2a83f-136">Requirement</span></span> | <span data-ttu-id="2a83f-137">Wert</span><span class="sxs-lookup"><span data-stu-id="2a83f-137">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a83f-138">Header</span><span class="sxs-lookup"><span data-stu-id="2a83f-138">Header</span></span><br/> | <dl> <span data-ttu-id="2a83f-139"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a83f-139"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a83f-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a83f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a83f-141">Direct3D-Strukturen</span><span class="sxs-lookup"><span data-stu-id="2a83f-141">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="2a83f-142">**Getleveldebug**</span><span class="sxs-lookup"><span data-stu-id="2a83f-142">**GetLevelDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getleveldesc)
</dt> <dt>

[<span data-ttu-id="2a83f-143">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="2a83f-143">**GetDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdesc)
</dt> <dt>

[<span data-ttu-id="2a83f-144">**Getleveldebug**</span><span class="sxs-lookup"><span data-stu-id="2a83f-144">**GetLevelDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getleveldesc)
</dt> </dl>

 

 
