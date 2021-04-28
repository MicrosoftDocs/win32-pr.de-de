---
description: 'D3DXCompileShaderFromResource-Funktion: Kompiliert eine Shaderdatei.'
ms.assetid: e944ae61-0c27-4795-8381-0ec9b3d8c3f4
title: D3DXCompileShaderFromResource-Funktion (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCompileShaderFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: de94754004cc42bcc6914d9513588a71a1a593dd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115808"
---
# <a name="d3dxcompileshaderfromresource-function"></a><span data-ttu-id="dc702-103">D3DXCompileShaderFromResource-Funktion</span><span class="sxs-lookup"><span data-stu-id="dc702-103">D3DXCompileShaderFromResource function</span></span>

<span data-ttu-id="dc702-104">Kompilieren Sie eine Shaderdatei.</span><span class="sxs-lookup"><span data-stu-id="dc702-104">Compile a shader file.</span></span>

> [!Note]  
> <span data-ttu-id="dc702-105">Anstatt diese Legacyfunktion zu verwenden, empfiehlt es sich, offline zu kompilieren, indem Fxc.exe Befehlszeilencompiler oder die [**D3DCompile-API**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dc702-105">Instead of using this legacy function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="dc702-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc702-106">Syntax</span></span>


```C++
HRESULT D3DXCompileShaderFromResource(
  _In_        HMODULE             hSrcModule,
  _In_        LPCSTR              pSrcResource,
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



## <a name="parameters"></a><span data-ttu-id="dc702-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc702-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc702-108">*hSrcModule* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="dc702-108">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc702-109">Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dc702-109">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dc702-110">Handle für ein Modul, das die Beschreibung des Effekts enthält.</span><span class="sxs-lookup"><span data-stu-id="dc702-110">Handle to a module containing the effect description.</span></span> <span data-ttu-id="dc702-111">Wenn dieser Parameter **NULL ist,** wird das aktuelle Modul verwendet.</span><span class="sxs-lookup"><span data-stu-id="dc702-111">If this parameter is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="dc702-112">*pSrcResource* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="dc702-112">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc702-113">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dc702-113">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dc702-114">Zeiger auf eine Zeichenfolge, die den Ressourcennamen angibt.</span><span class="sxs-lookup"><span data-stu-id="dc702-114">Pointer to a string that specifies the resource name.</span></span>

</dd> <dt>

<span data-ttu-id="dc702-115">*pDefdefine* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="dc702-115">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc702-116">Typ: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="dc702-116">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="dc702-117">Ein optionales **null-terminiertes** Array [**von D3DXMACRO-Strukturen.**](d3dxmacro.md)</span><span class="sxs-lookup"><span data-stu-id="dc702-117">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="dc702-118">Dieser Wert kann NULL **sein.**</span><span class="sxs-lookup"><span data-stu-id="dc702-118">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="dc702-119">*pInclude* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="dc702-119">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc702-120">Typ: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="dc702-120">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="dc702-121">Optionaler Schnittstellenzeiger [**ID3DXInclude**](id3dxinclude.md), der für die Behandlung von Include-Direktiven \# verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="dc702-121">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="dc702-122">Wenn dieser Wert **NULL ist,** wird includes entweder beim Kompilieren aus einer Datei oder beim Kompilieren aus einer Ressource oder einem Arbeitsspeicher \# als Fehler angesehen.</span><span class="sxs-lookup"><span data-stu-id="dc702-122">If this value is **NULL**, \#includes will either be honored when compiling from a file, or will error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="dc702-123">*pFunctionName* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="dc702-123">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc702-124">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dc702-124">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dc702-125">Zeiger auf die Shader-Einstiegspunktfunktion, bei der die Ausführung beginnt.</span><span class="sxs-lookup"><span data-stu-id="dc702-125">Pointer to the shader entry point function where execution begins.</span></span>

</dd> <dt>

<span data-ttu-id="dc702-126">*pProfile* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="dc702-126">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc702-127">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dc702-127">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dc702-128">Zeiger auf ein Shaderprofil, das den Shader-Anweisungssatz bestimmt.</span><span class="sxs-lookup"><span data-stu-id="dc702-128">Pointer to a shader profile which determines the shader instruction set.</span></span> <span data-ttu-id="dc702-129">Eine Liste der verfügbaren Profile finden Sie unter [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) oder [**D3DXGetPixelShaderProfile.**](d3dxgetpixelshaderprofile.md)</span><span class="sxs-lookup"><span data-stu-id="dc702-129">See [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) or [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) for a list of the profiles available.</span></span>

</dd> <dt>

<span data-ttu-id="dc702-130">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="dc702-130">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc702-131">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dc702-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dc702-132">Kompilierungsoptionen, die durch verschiedene Flags identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="dc702-132">Compile options identified by various flags.</span></span> <span data-ttu-id="dc702-133">Der Direct3D 10 HLSL-Compiler ist jetzt die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="dc702-133">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="dc702-134">Weitere Informationen finden Sie unter [D3DXSHADER-Flags.](d3dxshader-flags.md)</span><span class="sxs-lookup"><span data-stu-id="dc702-134">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="dc702-135">*ppShader* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dc702-135">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc702-136">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="dc702-136">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="dc702-137">Gibt einen Puffer zurück, der den erstellten Shader enthält.</span><span class="sxs-lookup"><span data-stu-id="dc702-137">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="dc702-138">Dieser Puffer enthält den kompilierten Shadercode sowie alle eingebetteten Debug- und Symboltabelleninformationen.</span><span class="sxs-lookup"><span data-stu-id="dc702-138">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="dc702-139">*ppErrorMsgs* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dc702-139">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc702-140">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="dc702-140">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="dc702-141">Gibt einen Puffer zurück, der eine Liste von Fehlern und Warnungen enthält, die während der Kompilierung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="dc702-141">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="dc702-142">Dies sind die gleichen Meldungen, die der Debugger anzeigt, wenn er im Debugmodus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dc702-142">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="dc702-143">Dieser Wert kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="dc702-143">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="dc702-144">*ppConstantTable* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dc702-144">*ppConstantTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc702-145">Typ: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span><span class="sxs-lookup"><span data-stu-id="dc702-145">Type: **[**LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span></span>

<span data-ttu-id="dc702-146">Gibt eine [**ID3DXConstantTable-Schnittstelle**](id3dxconstanttable.md) zurück, die für den Zugriff auf Shaderkonstanten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="dc702-146">Returns an [**ID3DXConstantTable**](id3dxconstanttable.md) interface, which can be used to access shader constants.</span></span> <span data-ttu-id="dc702-147">Dieser Wert kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="dc702-147">This value can be **NULL**.</span></span> <span data-ttu-id="dc702-148">Wenn Sie Ihre Anwendung als große Adressverwaltung kompilieren (d. h., Sie verwenden die Linkeroption /LARGEADDRESSAWARE, um Adressen zu verarbeiten, die größer als 2 GB sind), können Sie diesen Parameter nicht verwenden und müssen ihn auf **NULL** festlegen.</span><span class="sxs-lookup"><span data-stu-id="dc702-148">If you compile your application as large address aware (that is, you use the /LARGEADDRESSAWARE linker option to handle addresses larger than 2 GB), you cannot use this parameter and must set it to **NULL**.</span></span> <span data-ttu-id="dc702-149">Stattdessen müssen Sie die [**D3DXGetShaderConstantTableEx-Funktion**](d3dxgetshaderconstanttableex.md) verwenden, um die shaderkonstante Tabelle abzurufen, die in den Shader eingebettet ist.</span><span class="sxs-lookup"><span data-stu-id="dc702-149">Instead, you must use the [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) function to retrieve the shader-constant table that is embedded inside the shader.</span></span> <span data-ttu-id="dc702-150">In diesem **D3DXGetShaderConstantTableEx-Aufruf** müssen Sie das **Flag D3DXCONSTTABLE \_ LARGEADDRESSAWARE** an den *Flags-Parameter* übergeben, um anzugeben, dass auf bis zu 4 GB des virtuellen Adressraums zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="dc702-150">In this **D3DXGetShaderConstantTableEx** call, you must pass the **D3DXCONSTTABLE\_LARGEADDRESSAWARE** flag to the *Flags* parameter to specify to access up to 4 GB of virtual address space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc702-151">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dc702-151">Return value</span></span>

<span data-ttu-id="dc702-152">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dc702-152">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dc702-153">Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dc702-153">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="dc702-154">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="dc702-154">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc702-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dc702-155">Requirements</span></span>



| <span data-ttu-id="dc702-156">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dc702-156">Requirement</span></span> | <span data-ttu-id="dc702-157">Wert</span><span class="sxs-lookup"><span data-stu-id="dc702-157">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc702-158">Header</span><span class="sxs-lookup"><span data-stu-id="dc702-158">Header</span></span><br/>  | <dl> <span data-ttu-id="dc702-159"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="dc702-159"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="dc702-160">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dc702-160">Library</span></span><br/> | <dl> <span data-ttu-id="dc702-161"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="dc702-161"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="dc702-162">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="dc702-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc702-163">Shaderfunktionen</span><span class="sxs-lookup"><span data-stu-id="dc702-163">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="dc702-164">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="dc702-164">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="dc702-165">**D3DXCompileShaderFromFile**</span><span class="sxs-lookup"><span data-stu-id="dc702-165">**D3DXCompileShaderFromFile**</span></span>](d3dxcompileshaderfromfile.md)
</dt> </dl>

 

 
