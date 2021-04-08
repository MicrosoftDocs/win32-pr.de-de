---
description: Erstellen eines Effekts aus einer Beschreibung des ASCII-oder binären Effekts.
ms.assetid: b5868ba3-0869-46f7-804f-3103358a3ef5
title: D3DXCreateEffectFromFile-Funktion (D3DX9Effect. h)
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
ms.openlocfilehash: f34d0cdb3ae19772f21d8307fffb395c4d1ac9ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762279"
---
# <a name="d3dxcreateeffectfromfile-function"></a><span data-ttu-id="64d8c-103">D3DXCreateEffectFromFile-Funktion</span><span class="sxs-lookup"><span data-stu-id="64d8c-103">D3DXCreateEffectFromFile function</span></span>

<span data-ttu-id="64d8c-104">Erstellen eines Effekts aus einer Beschreibung des ASCII-oder binären Effekts.</span><span class="sxs-lookup"><span data-stu-id="64d8c-104">Create an effect from an ASCII or binary effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="64d8c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="64d8c-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="64d8c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="64d8c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64d8c-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64d8c-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64d8c-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="64d8c-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="64d8c-109">Zeiger auf das Gerät, das den Effekt erzeugt.</span><span class="sxs-lookup"><span data-stu-id="64d8c-109">Pointer to the device that will create the effect.</span></span> <span data-ttu-id="64d8c-110">Siehe [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="64d8c-110">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> <dt>

<span data-ttu-id="64d8c-111">*psrcfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64d8c-111">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64d8c-112">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="64d8c-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="64d8c-113">Zeiger auf den Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="64d8c-113">Pointer to the filename.</span></span> <span data-ttu-id="64d8c-114">Dieser Parameter unterstützt Unicode-und ANSI-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="64d8c-114">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="64d8c-115">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="64d8c-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="64d8c-116">*pdefinitionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64d8c-116">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64d8c-117">Typ: **Konstanten [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="64d8c-117">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="64d8c-118">Optionales, auf Null endendes Array von Präprozessormakro-Definitionen.</span><span class="sxs-lookup"><span data-stu-id="64d8c-118">Optional NULL-terminated array of preprocessor macro definitions.</span></span> <span data-ttu-id="64d8c-119">Siehe [**D3DXMACRO**](d3dxmacro.md).</span><span class="sxs-lookup"><span data-stu-id="64d8c-119">See [**D3DXMACRO**](d3dxmacro.md).</span></span>

</dd> <dt>

<span data-ttu-id="64d8c-120">*pinclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64d8c-120">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64d8c-121">Typ: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="64d8c-121">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="64d8c-122">Optionaler Schnittstellen Zeiger, [**ID3DXInclude**](id3dxinclude.md), der zum Verarbeiten von include-Direktiven verwendet werden soll \# .</span><span class="sxs-lookup"><span data-stu-id="64d8c-122">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="64d8c-123">Wenn dieser Wert **null** ist, \# wird includes bei der Kompilierung aus einer Datei berücksichtigt, oder es wird ein Fehler ausgelöst, wenn eine Kompilierung aus einer Ressource oder einem Arbeitsspeicher erfolgt.</span><span class="sxs-lookup"><span data-stu-id="64d8c-123">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="64d8c-124">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="64d8c-124">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64d8c-125">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="64d8c-125">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="64d8c-126">Wenn *psrcfile* einen Text Effekt enthält, können Flags eine Kombination aus [D3DXSHADER-Flags](d3dxshader-flags.md) und [D3DXFX](d3dxfx.md) -Flags sein. Andernfalls enthält *psrcfile* einen binären Effekt, und die einzigen Flags, die berücksichtigt werden, sind D3DXFX-Flags.</span><span class="sxs-lookup"><span data-stu-id="64d8c-126">If *pSrcFile* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *pSrcFile* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="64d8c-127">Der Direct3D 10 HLSL-Compiler ist nun der Standard.</span><span class="sxs-lookup"><span data-stu-id="64d8c-127">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="64d8c-128">Ausführliche Informationen finden Sie unter [Effect-Compiler-Tool](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="64d8c-128">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="64d8c-129">*ppool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64d8c-129">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64d8c-130">Typ: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="64d8c-130">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="64d8c-131">Zeiger auf ein [**ID3DXEffectPool**](id3dxeffectpool.md) -Objekt, das für freigegebene Parameter verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="64d8c-131">Pointer to a [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="64d8c-132">Wenn dieser Wert **null** ist, werden keine Parameter freigegeben.</span><span class="sxs-lookup"><span data-stu-id="64d8c-132">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="64d8c-133">*ppeer-ect* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="64d8c-133">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64d8c-134">Typ: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="64d8c-134">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="64d8c-135">Gibt einen Zeiger auf einen Puffer zurück, der den kompilierten Effekt enthält.</span><span class="sxs-lookup"><span data-stu-id="64d8c-135">Returns a pointer to a buffer containing the compiled effect.</span></span> <span data-ttu-id="64d8c-136">Siehe [**ID3DXEffect**](id3dxeffect.md).</span><span class="sxs-lookup"><span data-stu-id="64d8c-136">See [**ID3DXEffect**](id3dxeffect.md).</span></span>

</dd> <dt>

<span data-ttu-id="64d8c-137">*ppcompilationerrors* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="64d8c-137">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64d8c-138">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="64d8c-138">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="64d8c-139">Gibt einen Zeiger auf einen Puffer zurück, der eine Auflistung der Kompilierungsfehler enthält.</span><span class="sxs-lookup"><span data-stu-id="64d8c-139">Returns a pointer to a buffer containing a listing of compile errors.</span></span> <span data-ttu-id="64d8c-140">Siehe [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="64d8c-140">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64d8c-141">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="64d8c-141">Return value</span></span>

<span data-ttu-id="64d8c-142">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="64d8c-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="64d8c-143">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="64d8c-143">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="64d8c-144">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="64d8c-144">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="64d8c-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64d8c-145">Remarks</span></span>

<span data-ttu-id="64d8c-146">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="64d8c-146">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="64d8c-147">Andernfalls wird der LPCTSTR-Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="64d8c-147">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="64d8c-148">Die Compilereinstellung bestimmt auch die Funktions Version.</span><span class="sxs-lookup"><span data-stu-id="64d8c-148">The compiler setting also determines the function version.</span></span> <span data-ttu-id="64d8c-149">Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXCreateEffectFromFileW aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="64d8c-149">If Unicode is defined, the function call resolves to D3DXCreateEffectFromFileW.</span></span> <span data-ttu-id="64d8c-150">Andernfalls wird der Funktions Aufruhe in D3DXCreateEffectFromFileA aufgelöst, da ANSI-Zeichen folgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="64d8c-150">Otherwise, the function call resolves to D3DXCreateEffectFromFileA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="64d8c-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="64d8c-151">Requirements</span></span>



| <span data-ttu-id="64d8c-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="64d8c-152">Requirement</span></span> | <span data-ttu-id="64d8c-153">Wert</span><span class="sxs-lookup"><span data-stu-id="64d8c-153">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="64d8c-154">Header</span><span class="sxs-lookup"><span data-stu-id="64d8c-154">Header</span></span><br/>  | <dl> <span data-ttu-id="64d8c-155"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="64d8c-155"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="64d8c-156">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="64d8c-156">Library</span></span><br/> | <dl> <span data-ttu-id="64d8c-157"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="64d8c-157"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="64d8c-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64d8c-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64d8c-159">Effekt Funktionen</span><span class="sxs-lookup"><span data-stu-id="64d8c-159">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="64d8c-160">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="64d8c-160">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="64d8c-161">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="64d8c-161">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
