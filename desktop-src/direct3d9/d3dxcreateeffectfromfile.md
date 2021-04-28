---
description: 'D3DXCreateEffectFromFile-Funktion: Erstellt einen Effekt aus einer ASCII- oder Binäreffektbeschreibung.'
ms.assetid: b5868ba3-0869-46f7-804f-3103358a3ef5
title: D3DXCreateEffectFromFile-Funktion (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectFromFile
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d8b2afdd1e8008bc8e03efa670e5a4b37b6dc9f8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094318"
---
# <a name="d3dxcreateeffectfromfile-function"></a><span data-ttu-id="1594e-103">D3DXCreateEffectFromFile-Funktion</span><span class="sxs-lookup"><span data-stu-id="1594e-103">D3DXCreateEffectFromFile function</span></span>

<span data-ttu-id="1594e-104">Erstellen Sie einen Effekt aus einer ASCII- oder binären Effektbeschreibung.</span><span class="sxs-lookup"><span data-stu-id="1594e-104">Create an effect from an ASCII or binary effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="1594e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1594e-105">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectFromFile(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        LPCTSTR           pSrcFile,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="1594e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1594e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1594e-107">*pDevice* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="1594e-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1594e-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="1594e-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="1594e-109">Zeiger auf das Gerät, das den Effekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="1594e-109">Pointer to the device that will create the effect.</span></span> <span data-ttu-id="1594e-110">Siehe [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="1594e-110">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> <dt>

<span data-ttu-id="1594e-111">*pSrcFile* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="1594e-111">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1594e-112">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1594e-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1594e-113">Zeiger auf den Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="1594e-113">Pointer to the filename.</span></span> <span data-ttu-id="1594e-114">Dieser Parameter unterstützt sowohl Unicode- als auch ANSI-Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="1594e-114">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="1594e-115">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="1594e-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1594e-116">*pDefdefine* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="1594e-116">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1594e-117">Typ: **const [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="1594e-117">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="1594e-118">Optionales auf NULL beendetes Array von Präprozessormakrodefinitionen.</span><span class="sxs-lookup"><span data-stu-id="1594e-118">Optional NULL-terminated array of preprocessor macro definitions.</span></span> <span data-ttu-id="1594e-119">Siehe [**D3DXMACRO**](d3dxmacro.md).</span><span class="sxs-lookup"><span data-stu-id="1594e-119">See [**D3DXMACRO**](d3dxmacro.md).</span></span>

</dd> <dt>

<span data-ttu-id="1594e-120">*pInclude* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="1594e-120">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1594e-121">Typ: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="1594e-121">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="1594e-122">Optionaler Schnittstellenzeiger [**ID3DXInclude**](id3dxinclude.md), der für die Behandlung von Include-Direktiven \# verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1594e-122">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="1594e-123">Wenn dieser Wert **NULL ist,** wird includes entweder beim Kompilieren aus einer Datei oder beim Kompilieren aus einer Ressource oder einem Arbeitsspeicher \# zu einem Fehler führen.</span><span class="sxs-lookup"><span data-stu-id="1594e-123">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="1594e-124">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="1594e-124">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1594e-125">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1594e-125">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1594e-126">Wenn *pSrcFile* einen Texteffekt enthält, können Flags eine Kombination aus [D3DXSHADER-Flags](d3dxshader-flags.md) und [D3DXFX-Flags](d3dxfx.md) sein. Andernfalls enthält *pSrcFile* einen binären Effekt, und die einzigen berücksichtigten Flags sind D3DXFX-Flags.</span><span class="sxs-lookup"><span data-stu-id="1594e-126">If *pSrcFile* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *pSrcFile* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="1594e-127">Der Direct3D 10 HLSL-Compiler ist jetzt die Standardeinstellung.</span><span class="sxs-lookup"><span data-stu-id="1594e-127">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="1594e-128">Weitere Informationen finden Sie unter [Effektcompilertool.](../direct3dtools/fxc.md)</span><span class="sxs-lookup"><span data-stu-id="1594e-128">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="1594e-129">*pPool* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="1594e-129">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1594e-130">Typ: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="1594e-130">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="1594e-131">Zeiger auf ein [**ID3DXEffectPool-Objekt,**](id3dxeffectpool.md) das für freigegebene Parameter verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1594e-131">Pointer to a [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="1594e-132">Wenn dieser Wert **NULL** ist, werden keine Parameter freigegeben.</span><span class="sxs-lookup"><span data-stu-id="1594e-132">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="1594e-133">*ppEffect* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1594e-133">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1594e-134">Typ: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="1594e-134">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="1594e-135">Gibt einen Zeiger auf einen Puffer zurück, der den kompilierten Effekt enthält.</span><span class="sxs-lookup"><span data-stu-id="1594e-135">Returns a pointer to a buffer containing the compiled effect.</span></span> <span data-ttu-id="1594e-136">Siehe [**ID3DXEffect**](id3dxeffect.md).</span><span class="sxs-lookup"><span data-stu-id="1594e-136">See [**ID3DXEffect**](id3dxeffect.md).</span></span>

</dd> <dt>

<span data-ttu-id="1594e-137">*ppCompilationErrors* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1594e-137">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1594e-138">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="1594e-138">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="1594e-139">Gibt einen Zeiger auf einen Puffer zurück, der eine Auflistung von Kompilierungsfehlern enthält.</span><span class="sxs-lookup"><span data-stu-id="1594e-139">Returns a pointer to a buffer containing a listing of compile errors.</span></span> <span data-ttu-id="1594e-140">Siehe [**ID3DXBuffer.**](id3dxbuffer.md)</span><span class="sxs-lookup"><span data-stu-id="1594e-140">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1594e-141">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1594e-141">Return value</span></span>

<span data-ttu-id="1594e-142">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1594e-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1594e-143">Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1594e-143">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1594e-144">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="1594e-144">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="1594e-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1594e-145">Remarks</span></span>

<span data-ttu-id="1594e-146">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="1594e-146">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="1594e-147">Andernfalls wird der LPCTSTR-Datentyp in LPCSTR auflösen.</span><span class="sxs-lookup"><span data-stu-id="1594e-147">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="1594e-148">Die Compilereinstellung bestimmt auch die Funktionsversion.</span><span class="sxs-lookup"><span data-stu-id="1594e-148">The compiler setting also determines the function version.</span></span> <span data-ttu-id="1594e-149">Wenn Unicode definiert ist, wird der Funktionsaufruf in D3DXCreateEffectFromFileW auflösen.</span><span class="sxs-lookup"><span data-stu-id="1594e-149">If Unicode is defined, the function call resolves to D3DXCreateEffectFromFileW.</span></span> <span data-ttu-id="1594e-150">Andernfalls wird der Funktionsaufruf in D3DXCreateEffectFromFileA auflösen, da ANSI-Zeichenfolgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1594e-150">Otherwise, the function call resolves to D3DXCreateEffectFromFileA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="1594e-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1594e-151">Requirements</span></span>



| <span data-ttu-id="1594e-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1594e-152">Requirement</span></span> | <span data-ttu-id="1594e-153">Wert</span><span class="sxs-lookup"><span data-stu-id="1594e-153">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1594e-154">Header</span><span class="sxs-lookup"><span data-stu-id="1594e-154">Header</span></span><br/>  | <dl> <span data-ttu-id="1594e-155"><dt>D3DX9Effect.h</dt></span><span class="sxs-lookup"><span data-stu-id="1594e-155"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="1594e-156">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1594e-156">Library</span></span><br/> | <dl> <span data-ttu-id="1594e-157"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="1594e-157"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="1594e-158">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1594e-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1594e-159">Effect-Funktionen</span><span class="sxs-lookup"><span data-stu-id="1594e-159">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="1594e-160">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="1594e-160">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="1594e-161">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="1594e-161">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
