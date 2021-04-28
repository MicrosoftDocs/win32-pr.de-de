---
description: 'D3DXCompileShaderFromFile-Funktion: Kompiliert eine Shaderdatei.'
ms.assetid: 2ad6042f-3601-4f4a-9624-6319a3372355
title: D3DXCompileShaderFromFile-Funktion (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCompileShaderFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a4392a3c36b31deb4071c215ad9b41e7f40c21ee
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115848"
---
# <a name="d3dxcompileshaderfromfile-function"></a><span data-ttu-id="872d2-103">D3DXCompileShaderFromFile-Funktion</span><span class="sxs-lookup"><span data-stu-id="872d2-103">D3DXCompileShaderFromFile function</span></span>

<span data-ttu-id="872d2-104">Kompilieren Sie eine Shaderdatei.</span><span class="sxs-lookup"><span data-stu-id="872d2-104">Compile a shader file.</span></span>

> [!Note]  
> <span data-ttu-id="872d2-105">Anstatt diese Legacyfunktion zu verwenden, empfiehlt es sich, offline zu kompilieren, indem Fxc.exe Befehlszeilencompiler oder die [**D3DCompile-API**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="872d2-105">Instead of using this legacy function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="872d2-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="872d2-106">Syntax</span></span>


```C++
HRESULT D3DXCompileShaderFromFile(
  _In_        LPCTSTR             pSrcFile,
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



## <a name="parameters"></a><span data-ttu-id="872d2-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="872d2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="872d2-108">*pSrcFile* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="872d2-108">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="872d2-109">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="872d2-109">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="872d2-110">Zeiger auf eine Zeichenfolge, die den Dateinamen angibt.</span><span class="sxs-lookup"><span data-stu-id="872d2-110">Pointer to a string that specifies the filename.</span></span>

</dd> <dt>

<span data-ttu-id="872d2-111">*pDefdefine* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="872d2-111">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="872d2-112">Typ: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="872d2-112">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="872d2-113">Ein optionales **null-terminiertes** Array [**von D3DXMACRO-Strukturen.**](d3dxmacro.md)</span><span class="sxs-lookup"><span data-stu-id="872d2-113">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="872d2-114">Dieser Wert kann NULL **sein.**</span><span class="sxs-lookup"><span data-stu-id="872d2-114">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="872d2-115">*pInclude* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="872d2-115">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="872d2-116">Typ: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="872d2-116">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="872d2-117">Optionaler Schnittstellenzeiger [**ID3DXInclude**](id3dxinclude.md), der für die Behandlung von Include-Direktiven \# verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="872d2-117">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="872d2-118">Wenn dieser Wert **NULL ist,** wird includes entweder beim Kompilieren aus einer Datei oder beim Kompilieren aus einer Ressource oder einem Arbeitsspeicher \# zu einem Fehler führen.</span><span class="sxs-lookup"><span data-stu-id="872d2-118">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="872d2-119">*pFunctionName* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="872d2-119">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="872d2-120">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="872d2-120">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="872d2-121">Zeiger auf die Shader-Einstiegspunktfunktion, an der die Ausführung beginnt.</span><span class="sxs-lookup"><span data-stu-id="872d2-121">Pointer to the shader entry point function where execution begins.</span></span>

</dd> <dt>

<span data-ttu-id="872d2-122">*pProfile* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="872d2-122">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="872d2-123">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="872d2-123">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="872d2-124">Zeiger auf ein Shaderprofil, das den Shader-Anweisungssatz bestimmt.</span><span class="sxs-lookup"><span data-stu-id="872d2-124">Pointer to a shader profile which determines the shader instruction set.</span></span> <span data-ttu-id="872d2-125">Eine Liste der verfügbaren Profile finden Sie unter [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) oder [**D3DXGetPixelShaderProfile.**](d3dxgetpixelshaderprofile.md)</span><span class="sxs-lookup"><span data-stu-id="872d2-125">See [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) or [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) for a list of the profiles available.</span></span>

</dd> <dt>

<span data-ttu-id="872d2-126">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="872d2-126">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="872d2-127">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="872d2-127">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="872d2-128">Kompilierungsoptionen, die durch verschiedene Flags identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="872d2-128">Compile options identified by various flags.</span></span> <span data-ttu-id="872d2-129">Der Direct3D 10 HLSL-Compiler ist jetzt die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="872d2-129">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="872d2-130">Weitere Informationen finden Sie unter [D3DXSHADER-Flags.](d3dxshader-flags.md)</span><span class="sxs-lookup"><span data-stu-id="872d2-130">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="872d2-131">*ppShader* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="872d2-131">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="872d2-132">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="872d2-132">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="872d2-133">Gibt einen Puffer zurück, der den erstellten Shader enthält.</span><span class="sxs-lookup"><span data-stu-id="872d2-133">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="872d2-134">Dieser Puffer enthält den kompilierten Shadercode sowie alle eingebetteten Debug- und Symboltabelleninformationen.</span><span class="sxs-lookup"><span data-stu-id="872d2-134">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="872d2-135">*ppErrorMsgs* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="872d2-135">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="872d2-136">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="872d2-136">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="872d2-137">Gibt einen Puffer zurück, der eine Liste von Fehlern und Warnungen enthält, die während der Kompilierung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="872d2-137">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="872d2-138">Dies sind die gleichen Meldungen, die der Debugger anzeigt, wenn er im Debugmodus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="872d2-138">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="872d2-139">Dieser Wert kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="872d2-139">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="872d2-140">*ppConstantTable* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="872d2-140">*ppConstantTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="872d2-141">Typ: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span><span class="sxs-lookup"><span data-stu-id="872d2-141">Type: **[**LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span></span>

<span data-ttu-id="872d2-142">Gibt eine [**ID3DXConstantTable-Schnittstelle**](id3dxconstanttable.md) zurück, die für den Zugriff auf Shaderkonstanten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="872d2-142">Returns an [**ID3DXConstantTable**](id3dxconstanttable.md) interface, which can be used to access shader constants.</span></span> <span data-ttu-id="872d2-143">Dieser Wert kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="872d2-143">This value can be **NULL**.</span></span> <span data-ttu-id="872d2-144">Wenn Sie Ihre Anwendung als große Adressierung kompilieren (d. h., Sie verwenden die Linkeroption /LARGEADDRESSAWARE, um Adressen zu verarbeiten, die größer als 2 GB sind), können Sie diesen Parameter nicht verwenden und müssen ihn auf **NULL festlegen.**</span><span class="sxs-lookup"><span data-stu-id="872d2-144">If you compile your application as large address aware (that is, you use the /LARGEADDRESSAWARE linker option to handle addresses larger than 2 GB), you cannot use this parameter and must set it to **NULL**.</span></span> <span data-ttu-id="872d2-145">Stattdessen müssen Sie die [**D3DXGetShaderConstantTableEx-Funktion**](d3dxgetshaderconstanttableex.md) verwenden, um die shaderkonstante Tabelle abzurufen, die in den Shader eingebettet ist.</span><span class="sxs-lookup"><span data-stu-id="872d2-145">Instead, you must use the [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) function to retrieve the shader-constant table that is embedded inside the shader.</span></span> <span data-ttu-id="872d2-146">In diesem **D3DXGetShaderConstantTableEx-Aufruf** müssen Sie das **D3DXCONSTTABLE \_ LARGEADDRESSAWARE-Flag** an den *Flags-Parameter* übergeben, um den Zugriff auf bis zu 4 GB virtuellen Adressraum anzugeben.</span><span class="sxs-lookup"><span data-stu-id="872d2-146">In this **D3DXGetShaderConstantTableEx** call, you must pass the **D3DXCONSTTABLE\_LARGEADDRESSAWARE** flag to the *Flags* parameter to specify to access up to 4 GB of virtual address space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="872d2-147">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="872d2-147">Return value</span></span>

<span data-ttu-id="872d2-148">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="872d2-148">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="872d2-149">Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="872d2-149">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="872d2-150">Wenn die Funktion fehlschlägt, kann der Rückgabewert wie folgt sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ NOTIMPL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="872d2-150">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_NOTIMPL, E\_OUTOFMEMORY.</span></span>

<span data-ttu-id="872d2-151">E \_ NOTIMPL wird zurückgegeben, wenn Sie 1.1-Shader verwenden (im Vergleich \_ zu 1 \_ 1 und Ps \_ 1 \_ 1).</span><span class="sxs-lookup"><span data-stu-id="872d2-151">E\_NOTIMPL is returned if you're using 1.1 shaders (vs\_1\_1 and ps\_1\_1).</span></span>

## <a name="requirements"></a><span data-ttu-id="872d2-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="872d2-152">Requirements</span></span>



| <span data-ttu-id="872d2-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="872d2-153">Requirement</span></span> | <span data-ttu-id="872d2-154">Wert</span><span class="sxs-lookup"><span data-stu-id="872d2-154">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="872d2-155">Header</span><span class="sxs-lookup"><span data-stu-id="872d2-155">Header</span></span><br/>  | <dl> <span data-ttu-id="872d2-156"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="872d2-156"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="872d2-157">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="872d2-157">Library</span></span><br/> | <dl> <span data-ttu-id="872d2-158"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="872d2-158"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="872d2-159">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="872d2-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="872d2-160">Shaderfunktionen</span><span class="sxs-lookup"><span data-stu-id="872d2-160">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="872d2-161">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="872d2-161">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="872d2-162">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="872d2-162">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
