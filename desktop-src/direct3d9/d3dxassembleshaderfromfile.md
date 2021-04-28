---
description: 'D3DXAssembleShaderFromFile-Funktion: Erstellen eines Shaders'
ms.assetid: 2977b64a-b8cc-454b-8e28-291f6f2c6fc1
title: D3DXAssembleShaderFromFile-Funktion (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXAssembleShaderFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 91aaf2924638b1db5b0e8ec0782b90fa964a9543
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116028"
---
# <a name="d3dxassembleshaderfromfile-function"></a><span data-ttu-id="c0687-103">D3DXAssembleShaderFromFile-Funktion</span><span class="sxs-lookup"><span data-stu-id="c0687-103">D3DXAssembleShaderFromFile function</span></span>

<span data-ttu-id="c0687-104">Stellen Sie einen Shader zusammen.</span><span class="sxs-lookup"><span data-stu-id="c0687-104">Assemble a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0687-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0687-105">Syntax</span></span>


```C++
HRESULT D3DXAssembleShaderFromFile(
  _In_        LPCTSTR       pSrcFile,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _In_        DWORD         Flags,
  _Out_       LPD3DXBUFFER  *ppShader,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="c0687-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0687-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0687-107">*pSrcFile* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c0687-107">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0687-108">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c0687-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c0687-109">Zeiger auf eine Zeichenfolge, die den Dateinamen angibt.</span><span class="sxs-lookup"><span data-stu-id="c0687-109">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="c0687-110">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="c0687-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="c0687-111">Andernfalls wird der Zeichenfolgendatentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="c0687-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="c0687-112">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="c0687-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="c0687-113">*pDefine* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c0687-113">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0687-114">Typ: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="c0687-114">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="c0687-115">Ein optionales auf **NULL** endendes Array von [**D3DXMACRO-Strukturen.**](d3dxmacro.md)</span><span class="sxs-lookup"><span data-stu-id="c0687-115">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="c0687-116">Dieser Wert kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="c0687-116">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c0687-117">*pInclude* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c0687-117">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0687-118">Typ: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="c0687-118">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="c0687-119">Optionaler Schnittstellenzeiger [**ID3DXInclude**](id3dxinclude.md), der für die Behandlung von \# Includedirektiven verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c0687-119">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="c0687-120">Wenn dieser Wert **NULL** ist, \# wird includes entweder beim Kompilieren aus einer Datei berücksichtigt oder verursacht bei der Kompilierung aus einer Ressource oder aus dem Arbeitsspeicher einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="c0687-120">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="c0687-121">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="c0687-121">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0687-122">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c0687-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c0687-123">Kompilierungsoptionen, die durch verschiedene Flags identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="c0687-123">Compile options identified by various flags.</span></span> <span data-ttu-id="c0687-124">Der Direct3D 10 HLSL-Compiler ist jetzt die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="c0687-124">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="c0687-125">Weitere Informationen finden Sie unter [D3DXSHADER-Flags.](d3dxshader-flags.md)</span><span class="sxs-lookup"><span data-stu-id="c0687-125">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="c0687-126">*ppShader* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c0687-126">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0687-127">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="c0687-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="c0687-128">Gibt einen Puffer zurück, der den erstellten Shader enthält.</span><span class="sxs-lookup"><span data-stu-id="c0687-128">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="c0687-129">Dieser Puffer enthält den kompilierten Shadercode sowie alle eingebetteten Debug- und Symboltabelleninformationen.</span><span class="sxs-lookup"><span data-stu-id="c0687-129">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="c0687-130">*ppErrorMsgs* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c0687-130">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0687-131">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="c0687-131">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="c0687-132">Gibt einen Puffer zurück, der eine Auflistung von Fehlern und Warnungen enthält, die während der Kompilierung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="c0687-132">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="c0687-133">Dies sind die gleichen Meldungen, die der Debugger anzeigt, wenn er im Debugmodus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c0687-133">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="c0687-134">Dieser Wert kann NULL **sein.**</span><span class="sxs-lookup"><span data-stu-id="c0687-134">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0687-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c0687-135">Return value</span></span>

<span data-ttu-id="c0687-136">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c0687-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c0687-137">Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c0687-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c0687-138">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="c0687-138">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0687-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0687-139">Remarks</span></span>

<span data-ttu-id="c0687-140">Die Compilereinstellung bestimmt auch die Funktionsversion.</span><span class="sxs-lookup"><span data-stu-id="c0687-140">The compiler setting also determines the function version.</span></span> <span data-ttu-id="c0687-141">Wenn Unicode definiert ist, wird der Funktionsaufruf in D3DXAssembleShaderFromFileW auflösen.</span><span class="sxs-lookup"><span data-stu-id="c0687-141">If Unicode is defined, the function call resolves to D3DXAssembleShaderFromFileW.</span></span> <span data-ttu-id="c0687-142">Andernfalls wird der Funktionsaufruf in D3DXAssembleShaderFromFileA auflösen, da ANSI-Zeichenfolgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c0687-142">Otherwise, the function call resolves to D3DXAssembleShaderFromFileA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0687-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c0687-143">Requirements</span></span>



| <span data-ttu-id="c0687-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c0687-144">Requirement</span></span> | <span data-ttu-id="c0687-145">Wert</span><span class="sxs-lookup"><span data-stu-id="c0687-145">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0687-146">Header</span><span class="sxs-lookup"><span data-stu-id="c0687-146">Header</span></span><br/>  | <dl> <span data-ttu-id="c0687-147"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="c0687-147"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="c0687-148">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c0687-148">Library</span></span><br/> | <dl> <span data-ttu-id="c0687-149"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="c0687-149"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c0687-150">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c0687-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0687-151">Shaderfunktionen</span><span class="sxs-lookup"><span data-stu-id="c0687-151">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="c0687-152">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="c0687-152">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="c0687-153">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="c0687-153">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
