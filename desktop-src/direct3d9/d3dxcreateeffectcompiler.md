---
description: Erstellt einen Effekt Compiler aus einer Beschreibung des ASCII-Effekts.
ms.assetid: 96e883f4-4055-4b8b-940a-164bbf893af4
title: D3DXCreateEffectCompiler-Funktion (D3DX9Effect. h)
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
ms.openlocfilehash: 513b11ba12abe05126c122f8bc9bfcfa978df3fa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762282"
---
# <a name="d3dxcreateeffectcompiler-function"></a><span data-ttu-id="11e5b-103">D3DXCreateEffectCompiler-Funktion</span><span class="sxs-lookup"><span data-stu-id="11e5b-103">D3DXCreateEffectCompiler function</span></span>

<span data-ttu-id="11e5b-104">Erstellt einen Effekt Compiler aus einer Beschreibung des ASCII-Effekts.</span><span class="sxs-lookup"><span data-stu-id="11e5b-104">Creates an effect compiler from an ASCII effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="11e5b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="11e5b-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="11e5b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="11e5b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11e5b-107">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11e5b-107">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11e5b-108">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="11e5b-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="11e5b-109">Zeiger auf einen Puffer, der eine Beschreibung des Effekts enthält.</span><span class="sxs-lookup"><span data-stu-id="11e5b-109">Pointer to a buffer containing an effect description.</span></span>

</dd> <dt>

<span data-ttu-id="11e5b-110">*Srcdatalen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11e5b-110">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11e5b-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="11e5b-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="11e5b-112">Länge in Byte der Effekt Daten.</span><span class="sxs-lookup"><span data-stu-id="11e5b-112">Length, in bytes, of the effect data.</span></span>

</dd> <dt>

<span data-ttu-id="11e5b-113">*pdefinitionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11e5b-113">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11e5b-114">Typ: **Konstanten [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="11e5b-114">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="11e5b-115">Ein optionales **null** terminiertes Array von [**D3DXMACRO**](d3dxmacro.md) -Strukturen, die Präprozessordefinitionen beschreiben.</span><span class="sxs-lookup"><span data-stu-id="11e5b-115">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="11e5b-116">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="11e5b-116">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="11e5b-117">*pinclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11e5b-117">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11e5b-118">Typ: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="11e5b-118">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="11e5b-119">Optionaler Schnittstellen Zeiger, [**ID3DXInclude**](id3dxinclude.md), der zum Verarbeiten von include-Direktiven verwendet werden soll \# .</span><span class="sxs-lookup"><span data-stu-id="11e5b-119">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="11e5b-120">Wenn dieser Wert **null** ist, \# wird includes bei der Kompilierung aus einer Datei berücksichtigt, oder es wird ein Fehler ausgelöst, wenn eine Kompilierung aus einer Ressource oder einem Arbeitsspeicher erfolgt.</span><span class="sxs-lookup"><span data-stu-id="11e5b-120">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="11e5b-121">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="11e5b-121">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11e5b-122">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="11e5b-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="11e5b-123">Kompilierungsoptionen, die durch verschiedene Flags identifiziert werden (siehe [D3DXSHADER Flags](d3dxshader-flags.md)).</span><span class="sxs-lookup"><span data-stu-id="11e5b-123">Compile options identified by various flags (see [D3DXSHADER Flags](d3dxshader-flags.md)).</span></span> <span data-ttu-id="11e5b-124">Der Direct3D 10 HLSL-Compiler ist nun der Standard.</span><span class="sxs-lookup"><span data-stu-id="11e5b-124">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="11e5b-125">Ausführliche Informationen finden Sie unter [Effect-Compiler-Tool](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="11e5b-125">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="11e5b-126">*ppeer-ectcompiler* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="11e5b-126">*ppEffectCompiler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11e5b-127">Typ: **[ **LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span><span class="sxs-lookup"><span data-stu-id="11e5b-127">Type: **[**LPD3DXEFFECTCOMPILER**](id3dxeffectcompiler.md)\***</span></span>

<span data-ttu-id="11e5b-128">Adresse eines Zeigers auf eine [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) -Schnittstelle, die den Effekt Compiler enthält.</span><span class="sxs-lookup"><span data-stu-id="11e5b-128">Address of a pointer to an [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) interface containing the effect compiler.</span></span>

</dd> <dt>

<span data-ttu-id="11e5b-129">*ppparsererrors* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="11e5b-129">*ppParseErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11e5b-130">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="11e5b-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="11e5b-131">Adresse eines Zeigers auf eine [**ID3DXBuffer**](id3dxbuffer.md) -Schnittstelle, die Fehlermeldungen enthält, die während der Kompilierung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="11e5b-131">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface containing any error messages that occurred during compilation.</span></span> <span data-ttu-id="11e5b-132">Dieser Parameter kann auf **null** festgelegt werden, um Fehlermeldungen zu ignorieren.</span><span class="sxs-lookup"><span data-stu-id="11e5b-132">This parameter can be set to **NULL** to ignore error messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11e5b-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="11e5b-133">Return value</span></span>

<span data-ttu-id="11e5b-134">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="11e5b-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="11e5b-135">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="11e5b-135">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="11e5b-136">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="11e5b-136">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="11e5b-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11e5b-137">Requirements</span></span>



| <span data-ttu-id="11e5b-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11e5b-138">Requirement</span></span> | <span data-ttu-id="11e5b-139">Wert</span><span class="sxs-lookup"><span data-stu-id="11e5b-139">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="11e5b-140">Header</span><span class="sxs-lookup"><span data-stu-id="11e5b-140">Header</span></span><br/>  | <dl> <span data-ttu-id="11e5b-141"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="11e5b-141"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="11e5b-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="11e5b-142">Library</span></span><br/> | <dl> <span data-ttu-id="11e5b-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11e5b-143"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="11e5b-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11e5b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11e5b-145">Effekt Funktionen</span><span class="sxs-lookup"><span data-stu-id="11e5b-145">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="11e5b-146">**D3DXCreateEffectCompilerFromFile**</span><span class="sxs-lookup"><span data-stu-id="11e5b-146">**D3DXCreateEffectCompilerFromFile**</span></span>](d3dxcreateeffectcompilerfromfile.md)
</dt> <dt>

[<span data-ttu-id="11e5b-147">**D3DXCreateEffectCompilerFromResource**</span><span class="sxs-lookup"><span data-stu-id="11e5b-147">**D3DXCreateEffectCompilerFromResource**</span></span>](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 
