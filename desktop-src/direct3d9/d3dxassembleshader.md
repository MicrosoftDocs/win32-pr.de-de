---
description: 'D3DXAssembleShader-Funktion: Stellt einen Shader zusammen.'
ms.assetid: 24c3dcae-9397-4856-b072-0ae340157bf9
title: D3DXAssembleShader-Funktion (D3DX9Shader.h)
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
ms.openlocfilehash: 891281ebc3db970ca61132fe49ba98531ca1d879
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116048"
---
# <a name="d3dxassembleshader-function"></a><span data-ttu-id="1d6b8-103">D3DXAssembleShader-Funktion</span><span class="sxs-lookup"><span data-stu-id="1d6b8-103">D3DXAssembleShader function</span></span>

<span data-ttu-id="1d6b8-104">Stellen Sie einen Shader zusammen.</span><span class="sxs-lookup"><span data-stu-id="1d6b8-104">Assemble a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d6b8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d6b8-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="1d6b8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d6b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d6b8-107">*pSrcData* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="1d6b8-107">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d6b8-108">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1d6b8-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1d6b8-109">Zeiger auf einen Speicherpuffer, der die Shaderdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="1d6b8-109">Pointer to a memory buffer that contains the shader data.</span></span>

</dd> <dt>

<span data-ttu-id="1d6b8-110">*SrcDataLen* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="1d6b8-110">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d6b8-111">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1d6b8-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1d6b8-112">Länge der Effektdaten in Bytes.</span><span class="sxs-lookup"><span data-stu-id="1d6b8-112">Length of the effect data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="1d6b8-113">*pDefdefine* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="1d6b8-113">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d6b8-114">Typ: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="1d6b8-114">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="1d6b8-115">Ein optionales **null-terminiertes** Array [**von D3DXMACRO-Strukturen.**](d3dxmacro.md)</span><span class="sxs-lookup"><span data-stu-id="1d6b8-115">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="1d6b8-116">Dieser Wert kann NULL **sein.**</span><span class="sxs-lookup"><span data-stu-id="1d6b8-116">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1d6b8-117">*pInclude* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="1d6b8-117">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d6b8-118">Typ: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="1d6b8-118">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="1d6b8-119">Optionaler Schnittstellenzeiger [**ID3DXInclude**](id3dxinclude.md), der für die Behandlung von Include-Direktiven \# verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1d6b8-119">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="1d6b8-120">Wenn dieser Wert **NULL ist,** wird includes entweder beim Kompilieren aus einer Datei oder beim Kompilieren aus einer Ressource oder einem Arbeitsspeicher \# zu einem Fehler führen.</span><span class="sxs-lookup"><span data-stu-id="1d6b8-120">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="1d6b8-121">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="1d6b8-121">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d6b8-122">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1d6b8-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1d6b8-123">Kompilierungsoptionen, die durch verschiedene Flags identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="1d6b8-123">Compile options identified by various flags.</span></span> <span data-ttu-id="1d6b8-124">Der Direct3D 10 HLSL-Compiler ist jetzt die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="1d6b8-124">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="1d6b8-125">Weitere Informationen finden Sie unter [D3DXSHADER-Flags.](d3dxshader-flags.md)</span><span class="sxs-lookup"><span data-stu-id="1d6b8-125">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="1d6b8-126">*ppShader* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1d6b8-126">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d6b8-127">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="1d6b8-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="1d6b8-128">Gibt einen Puffer zurück, der den erstellten Shader enthält.</span><span class="sxs-lookup"><span data-stu-id="1d6b8-128">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="1d6b8-129">Dieser Puffer enthält den kompilierten Shadercode sowie alle eingebetteten Debug- und Symboltabelleninformationen.</span><span class="sxs-lookup"><span data-stu-id="1d6b8-129">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="1d6b8-130">*ppErrorMsgs* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1d6b8-130">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d6b8-131">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="1d6b8-131">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="1d6b8-132">Gibt einen Puffer zurück, der eine Liste von Fehlern und Warnungen enthält, die während der Kompilierung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="1d6b8-132">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="1d6b8-133">Dies sind die gleichen Meldungen, die der Debugger anzeigt, wenn er im Debugmodus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1d6b8-133">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="1d6b8-134">Dieser Wert kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="1d6b8-134">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d6b8-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1d6b8-135">Return value</span></span>

<span data-ttu-id="1d6b8-136">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1d6b8-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1d6b8-137">Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1d6b8-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1d6b8-138">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="1d6b8-138">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d6b8-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d6b8-139">Requirements</span></span>



| <span data-ttu-id="1d6b8-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d6b8-140">Requirement</span></span> | <span data-ttu-id="1d6b8-141">Wert</span><span class="sxs-lookup"><span data-stu-id="1d6b8-141">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d6b8-142">Header</span><span class="sxs-lookup"><span data-stu-id="1d6b8-142">Header</span></span><br/>  | <dl> <span data-ttu-id="1d6b8-143"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="1d6b8-143"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="1d6b8-144">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1d6b8-144">Library</span></span><br/> | <dl> <span data-ttu-id="1d6b8-145"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="1d6b8-145"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="1d6b8-146">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1d6b8-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d6b8-147">Shaderfunktionen</span><span class="sxs-lookup"><span data-stu-id="1d6b8-147">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="1d6b8-148">**D3DXAssembleShaderFromFile**</span><span class="sxs-lookup"><span data-stu-id="1d6b8-148">**D3DXAssembleShaderFromFile**</span></span>](d3dxassembleshaderfromfile.md)
</dt> <dt>

[<span data-ttu-id="1d6b8-149">**D3DXAssembleShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="1d6b8-149">**D3DXAssembleShaderFromResource**</span></span>](d3dxassembleshaderfromresource.md)
</dt> </dl>

 

 
