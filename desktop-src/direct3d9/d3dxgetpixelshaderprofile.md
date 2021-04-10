---
description: Gibt den Namen des höchsten HLSL-Profils (High-Level Shader Language) zurück, das von einem bestimmten Gerät unterstützt wird.
ms.assetid: a6c1be4e-f6f5-4f08-b6a7-b9c621e5f19b
title: D3DXGetPixelShaderProfile-Funktion (D3DX9Shader. h)
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
ms.openlocfilehash: ad1f430a95b1ff2173dceb1e0561dccf3d0ee88d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961600"
---
# <a name="d3dxgetpixelshaderprofile-function"></a><span data-ttu-id="1e412-103">D3DXGetPixelShaderProfile-Funktion</span><span class="sxs-lookup"><span data-stu-id="1e412-103">D3DXGetPixelShaderProfile function</span></span>

<span data-ttu-id="1e412-104">Gibt den Namen des höchsten HLSL-Profils (High-Level Shader Language) zurück, das von einem bestimmten Gerät unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="1e412-104">Returns the name of the highest high-level shader language (HLSL) profile supported by a given device.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e412-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e412-105">Syntax</span></span>


```C++
LPCSTR D3DXGetPixelShaderProfile(
  _In_ LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a><span data-ttu-id="1e412-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e412-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e412-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1e412-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e412-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="1e412-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="1e412-109">Zeiger auf das Gerät.</span><span class="sxs-lookup"><span data-stu-id="1e412-109">Pointer to the device.</span></span> <span data-ttu-id="1e412-110">Siehe [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="1e412-110">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e412-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1e412-111">Return value</span></span>

<span data-ttu-id="1e412-112">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1e412-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1e412-113">Der HLSL-Profilname.</span><span class="sxs-lookup"><span data-stu-id="1e412-113">The HLSL profile name.</span></span>

<span data-ttu-id="1e412-114">Wenn das Gerät keine Pixel-Shader unterstützt, gibt die Funktion **null** zurück.</span><span class="sxs-lookup"><span data-stu-id="1e412-114">If the device does not support pixel shaders then the function returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e412-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1e412-115">Remarks</span></span>

<span data-ttu-id="1e412-116">Ein Shader-Profil gibt die zu verwendende Assembly-Shader-Version und die Funktionen an, die dem HLSL-Compiler beim Kompilieren eines Shaders zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="1e412-116">A shader profile specifies the assembly shader version to use and the capabilities available to the HLSL compiler when compiling a shader.</span></span> <span data-ttu-id="1e412-117">In der folgenden Tabelle sind die unterstützten Pixel-shaderprofile aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="1e412-117">The following table lists the pixel shader profiles that are supported.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1e412-118">Shader-Profil</span><span class="sxs-lookup"><span data-stu-id="1e412-118">Shader Profile</span></span></th>
<th><span data-ttu-id="1e412-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1e412-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1e412-120">ps_1_1</span><span class="sxs-lookup"><span data-stu-id="1e412-120">ps_1_1</span></span></td>
<td><span data-ttu-id="1e412-121">Kompilieren Sie in ps_1_1 Version.</span><span class="sxs-lookup"><span data-stu-id="1e412-121">Compile to ps_1_1 version.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e412-122">ps_1_2</span><span class="sxs-lookup"><span data-stu-id="1e412-122">ps_1_2</span></span></td>
<td><span data-ttu-id="1e412-123">Kompilieren Sie in ps_1_2 Version.</span><span class="sxs-lookup"><span data-stu-id="1e412-123">Compile to ps_1_2 version.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e412-124">ps_1_3</span><span class="sxs-lookup"><span data-stu-id="1e412-124">ps_1_3</span></span></td>
<td><span data-ttu-id="1e412-125">Kompilieren Sie in ps_1_3 Version.</span><span class="sxs-lookup"><span data-stu-id="1e412-125">Compile to ps_1_3 version.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e412-126">ps_1_4</span><span class="sxs-lookup"><span data-stu-id="1e412-126">ps_1_4</span></span></td>
<td><span data-ttu-id="1e412-127">Kompilieren Sie in ps_1_4 Version.</span><span class="sxs-lookup"><span data-stu-id="1e412-127">Compile to ps_1_4 version.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e412-128">ps_2_0</span><span class="sxs-lookup"><span data-stu-id="1e412-128">ps_2_0</span></span></td>
<td><span data-ttu-id="1e412-129">Kompilieren Sie in PS_2_0 Version.</span><span class="sxs-lookup"><span data-stu-id="1e412-129">Compile to ps_2_0 version.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e412-130">ps_2_a</span><span class="sxs-lookup"><span data-stu-id="1e412-130">ps_2_a</span></span></td>
<td><span data-ttu-id="1e412-131">Identisch mit dem PS_2_0 Profil mit den folgenden zusätzlichen Funktionen, die für den Compiler als Ziel verfügbar sind:</span><span class="sxs-lookup"><span data-stu-id="1e412-131">Same as the ps_2_0 profile, with the following additional capabilities available for the compiler to target:</span></span>
<ul>
<li><span data-ttu-id="1e412-132">Die Anzahl der temporären Register (r #) ist größer als oder gleich 22.</span><span class="sxs-lookup"><span data-stu-id="1e412-132">Number of Temporary Registers (r#) is greater than or equal to 22.</span></span></li>
<li><span data-ttu-id="1e412-133">Beliebiger Quellpfad.</span><span class="sxs-lookup"><span data-stu-id="1e412-133">Arbitrary source swizzle.</span></span></li>
<li><span data-ttu-id="1e412-134">Farbverlaufs Anweisungen: DSX, DSY.</span><span class="sxs-lookup"><span data-stu-id="1e412-134">Gradient instructions: dsx, dsy.</span></span></li>
<li><span data-ttu-id="1e412-135">Prädikation übersprungen.</span><span class="sxs-lookup"><span data-stu-id="1e412-135">Predication.</span></span></li>
<li><span data-ttu-id="1e412-136">Keine abhängige Textur Lese Begrenzung.</span><span class="sxs-lookup"><span data-stu-id="1e412-136">No dependent texture read limit.</span></span></li>
<li><span data-ttu-id="1e412-137">Keine Beschränkung für die Anzahl der Textur Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="1e412-137">No limit for the number of texture instructions.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e412-138">ps_2_b</span><span class="sxs-lookup"><span data-stu-id="1e412-138">ps_2_b</span></span></td>
<td><span data-ttu-id="1e412-139">Identisch mit dem PS_2_0 Profil mit den folgenden zusätzlichen Funktionen, die für den Compiler als Ziel verfügbar sind:</span><span class="sxs-lookup"><span data-stu-id="1e412-139">Same as the ps_2_0 profile, with the following additional capabilities available for the compiler to target:</span></span>
<ul>
<li><span data-ttu-id="1e412-140">Die Anzahl der temporären Register (r #) ist größer als oder gleich 32.</span><span class="sxs-lookup"><span data-stu-id="1e412-140">Number of Temporary Registers (r#) is greater than or equal to 32.</span></span></li>
<li><span data-ttu-id="1e412-141">Keine Beschränkung für die Anzahl der Textur Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="1e412-141">No limit for the number of texture instructions.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e412-142">ps_3_0</span><span class="sxs-lookup"><span data-stu-id="1e412-142">ps_3_0</span></span></td>
<td><span data-ttu-id="1e412-143">Kompilieren Sie in ps_3_0 Version.</span><span class="sxs-lookup"><span data-stu-id="1e412-143">Compile to ps_3_0 version.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="1e412-144">Weitere Informationen zu den Unterschieden zwischen shaderversionen finden Sie [unter Unterschiede bei Pixel-Shadern](../direct3dhlsl/dx9-graphics-reference-asm-ps-differences.md).</span><span class="sxs-lookup"><span data-stu-id="1e412-144">For more information about the differences between shader versions, see [Pixel Shader Differences](../direct3dhlsl/dx9-graphics-reference-asm-ps-differences.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1e412-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e412-145">Requirements</span></span>



| <span data-ttu-id="1e412-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1e412-146">Requirement</span></span> | <span data-ttu-id="1e412-147">Wert</span><span class="sxs-lookup"><span data-stu-id="1e412-147">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e412-148">Header</span><span class="sxs-lookup"><span data-stu-id="1e412-148">Header</span></span><br/>  | <dl> <span data-ttu-id="1e412-149"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e412-149"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="1e412-150">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1e412-150">Library</span></span><br/> | <dl> <span data-ttu-id="1e412-151"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1e412-151"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="1e412-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e412-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e412-153">Shaderfunktionen</span><span class="sxs-lookup"><span data-stu-id="1e412-153">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
