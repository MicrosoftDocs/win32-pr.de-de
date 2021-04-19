---
description: Kompilieren Sie eine Shader-Datei.
ms.assetid: 2ad6042f-3601-4f4a-9624-6319a3372355
title: D3DXCompileShaderFromFile-Funktion (D3DX9Shader. h)
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
ms.openlocfilehash: 865241142fa13ec9d34826bfe334c30b38ca78d5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353371"
---
# <a name="d3dxcompileshaderfromfile-function"></a><span data-ttu-id="5437d-103">D3DXCompileShaderFromFile-Funktion</span><span class="sxs-lookup"><span data-stu-id="5437d-103">D3DXCompileShaderFromFile function</span></span>

<span data-ttu-id="5437d-104">Kompilieren Sie eine Shader-Datei.</span><span class="sxs-lookup"><span data-stu-id="5437d-104">Compile a shader file.</span></span>

> [!Note]  
> <span data-ttu-id="5437d-105">Anstatt diese Legacy Funktion zu verwenden, wird empfohlen, dass Sie die Offline Kompilierung mit dem Fxc.exe-Befehlszeilen Compiler oder der [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) -API verwenden.</span><span class="sxs-lookup"><span data-stu-id="5437d-105">Instead of using this legacy function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="5437d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5437d-106">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="5437d-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5437d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5437d-108">*psrcfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5437d-108">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5437d-109">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5437d-109">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5437d-110">Zeiger auf eine Zeichenfolge, die den Dateinamen angibt.</span><span class="sxs-lookup"><span data-stu-id="5437d-110">Pointer to a string that specifies the filename.</span></span>

</dd> <dt>

<span data-ttu-id="5437d-111">*pdefinitionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5437d-111">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5437d-112">Typ: **Konstanten [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="5437d-112">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="5437d-113">Ein optionales **null** terminiertes Array von [**D3DXMACRO**](d3dxmacro.md) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="5437d-113">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="5437d-114">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="5437d-114">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5437d-115">*pinclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5437d-115">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5437d-116">Typ: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="5437d-116">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="5437d-117">Optionaler Schnittstellen Zeiger, [**ID3DXInclude**](id3dxinclude.md), der zum Verarbeiten von include-Direktiven verwendet werden soll \# .</span><span class="sxs-lookup"><span data-stu-id="5437d-117">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="5437d-118">Wenn dieser Wert **null** ist, \# wird includes bei der Kompilierung aus einer Datei berücksichtigt, oder es wird ein Fehler ausgelöst, wenn eine Kompilierung aus einer Ressource oder einem Arbeitsspeicher erfolgt.</span><span class="sxs-lookup"><span data-stu-id="5437d-118">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="5437d-119">*pfunctionname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5437d-119">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5437d-120">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5437d-120">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5437d-121">Zeiger zur Funktion des Shader-Einstiegs Punkts, bei dem die Ausführung beginnt.</span><span class="sxs-lookup"><span data-stu-id="5437d-121">Pointer to the shader entry point function where execution begins.</span></span>

</dd> <dt>

<span data-ttu-id="5437d-122">*pprofile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5437d-122">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5437d-123">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5437d-123">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5437d-124">Zeiger auf ein Shader-Profil, das den Shader-Anweisungs Satz bestimmt.</span><span class="sxs-lookup"><span data-stu-id="5437d-124">Pointer to a shader profile which determines the shader instruction set.</span></span> <span data-ttu-id="5437d-125">Eine Liste der verfügbaren Profile finden Sie unter [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) oder [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="5437d-125">See [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) or [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) for a list of the profiles available.</span></span>

</dd> <dt>

<span data-ttu-id="5437d-126">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="5437d-126">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5437d-127">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5437d-127">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5437d-128">Kompilierungsoptionen, die durch verschiedene Flags identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="5437d-128">Compile options identified by various flags.</span></span> <span data-ttu-id="5437d-129">Der Direct3D 10 HLSL-Compiler ist nun der Standard.</span><span class="sxs-lookup"><span data-stu-id="5437d-129">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="5437d-130">Weitere Informationen finden Sie unter [D3DXSHADER-Flags](d3dxshader-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="5437d-130">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="5437d-131">*ppshader* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5437d-131">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5437d-132">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="5437d-132">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="5437d-133">Gibt einen Puffer zurück, der den erstellten Shader enthält.</span><span class="sxs-lookup"><span data-stu-id="5437d-133">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="5437d-134">Dieser Puffer enthält den kompilierten Shader-Code sowie alle eingebetteten Debug-und Symboltabellen Informationen.</span><span class="sxs-lookup"><span data-stu-id="5437d-134">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="5437d-135">*pperrormsgs* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5437d-135">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5437d-136">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="5437d-136">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="5437d-137">Gibt einen Puffer zurück, der eine Auflistung von Fehlern und Warnungen enthält, die während der Kompilierung gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="5437d-137">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="5437d-138">Dies sind die gleichen Meldungen, die der Debugger anzeigt, wenn er im Debugmodus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5437d-138">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="5437d-139">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="5437d-139">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5437d-140">*ppconstanbar* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5437d-140">*ppConstantTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5437d-141">Typ: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span><span class="sxs-lookup"><span data-stu-id="5437d-141">Type: **[**LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span></span>

<span data-ttu-id="5437d-142">Gibt eine [**ID3DXConstantTable**](id3dxconstanttable.md) -Schnittstelle zurück, die für den Zugriff auf shaderkonstanten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5437d-142">Returns an [**ID3DXConstantTable**](id3dxconstanttable.md) interface, which can be used to access shader constants.</span></span> <span data-ttu-id="5437d-143">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="5437d-143">This value can be **NULL**.</span></span> <span data-ttu-id="5437d-144">Wenn Sie die Anwendung als große Adressen unterstützen (d. h. mit der/LARGEADDRESSAWARE-Linkeroption, um Adressen zu verarbeiten, die größer als 2 GB sind), können Sie diesen Parameter nicht verwenden und müssen ihn auf **null** festlegen.</span><span class="sxs-lookup"><span data-stu-id="5437d-144">If you compile your application as large address aware (that is, you use the /LARGEADDRESSAWARE linker option to handle addresses larger than 2 GB), you cannot use this parameter and must set it to **NULL**.</span></span> <span data-ttu-id="5437d-145">Stattdessen müssen Sie die [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) -Funktion verwenden, um die in den Shader eingebettete Shader-Konstante Tabelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5437d-145">Instead, you must use the [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) function to retrieve the shader-constant table that is embedded inside the shader.</span></span> <span data-ttu-id="5437d-146">In diesem **D3DXGetShaderConstantTableEx** -Aufruf müssen Sie das Flag **D3DXCONSTTABLE \_ LARGEADDRESSAWARE** an den *Flags* -Parameter übergeben, um anzugeben, dass auf bis zu 4 GB virtuellen Adressraum zugegriffen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5437d-146">In this **D3DXGetShaderConstantTableEx** call, you must pass the **D3DXCONSTTABLE\_LARGEADDRESSAWARE** flag to the *Flags* parameter to specify to access up to 4 GB of virtual address space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5437d-147">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5437d-147">Return value</span></span>

<span data-ttu-id="5437d-148">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5437d-148">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5437d-149">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5437d-149">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5437d-150">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, e \_ notimpl, e \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="5437d-150">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_NOTIMPL, E\_OUTOFMEMORY.</span></span>

<span data-ttu-id="5437d-151">E \_ notimpl wird zurückgegeben, wenn Sie 1,1 Shader (vs \_ 1 \_ 1 und PS \_ 1 \_ 1) verwenden.</span><span class="sxs-lookup"><span data-stu-id="5437d-151">E\_NOTIMPL is returned if you're using 1.1 shaders (vs\_1\_1 and ps\_1\_1).</span></span>

## <a name="requirements"></a><span data-ttu-id="5437d-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5437d-152">Requirements</span></span>



| <span data-ttu-id="5437d-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5437d-153">Requirement</span></span> | <span data-ttu-id="5437d-154">Wert</span><span class="sxs-lookup"><span data-stu-id="5437d-154">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5437d-155">Header</span><span class="sxs-lookup"><span data-stu-id="5437d-155">Header</span></span><br/>  | <dl> <span data-ttu-id="5437d-156"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="5437d-156"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="5437d-157">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5437d-157">Library</span></span><br/> | <dl> <span data-ttu-id="5437d-158"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5437d-158"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5437d-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5437d-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5437d-160">Shaderfunktionen</span><span class="sxs-lookup"><span data-stu-id="5437d-160">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="5437d-161">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="5437d-161">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="5437d-162">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="5437d-162">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
