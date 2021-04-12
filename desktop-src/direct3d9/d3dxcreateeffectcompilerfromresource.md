---
description: Erstellt eine ID3DXEffectCompiler aus einer Beschreibung des ASCII-Effekts.
ms.assetid: 041e0a3f-3dc6-4cc3-8380-d4a79a3f647a
title: D3DXCreateEffectCompilerFromResource-Funktion (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectCompilerFromResource
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1a3dabe0a2690c84e125af6d321397cbe3765f83
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219563"
---
# <a name="d3dxcreateeffectcompilerfromresource-function"></a><span data-ttu-id="0ef66-103">D3DXCreateEffectCompilerFromResource-Funktion</span><span class="sxs-lookup"><span data-stu-id="0ef66-103">D3DXCreateEffectCompilerFromResource function</span></span>

<span data-ttu-id="0ef66-104">Erstellt eine [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) aus einer Beschreibung des ASCII-Effekts.</span><span class="sxs-lookup"><span data-stu-id="0ef66-104">Creates an [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) from an ASCII effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ef66-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ef66-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectCompilerFromResource(
  _In_        HMODULE              hSrcModule,
  _In_        LPCTSTR              pSrcResource,
  _In_  const D3DXMACRO            *pDefines,
  _In_        LPD3DXINCLUDE        pInclude,
  _In_        DWORD                Flags,
  _Out_       LPD3DXEFFECTCOMPILER *ppEffectCompiler,
  _Out_       LPD3DXBUFFER         *ppParseErrors
);
```



## <a name="parameters"></a><span data-ttu-id="0ef66-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ef66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ef66-107">*hsrcmodule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ef66-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ef66-108">Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0ef66-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0ef66-109">Handle für ein Modul, das die Beschreibung des Effekts enthält.</span><span class="sxs-lookup"><span data-stu-id="0ef66-109">Handle to a module containing the effect description.</span></span> <span data-ttu-id="0ef66-110">Wenn dieser Parameter **null** ist, wird das aktuelle Modul verwendet.</span><span class="sxs-lookup"><span data-stu-id="0ef66-110">If this parameter is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="0ef66-111">*psrkresource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ef66-111">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ef66-112">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0ef66-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0ef66-113">Ein Zeiger auf die Ressource.</span><span class="sxs-lookup"><span data-stu-id="0ef66-113">Pointer to the resource.</span></span> <span data-ttu-id="0ef66-114">Dieser Parameter unterstützt Unicode-und ANSI-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="0ef66-114">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="0ef66-115">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="0ef66-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="0ef66-116">*pdefinitionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ef66-116">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ef66-117">Typ: **Konstanten [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="0ef66-117">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="0ef66-118">Ein optionales **null** terminiertes Array von [**D3DXMACRO**](d3dxmacro.md) -Strukturen, die Präprozessordefinitionen beschreiben.</span><span class="sxs-lookup"><span data-stu-id="0ef66-118">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="0ef66-119">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="0ef66-119">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0ef66-120">*pinclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ef66-120">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ef66-121">Typ: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="0ef66-121">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="0ef66-122">Optionaler Schnittstellen Zeiger, [**ID3DXInclude**](id3dxinclude.md), der zum Verarbeiten von include-Direktiven verwendet werden soll \# .</span><span class="sxs-lookup"><span data-stu-id="0ef66-122">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="0ef66-123">Wenn dieser Wert **null** ist, \# wird includes bei der Kompilierung aus einer Datei berücksichtigt, oder es wird ein Fehler ausgelöst, wenn eine Kompilierung aus einer Ressource oder einem Arbeitsspeicher erfolgt.</span><span class="sxs-lookup"><span data-stu-id="0ef66-123">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="0ef66-124">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="0ef66-124">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ef66-125">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0ef66-125">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0ef66-126">Kompilierungsoptionen, die durch verschiedene Flags identifiziert werden (siehe [D3DXSHADER Flags](d3dxshader-flags.md)).</span><span class="sxs-lookup"><span data-stu-id="0ef66-126">Compile options identified by various flags (see [D3DXSHADER Flags](d3dxshader-flags.md)).</span></span> <span data-ttu-id="0ef66-127">Der Direct3D 10 HLSL-Compiler ist nun der Standard.</span><span class="sxs-lookup"><span data-stu-id="0ef66-127">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="0ef66-128">Ausführliche Informationen finden Sie unter [Effect-Compiler-Tool](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="0ef66-128">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="0ef66-129">*ppeer-ectcompiler* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0ef66-129">*ppEffectCompiler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ef66-130">Typ: **[ **LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span><span class="sxs-lookup"><span data-stu-id="0ef66-130">Type: **[**LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span></span>

<span data-ttu-id="0ef66-131">Adresse eines Zeigers auf eine [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) -Schnittstelle, die den Effekt Compiler enthält.</span><span class="sxs-lookup"><span data-stu-id="0ef66-131">Address of a pointer to an [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) interface, containing the effect compiler.</span></span>

</dd> <dt>

<span data-ttu-id="0ef66-132">*ppparsererrors* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0ef66-132">*ppParseErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ef66-133">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="0ef66-133">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="0ef66-134">Adresse eines Zeigers auf eine [**ID3DXBuffer**](id3dxbuffer.md) -Schnittstelle, die alle Fehlermeldungen enthält, die während der Kompilierung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="0ef66-134">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, containing any error messages that occurred during compilation.</span></span> <span data-ttu-id="0ef66-135">Dieser Parameter kann auf **null** festgelegt werden, um Fehlermeldungen zu ignorieren.</span><span class="sxs-lookup"><span data-stu-id="0ef66-135">This parameter can be set to **NULL** to ignore error messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ef66-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0ef66-136">Return value</span></span>

<span data-ttu-id="0ef66-137">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0ef66-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0ef66-138">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0ef66-138">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0ef66-139">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="0ef66-139">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ef66-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0ef66-140">Remarks</span></span>

<span data-ttu-id="0ef66-141">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="0ef66-141">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="0ef66-142">Andernfalls wird der LPCTSTR-Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="0ef66-142">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="0ef66-143">Die Compilereinstellung bestimmt auch die Funktions Version.</span><span class="sxs-lookup"><span data-stu-id="0ef66-143">The compiler setting also determines the function version.</span></span> <span data-ttu-id="0ef66-144">Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXCreateEffectCompilerFromResourceW aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="0ef66-144">If Unicode is defined, the function call resolves to D3DXCreateEffectCompilerFromResourceW.</span></span> <span data-ttu-id="0ef66-145">Andernfalls wird der Funktions Aufruhe in D3DXCreateEffectCompilerFromResourceA aufgelöst, da ANSI-Zeichen folgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0ef66-145">Otherwise, the function call resolves to D3DXCreateEffectCompilerFromResourceA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ef66-146">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ef66-146">Requirements</span></span>



| <span data-ttu-id="0ef66-147">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ef66-147">Requirement</span></span> | <span data-ttu-id="0ef66-148">Wert</span><span class="sxs-lookup"><span data-stu-id="0ef66-148">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ef66-149">Header</span><span class="sxs-lookup"><span data-stu-id="0ef66-149">Header</span></span><br/>  | <dl> <span data-ttu-id="0ef66-150"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ef66-150"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="0ef66-151">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0ef66-151">Library</span></span><br/> | <dl> <span data-ttu-id="0ef66-152"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0ef66-152"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0ef66-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ef66-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ef66-154">Effekt Funktionen</span><span class="sxs-lookup"><span data-stu-id="0ef66-154">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="0ef66-155">**D3DXCreateEffectCompiler**</span><span class="sxs-lookup"><span data-stu-id="0ef66-155">**D3DXCreateEffectCompiler**</span></span>](d3dxcreateeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="0ef66-156">**D3DXCreateEffectCompilerFromFile**</span><span class="sxs-lookup"><span data-stu-id="0ef66-156">**D3DXCreateEffectCompilerFromFile**</span></span>](d3dxcreateeffectcompilerfromfile.md)
</dt> </dl>

 

 
