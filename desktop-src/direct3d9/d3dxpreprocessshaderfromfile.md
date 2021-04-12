---
description: Führt eine Vorverarbeitung einer shaderdatei ohne Kompilierung durch. Dadurch werden alle \# Definitionen und \# includes aufgelöst, und es wird ein eigenständiger Shader für die nachfolgende Kompilierung bereitgestellt.
ms.assetid: 1be68cc0-b4a3-41b4-b956-b96ed439be9e
title: D3DXPreprocessShaderFromFile-Funktion (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPreprocessShaderFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1ba9cf35418bbbe6fe4b39341031fd1e056b27dd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354777"
---
# <a name="d3dxpreprocessshaderfromfile-function"></a><span data-ttu-id="628c8-104">D3DXPreprocessShaderFromFile-Funktion</span><span class="sxs-lookup"><span data-stu-id="628c8-104">D3DXPreprocessShaderFromFile function</span></span>

<span data-ttu-id="628c8-105">Führt eine Vorverarbeitung einer shaderdatei ohne Kompilierung durch.</span><span class="sxs-lookup"><span data-stu-id="628c8-105">Preprocesses a shader file without performing compilation.</span></span> <span data-ttu-id="628c8-106">Dadurch werden alle \# Definitionen und \# includes aufgelöst, und es wird ein eigenständiger Shader für die nachfolgende Kompilierung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="628c8-106">This resolves all \#defines and \#includes, providing a self-contained shader for subsequent compilation.</span></span>

> [!Note]  
> <span data-ttu-id="628c8-107">Anstatt diese Legacy Funktion zu verwenden, empfiehlt es sich, die [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) -API zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="628c8-107">Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="628c8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="628c8-108">Syntax</span></span>


```C++
HRESULT D3DXPreprocessShaderFromFile(
  _In_        LPCSTR        pSrcFile,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _Out_       LPD3DXBUFFER  *ppShaderText,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="628c8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="628c8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="628c8-110">*psrcfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="628c8-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="628c8-111">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="628c8-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="628c8-112">Ein Zeiger auf eine Zeichenfolge, die den Dateinamen des Shaders angibt.</span><span class="sxs-lookup"><span data-stu-id="628c8-112">Pointer to a string that specifies the filename of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="628c8-113">*pdefinitionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="628c8-113">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="628c8-114">Typ: **Konstanten [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="628c8-114">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="628c8-115">Ein optionales **null** terminiertes Array von [**D3DXMACRO**](d3dxmacro.md) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="628c8-115">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="628c8-116">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="628c8-116">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="628c8-117">*pinclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="628c8-117">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="628c8-118">Typ: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="628c8-118">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="628c8-119">Optionaler Schnittstellen Zeiger, [**ID3DXInclude**](id3dxinclude.md), der zum Verarbeiten von include-Direktiven verwendet werden soll \# .</span><span class="sxs-lookup"><span data-stu-id="628c8-119">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="628c8-120">Wenn dieser Wert **null** ist, \# wird includes bei der Kompilierung aus einer Datei berücksichtigt, oder es wird ein Fehler ausgelöst, wenn eine Kompilierung aus einer Ressource oder einem Arbeitsspeicher erfolgt.</span><span class="sxs-lookup"><span data-stu-id="628c8-120">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="628c8-121">*ppshadertext* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="628c8-121">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="628c8-122">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="628c8-122">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="628c8-123">Gibt einen Puffer mit einer einzelnen großen Zeichenfolge zurück, die den resultierenden formatierten Tokenstream darstellt.</span><span class="sxs-lookup"><span data-stu-id="628c8-123">Returns a buffer containing a single large string that represents the resulting formatted token stream.</span></span>

</dd> <dt>

<span data-ttu-id="628c8-124">*pperrormsgs* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="628c8-124">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="628c8-125">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="628c8-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="628c8-126">Gibt einen Puffer zurück, der eine Auflistung von Fehlern und Warnungen enthält, die während der Kompilierung gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="628c8-126">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="628c8-127">Dies sind die gleichen Meldungen, die der Debugger anzeigt, wenn er im Debugmodus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="628c8-127">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="628c8-128">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="628c8-128">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="628c8-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="628c8-129">Return value</span></span>

<span data-ttu-id="628c8-130">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="628c8-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="628c8-131">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="628c8-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="628c8-132">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="628c8-132">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="628c8-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="628c8-133">Requirements</span></span>



| <span data-ttu-id="628c8-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="628c8-134">Requirement</span></span> | <span data-ttu-id="628c8-135">Wert</span><span class="sxs-lookup"><span data-stu-id="628c8-135">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="628c8-136">Header</span><span class="sxs-lookup"><span data-stu-id="628c8-136">Header</span></span><br/>  | <dl> <span data-ttu-id="628c8-137"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="628c8-137"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="628c8-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="628c8-138">Library</span></span><br/> | <dl> <span data-ttu-id="628c8-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="628c8-139"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="628c8-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="628c8-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="628c8-141">Shaderfunktionen</span><span class="sxs-lookup"><span data-stu-id="628c8-141">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="628c8-142">**D3DXPreprocessShader**</span><span class="sxs-lookup"><span data-stu-id="628c8-142">**D3DXPreprocessShader**</span></span>](d3dxpreprocessshader.md)
</dt> <dt>

[<span data-ttu-id="628c8-143">**D3DXPreprocessShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="628c8-143">**D3DXPreprocessShaderFromResource**</span></span>](d3dxpreprocessshaderfromresource.md)
</dt> </dl>

 

 
