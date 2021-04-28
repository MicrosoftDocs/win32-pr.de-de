---
description: 'D3DXCreateEffectCompiler-Funktion: Erstellt einen Effektcompiler aus einer ASCII-Effektbeschreibung.'
ms.assetid: 96e883f4-4055-4b8b-940a-164bbf893af4
title: D3DXCreateEffectCompiler-Funktion (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectCompiler
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 38ab58ed15609d468d25f4406353448e4fd6adb4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115768"
---
# <a name="d3dxcreateeffectcompiler-function"></a><span data-ttu-id="33c52-103">D3DXCreateEffectCompiler-Funktion</span><span class="sxs-lookup"><span data-stu-id="33c52-103">D3DXCreateEffectCompiler function</span></span>

<span data-ttu-id="33c52-104">Erstellt einen Effektcompiler aus einer ASCII-Effektbeschreibung.</span><span class="sxs-lookup"><span data-stu-id="33c52-104">Creates an effect compiler from an ASCII effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="33c52-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="33c52-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectCompiler(
  _In_        LPCSTR               pSrcData,
  _In_        UINT                 SrcDataLen,
  _In_  const D3DXMACRO            *pDefines,
  _In_        LPD3DXINCLUDE        pInclude,
  _In_        DWORD                Flags,
  _Out_       LPD3DXEFFECTCOMPILER *ppEffectCompiler,
  _Out_       LPD3DXBUFFER         *ppParseErrors
);
```



## <a name="parameters"></a><span data-ttu-id="33c52-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="33c52-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33c52-107">*pSrcData* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="33c52-107">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33c52-108">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="33c52-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="33c52-109">Zeiger auf einen Puffer, der eine Effektbeschreibung enthält.</span><span class="sxs-lookup"><span data-stu-id="33c52-109">Pointer to a buffer containing an effect description.</span></span>

</dd> <dt>

<span data-ttu-id="33c52-110">*SrcDataLen* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="33c52-110">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33c52-111">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="33c52-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="33c52-112">Länge der Effect-Daten in Bytes.</span><span class="sxs-lookup"><span data-stu-id="33c52-112">Length, in bytes, of the effect data.</span></span>

</dd> <dt>

<span data-ttu-id="33c52-113">*pDefine* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="33c52-113">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33c52-114">Typ: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="33c52-114">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="33c52-115">Ein optionales Mit **NULL** endendes Array von [**D3DXMACRO-Strukturen,**](d3dxmacro.md) die Präprozessordefinitionen beschreiben.</span><span class="sxs-lookup"><span data-stu-id="33c52-115">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="33c52-116">Dieser Wert kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="33c52-116">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="33c52-117">*pInclude* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="33c52-117">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33c52-118">Typ: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="33c52-118">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="33c52-119">Optionaler Schnittstellenzeiger [**ID3DXInclude**](id3dxinclude.md), der für die Behandlung von \# Includedirektiven verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="33c52-119">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="33c52-120">Wenn dieser Wert **NULL** ist, \# wird includes entweder beim Kompilieren aus einer Datei berücksichtigt oder verursacht bei der Kompilierung aus einer Ressource oder aus dem Arbeitsspeicher einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="33c52-120">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="33c52-121">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="33c52-121">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33c52-122">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="33c52-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="33c52-123">Durch verschiedene Flags identifizierte Kompilierungsoptionen (siehe [D3DXSHADER-Flags).](d3dxshader-flags.md)</span><span class="sxs-lookup"><span data-stu-id="33c52-123">Compile options identified by various flags (see [D3DXSHADER Flags](d3dxshader-flags.md)).</span></span> <span data-ttu-id="33c52-124">Der Direct3D 10 HLSL-Compiler ist jetzt die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="33c52-124">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="33c52-125">Weitere [Informationen finden Sie unter Effect-Compiler Tool](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="33c52-125">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="33c52-126">*ppEffectCompiler* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="33c52-126">*ppEffectCompiler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="33c52-127">Typ: **[ **LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span><span class="sxs-lookup"><span data-stu-id="33c52-127">Type: **[**LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span></span>

<span data-ttu-id="33c52-128">Adresse eines Zeigers auf eine [**ID3DXEffectCompiler-Schnittstelle,**](id3dxeffectcompiler.md) die den Effektcompiler enthält.</span><span class="sxs-lookup"><span data-stu-id="33c52-128">Address of a pointer to an [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) interface containing the effect compiler.</span></span>

</dd> <dt>

<span data-ttu-id="33c52-129">*ppParseErrors* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="33c52-129">*ppParseErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="33c52-130">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="33c52-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="33c52-131">Adresse eines Zeigers auf eine [**ID3DXBuffer-Schnittstelle,**](id3dxbuffer.md) die alle Fehlermeldungen enthält, die während der Kompilierung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="33c52-131">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface containing any error messages that occurred during compilation.</span></span> <span data-ttu-id="33c52-132">Dieser Parameter kann auf NULL festgelegt **werden,** um Fehlermeldungen zu ignorieren.</span><span class="sxs-lookup"><span data-stu-id="33c52-132">This parameter can be set to **NULL** to ignore error messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33c52-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="33c52-133">Return value</span></span>

<span data-ttu-id="33c52-134">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="33c52-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="33c52-135">Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="33c52-135">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="33c52-136">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="33c52-136">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="33c52-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33c52-137">Requirements</span></span>



| <span data-ttu-id="33c52-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33c52-138">Requirement</span></span> | <span data-ttu-id="33c52-139">Wert</span><span class="sxs-lookup"><span data-stu-id="33c52-139">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="33c52-140">Header</span><span class="sxs-lookup"><span data-stu-id="33c52-140">Header</span></span><br/>  | <dl> <span data-ttu-id="33c52-141"><dt>D3DX9Effect.h</dt></span><span class="sxs-lookup"><span data-stu-id="33c52-141"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="33c52-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="33c52-142">Library</span></span><br/> | <dl> <span data-ttu-id="33c52-143"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="33c52-143"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="33c52-144">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="33c52-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33c52-145">Effect-Funktionen</span><span class="sxs-lookup"><span data-stu-id="33c52-145">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="33c52-146">**D3DXCreateEffectCompilerFromFile**</span><span class="sxs-lookup"><span data-stu-id="33c52-146">**D3DXCreateEffectCompilerFromFile**</span></span>](d3dxcreateeffectcompilerfromfile.md)
</dt> <dt>

[<span data-ttu-id="33c52-147">**D3DXCreateEffectCompilerFromResource**</span><span class="sxs-lookup"><span data-stu-id="33c52-147">**D3DXCreateEffectCompilerFromResource**</span></span>](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 
