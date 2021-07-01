---
title: GetDimensions (DirectX HLSL-Texturobjekt)
description: Ruft Texturgrößeninformationen ab. Der Syntaxblock zeigt alle Parameter an, die in der Methodendeklaration möglich sind. Die Tabelle im Abschnitt "Hinweise" zeigt, welche Parameter für jeden Texturobjekttyp implementiert werden.
ms.assetid: b72e54da-382a-4b90-bbfe-0b32effc7c05
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bb6ef3c35af60ea776622718099acdedb5188ba8
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119836"
---
# <a name="getdimensions-directx-hlsl-texture-object"></a><span data-ttu-id="636e3-105">GetDimensions (DirectX HLSL-Texturobjekt)</span><span class="sxs-lookup"><span data-stu-id="636e3-105">GetDimensions (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="636e3-106">Ruft Texturgrößeninformationen ab.</span><span class="sxs-lookup"><span data-stu-id="636e3-106">Gets texture size information.</span></span> <span data-ttu-id="636e3-107">Der Syntaxblock zeigt alle Parameter an, die in der Methodendeklaration möglich sind.</span><span class="sxs-lookup"><span data-stu-id="636e3-107">The syntax block shows all the parameters that are possible in the method declaration.</span></span> <span data-ttu-id="636e3-108">Die Tabelle im Abschnitt "Hinweise" zeigt, welche Parameter für jeden Texturobjekttyp implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="636e3-108">The table in the Remarks section shows which parameters are implemented for each texture-object type.</span></span>

<span data-ttu-id="636e3-109">void Object.GetDimensions( UINT MipLevel, typeX Width, typeX Height, typeX Elements, typeX Depth, typeX NumberOfLevels, typeX NumberOfSamples );</span><span class="sxs-lookup"><span data-stu-id="636e3-109">void Object.GetDimensions( UINT MipLevel, typeX Width, typeX Height, typeX Elements, typeX Depth, typeX NumberOfLevels, typeX NumberOfSamples );</span></span>



 

<span data-ttu-id="636e3-110">typeX gibt an, dass es zwei mögliche Typen gibt: **uint** oder **float**.</span><span class="sxs-lookup"><span data-stu-id="636e3-110">typeX denotes that there are two possible types: **uint** or **float**.</span></span>

## <a name="parameters"></a><span data-ttu-id="636e3-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="636e3-111">Parameters</span></span>



| <span data-ttu-id="636e3-112">Element</span><span class="sxs-lookup"><span data-stu-id="636e3-112">Item</span></span>                                                                                                                               | <span data-ttu-id="636e3-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="636e3-113">Description</span></span>                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="636e3-114"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Objekt*</span><span class="sxs-lookup"><span data-stu-id="636e3-114"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Object*</span></span><br/>                                     | <span data-ttu-id="636e3-115">Beliebiger [Texturobjekttyp](dx-graphics-hlsl-to-type.md) mit Ausnahme eines **Buffer-Objekts.**</span><span class="sxs-lookup"><span data-stu-id="636e3-115">Any [texture-object](dx-graphics-hlsl-to-type.md) type except a **Buffer** object.</span></span><br/>                                       |
| <span data-ttu-id="636e3-116"><span id="MipLevel"></span><span id="miplevel"></span><span id="MIPLEVEL"></span>*MipLevel*</span><span class="sxs-lookup"><span data-stu-id="636e3-116"><span id="MipLevel"></span><span id="miplevel"></span><span id="MIPLEVEL"></span>*MipLevel*</span></span><br/>                             | <span data-ttu-id="636e3-117">\[in \] Ein nullbasierter Index, der die Mipmapebene identifiziert.</span><span class="sxs-lookup"><span data-stu-id="636e3-117">\[in\] A zero-based index that identifies the mipmap level.</span></span> <span data-ttu-id="636e3-118">Wenn dieses Argument nicht verwendet wird, wird die erste MIP-Ebene angenommen.</span><span class="sxs-lookup"><span data-stu-id="636e3-118">If this argument is not used, the first mip level is assumed.</span></span><br/> |
| <span data-ttu-id="636e3-119"><span id="Width"></span><span id="width"></span><span id="WIDTH"></span>*Breite*</span><span class="sxs-lookup"><span data-stu-id="636e3-119"><span id="Width"></span><span id="width"></span><span id="WIDTH"></span>*Width*</span></span><br/>                                         | <span data-ttu-id="636e3-120">\[out \] Die Texturbreite in Texeln.</span><span class="sxs-lookup"><span data-stu-id="636e3-120">\[out\] The texture width, in texels.</span></span><br/>                                                                                     |
| <span data-ttu-id="636e3-121"><span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>*Höhe*</span><span class="sxs-lookup"><span data-stu-id="636e3-121"><span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>*Height*</span></span><br/>                                     | <span data-ttu-id="636e3-122">\[out \] Die Texturhöhe in Texeln.</span><span class="sxs-lookup"><span data-stu-id="636e3-122">\[out\] The texture height, in texels.</span></span><br/>                                                                                    |
| <span data-ttu-id="636e3-123"><span id="Elements"></span><span id="elements"></span><span id="ELEMENTS"></span>*Elemente*</span><span class="sxs-lookup"><span data-stu-id="636e3-123"><span id="Elements"></span><span id="elements"></span><span id="ELEMENTS"></span>*Elements*</span></span><br/>                             | <span data-ttu-id="636e3-124">\[out \] Die Anzahl der Elemente in einem Array.</span><span class="sxs-lookup"><span data-stu-id="636e3-124">\[out\] The number of elements in an array.</span></span><br/>                                                                               |
| <span data-ttu-id="636e3-125"><span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>*Tiefe*</span><span class="sxs-lookup"><span data-stu-id="636e3-125"><span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>*Depth*</span></span><br/>                                         | <span data-ttu-id="636e3-126">\[out \] Die Texturtiefe in Texeln.</span><span class="sxs-lookup"><span data-stu-id="636e3-126">\[out\] The texture depth, in texels.</span></span><br/>                                                                                     |
| <span data-ttu-id="636e3-127"><span id="NumberOfLevels"></span><span id="numberoflevels"></span><span id="NUMBEROFLEVELS"></span>*NumberOfLevels*</span><span class="sxs-lookup"><span data-stu-id="636e3-127"><span id="NumberOfLevels"></span><span id="numberoflevels"></span><span id="NUMBEROFLEVELS"></span>*NumberOfLevels*</span></span><br/>     | <span data-ttu-id="636e3-128">\[out \] Die Anzahl der Mipmap-Ebenen.</span><span class="sxs-lookup"><span data-stu-id="636e3-128">\[out\] The number of mipmap levels.</span></span><br/>                                                                                      |
| <span data-ttu-id="636e3-129"><span id="NumberOfSamples"></span><span id="numberofsamples"></span><span id="NUMBEROFSAMPLES"></span>*NumberOfSamples*</span><span class="sxs-lookup"><span data-stu-id="636e3-129"><span id="NumberOfSamples"></span><span id="numberofsamples"></span><span id="NUMBEROFSAMPLES"></span>*NumberOfSamples*</span></span><br/> | <span data-ttu-id="636e3-130">\[out \] Die Anzahl der Beispiele.</span><span class="sxs-lookup"><span data-stu-id="636e3-130">\[out\] The number of samples.</span></span><br/>                                                                                            |



 

## <a name="return-value"></a><span data-ttu-id="636e3-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="636e3-131">Return Value</span></span>

<span data-ttu-id="636e3-132">Keiner</span><span class="sxs-lookup"><span data-stu-id="636e3-132">None</span></span>

## <a name="overloaded-methods"></a><span data-ttu-id="636e3-133">Überladene Methoden</span><span class="sxs-lookup"><span data-stu-id="636e3-133">Overloaded Methods</span></span>

<span data-ttu-id="636e3-134">In dieser Tabelle werden alle verschiedenen Versionen der -Methode aufgeführt. -Versionen unterscheiden sich durch die Anzahl der Eingabeparameter.</span><span class="sxs-lookup"><span data-stu-id="636e3-134">This table lists all the different versions of the method; versions differs by the number of input parameters.</span></span> <span data-ttu-id="636e3-135">Beachten Sie, dass es für jede Methode, die ganzzahlige Parameter angibt, eine überladene Methode gibt, die Gleitkommaparameter verwendet.</span><span class="sxs-lookup"><span data-stu-id="636e3-135">Notice that for every method that takes integer parameters, there is an overloaded method that takes floating-point parameters.</span></span>



| <span data-ttu-id="636e3-136">Texture-Object Typ</span><span class="sxs-lookup"><span data-stu-id="636e3-136">Texture-Object Type</span></span> | <span data-ttu-id="636e3-137">Eingabeparameter</span><span class="sxs-lookup"><span data-stu-id="636e3-137">Input Parameters</span></span>                                                               |
|---------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="636e3-138">Texture1D</span><span class="sxs-lookup"><span data-stu-id="636e3-138">Texture1D</span></span>           | <span data-ttu-id="636e3-139">UINT MipLevel, UINT Width, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="636e3-139">UINT MipLevel, UINT Width, UINT NumberOfLevels</span></span>                                 |
| <span data-ttu-id="636e3-140">Texture1D</span><span class="sxs-lookup"><span data-stu-id="636e3-140">Texture1D</span></span>           | <span data-ttu-id="636e3-141">UINT-Breite</span><span class="sxs-lookup"><span data-stu-id="636e3-141">UINT Width</span></span>                                                                     |
| <span data-ttu-id="636e3-142">Texture1D</span><span class="sxs-lookup"><span data-stu-id="636e3-142">Texture1D</span></span>           | <span data-ttu-id="636e3-143">UINT MipLevel, float Width, float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="636e3-143">UINT MipLevel, float Width, float NumberOfLevels</span></span>                               |
| <span data-ttu-id="636e3-144">Texture1D</span><span class="sxs-lookup"><span data-stu-id="636e3-144">Texture1D</span></span>           | <span data-ttu-id="636e3-145">float Width</span><span class="sxs-lookup"><span data-stu-id="636e3-145">float Width</span></span>                                                                    |
| <span data-ttu-id="636e3-146">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="636e3-146">Texture1DArray</span></span>      | <span data-ttu-id="636e3-147">UINT MipLevel, UINT Width, UINT Elements, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="636e3-147">UINT MipLevel, UINT Width, UINT Elements, UINT NumberOfLevels</span></span>                  |
| <span data-ttu-id="636e3-148">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="636e3-148">Texture1DArray</span></span>      | <span data-ttu-id="636e3-149">UINT-Breite, UINT-Elemente</span><span class="sxs-lookup"><span data-stu-id="636e3-149">UINT Width, UINT Elements</span></span>                                                      |
| <span data-ttu-id="636e3-150">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="636e3-150">Texture1DArray</span></span>      | <span data-ttu-id="636e3-151">UINT MipLevel, float Width, float Elements, float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="636e3-151">UINT MipLevel, float Width, float Elements, float NumberOfLevels</span></span>               |
| <span data-ttu-id="636e3-152">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="636e3-152">Texture1DArray</span></span>      | <span data-ttu-id="636e3-153">float Width, float Elements</span><span class="sxs-lookup"><span data-stu-id="636e3-153">float Width, float Elements</span></span>                                                    |
| <span data-ttu-id="636e3-154">Texture2D</span><span class="sxs-lookup"><span data-stu-id="636e3-154">Texture2D</span></span>           | <span data-ttu-id="636e3-155">UINT MipLevel, UINT Width, UINT Height, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="636e3-155">UINT MipLevel, UINT Width, UINT Height, UINT NumberOfLevels</span></span>                    |
| <span data-ttu-id="636e3-156">Texture2D</span><span class="sxs-lookup"><span data-stu-id="636e3-156">Texture2D</span></span>           | <span data-ttu-id="636e3-157">UINT-Breite, UINT-Höhe</span><span class="sxs-lookup"><span data-stu-id="636e3-157">UINT Width, UINT Height</span></span>                                                        |
| <span data-ttu-id="636e3-158">Texture2D</span><span class="sxs-lookup"><span data-stu-id="636e3-158">Texture2D</span></span>           | <span data-ttu-id="636e3-159">UINT MipLevel, float Width, float Height, float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="636e3-159">UINT MipLevel, float Width, float Height, float NumberOfLevels</span></span>                 |
| <span data-ttu-id="636e3-160">Texture2D</span><span class="sxs-lookup"><span data-stu-id="636e3-160">Texture2D</span></span>           | <span data-ttu-id="636e3-161">float Width, float Height</span><span class="sxs-lookup"><span data-stu-id="636e3-161">float Width, float Height</span></span>                                                      |
| <span data-ttu-id="636e3-162">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="636e3-162">Texture2DArray</span></span>      | <span data-ttu-id="636e3-163">UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="636e3-163">UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels</span></span>     |
| <span data-ttu-id="636e3-164">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="636e3-164">Texture2DArray</span></span>      | <span data-ttu-id="636e3-165">UINT-Breite, UINT-Höhe, UINT-Elemente</span><span class="sxs-lookup"><span data-stu-id="636e3-165">UINT Width, UINT Height, UINT Elements</span></span>                                         |
| <span data-ttu-id="636e3-166">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="636e3-166">Texture2DArray</span></span>      | <span data-ttu-id="636e3-167">UINT MipLevel, float Width, float Height, float Elements, float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="636e3-167">UINT MipLevel, float Width, float Height, float Elements, float NumberOfLevels</span></span> |
| <span data-ttu-id="636e3-168">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="636e3-168">Texture2DArray</span></span>      | <span data-ttu-id="636e3-169">float Width, float Height, float Elements</span><span class="sxs-lookup"><span data-stu-id="636e3-169">float Width, float Height, float Elements</span></span>                                      |
| <span data-ttu-id="636e3-170">Texture3D</span><span class="sxs-lookup"><span data-stu-id="636e3-170">Texture3D</span></span>           | <span data-ttu-id="636e3-171">UINT MipLevel, UINT Width, UINT Height, UINT Depth, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="636e3-171">UINT MipLevel, UINT Width, UINT Height, UINT Depth, UINT NumberOfLevels</span></span>        |
| <span data-ttu-id="636e3-172">Texture3D</span><span class="sxs-lookup"><span data-stu-id="636e3-172">Texture3D</span></span>           | <span data-ttu-id="636e3-173">UINT-Breite, UINT-Höhe, UINT-Tiefe</span><span class="sxs-lookup"><span data-stu-id="636e3-173">UINT Width, UINT Height, UINT Depth</span></span>                                            |
| <span data-ttu-id="636e3-174">Texture3D</span><span class="sxs-lookup"><span data-stu-id="636e3-174">Texture3D</span></span>           | <span data-ttu-id="636e3-175">UINT MipLevel, float Width, float Height, float Depth, float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="636e3-175">UINT MipLevel, float Width, float Height, float Depth, float NumberOfLevels</span></span>    |
| <span data-ttu-id="636e3-176">Texture3D</span><span class="sxs-lookup"><span data-stu-id="636e3-176">Texture3D</span></span>           | <span data-ttu-id="636e3-177">float Width, float Height, float Depth</span><span class="sxs-lookup"><span data-stu-id="636e3-177">float Width, float Height, float Depth</span></span>                                         |
| <span data-ttu-id="636e3-178">TextureCube</span><span class="sxs-lookup"><span data-stu-id="636e3-178">TextureCube</span></span>         | <span data-ttu-id="636e3-179">UINT MipLevel, UINT Width, UINT Height, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="636e3-179">UINT MipLevel, UINT Width, UINT Height, UINT NumberOfLevels</span></span>                    |
| <span data-ttu-id="636e3-180">TextureCube</span><span class="sxs-lookup"><span data-stu-id="636e3-180">TextureCube</span></span>         | <span data-ttu-id="636e3-181">UINT-Breite, UINT-Höhe</span><span class="sxs-lookup"><span data-stu-id="636e3-181">UINT Width, UINT Height</span></span>                                                        |
| <span data-ttu-id="636e3-182">TextureCube</span><span class="sxs-lookup"><span data-stu-id="636e3-182">TextureCube</span></span>         | <span data-ttu-id="636e3-183">UINT MipLevel, float Width, float Height, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="636e3-183">UINT MipLevel, float Width, float Height, UINT NumberOfLevels</span></span>                  |
| <span data-ttu-id="636e3-184">TextureCube</span><span class="sxs-lookup"><span data-stu-id="636e3-184">TextureCube</span></span>         | <span data-ttu-id="636e3-185">float Width, float Height</span><span class="sxs-lookup"><span data-stu-id="636e3-185">float Width, float Height</span></span>                                                      |
| <span data-ttu-id="636e3-186">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="636e3-186">TextureCubeArray</span></span>    | <span data-ttu-id="636e3-187">UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="636e3-187">UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels</span></span>     |
| <span data-ttu-id="636e3-188">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="636e3-188">TextureCubeArray</span></span>    | <span data-ttu-id="636e3-189">UINT-Breite, UINT-Höhe, UINT-Elemente</span><span class="sxs-lookup"><span data-stu-id="636e3-189">UINT Width, UINT Height, UINT Elements</span></span>                                         |
| <span data-ttu-id="636e3-190">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="636e3-190">TextureCubeArray</span></span>    | <span data-ttu-id="636e3-191">UINT MipLevel, float Width, float Height, float Elements, float NumberOfLevels</span><span class="sxs-lookup"><span data-stu-id="636e3-191">UINT MipLevel, float Width, float Height, float Elements, float NumberOfLevels</span></span> |
| <span data-ttu-id="636e3-192">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="636e3-192">TextureCubeArray</span></span>    | <span data-ttu-id="636e3-193">float Width, float Height, float Elements</span><span class="sxs-lookup"><span data-stu-id="636e3-193">float Width, float Height, float Elements</span></span>                                      |
| <span data-ttu-id="636e3-194">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="636e3-194">Texture2DMS</span></span>         | <span data-ttu-id="636e3-195">UINT-Breite, UINT-Höhe, UINT-Beispiele</span><span class="sxs-lookup"><span data-stu-id="636e3-195">UINT Width, UINT Height, UINT Samples</span></span>                                          |
| <span data-ttu-id="636e3-196">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="636e3-196">Texture2DMS</span></span>         | <span data-ttu-id="636e3-197">float Width, float Height, float Samples</span><span class="sxs-lookup"><span data-stu-id="636e3-197">float Width, float Height, float Samples</span></span>                                       |
| <span data-ttu-id="636e3-198">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="636e3-198">Texture2DMSArray</span></span>    | <span data-ttu-id="636e3-199">UINT-Breite, UINT-Höhe, UINT-Elemente, UINT-Beispiele</span><span class="sxs-lookup"><span data-stu-id="636e3-199">UINT Width, UINT Height, UINT Elements, UINT Samples</span></span>                           |
| <span data-ttu-id="636e3-200">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="636e3-200">Texture2DMSArray</span></span>    | <span data-ttu-id="636e3-201">float Width, float Height, float Elements, float Samples</span><span class="sxs-lookup"><span data-stu-id="636e3-201">float Width, float Height, float Elements, float Samples</span></span>                       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="636e3-202">Shader-Mindestmodell</span><span class="sxs-lookup"><span data-stu-id="636e3-202">Minimum Shader Model</span></span>

<span data-ttu-id="636e3-203">Diese Funktion wird in den folgenden Shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="636e3-203">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="636e3-204">Vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="636e3-204">vs\_4\_0</span></span> | <span data-ttu-id="636e3-205">Vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="636e3-205">vs\_4\_1</span></span>  | <span data-ttu-id="636e3-206">ps \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="636e3-206">ps\_4\_0</span></span> | <span data-ttu-id="636e3-207">ps \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="636e3-207">ps\_4\_1</span></span>  | <span data-ttu-id="636e3-208">gs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="636e3-208">gs\_4\_0</span></span> | <span data-ttu-id="636e3-209">gs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="636e3-209">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
| <span data-ttu-id="636e3-210">x</span><span class="sxs-lookup"><span data-stu-id="636e3-210">x</span></span>        | <span data-ttu-id="636e3-211">x</span><span class="sxs-lookup"><span data-stu-id="636e3-211">x</span></span>         | <span data-ttu-id="636e3-212">x</span><span class="sxs-lookup"><span data-stu-id="636e3-212">x</span></span>        | <span data-ttu-id="636e3-213">x</span><span class="sxs-lookup"><span data-stu-id="636e3-213">x</span></span>         | <span data-ttu-id="636e3-214">x</span><span class="sxs-lookup"><span data-stu-id="636e3-214">x</span></span>        | <span data-ttu-id="636e3-215">x</span><span class="sxs-lookup"><span data-stu-id="636e3-215">x</span></span>         |



 

1.  <span data-ttu-id="636e3-216">Gibt Dimensionen für die größte (nullth) mipmap-Ebene zurück.</span><span class="sxs-lookup"><span data-stu-id="636e3-216">Returns dimensions for the largest (zeroth) mipmap level.</span></span>
2.  <span data-ttu-id="636e3-217">TextureCubeArray ist im Shadermodell 4.1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="636e3-217">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
3.  <span data-ttu-id="636e3-218">Shadermodell 4.1 ist in Direct3D 10.1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="636e3-218">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="related-topics"></a><span data-ttu-id="636e3-219">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="636e3-219">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="636e3-220">Texturobjekt</span><span class="sxs-lookup"><span data-stu-id="636e3-220">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





