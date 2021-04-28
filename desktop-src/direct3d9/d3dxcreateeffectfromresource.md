---
description: 'D3DXCreateEffectFromResource-Funktion: Erstellt einen Effekt aus einer ASCII- oder binären Effektbeschreibung.'
ms.assetid: 8385512c-e93d-4c07-b353-87717eb58bcd
title: D3DXCreateEffectFromResource-Funktion (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectFromResource
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f2a84d2da1f3ca88a117c0150e7b27485838c300
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107688"
---
# <a name="d3dxcreateeffectfromresource-function"></a><span data-ttu-id="ca12d-103">D3DXCreateEffectFromResource-Funktion</span><span class="sxs-lookup"><span data-stu-id="ca12d-103">D3DXCreateEffectFromResource function</span></span>

<span data-ttu-id="ca12d-104">Erstellen Sie einen Effekt aus einer ASCII- oder binären Effektbeschreibung.</span><span class="sxs-lookup"><span data-stu-id="ca12d-104">Create an effect from an ASCII or binary effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca12d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca12d-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectFromResource(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        HMODULE           hSrcModule,
  _In_        LPCTSTR           pSrcResource,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="ca12d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca12d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca12d-107">*pDevice* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ca12d-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca12d-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="ca12d-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="ca12d-109">Zeiger auf das Gerät.</span><span class="sxs-lookup"><span data-stu-id="ca12d-109">Pointer to the device.</span></span>

</dd> <dt>

<span data-ttu-id="ca12d-110">*hSrcModule* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ca12d-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca12d-111">Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ca12d-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ca12d-112">Handle für ein Modul, das die Beschreibung des Effekts enthält.</span><span class="sxs-lookup"><span data-stu-id="ca12d-112">Handle to a module containing the effect description.</span></span> <span data-ttu-id="ca12d-113">Wenn dieser Parameter **NULL** ist, wird das aktuelle Modul verwendet.</span><span class="sxs-lookup"><span data-stu-id="ca12d-113">If this parameter is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="ca12d-114">*pSrcResource* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ca12d-114">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca12d-115">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ca12d-115">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ca12d-116">Zeiger auf die Ressource.</span><span class="sxs-lookup"><span data-stu-id="ca12d-116">Pointer to the resource.</span></span> <span data-ttu-id="ca12d-117">Dieser Parameter unterstützt sowohl Unicode- als auch ANSI-Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="ca12d-117">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="ca12d-118">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="ca12d-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ca12d-119">*pDefine* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ca12d-119">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca12d-120">Typ: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="ca12d-120">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="ca12d-121">Ein optionales Mit **NULL** endendes Array von [**D3DXMACRO-Strukturen,**](d3dxmacro.md) die Präprozessordefinitionen beschreiben.</span><span class="sxs-lookup"><span data-stu-id="ca12d-121">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="ca12d-122">Dieser Wert kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="ca12d-122">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ca12d-123">*pInclude* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ca12d-123">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca12d-124">Typ: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="ca12d-124">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="ca12d-125">Optionaler Schnittstellenzeiger [**ID3DXInclude**](id3dxinclude.md), der für die Behandlung von \# Includedirektiven verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ca12d-125">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="ca12d-126">Wenn dieser Wert **NULL** ist, \# wird includes entweder beim Kompilieren aus einer Datei berücksichtigt oder verursacht bei der Kompilierung aus einer Ressource oder aus dem Arbeitsspeicher einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="ca12d-126">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="ca12d-127">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="ca12d-127">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca12d-128">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ca12d-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ca12d-129">Wenn *hSrcModule* einen Texteffekt enthält, können Flags eine Kombination aus [D3DXSHADER-Flags](d3dxshader-flags.md) und [D3DXFX-Flags](d3dxfx.md) sein. Andernfalls enthält *hSrcModule* einen binären Effekt, und die einzigen berücksichtigten Flags sind D3DXFX-Flags.</span><span class="sxs-lookup"><span data-stu-id="ca12d-129">If *hSrcModule* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *hSrcModule* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="ca12d-130">Der Direct3D 10 HLSL-Compiler ist jetzt die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="ca12d-130">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="ca12d-131">Weitere Informationen finden Sie unter [Effektcompilertool.](../direct3dtools/fxc.md)</span><span class="sxs-lookup"><span data-stu-id="ca12d-131">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="ca12d-132">*pPool* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ca12d-132">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca12d-133">Typ: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="ca12d-133">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="ca12d-134">Zeiger auf ein [**ID3DXEffectPool-Objekt,**](id3dxeffectpool.md) das für freigegebene Parameter verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ca12d-134">Pointer to a [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="ca12d-135">Wenn dieser Wert **NULL** ist, werden keine Parameter freigegeben.</span><span class="sxs-lookup"><span data-stu-id="ca12d-135">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="ca12d-136">*ppEffect* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ca12d-136">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ca12d-137">Typ: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="ca12d-137">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="ca12d-138">Gibt einen Puffer zurück, der den kompilierten Effekt enthält.</span><span class="sxs-lookup"><span data-stu-id="ca12d-138">Returns a buffer containing the compiled effect.</span></span>

</dd> <dt>

<span data-ttu-id="ca12d-139">*ppCompilationErrors* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ca12d-139">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ca12d-140">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="ca12d-140">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="ca12d-141">Gibt einen Puffer zurück, der eine Auflistung von Kompilierungsfehlern enthält.</span><span class="sxs-lookup"><span data-stu-id="ca12d-141">Returns a buffer containing a listing of compile errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca12d-142">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ca12d-142">Return value</span></span>

<span data-ttu-id="ca12d-143">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ca12d-143">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ca12d-144">Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ca12d-144">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ca12d-145">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ca12d-145">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca12d-146">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ca12d-146">Remarks</span></span>

<span data-ttu-id="ca12d-147">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR auflösen.</span><span class="sxs-lookup"><span data-stu-id="ca12d-147">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="ca12d-148">Andernfalls wird der LPCTSTR-Datentyp in LPCSTR auflösen.</span><span class="sxs-lookup"><span data-stu-id="ca12d-148">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="ca12d-149">Die Compilereinstellung bestimmt auch die Funktionsversion.</span><span class="sxs-lookup"><span data-stu-id="ca12d-149">The compiler setting also determines the function version.</span></span> <span data-ttu-id="ca12d-150">Wenn Unicode definiert ist, wird der Funktionsaufruf in D3DXCreateEffectFromResourceW auflösen.</span><span class="sxs-lookup"><span data-stu-id="ca12d-150">If Unicode is defined, the function call resolves to D3DXCreateEffectFromResourceW.</span></span> <span data-ttu-id="ca12d-151">Andernfalls wird der Funktionsaufruf in D3DXCreateEffectFromResourceA auflösen, da ANSI-Zeichenfolgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ca12d-151">Otherwise, the function call resolves to D3DXCreateEffectFromResourceA because ANSI strings are being used.</span></span>

<span data-ttu-id="ca12d-152">D3DXCreateEffectFromResource lädt Daten aus einer Ressource vom Typ RT \_ RCDATA.</span><span class="sxs-lookup"><span data-stu-id="ca12d-152">D3DXCreateEffectFromResource loads data from a resource of type RT\_RCDATA.</span></span> <span data-ttu-id="ca12d-153">Weitere Informationen zu Windows-Ressourcen finden Sie unter MSDN.</span><span class="sxs-lookup"><span data-stu-id="ca12d-153">See MSDN for more information about Windows resources.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca12d-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca12d-154">Requirements</span></span>



| <span data-ttu-id="ca12d-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca12d-155">Requirement</span></span> | <span data-ttu-id="ca12d-156">Wert</span><span class="sxs-lookup"><span data-stu-id="ca12d-156">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca12d-157">Header</span><span class="sxs-lookup"><span data-stu-id="ca12d-157">Header</span></span><br/>  | <dl> <span data-ttu-id="ca12d-158"><dt>D3DX9Effect.h</dt></span><span class="sxs-lookup"><span data-stu-id="ca12d-158"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="ca12d-159">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ca12d-159">Library</span></span><br/> | <dl> <span data-ttu-id="ca12d-160"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="ca12d-160"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ca12d-161">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ca12d-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca12d-162">Effect-Funktionen</span><span class="sxs-lookup"><span data-stu-id="ca12d-162">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="ca12d-163">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="ca12d-163">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="ca12d-164">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="ca12d-164">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
