---
description: Material Merkmale für die präberechnete Glanz Farbe (SH) (SH).
ms.assetid: 2be49f96-ac61-46aa-8d56-d8eee8dca9ed
title: D3DXSHMATERIAL-Struktur (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMATERIAL
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 0600cc0c1ebe086f0d6679182125350b1ee8ca98
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367362"
---
# <a name="d3dxshmaterial-structure"></a><span data-ttu-id="6d0a6-103">D3DXSHMATERIAL-Struktur</span><span class="sxs-lookup"><span data-stu-id="6d0a6-103">D3DXSHMATERIAL structure</span></span>

<span data-ttu-id="6d0a6-104">Material Merkmale für die präberechnete Glanz Farbe (SH) (SH).</span><span class="sxs-lookup"><span data-stu-id="6d0a6-104">Spherical harmonic (SH) precomputed radiance transfer (PRT) material characteristics.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d0a6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d0a6-105">Syntax</span></span>


```C++
typedef struct D3DXSHMATERIAL {
  D3DCOLORVALUE Diffuse;
  BOOL          bMirror;
  BOOL          bSubSurf;
  FLOAT         RelativeIndexOfRefraction;
  D3DCOLORVALUE Absorption;
  D3DCOLORVALUE ReducedScattering;
} D3DXSHMATERIAL, *LPD3DXSHMATERIAL;
```



## <a name="members"></a><span data-ttu-id="6d0a6-106">Member</span><span class="sxs-lookup"><span data-stu-id="6d0a6-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="6d0a6-107">**Diffus**</span><span class="sxs-lookup"><span data-stu-id="6d0a6-107">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="6d0a6-108">Typ: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="6d0a6-108">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6d0a6-109">Diffuses Albedo der Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="6d0a6-109">Diffuse albedo of the surface.</span></span> <span data-ttu-id="6d0a6-110">Dieser Wert wird ignoriert, wenn das Objekt eine Spiegelung ist.</span><span class="sxs-lookup"><span data-stu-id="6d0a6-110">This value is ignored if the object is a mirror.</span></span>

</dd> <dt>

<span data-ttu-id="6d0a6-111">**bmirror**</span><span class="sxs-lookup"><span data-stu-id="6d0a6-111">**bMirror**</span></span>
</dt> <dd>

<span data-ttu-id="6d0a6-112">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6d0a6-112">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6d0a6-113">Muss auf " **false**" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6d0a6-113">Must be set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="6d0a6-114">**bsubsurf**</span><span class="sxs-lookup"><span data-stu-id="6d0a6-114">**bSubSurf**</span></span>
</dt> <dd>

<span data-ttu-id="6d0a6-115">Typ: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6d0a6-115">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6d0a6-116">Auf " **true** " festlegen, um unter Oberflächen-Scattering zu aktivieren; jedes Objekt, das die unter oberflächenzererung durchführt, darf kein Spiegel sein.</span><span class="sxs-lookup"><span data-stu-id="6d0a6-116">Set to **TRUE** to enable subsurface scattering; any object that does subsurface scattering cannot be a mirror.</span></span>

</dd> <dt>

<span data-ttu-id="6d0a6-117">**Relativeingedexofrebruchteil**</span><span class="sxs-lookup"><span data-stu-id="6d0a6-117">**RelativeIndexOfRefraction**</span></span>
</dt> <dd>

<span data-ttu-id="6d0a6-118">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6d0a6-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6d0a6-119">Der relative Index der abbrechungs Rate ist das Verhältnis zwischen zwei absoluten Indizes der abbrechungs Rate.</span><span class="sxs-lookup"><span data-stu-id="6d0a6-119">Relative index of refraction is the ratio between two absolute indexes of refraction.</span></span> <span data-ttu-id="6d0a6-120">Ein Index der abbrechungs Rate ist das Verhältnis des Sinus des Winkels in den Sinus des Winkels der abbrechungs Spitze.</span><span class="sxs-lookup"><span data-stu-id="6d0a6-120">An index of refraction is the ratio of the sine of the angle of incidence to the sine of the angle of refraction.</span></span>

</dd> <dt>

<span data-ttu-id="6d0a6-121">**Übernahme**</span><span class="sxs-lookup"><span data-stu-id="6d0a6-121">**Absorption**</span></span>
</dt> <dd>

<span data-ttu-id="6d0a6-122">Typ: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="6d0a6-122">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6d0a6-123">Der Absorptionskoeffizienten ist ein Parameter für die volumerenderinggleichung, mit der die Licht Weitergabe auf einem teilnehmenden Medium modelliert wird</span><span class="sxs-lookup"><span data-stu-id="6d0a6-123">The absorption coefficient is a parameter to the volume rendering equation used to model light propagation in a participating medium.</span></span>

</dd> <dt>

<span data-ttu-id="6d0a6-124">**Reducedscattering**</span><span class="sxs-lookup"><span data-stu-id="6d0a6-124">**ReducedScattering**</span></span>
</dt> <dd>

<span data-ttu-id="6d0a6-125">Typ: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="6d0a6-125">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6d0a6-126">Der reduzierte Streuungs Koeffizienten ist ein Parameter für die volumerenderinggleichung, die zum Modellieren der Licht Weitergabe in einem teilnehmenden Medium verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6d0a6-126">The reduced scattering coefficient is a parameter to the volume rendering equation used to model light propagation in a participating medium.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6d0a6-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d0a6-127">Remarks</span></span>

<span data-ttu-id="6d0a6-128">Nicht--spektrale Szenen verwenden den roten Kanal aus den Materialien anstelle des Leuchtkraft Werts.</span><span class="sxs-lookup"><span data-stu-id="6d0a6-128">Non-spectral scenes use the red channel from the materials instead of the luminance value.</span></span>

<span data-ttu-id="6d0a6-129">Weitere Informationen zu PRT finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="6d0a6-129">For more information about PRT see:</span></span>

-   <span data-ttu-id="6d0a6-130">Jensen, Henrik wann, et al. SIGGRAPH-Prozess: ein praktisches Modell für den subsurface Light-Transport, 2001.</span><span class="sxs-lookup"><span data-stu-id="6d0a6-130">Jensen, Henrik Wann, et al. Siggraph Proceedings: A Practical Model for Subsurface Light Transport, 2001.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d0a6-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d0a6-131">Requirements</span></span>



| <span data-ttu-id="6d0a6-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6d0a6-132">Requirement</span></span> | <span data-ttu-id="6d0a6-133">Wert</span><span class="sxs-lookup"><span data-stu-id="6d0a6-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d0a6-134">Header</span><span class="sxs-lookup"><span data-stu-id="6d0a6-134">Header</span></span><br/> | <dl> <span data-ttu-id="6d0a6-135"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d0a6-135"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d0a6-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d0a6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d0a6-137">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="6d0a6-137">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
