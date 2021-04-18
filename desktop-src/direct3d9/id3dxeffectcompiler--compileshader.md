---
description: Kompiliert einen Shader aus einem Effekt, der eine oder mehrere Funktionen enthält.
ms.assetid: f34a2975-dcd5-4917-9b11-ed40583272f9
title: 'ID3DXEffectCompiler:: compileshader-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler.CompileShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 375646202e102623053c179398329ad2286e6c1b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371927"
---
# <a name="id3dxeffectcompilercompileshader-method"></a><span data-ttu-id="c0384-103">ID3DXEffectCompiler:: compileshader-Methode</span><span class="sxs-lookup"><span data-stu-id="c0384-103">ID3DXEffectCompiler::CompileShader method</span></span>

<span data-ttu-id="c0384-104">Kompiliert einen Shader aus einem Effekt, der eine oder mehrere Funktionen enthält.</span><span class="sxs-lookup"><span data-stu-id="c0384-104">Compiles a shader from an effect that contains one or more functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0384-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0384-105">Syntax</span></span>


```C++
HRESULT CompileShader(
  [in]          D3DXHANDLE          hFunction,
  [in]          LPCSTR              pTarget,
  [in]          DWORD               Flags,
  [out, retval] LPD3DXBUFFER        *ppShader,
  [out, retval] LPD3DXBUFFER        *ppErrorMsgs,
  [out]         LPD3DXCONSTANTTABLE *ppConstantTable
);
```



## <a name="parameters"></a><span data-ttu-id="c0384-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0384-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0384-107">*hfunction* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c0384-107">*hFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0384-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="c0384-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="c0384-109">Eindeutiger Bezeichner für die Funktion, die kompiliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c0384-109">Unique identifier to the function to be compiled.</span></span> <span data-ttu-id="c0384-110">Dieser Wert darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="c0384-110">This value must not be **NULL**.</span></span> <span data-ttu-id="c0384-111">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="c0384-111">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0384-112">*pTARGET* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c0384-112">*pTarget* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0384-113">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c0384-113">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c0384-114">Zeiger auf ein Shader-Profil, das den Shader-Anweisungs Satz bestimmt.</span><span class="sxs-lookup"><span data-stu-id="c0384-114">Pointer to a shader profile which determines the shader instruction set.</span></span> <span data-ttu-id="c0384-115">Eine Liste der verfügbaren Profile finden Sie unter [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) oder [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="c0384-115">See [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) or [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) for a list of the profiles available.</span></span>

</dd> <dt>

<span data-ttu-id="c0384-116">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="c0384-116">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0384-117">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c0384-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c0384-118">Kompilierungsoptionen, die durch verschiedene Flags identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="c0384-118">Compile options identified by various flags.</span></span> <span data-ttu-id="c0384-119">Der Direct3D 10 HLSL-Compiler ist nun der Standard.</span><span class="sxs-lookup"><span data-stu-id="c0384-119">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="c0384-120">Weitere Informationen finden Sie unter [D3DXSHADER-Flags](d3dxshader-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="c0384-120">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="c0384-121">*ppshader* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="c0384-121">*ppShader* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="c0384-122">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="c0384-122">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="c0384-123">Der Puffer, der den kompilierten Shader enthält.</span><span class="sxs-lookup"><span data-stu-id="c0384-123">Buffer containing the compiled shader.</span></span> <span data-ttu-id="c0384-124">Der compilershader ist ein Array von DWORDs.</span><span class="sxs-lookup"><span data-stu-id="c0384-124">The compiler shader is an array of DWORDs.</span></span> <span data-ttu-id="c0384-125">Weitere Informationen zum Zugreifen auf den Puffer finden Sie unter [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="c0384-125">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0384-126">*pperrormsgs* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="c0384-126">*ppErrorMsgs* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="c0384-127">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="c0384-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="c0384-128">Puffer, der mindestens die erste Kompilierungs Fehlermeldung enthält, die aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="c0384-128">Buffer containing at least the first compile error message that occurred.</span></span> <span data-ttu-id="c0384-129">Dies schließt Compilerfehler und allgemeine sprach Kompilierungsfehler ein.</span><span class="sxs-lookup"><span data-stu-id="c0384-129">This includes effect compiler errors and high-level language compile errors.</span></span> <span data-ttu-id="c0384-130">Weitere Informationen zum Zugreifen auf den Puffer finden Sie unter [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="c0384-130">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0384-131">*ppconstanbar* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c0384-131">*ppConstantTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0384-132">Typ: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span><span class="sxs-lookup"><span data-stu-id="c0384-132">Type: **[**LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span></span>

<span data-ttu-id="c0384-133">Gibt eine [**ID3DXConstantTable**](id3dxconstanttable.md) -Schnittstelle zurück, die für den Zugriff auf shaderkonstanten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c0384-133">Returns an [**ID3DXConstantTable**](id3dxconstanttable.md) interface, which can be used to access shader constants.</span></span> <span data-ttu-id="c0384-134">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="c0384-134">This value can be **NULL**.</span></span> <span data-ttu-id="c0384-135">Wenn Sie die Anwendung als große Adressen unterstützen (d. h. mit der/LARGEADDRESSAWARE-Linkeroption, um Adressen zu verarbeiten, die größer als 2 GB sind), können Sie diesen Parameter nicht verwenden und müssen ihn auf **null** festlegen.</span><span class="sxs-lookup"><span data-stu-id="c0384-135">If you compile your application as large address aware (that is, you use the /LARGEADDRESSAWARE linker option to handle addresses larger than 2 GB), you cannot use this parameter and must set it to **NULL**.</span></span> <span data-ttu-id="c0384-136">Stattdessen müssen Sie die [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) -Funktion verwenden, um die in den Shader eingebettete Shader-Konstante Tabelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c0384-136">Instead, you must use the [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) function to retrieve the shader-constant table that is embedded inside the shader.</span></span> <span data-ttu-id="c0384-137">In diesem **D3DXGetShaderConstantTableEx** -Aufruf müssen Sie das Flag **D3DXCONSTTABLE \_ LARGEADDRESSAWARE** an den *Flags* -Parameter übergeben, um anzugeben, dass auf bis zu 4 GB virtuellen Adressraum zugegriffen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c0384-137">In this **D3DXGetShaderConstantTableEx** call, you must pass the **D3DXCONSTTABLE\_LARGEADDRESSAWARE** flag to the *Flags* parameter to specify to access up to 4 GB of virtual address space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0384-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c0384-138">Return value</span></span>

<span data-ttu-id="c0384-139">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c0384-139">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c0384-140">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c0384-140">If the method succeeds, the return value is S\_OK.</span></span>

<span data-ttu-id="c0384-141">Wenn die Argumente ungültig sind, gibt die Methode D3DERR \_ invalidcallzurück.</span><span class="sxs-lookup"><span data-stu-id="c0384-141">If the arguments are invalid, the method will return D3DERR\_INVALIDCALL.</span></span>

<span data-ttu-id="c0384-142">Wenn die Methode fehlschlägt, lautet der Rückgabewert E \_ Fail.</span><span class="sxs-lookup"><span data-stu-id="c0384-142">If the method fails, the return value will be E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0384-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0384-143">Remarks</span></span>

<span data-ttu-id="c0384-144">Ziele können für Vertex-Shader, Pixel-Shader und Textur Füll Funktionen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c0384-144">Targets can be specified for vertex shaders, pixel shaders, and texture fill functions.</span></span>



|                       |                                                                       |
|-----------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="c0384-145">Vertex-Shader-Ziele</span><span class="sxs-lookup"><span data-stu-id="c0384-145">Vertex shader targets</span></span> | <span data-ttu-id="c0384-146">vs \_ 1 \_ 1, vs \_ 2 \_ 0, vs \_ 2 \_ SW, vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c0384-146">vs\_1\_1, vs\_2\_0, vs\_2\_sw, vs\_3\_0</span></span>                               |
| <span data-ttu-id="c0384-147">Pixel-Shader-Ziele</span><span class="sxs-lookup"><span data-stu-id="c0384-147">Pixel shader targets</span></span>  | <span data-ttu-id="c0384-148">PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4, PS \_ 2 \_ 0, PS \_ 2 \_ SW, PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c0384-148">ps\_1\_1, ps\_1\_2, ps\_1\_3, ps\_1\_4, ps\_2\_0, ps\_2\_sw, ps\_3\_0</span></span> |
| <span data-ttu-id="c0384-149">Textur Füll Ziele</span><span class="sxs-lookup"><span data-stu-id="c0384-149">Texture fill targets</span></span>  | <span data-ttu-id="c0384-150">TX \_ 0, TX \_ 1</span><span class="sxs-lookup"><span data-stu-id="c0384-150">tx\_0, tx\_1</span></span>                                                          |



 

<span data-ttu-id="c0384-151">Diese Methode kompiliert einen Shader aus einer Funktion, die in einer C-ähnlichen Sprache geschrieben ist.</span><span class="sxs-lookup"><span data-stu-id="c0384-151">This method compiles a shader from a function that is written in a C-like language.</span></span> <span data-ttu-id="c0384-152">Weitere Informationen finden Sie unter [HLSL](../direct3dhlsl/dx-graphics-hlsl.md).</span><span class="sxs-lookup"><span data-stu-id="c0384-152">For more information, see [HLSL](../direct3dhlsl/dx-graphics-hlsl.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0384-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c0384-153">Requirements</span></span>



| <span data-ttu-id="c0384-154">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c0384-154">Requirement</span></span> | <span data-ttu-id="c0384-155">Wert</span><span class="sxs-lookup"><span data-stu-id="c0384-155">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0384-156">Header</span><span class="sxs-lookup"><span data-stu-id="c0384-156">Header</span></span><br/>  | <dl> <span data-ttu-id="c0384-157"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0384-157"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="c0384-158">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c0384-158">Library</span></span><br/> | <dl> <span data-ttu-id="c0384-159"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c0384-159"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c0384-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0384-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0384-161">ID3DXEffectCompiler</span><span class="sxs-lookup"><span data-stu-id="c0384-161">ID3DXEffectCompiler</span></span>](id3dxeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="c0384-162">**D3DXGetShaderConstantTable**</span><span class="sxs-lookup"><span data-stu-id="c0384-162">**D3DXGetShaderConstantTable**</span></span>](d3dxgetshaderconstanttable.md)
</dt> </dl>

 

 
