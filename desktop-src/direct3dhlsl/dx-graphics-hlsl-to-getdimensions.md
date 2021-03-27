---
title: GetDimensions (DirectX HLSL-Textur Objekt)
description: Ruft Textur Größen Informationen ab. Der Syntax Block zeigt alle Parameter an, die in der Methoden Deklaration möglich sind. Die Tabelle im Abschnitt "Hinweise" zeigt, welche Parameter für jeden Textur Objekttyp implementiert werden.
ms.assetid: b72e54da-382a-4b90-bbfe-0b32effc7c05
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0ad4be68049c92955c5ddb06a0c5eccfe2c26b77
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857763"
---
# <a name="getdimensions-directx-hlsl-texture-object"></a><span data-ttu-id="1fb5d-105">GetDimensions (DirectX HLSL-Textur Objekt)</span><span class="sxs-lookup"><span data-stu-id="1fb5d-105">GetDimensions (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="1fb5d-106">Ruft Textur Größen Informationen ab.</span><span class="sxs-lookup"><span data-stu-id="1fb5d-106">Gets texture size information.</span></span> <span data-ttu-id="1fb5d-107">Der Syntax Block zeigt alle Parameter an, die in der Methoden Deklaration möglich sind.</span><span class="sxs-lookup"><span data-stu-id="1fb5d-107">The syntax block shows all the parameters that are possible in the method declaration.</span></span> <span data-ttu-id="1fb5d-108">Die Tabelle im Abschnitt "Hinweise" zeigt, welche Parameter für jeden Textur Objekttyp implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="1fb5d-108">The table in the Remarks section shows which parameters are implemented for each texture-object type.</span></span>



|                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fb5d-109">void Object. GetDimensions (uint miplevel, Typex Width, Typex Height, Typex-Elemente, Typex-Tiefe, Typex-nummerierer, Typex-nummerierproben);</span><span class="sxs-lookup"><span data-stu-id="1fb5d-109">void Object.GetDimensions( UINT MipLevel, typeX Width, typeX Height, typeX Elements, typeX Depth, typeX NumberOfLevels, typeX NumberOfSamples );</span></span> |



 

<span data-ttu-id="1fb5d-110">TypeX gibt an, dass zwei mögliche Typen vorhanden sind: " **uint** " oder " **float**".</span><span class="sxs-lookup"><span data-stu-id="1fb5d-110">typeX denotes that there are two possible types: **uint** or **float**.</span></span>

## <a name="parameters"></a><span data-ttu-id="1fb5d-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="1fb5d-111">Parameters</span></span>



| <span data-ttu-id="1fb5d-112">Element</span><span class="sxs-lookup"><span data-stu-id="1fb5d-112">Item</span></span>                                                                                                                               | <span data-ttu-id="1fb5d-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1fb5d-113">Description</span></span>                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fb5d-114"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Objekt*</span><span class="sxs-lookup"><span data-stu-id="1fb5d-114"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Object*</span></span><br/>                                     | <span data-ttu-id="1fb5d-115">Ein beliebiger [Textur Objekttyp](dx-graphics-hlsl-to-type.md) mit Ausnahme eines **Puffer** Objekts.</span><span class="sxs-lookup"><span data-stu-id="1fb5d-115">Any [texture-object](dx-graphics-hlsl-to-type.md) type except a **Buffer** object.</span></span><br/>                                       |
| <span data-ttu-id="1fb5d-116"><span id="MipLevel"></span><span id="miplevel"></span><span id="MIPLEVEL"></span>*Miplevel*</span><span class="sxs-lookup"><span data-stu-id="1fb5d-116"><span id="MipLevel"></span><span id="miplevel"></span><span id="MIPLEVEL"></span>*MipLevel*</span></span><br/>                             | <span data-ttu-id="1fb5d-117">\[in \] einem NULL basierten Index, der die MipMap-Ebene identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1fb5d-117">\[in\] A zero-based index that identifies the mipmap level.</span></span> <span data-ttu-id="1fb5d-118">Wenn dieses Argument nicht verwendet wird, wird die erste MIP-Ebene angenommen.</span><span class="sxs-lookup"><span data-stu-id="1fb5d-118">If this argument is not used, the first mip level is assumed.</span></span><br/> |
| <span data-ttu-id="1fb5d-119"><span id="Width"></span><span id="width"></span><span id="WIDTH"></span>*Breite*</span><span class="sxs-lookup"><span data-stu-id="1fb5d-119"><span id="Width"></span><span id="width"></span><span id="WIDTH"></span>*Width*</span></span><br/>                                         | <span data-ttu-id="1fb5d-120">\[\]die Textur Breite in Texels.</span><span class="sxs-lookup"><span data-stu-id="1fb5d-120">\[out\] The texture width, in texels.</span></span><br/>                                                                                     |
| <span data-ttu-id="1fb5d-121"><span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>*Flugh*</span><span class="sxs-lookup"><span data-stu-id="1fb5d-121"><span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>*Height*</span></span><br/>                                     | <span data-ttu-id="1fb5d-122">\[\]die Textur Höhe in Texels.</span><span class="sxs-lookup"><span data-stu-id="1fb5d-122">\[out\] The texture height, in texels.</span></span><br/>                                                                                    |
| <span data-ttu-id="1fb5d-123"><span id="Elements"></span><span id="elements"></span><span id="ELEMENTS"></span>*Aspekte*</span><span class="sxs-lookup"><span data-stu-id="1fb5d-123"><span id="Elements"></span><span id="elements"></span><span id="ELEMENTS"></span>*Elements*</span></span><br/>                             | <span data-ttu-id="1fb5d-124">\[gibt \] die Anzahl von Elementen in einem Array zurück.</span><span class="sxs-lookup"><span data-stu-id="1fb5d-124">\[out\] The number of elements in an array.</span></span><br/>                                                                               |
| <span data-ttu-id="1fb5d-125"><span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>*Eingeh*</span><span class="sxs-lookup"><span data-stu-id="1fb5d-125"><span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>*Depth*</span></span><br/>                                         | <span data-ttu-id="1fb5d-126">\[\]die Textur Tiefe in Texels.</span><span class="sxs-lookup"><span data-stu-id="1fb5d-126">\[out\] The texture depth, in texels.</span></span><br/>                                                                                     |
| <span data-ttu-id="1fb5d-127"><span id="NumberOfLevels"></span><span id="numberoflevels"></span><span id="NUMBEROFLEVELS"></span>*Nummerige*</span><span class="sxs-lookup"><span data-stu-id="1fb5d-127"><span id="NumberOfLevels"></span><span id="numberoflevels"></span><span id="NUMBEROFLEVELS"></span>*NumberOfLevels*</span></span><br/>     | <span data-ttu-id="1fb5d-128">\[\]die Anzahl von MipMap-Ebenen.</span><span class="sxs-lookup"><span data-stu-id="1fb5d-128">\[out\] The number of mipmap levels.</span></span><br/>                                                                                      |
| <span data-ttu-id="1fb5d-129"><span id="NumberOfSamples"></span><span id="numberofsamples"></span><span id="NUMBEROFSAMPLES"></span>*Anzahl von Beispielen*</span><span class="sxs-lookup"><span data-stu-id="1fb5d-129"><span id="NumberOfSamples"></span><span id="numberofsamples"></span><span id="NUMBEROFSAMPLES"></span>*NumberOfSamples*</span></span><br/> | <span data-ttu-id="1fb5d-130">\[gibt \] die Anzahl der Stichproben an.</span><span class="sxs-lookup"><span data-stu-id="1fb5d-130">\[out\] The number of samples.</span></span><br/>                                                                                            |



 

## <a name="return-value"></a><span data-ttu-id="1fb5d-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1fb5d-131">Return Value</span></span>

<span data-ttu-id="1fb5d-132">Keiner</span><span class="sxs-lookup"><span data-stu-id="1fb5d-132">None</span></span>

## <a name="overloaded-methods"></a><span data-ttu-id="1fb5d-133">Überladene Methoden</span><span class="sxs-lookup"><span data-stu-id="1fb5d-133">Overloaded Methods</span></span>

<span data-ttu-id="1fb5d-134">Diese Tabelle listet alle unterschiedlichen Versionen der-Methode auf. Versionen unterscheiden sich je nach Anzahl der Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="1fb5d-134">This table lists all the different versions of the method; versions differs by the number of input parameters.</span></span> <span data-ttu-id="1fb5d-135">Beachten Sie, dass für jede Methode, die ganzzahlige Parameter annimmt, eine überladene Methode vorhanden ist, die Gleit Komma Parameter annimmt.</span><span class="sxs-lookup"><span data-stu-id="1fb5d-135">Notice that for every method that takes integer parameters, there is an overloaded method that takes floating-point parameters.</span></span>



| <span data-ttu-id="1fb5d-136">Texture-Object-Typ</span><span class="sxs-lookup"><span data-stu-id="1fb5d-136">Texture-Object Type</span></span> | <span data-ttu-id="1fb5d-137">Eingabeparameter</span><span class="sxs-lookup"><span data-stu-id="1fb5d-137">Input Parameters</span></span>                                                               |
|---------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="1fb5d-138">Texture1D</span><span class="sxs-lookup"><span data-stu-id="1fb5d-138">Texture1D</span></span>           | <span data-ttu-id="1fb5d-139">Uint miplevel, uint Width, uint nummerioflevels</span><span class="sxs-lookup"><span data-stu-id="1fb5d-139">UINT MipLevel, UINT Width, UINT NumberOfLevels</span></span>                                 |
| <span data-ttu-id="1fb5d-140">Texture1D</span><span class="sxs-lookup"><span data-stu-id="1fb5d-140">Texture1D</span></span>           | <span data-ttu-id="1fb5d-141">Uint-Breite</span><span class="sxs-lookup"><span data-stu-id="1fb5d-141">UINT Width</span></span>                                                                     |
| <span data-ttu-id="1fb5d-142">Texture1D</span><span class="sxs-lookup"><span data-stu-id="1fb5d-142">Texture1D</span></span>           | <span data-ttu-id="1fb5d-143">Uint-miplevel, float-Breite, float-Anzahlungs Zeichen</span><span class="sxs-lookup"><span data-stu-id="1fb5d-143">UINT MipLevel, float Width, float NumberOfLevels</span></span>                               |
| <span data-ttu-id="1fb5d-144">Texture1D</span><span class="sxs-lookup"><span data-stu-id="1fb5d-144">Texture1D</span></span>           | <span data-ttu-id="1fb5d-145">Gleit Komma Breite</span><span class="sxs-lookup"><span data-stu-id="1fb5d-145">float Width</span></span>                                                                    |
| <span data-ttu-id="1fb5d-146">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="1fb5d-146">Texture1DArray</span></span>      | <span data-ttu-id="1fb5d-147">Uint miplevel, uint Width, uint-Elemente, uint-Anzahlungs Elemente</span><span class="sxs-lookup"><span data-stu-id="1fb5d-147">UINT MipLevel, UINT Width, UINT Elements, UINT NumberOfLevels</span></span>                  |
| <span data-ttu-id="1fb5d-148">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="1fb5d-148">Texture1DArray</span></span>      | <span data-ttu-id="1fb5d-149">Uint-Breite, uint-Elemente</span><span class="sxs-lookup"><span data-stu-id="1fb5d-149">UINT Width, UINT Elements</span></span>                                                      |
| <span data-ttu-id="1fb5d-150">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="1fb5d-150">Texture1DArray</span></span>      | <span data-ttu-id="1fb5d-151">Uint miplevel, float width, float-Elemente, float-Anzahlungs Zeichen</span><span class="sxs-lookup"><span data-stu-id="1fb5d-151">UINT MipLevel, float Width, float Elements, float NumberOfLevels</span></span>               |
| <span data-ttu-id="1fb5d-152">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="1fb5d-152">Texture1DArray</span></span>      | <span data-ttu-id="1fb5d-153">float-Breite, float-Elemente</span><span class="sxs-lookup"><span data-stu-id="1fb5d-153">float Width, float Elements</span></span>                                                    |
| <span data-ttu-id="1fb5d-154">Texture2D</span><span class="sxs-lookup"><span data-stu-id="1fb5d-154">Texture2D</span></span>           | <span data-ttu-id="1fb5d-155">Uint miplevel, uint Width, uint Height, uint nummerioflevels</span><span class="sxs-lookup"><span data-stu-id="1fb5d-155">UINT MipLevel, UINT Width, UINT Height, UINT NumberOfLevels</span></span>                    |
| <span data-ttu-id="1fb5d-156">Texture2D</span><span class="sxs-lookup"><span data-stu-id="1fb5d-156">Texture2D</span></span>           | <span data-ttu-id="1fb5d-157">Uint-Breite, uint-Höhe</span><span class="sxs-lookup"><span data-stu-id="1fb5d-157">UINT Width, UINT Height</span></span>                                                        |
| <span data-ttu-id="1fb5d-158">Texture2D</span><span class="sxs-lookup"><span data-stu-id="1fb5d-158">Texture2D</span></span>           | <span data-ttu-id="1fb5d-159">Uint-miplevel, float-Breite, float-Höhe, float-Anzahlungs Zeichen</span><span class="sxs-lookup"><span data-stu-id="1fb5d-159">UINT MipLevel, float Width, float Height, float NumberOfLevels</span></span>                 |
| <span data-ttu-id="1fb5d-160">Texture2D</span><span class="sxs-lookup"><span data-stu-id="1fb5d-160">Texture2D</span></span>           | <span data-ttu-id="1fb5d-161">float-Breite, float-Höhe</span><span class="sxs-lookup"><span data-stu-id="1fb5d-161">float Width, float Height</span></span>                                                      |
| <span data-ttu-id="1fb5d-162">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="1fb5d-162">Texture2DArray</span></span>      | <span data-ttu-id="1fb5d-163">Uint miplevel, uint Width, uint Height, uint-Elemente, uint-nummerioflevels</span><span class="sxs-lookup"><span data-stu-id="1fb5d-163">UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels</span></span>     |
| <span data-ttu-id="1fb5d-164">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="1fb5d-164">Texture2DArray</span></span>      | <span data-ttu-id="1fb5d-165">Uint-Breite, uint-Höhe, uint-Elemente</span><span class="sxs-lookup"><span data-stu-id="1fb5d-165">UINT Width, UINT Height, UINT Elements</span></span>                                         |
| <span data-ttu-id="1fb5d-166">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="1fb5d-166">Texture2DArray</span></span>      | <span data-ttu-id="1fb5d-167">Uint-miplevel, float-Breite, float-Höhe, float-Elemente, float-anzahloflecken</span><span class="sxs-lookup"><span data-stu-id="1fb5d-167">UINT MipLevel, float Width, float Height, float Elements, float NumberOfLevels</span></span> |
| <span data-ttu-id="1fb5d-168">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="1fb5d-168">Texture2DArray</span></span>      | <span data-ttu-id="1fb5d-169">float-Breite, float-Höhe, float-Elemente</span><span class="sxs-lookup"><span data-stu-id="1fb5d-169">float Width, float Height, float Elements</span></span>                                      |
| <span data-ttu-id="1fb5d-170">Texture3D</span><span class="sxs-lookup"><span data-stu-id="1fb5d-170">Texture3D</span></span>           | <span data-ttu-id="1fb5d-171">Uint miplevel, uint Width, uint Height, uint-Tiefe, uint-nummerioflevels</span><span class="sxs-lookup"><span data-stu-id="1fb5d-171">UINT MipLevel, UINT Width, UINT Height, UINT Depth, UINT NumberOfLevels</span></span>        |
| <span data-ttu-id="1fb5d-172">Texture3D</span><span class="sxs-lookup"><span data-stu-id="1fb5d-172">Texture3D</span></span>           | <span data-ttu-id="1fb5d-173">Uint-Breite, uint-Höhe, uint-Tiefe</span><span class="sxs-lookup"><span data-stu-id="1fb5d-173">UINT Width, UINT Height, UINT Depth</span></span>                                            |
| <span data-ttu-id="1fb5d-174">Texture3D</span><span class="sxs-lookup"><span data-stu-id="1fb5d-174">Texture3D</span></span>           | <span data-ttu-id="1fb5d-175">Uint miplevel, float width, float height, float-Tiefe, float-Anzahlungs Zeichen</span><span class="sxs-lookup"><span data-stu-id="1fb5d-175">UINT MipLevel, float Width, float Height, float Depth, float NumberOfLevels</span></span>    |
| <span data-ttu-id="1fb5d-176">Texture3D</span><span class="sxs-lookup"><span data-stu-id="1fb5d-176">Texture3D</span></span>           | <span data-ttu-id="1fb5d-177">float-Breite, float-Höhe, Gleit Komma Tiefe</span><span class="sxs-lookup"><span data-stu-id="1fb5d-177">float Width, float Height, float Depth</span></span>                                         |
| <span data-ttu-id="1fb5d-178">TextureCube</span><span class="sxs-lookup"><span data-stu-id="1fb5d-178">TextureCube</span></span>         | <span data-ttu-id="1fb5d-179">Uint miplevel, uint Width, uint Height, uint nummerioflevels</span><span class="sxs-lookup"><span data-stu-id="1fb5d-179">UINT MipLevel, UINT Width, UINT Height, UINT NumberOfLevels</span></span>                    |
| <span data-ttu-id="1fb5d-180">TextureCube</span><span class="sxs-lookup"><span data-stu-id="1fb5d-180">TextureCube</span></span>         | <span data-ttu-id="1fb5d-181">Uint-Breite, uint-Höhe</span><span class="sxs-lookup"><span data-stu-id="1fb5d-181">UINT Width, UINT Height</span></span>                                                        |
| <span data-ttu-id="1fb5d-182">TextureCube</span><span class="sxs-lookup"><span data-stu-id="1fb5d-182">TextureCube</span></span>         | <span data-ttu-id="1fb5d-183">Uint-miplevel, float-Breite, float-Höhe, uint-Anzahlungs Zeichen</span><span class="sxs-lookup"><span data-stu-id="1fb5d-183">UINT MipLevel, float Width, float Height, UINT NumberOfLevels</span></span>                  |
| <span data-ttu-id="1fb5d-184">TextureCube</span><span class="sxs-lookup"><span data-stu-id="1fb5d-184">TextureCube</span></span>         | <span data-ttu-id="1fb5d-185">float-Breite, float-Höhe</span><span class="sxs-lookup"><span data-stu-id="1fb5d-185">float Width, float Height</span></span>                                                      |
| <span data-ttu-id="1fb5d-186">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="1fb5d-186">TextureCubeArray</span></span>    | <span data-ttu-id="1fb5d-187">Uint miplevel, uint Width, uint Height, uint-Elemente, uint-nummerioflevels</span><span class="sxs-lookup"><span data-stu-id="1fb5d-187">UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels</span></span>     |
| <span data-ttu-id="1fb5d-188">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="1fb5d-188">TextureCubeArray</span></span>    | <span data-ttu-id="1fb5d-189">Uint-Breite, uint-Höhe, uint-Elemente</span><span class="sxs-lookup"><span data-stu-id="1fb5d-189">UINT Width, UINT Height, UINT Elements</span></span>                                         |
| <span data-ttu-id="1fb5d-190">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="1fb5d-190">TextureCubeArray</span></span>    | <span data-ttu-id="1fb5d-191">Uint-miplevel, float-Breite, float-Höhe, float-Elemente, float-anzahloflecken</span><span class="sxs-lookup"><span data-stu-id="1fb5d-191">UINT MipLevel, float Width, float Height, float Elements, float NumberOfLevels</span></span> |
| <span data-ttu-id="1fb5d-192">Texturecubearray</span><span class="sxs-lookup"><span data-stu-id="1fb5d-192">TextureCubeArray</span></span>    | <span data-ttu-id="1fb5d-193">float-Breite, float-Höhe, float-Elemente</span><span class="sxs-lookup"><span data-stu-id="1fb5d-193">float Width, float Height, float Elements</span></span>                                      |
| <span data-ttu-id="1fb5d-194">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="1fb5d-194">Texture2DMS</span></span>         | <span data-ttu-id="1fb5d-195">Uint-Breite, uint-Höhe, uint-Beispiele</span><span class="sxs-lookup"><span data-stu-id="1fb5d-195">UINT Width, UINT Height, UINT Samples</span></span>                                          |
| <span data-ttu-id="1fb5d-196">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="1fb5d-196">Texture2DMS</span></span>         | <span data-ttu-id="1fb5d-197">float-Breite, float-Höhe, float-Stichproben</span><span class="sxs-lookup"><span data-stu-id="1fb5d-197">float Width, float Height, float Samples</span></span>                                       |
| <span data-ttu-id="1fb5d-198">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="1fb5d-198">Texture2DMSArray</span></span>    | <span data-ttu-id="1fb5d-199">Uint Width, uint Height, uint-Elemente, uint-Beispiele</span><span class="sxs-lookup"><span data-stu-id="1fb5d-199">UINT Width, UINT Height, UINT Elements, UINT Samples</span></span>                           |
| <span data-ttu-id="1fb5d-200">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="1fb5d-200">Texture2DMSArray</span></span>    | <span data-ttu-id="1fb5d-201">float-Breite, float-Höhe, float-Elemente, float-Beispiele</span><span class="sxs-lookup"><span data-stu-id="1fb5d-201">float Width, float Height, float Elements, float Samples</span></span>                       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1fb5d-202">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="1fb5d-202">Minimum Shader Model</span></span>

<span data-ttu-id="1fb5d-203">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1fb5d-203">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1fb5d-204">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1fb5d-204">vs\_4\_0</span></span> | <span data-ttu-id="1fb5d-205">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="1fb5d-205">vs\_4\_1</span></span>  | <span data-ttu-id="1fb5d-206">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1fb5d-206">ps\_4\_0</span></span> | <span data-ttu-id="1fb5d-207">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="1fb5d-207">ps\_4\_1</span></span>  | <span data-ttu-id="1fb5d-208">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1fb5d-208">gs\_4\_0</span></span> | <span data-ttu-id="1fb5d-209">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="1fb5d-209">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
| <span data-ttu-id="1fb5d-210">x</span><span class="sxs-lookup"><span data-stu-id="1fb5d-210">x</span></span>        | <span data-ttu-id="1fb5d-211">x</span><span class="sxs-lookup"><span data-stu-id="1fb5d-211">x</span></span>         | <span data-ttu-id="1fb5d-212">x</span><span class="sxs-lookup"><span data-stu-id="1fb5d-212">x</span></span>        | <span data-ttu-id="1fb5d-213">x</span><span class="sxs-lookup"><span data-stu-id="1fb5d-213">x</span></span>         | <span data-ttu-id="1fb5d-214">x</span><span class="sxs-lookup"><span data-stu-id="1fb5d-214">x</span></span>        | <span data-ttu-id="1fb5d-215">x</span><span class="sxs-lookup"><span data-stu-id="1fb5d-215">x</span></span>         |



 

1.  <span data-ttu-id="1fb5d-216">Gibt Dimensionen für die größte (nullte) MipMap-Ebene zurück.</span><span class="sxs-lookup"><span data-stu-id="1fb5d-216">Returns dimensions for the largest (zeroth) mipmap level.</span></span>
2.  <span data-ttu-id="1fb5d-217">Texturecubearray ist im Shader-Modell 4,1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1fb5d-217">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
3.  <span data-ttu-id="1fb5d-218">Das Shader-Modell 4,1 ist in Direct3D 10,1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1fb5d-218">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1fb5d-219">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1fb5d-219">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fb5d-220">Texture-Objekt</span><span class="sxs-lookup"><span data-stu-id="1fb5d-220">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





