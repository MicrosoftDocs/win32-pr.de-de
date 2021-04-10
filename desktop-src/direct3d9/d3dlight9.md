---
description: Definiert einen Satz von Beleuchtungs Eigenschaften.
ms.assetid: 25ce9d72-949c-41fc-8e3b-146d6a2de0dc
title: D3DLIGHT9-Struktur (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLIGHT9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 90e72fbb2bf4f1d74a74dc177346387b36eb25e0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219569"
---
# <a name="d3dlight9-structure"></a><span data-ttu-id="bde23-103">D3DLIGHT9-Struktur</span><span class="sxs-lookup"><span data-stu-id="bde23-103">D3DLIGHT9 structure</span></span>

<span data-ttu-id="bde23-104">Definiert einen Satz von Beleuchtungs Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="bde23-104">Defines a set of lighting properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bde23-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bde23-105">Syntax</span></span>


```C++
typedef struct D3DLIGHT9 {
  D3DLIGHTTYPE  Type;
  D3DCOLORVALUE Diffuse;
  D3DCOLORVALUE Specular;
  D3DCOLORVALUE Ambient;
  D3DVECTOR     Position;
  D3DVECTOR     Direction;
  float         Range;
  float         Falloff;
  float         Attenuation0;
  float         Attenuation1;
  float         Attenuation2;
  float         Theta;
  float         Phi;
} D3DLIGHT9, *LPD3DLIGHT;
```



## <a name="members"></a><span data-ttu-id="bde23-106">Member</span><span class="sxs-lookup"><span data-stu-id="bde23-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="bde23-107">**Type**</span><span class="sxs-lookup"><span data-stu-id="bde23-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="bde23-108">Typ: **[ **D3DLIGHTTYPE**](./d3dlighttype.md)**</span><span class="sxs-lookup"><span data-stu-id="bde23-108">Type: **[**D3DLIGHTTYPE**](./d3dlighttype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bde23-109">Der Typ der Lichtquelle.</span><span class="sxs-lookup"><span data-stu-id="bde23-109">Type of the light source.</span></span> <span data-ttu-id="bde23-110">Dieser Wert ist einer der Member des [**D3DLIGHTTYPE**](./d3dlighttype.md) -Enumerationstyps.</span><span class="sxs-lookup"><span data-stu-id="bde23-110">This value is one of the members of the [**D3DLIGHTTYPE**](./d3dlighttype.md) enumerated type.</span></span>

</dd> <dt>

<span data-ttu-id="bde23-111">**Diffus**</span><span class="sxs-lookup"><span data-stu-id="bde23-111">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="bde23-112">Typ: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="bde23-112">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bde23-113">Vom Licht ausgegebene diffuse Farbe.</span><span class="sxs-lookup"><span data-stu-id="bde23-113">Diffuse color emitted by the light.</span></span> <span data-ttu-id="bde23-114">Dieser Member ist eine [**D3DCOLORVALUE**](d3dcolorvalue.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="bde23-114">This member is a [**D3DCOLORVALUE**](d3dcolorvalue.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="bde23-115">**Glänzend**</span><span class="sxs-lookup"><span data-stu-id="bde23-115">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="bde23-116">Typ: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="bde23-116">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bde23-117">Glanz Farbe, die vom Licht ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="bde23-117">Specular color emitted by the light.</span></span> <span data-ttu-id="bde23-118">Dieser Member ist eine [**D3DCOLORVALUE**](d3dcolorvalue.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="bde23-118">This member is a [**D3DCOLORVALUE**](d3dcolorvalue.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="bde23-119">**Umgebend**</span><span class="sxs-lookup"><span data-stu-id="bde23-119">**Ambient**</span></span>
</dt> <dd>

<span data-ttu-id="bde23-120">Typ: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="bde23-120">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bde23-121">Umgebungs Farbe, die vom Licht ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="bde23-121">Ambient color emitted by the light.</span></span> <span data-ttu-id="bde23-122">Dieser Member ist eine [**D3DCOLORVALUE**](d3dcolorvalue.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="bde23-122">This member is a [**D3DCOLORVALUE**](d3dcolorvalue.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="bde23-123">**Position**</span><span class="sxs-lookup"><span data-stu-id="bde23-123">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="bde23-124">Typ: **[ **D3DVECTOR**](d3dvector.md)**</span><span class="sxs-lookup"><span data-stu-id="bde23-124">Type: **[**D3DVECTOR**](d3dvector.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bde23-125">Die Position des Lichts im Raum, der durch eine [**D3DVECTOR**](d3dvector.md) -Struktur angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="bde23-125">Position of the light in world space, specified by a [**D3DVECTOR**](d3dvector.md) structure.</span></span> <span data-ttu-id="bde23-126">Dieser Member hat keine Bedeutung für direktionale Lichter und wird in diesem Fall ignoriert.</span><span class="sxs-lookup"><span data-stu-id="bde23-126">This member has no meaning for directional lights and is ignored in that case.</span></span>

</dd> <dt>

<span data-ttu-id="bde23-127">**Richtung**</span><span class="sxs-lookup"><span data-stu-id="bde23-127">**Direction**</span></span>
</dt> <dd>

<span data-ttu-id="bde23-128">Typ: **[ **D3DVECTOR**](d3dvector.md)**</span><span class="sxs-lookup"><span data-stu-id="bde23-128">Type: **[**D3DVECTOR**](d3dvector.md)**</span></span>

</dd> <dd>

<span data-ttu-id="bde23-129">Die Richtung, die das Licht im Raum der Welt zeigt, die durch eine [**D3DVECTOR**](d3dvector.md) -Struktur angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="bde23-129">Direction that the light is pointing in world space, specified by a [**D3DVECTOR**](d3dvector.md) structure.</span></span> <span data-ttu-id="bde23-130">Dieser Member hat nur für direktionale und Scheinwerfer Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="bde23-130">This member has meaning only for directional and spotlights.</span></span> <span data-ttu-id="bde23-131">Dieser Vektor muss nicht normalisiert werden, er sollte jedoch eine Länge ungleich NULL aufweisen.</span><span class="sxs-lookup"><span data-stu-id="bde23-131">This vector need not be normalized, but it should have a nonzero length.</span></span>

</dd> <dt>

<span data-ttu-id="bde23-132">**Bereich**</span><span class="sxs-lookup"><span data-stu-id="bde23-132">**Range**</span></span>
</dt> <dd>

<span data-ttu-id="bde23-133">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="bde23-133">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="bde23-134">Der Abstand, über den das Licht keine Auswirkung hat.</span><span class="sxs-lookup"><span data-stu-id="bde23-134">Distance beyond which the light has no effect.</span></span> <span data-ttu-id="bde23-135">Der maximal zulässige Wert für diesen Member ist die Quadratwurzel von FLT \_ Max.</span><span class="sxs-lookup"><span data-stu-id="bde23-135">The maximum allowable value for this member is the square root of FLT\_MAX.</span></span> <span data-ttu-id="bde23-136">Dieser Member wirkt sich nicht auf direktionale Lichter aus.</span><span class="sxs-lookup"><span data-stu-id="bde23-136">This member does not affect directional lights.</span></span>

</dd> <dt>

<span data-ttu-id="bde23-137">**Übergang**</span><span class="sxs-lookup"><span data-stu-id="bde23-137">**Falloff**</span></span>
</dt> <dd>

<span data-ttu-id="bde23-138">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="bde23-138">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="bde23-139">Verringerung der Beleuchtung zwischen dem inneren Kegel eines Spotlight (dem von der TA angegebenen Winkel) und dem äußeren Rand des äußeren Kegel (der von Phi angegebene Winkel).</span><span class="sxs-lookup"><span data-stu-id="bde23-139">Decrease in illumination between a spotlight's inner cone (the angle specified by Theta) and the outer edge of the outer cone (the angle specified by Phi).</span></span>

<span data-ttu-id="bde23-140">Die Auswirkung von "atzuweisung" auf die Beleuchtung ist sehr gering.</span><span class="sxs-lookup"><span data-stu-id="bde23-140">The effect of falloff on the lighting is subtle.</span></span> <span data-ttu-id="bde23-141">Darüber hinaus wird eine geringe Leistungs Einbuße durch die Strukturierung der "f-Zuweisung"-Kurve verursacht.</span><span class="sxs-lookup"><span data-stu-id="bde23-141">Furthermore, a small performance penalty is incurred by shaping the falloff curve.</span></span> <span data-ttu-id="bde23-142">Aus diesen Gründen legen die meisten Entwickler diesen Wert auf 1,0 fest.</span><span class="sxs-lookup"><span data-stu-id="bde23-142">For these reasons, most developers set this value to 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="bde23-143">**Attenuation0**</span><span class="sxs-lookup"><span data-stu-id="bde23-143">**Attenuation0**</span></span>
</dt> <dd>

<span data-ttu-id="bde23-144">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="bde23-144">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="bde23-145">Ein Wert, der angibt, wie sich die Lichtintensität über den Abstand ändert</span><span class="sxs-lookup"><span data-stu-id="bde23-145">Value specifying how the light intensity changes over distance.</span></span> <span data-ttu-id="bde23-146">Die Dämpfungswerte werden bei direktionalen Lichtern ignoriert.</span><span class="sxs-lookup"><span data-stu-id="bde23-146">Attenuation values are ignored for directional lights.</span></span> <span data-ttu-id="bde23-147">Dieser Member stellt eine Dämpfungs Konstante dar.</span><span class="sxs-lookup"><span data-stu-id="bde23-147">This member represents an attenuation constant.</span></span> <span data-ttu-id="bde23-148">Weitere Informationen zur Dämpfung finden Sie unter [Light Properties (Direct3D 9)](light-properties.md).</span><span class="sxs-lookup"><span data-stu-id="bde23-148">For information about attenuation, see [Light Properties (Direct3D 9)](light-properties.md).</span></span> <span data-ttu-id="bde23-149">Gültige Werte für diesen Member liegen zwischen 0,0 und unendlich.</span><span class="sxs-lookup"><span data-stu-id="bde23-149">Valid values for this member range from 0.0 to infinity.</span></span> <span data-ttu-id="bde23-150">Bei nicht direktionalen Lichtern sollten alle drei Dämpfungswerte nicht gleichzeitig auf 0,0 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="bde23-150">For non-directional lights, all three attenuation values should not be set to 0.0 at the same time.</span></span>

</dd> <dt>

<span data-ttu-id="bde23-151">**Attenuation1**</span><span class="sxs-lookup"><span data-stu-id="bde23-151">**Attenuation1**</span></span>
</dt> <dd>

<span data-ttu-id="bde23-152">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="bde23-152">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="bde23-153">Ein Wert, der angibt, wie sich die Lichtintensität über den Abstand ändert</span><span class="sxs-lookup"><span data-stu-id="bde23-153">Value specifying how the light intensity changes over distance.</span></span> <span data-ttu-id="bde23-154">Die Dämpfungswerte werden bei direktionalen Lichtern ignoriert.</span><span class="sxs-lookup"><span data-stu-id="bde23-154">Attenuation values are ignored for directional lights.</span></span> <span data-ttu-id="bde23-155">Dieser Member stellt eine Dämpfungs Konstante dar.</span><span class="sxs-lookup"><span data-stu-id="bde23-155">This member represents an attenuation constant.</span></span> <span data-ttu-id="bde23-156">Weitere Informationen zur Dämpfung finden Sie unter [Light Properties (Direct3D 9)](light-properties.md).</span><span class="sxs-lookup"><span data-stu-id="bde23-156">For information about attenuation, see [Light Properties (Direct3D 9)](light-properties.md).</span></span> <span data-ttu-id="bde23-157">Gültige Werte für diesen Member liegen zwischen 0,0 und unendlich.</span><span class="sxs-lookup"><span data-stu-id="bde23-157">Valid values for this member range from 0.0 to infinity.</span></span> <span data-ttu-id="bde23-158">Bei nicht direktionalen Lichtern sollten alle drei Dämpfungswerte nicht gleichzeitig auf 0,0 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="bde23-158">For non-directional lights, all three attenuation values should not be set to 0.0 at the same time.</span></span>

</dd> <dt>

<span data-ttu-id="bde23-159">**Attenuation2**</span><span class="sxs-lookup"><span data-stu-id="bde23-159">**Attenuation2**</span></span>
</dt> <dd>

<span data-ttu-id="bde23-160">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="bde23-160">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="bde23-161">Ein Wert, der angibt, wie sich die Lichtintensität über den Abstand ändert</span><span class="sxs-lookup"><span data-stu-id="bde23-161">Value specifying how the light intensity changes over distance.</span></span> <span data-ttu-id="bde23-162">Die Dämpfungswerte werden bei direktionalen Lichtern ignoriert.</span><span class="sxs-lookup"><span data-stu-id="bde23-162">Attenuation values are ignored for directional lights.</span></span> <span data-ttu-id="bde23-163">Dieser Member stellt eine Dämpfungs Konstante dar.</span><span class="sxs-lookup"><span data-stu-id="bde23-163">This member represents an attenuation constant.</span></span> <span data-ttu-id="bde23-164">Weitere Informationen zur Dämpfung finden Sie unter [Light Properties (Direct3D 9)](light-properties.md).</span><span class="sxs-lookup"><span data-stu-id="bde23-164">For information about attenuation, see [Light Properties (Direct3D 9)](light-properties.md).</span></span> <span data-ttu-id="bde23-165">Gültige Werte für diesen Member liegen zwischen 0,0 und unendlich.</span><span class="sxs-lookup"><span data-stu-id="bde23-165">Valid values for this member range from 0.0 to infinity.</span></span> <span data-ttu-id="bde23-166">Bei nicht direktionalen Lichtern sollten alle drei Dämpfungswerte nicht gleichzeitig auf 0,0 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="bde23-166">For non-directional lights, all three attenuation values should not be set to 0.0 at the same time.</span></span>

</dd> <dt>

<span data-ttu-id="bde23-167">**Theta**</span><span class="sxs-lookup"><span data-stu-id="bde23-167">**Theta**</span></span>
</dt> <dd>

<span data-ttu-id="bde23-168">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="bde23-168">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="bde23-169">Der Winkel im Bogenmaße des inneren Kegel eines Spotlight, d. h. der vollständig beleuchtete Spotlight-Kegel.</span><span class="sxs-lookup"><span data-stu-id="bde23-169">Angle, in radians, of a spotlight's inner cone - that is, the fully illuminated spotlight cone.</span></span> <span data-ttu-id="bde23-170">Dieser Wert muss zwischen 0 und dem von Phi angegebenen Wert liegen.</span><span class="sxs-lookup"><span data-stu-id="bde23-170">This value must be in the range from 0 through the value specified by Phi.</span></span>

</dd> <dt>

<span data-ttu-id="bde23-171">**Patientendaten**</span><span class="sxs-lookup"><span data-stu-id="bde23-171">**Phi**</span></span>
</dt> <dd>

<span data-ttu-id="bde23-172">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="bde23-172">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="bde23-173">Der Winkel im Bogenmaße, der den äußeren Rand des äußeren Rands des Spotlight definiert.</span><span class="sxs-lookup"><span data-stu-id="bde23-173">Angle, in radians, defining the outer edge of the spotlight's outer cone.</span></span> <span data-ttu-id="bde23-174">Punkte außerhalb dieses Kegel werden nicht durch das Spotlight beleuchtet.</span><span class="sxs-lookup"><span data-stu-id="bde23-174">Points outside this cone are not lit by the spotlight.</span></span> <span data-ttu-id="bde23-175">Dieser Wert muss zwischen 0 und PI liegen.</span><span class="sxs-lookup"><span data-stu-id="bde23-175">This value must be between 0 and pi.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bde23-176">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bde23-176">Requirements</span></span>



| <span data-ttu-id="bde23-177">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bde23-177">Requirement</span></span> | <span data-ttu-id="bde23-178">Wert</span><span class="sxs-lookup"><span data-stu-id="bde23-178">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bde23-179">Header</span><span class="sxs-lookup"><span data-stu-id="bde23-179">Header</span></span><br/> | <dl> <span data-ttu-id="bde23-180"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="bde23-180"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bde23-181">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bde23-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bde23-182">Direct3D-Strukturen</span><span class="sxs-lookup"><span data-stu-id="bde23-182">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="bde23-183">**GetLight**</span><span class="sxs-lookup"><span data-stu-id="bde23-183">**GetLight**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getlight)
</dt> <dt>

[<span data-ttu-id="bde23-184">**Setlight**</span><span class="sxs-lookup"><span data-stu-id="bde23-184">**SetLight**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight)
</dt> </dl>

 

 
