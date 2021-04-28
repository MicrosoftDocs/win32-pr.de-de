---
description: 'D3DXGetVertexShaderProfile-Funktion: Gibt den Namen des höchsten HLSL-Profils (High-Level Shader Language) zurück, das von einem bestimmten Gerät unterstützt wird.'
ms.assetid: a50e2a17-8170-4364-a562-7886593341b3
title: D3DXGetVertexShaderProfile-Funktion (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetVertexShaderProfile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 70d6cdf79fdd91e819d54702682515aa3e4810b4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114458"
---
# <a name="d3dxgetvertexshaderprofile-function"></a><span data-ttu-id="4130e-103">D3DXGetVertexShaderProfile-Funktion</span><span class="sxs-lookup"><span data-stu-id="4130e-103">D3DXGetVertexShaderProfile function</span></span>

<span data-ttu-id="4130e-104">Gibt den Namen des höchsten HLSL-Profils (High-Level Shader Language) zurück, das von einem bestimmten Gerät unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="4130e-104">Returns the name of the highest high-level shader language (HLSL) profile supported by a given device.</span></span>

## <a name="syntax"></a><span data-ttu-id="4130e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4130e-105">Syntax</span></span>


```C++
LPCSTR D3DXGetVertexShaderProfile(
  _In_ LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a><span data-ttu-id="4130e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4130e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4130e-107">*pDevice* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="4130e-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4130e-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="4130e-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="4130e-109">Zeiger auf das Gerät.</span><span class="sxs-lookup"><span data-stu-id="4130e-109">Pointer to the device.</span></span> <span data-ttu-id="4130e-110">Siehe [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="4130e-110">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4130e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4130e-111">Return value</span></span>

<span data-ttu-id="4130e-112">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4130e-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4130e-113">Der HLSL-Profilname.</span><span class="sxs-lookup"><span data-stu-id="4130e-113">The HLSL profile name.</span></span>

<span data-ttu-id="4130e-114">Wenn das Gerät keine Vertex-Shader unterstützt, gibt die Funktion **NULL** zurück.</span><span class="sxs-lookup"><span data-stu-id="4130e-114">If the device does not support vertex shaders then the function returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4130e-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4130e-115">Remarks</span></span>

<span data-ttu-id="4130e-116">Ein Shaderprofil gibt die zu verwendende Assembly-Shaderversion und die Funktionen an, die dem HLSL-Compiler beim Kompilieren eines Shaders zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="4130e-116">A shader profile specifies the assembly shader version to use and the capabilities available to the HLSL compiler when compiling a shader.</span></span> <span data-ttu-id="4130e-117">In der folgenden Tabelle sind die unterstützten Vertex-Shaderprofile aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="4130e-117">The following table lists the vertex shader profiles that are supported.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4130e-118">Shaderprofil</span><span class="sxs-lookup"><span data-stu-id="4130e-118">Shader Profile</span></span></th>
<th><span data-ttu-id="4130e-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4130e-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4130e-120">vs_1_1</span><span class="sxs-lookup"><span data-stu-id="4130e-120">vs_1_1</span></span></td>
<td><span data-ttu-id="4130e-121">Kompilieren Sie in vs_1_1 Version.</span><span class="sxs-lookup"><span data-stu-id="4130e-121">Compile to vs_1_1 version.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4130e-122">vs_2_0</span><span class="sxs-lookup"><span data-stu-id="4130e-122">vs_2_0</span></span></td>
<td><span data-ttu-id="4130e-123">Kompilieren Sie in vs_2_0 Version.</span><span class="sxs-lookup"><span data-stu-id="4130e-123">Compile to vs_2_0 version.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4130e-124">vs_2_a</span><span class="sxs-lookup"><span data-stu-id="4130e-124">vs_2_a</span></span></td>
<td><span data-ttu-id="4130e-125">Entspricht dem vs_2_0 Profil mit den folgenden zusätzlichen Funktionen, die der Compiler als Ziel hat:</span><span class="sxs-lookup"><span data-stu-id="4130e-125">Same as the vs_2_0 profile, with the following additional capabilities available for the compiler to target:</span></span>
<ul>
<li><span data-ttu-id="4130e-126">Die Anzahl temporärer Register (r#) ist größer oder gleich 13.</span><span class="sxs-lookup"><span data-stu-id="4130e-126">Number of Temporary Registers (r#) is greater than or equal to 13.</span></span></li>
<li><span data-ttu-id="4130e-127">Anweisung zur dynamischen Flusssteuerung.</span><span class="sxs-lookup"><span data-stu-id="4130e-127">Dynamic flow control instruction.</span></span></li>
<li><span data-ttu-id="4130e-128">Prädication.</span><span class="sxs-lookup"><span data-stu-id="4130e-128">Predication.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4130e-129">vs_3_0</span><span class="sxs-lookup"><span data-stu-id="4130e-129">vs_3_0</span></span></td>
<td><span data-ttu-id="4130e-130">Kompilieren Sie vs_3_0 Version.</span><span class="sxs-lookup"><span data-stu-id="4130e-130">Compile to vs_3_0 version.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="4130e-131">Weitere Informationen zu den Unterschieden zwischen shader-Versionen finden Sie unter [Vertex Shader Differences](../direct3dhlsl/dx9-graphics-reference-asm-vs-differences.md).</span><span class="sxs-lookup"><span data-stu-id="4130e-131">For more information about the differences between shader versions, see [Vertex Shader Differences](../direct3dhlsl/dx9-graphics-reference-asm-vs-differences.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4130e-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4130e-132">Requirements</span></span>



| <span data-ttu-id="4130e-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4130e-133">Requirement</span></span> | <span data-ttu-id="4130e-134">Wert</span><span class="sxs-lookup"><span data-stu-id="4130e-134">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4130e-135">Header</span><span class="sxs-lookup"><span data-stu-id="4130e-135">Header</span></span><br/>  | <dl> <span data-ttu-id="4130e-136"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="4130e-136"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="4130e-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4130e-137">Library</span></span><br/> | <dl> <span data-ttu-id="4130e-138"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="4130e-138"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="4130e-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4130e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4130e-140">Shaderfunktionen</span><span class="sxs-lookup"><span data-stu-id="4130e-140">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
