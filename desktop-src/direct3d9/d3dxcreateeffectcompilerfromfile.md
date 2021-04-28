---
description: 'D3DXCreateEffectCompilerFromFile-Funktion: Erstellt einen Effektcompiler aus einer ASCII-Effektbeschreibung.'
ms.assetid: 87438a1e-4149-42ef-aa7a-9f0549eb7982
title: D3DXCreateEffectCompilerFromFile-Funktion (D3DX9Effect.h)
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
ms.openlocfilehash: 0c054b31b1ab70d1378c794be13058204b994ee2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087978"
---
# <a name="d3dxcreateeffectcompilerfromfile-function"></a><span data-ttu-id="7a936-103">D3DXCreateEffectCompilerFromFile-Funktion</span><span class="sxs-lookup"><span data-stu-id="7a936-103">D3DXCreateEffectCompilerFromFile function</span></span>

<span data-ttu-id="7a936-104">Erstellt einen Effektcompiler aus einer ASCII-Effektbeschreibung.</span><span class="sxs-lookup"><span data-stu-id="7a936-104">Creates an effect compiler from an ASCII effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a936-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a936-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="7a936-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a936-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a936-107">*pSrcFile* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="7a936-107">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a936-108">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7a936-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7a936-109">Zeiger auf den Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="7a936-109">Pointer to the filename.</span></span> <span data-ttu-id="7a936-110">Dieser Parameter unterstützt sowohl Unicode- als auch ANSI-Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="7a936-110">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="7a936-111">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="7a936-111">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="7a936-112">*pDefdefine* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="7a936-112">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a936-113">Typ: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="7a936-113">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="7a936-114">Ein optionales **auf NULL** beendetes Array [**von D3DXMACRO-Strukturen,**](d3dxmacro.md) die Präprozessordefinitionen beschreiben.</span><span class="sxs-lookup"><span data-stu-id="7a936-114">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="7a936-115">Dieser Wert kann NULL **sein.**</span><span class="sxs-lookup"><span data-stu-id="7a936-115">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7a936-116">*pInclude* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="7a936-116">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a936-117">Typ: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="7a936-117">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="7a936-118">Optionaler Schnittstellenzeiger [**ID3DXInclude**](id3dxinclude.md), der für die Behandlung von Include-Direktiven \# verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7a936-118">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="7a936-119">Wenn dieser Wert **NULL ist,** wird includes entweder beim Kompilieren aus einer Datei oder beim Kompilieren aus einer Ressource oder einem Arbeitsspeicher \# zu einem Fehler führen.</span><span class="sxs-lookup"><span data-stu-id="7a936-119">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="7a936-120">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="7a936-120">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a936-121">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7a936-121">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7a936-122">Kompilierungsoptionen, die durch verschiedene Flags identifiziert werden (siehe [D3DXSHADER-Flags](d3dxshader-flags.md)).</span><span class="sxs-lookup"><span data-stu-id="7a936-122">Compile options identified by various flags (see [D3DXSHADER Flags](d3dxshader-flags.md)).</span></span> <span data-ttu-id="7a936-123">Der Direct3D 10 HLSL-Compiler ist jetzt die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="7a936-123">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="7a936-124">Weitere [Informationen finden Sie unter Effect-Compiler Tool](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="7a936-124">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="7a936-125">*ppEffectCompiler* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7a936-125">*ppEffectCompiler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a936-126">Typ: **[ **LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span><span class="sxs-lookup"><span data-stu-id="7a936-126">Type: **[**LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span></span>

<span data-ttu-id="7a936-127">Adresse eines Zeigers auf eine [**ID3DXEffectCompiler-Schnittstelle,**](id3dxeffectcompiler.md) die den Effektcompiler enthält.</span><span class="sxs-lookup"><span data-stu-id="7a936-127">Address of a pointer to an [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) interface, containing the effect compiler.</span></span>

</dd> <dt>

<span data-ttu-id="7a936-128">*ppParseErrors* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7a936-128">*ppParseErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a936-129">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="7a936-129">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="7a936-130">Adresse eines Zeigers auf eine [**ID3DXBuffer-Schnittstelle,**](id3dxbuffer.md) die alle Fehlermeldungen enthält, die während der Kompilierung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="7a936-130">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, containing any error messages that occurred during compilation.</span></span> <span data-ttu-id="7a936-131">Dieser Parameter kann auf **NULL** festgelegt werden, um Fehlermeldungen zu ignorieren.</span><span class="sxs-lookup"><span data-stu-id="7a936-131">This parameter can be set to **NULL** to ignore error messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a936-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7a936-132">Return value</span></span>

<span data-ttu-id="7a936-133">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7a936-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7a936-134">Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7a936-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7a936-135">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="7a936-135">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a936-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a936-136">Remarks</span></span>

<span data-ttu-id="7a936-137">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="7a936-137">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="7a936-138">Andernfalls wird der LPCTSTR-Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="7a936-138">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="7a936-139">Die Compilereinstellung bestimmt auch die Funktionsversion.</span><span class="sxs-lookup"><span data-stu-id="7a936-139">The compiler setting also determines the function version.</span></span> <span data-ttu-id="7a936-140">Wenn Unicode definiert ist, wird der Funktionsaufruf in D3DXCreateEffectCompilerFromFileW aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="7a936-140">If Unicode is defined, the function call resolves to D3DXCreateEffectCompilerFromFileW.</span></span> <span data-ttu-id="7a936-141">Andernfalls wird der Funktionsaufruf in D3DXCreateEffectCompilerFromFileA aufgelöst, da ANSI-Zeichenfolgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7a936-141">Otherwise, the function call resolves to D3DXCreateEffectCompilerFromFileA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a936-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a936-142">Requirements</span></span>



| <span data-ttu-id="7a936-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a936-143">Requirement</span></span> | <span data-ttu-id="7a936-144">Wert</span><span class="sxs-lookup"><span data-stu-id="7a936-144">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a936-145">Header</span><span class="sxs-lookup"><span data-stu-id="7a936-145">Header</span></span><br/>  | <dl> <span data-ttu-id="7a936-146"><dt>D3DX9Effect.h</dt></span><span class="sxs-lookup"><span data-stu-id="7a936-146"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="7a936-147">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7a936-147">Library</span></span><br/> | <dl> <span data-ttu-id="7a936-148"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="7a936-148"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7a936-149">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7a936-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a936-150">Effect-Funktionen</span><span class="sxs-lookup"><span data-stu-id="7a936-150">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="7a936-151">**D3DXCreateEffectCompiler**</span><span class="sxs-lookup"><span data-stu-id="7a936-151">**D3DXCreateEffectCompiler**</span></span>](d3dxcreateeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="7a936-152">**D3DXCreateEffectCompilerFromResource**</span><span class="sxs-lookup"><span data-stu-id="7a936-152">**D3DXCreateEffectCompilerFromResource**</span></span>](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 
