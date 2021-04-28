---
description: 'D3DXAssembleShaderFromResource-Funktion: Assemblieren eines Shaders.'
ms.assetid: a0d31b15-db79-4aa8-afd8-fa1e20c61725
title: D3DXAssembleShaderFromResource-Funktion (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXAssembleShaderFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 78df978201df37269b7d33058effc16eadc9d16f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116017"
---
# <a name="d3dxassembleshaderfromresource-function"></a><span data-ttu-id="d203d-103">D3DXAssembleShaderFromResource-Funktion</span><span class="sxs-lookup"><span data-stu-id="d203d-103">D3DXAssembleShaderFromResource function</span></span>

<span data-ttu-id="d203d-104">Stellen Sie einen Shader zusammen.</span><span class="sxs-lookup"><span data-stu-id="d203d-104">Assemble a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="d203d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d203d-105">Syntax</span></span>


```C++
HRESULT D3DXAssembleShaderFromResource(
  _In_        HMODULE       hSrcModule,
  _In_        LPCTSTR       pSrcResource,
  _In_  const D3DXMACRO     *pDefines,
  _In_        LPD3DXINCLUDE pInclude,
  _In_        DWORD         Flags,
  _Out_       LPD3DXBUFFER  *ppShader,
  _Out_       LPD3DXBUFFER  *ppErrorMsgs
);
```



## <a name="parameters"></a><span data-ttu-id="d203d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d203d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d203d-107">*hSrcModule* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d203d-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d203d-108">Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d203d-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d203d-109">Handle für ein Modul, das die Beschreibung des Effekts enthält.</span><span class="sxs-lookup"><span data-stu-id="d203d-109">Handle to a module containing the effect description.</span></span> <span data-ttu-id="d203d-110">Wenn dieser Parameter **NULL** ist, wird das aktuelle Modul verwendet.</span><span class="sxs-lookup"><span data-stu-id="d203d-110">If this parameter is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="d203d-111">*pSrcResource* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d203d-111">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d203d-112">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d203d-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d203d-113">Zeiger auf eine Zeichenfolge, die den Ressourcennamen angibt.</span><span class="sxs-lookup"><span data-stu-id="d203d-113">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="d203d-114">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="d203d-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="d203d-115">Andernfalls wird der Zeichenfolgendatentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="d203d-115">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="d203d-116">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="d203d-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="d203d-117">*pDefine* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d203d-117">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d203d-118">Typ: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="d203d-118">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="d203d-119">Ein optionales auf **NULL** endendes Array von [**D3DXMACRO-Strukturen.**](d3dxmacro.md)</span><span class="sxs-lookup"><span data-stu-id="d203d-119">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="d203d-120">Dieser Wert kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="d203d-120">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d203d-121">*pInclude* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d203d-121">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d203d-122">Typ: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="d203d-122">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="d203d-123">Optionaler Schnittstellenzeiger [**ID3DXInclude**](id3dxinclude.md), der für die Behandlung von \# Includedirektiven verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d203d-123">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="d203d-124">Wenn dieser Wert **NULL ist,** wird includes entweder beim Kompilieren aus einer Datei oder beim Kompilieren aus einer Ressource oder einem Arbeitsspeicher \# zu einem Fehler führen.</span><span class="sxs-lookup"><span data-stu-id="d203d-124">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="d203d-125">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="d203d-125">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d203d-126">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d203d-126">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d203d-127">Kompilierungsoptionen, die durch verschiedene Flags identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="d203d-127">Compile options identified by various flags.</span></span> <span data-ttu-id="d203d-128">Der Direct3D 10 HLSL-Compiler ist jetzt die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="d203d-128">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="d203d-129">Weitere Informationen finden Sie unter [D3DXSHADER-Flags.](d3dxshader-flags.md)</span><span class="sxs-lookup"><span data-stu-id="d203d-129">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="d203d-130">*ppShader* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d203d-130">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d203d-131">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="d203d-131">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="d203d-132">Gibt einen Puffer zurück, der den erstellten Shader enthält.</span><span class="sxs-lookup"><span data-stu-id="d203d-132">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="d203d-133">Dieser Puffer enthält den kompilierten Shadercode sowie alle eingebetteten Debug- und Symboltabelleninformationen.</span><span class="sxs-lookup"><span data-stu-id="d203d-133">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="d203d-134">*ppErrorMsgs* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d203d-134">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d203d-135">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="d203d-135">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="d203d-136">Gibt einen Puffer zurück, der eine Auflistung von Fehlern und Warnungen enthält, die während der Kompilierung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="d203d-136">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="d203d-137">Dies sind die gleichen Meldungen, die der Debugger anzeigt, wenn er im Debugmodus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d203d-137">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="d203d-138">Dieser Wert kann NULL **sein.**</span><span class="sxs-lookup"><span data-stu-id="d203d-138">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d203d-139">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d203d-139">Return value</span></span>

<span data-ttu-id="d203d-140">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d203d-140">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d203d-141">Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d203d-141">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d203d-142">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="d203d-142">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="d203d-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d203d-143">Remarks</span></span>

<span data-ttu-id="d203d-144">Die Compilereinstellung bestimmt auch die Funktionsversion.</span><span class="sxs-lookup"><span data-stu-id="d203d-144">The compiler setting also determines the function version.</span></span> <span data-ttu-id="d203d-145">Wenn Unicode definiert ist, wird der Funktionsaufruf in D3DXAssembleShaderFromResourceW auflösen.</span><span class="sxs-lookup"><span data-stu-id="d203d-145">If Unicode is defined, the function call resolves to D3DXAssembleShaderFromResourceW.</span></span> <span data-ttu-id="d203d-146">Andernfalls wird der Funktionsaufruf in D3DXAssembleShaderFromResourceA auflösen, da ANSI-Zeichenfolgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d203d-146">Otherwise, the function call resolves to D3DXAssembleShaderFromResourceA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="d203d-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d203d-147">Requirements</span></span>



| <span data-ttu-id="d203d-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d203d-148">Requirement</span></span> | <span data-ttu-id="d203d-149">Wert</span><span class="sxs-lookup"><span data-stu-id="d203d-149">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d203d-150">Header</span><span class="sxs-lookup"><span data-stu-id="d203d-150">Header</span></span><br/>  | <dl> <span data-ttu-id="d203d-151"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="d203d-151"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="d203d-152">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d203d-152">Library</span></span><br/> | <dl> <span data-ttu-id="d203d-153"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="d203d-153"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d203d-154">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d203d-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d203d-155">Shaderfunktionen</span><span class="sxs-lookup"><span data-stu-id="d203d-155">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="d203d-156">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="d203d-156">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="d203d-157">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="d203d-157">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
