---
description: Führt eine Vorverarbeitung einer Shaderressource ohne Kompilierung durch. Dadurch werden alle \# Definitionen und \# includes aufgelöst, und es wird ein eigenständiger Shader für die nachfolgende Kompilierung bereitgestellt.
ms.assetid: a00c2db9-d7ba-48ab-80e3-dc20774e1b1e
title: D3DXPreprocessShaderFromResource-Funktion (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPreprocessShaderFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c45073d0b84ef6fb33d378c4c18f862f55c6b84a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354656"
---
# <a name="d3dxpreprocessshaderfromresource-function"></a><span data-ttu-id="a6f84-104">D3DXPreprocessShaderFromResource-Funktion</span><span class="sxs-lookup"><span data-stu-id="a6f84-104">D3DXPreprocessShaderFromResource function</span></span>

<span data-ttu-id="a6f84-105">Führt eine Vorverarbeitung einer Shaderressource ohne Kompilierung durch.</span><span class="sxs-lookup"><span data-stu-id="a6f84-105">Preprocesses a shader resource without performing compilation.</span></span> <span data-ttu-id="a6f84-106">Dadurch werden alle \# Definitionen und \# includes aufgelöst, und es wird ein eigenständiger Shader für die nachfolgende Kompilierung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="a6f84-106">This resolves all \#defines and \#includes, providing a self-contained shader for subsequent compilation.</span></span>

> [!Note]  
> <span data-ttu-id="a6f84-107">Anstatt diese Legacy Funktion zu verwenden, empfiehlt es sich, die [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) -API zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a6f84-107">Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="a6f84-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6f84-108">Syntax</span></span>


```C++
HRESULT D3DXPreprocessShaderFromResource(
  _In_        HMODULE       hSrcModule,
  _In_        LPCSTR        pSrcResource,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _Out_       LPD3DXBUFFER  *ppShaderText,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="a6f84-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6f84-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6f84-110">*hsrcmodule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6f84-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6f84-111">Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a6f84-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a6f84-112">Handle für das Modul, das die Shader-Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="a6f84-112">Handle to the module that holds the shader resource.</span></span> <span data-ttu-id="a6f84-113">Wenn dieser Wert **null** ist, wird das aktuelle Modul verwendet.</span><span class="sxs-lookup"><span data-stu-id="a6f84-113">If this value is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="a6f84-114">*psrkresource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6f84-114">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6f84-115">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a6f84-115">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a6f84-116">Eine Zeichenfolge, die den Namen der Ressource im Modul darstellt.</span><span class="sxs-lookup"><span data-stu-id="a6f84-116">String that represents the name of the resource in the module.</span></span>

</dd> <dt>

<span data-ttu-id="a6f84-117">*pdefinitionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6f84-117">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6f84-118">Typ: **Konstanten [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="a6f84-118">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="a6f84-119">Ein optionales **null** terminiertes Array von [**D3DXMACRO**](d3dxmacro.md) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="a6f84-119">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="a6f84-120">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="a6f84-120">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a6f84-121">*pinclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6f84-121">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6f84-122">Typ: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="a6f84-122">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="a6f84-123">Optionaler Schnittstellen Zeiger, [**ID3DXInclude**](id3dxinclude.md), der zum Verarbeiten von include-Direktiven verwendet werden soll \# .</span><span class="sxs-lookup"><span data-stu-id="a6f84-123">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="a6f84-124">Wenn dieser Wert **null** ist, \# wird includes bei der Kompilierung aus einer Datei berücksichtigt, oder es wird ein Fehler ausgelöst, wenn eine Kompilierung aus einer Ressource oder einem Arbeitsspeicher erfolgt.</span><span class="sxs-lookup"><span data-stu-id="a6f84-124">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="a6f84-125">*ppshadertext* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a6f84-125">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a6f84-126">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="a6f84-126">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="a6f84-127">Gibt einen Puffer mit einer einzelnen großen Zeichenfolge zurück, die den resultierenden formatierten Tokenstream darstellt.</span><span class="sxs-lookup"><span data-stu-id="a6f84-127">Returns a buffer containing a single large string that represents the resulting formatted token stream.</span></span>

</dd> <dt>

<span data-ttu-id="a6f84-128">*pperrormsgs* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a6f84-128">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a6f84-129">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="a6f84-129">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="a6f84-130">Gibt einen Puffer zurück, der eine Auflistung von Fehlern und Warnungen enthält, die während der Kompilierung gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="a6f84-130">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="a6f84-131">Dies sind die gleichen Meldungen, die der Debugger anzeigt, wenn er im Debugmodus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a6f84-131">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="a6f84-132">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="a6f84-132">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6f84-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a6f84-133">Return value</span></span>

<span data-ttu-id="a6f84-134">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a6f84-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a6f84-135">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a6f84-135">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a6f84-136">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="a6f84-136">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6f84-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a6f84-137">Requirements</span></span>



| <span data-ttu-id="a6f84-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a6f84-138">Requirement</span></span> | <span data-ttu-id="a6f84-139">Wert</span><span class="sxs-lookup"><span data-stu-id="a6f84-139">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6f84-140">Header</span><span class="sxs-lookup"><span data-stu-id="a6f84-140">Header</span></span><br/>  | <dl> <span data-ttu-id="a6f84-141"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6f84-141"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="a6f84-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a6f84-142">Library</span></span><br/> | <dl> <span data-ttu-id="a6f84-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a6f84-143"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a6f84-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6f84-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6f84-145">Shaderfunktionen</span><span class="sxs-lookup"><span data-stu-id="a6f84-145">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="a6f84-146">**D3DXPreprocessShaderFromFile**</span><span class="sxs-lookup"><span data-stu-id="a6f84-146">**D3DXPreprocessShaderFromFile**</span></span>](d3dxpreprocessshaderfromfile.md)
</dt> <dt>

[<span data-ttu-id="a6f84-147">**D3DXPreprocessShader**</span><span class="sxs-lookup"><span data-stu-id="a6f84-147">**D3DXPreprocessShader**</span></span>](d3dxpreprocessshader.md)
</dt> </dl>

 

 
