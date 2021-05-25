---
description: Kompiliert einen Shader aus einem Effekt, der eine oder mehrere Funktionen enthält.
ms.assetid: f34a2975-dcd5-4917-9b11-ed40583272f9
title: ID3DXEffectCompiler::CompileShader-Methode (D3DX9Effect.h)
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
ms.openlocfilehash: 3e8d1d72fccd5c4ad47d21d05ee46013860a7743
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343625"
---
# <a name="id3dxeffectcompilercompileshader-method"></a><span data-ttu-id="c45c6-103">ID3DXEffectCompiler::CompileShader-Methode</span><span class="sxs-lookup"><span data-stu-id="c45c6-103">ID3DXEffectCompiler::CompileShader method</span></span>

<span data-ttu-id="c45c6-104">Kompiliert einen Shader aus einem Effekt, der eine oder mehrere Funktionen enthält.</span><span class="sxs-lookup"><span data-stu-id="c45c6-104">Compiles a shader from an effect that contains one or more functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="c45c6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c45c6-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="c45c6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c45c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c45c6-107">*hFunction* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c45c6-107">*hFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c45c6-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="c45c6-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="c45c6-109">Eindeutiger Bezeichner für die zu kompilierende Funktion.</span><span class="sxs-lookup"><span data-stu-id="c45c6-109">Unique identifier to the function to be compiled.</span></span> <span data-ttu-id="c45c6-110">Dieser Wert darf nicht **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="c45c6-110">This value must not be **NULL**.</span></span> <span data-ttu-id="c45c6-111">Siehe [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="c45c6-111">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="c45c6-112">*pTarget* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c45c6-112">*pTarget* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c45c6-113">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c45c6-113">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c45c6-114">Zeiger auf ein Shaderprofil, das den Shader-Anweisungssatz bestimmt.</span><span class="sxs-lookup"><span data-stu-id="c45c6-114">Pointer to a shader profile which determines the shader instruction set.</span></span> <span data-ttu-id="c45c6-115">Eine Liste der verfügbaren Profile finden Sie unter [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) oder [**D3DXGetPixelShaderProfile.**](d3dxgetpixelshaderprofile.md)</span><span class="sxs-lookup"><span data-stu-id="c45c6-115">See [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) or [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) for a list of the profiles available.</span></span>

</dd> <dt>

<span data-ttu-id="c45c6-116">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="c45c6-116">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c45c6-117">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c45c6-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c45c6-118">Kompilierungsoptionen, die durch verschiedene Flags identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="c45c6-118">Compile options identified by various flags.</span></span> <span data-ttu-id="c45c6-119">Der Direct3D 10 HLSL-Compiler ist jetzt die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="c45c6-119">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="c45c6-120">Weitere Informationen finden Sie unter [D3DXSHADER-Flags.](d3dxshader-flags.md)</span><span class="sxs-lookup"><span data-stu-id="c45c6-120">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="c45c6-121">*ppShader* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="c45c6-121">*ppShader* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="c45c6-122">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="c45c6-122">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="c45c6-123">Puffer, der den kompilierten Shader enthält.</span><span class="sxs-lookup"><span data-stu-id="c45c6-123">Buffer containing the compiled shader.</span></span> <span data-ttu-id="c45c6-124">Der Compiler-Shader ist ein Array von DWORDs.</span><span class="sxs-lookup"><span data-stu-id="c45c6-124">The compiler shader is an array of DWORDs.</span></span> <span data-ttu-id="c45c6-125">Weitere Informationen zum Zugreifen auf den Puffer finden Sie unter [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="c45c6-125">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="c45c6-126">*ppErrorMsgs* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="c45c6-126">*ppErrorMsgs* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="c45c6-127">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="c45c6-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="c45c6-128">Puffer, der mindestens die erste aufgetretene Kompilierfehlermeldung enthält.</span><span class="sxs-lookup"><span data-stu-id="c45c6-128">Buffer containing at least the first compile error message that occurred.</span></span> <span data-ttu-id="c45c6-129">Dies schließt Auswirkungencompilerfehler und Fehler bei der Sprachcompilierung auf hoher Ebene ein.</span><span class="sxs-lookup"><span data-stu-id="c45c6-129">This includes effect compiler errors and high-level language compile errors.</span></span> <span data-ttu-id="c45c6-130">Weitere Informationen zum Zugreifen auf den Puffer finden Sie unter [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="c45c6-130">For more information about accessing the buffer, see [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> <dt>

<span data-ttu-id="c45c6-131">*ppConstantTable* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c45c6-131">*ppConstantTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c45c6-132">Typ: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span><span class="sxs-lookup"><span data-stu-id="c45c6-132">Type: **[**LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span></span>

<span data-ttu-id="c45c6-133">Gibt eine [**ID3DXConstantTable-Schnittstelle**](id3dxconstanttable.md) zurück, die für den Zugriff auf Shaderkonstanten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c45c6-133">Returns an [**ID3DXConstantTable**](id3dxconstanttable.md) interface, which can be used to access shader constants.</span></span> <span data-ttu-id="c45c6-134">Dieser Wert kann NULL **sein.**</span><span class="sxs-lookup"><span data-stu-id="c45c6-134">This value can be **NULL**.</span></span> <span data-ttu-id="c45c6-135">Wenn Sie Ihre Anwendung als große Adressierung kompilieren (d. h., Sie verwenden die Linkeroption /LARGEADDRESSAWARE, um Adressen zu verarbeiten, die größer als 2 GB sind), können Sie diesen Parameter nicht verwenden und müssen ihn auf **NULL festlegen.**</span><span class="sxs-lookup"><span data-stu-id="c45c6-135">If you compile your application as large address aware (that is, you use the /LARGEADDRESSAWARE linker option to handle addresses larger than 2 GB), you cannot use this parameter and must set it to **NULL**.</span></span> <span data-ttu-id="c45c6-136">Stattdessen müssen Sie die [**D3DXGetShaderConstantTableEx-Funktion**](d3dxgetshaderconstanttableex.md) verwenden, um die shaderkonstante Tabelle abzurufen, die in den Shader eingebettet ist.</span><span class="sxs-lookup"><span data-stu-id="c45c6-136">Instead, you must use the [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) function to retrieve the shader-constant table that is embedded inside the shader.</span></span> <span data-ttu-id="c45c6-137">In diesem **D3DXGetShaderConstantTableEx-Aufruf** müssen Sie das **D3DXCONSTTABLE \_ LARGEADDRESSAWARE-Flag** an den *Flags-Parameter* übergeben, um den Zugriff auf bis zu 4 GB virtuellen Adressraum anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c45c6-137">In this **D3DXGetShaderConstantTableEx** call, you must pass the **D3DXCONSTTABLE\_LARGEADDRESSAWARE** flag to the *Flags* parameter to specify to access up to 4 GB of virtual address space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c45c6-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c45c6-138">Return value</span></span>

<span data-ttu-id="c45c6-139">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c45c6-139">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c45c6-140">Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c45c6-140">If the method succeeds, the return value is S\_OK.</span></span>

<span data-ttu-id="c45c6-141">Wenn die Argumente ungültig sind, gibt die Methode D3DERR \_ INVALIDCALL zurück.</span><span class="sxs-lookup"><span data-stu-id="c45c6-141">If the arguments are invalid, the method will return D3DERR\_INVALIDCALL.</span></span>

<span data-ttu-id="c45c6-142">Wenn bei der Methode ein Fehler auftritt, ist der Rückgabewert E \_ FAIL.</span><span class="sxs-lookup"><span data-stu-id="c45c6-142">If the method fails, the return value will be E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c45c6-143">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c45c6-143">Remarks</span></span>

<span data-ttu-id="c45c6-144">Ziele können für Vertex-Shader, Pixel-Shader und Texturfüllfunktionen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c45c6-144">Targets can be specified for vertex shaders, pixel shaders, and texture fill functions.</span></span>



| <span data-ttu-id="c45c6-145">Ziele</span><span class="sxs-lookup"><span data-stu-id="c45c6-145">Targets</span></span>                      | <span data-ttu-id="c45c6-146">Functions</span><span class="sxs-lookup"><span data-stu-id="c45c6-146">Functions</span></span>                                                                      |
|-----------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="c45c6-147">Vertex-Shaderziele</span><span class="sxs-lookup"><span data-stu-id="c45c6-147">Vertex shader targets</span></span> | <span data-ttu-id="c45c6-148">Vs \_ 1 \_ 1, vs \_ 2 \_ 0, vs \_ 2 \_ sw, vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c45c6-148">vs\_1\_1, vs\_2\_0, vs\_2\_sw, vs\_3\_0</span></span>                               |
| <span data-ttu-id="c45c6-149">Pixel-Shaderziele</span><span class="sxs-lookup"><span data-stu-id="c45c6-149">Pixel shader targets</span></span>  | <span data-ttu-id="c45c6-150">ps \_ 1 \_ 1, ps \_ 1 \_ 2, ps \_ 1 \_ 3, ps \_ 1 \_ 4, ps \_ 2 \_ 0, ps \_ 2 \_ sw, ps \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c45c6-150">ps\_1\_1, ps\_1\_2, ps\_1\_3, ps\_1\_4, ps\_2\_0, ps\_2\_sw, ps\_3\_0</span></span> |
| <span data-ttu-id="c45c6-151">Texturfüllziele</span><span class="sxs-lookup"><span data-stu-id="c45c6-151">Texture fill targets</span></span>  | <span data-ttu-id="c45c6-152">tx \_ 0, tx \_ 1</span><span class="sxs-lookup"><span data-stu-id="c45c6-152">tx\_0, tx\_1</span></span>                                                          |



 

<span data-ttu-id="c45c6-153">Diese Methode kompiliert einen Shader aus einer Funktion, die in einer C-ähnlichen Sprache geschrieben ist.</span><span class="sxs-lookup"><span data-stu-id="c45c6-153">This method compiles a shader from a function that is written in a C-like language.</span></span> <span data-ttu-id="c45c6-154">Weitere Informationen finden Sie unter [HLSL](../direct3dhlsl/dx-graphics-hlsl.md).</span><span class="sxs-lookup"><span data-stu-id="c45c6-154">For more information, see [HLSL](../direct3dhlsl/dx-graphics-hlsl.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c45c6-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c45c6-155">Requirements</span></span>



| <span data-ttu-id="c45c6-156">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c45c6-156">Requirement</span></span> | <span data-ttu-id="c45c6-157">Wert</span><span class="sxs-lookup"><span data-stu-id="c45c6-157">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c45c6-158">Header</span><span class="sxs-lookup"><span data-stu-id="c45c6-158">Header</span></span><br/>  | <dl> <span data-ttu-id="c45c6-159"><dt>D3DX9Effect.h</dt></span><span class="sxs-lookup"><span data-stu-id="c45c6-159"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="c45c6-160">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c45c6-160">Library</span></span><br/> | <dl> <span data-ttu-id="c45c6-161"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="c45c6-161"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c45c6-162">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c45c6-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c45c6-163">ID3DXEffectCompiler</span><span class="sxs-lookup"><span data-stu-id="c45c6-163">ID3DXEffectCompiler</span></span>](id3dxeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="c45c6-164">**D3DXGetShaderConstantTable**</span><span class="sxs-lookup"><span data-stu-id="c45c6-164">**D3DXGetShaderConstantTable**</span></span>](d3dxgetshaderconstanttable.md)
</dt> </dl>

 

 
