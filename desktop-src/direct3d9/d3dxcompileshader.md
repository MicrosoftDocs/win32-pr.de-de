---
description: Kompilieren Sie eine Shader-Datei.
ms.assetid: 9b19ab67-d5d5-482d-b3fe-ce20b64d7ad8
title: D3DXCompileShader-Funktion (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCompileShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 65dd9f74280abe7ee2fe427a4772b14b88742e97
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354727"
---
# <a name="d3dxcompileshader-function"></a><span data-ttu-id="e7e60-103">D3DXCompileShader-Funktion</span><span class="sxs-lookup"><span data-stu-id="e7e60-103">D3DXCompileShader function</span></span>

<span data-ttu-id="e7e60-104">Kompilieren Sie eine Shader-Datei.</span><span class="sxs-lookup"><span data-stu-id="e7e60-104">Compile a shader file.</span></span>

> [!Note]  
> <span data-ttu-id="e7e60-105">Anstatt diese Legacy Funktion zu verwenden, wird empfohlen, dass Sie die Offline Kompilierung mit dem Fxc.exe-Befehlszeilen Compiler oder der [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) -API verwenden.</span><span class="sxs-lookup"><span data-stu-id="e7e60-105">Instead of using this legacy function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="e7e60-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7e60-106">Syntax</span></span>


```C++
HRESULT D3DXCompileShader(
  _In_        LPCSTR              pSrcData,
  _In_        UINT                srcDataLen,
  _In_  const D3DXMACRO           *pDefines,
  _In_        LPD3DXINCLUDE       pInclude,
  _In_        LPCSTR              pFunctionName,
  _In_        LPCSTR              pProfile,
  _In_        DWORD               Flags,
  _Out_       LPD3DXBUFFER        *ppShader,
  _Out_       LPD3DXBUFFER        *ppErrorMsgs,
  _Out_       LPD3DXCONSTANTTABLE *ppConstantTable
);
```



## <a name="parameters"></a><span data-ttu-id="e7e60-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7e60-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7e60-108">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7e60-108">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7e60-109">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e7e60-109">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e7e60-110">Zeiger auf eine Zeichenfolge, die den Shader enthält.</span><span class="sxs-lookup"><span data-stu-id="e7e60-110">Pointer to a string that contains the shader.</span></span>

</dd> <dt>

<span data-ttu-id="e7e60-111">*srcdatalen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7e60-111">*srcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7e60-112">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e7e60-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e7e60-113">Länge der Daten in Bytes.</span><span class="sxs-lookup"><span data-stu-id="e7e60-113">Length of the data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e7e60-114">*pdefinitionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7e60-114">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7e60-115">Typ: **Konstanten [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="e7e60-115">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="e7e60-116">Ein optionales **null** terminiertes Array von [**D3DXMACRO**](d3dxmacro.md) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="e7e60-116">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="e7e60-117">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="e7e60-117">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e7e60-118">*pinclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7e60-118">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7e60-119">Typ: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="e7e60-119">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="e7e60-120">Optionaler Schnittstellen Zeiger, [**ID3DXInclude**](id3dxinclude.md), der zum Verarbeiten von include-Direktiven verwendet werden soll \# .</span><span class="sxs-lookup"><span data-stu-id="e7e60-120">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="e7e60-121">Wenn dieser Wert **null** ist, \# wird includes bei der Kompilierung aus einer Datei berücksichtigt, oder es wird ein Fehler ausgelöst, wenn eine Kompilierung aus einer Ressource oder einem Arbeitsspeicher erfolgt.</span><span class="sxs-lookup"><span data-stu-id="e7e60-121">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="e7e60-122">*pfunctionname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7e60-122">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7e60-123">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e7e60-123">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e7e60-124">Zeiger auf eine Zeichenfolge, die den Namen der Shader-Einstiegspunkt Funktion enthält, bei der die Ausführung beginnt.</span><span class="sxs-lookup"><span data-stu-id="e7e60-124">Pointer to a string that contains the name of the shader entry point function where execution begins.</span></span>

</dd> <dt>

<span data-ttu-id="e7e60-125">*pprofile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7e60-125">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7e60-126">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e7e60-126">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e7e60-127">Zeiger auf ein Shader-Profil, das den Shader-Anweisungs Satz bestimmt.</span><span class="sxs-lookup"><span data-stu-id="e7e60-127">Pointer to a shader profile which determines the shader instruction set.</span></span> <span data-ttu-id="e7e60-128">Eine Liste der verfügbaren Profile finden Sie unter [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) oder [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="e7e60-128">See [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) or [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) for a list of the profiles available.</span></span>

</dd> <dt>

<span data-ttu-id="e7e60-129">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="e7e60-129">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7e60-130">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e7e60-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e7e60-131">Kompilierungsoptionen, die durch verschiedene Flags identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="e7e60-131">Compile options identified by various flags.</span></span> <span data-ttu-id="e7e60-132">Der Direct3D 10 HLSL-Compiler ist nun der Standard.</span><span class="sxs-lookup"><span data-stu-id="e7e60-132">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="e7e60-133">Weitere Informationen finden Sie unter [D3DXSHADER-Flags](d3dxshader-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="e7e60-133">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="e7e60-134">*ppshader* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e7e60-134">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7e60-135">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="e7e60-135">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="e7e60-136">Gibt einen Puffer zurück, der den erstellten Shader enthält.</span><span class="sxs-lookup"><span data-stu-id="e7e60-136">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="e7e60-137">Dieser Puffer enthält den kompilierten Shader-Code sowie alle eingebetteten Debug-und Symboltabellen Informationen.</span><span class="sxs-lookup"><span data-stu-id="e7e60-137">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="e7e60-138">*pperrormsgs* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e7e60-138">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7e60-139">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="e7e60-139">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="e7e60-140">Gibt einen Puffer zurück, der eine Auflistung von Fehlern und Warnungen enthält, die während der Kompilierung gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="e7e60-140">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="e7e60-141">Dies sind die gleichen Meldungen, die der Debugger anzeigt, wenn er im Debugmodus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e7e60-141">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="e7e60-142">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="e7e60-142">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e7e60-143">*ppconstanbar* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e7e60-143">*ppConstantTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7e60-144">Typ: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span><span class="sxs-lookup"><span data-stu-id="e7e60-144">Type: **[**LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span></span>

<span data-ttu-id="e7e60-145">Gibt eine [**ID3DXConstantTable**](id3dxconstanttable.md) -Schnittstelle zurück, die für den Zugriff auf shaderkonstanten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e7e60-145">Returns an [**ID3DXConstantTable**](id3dxconstanttable.md) interface, which can be used to access shader constants.</span></span> <span data-ttu-id="e7e60-146">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="e7e60-146">This value can be **NULL**.</span></span> <span data-ttu-id="e7e60-147">Wenn Sie die Anwendung als große Adressen unterstützen (d. h. mit der/LARGEADDRESSAWARE-Linkeroption, um Adressen zu verarbeiten, die größer als 2 GB sind), können Sie diesen Parameter nicht verwenden und müssen ihn auf **null** festlegen.</span><span class="sxs-lookup"><span data-stu-id="e7e60-147">If you compile your application as large address aware (that is, you use the /LARGEADDRESSAWARE linker option to handle addresses larger than 2 GB), you cannot use this parameter and must set it to **NULL**.</span></span> <span data-ttu-id="e7e60-148">Stattdessen müssen Sie die [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) -Funktion verwenden, um die in den Shader eingebettete Shader-Konstante Tabelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e7e60-148">Instead, you must use the [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) function to retrieve the shader-constant table that is embedded inside the shader.</span></span> <span data-ttu-id="e7e60-149">In diesem **D3DXGetShaderConstantTableEx** -Aufruf müssen Sie das Flag **D3DXCONSTTABLE \_ LARGEADDRESSAWARE** an den *Flags* -Parameter übergeben, um anzugeben, dass auf bis zu 4 GB virtuellen Adressraum zugegriffen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e7e60-149">In this **D3DXGetShaderConstantTableEx** call, you must pass the **D3DXCONSTTABLE\_LARGEADDRESSAWARE** flag to the *Flags* parameter to specify to access up to 4 GB of virtual address space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7e60-150">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e7e60-150">Return value</span></span>

<span data-ttu-id="e7e60-151">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e7e60-151">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e7e60-152">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e7e60-152">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e7e60-153">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="e7e60-153">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7e60-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7e60-154">Requirements</span></span>



| <span data-ttu-id="e7e60-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7e60-155">Requirement</span></span> | <span data-ttu-id="e7e60-156">Wert</span><span class="sxs-lookup"><span data-stu-id="e7e60-156">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7e60-157">Header</span><span class="sxs-lookup"><span data-stu-id="e7e60-157">Header</span></span><br/>  | <dl> <span data-ttu-id="e7e60-158"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7e60-158"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="e7e60-159">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e7e60-159">Library</span></span><br/> | <dl> <span data-ttu-id="e7e60-160"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7e60-160"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e7e60-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7e60-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7e60-162">Shaderfunktionen</span><span class="sxs-lookup"><span data-stu-id="e7e60-162">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="e7e60-163">**D3DXCompileShaderFromFile**</span><span class="sxs-lookup"><span data-stu-id="e7e60-163">**D3DXCompileShaderFromFile**</span></span>](d3dxcompileshaderfromfile.md)
</dt> <dt>

[<span data-ttu-id="e7e60-164">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="e7e60-164">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
