---
description: Definiert die Scheitelpunkt Deklarations Methode, bei der es sich um einen vordefinierten Vorgang handelt, der vom Mosaik Prozess (oder einer beliebigen prozeduralen Geometrie Routine auf den Scheitelpunkt Daten während des Mosaik Vorgangs) ausgeführt wird.
ms.assetid: 030e04a6-4e2d-4756-80ef-e4a6a0103fd1
title: D3DDECLMETHOD-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDECLMETHOD
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 534fef5a4eaf9d22d502097124dcecdb91433f73
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354386"
---
# <a name="d3ddeclmethod-enumeration"></a><span data-ttu-id="1814b-103">D3DDECLMETHOD-Enumeration</span><span class="sxs-lookup"><span data-stu-id="1814b-103">D3DDECLMETHOD enumeration</span></span>

<span data-ttu-id="1814b-104">Definiert die Scheitelpunkt Deklarations Methode, bei der es sich um einen vordefinierten Vorgang handelt, der vom Mosaik Prozess (oder einer beliebigen prozeduralen Geometrie Routine auf den Scheitelpunkt Daten während des Mosaik Vorgangs) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1814b-104">Defines the vertex declaration method which is a predefined operation performed by the tessellator (or any procedural geometry routine on the vertex data during tessellation).</span></span>

## <a name="syntax"></a><span data-ttu-id="1814b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1814b-105">Syntax</span></span>


```C++
typedef enum D3DDECLMETHOD { 
  D3DDECLMETHOD_DEFAULT           = 0,
  D3DDECLMETHOD_PARTIALU          = 1,
  D3DDECLMETHOD_PARTIALV          = 2,
  D3DDECLMETHOD_CROSSUV           = 3,
  D3DDECLMETHOD_UV                = 4,
  D3DDECLMETHOD_LOOKUP            = 5,
  D3DDECLMETHOD_LOOKUPPRESAMPLED  = 6
} D3DDECLMETHOD, *LPD3DDECLMETHOD;
```



## <a name="constants"></a><span data-ttu-id="1814b-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="1814b-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1814b-107"><span id="D3DDECLMETHOD_DEFAULT"></span><span id="d3ddeclmethod_default"></span>**D3DDECLMETHOD \_ Standard**</span><span class="sxs-lookup"><span data-stu-id="1814b-107"><span id="D3DDECLMETHOD_DEFAULT"></span><span id="d3ddeclmethod_default"></span>**D3DDECLMETHOD\_DEFAULT**</span></span>
</dt> <dd>

<span data-ttu-id="1814b-108">Standardwert.</span><span class="sxs-lookup"><span data-stu-id="1814b-108">Default value.</span></span> <span data-ttu-id="1814b-109">Der Mosaik Dienst kopiert die Scheitelpunkt Daten (Spline-Daten für Patches) unverändert und ohne zusätzliche Berechnungen.</span><span class="sxs-lookup"><span data-stu-id="1814b-109">The tessellator copies the vertex data (spline data for patches) as is, with no additional calculations.</span></span> <span data-ttu-id="1814b-110">Wenn der Mosaik Prozess verwendet wird, wird dieses Element interpoliert.</span><span class="sxs-lookup"><span data-stu-id="1814b-110">When the tessellator is used, this element is interpolated.</span></span> <span data-ttu-id="1814b-111">Andernfalls werden Scheitelpunkt Daten in das Eingabe Register kopiert.</span><span class="sxs-lookup"><span data-stu-id="1814b-111">Otherwise vertex data is copied into the input register.</span></span> <span data-ttu-id="1814b-112">Der Eingabe-und Ausgabetyp kann ein beliebiger Wert sein, aber immer derselbe Typ.</span><span class="sxs-lookup"><span data-stu-id="1814b-112">The input and output type can be any value, but are always the same type.</span></span>

</dd> <dt>

<span data-ttu-id="1814b-113"><span id="D3DDECLMETHOD_PARTIALU"></span><span id="d3ddeclmethod_partialu"></span>**D3DDECLMETHOD \_ partialu**</span><span class="sxs-lookup"><span data-stu-id="1814b-113"><span id="D3DDECLMETHOD_PARTIALU"></span><span id="d3ddeclmethod_partialu"></span>**D3DDECLMETHOD\_PARTIALU**</span></span>
</dt> <dd>

<span data-ttu-id="1814b-114">Berechnet den Tangens an einem Punkt des Rechtecks oder Dreiecks Patches in der U-Richtung.</span><span class="sxs-lookup"><span data-stu-id="1814b-114">Computes the tangent at a point on the rectangle or triangle patch in the U direction.</span></span> <span data-ttu-id="1814b-115">Der Eingabetyp kann einer der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="1814b-115">The input type can be one of the following:</span></span>

-   <span data-ttu-id="1814b-116">D3DDECLTYPE \_ D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="1814b-116">D3DDECLTYPE\_D3DCOLOR</span></span>
-   <span data-ttu-id="1814b-117">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="1814b-117">D3DDECLTYPE\_FLOAT3</span></span>
-   <span data-ttu-id="1814b-118">D3DDECLTYPE \_ float4</span><span class="sxs-lookup"><span data-stu-id="1814b-118">D3DDECLTYPE\_FLOAT4</span></span>
-   <span data-ttu-id="1814b-119">D3DDECLTYPE \_ SHORT4</span><span class="sxs-lookup"><span data-stu-id="1814b-119">D3DDECLTYPE\_SHORT4</span></span>
-   <span data-ttu-id="1814b-120">D3DDECLTYPE \_ UBYTE4</span><span class="sxs-lookup"><span data-stu-id="1814b-120">D3DDECLTYPE\_UBYTE4</span></span>

<span data-ttu-id="1814b-121">Der Ausgabetyp ist immer D3DDECLTYPE \_ FLOAT3.</span><span class="sxs-lookup"><span data-stu-id="1814b-121">The output type is always D3DDECLTYPE\_FLOAT3.</span></span>

</dd> <dt>

<span data-ttu-id="1814b-122"><span id="D3DDECLMETHOD_PARTIALV"></span><span id="d3ddeclmethod_partialv"></span>**D3DDECLMETHOD \_ partialv**</span><span class="sxs-lookup"><span data-stu-id="1814b-122"><span id="D3DDECLMETHOD_PARTIALV"></span><span id="d3ddeclmethod_partialv"></span>**D3DDECLMETHOD\_PARTIALV**</span></span>
</dt> <dd>

<span data-ttu-id="1814b-123">Berechnet den Tangens an einem Punkt des Rechtecks oder Dreiecks Patches in der V-Richtung.</span><span class="sxs-lookup"><span data-stu-id="1814b-123">Computes the tangent at a point on the rectangle or triangle patch in the V direction.</span></span> <span data-ttu-id="1814b-124">Der Eingabetyp kann einer der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="1814b-124">The input type can be one of the following:</span></span>

-   <span data-ttu-id="1814b-125">D3DDECLTYPE \_ D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="1814b-125">D3DDECLTYPE\_D3DCOLOR</span></span>
-   <span data-ttu-id="1814b-126">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="1814b-126">D3DDECLTYPE\_FLOAT3</span></span>
-   <span data-ttu-id="1814b-127">D3DDECLTYPE \_ float4</span><span class="sxs-lookup"><span data-stu-id="1814b-127">D3DDECLTYPE\_FLOAT4</span></span>
-   <span data-ttu-id="1814b-128">D3DDECLTYPE \_ SHORT4</span><span class="sxs-lookup"><span data-stu-id="1814b-128">D3DDECLTYPE\_SHORT4</span></span>
-   <span data-ttu-id="1814b-129">D3DDECLTYPE \_ UBYTE4</span><span class="sxs-lookup"><span data-stu-id="1814b-129">D3DDECLTYPE\_UBYTE4</span></span>

<span data-ttu-id="1814b-130">Der Ausgabetyp ist immer D3DDECLTYPE \_ FLOAT3.</span><span class="sxs-lookup"><span data-stu-id="1814b-130">The output type is always D3DDECLTYPE\_FLOAT3.</span></span>

</dd> <dt>

<span data-ttu-id="1814b-131"><span id="D3DDECLMETHOD_CROSSUV"></span><span id="d3ddeclmethod_crossuv"></span>**D3DDECLMETHOD \_ crossuv**</span><span class="sxs-lookup"><span data-stu-id="1814b-131"><span id="D3DDECLMETHOD_CROSSUV"></span><span id="d3ddeclmethod_crossuv"></span>**D3DDECLMETHOD\_CROSSUV**</span></span>
</dt> <dd>

<span data-ttu-id="1814b-132">Berechnet den normalen an einem Punkt des Rechtecks oder Dreiecks Patches, indem das Kreuz Produkt von zwei Tangenten übernommen wird.</span><span class="sxs-lookup"><span data-stu-id="1814b-132">Computes the normal at a point on the rectangle or triangle patch by taking the cross product of two tangents.</span></span> <span data-ttu-id="1814b-133">Der Eingabetyp kann einer der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="1814b-133">The input type can be one of the following:</span></span>

-   <span data-ttu-id="1814b-134">D3DDECLTYPE \_ D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="1814b-134">D3DDECLTYPE\_D3DCOLOR</span></span>
-   <span data-ttu-id="1814b-135">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="1814b-135">D3DDECLTYPE\_FLOAT3</span></span>
-   <span data-ttu-id="1814b-136">D3DDECLTYPE \_ float4</span><span class="sxs-lookup"><span data-stu-id="1814b-136">D3DDECLTYPE\_FLOAT4</span></span>
-   <span data-ttu-id="1814b-137">D3DDECLTYPE \_ SHORT4</span><span class="sxs-lookup"><span data-stu-id="1814b-137">D3DDECLTYPE\_SHORT4</span></span>
-   <span data-ttu-id="1814b-138">D3DDECLTYPE \_ UBYTE4</span><span class="sxs-lookup"><span data-stu-id="1814b-138">D3DDECLTYPE\_UBYTE4</span></span>

<span data-ttu-id="1814b-139">Der Ausgabetyp ist immer D3DDECLTYPE \_ FLOAT3.</span><span class="sxs-lookup"><span data-stu-id="1814b-139">The output type is always D3DDECLTYPE\_FLOAT3.</span></span>

</dd> <dt>

<span data-ttu-id="1814b-140"><span id="D3DDECLMETHOD_UV"></span><span id="d3ddeclmethod_uv"></span>**D3DDECLMETHOD \_ -UV**</span><span class="sxs-lookup"><span data-stu-id="1814b-140"><span id="D3DDECLMETHOD_UV"></span><span id="d3ddeclmethod_uv"></span>**D3DDECLMETHOD\_UV**</span></span>
</dt> <dd>

<span data-ttu-id="1814b-141">Kopieren Sie die U-V-Werte an einem Punkt des Rechtecks oder Dreiecks Patches.</span><span class="sxs-lookup"><span data-stu-id="1814b-141">Copy out the U, V values at a point on the rectangle or triangle patch.</span></span> <span data-ttu-id="1814b-142">Dies führt zu einem 2D-float-Wert.</span><span class="sxs-lookup"><span data-stu-id="1814b-142">This results in a 2D float.</span></span> <span data-ttu-id="1814b-143">Der Eingabetyp muss auf D3DDECLTYPE nicht \_ verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1814b-143">The input type must be set to D3DDECLTYPE\_UNUSED.</span></span> <span data-ttu-id="1814b-144">Der Ausgabedatentyp lautet immer D3DDECLTYPE \_ FLOAT2.</span><span class="sxs-lookup"><span data-stu-id="1814b-144">The output data type is always D3DDECLTYPE\_FLOAT2.</span></span> <span data-ttu-id="1814b-145">Der Eingabestream und Offset werden ebenfalls nicht verwendet (muss jedoch auf 0 festgelegt werden).</span><span class="sxs-lookup"><span data-stu-id="1814b-145">The input stream and offset are also unused (but must be set to 0).</span></span>

</dd> <dt>

<span data-ttu-id="1814b-146"><span id="D3DDECLMETHOD_LOOKUP"></span><span id="d3ddeclmethod_lookup"></span>**D3DDECLMETHOD- \_ Suche**</span><span class="sxs-lookup"><span data-stu-id="1814b-146"><span id="D3DDECLMETHOD_LOOKUP"></span><span id="d3ddeclmethod_lookup"></span>**D3DDECLMETHOD\_LOOKUP**</span></span>
</dt> <dd>

<span data-ttu-id="1814b-147">Suchen Sie eine Verschiebungs Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="1814b-147">Look up a displacement map.</span></span> <span data-ttu-id="1814b-148">Der Eingabetyp kann einer der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="1814b-148">The input type can be one of the following:</span></span>

-   <span data-ttu-id="1814b-149">D3DDECLTYPE \_ FLOAT2</span><span class="sxs-lookup"><span data-stu-id="1814b-149">D3DDECLTYPE\_FLOAT2</span></span>
-   <span data-ttu-id="1814b-150">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="1814b-150">D3DDECLTYPE\_FLOAT3</span></span>
-   <span data-ttu-id="1814b-151">D3DDECLTYPE \_ float4</span><span class="sxs-lookup"><span data-stu-id="1814b-151">D3DDECLTYPE\_FLOAT4</span></span>

<span data-ttu-id="1814b-152">Nur die x-und y-Komponenten werden für die Textur kartogramm-Suche verwendet.</span><span class="sxs-lookup"><span data-stu-id="1814b-152">Only the .x and .y components are used for the texture map lookup.</span></span> <span data-ttu-id="1814b-153">Der Ausgabetyp ist immer D3DDECLTYPE \_ FLOAT1.</span><span class="sxs-lookup"><span data-stu-id="1814b-153">The output type is always D3DDECLTYPE\_FLOAT1.</span></span> <span data-ttu-id="1814b-154">Das Gerät muss die Verschiebungs Zuordnung unterstützen.</span><span class="sxs-lookup"><span data-stu-id="1814b-154">The device must support displacement mapping.</span></span> <span data-ttu-id="1814b-155">Weitere Informationen zur Verschiebungs Zuordnung finden Sie unter [Verschiebungs Zuordnung (Direct3D 9)](displacement-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="1814b-155">For more information about displacement mapping, see [Displacement Mapping (Direct3D 9)](displacement-mapping.md).</span></span> <span data-ttu-id="1814b-156">Diese Konstante wird nur von der programmierbaren Pipeline für n-Patchdaten unterstützt, wenn n-Patches aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="1814b-156">This constant is supported only by the programmable pipeline on N-patch data, if N-patches are enabled.</span></span>

</dd> <dt>

<span data-ttu-id="1814b-157"><span id="D3DDECLMETHOD_LOOKUPPRESAMPLED"></span><span id="d3ddeclmethod_lookuppresampled"></span>**D3DDECLMETHOD \_ lookuppresampling**</span><span class="sxs-lookup"><span data-stu-id="1814b-157"><span id="D3DDECLMETHOD_LOOKUPPRESAMPLED"></span><span id="d3ddeclmethod_lookuppresampled"></span>**D3DDECLMETHOD\_LOOKUPPRESAMPLED**</span></span>
</dt> <dd>

<span data-ttu-id="1814b-158">Suchen Sie eine Verschiebungs Zuordnung mit präsampling.</span><span class="sxs-lookup"><span data-stu-id="1814b-158">Look up a presampled displacement map.</span></span> <span data-ttu-id="1814b-159">Der Eingabetyp muss auf D3DDECLTYPE nicht \_ verwendet werden. der streamindex und der Streamoffset müssen auf 0 festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1814b-159">The input type must be set to D3DDECLTYPE\_UNUSED; the stream index and the stream offset must be set to 0.</span></span> <span data-ttu-id="1814b-160">Der Ausgabetyp für diesen Vorgang lautet immer D3DDECLTYPE \_ FLOAT1.</span><span class="sxs-lookup"><span data-stu-id="1814b-160">The output type for this operation is always D3DDECLTYPE\_FLOAT1.</span></span> <span data-ttu-id="1814b-161">Das Gerät muss die Verschiebungs Zuordnung unterstützen.</span><span class="sxs-lookup"><span data-stu-id="1814b-161">The device must support displacement mapping.</span></span> <span data-ttu-id="1814b-162">Weitere Informationen zur Verschiebungs Zuordnung finden Sie unter [Verschiebungs Zuordnung (Direct3D 9)](displacement-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="1814b-162">For more information about displacement mapping, see [Displacement Mapping (Direct3D 9)](displacement-mapping.md).</span></span> <span data-ttu-id="1814b-163">Diese Konstante wird nur von der programmierbaren Pipeline für n-Patchdaten unterstützt, wenn n-Patches aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="1814b-163">This constant is supported only by the programmable pipeline on N-patch data, if N-patches are enabled.</span></span> <span data-ttu-id="1814b-164">Diese Methode kann nur mit D3DDECLUSAGE Sample verwendet werden \_ .</span><span class="sxs-lookup"><span data-stu-id="1814b-164">This method can be used only with D3DDECLUSAGE\_SAMPLE.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1814b-165">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1814b-165">Remarks</span></span>

<span data-ttu-id="1814b-166">Der Mosaik Prozess untersucht die-Methode, um zu bestimmen, welche Daten während des Mosaik Prozesses aus den Scheitelpunkt Daten berechnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1814b-166">The tessellator looks at the method to determine what data to calculate from the vertex data during tessellation.</span></span> <span data-ttu-id="1814b-167">Für Mesh-Daten sollte der Standardwert verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1814b-167">Mesh data should use the default value.</span></span> <span data-ttu-id="1814b-168">Patches können jeden der anderen implementierten Typen verwenden.</span><span class="sxs-lookup"><span data-stu-id="1814b-168">Patches can use any of the other implemented types.</span></span>

<span data-ttu-id="1814b-169">Vertex-Daten werden mit einem Array von [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) -Strukturen deklariert.</span><span class="sxs-lookup"><span data-stu-id="1814b-169">Vertex data is declared with an array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) structures.</span></span> <span data-ttu-id="1814b-170">Jedes Element im Array enthält eine Scheitelpunkt Deklarations Methode.</span><span class="sxs-lookup"><span data-stu-id="1814b-170">Each element in the array contains a vertex declaration method.</span></span>

<span data-ttu-id="1814b-171">Neben der Verwendung von D3DDECLMETHOD \_ Default kann ein normales Mesh \_ die D3DDECLMETHOD Lookup-Methode und die D3DDECLMETHOD \_ lookuppresampling-Methode verwenden, wenn N-Patches aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="1814b-171">In addition to using D3DDECLMETHOD\_DEFAULT, a normal mesh can use D3DDECLMETHOD\_LOOKUP and D3DDECLMETHOD\_LOOKUPPRESAMPLED methods when N-patches are enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="1814b-172">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1814b-172">Requirements</span></span>



| <span data-ttu-id="1814b-173">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1814b-173">Requirement</span></span> | <span data-ttu-id="1814b-174">Wert</span><span class="sxs-lookup"><span data-stu-id="1814b-174">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1814b-175">Header</span><span class="sxs-lookup"><span data-stu-id="1814b-175">Header</span></span><br/> | <dl> <span data-ttu-id="1814b-176"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="1814b-176"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1814b-177">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1814b-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1814b-178">Direct3D-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="1814b-178">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




