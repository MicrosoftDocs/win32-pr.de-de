---
description: 'D3DXGetPixelShaderProfile-Funktion: Gibt den Namen des höchsten HLSL-Profils (High-Level Shader Language) zurück, das von einem bestimmten Gerät unterstützt wird.'
ms.assetid: a6c1be4e-f6f5-4f08-b6a7-b9c621e5f19b
title: D3DXGetPixelShaderProfile-Funktion (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetPixelShaderProfile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7d24e19d49a8a96f91847892f519ef6c06d25ef5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114437"
---
# <a name="d3dxgetpixelshaderprofile-function"></a><span data-ttu-id="33054-103">D3DXGetPixelShaderProfile-Funktion</span><span class="sxs-lookup"><span data-stu-id="33054-103">D3DXGetPixelShaderProfile function</span></span>

<span data-ttu-id="33054-104">Gibt den Namen des höchsten HLSL-Profils (High-Level Shader Language) zurück, das von einem bestimmten Gerät unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="33054-104">Returns the name of the highest high-level shader language (HLSL) profile supported by a given device.</span></span>

## <a name="syntax"></a><span data-ttu-id="33054-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="33054-105">Syntax</span></span>


```C++
LPCSTR D3DXGetPixelShaderProfile(
  _In_ LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a><span data-ttu-id="33054-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="33054-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33054-107">*pDevice* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="33054-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33054-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="33054-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="33054-109">Zeiger auf das Gerät.</span><span class="sxs-lookup"><span data-stu-id="33054-109">Pointer to the device.</span></span> <span data-ttu-id="33054-110">Siehe [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="33054-110">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33054-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="33054-111">Return value</span></span>

<span data-ttu-id="33054-112">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="33054-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="33054-113">Der HLSL-Profilname.</span><span class="sxs-lookup"><span data-stu-id="33054-113">The HLSL profile name.</span></span>

<span data-ttu-id="33054-114">Wenn das Gerät keine Pixelshader unterstützt, gibt die Funktion **NULL** zurück.</span><span class="sxs-lookup"><span data-stu-id="33054-114">If the device does not support pixel shaders then the function returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="33054-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="33054-115">Remarks</span></span>

<span data-ttu-id="33054-116">Ein Shaderprofil gibt die zu verwendende Assembly-Shaderversion und die Funktionen an, die dem HLSL-Compiler beim Kompilieren eines Shaders zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="33054-116">A shader profile specifies the assembly shader version to use and the capabilities available to the HLSL compiler when compiling a shader.</span></span> <span data-ttu-id="33054-117">In der folgenden Tabelle sind die unterstützten Pixel-Shaderprofile aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="33054-117">The following table lists the pixel shader profiles that are supported.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="33054-118">Shaderprofil</span><span class="sxs-lookup"><span data-stu-id="33054-118">Shader Profile</span></span></th>
<th><span data-ttu-id="33054-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="33054-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33054-120">ps_1_1</span><span class="sxs-lookup"><span data-stu-id="33054-120">ps_1_1</span></span></td>
<td><span data-ttu-id="33054-121">Kompilieren Sie in ps_1_1 Version.</span><span class="sxs-lookup"><span data-stu-id="33054-121">Compile to ps_1_1 version.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33054-122">ps_1_2</span><span class="sxs-lookup"><span data-stu-id="33054-122">ps_1_2</span></span></td>
<td><span data-ttu-id="33054-123">Kompilieren Sie in ps_1_2 Version.</span><span class="sxs-lookup"><span data-stu-id="33054-123">Compile to ps_1_2 version.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33054-124">ps_1_3</span><span class="sxs-lookup"><span data-stu-id="33054-124">ps_1_3</span></span></td>
<td><span data-ttu-id="33054-125">Kompilieren Sie in ps_1_3 Version.</span><span class="sxs-lookup"><span data-stu-id="33054-125">Compile to ps_1_3 version.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33054-126">ps_1_4</span><span class="sxs-lookup"><span data-stu-id="33054-126">ps_1_4</span></span></td>
<td><span data-ttu-id="33054-127">Kompilieren Sie in ps_1_4 Version.</span><span class="sxs-lookup"><span data-stu-id="33054-127">Compile to ps_1_4 version.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33054-128">ps_2_0</span><span class="sxs-lookup"><span data-stu-id="33054-128">ps_2_0</span></span></td>
<td><span data-ttu-id="33054-129">Kompilieren Sie in ps_2_0 Version.</span><span class="sxs-lookup"><span data-stu-id="33054-129">Compile to ps_2_0 version.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33054-130">ps_2_a</span><span class="sxs-lookup"><span data-stu-id="33054-130">ps_2_a</span></span></td>
<td><span data-ttu-id="33054-131">Entspricht dem ps_2_0 Profil mit den folgenden zusätzlichen Funktionen, die der Compiler als Ziel hat:</span><span class="sxs-lookup"><span data-stu-id="33054-131">Same as the ps_2_0 profile, with the following additional capabilities available for the compiler to target:</span></span>
<ul>
<li><span data-ttu-id="33054-132">Die Anzahl temporärer Register (r#) ist größer oder gleich 22.</span><span class="sxs-lookup"><span data-stu-id="33054-132">Number of Temporary Registers (r#) is greater than or equal to 22.</span></span></li>
<li><span data-ttu-id="33054-133">Beliebige Quellwizzle.</span><span class="sxs-lookup"><span data-stu-id="33054-133">Arbitrary source swizzle.</span></span></li>
<li><span data-ttu-id="33054-134">Farbverlaufsanweisungen: dsx, dsy.</span><span class="sxs-lookup"><span data-stu-id="33054-134">Gradient instructions: dsx, dsy.</span></span></li>
<li><span data-ttu-id="33054-135">Prädikation:</span><span class="sxs-lookup"><span data-stu-id="33054-135">Predication.</span></span></li>
<li><span data-ttu-id="33054-136">Kein Leselimit für abhängige Textur.</span><span class="sxs-lookup"><span data-stu-id="33054-136">No dependent texture read limit.</span></span></li>
<li><span data-ttu-id="33054-137">Keine Beschränkung für die Anzahl der Texturanweisungen.</span><span class="sxs-lookup"><span data-stu-id="33054-137">No limit for the number of texture instructions.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33054-138">ps_2_b</span><span class="sxs-lookup"><span data-stu-id="33054-138">ps_2_b</span></span></td>
<td><span data-ttu-id="33054-139">Entspricht dem ps_2_0 Profil mit den folgenden zusätzlichen Funktionen, die der Compiler als Ziel hat:</span><span class="sxs-lookup"><span data-stu-id="33054-139">Same as the ps_2_0 profile, with the following additional capabilities available for the compiler to target:</span></span>
<ul>
<li><span data-ttu-id="33054-140">Die Anzahl temporärer Register (r#) ist größer oder gleich 32.</span><span class="sxs-lookup"><span data-stu-id="33054-140">Number of Temporary Registers (r#) is greater than or equal to 32.</span></span></li>
<li><span data-ttu-id="33054-141">Keine Beschränkung für die Anzahl der Texturanweisungen.</span><span class="sxs-lookup"><span data-stu-id="33054-141">No limit for the number of texture instructions.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33054-142">ps_3_0</span><span class="sxs-lookup"><span data-stu-id="33054-142">ps_3_0</span></span></td>
<td><span data-ttu-id="33054-143">Kompilieren Sie in ps_3_0 Version.</span><span class="sxs-lookup"><span data-stu-id="33054-143">Compile to ps_3_0 version.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="33054-144">Weitere Informationen zu den Unterschieden zwischen Shaderversionen finden Sie unter [Pixelshader-Unterschiede.](../direct3dhlsl/dx9-graphics-reference-asm-ps-differences.md)</span><span class="sxs-lookup"><span data-stu-id="33054-144">For more information about the differences between shader versions, see [Pixel Shader Differences](../direct3dhlsl/dx9-graphics-reference-asm-ps-differences.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="33054-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33054-145">Requirements</span></span>



| <span data-ttu-id="33054-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33054-146">Requirement</span></span> | <span data-ttu-id="33054-147">Wert</span><span class="sxs-lookup"><span data-stu-id="33054-147">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="33054-148">Header</span><span class="sxs-lookup"><span data-stu-id="33054-148">Header</span></span><br/>  | <dl> <span data-ttu-id="33054-149"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="33054-149"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="33054-150">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="33054-150">Library</span></span><br/> | <dl> <span data-ttu-id="33054-151"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="33054-151"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="33054-152">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="33054-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33054-153">Shaderfunktionen</span><span class="sxs-lookup"><span data-stu-id="33054-153">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
