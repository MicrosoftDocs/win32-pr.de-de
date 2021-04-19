---
description: Assemblieren Sie einen Shader.
ms.assetid: 2977b64a-b8cc-454b-8e28-291f6f2c6fc1
title: D3DXAssembleShaderFromFile-Funktion (D3DX9Shader. h)
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
ms.openlocfilehash: a6e355f6ce51158f72757f771114346899557c59
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366655"
---
# <a name="d3dxassembleshaderfromfile-function"></a><span data-ttu-id="8e15d-103">D3DXAssembleShaderFromFile-Funktion</span><span class="sxs-lookup"><span data-stu-id="8e15d-103">D3DXAssembleShaderFromFile function</span></span>

<span data-ttu-id="8e15d-104">Assemblieren Sie einen Shader.</span><span class="sxs-lookup"><span data-stu-id="8e15d-104">Assemble a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e15d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e15d-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="8e15d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e15d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e15d-107">*psrcfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8e15d-107">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e15d-108">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8e15d-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8e15d-109">Zeiger auf eine Zeichenfolge, die den Dateinamen angibt.</span><span class="sxs-lookup"><span data-stu-id="8e15d-109">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="8e15d-110">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="8e15d-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="8e15d-111">Andernfalls wird der String-Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="8e15d-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="8e15d-112">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="8e15d-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="8e15d-113">*pdefinitionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8e15d-113">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e15d-114">Typ: **Konstanten [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="8e15d-114">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="8e15d-115">Ein optionales **null** terminiertes Array von [**D3DXMACRO**](d3dxmacro.md) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="8e15d-115">An optional **NULL** terminated array of [**D3DXMACRO**](d3dxmacro.md) structures.</span></span> <span data-ttu-id="8e15d-116">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="8e15d-116">This value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8e15d-117">*pinclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8e15d-117">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e15d-118">Typ: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="8e15d-118">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="8e15d-119">Optionaler Schnittstellen Zeiger, [**ID3DXInclude**](id3dxinclude.md), der zum Verarbeiten von include-Direktiven verwendet werden soll \# .</span><span class="sxs-lookup"><span data-stu-id="8e15d-119">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="8e15d-120">Wenn dieser Wert **null** ist, \# wird includes bei der Kompilierung aus einer Datei berücksichtigt, oder es wird ein Fehler ausgelöst, wenn eine Kompilierung aus einer Ressource oder einem Arbeitsspeicher erfolgt.</span><span class="sxs-lookup"><span data-stu-id="8e15d-120">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="8e15d-121">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="8e15d-121">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e15d-122">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8e15d-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8e15d-123">Kompilierungsoptionen, die durch verschiedene Flags identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="8e15d-123">Compile options identified by various flags.</span></span> <span data-ttu-id="8e15d-124">Der Direct3D 10 HLSL-Compiler ist nun der Standard.</span><span class="sxs-lookup"><span data-stu-id="8e15d-124">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="8e15d-125">Weitere Informationen finden Sie unter [D3DXSHADER-Flags](d3dxshader-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="8e15d-125">See [D3DXSHADER Flags](d3dxshader-flags.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="8e15d-126">*ppshader* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8e15d-126">*ppShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e15d-127">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="8e15d-127">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="8e15d-128">Gibt einen Puffer zurück, der den erstellten Shader enthält.</span><span class="sxs-lookup"><span data-stu-id="8e15d-128">Returns a buffer containing the created shader.</span></span> <span data-ttu-id="8e15d-129">Dieser Puffer enthält den kompilierten Shader-Code sowie alle eingebetteten Debug-und Symboltabellen Informationen.</span><span class="sxs-lookup"><span data-stu-id="8e15d-129">This buffer contains the compiled shader code, as well as any embedded debug and symbol table information.</span></span>

</dd> <dt>

<span data-ttu-id="8e15d-130">*pperrormsgs* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8e15d-130">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e15d-131">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="8e15d-131">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="8e15d-132">Gibt einen Puffer zurück, der eine Auflistung von Fehlern und Warnungen enthält, die während der Kompilierung gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="8e15d-132">Returns a buffer containing a listing of errors and warnings that were encountered during the compile.</span></span> <span data-ttu-id="8e15d-133">Dies sind die gleichen Meldungen, die der Debugger anzeigt, wenn er im Debugmodus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8e15d-133">These are the same messages the debugger displays when running in debug mode.</span></span> <span data-ttu-id="8e15d-134">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="8e15d-134">This value may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e15d-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8e15d-135">Return value</span></span>

<span data-ttu-id="8e15d-136">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8e15d-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8e15d-137">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8e15d-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8e15d-138">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="8e15d-138">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e15d-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8e15d-139">Remarks</span></span>

<span data-ttu-id="8e15d-140">Die Compilereinstellung bestimmt auch die Funktions Version.</span><span class="sxs-lookup"><span data-stu-id="8e15d-140">The compiler setting also determines the function version.</span></span> <span data-ttu-id="8e15d-141">Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXAssembleShaderFromFileW aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="8e15d-141">If Unicode is defined, the function call resolves to D3DXAssembleShaderFromFileW.</span></span> <span data-ttu-id="8e15d-142">Andernfalls wird der Funktions Aufruhe in D3DXAssembleShaderFromFileA aufgelöst, da ANSI-Zeichen folgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8e15d-142">Otherwise, the function call resolves to D3DXAssembleShaderFromFileA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e15d-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8e15d-143">Requirements</span></span>



| <span data-ttu-id="8e15d-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8e15d-144">Requirement</span></span> | <span data-ttu-id="8e15d-145">Wert</span><span class="sxs-lookup"><span data-stu-id="8e15d-145">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e15d-146">Header</span><span class="sxs-lookup"><span data-stu-id="8e15d-146">Header</span></span><br/>  | <dl> <span data-ttu-id="8e15d-147"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e15d-147"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="8e15d-148">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8e15d-148">Library</span></span><br/> | <dl> <span data-ttu-id="8e15d-149"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8e15d-149"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8e15d-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e15d-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e15d-151">Shaderfunktionen</span><span class="sxs-lookup"><span data-stu-id="8e15d-151">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> <dt>

[<span data-ttu-id="8e15d-152">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="8e15d-152">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="8e15d-153">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="8e15d-153">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
