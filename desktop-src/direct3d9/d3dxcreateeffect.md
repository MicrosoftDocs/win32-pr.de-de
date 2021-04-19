---
description: Erstellen eines Effekts aus einer Beschreibung des ASCII-oder binären Effekts.
ms.assetid: 1cbd91f2-3cda-4770-a3c5-b1e6702628d1
title: D3DXCreateEffect-Funktion (D3DX9Effect. h)
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
ms.openlocfilehash: 3d5ac013617368ba4d702815d79aa411ea2988b3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367451"
---
# <a name="d3dxcreateeffect-function"></a><span data-ttu-id="1b7da-103">D3DXCreateEffect-Funktion</span><span class="sxs-lookup"><span data-stu-id="1b7da-103">D3DXCreateEffect function</span></span>

<span data-ttu-id="1b7da-104">Erstellen eines Effekts aus einer Beschreibung des ASCII-oder binären Effekts.</span><span class="sxs-lookup"><span data-stu-id="1b7da-104">Create an effect from an ASCII or binary effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b7da-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b7da-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="1b7da-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b7da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b7da-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b7da-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b7da-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="1b7da-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="1b7da-109">Zeiger auf das Gerät, das den Effekt erzeugt.</span><span class="sxs-lookup"><span data-stu-id="1b7da-109">Pointer to the device that will create the effect.</span></span> <span data-ttu-id="1b7da-110">Siehe [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="1b7da-110">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> <dt>

<span data-ttu-id="1b7da-111">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b7da-111">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b7da-112">Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1b7da-112">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1b7da-113">Zeiger auf einen Puffer, der eine Beschreibung des Effekts enthält.</span><span class="sxs-lookup"><span data-stu-id="1b7da-113">Pointer to a buffer containing an effect description.</span></span>

</dd> <dt>

<span data-ttu-id="1b7da-114">*Srcdatalen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b7da-114">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b7da-115">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1b7da-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1b7da-116">Länge der Effekt Daten in Bytes.</span><span class="sxs-lookup"><span data-stu-id="1b7da-116">Length of the effect data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="1b7da-117">*pdefinitionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b7da-117">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b7da-118">Typ: **Konstanten [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="1b7da-118">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="1b7da-119">Ein optionales **null** terminiertes Array von [**D3DXMACRO**](d3dxmacro.md) -Strukturen, die Präprozessordefinitionen beschreiben.</span><span class="sxs-lookup"><span data-stu-id="1b7da-119">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="1b7da-120">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="1b7da-120">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1b7da-121">*pinclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b7da-121">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b7da-122">Typ: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="1b7da-122">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="1b7da-123">Optionaler Schnittstellen Zeiger, [**ID3DXInclude**](id3dxinclude.md), der zum Verarbeiten von include-Direktiven verwendet werden soll \# .</span><span class="sxs-lookup"><span data-stu-id="1b7da-123">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="1b7da-124">Wenn dieser Wert **null** ist, \# wird includes bei der Kompilierung aus einer Datei berücksichtigt, oder es wird ein Fehler ausgelöst, wenn eine Kompilierung aus einer Ressource oder einem Arbeitsspeicher erfolgt.</span><span class="sxs-lookup"><span data-stu-id="1b7da-124">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="1b7da-125">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="1b7da-125">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b7da-126">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1b7da-126">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1b7da-127">Wenn *pSrcData* einen Text Effekt enthält, können Flags eine Kombination aus [D3DXSHADER-Flags](d3dxshader-flags.md) und [D3DXFX](d3dxfx.md) -Flags sein. Andernfalls enthält *pSrcData* einen binären Effekt, und die einzigen Flags, die berücksichtigt werden, sind D3DXFX-Flags.</span><span class="sxs-lookup"><span data-stu-id="1b7da-127">If *pSrcData* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *pSrcData* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="1b7da-128">Der Direct3D 10 HLSL-Compiler ist nun der Standard.</span><span class="sxs-lookup"><span data-stu-id="1b7da-128">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="1b7da-129">Ausführliche Informationen finden Sie unter [Effect-Compiler-Tool](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="1b7da-129">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="1b7da-130">*ppool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b7da-130">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b7da-131">Typ: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="1b7da-131">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="1b7da-132">Zeiger auf ein [**ID3DXEffectPool**](id3dxeffectpool.md) -Objekt, das für freigegebene Parameter verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1b7da-132">Pointer to a [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="1b7da-133">Wenn dieser Wert **null** ist, werden keine Parameter freigegeben.</span><span class="sxs-lookup"><span data-stu-id="1b7da-133">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="1b7da-134">*ppeer-ect* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1b7da-134">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b7da-135">Typ: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="1b7da-135">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="1b7da-136">Gibt einen Zeiger auf eine [**ID3DXEffect**](id3dxeffect.md) -Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="1b7da-136">Returns a pointer to an [**ID3DXEffect**](id3dxeffect.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="1b7da-137">*ppcompilationerrors* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1b7da-137">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b7da-138">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="1b7da-138">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="1b7da-139">Gibt einen Puffer zurück, der eine Auflistung der Kompilierungsfehler enthält.</span><span class="sxs-lookup"><span data-stu-id="1b7da-139">Returns a buffer containing a listing of compile errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b7da-140">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1b7da-140">Return value</span></span>

<span data-ttu-id="1b7da-141">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1b7da-141">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1b7da-142">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1b7da-142">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1b7da-143">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="1b7da-143">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b7da-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1b7da-144">Requirements</span></span>



| <span data-ttu-id="1b7da-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b7da-145">Requirement</span></span> | <span data-ttu-id="1b7da-146">Wert</span><span class="sxs-lookup"><span data-stu-id="1b7da-146">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b7da-147">Header</span><span class="sxs-lookup"><span data-stu-id="1b7da-147">Header</span></span><br/>  | <dl> <span data-ttu-id="1b7da-148"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b7da-148"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="1b7da-149">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1b7da-149">Library</span></span><br/> | <dl> <span data-ttu-id="1b7da-150"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1b7da-150"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="1b7da-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b7da-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b7da-152">Effekt Funktionen</span><span class="sxs-lookup"><span data-stu-id="1b7da-152">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="1b7da-153">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="1b7da-153">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="1b7da-154">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="1b7da-154">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
