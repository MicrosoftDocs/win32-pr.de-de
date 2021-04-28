---
description: 'D3DXCreateEffect-Funktion: Erstellt einen Effekt aus einer ASCII- oder binären Effektbeschreibung.'
ms.assetid: 1cbd91f2-3cda-4770-a3c5-b1e6702628d1
title: D3DXCreateEffect-Funktion (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffect
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6821375dfc672d4937c335cf85dab12ba31b726c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115778"
---
# <a name="d3dxcreateeffect-function"></a><span data-ttu-id="3a24d-103">D3DXCreateEffect-Funktion</span><span class="sxs-lookup"><span data-stu-id="3a24d-103">D3DXCreateEffect function</span></span>

<span data-ttu-id="3a24d-104">Erstellen Sie einen Effekt aus einer ASCII- oder binären Effektbeschreibung.</span><span class="sxs-lookup"><span data-stu-id="3a24d-104">Create an effect from an ASCII or binary effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a24d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a24d-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffect(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        LPCVOID           pSrcData,
  _In_        UINT              SrcDataLen,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="3a24d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a24d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a24d-107">*pDevice* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="3a24d-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a24d-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="3a24d-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="3a24d-109">Zeiger auf das Gerät, das den Effekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="3a24d-109">Pointer to the device that will create the effect.</span></span> <span data-ttu-id="3a24d-110">Siehe [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="3a24d-110">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> <dt>

<span data-ttu-id="3a24d-111">*pSrcData* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="3a24d-111">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a24d-112">Typ: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3a24d-112">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3a24d-113">Zeiger auf einen Puffer, der eine Effektbeschreibung enthält.</span><span class="sxs-lookup"><span data-stu-id="3a24d-113">Pointer to a buffer containing an effect description.</span></span>

</dd> <dt>

<span data-ttu-id="3a24d-114">*SrcDataLen* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="3a24d-114">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a24d-115">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3a24d-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3a24d-116">Länge der Effektdaten in Bytes.</span><span class="sxs-lookup"><span data-stu-id="3a24d-116">Length of the effect data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="3a24d-117">*pDefdefine* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="3a24d-117">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a24d-118">Typ: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="3a24d-118">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="3a24d-119">Ein optionales **auf NULL** beendetes Array [**von D3DXMACRO-Strukturen,**](d3dxmacro.md) die Präprozessordefinitionen beschreiben.</span><span class="sxs-lookup"><span data-stu-id="3a24d-119">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="3a24d-120">Dieser Wert kann NULL **sein.**</span><span class="sxs-lookup"><span data-stu-id="3a24d-120">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3a24d-121">*pInclude* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="3a24d-121">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a24d-122">Typ: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="3a24d-122">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="3a24d-123">Optionaler Schnittstellenzeiger [**ID3DXInclude**](id3dxinclude.md), der für die Behandlung von \# Includedirektiven verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3a24d-123">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="3a24d-124">Wenn dieser Wert **NULL** ist, \# wird includes entweder beim Kompilieren aus einer Datei berücksichtigt oder verursacht bei der Kompilierung aus einer Ressource oder aus dem Arbeitsspeicher einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="3a24d-124">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="3a24d-125">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="3a24d-125">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a24d-126">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3a24d-126">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3a24d-127">Wenn *pSrcData* einen Texteffekt enthält, können Flags eine Kombination aus [D3DXSHADER-Flags](d3dxshader-flags.md) und [D3DXFX-Flags](d3dxfx.md) sein. Andernfalls enthält *pSrcData* einen binären Effekt, und die einzigen berücksichtigten Flags sind D3DXFX-Flags.</span><span class="sxs-lookup"><span data-stu-id="3a24d-127">If *pSrcData* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *pSrcData* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="3a24d-128">Der Direct3D 10 HLSL-Compiler ist jetzt die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="3a24d-128">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="3a24d-129">Weitere Informationen finden Sie unter [Effektcompilertool.](../direct3dtools/fxc.md)</span><span class="sxs-lookup"><span data-stu-id="3a24d-129">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="3a24d-130">*pPool* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="3a24d-130">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a24d-131">Typ: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="3a24d-131">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="3a24d-132">Zeiger auf ein [**ID3DXEffectPool-Objekt,**](id3dxeffectpool.md) das für freigegebene Parameter verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3a24d-132">Pointer to a [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="3a24d-133">Wenn dieser Wert **NULL** ist, werden keine Parameter freigegeben.</span><span class="sxs-lookup"><span data-stu-id="3a24d-133">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="3a24d-134">*ppEffect* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3a24d-134">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a24d-135">Typ: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="3a24d-135">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="3a24d-136">Gibt einen Zeiger auf eine [**ID3DXEffect-Schnittstelle**](id3dxeffect.md) zurück.</span><span class="sxs-lookup"><span data-stu-id="3a24d-136">Returns a pointer to an [**ID3DXEffect**](id3dxeffect.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="3a24d-137">*ppCompilationErrors* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3a24d-137">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a24d-138">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="3a24d-138">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="3a24d-139">Gibt einen Puffer zurück, der eine Auflistung von Kompilierungsfehlern enthält.</span><span class="sxs-lookup"><span data-stu-id="3a24d-139">Returns a buffer containing a listing of compile errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a24d-140">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3a24d-140">Return value</span></span>

<span data-ttu-id="3a24d-141">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3a24d-141">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3a24d-142">Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3a24d-142">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3a24d-143">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="3a24d-143">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a24d-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3a24d-144">Requirements</span></span>



| <span data-ttu-id="3a24d-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3a24d-145">Requirement</span></span> | <span data-ttu-id="3a24d-146">Wert</span><span class="sxs-lookup"><span data-stu-id="3a24d-146">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a24d-147">Header</span><span class="sxs-lookup"><span data-stu-id="3a24d-147">Header</span></span><br/>  | <dl> <span data-ttu-id="3a24d-148"><dt>D3DX9Effect.h</dt></span><span class="sxs-lookup"><span data-stu-id="3a24d-148"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="3a24d-149">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3a24d-149">Library</span></span><br/> | <dl> <span data-ttu-id="3a24d-150"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="3a24d-150"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="3a24d-151">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3a24d-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a24d-152">Effect-Funktionen</span><span class="sxs-lookup"><span data-stu-id="3a24d-152">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="3a24d-153">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="3a24d-153">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="3a24d-154">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="3a24d-154">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
