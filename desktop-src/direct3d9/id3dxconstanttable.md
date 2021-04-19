---
description: Die ID3DXConstantTable-Schnittstelle wird verwendet, um auf die Konstante Tabelle zuzugreifen. Diese Tabelle enthält die Variablen, die von den sprach-Shadern und-Effekten auf hoher Ebene verwendet werden.
ms.assetid: 5d412c77-3d35-4913-86e5-8efa0549a2bb
title: ID3DXConstantTable-Schnittstelle (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bb2b7614c4d6a0e677f71e66ab94abdb89deb973
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366648"
---
# <a name="id3dxconstanttable-interface"></a><span data-ttu-id="c94d0-104">ID3DXConstantTable-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="c94d0-104">ID3DXConstantTable interface</span></span>

<span data-ttu-id="c94d0-105">Die ID3DXConstantTable-Schnittstelle wird verwendet, um auf die Konstante Tabelle zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="c94d0-105">The ID3DXConstantTable interface is used to access the constant table.</span></span> <span data-ttu-id="c94d0-106">Diese Tabelle enthält die Variablen, die von den sprach-Shadern und-Effekten auf hoher Ebene verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c94d0-106">This table contains the variables that are used by high-level language shaders and effects.</span></span>

## <a name="members"></a><span data-ttu-id="c94d0-107">Member</span><span class="sxs-lookup"><span data-stu-id="c94d0-107">Members</span></span>

<span data-ttu-id="c94d0-108">Die **ID3DXConstantTable** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="c94d0-108">The **ID3DXConstantTable** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c94d0-109">**ID3DXConstantTable** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c94d0-109">**ID3DXConstantTable** also has these types of members:</span></span>

-   [<span data-ttu-id="c94d0-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="c94d0-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c94d0-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="c94d0-111">Methods</span></span>

<span data-ttu-id="c94d0-112">Die **ID3DXConstantTable** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="c94d0-112">The **ID3DXConstantTable** interface has these methods.</span></span>



| <span data-ttu-id="c94d0-113">Methode</span><span class="sxs-lookup"><span data-stu-id="c94d0-113">Method</span></span>                                                                                       | <span data-ttu-id="c94d0-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c94d0-114">Description</span></span>                                                                                                                        |
|:---------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c94d0-115">**Getbufferpointer**</span><span class="sxs-lookup"><span data-stu-id="c94d0-115">**GetBufferPointer**</span></span>](id3dxconstanttable--getbufferpointer.md)                             | <span data-ttu-id="c94d0-116">Ruft einen Zeiger auf den Puffer ab, der die Konstante Tabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="c94d0-116">Gets a pointer to the buffer that contains the constant table.</span></span><br/>                                                          |
| [<span data-ttu-id="c94d0-117">**GetBufferSize**</span><span class="sxs-lookup"><span data-stu-id="c94d0-117">**GetBufferSize**</span></span>](id3dxconstanttable--getbuffersize.md)                                   | <span data-ttu-id="c94d0-118">Ruft die Puffergröße der Konstanten Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="c94d0-118">Gets the buffer size of the constant table.</span></span><br/>                                                                             |
| [<span data-ttu-id="c94d0-119">**Getconstant**</span><span class="sxs-lookup"><span data-stu-id="c94d0-119">**GetConstant**</span></span>](id3dxconstanttable--getconstant.md)                                       | <span data-ttu-id="c94d0-120">Ruft eine Konstante ab, indem ihr Index gesucht wird.</span><span class="sxs-lookup"><span data-stu-id="c94d0-120">Gets a constant by looking up its index.</span></span><br/>                                                                                |
| [<span data-ttu-id="c94d0-121">**Getconstantbyname**</span><span class="sxs-lookup"><span data-stu-id="c94d0-121">**GetConstantByName**</span></span>](id3dxconstanttable--getconstantbyname.md)                           | <span data-ttu-id="c94d0-122">Ruft eine Konstante ab, indem Ihr Name gesucht wird.</span><span class="sxs-lookup"><span data-stu-id="c94d0-122">Gets a constant by looking up its name.</span></span><br/>                                                                                 |
| [<span data-ttu-id="c94d0-123">**Getconstantdebug**</span><span class="sxs-lookup"><span data-stu-id="c94d0-123">**GetConstantDesc**</span></span>](id3dxconstanttable--getconstantdesc.md)                               | <span data-ttu-id="c94d0-124">Ruft einen Zeiger auf ein Array konstanter Beschreibungen in der Konstanten Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="c94d0-124">Gets a pointer to an array of constant descriptions in the constant table.</span></span><br/>                                              |
| [<span data-ttu-id="c94d0-125">**Getconstantelements**</span><span class="sxs-lookup"><span data-stu-id="c94d0-125">**GetConstantElement**</span></span>](id3dxconstanttable--getconstantelement.md)                         | <span data-ttu-id="c94d0-126">Ruft eine Konstante von einem Array von Konstanten ab.</span><span class="sxs-lookup"><span data-stu-id="c94d0-126">Gets a constant from an array of constants.</span></span> <span data-ttu-id="c94d0-127">Ein Array besteht aus Elementen.</span><span class="sxs-lookup"><span data-stu-id="c94d0-127">An array is made up of elements.</span></span><br/>                                            |
| [<span data-ttu-id="c94d0-128">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="c94d0-128">**GetDesc**</span></span>](id3dxconstanttable--getdesc.md)                                               | <span data-ttu-id="c94d0-129">Ruft eine Beschreibung der Konstanten Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="c94d0-129">Gets a description of the constant table.</span></span><br/>                                                                               |
| [<span data-ttu-id="c94d0-130">**Getsamplerindex**</span><span class="sxs-lookup"><span data-stu-id="c94d0-130">**GetSamplerIndex**</span></span>](id3dxconstanttable--getsamplerindex.md)                               | <span data-ttu-id="c94d0-131">Gibt den samplerindex zurück.</span><span class="sxs-lookup"><span data-stu-id="c94d0-131">Returns the sampler index.</span></span><br/>                                                                                              |
| [<span data-ttu-id="c94d0-132">**SetBool**</span><span class="sxs-lookup"><span data-stu-id="c94d0-132">**SetBool**</span></span>](id3dxconstanttable--setbool.md)                                               | <span data-ttu-id="c94d0-133">Legt einen booleschen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="c94d0-133">Sets a Boolean value.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="c94d0-134">**Setboolarray**</span><span class="sxs-lookup"><span data-stu-id="c94d0-134">**SetBoolArray**</span></span>](id3dxconstanttable--setboolarray.md)                                     | <span data-ttu-id="c94d0-135">Legt ein Array von booleschen Werten fest.</span><span class="sxs-lookup"><span data-stu-id="c94d0-135">Sets an array of Boolean values.</span></span><br/>                                                                                        |
| [<span data-ttu-id="c94d0-136">**SetDefaults**</span><span class="sxs-lookup"><span data-stu-id="c94d0-136">**SetDefaults**</span></span>](id3dxconstanttable--setdefaults.md)                                       | <span data-ttu-id="c94d0-137">Legt die Konstanten auf ihre Standardwerte fest.</span><span class="sxs-lookup"><span data-stu-id="c94d0-137">Sets the constants to their default values.</span></span> <span data-ttu-id="c94d0-138">Die Standardwerte werden in den Variablen Deklarationen im Shader deklariert.</span><span class="sxs-lookup"><span data-stu-id="c94d0-138">The default values are declared in the variable declarations in the shader.</span></span><br/> |
| [<span data-ttu-id="c94d0-139">**SetFloat**</span><span class="sxs-lookup"><span data-stu-id="c94d0-139">**SetFloat**</span></span>](id3dxconstanttable--setfloat.md)                                             | <span data-ttu-id="c94d0-140">Legt eine Gleit Komma Zahl fest.</span><span class="sxs-lookup"><span data-stu-id="c94d0-140">Sets a floating-point number.</span></span><br/>                                                                                           |
| [<span data-ttu-id="c94d0-141">**Setfloatarray**</span><span class="sxs-lookup"><span data-stu-id="c94d0-141">**SetFloatArray**</span></span>](id3dxconstanttable--setfloatarray.md)                                   | <span data-ttu-id="c94d0-142">Legt ein Array von Gleit Komma Zahlen fest.</span><span class="sxs-lookup"><span data-stu-id="c94d0-142">Sets an array of floating-point numbers.</span></span><br/>                                                                                |
| [<span data-ttu-id="c94d0-143">**SetInt**</span><span class="sxs-lookup"><span data-stu-id="c94d0-143">**SetInt**</span></span>](id3dxconstanttable--setint.md)                                                 | <span data-ttu-id="c94d0-144">Legt einen ganzzahligen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="c94d0-144">Sets an integer value.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="c94d0-145">**"Tartintarray"**</span><span class="sxs-lookup"><span data-stu-id="c94d0-145">**SetIntArray**</span></span>](id3dxconstanttable--setintarray.md)                                       | <span data-ttu-id="c94d0-146">Legt ein Array von ganzen Zahlen fest.</span><span class="sxs-lookup"><span data-stu-id="c94d0-146">Sets an array of integers.</span></span><br/>                                                                                              |
| [<span data-ttu-id="c94d0-147">**SetMatrix**</span><span class="sxs-lookup"><span data-stu-id="c94d0-147">**SetMatrix**</span></span>](id3dxconstanttable--setmatrix.md)                                           | <span data-ttu-id="c94d0-148">Legt eine nicht übersetzte Matrix fest.</span><span class="sxs-lookup"><span data-stu-id="c94d0-148">Sets a nontransposed matrix.</span></span><br/>                                                                                            |
| [<span data-ttu-id="c94d0-149">**Setmatrixarray**</span><span class="sxs-lookup"><span data-stu-id="c94d0-149">**SetMatrixArray**</span></span>](id3dxconstanttable--setmatrixarray.md)                                 | <span data-ttu-id="c94d0-150">Legt ein Array nicht umsetzbarer Matrizen fest.</span><span class="sxs-lookup"><span data-stu-id="c94d0-150">Sets an array of nontransposed matrices.</span></span><br/>                                                                                |
| [<span data-ttu-id="c94d0-151">**Setmatrixpointerarray**</span><span class="sxs-lookup"><span data-stu-id="c94d0-151">**SetMatrixPointerArray**</span></span>](id3dxconstanttable--setmatrixpointerarray.md)                   | <span data-ttu-id="c94d0-152">Legt ein Array von Zeigern auf nicht umgesetzte Matrizen fest.</span><span class="sxs-lookup"><span data-stu-id="c94d0-152">Sets an array of pointers to nontransposed matrices.</span></span><br/>                                                                    |
| [<span data-ttu-id="c94d0-153">**Setmatrixtransform**</span><span class="sxs-lookup"><span data-stu-id="c94d0-153">**SetMatrixTranspose**</span></span>](id3dxconstanttable--setmatrixtranspose.md)                         | <span data-ttu-id="c94d0-154">Legt eine übersetzte Matrix fest.</span><span class="sxs-lookup"><span data-stu-id="c94d0-154">Sets a transposed matrix.</span></span><br/>                                                                                               |
| [<span data-ttu-id="c94d0-155">**Setmatrixtransposearray**</span><span class="sxs-lookup"><span data-stu-id="c94d0-155">**SetMatrixTransposeArray**</span></span>](id3dxconstanttable--setmatrixtransposearray.md)               | <span data-ttu-id="c94d0-156">Legt ein Array von umsetzten Matrizen fest.</span><span class="sxs-lookup"><span data-stu-id="c94d0-156">Sets an array of transposed matrices.</span></span><br/>                                                                                   |
| [<span data-ttu-id="c94d0-157">**Setmatrixtransposepointerarray**</span><span class="sxs-lookup"><span data-stu-id="c94d0-157">**SetMatrixTransposePointerArray**</span></span>](id3dxconstanttable--setmatrixtransposepointerarray.md) | <span data-ttu-id="c94d0-158">Legt ein Array von Zeigern auf umgesetzte Matrizen fest.</span><span class="sxs-lookup"><span data-stu-id="c94d0-158">Sets an array of pointers to transposed matrices.</span></span><br/>                                                                       |
| [<span data-ttu-id="c94d0-159">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="c94d0-159">**SetValue**</span></span>](id3dxconstanttable--setvalue.md)                                             | <span data-ttu-id="c94d0-160">Legt den Inhalt des Puffers auf die Konstante Tabelle fest.</span><span class="sxs-lookup"><span data-stu-id="c94d0-160">Sets the contents of the buffer to the constant table.</span></span><br/>                                                                  |
| [<span data-ttu-id="c94d0-161">**Setvector**</span><span class="sxs-lookup"><span data-stu-id="c94d0-161">**SetVector**</span></span>](id3dxconstanttable--setvector.md)                                           | <span data-ttu-id="c94d0-162">Legt einen 4D-Vektor fest.</span><span class="sxs-lookup"><span data-stu-id="c94d0-162">Sets a 4D vector.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="c94d0-163">**Setvector Array**</span><span class="sxs-lookup"><span data-stu-id="c94d0-163">**SetVectorArray**</span></span>](id3dxconstanttable--setvectorarray.md)                                 | <span data-ttu-id="c94d0-164">Legt ein Array von 4D-Vektoren fest.</span><span class="sxs-lookup"><span data-stu-id="c94d0-164">Sets an array of 4D vectors.</span></span><br/>                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="c94d0-165">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c94d0-165">Remarks</span></span>

<span data-ttu-id="c94d0-166">Der LPD3DXCONSTANTTABLE-Typ wird als Zeiger auf die **ID3DXConstantTable** -Schnittstelle definiert.</span><span class="sxs-lookup"><span data-stu-id="c94d0-166">The LPD3DXCONSTANTTABLE type is defined as a pointer to the **ID3DXConstantTable** interface.</span></span>


```
typedef interface ID3DXConstantTable ID3DXConstantTable;
typedef interface ID3DXConstantTable *LPD3DXCONSTANTTABLE;
```



## <a name="requirements"></a><span data-ttu-id="c94d0-167">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c94d0-167">Requirements</span></span>



| <span data-ttu-id="c94d0-168">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c94d0-168">Requirement</span></span> | <span data-ttu-id="c94d0-169">Wert</span><span class="sxs-lookup"><span data-stu-id="c94d0-169">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c94d0-170">Header</span><span class="sxs-lookup"><span data-stu-id="c94d0-170">Header</span></span><br/>  | <dl> <span data-ttu-id="c94d0-171"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="c94d0-171"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="c94d0-172">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c94d0-172">Library</span></span><br/> | <dl> <span data-ttu-id="c94d0-173"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c94d0-173"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c94d0-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c94d0-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c94d0-175">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="c94d0-175">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
