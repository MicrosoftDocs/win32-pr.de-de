---
description: Erstellen eines Effekts aus einer Beschreibung des ASCII-oder binären Effekts.
ms.assetid: 8385512c-e93d-4c07-b353-87717eb58bcd
title: D3DXCreateEffectFromResource-Funktion (D3DX9Effect. h)
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
ms.openlocfilehash: 36db2c82debc542301ba44d4baa74ecaaf01245e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357262"
---
# <a name="d3dxcreateeffectfromresource-function"></a><span data-ttu-id="017eb-103">D3DXCreateEffectFromResource-Funktion</span><span class="sxs-lookup"><span data-stu-id="017eb-103">D3DXCreateEffectFromResource function</span></span>

<span data-ttu-id="017eb-104">Erstellen eines Effekts aus einer Beschreibung des ASCII-oder binären Effekts.</span><span class="sxs-lookup"><span data-stu-id="017eb-104">Create an effect from an ASCII or binary effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="017eb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="017eb-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="017eb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="017eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="017eb-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="017eb-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="017eb-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="017eb-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="017eb-109">Zeiger auf das Gerät.</span><span class="sxs-lookup"><span data-stu-id="017eb-109">Pointer to the device.</span></span>

</dd> <dt>

<span data-ttu-id="017eb-110">*hsrcmodule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="017eb-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="017eb-111">Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="017eb-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="017eb-112">Handle für ein Modul, das die Beschreibung des Effekts enthält.</span><span class="sxs-lookup"><span data-stu-id="017eb-112">Handle to a module containing the effect description.</span></span> <span data-ttu-id="017eb-113">Wenn dieser Parameter **null** ist, wird das aktuelle Modul verwendet.</span><span class="sxs-lookup"><span data-stu-id="017eb-113">If this parameter is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="017eb-114">*psrkresource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="017eb-114">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="017eb-115">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="017eb-115">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="017eb-116">Ein Zeiger auf die Ressource.</span><span class="sxs-lookup"><span data-stu-id="017eb-116">Pointer to the resource.</span></span> <span data-ttu-id="017eb-117">Dieser Parameter unterstützt Unicode-und ANSI-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="017eb-117">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="017eb-118">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="017eb-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="017eb-119">*pdefinitionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="017eb-119">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="017eb-120">Typ: **Konstanten [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="017eb-120">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="017eb-121">Ein optionales **null** terminiertes Array von [**D3DXMACRO**](d3dxmacro.md) -Strukturen, die Präprozessordefinitionen beschreiben.</span><span class="sxs-lookup"><span data-stu-id="017eb-121">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="017eb-122">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="017eb-122">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="017eb-123">*pinclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="017eb-123">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="017eb-124">Typ: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="017eb-124">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="017eb-125">Optionaler Schnittstellen Zeiger, [**ID3DXInclude**](id3dxinclude.md), der zum Verarbeiten von include-Direktiven verwendet werden soll \# .</span><span class="sxs-lookup"><span data-stu-id="017eb-125">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="017eb-126">Wenn dieser Wert **null** ist, \# wird includes bei der Kompilierung aus einer Datei berücksichtigt, oder es wird ein Fehler ausgelöst, wenn eine Kompilierung aus einer Ressource oder einem Arbeitsspeicher erfolgt.</span><span class="sxs-lookup"><span data-stu-id="017eb-126">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="017eb-127">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="017eb-127">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="017eb-128">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="017eb-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="017eb-129">Wenn *hsrcmodule* einen Text Effekt enthält, können Flags eine Kombination aus [D3DXSHADER-Flags](d3dxshader-flags.md) und [D3DXFX](d3dxfx.md) -Flags sein. Andernfalls enthält *hsrcmodule* einen binären Effekt, und die einzigen Flags, die berücksichtigt werden, sind D3DXFX-Flags.</span><span class="sxs-lookup"><span data-stu-id="017eb-129">If *hSrcModule* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *hSrcModule* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="017eb-130">Der Direct3D 10 HLSL-Compiler ist nun der Standard.</span><span class="sxs-lookup"><span data-stu-id="017eb-130">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="017eb-131">Ausführliche Informationen finden Sie unter [Effect-Compiler-Tool](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="017eb-131">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="017eb-132">*ppool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="017eb-132">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="017eb-133">Typ: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="017eb-133">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="017eb-134">Zeiger auf ein [**ID3DXEffectPool**](id3dxeffectpool.md) -Objekt, das für freigegebene Parameter verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="017eb-134">Pointer to a [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="017eb-135">Wenn dieser Wert **null** ist, werden keine Parameter freigegeben.</span><span class="sxs-lookup"><span data-stu-id="017eb-135">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="017eb-136">*ppeer-ect* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="017eb-136">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="017eb-137">Typ: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="017eb-137">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="017eb-138">Gibt einen Puffer zurück, der den kompilierten Effekt enthält.</span><span class="sxs-lookup"><span data-stu-id="017eb-138">Returns a buffer containing the compiled effect.</span></span>

</dd> <dt>

<span data-ttu-id="017eb-139">*ppcompilationerrors* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="017eb-139">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="017eb-140">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="017eb-140">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="017eb-141">Gibt einen Puffer zurück, der eine Auflistung der Kompilierungsfehler enthält.</span><span class="sxs-lookup"><span data-stu-id="017eb-141">Returns a buffer containing a listing of compile errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="017eb-142">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="017eb-142">Return value</span></span>

<span data-ttu-id="017eb-143">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="017eb-143">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="017eb-144">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="017eb-144">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="017eb-145">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="017eb-145">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="017eb-146">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="017eb-146">Remarks</span></span>

<span data-ttu-id="017eb-147">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="017eb-147">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="017eb-148">Andernfalls wird der LPCTSTR-Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="017eb-148">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="017eb-149">Die Compilereinstellung bestimmt auch die Funktions Version.</span><span class="sxs-lookup"><span data-stu-id="017eb-149">The compiler setting also determines the function version.</span></span> <span data-ttu-id="017eb-150">Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXCreateEffectFromResourceW aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="017eb-150">If Unicode is defined, the function call resolves to D3DXCreateEffectFromResourceW.</span></span> <span data-ttu-id="017eb-151">Andernfalls wird der Funktions Aufruhe in D3DXCreateEffectFromResourceA aufgelöst, da ANSI-Zeichen folgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="017eb-151">Otherwise, the function call resolves to D3DXCreateEffectFromResourceA because ANSI strings are being used.</span></span>

<span data-ttu-id="017eb-152">D3DXCreateEffectFromResource lädt Daten aus einer Ressource vom Typ RT \_ RCDATA.</span><span class="sxs-lookup"><span data-stu-id="017eb-152">D3DXCreateEffectFromResource loads data from a resource of type RT\_RCDATA.</span></span> <span data-ttu-id="017eb-153">Weitere Informationen zu Windows-Ressourcen finden Sie in der MSDN-Website.</span><span class="sxs-lookup"><span data-stu-id="017eb-153">See MSDN for more information about Windows resources.</span></span>

## <a name="requirements"></a><span data-ttu-id="017eb-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="017eb-154">Requirements</span></span>



| <span data-ttu-id="017eb-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="017eb-155">Requirement</span></span> | <span data-ttu-id="017eb-156">Wert</span><span class="sxs-lookup"><span data-stu-id="017eb-156">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="017eb-157">Header</span><span class="sxs-lookup"><span data-stu-id="017eb-157">Header</span></span><br/>  | <dl> <span data-ttu-id="017eb-158"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="017eb-158"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="017eb-159">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="017eb-159">Library</span></span><br/> | <dl> <span data-ttu-id="017eb-160"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="017eb-160"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="017eb-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="017eb-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="017eb-162">Effekt Funktionen</span><span class="sxs-lookup"><span data-stu-id="017eb-162">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="017eb-163">**D3DXCompileShader**</span><span class="sxs-lookup"><span data-stu-id="017eb-163">**D3DXCompileShader**</span></span>](d3dxcompileshader.md)
</dt> <dt>

[<span data-ttu-id="017eb-164">**D3DXCompileShaderFromResource**</span><span class="sxs-lookup"><span data-stu-id="017eb-164">**D3DXCompileShaderFromResource**</span></span>](d3dxcompileshaderfromresource.md)
</dt> </dl>

 

 
