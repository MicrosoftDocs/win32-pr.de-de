---
description: Erstellen eines Effekts aus einer Beschreibung des ASCII-oder binären Effekts. Diese Funktion ist eine erweiterte Version von D3DXCreateEffectFromFile, mit der eine Anwendung steuern kann, welche Parameter vom Effects-System ignoriert werden.
ms.assetid: 963caa1e-bc1a-4d4b-bdb1-50b17d8b4132
title: D3DXCreateEffectFromFileEx-Funktion (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectFromFileEx
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b3d97c5aa23dd0711cfb00585e5b8ba7d410fc02
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355218"
---
# <a name="d3dxcreateeffectfromfileex-function"></a><span data-ttu-id="08ab5-104">D3DXCreateEffectFromFileEx-Funktion</span><span class="sxs-lookup"><span data-stu-id="08ab5-104">D3DXCreateEffectFromFileEx function</span></span>

<span data-ttu-id="08ab5-105">Erstellen eines Effekts aus einer Beschreibung des ASCII-oder binären Effekts.</span><span class="sxs-lookup"><span data-stu-id="08ab5-105">Create an effect from an ASCII or binary effect description.</span></span> <span data-ttu-id="08ab5-106">Diese Funktion ist eine erweiterte Version von [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) , mit der eine Anwendung steuern kann, welche Parameter vom Effects-System ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="08ab5-106">This function is an extended version of [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) that allows an application to control which parameters are ignored by the effects system.</span></span>

## <a name="syntax"></a><span data-ttu-id="08ab5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="08ab5-107">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectFromFileEx(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        LPCTSTR           pSrcFile,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        LPCSTR            pSkipConstants,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="08ab5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="08ab5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08ab5-109">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08ab5-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08ab5-110">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="08ab5-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="08ab5-111">Zeiger auf das Gerät, das den Effekt erzeugt.</span><span class="sxs-lookup"><span data-stu-id="08ab5-111">Pointer to the device that will create the effect.</span></span> <span data-ttu-id="08ab5-112">Siehe [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="08ab5-112">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> <dt>

<span data-ttu-id="08ab5-113">*psrcfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08ab5-113">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08ab5-114">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="08ab5-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="08ab5-115">Zeiger auf den Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="08ab5-115">Pointer to the filename.</span></span> <span data-ttu-id="08ab5-116">Dieser Parameter unterstützt Unicode-und ANSI-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="08ab5-116">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="08ab5-117">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="08ab5-117">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="08ab5-118">*pdefinitionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08ab5-118">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08ab5-119">Typ: **Konstanten [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="08ab5-119">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="08ab5-120">Optionales, auf Null endendes Array von Präprozessormakro-Definitionen.</span><span class="sxs-lookup"><span data-stu-id="08ab5-120">Optional NULL-terminated array of preprocessor macro definitions.</span></span> <span data-ttu-id="08ab5-121">Siehe [**D3DXMACRO**](d3dxmacro.md).</span><span class="sxs-lookup"><span data-stu-id="08ab5-121">See [**D3DXMACRO**](d3dxmacro.md).</span></span>

</dd> <dt>

<span data-ttu-id="08ab5-122">*pinclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08ab5-122">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08ab5-123">Typ: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="08ab5-123">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="08ab5-124">Optionaler Schnittstellen Zeiger, [**ID3DXInclude**](id3dxinclude.md), der zum Verarbeiten von include-Direktiven verwendet werden soll \# .</span><span class="sxs-lookup"><span data-stu-id="08ab5-124">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="08ab5-125">Wenn dieser Wert **null** ist, \# wird includes bei der Kompilierung aus einer Datei berücksichtigt, oder es wird ein Fehler ausgelöst, wenn eine Kompilierung aus einer Ressource oder einem Arbeitsspeicher erfolgt.</span><span class="sxs-lookup"><span data-stu-id="08ab5-125">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="08ab5-126">*pskipkonstanten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08ab5-126">*pSkipConstants* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08ab5-127">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="08ab5-127">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="08ab5-128">Eine Zeichenfolge von Effekt Parametern, die vom Effektsystem ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="08ab5-128">A string of effect parameters that will be ignored by the effect system.</span></span> <span data-ttu-id="08ab5-129">Die Zeichenfolge muss **null** sein und muss den Namen jeder von der Anwendung verwalteten Konstante enthalten, die durch ein Semikolon getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="08ab5-129">The string must be **NULL** terminated, and needs to contain the name of each application-managed constant separated by a semicolon.</span></span>

</dd> <dt>

<span data-ttu-id="08ab5-130">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="08ab5-130">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08ab5-131">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="08ab5-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="08ab5-132">Wenn *psrcfile* einen Text Effekt enthält, können Flags eine Kombination aus [D3DXSHADER-Flags](d3dxshader-flags.md) und [D3DXFX](d3dxfx.md) -Flags sein. Andernfalls enthält *psrcfile* einen binären Effekt, und die einzigen Flags, die berücksichtigt werden, sind D3DXFX-Flags.</span><span class="sxs-lookup"><span data-stu-id="08ab5-132">If *pSrcFile* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *pSrcFile* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="08ab5-133">Der Direct3D 10 HLSL-Compiler ist nun der Standard.</span><span class="sxs-lookup"><span data-stu-id="08ab5-133">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="08ab5-134">Ausführliche Informationen finden Sie unter [Effect-Compiler-Tool](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="08ab5-134">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="08ab5-135">*ppool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08ab5-135">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08ab5-136">Typ: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="08ab5-136">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="08ab5-137">Zeiger auf ein [**ID3DXEffectPool**](id3dxeffectpool.md) -Objekt, das für freigegebene Parameter verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="08ab5-137">Pointer to a [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="08ab5-138">Wenn dieser Wert **null** ist, werden keine Parameter freigegeben.</span><span class="sxs-lookup"><span data-stu-id="08ab5-138">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="08ab5-139">*ppeer-ect* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="08ab5-139">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="08ab5-140">Typ: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="08ab5-140">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="08ab5-141">Gibt einen Zeiger auf einen Puffer zurück, der den kompilierten Effekt enthält.</span><span class="sxs-lookup"><span data-stu-id="08ab5-141">Returns a pointer to a buffer containing the compiled effect.</span></span> <span data-ttu-id="08ab5-142">Siehe [**ID3DXEffect**](id3dxeffect.md).</span><span class="sxs-lookup"><span data-stu-id="08ab5-142">See [**ID3DXEffect**](id3dxeffect.md).</span></span>

</dd> <dt>

<span data-ttu-id="08ab5-143">*ppcompilationerrors* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="08ab5-143">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="08ab5-144">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="08ab5-144">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="08ab5-145">Gibt einen Zeiger auf einen Puffer zurück, der eine Auflistung der Kompilierungsfehler enthält.</span><span class="sxs-lookup"><span data-stu-id="08ab5-145">Returns a pointer to a buffer containing a listing of compile errors.</span></span> <span data-ttu-id="08ab5-146">Siehe [**ID3DXBuffer**](id3dxbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="08ab5-146">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08ab5-147">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="08ab5-147">Return value</span></span>

<span data-ttu-id="08ab5-148">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="08ab5-148">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="08ab5-149">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="08ab5-149">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="08ab5-150">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="08ab5-150">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="08ab5-151">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08ab5-151">Remarks</span></span>

<span data-ttu-id="08ab5-152">Diese Funktion ist eine erweiterte Version von [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) , mit der eine Anwendung angeben kann, welche Effekt Konstanten von der Anwendung verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="08ab5-152">This function is an extended version of [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) that allows an application to specify which effect constants will be managed by the application.</span></span> <span data-ttu-id="08ab5-153">Eine Konstante, die von der Anwendung verwaltet wird, wird vom Effects-System ignoriert.</span><span class="sxs-lookup"><span data-stu-id="08ab5-153">A constant that is managed by the application is ignored by the effects system.</span></span> <span data-ttu-id="08ab5-154">Das heißt, die Anwendung ist dafür verantwortlich, die Konstante zu initialisieren und ihren Zustand zu speichern und wiederherzustellen, wenn dies angemessen ist.</span><span class="sxs-lookup"><span data-stu-id="08ab5-154">That is, the application is responsible for initializing the constant as well as saving and restoring its state whenever appropriate.</span></span>

<span data-ttu-id="08ab5-155">Diese Funktion überprüft jede Konstante in pskipkonstanten, um Folgendes anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="08ab5-155">This function checks each constant in pSkipConstants to see that:</span></span>

-   <span data-ttu-id="08ab5-156">Er ist an ein konstantes Register gebunden.</span><span class="sxs-lookup"><span data-stu-id="08ab5-156">It is bound to a constant register.</span></span>
-   <span data-ttu-id="08ab5-157">Sie wird nur im HLSL-Shader-Code verwendet.</span><span class="sxs-lookup"><span data-stu-id="08ab5-157">It is only used in HLSL shader code.</span></span>

<span data-ttu-id="08ab5-158">Wenn eine Konstante in der Zeichenfolge benannt wird, die nicht in der Auswirkung vorhanden ist, wird Sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="08ab5-158">If a constant is named in the string that is not present in the effect, it is ignored.</span></span>

<span data-ttu-id="08ab5-159">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="08ab5-159">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="08ab5-160">Andernfalls wird der LPCTSTR-Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="08ab5-160">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="08ab5-161">Die Compilereinstellung bestimmt auch die Funktions Version.</span><span class="sxs-lookup"><span data-stu-id="08ab5-161">The compiler setting also determines the function version.</span></span> <span data-ttu-id="08ab5-162">Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXCreateEffectFromFileW aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="08ab5-162">If Unicode is defined, the function call resolves to D3DXCreateEffectFromFileW.</span></span> <span data-ttu-id="08ab5-163">Andernfalls wird der Funktions Aufruhe in D3DXCreateEffectFromFileA aufgelöst, da ANSI-Zeichen folgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="08ab5-163">Otherwise, the function call resolves to D3DXCreateEffectFromFileA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="08ab5-164">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="08ab5-164">Requirements</span></span>



| <span data-ttu-id="08ab5-165">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08ab5-165">Requirement</span></span> | <span data-ttu-id="08ab5-166">Wert</span><span class="sxs-lookup"><span data-stu-id="08ab5-166">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="08ab5-167">Header</span><span class="sxs-lookup"><span data-stu-id="08ab5-167">Header</span></span><br/>  | <dl> <span data-ttu-id="08ab5-168"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="08ab5-168"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="08ab5-169">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="08ab5-169">Library</span></span><br/> | <dl> <span data-ttu-id="08ab5-170"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="08ab5-170"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="08ab5-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08ab5-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08ab5-172">Effekt Funktionen</span><span class="sxs-lookup"><span data-stu-id="08ab5-172">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="08ab5-173">**D3DXCreateEffectEx**</span><span class="sxs-lookup"><span data-stu-id="08ab5-173">**D3DXCreateEffectEx**</span></span>](d3dxcreateeffectex.md)
</dt> <dt>

[<span data-ttu-id="08ab5-174">**D3DXCreateEffectFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="08ab5-174">**D3DXCreateEffectFromResourceEx**</span></span>](d3dxcreateeffectfromresourceex.md)
</dt> </dl>

 

 
