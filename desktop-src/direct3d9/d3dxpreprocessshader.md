---
description: Führt einen Shader vor, ohne eine Kompilierung auszuführen. Dadurch werden alle \# Definitionen und \# includes aufgelöst, und es wird ein eigenständiger Shader für die nachfolgende Kompilierung bereitgestellt.
ms.assetid: d91258ed-6206-487a-aa81-e7c2bcea21ea
title: D3DXPreprocessShader-Funktion (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPreprocessShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 042cebe4e678ac1715a37ec3425ec0f21561797c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530854"
---
# <a name="d3dxpreprocessshader-function"></a><span data-ttu-id="59d70-104">D3DXPreprocessShader-Funktion</span><span class="sxs-lookup"><span data-stu-id="59d70-104">D3DXPreprocessShader function</span></span>

<span data-ttu-id="59d70-105">Führt einen Shader vor, ohne eine Kompilierung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="59d70-105">Preprocesses a shader without performing compilation.</span></span> <span data-ttu-id="59d70-106">Dadurch werden alle \# Definitionen und \# includes aufgelöst, und es wird ein eigenständiger Shader für die nachfolgende Kompilierung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="59d70-106">This resolves all \#defines and \#includes, providing a self-contained shader for subsequent compilation.</span></span>

> [!Note]  
> <span data-ttu-id="59d70-107">Anstatt diese Legacy Funktion zu verwenden, empfiehlt es sich, die [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) -API zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="59d70-107">Instead of using this legacy function, we recommend that you use the [**D3DPreprocess**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess) API.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="59d70-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="59d70-108">Syntax</span></span>


```C++
HRESULT D3DXPreprocessShader(
  _In_        LPCSTR        pSrcData,
  _In_        UINT          SrcDataSize,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _Out_       LPD3DXBUFFER  *ppShaderText,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="59d70-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="59d70-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59d70-110">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59d70-110">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59d70-111">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="59d70-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="59d70-112">Zeiger auf eine Zeichenfolge, die den Shader enthält.</span><span class="sxs-lookup"><span data-stu-id="59d70-112">Pointer to a string that contains the shader.</span></span>

</dd> <dt>

<span data-ttu-id="59d70-113">*Srcdatasize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59d70-113">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59d70-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="59d70-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="59d70-115">Länge der Daten in Bytes.</span><span class="sxs-lookup"><span data-stu-id="59d70-115">Length of the data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="59d70-116">*pdefinitionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59d70-116">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59d70-117">Typ: **Konstanten [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="59d70-117">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="59d70-118">Ein optionales **null** terminiertes Array von [**D3DXMACRO**](d3dxmacro.md) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="59d70-118">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="59d70-119">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="59d70-119">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="59d70-120">*pinclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59d70-120">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59d70-121">Typ: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="59d70-121">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="59d70-122">Optionaler Schnittstellen Zeiger, [**ID3DXInclude**](id3dxinclude.md), der zum Verarbeiten von include-Direktiven verwendet werden soll \# .</span><span class="sxs-lookup"><span data-stu-id="59d70-122">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="59d70-123">Wenn dieser Wert **null** ist, \# wird includes bei der Kompilierung aus einer Datei berücksichtigt, oder es wird ein Fehler ausgelöst, wenn eine Kompilierung aus einer Ressource oder einem Arbeitsspeicher erfolgt.</span><span class="sxs-lookup"><span data-stu-id="59d70-123">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="59d70-124">*ppshadertext* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="59d70-124">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59d70-125">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="59d70-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="59d70-126">Gibt einen Puffer mit einer einzelnen großen Zeichenfolge zurück, die den resultierenden formatierten Tokenstream darstellt.</span><span class="sxs-lookup"><span data-stu-id="59d70-126">Returns a buffer containing a single large string that represents the resulting formatted token stream.</span></span>

</dd> <dt>

<span data-ttu-id="59d70-127">*pperrormsgs* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="59d70-127">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59d70-128">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="59d70-128">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="59d70-129">Gibt einen Puffer zurück, der eine Auflistung von Fehlern und Warnungen enthält, die während der Kompilierung gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="59d70-129">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="59d70-130">Dies sind die gleichen Meldungen, die der Debugger anzeigt, wenn er im Debugmodus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="59d70-130">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="59d70-131">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="59d70-131">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59d70-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="59d70-132">Return value</span></span>

<span data-ttu-id="59d70-133">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="59d70-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="59d70-134">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="59d70-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="59d70-135">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="59d70-135">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="59d70-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="59d70-136">Requirements</span></span>



| <span data-ttu-id="59d70-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="59d70-137">Requirement</span></span> | <span data-ttu-id="59d70-138">Wert</span><span class="sxs-lookup"><span data-stu-id="59d70-138">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="59d70-139">Header</span><span class="sxs-lookup"><span data-stu-id="59d70-139">Header</span></span><br/>  | <dl> <span data-ttu-id="59d70-140"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="59d70-140"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="59d70-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="59d70-141">Library</span></span><br/> | <dl> <span data-ttu-id="59d70-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="59d70-142"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="59d70-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59d70-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59d70-144">Shaderfunktionen</span><span class="sxs-lookup"><span data-stu-id="59d70-144">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="59d70-145">**D3DXPreprocessShaderFromFile**</span><span class="sxs-lookup"><span data-stu-id="59d70-145">**D3DXPreprocessShaderFromFile**</span></span>](d3dxpreprocessshaderfromfile.md)
</dt> <dt>

[<span data-ttu-id="59d70-146">**D3DXPreprocessShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="59d70-146">**D3DXPreprocessShaderFromResource**</span></span>](d3dxpreprocessshaderfromresource.md)
</dt> </dl>

 

 
