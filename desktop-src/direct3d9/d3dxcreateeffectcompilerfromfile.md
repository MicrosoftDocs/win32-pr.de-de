---
description: Erstellt einen Effekt Compiler aus einer Beschreibung des ASCII-Effekts.
ms.assetid: 87438a1e-4149-42ef-aa7a-9f0549eb7982
title: D3DXCreateEffectCompilerFromFile-Funktion (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectCompilerFromFile
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: fe27683078f77d7d444bd3a763fc326e749f7517
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355019"
---
# <a name="d3dxcreateeffectcompilerfromfile-function"></a><span data-ttu-id="e43b7-103">D3DXCreateEffectCompilerFromFile-Funktion</span><span class="sxs-lookup"><span data-stu-id="e43b7-103">D3DXCreateEffectCompilerFromFile function</span></span>

<span data-ttu-id="e43b7-104">Erstellt einen Effekt Compiler aus einer Beschreibung des ASCII-Effekts.</span><span class="sxs-lookup"><span data-stu-id="e43b7-104">Creates an effect compiler from an ASCII effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="e43b7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e43b7-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectCompilerFromFile(
  _In_        LPCTSTR              pSrcFile,
  _In_  const D3DXMACRO            *pDefines,
  _In_        LPD3DXINCLUDE        pInclude,
  _In_        DWORD                Flags,
  _Out_       LPD3DXEFFECTCOMPILER *ppEffectCompiler,
  _Out_       LPD3DXBUFFER         *ppParseErrors
);
```



## <a name="parameters"></a><span data-ttu-id="e43b7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e43b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e43b7-107">*psrcfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e43b7-107">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e43b7-108">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e43b7-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e43b7-109">Zeiger auf den Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="e43b7-109">Pointer to the filename.</span></span> <span data-ttu-id="e43b7-110">Dieser Parameter unterstützt Unicode-und ANSI-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="e43b7-110">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="e43b7-111">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="e43b7-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="e43b7-112">*pdefinitionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e43b7-112">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e43b7-113">Typ: **Konstanten [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="e43b7-113">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="e43b7-114">Ein optionales **null** terminiertes Array von [**D3DXMACRO**](d3dxmacro.md) -Strukturen, die Präprozessordefinitionen beschreiben.</span><span class="sxs-lookup"><span data-stu-id="e43b7-114">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="e43b7-115">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="e43b7-115">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e43b7-116">*pinclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e43b7-116">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e43b7-117">Typ: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="e43b7-117">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="e43b7-118">Optionaler Schnittstellen Zeiger, [**ID3DXInclude**](id3dxinclude.md), der zum Verarbeiten von include-Direktiven verwendet werden soll \# .</span><span class="sxs-lookup"><span data-stu-id="e43b7-118">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="e43b7-119">Wenn dieser Wert **null** ist, \# wird includes bei der Kompilierung aus einer Datei berücksichtigt, oder es wird ein Fehler ausgelöst, wenn eine Kompilierung aus einer Ressource oder einem Arbeitsspeicher erfolgt.</span><span class="sxs-lookup"><span data-stu-id="e43b7-119">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="e43b7-120">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="e43b7-120">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e43b7-121">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e43b7-121">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e43b7-122">Kompilierungsoptionen, die durch verschiedene Flags identifiziert werden (siehe [D3DXSHADER Flags](d3dxshader-flags.md)).</span><span class="sxs-lookup"><span data-stu-id="e43b7-122">Compile options identified by various flags (see [D3DXSHADER Flags](d3dxshader-flags.md)).</span></span> <span data-ttu-id="e43b7-123">Der Direct3D 10 HLSL-Compiler ist nun der Standard.</span><span class="sxs-lookup"><span data-stu-id="e43b7-123">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="e43b7-124">Ausführliche Informationen finden Sie unter [Effect-Compiler-Tool](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="e43b7-124">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="e43b7-125">*ppeer-ectcompiler* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e43b7-125">*ppEffectCompiler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e43b7-126">Typ: **[ **LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span><span class="sxs-lookup"><span data-stu-id="e43b7-126">Type: **[**LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span></span>

<span data-ttu-id="e43b7-127">Adresse eines Zeigers auf eine [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) -Schnittstelle, die den Effekt Compiler enthält.</span><span class="sxs-lookup"><span data-stu-id="e43b7-127">Address of a pointer to an [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) interface, containing the effect compiler.</span></span>

</dd> <dt>

<span data-ttu-id="e43b7-128">*ppparsererrors* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e43b7-128">*ppParseErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e43b7-129">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="e43b7-129">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="e43b7-130">Adresse eines Zeigers auf eine [**ID3DXBuffer**](id3dxbuffer.md) -Schnittstelle, die alle Fehlermeldungen enthält, die während der Kompilierung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="e43b7-130">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, containing any error messages that occurred during compilation.</span></span> <span data-ttu-id="e43b7-131">Dieser Parameter kann auf **null** festgelegt werden, um Fehlermeldungen zu ignorieren.</span><span class="sxs-lookup"><span data-stu-id="e43b7-131">This parameter can be set to **NULL** to ignore error messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e43b7-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e43b7-132">Return value</span></span>

<span data-ttu-id="e43b7-133">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e43b7-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e43b7-134">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e43b7-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e43b7-135">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="e43b7-135">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="e43b7-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e43b7-136">Remarks</span></span>

<span data-ttu-id="e43b7-137">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="e43b7-137">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="e43b7-138">Andernfalls wird der LPCTSTR-Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="e43b7-138">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="e43b7-139">Die Compilereinstellung bestimmt auch die Funktions Version.</span><span class="sxs-lookup"><span data-stu-id="e43b7-139">The compiler setting also determines the function version.</span></span> <span data-ttu-id="e43b7-140">Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXCreateEffectCompilerFromFileW aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="e43b7-140">If Unicode is defined, the function call resolves to D3DXCreateEffectCompilerFromFileW.</span></span> <span data-ttu-id="e43b7-141">Andernfalls wird der Funktions Aufruhe in D3DXCreateEffectCompilerFromFileA aufgelöst, da ANSI-Zeichen folgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e43b7-141">Otherwise, the function call resolves to D3DXCreateEffectCompilerFromFileA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="e43b7-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e43b7-142">Requirements</span></span>



| <span data-ttu-id="e43b7-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e43b7-143">Requirement</span></span> | <span data-ttu-id="e43b7-144">Wert</span><span class="sxs-lookup"><span data-stu-id="e43b7-144">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e43b7-145">Header</span><span class="sxs-lookup"><span data-stu-id="e43b7-145">Header</span></span><br/>  | <dl> <span data-ttu-id="e43b7-146"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="e43b7-146"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="e43b7-147">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e43b7-147">Library</span></span><br/> | <dl> <span data-ttu-id="e43b7-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e43b7-148"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e43b7-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e43b7-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e43b7-150">Effekt Funktionen</span><span class="sxs-lookup"><span data-stu-id="e43b7-150">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="e43b7-151">**D3DXCreateEffectCompiler**</span><span class="sxs-lookup"><span data-stu-id="e43b7-151">**D3DXCreateEffectCompiler**</span></span>](d3dxcreateeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="e43b7-152">**D3DXCreateEffectCompilerFromResource**</span><span class="sxs-lookup"><span data-stu-id="e43b7-152">**D3DXCreateEffectCompilerFromResource**</span></span>](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 
