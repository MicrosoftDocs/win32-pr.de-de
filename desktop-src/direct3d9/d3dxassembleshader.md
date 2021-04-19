---
description: Assemblieren Sie einen Shader.
ms.assetid: 24c3dcae-9397-4856-b072-0ae340157bf9
title: D3DXAssembleShader-Funktion (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXAssembleShader
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f7268d394021c7dc1be665f8ed8781a827d1fcdb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370437"
---
# <a name="d3dxassembleshader-function"></a><span data-ttu-id="e78c6-103">D3DXAssembleShader-Funktion</span><span class="sxs-lookup"><span data-stu-id="e78c6-103">D3DXAssembleShader function</span></span>

<span data-ttu-id="e78c6-104">Assemblieren Sie einen Shader.</span><span class="sxs-lookup"><span data-stu-id="e78c6-104">Assemble a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="e78c6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e78c6-105">Syntax</span></span>


```C++
HRESULT D3DXAssembleShader(
  _In_        LPCSTR        pSrcData,
  _In_        UINT          SrcDataLen,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _In_        DWORD         Flags,
  _Out_       LPD3DXBUFFER  *ppShader,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="e78c6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e78c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e78c6-107">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e78c6-107">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e78c6-108">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e78c6-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e78c6-109">Zeiger auf einen Arbeitsspeicher Puffer, der die Shader-Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="e78c6-109">Pointer to a memory buffer that contains the shader data.</span></span>

</dd> <dt>

<span data-ttu-id="e78c6-110">*Srcdatalen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e78c6-110">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e78c6-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e78c6-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e78c6-112">Länge der Effekt Daten in Bytes.</span><span class="sxs-lookup"><span data-stu-id="e78c6-112">Length of the effect data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e78c6-113">*pdefinitionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e78c6-113">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e78c6-114">Typ: **Konstanten [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="e78c6-114">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="e78c6-115">Ein optionales **null** terminiertes Array von [**D3DXMACRO**](d3dxmacro.md) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="e78c6-115">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="e78c6-116">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="e78c6-116">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e78c6-117">*pinclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e78c6-117">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e78c6-118">Typ: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="e78c6-118">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="e78c6-119">Optionaler Schnittstellen Zeiger, [**ID3DXInclude**](id3dxinclude.md), der zum Verarbeiten von include-Direktiven verwendet werden soll \# .</span><span class="sxs-lookup"><span data-stu-id="e78c6-119">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="e78c6-120">Wenn dieser Wert **null** ist, \# wird includes bei der Kompilierung aus einer Datei berücksichtigt, oder es wird ein Fehler ausgelöst, wenn eine Kompilierung aus einer Ressource oder einem Arbeitsspeicher erfolgt.</span><span class="sxs-lookup"><span data-stu-id="e78c6-120">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="e78c6-121">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="e78c6-121">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e78c6-122">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e78c6-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e78c6-123">Kompilierungsoptionen, die durch verschiedene Flags identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="e78c6-123">Compile options identified by various flags.</span></span> <span data-ttu-id="e78c6-124">Der Direct3D 10 HLSL-Compiler ist nun der Standard.</span><span class="sxs-lookup"><span data-stu-id="e78c6-124">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="e78c6-125">Weitere Informationen finden Sie unter [D3DXSHADER-Flags](d3dxshader-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="e78c6-125">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="e78c6-126">*ppshader* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e78c6-126">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e78c6-127">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="e78c6-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="e78c6-128">Gibt einen Puffer zurück, der den erstellten Shader enthält.</span><span class="sxs-lookup"><span data-stu-id="e78c6-128">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="e78c6-129">Dieser Puffer enthält den kompilierten Shader-Code sowie alle eingebetteten Debug-und Symboltabellen Informationen.</span><span class="sxs-lookup"><span data-stu-id="e78c6-129">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="e78c6-130">*pperrormsgs* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e78c6-130">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e78c6-131">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="e78c6-131">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="e78c6-132">Gibt einen Puffer zurück, der eine Auflistung von Fehlern und Warnungen enthält, die während der Kompilierung gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="e78c6-132">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="e78c6-133">Dies sind die gleichen Meldungen, die der Debugger anzeigt, wenn er im Debugmodus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e78c6-133">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="e78c6-134">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="e78c6-134">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e78c6-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e78c6-135">Return value</span></span>

<span data-ttu-id="e78c6-136">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e78c6-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e78c6-137">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e78c6-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e78c6-138">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="e78c6-138">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="e78c6-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e78c6-139">Requirements</span></span>



| <span data-ttu-id="e78c6-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e78c6-140">Requirement</span></span> | <span data-ttu-id="e78c6-141">Wert</span><span class="sxs-lookup"><span data-stu-id="e78c6-141">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e78c6-142">Header</span><span class="sxs-lookup"><span data-stu-id="e78c6-142">Header</span></span><br/>  | <dl> <span data-ttu-id="e78c6-143"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="e78c6-143"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="e78c6-144">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e78c6-144">Library</span></span><br/> | <dl> <span data-ttu-id="e78c6-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e78c6-145"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e78c6-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e78c6-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e78c6-147">Shaderfunktionen</span><span class="sxs-lookup"><span data-stu-id="e78c6-147">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="e78c6-148">**D3DXAssembleShaderFromFile**</span><span class="sxs-lookup"><span data-stu-id="e78c6-148">**D3DXAssembleShaderFromFile**</span></span>](d3dxassembleshaderfromfile.md)
</dt> <dt>

[<span data-ttu-id="e78c6-149">**D3DXAssembleShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="e78c6-149">**D3DXAssembleShaderFromResource**</span></span>](d3dxassembleshaderfromresource.md)
</dt> </dl>

 

 
