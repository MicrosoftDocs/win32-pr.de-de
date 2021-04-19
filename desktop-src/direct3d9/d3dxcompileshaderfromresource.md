---
description: Kompilieren Sie eine Shader-Datei.
ms.assetid: e944ae61-0c27-4795-8381-0ec9b3d8c3f4
title: D3DXCompileShaderFromResource-Funktion (D3DX9Shader. h)
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
ms.openlocfilehash: e1bbb48fa2932eecb82c1c45d303d7afb948fa4d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373523"
---
# <a name="d3dxcompileshaderfromresource-function"></a><span data-ttu-id="82b73-103">D3DXCompileShaderFromResource-Funktion</span><span class="sxs-lookup"><span data-stu-id="82b73-103">D3DXCompileShaderFromResource function</span></span>

<span data-ttu-id="82b73-104">Kompilieren Sie eine Shader-Datei.</span><span class="sxs-lookup"><span data-stu-id="82b73-104">Compile a shader file.</span></span>

> [!Note]  
> <span data-ttu-id="82b73-105">Anstatt diese Legacy Funktion zu verwenden, wird empfohlen, dass Sie die Offline Kompilierung mit dem Fxc.exe-Befehlszeilen Compiler oder der [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) -API verwenden.</span><span class="sxs-lookup"><span data-stu-id="82b73-105">Instead of using this legacy function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use the [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="82b73-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="82b73-106">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="82b73-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="82b73-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82b73-108">*hsrcmodule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="82b73-108">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82b73-109">Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82b73-109">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="82b73-110">Handle für ein Modul, das die Beschreibung des Effekts enthält.</span><span class="sxs-lookup"><span data-stu-id="82b73-110">Handle to a module containing the effect description.</span></span> <span data-ttu-id="82b73-111">Wenn dieser Parameter **null** ist, wird das aktuelle Modul verwendet.</span><span class="sxs-lookup"><span data-stu-id="82b73-111">If this parameter is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="82b73-112">*psrkresource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="82b73-112">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82b73-113">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82b73-113">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="82b73-114">Zeiger auf eine Zeichenfolge, die den Ressourcennamen angibt.</span><span class="sxs-lookup"><span data-stu-id="82b73-114">Pointer to a string that specifies the resource name.</span></span>

</dd> <dt>

<span data-ttu-id="82b73-115">*pdefinitionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="82b73-115">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82b73-116">Typ: **Konstanten [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="82b73-116">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="82b73-117">Ein optionales **null** terminiertes Array von [**D3DXMACRO**](d3dxmacro.md) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="82b73-117">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="82b73-118">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="82b73-118">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="82b73-119">*pinclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="82b73-119">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82b73-120">Typ: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="82b73-120">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="82b73-121">Optionaler Schnittstellen Zeiger, [**ID3DXInclude**](id3dxinclude.md), der zum Verarbeiten von include-Direktiven verwendet werden soll \# .</span><span class="sxs-lookup"><span data-stu-id="82b73-121">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="82b73-122">Wenn dieser Wert **null** ist, \# wird includes bei der Kompilierung aus einer Datei berücksichtigt, oder bei der Kompilierung aus einer Ressource oder einem Arbeitsspeicher wird ein Fehler ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="82b73-122">If this value is **NULL**, \#includes will either be honored when compiling from a file, or will error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="82b73-123">*pfunctionname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="82b73-123">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82b73-124">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82b73-124">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="82b73-125">Zeiger zur Funktion des Shader-Einstiegs Punkts, bei dem die Ausführung beginnt.</span><span class="sxs-lookup"><span data-stu-id="82b73-125">Pointer to the shader entry point function where execution begins.</span></span>

</dd> <dt>

<span data-ttu-id="82b73-126">*pprofile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="82b73-126">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82b73-127">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82b73-127">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="82b73-128">Zeiger auf ein Shader-Profil, das den Shader-Anweisungs Satz bestimmt.</span><span class="sxs-lookup"><span data-stu-id="82b73-128">Pointer to a shader profile which determines the shader instruction set.</span></span> <span data-ttu-id="82b73-129">Eine Liste der verfügbaren Profile finden Sie unter [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) oder [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="82b73-129">See [**D3DXGetVertexShaderProfile**](d3dxgetvertexshaderprofile.md) or [**D3DXGetPixelShaderProfile**](d3dxgetpixelshaderprofile.md) for a list of the profiles available.</span></span>

</dd> <dt>

<span data-ttu-id="82b73-130">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="82b73-130">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82b73-131">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="82b73-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="82b73-132">Kompilierungsoptionen, die durch verschiedene Flags identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="82b73-132">Compile options identified by various flags.</span></span> <span data-ttu-id="82b73-133">Der Direct3D 10 HLSL-Compiler ist nun der Standard.</span><span class="sxs-lookup"><span data-stu-id="82b73-133">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="82b73-134">Weitere Informationen finden Sie unter [D3DXSHADER-Flags](d3dxshader-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="82b73-134">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="82b73-135">*ppshader* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="82b73-135">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82b73-136">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="82b73-136">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="82b73-137">Gibt einen Puffer zurück, der den erstellten Shader enthält.</span><span class="sxs-lookup"><span data-stu-id="82b73-137">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="82b73-138">Dieser Puffer enthält den kompilierten Shader-Code sowie alle eingebetteten Debug-und Symboltabellen Informationen.</span><span class="sxs-lookup"><span data-stu-id="82b73-138">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="82b73-139">*pperrormsgs* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="82b73-139">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82b73-140">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="82b73-140">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="82b73-141">Gibt einen Puffer zurück, der eine Auflistung von Fehlern und Warnungen enthält, die während der Kompilierung gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="82b73-141">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="82b73-142">Dies sind die gleichen Meldungen, die der Debugger anzeigt, wenn er im Debugmodus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="82b73-142">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="82b73-143">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="82b73-143">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="82b73-144">*ppconstanbar* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="82b73-144">*ppConstantTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82b73-145">Typ: **[ **LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span><span class="sxs-lookup"><span data-stu-id="82b73-145">Type: **[**LPD3DXCONSTANTTABLE**](id3dxconstanttable.md)\***</span></span>

<span data-ttu-id="82b73-146">Gibt eine [**ID3DXConstantTable**](id3dxconstanttable.md) -Schnittstelle zurück, die für den Zugriff auf shaderkonstanten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="82b73-146">Returns an [**ID3DXConstantTable**](id3dxconstanttable.md) interface, which can be used to access shader constants.</span></span> <span data-ttu-id="82b73-147">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="82b73-147">This value can be **NULL**.</span></span> <span data-ttu-id="82b73-148">Wenn Sie die Anwendung als große Adressen unterstützen (d. h. mit der/LARGEADDRESSAWARE-Linkeroption, um Adressen zu verarbeiten, die größer als 2 GB sind), können Sie diesen Parameter nicht verwenden und müssen ihn auf **null** festlegen.</span><span class="sxs-lookup"><span data-stu-id="82b73-148">If you compile your application as large address aware (that is, you use the /LARGEADDRESSAWARE linker option to handle addresses larger than 2 GB), you cannot use this parameter and must set it to **NULL**.</span></span> <span data-ttu-id="82b73-149">Stattdessen müssen Sie die [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) -Funktion verwenden, um die in den Shader eingebettete Shader-Konstante Tabelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="82b73-149">Instead, you must use the [**D3DXGetShaderConstantTableEx**](d3dxgetshaderconstanttableex.md) function to retrieve the shader-constant table that is embedded inside the shader.</span></span> <span data-ttu-id="82b73-150">In diesem **D3DXGetShaderConstantTableEx** -Aufruf müssen Sie das Flag **D3DXCONSTTABLE \_ LARGEADDRESSAWARE** an den *Flags* -Parameter übergeben, um anzugeben, dass auf bis zu 4 GB virtuellen Adressraum zugegriffen werden soll.</span><span class="sxs-lookup"><span data-stu-id="82b73-150">In this **D3DXGetShaderConstantTableEx** call, you must pass the **D3DXCONSTTABLE\_LARGEADDRESSAWARE** flag to the *Flags* parameter to specify to access up to 4 GB of virtual address space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82b73-151">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="82b73-151">Return value</span></span>

<span data-ttu-id="82b73-152">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="82b73-152">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="82b73-153">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="82b73-153">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="82b73-154">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="82b73-154">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="82b73-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="82b73-155">Requirements</span></span>



| <span data-ttu-id="82b73-156">Anforderung</span><span class="sxs-lookup"><span data-stu-id="82b73-156">Requirement</span></span> | <span data-ttu-id="82b73-157">Wert</span><span class="sxs-lookup"><span data-stu-id="82b73-157">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="82b73-158">Header</span><span class="sxs-lookup"><span data-stu-id="82b73-158">Header</span></span><br/>  | <dl> <span data-ttu-id="82b73-159"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="82b73-159"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="82b73-160">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="82b73-160">Library</span></span><br/> | <dl> <span data-ttu-id="82b73-161"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="82b73-161"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="82b73-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82b73-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82b73-163">Shaderfunktionen</span><span class="sxs-lookup"><span data-stu-id="82b73-163">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="82b73-164">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="82b73-164">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="82b73-165">**D3DXCompileShaderFromFile**</span><span class="sxs-lookup"><span data-stu-id="82b73-165">**D3DXCompileShaderFromFile**</span></span>](d3dxcompileshaderfromfile.md)
</dt> </dl>

 

 
