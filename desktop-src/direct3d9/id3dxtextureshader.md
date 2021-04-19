---
description: Die ID3DXTextureShader-Schnittstelle.
ms.assetid: 48ea307d-857f-4b73-9e13-de391fbce07b
title: ID3DXTextureShader-Schnittstelle (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c1b9581bced9d501800a8a8f3cb5d31a563ac261
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366456"
---
# <a name="id3dxtextureshader-interface"></a><span data-ttu-id="008ba-103">ID3DXTextureShader-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="008ba-103">ID3DXTextureShader interface</span></span>

<span data-ttu-id="008ba-104">Die ID3DXTextureShader-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="008ba-104">The ID3DXTextureShader interface.</span></span>

## <a name="members"></a><span data-ttu-id="008ba-105">Member</span><span class="sxs-lookup"><span data-stu-id="008ba-105">Members</span></span>

<span data-ttu-id="008ba-106">Die **ID3DXTextureShader** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="008ba-106">The **ID3DXTextureShader** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="008ba-107">**ID3DXTextureShader** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="008ba-107">**ID3DXTextureShader** also has these types of members:</span></span>

-   [<span data-ttu-id="008ba-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="008ba-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="008ba-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="008ba-109">Methods</span></span>

<span data-ttu-id="008ba-110">Die **ID3DXTextureShader** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="008ba-110">The **ID3DXTextureShader** interface has these methods.</span></span>



| <span data-ttu-id="008ba-111">Methode</span><span class="sxs-lookup"><span data-stu-id="008ba-111">Method</span></span>                                                                                       | <span data-ttu-id="008ba-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="008ba-112">Description</span></span>                                                                 |
|:---------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="008ba-113">**Getconstant**</span><span class="sxs-lookup"><span data-stu-id="008ba-113">**GetConstant**</span></span>](id3dxtextureshader--getconstant.md)                                       | <span data-ttu-id="008ba-114">Ruft eine Konstante ab, indem ihr Index gesucht wird.</span><span class="sxs-lookup"><span data-stu-id="008ba-114">Gets a constant by looking up its index.</span></span><br/>                         |
| [<span data-ttu-id="008ba-115">**Getconstantbuffer**</span><span class="sxs-lookup"><span data-stu-id="008ba-115">**GetConstantBuffer**</span></span>](id3dxtextureshader--getconstantbuffer.md)                           | <span data-ttu-id="008ba-116">Einen Zeiger auf die Konstante Tabelle erhalten.</span><span class="sxs-lookup"><span data-stu-id="008ba-116">Get a pointer to the constant table.</span></span><br/>                             |
| [<span data-ttu-id="008ba-117">**Getconstantbyname**</span><span class="sxs-lookup"><span data-stu-id="008ba-117">**GetConstantByName**</span></span>](id3dxtextureshader--getconstantbyname.md)                           | <span data-ttu-id="008ba-118">Ruft eine Konstante ab, indem Ihr Name gesucht wird.</span><span class="sxs-lookup"><span data-stu-id="008ba-118">Gets a constant by looking up its name.</span></span><br/>                          |
| [<span data-ttu-id="008ba-119">**Getconstantdebug**</span><span class="sxs-lookup"><span data-stu-id="008ba-119">**GetConstantDesc**</span></span>](id3dxtextureshader--getconstantdesc.md)                               | <span data-ttu-id="008ba-120">Ruft einen Zeiger auf das Array von Konstanten in der Konstanten Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="008ba-120">Gets a pointer to the array of constants in the constant table.</span></span><br/>  |
| [<span data-ttu-id="008ba-121">**Getconstantelements**</span><span class="sxs-lookup"><span data-stu-id="008ba-121">**GetConstantElement**</span></span>](id3dxtextureshader--getconstantelement.md)                         | <span data-ttu-id="008ba-122">Eine Konstante aus der Konstanten Tabelle erhalten.</span><span class="sxs-lookup"><span data-stu-id="008ba-122">Get a constant from the constant table.</span></span><br/>                          |
| [<span data-ttu-id="008ba-123">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="008ba-123">**GetDesc**</span></span>](id3dxtextureshader--getdesc.md)                                               | <span data-ttu-id="008ba-124">Ruft eine Beschreibung der Konstanten Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="008ba-124">Gets a description of the constant table.</span></span><br/>                        |
| [<span data-ttu-id="008ba-125">**GetFunction**</span><span class="sxs-lookup"><span data-stu-id="008ba-125">**GetFunction**</span></span>](id3dxtextureshader--getfunction.md)                                       | <span data-ttu-id="008ba-126">Ruft einen Zeiger auf die Funktion DWORD-Stream ab.</span><span class="sxs-lookup"><span data-stu-id="008ba-126">Gets a pointer to the function DWORD stream.</span></span><br/>                     |
| [<span data-ttu-id="008ba-127">**SetBool**</span><span class="sxs-lookup"><span data-stu-id="008ba-127">**SetBool**</span></span>](id3dxtextureshader--setbool.md)                                               | <span data-ttu-id="008ba-128">Legt einen booleschen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="008ba-128">Sets a BOOL value.</span></span><br/>                                               |
| [<span data-ttu-id="008ba-129">**Setboolarray**</span><span class="sxs-lookup"><span data-stu-id="008ba-129">**SetBoolArray**</span></span>](id3dxtextureshader--setboolarray.md)                                     | <span data-ttu-id="008ba-130">Legt ein Array von booleschen Werten fest.</span><span class="sxs-lookup"><span data-stu-id="008ba-130">Sets an array of BOOL values.</span></span><br/>                                    |
| [<span data-ttu-id="008ba-131">**SetDefaults**</span><span class="sxs-lookup"><span data-stu-id="008ba-131">**SetDefaults**</span></span>](id3dxtextureshader--setdefaults.md)                                       | <span data-ttu-id="008ba-132">Legt die Konstanten auf die im Shader deklarierten Standardwerte fest.</span><span class="sxs-lookup"><span data-stu-id="008ba-132">Sets the constants to the default values declared in the shader.</span></span><br/> |
| [<span data-ttu-id="008ba-133">**SetFloat**</span><span class="sxs-lookup"><span data-stu-id="008ba-133">**SetFloat**</span></span>](id3dxtextureshader--setfloat.md)                                             | <span data-ttu-id="008ba-134">Legt eine Gleit Komma Zahl fest.</span><span class="sxs-lookup"><span data-stu-id="008ba-134">Sets a floating-point number.</span></span><br/>                                    |
| [<span data-ttu-id="008ba-135">**Setfloatarray**</span><span class="sxs-lookup"><span data-stu-id="008ba-135">**SetFloatArray**</span></span>](id3dxtextureshader--setfloatarray.md)                                   | <span data-ttu-id="008ba-136">Legt ein Array von Gleit Komma Zahlen fest.</span><span class="sxs-lookup"><span data-stu-id="008ba-136">Sets an array of floating-point numbers.</span></span><br/>                         |
| [<span data-ttu-id="008ba-137">**SetInt**</span><span class="sxs-lookup"><span data-stu-id="008ba-137">**SetInt**</span></span>](id3dxtextureshader--setint.md)                                                 | <span data-ttu-id="008ba-138">Legt einen ganzzahligen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="008ba-138">Sets an integer value.</span></span><br/>                                           |
| [<span data-ttu-id="008ba-139">**"Tartintarray"**</span><span class="sxs-lookup"><span data-stu-id="008ba-139">**SetIntArray**</span></span>](id3dxtextureshader--setintarray.md)                                       | <span data-ttu-id="008ba-140">Legt ein Array von ganzen Zahlen fest.</span><span class="sxs-lookup"><span data-stu-id="008ba-140">Sets an array of integers.</span></span><br/>                                       |
| [<span data-ttu-id="008ba-141">**SetMatrix**</span><span class="sxs-lookup"><span data-stu-id="008ba-141">**SetMatrix**</span></span>](id3dxtextureshader--setmatrix.md)                                           | <span data-ttu-id="008ba-142">Legt eine nicht übersetzte Matrix fest.</span><span class="sxs-lookup"><span data-stu-id="008ba-142">Sets a non-transposed matrix.</span></span><br/>                                    |
| [<span data-ttu-id="008ba-143">**Setmatrixarray**</span><span class="sxs-lookup"><span data-stu-id="008ba-143">**SetMatrixArray**</span></span>](id3dxtextureshader--setmatrixarray.md)                                 | <span data-ttu-id="008ba-144">Legt ein Array von nicht übersetzten Matrizen fest.</span><span class="sxs-lookup"><span data-stu-id="008ba-144">Sets an array of non-transposed matrices.</span></span><br/>                        |
| [<span data-ttu-id="008ba-145">**Setmatrixpointerarray**</span><span class="sxs-lookup"><span data-stu-id="008ba-145">**SetMatrixPointerArray**</span></span>](id3dxtextureshader--setmatrixpointerarray.md)                   | <span data-ttu-id="008ba-146">Legt ein Array von Zeigern auf nicht übersetzte Matrizen fest.</span><span class="sxs-lookup"><span data-stu-id="008ba-146">Sets an array of pointers to non-transposed matrices.</span></span><br/>            |
| [<span data-ttu-id="008ba-147">**Setmatrixtransform**</span><span class="sxs-lookup"><span data-stu-id="008ba-147">**SetMatrixTranspose**</span></span>](id3dxtextureshader--setmatrixtranspose.md)                         | <span data-ttu-id="008ba-148">Legt eine übersetzte Matrix fest.</span><span class="sxs-lookup"><span data-stu-id="008ba-148">Sets a transposed matrix.</span></span><br/>                                        |
| [<span data-ttu-id="008ba-149">**Setmatrixtransposearray**</span><span class="sxs-lookup"><span data-stu-id="008ba-149">**SetMatrixTransposeArray**</span></span>](id3dxtextureshader--setmatrixtransposearray.md)               | <span data-ttu-id="008ba-150">Legt ein Array von umsetzten Matrizen fest.</span><span class="sxs-lookup"><span data-stu-id="008ba-150">Sets an array of transposed matrices.</span></span><br/>                            |
| [<span data-ttu-id="008ba-151">**Setmatrixtransposepointerarray**</span><span class="sxs-lookup"><span data-stu-id="008ba-151">**SetMatrixTransposePointerArray**</span></span>](id3dxtextureshader--setmatrixtransposepointerarray.md) | <span data-ttu-id="008ba-152">Legt ein Array von Zeigern auf umgesetzte Matrizen fest.</span><span class="sxs-lookup"><span data-stu-id="008ba-152">Sets an array of pointers to transposed matrices.</span></span><br/>                |
| [<span data-ttu-id="008ba-153">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="008ba-153">**SetValue**</span></span>](id3dxtextureshader--setvalue.md)                                             | <span data-ttu-id="008ba-154">Legt die Konstante Tabelle mit den Daten im Puffer fest.</span><span class="sxs-lookup"><span data-stu-id="008ba-154">Sets the constant table with the data in the buffer.</span></span><br/>             |
| [<span data-ttu-id="008ba-155">**Setvector**</span><span class="sxs-lookup"><span data-stu-id="008ba-155">**SetVector**</span></span>](id3dxtextureshader--setvector.md)                                           | <span data-ttu-id="008ba-156">Legt einen 4D-Vektor fest.</span><span class="sxs-lookup"><span data-stu-id="008ba-156">Sets a 4D vector.</span></span><br/>                                                |
| [<span data-ttu-id="008ba-157">**Setvector Array**</span><span class="sxs-lookup"><span data-stu-id="008ba-157">**SetVectorArray**</span></span>](id3dxtextureshader--setvectorarray.md)                                 | <span data-ttu-id="008ba-158">Legt ein Array von 4D-Vektoren fest.</span><span class="sxs-lookup"><span data-stu-id="008ba-158">Sets an array of 4D vectors.</span></span><br/>                                     |



 

## <a name="remarks"></a><span data-ttu-id="008ba-159">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="008ba-159">Remarks</span></span>

<span data-ttu-id="008ba-160">Die **ID3DXTextureShader** -Schnittstelle wird durch Aufrufen der [**D3DXCreateTextureShader**](d3dxcreatetextureshader.md) -Funktion abgerufen.</span><span class="sxs-lookup"><span data-stu-id="008ba-160">The **ID3DXTextureShader** interface is obtained by calling the [**D3DXCreateTextureShader**](d3dxcreatetextureshader.md) function.</span></span>

<span data-ttu-id="008ba-161">Die **ID3DXTextureShader** -Schnittstelle erbt wie alle COM-Schnittstellen die [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="008ba-161">The **ID3DXTextureShader** interface, like all COM interfaces, inherits the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span>

<span data-ttu-id="008ba-162">Der LPD3DXTEXTURESHADER-Typ wird als Zeiger auf die **ID3DXTextureShader** -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="008ba-162">The LPD3DXTEXTURESHADER type is defined as a pointer to the **ID3DXTextureShader** interface.</span></span>


```
typedef interface ID3DXTextureShader *LPD3DXTEXTURESHADER;
```



## <a name="requirements"></a><span data-ttu-id="008ba-163">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="008ba-163">Requirements</span></span>



| <span data-ttu-id="008ba-164">Anforderung</span><span class="sxs-lookup"><span data-stu-id="008ba-164">Requirement</span></span> | <span data-ttu-id="008ba-165">Wert</span><span class="sxs-lookup"><span data-stu-id="008ba-165">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="008ba-166">Header</span><span class="sxs-lookup"><span data-stu-id="008ba-166">Header</span></span><br/>  | <dl> <span data-ttu-id="008ba-167"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="008ba-167"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="008ba-168">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="008ba-168">Library</span></span><br/> | <dl> <span data-ttu-id="008ba-169"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="008ba-169"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="008ba-170">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="008ba-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="008ba-171">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="008ba-171">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
