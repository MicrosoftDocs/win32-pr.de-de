---
description: Gibt Materialeigenschaften an.
ms.assetid: 943e6f6d-8091-462f-8c44-e0c27686934a
title: D3DMATERIAL9-Struktur (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMATERIAL9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b9c3ad93fe2cb80fe758e2e66da37cce9d4267ad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394157"
---
# <a name="d3dmaterial9-structure"></a><span data-ttu-id="d48e2-103">D3DMATERIAL9-Struktur</span><span class="sxs-lookup"><span data-stu-id="d48e2-103">D3DMATERIAL9 structure</span></span>

<span data-ttu-id="d48e2-104">Gibt Materialeigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="d48e2-104">Specifies material properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d48e2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d48e2-105">Syntax</span></span>


```C++
typedef struct D3DMATERIAL9 {
  D3DCOLORVALUE Diffuse;
  D3DCOLORVALUE Ambient;
  D3DCOLORVALUE Specular;
  D3DCOLORVALUE Emissive;
  float         Power;
} D3DMATERIAL9, *LPD3DMATERIAL9;
```



## <a name="members"></a><span data-ttu-id="d48e2-106">Member</span><span class="sxs-lookup"><span data-stu-id="d48e2-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d48e2-107">**Diffus**</span><span class="sxs-lookup"><span data-stu-id="d48e2-107">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="d48e2-108">Typ: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="d48e2-108">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d48e2-109">Ein-Wert, der die diffuse Farbe des Materials angibt.</span><span class="sxs-lookup"><span data-stu-id="d48e2-109">Value specifying the diffuse color of the material.</span></span> <span data-ttu-id="d48e2-110">Siehe [**D3DCOLORVALUE**](d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="d48e2-110">See [**D3DCOLORVALUE**](d3dcolorvalue.md).</span></span>

</dd> <dt>

<span data-ttu-id="d48e2-111">**Umgebend**</span><span class="sxs-lookup"><span data-stu-id="d48e2-111">**Ambient**</span></span>
</dt> <dd>

<span data-ttu-id="d48e2-112">Typ: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="d48e2-112">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d48e2-113">Ein-Wert, der die Ambiente-Farbe des Materials angibt.</span><span class="sxs-lookup"><span data-stu-id="d48e2-113">Value specifying the ambient color of the material.</span></span> <span data-ttu-id="d48e2-114">Siehe [**D3DCOLORVALUE**](d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="d48e2-114">See [**D3DCOLORVALUE**](d3dcolorvalue.md).</span></span>

</dd> <dt>

<span data-ttu-id="d48e2-115">**Glänzend**</span><span class="sxs-lookup"><span data-stu-id="d48e2-115">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="d48e2-116">Typ: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="d48e2-116">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d48e2-117">Ein-Wert, der die Glanz Farbe des Materials angibt.</span><span class="sxs-lookup"><span data-stu-id="d48e2-117">Value specifying the specular color of the material.</span></span> <span data-ttu-id="d48e2-118">Siehe [**D3DCOLORVALUE**](d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="d48e2-118">See [**D3DCOLORVALUE**](d3dcolorvalue.md).</span></span>

</dd> <dt>

<span data-ttu-id="d48e2-119">**Selbstleuchtend**</span><span class="sxs-lookup"><span data-stu-id="d48e2-119">**Emissive**</span></span>
</dt> <dd>

<span data-ttu-id="d48e2-120">Typ: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="d48e2-120">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d48e2-121">Ein-Wert, der die selbst leuchtendes Farbe des Materials angibt.</span><span class="sxs-lookup"><span data-stu-id="d48e2-121">Value specifying the emissive color of the material.</span></span> <span data-ttu-id="d48e2-122">Siehe [**D3DCOLORVALUE**](d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="d48e2-122">See [**D3DCOLORVALUE**](d3dcolorvalue.md).</span></span>

</dd> <dt>

<span data-ttu-id="d48e2-123">**Energie**</span><span class="sxs-lookup"><span data-stu-id="d48e2-123">**Power**</span></span>
</dt> <dd>

<span data-ttu-id="d48e2-124">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="d48e2-124">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="d48e2-125">Ein Gleit Komma Wert, der die Schärfe von Glanzlichtern angibt.</span><span class="sxs-lookup"><span data-stu-id="d48e2-125">Floating-point value specifying the sharpness of specular highlights.</span></span> <span data-ttu-id="d48e2-126">Je höher der Wert ist, desto stärker ist die Hervorhebung.</span><span class="sxs-lookup"><span data-stu-id="d48e2-126">The higher the value, the sharper the highlight.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d48e2-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d48e2-127">Remarks</span></span>

<span data-ttu-id="d48e2-128">Um Glanzlichter zu deaktivieren, legen Sie D3DRS \_ specularenable mithilfe von [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)auf **false** fest.</span><span class="sxs-lookup"><span data-stu-id="d48e2-128">To turn off specular highlights, set D3DRS\_SPECULARENABLE to **FALSE**, using [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md).</span></span> <span data-ttu-id="d48e2-129">Dies ist die schnellste Option, da keine Glanzlichter berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="d48e2-129">This is the fastest option because no specular highlights will be calculated.</span></span>

<span data-ttu-id="d48e2-130">Weitere Informationen zur Berechnung Glanzlichter mithilfe der Beleuchtungs-Engine finden Sie unter Glanz [Beleuchtung (Direct3D 9)](specular-lighting.md).</span><span class="sxs-lookup"><span data-stu-id="d48e2-130">For more information about using the lighting engine to calculate specular lighting, see [Specular Lighting (Direct3D 9)](specular-lighting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d48e2-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d48e2-131">Requirements</span></span>



| <span data-ttu-id="d48e2-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d48e2-132">Requirement</span></span> | <span data-ttu-id="d48e2-133">Wert</span><span class="sxs-lookup"><span data-stu-id="d48e2-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d48e2-134">Header</span><span class="sxs-lookup"><span data-stu-id="d48e2-134">Header</span></span><br/> | <dl> <span data-ttu-id="d48e2-135"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="d48e2-135"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d48e2-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d48e2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d48e2-137">Direct3D-Strukturen</span><span class="sxs-lookup"><span data-stu-id="d48e2-137">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="d48e2-138">**IDirect3DDevice9:: getmaterial**</span><span class="sxs-lookup"><span data-stu-id="d48e2-138">**IDirect3DDevice9::GetMaterial**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getmaterial)
</dt> <dt>

[<span data-ttu-id="d48e2-139">**IDirect3DDevice9:: setmaterial**</span><span class="sxs-lookup"><span data-stu-id="d48e2-139">**IDirect3DDevice9::SetMaterial**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial)
</dt> </dl>

 

 
