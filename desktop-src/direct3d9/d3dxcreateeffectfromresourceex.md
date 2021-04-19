---
description: Erstellen eines Effekts aus einer Beschreibung des ASCII-oder binären Effekts. Dies ist eine erweiterte Version von D3DXCreateEffectFromResource, mit der eine Anwendung steuern kann, welche Parameter vom Effects-System ignoriert werden.
ms.assetid: 5937bdb1-750a-41f8-a49d-3643427f3e3c
title: D3DXCreateEffectFromResourceEx-Funktion (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectFromResourceEx
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d0ae7a0ee43f93019f3c4c1f6145b3d8aa0e4367
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363996"
---
# <a name="d3dxcreateeffectfromresourceex-function"></a><span data-ttu-id="08538-104">D3DXCreateEffectFromResourceEx-Funktion</span><span class="sxs-lookup"><span data-stu-id="08538-104">D3DXCreateEffectFromResourceEx function</span></span>

<span data-ttu-id="08538-105">Erstellen eines Effekts aus einer Beschreibung des ASCII-oder binären Effekts.</span><span class="sxs-lookup"><span data-stu-id="08538-105">Create an effect from an ASCII or binary effect description.</span></span> <span data-ttu-id="08538-106">Dies ist eine erweiterte Version von [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md) , mit der eine Anwendung steuern kann, welche Parameter vom Effects-System ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="08538-106">This is an extended version of [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md) that allows an application to control which parameters are ignored by the effects system.</span></span>

## <a name="syntax"></a><span data-ttu-id="08538-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="08538-107">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectFromResourceEx(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        HMODULE           hSrcModule,
  _In_        LPCTSTR           pSrcResource,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        LPCSTR            pSkipConstants,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="08538-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="08538-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08538-109">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08538-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08538-110">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="08538-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="08538-111">Zeiger auf das Gerät.</span><span class="sxs-lookup"><span data-stu-id="08538-111">Pointer to the device.</span></span>

</dd> <dt>

<span data-ttu-id="08538-112">*hsrcmodule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08538-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08538-113">Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="08538-113">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="08538-114">Handle für ein Modul, das die Beschreibung des Effekts enthält.</span><span class="sxs-lookup"><span data-stu-id="08538-114">Handle to a module containing the effect description.</span></span> <span data-ttu-id="08538-115">Wenn dieser Parameter **null** ist, wird das aktuelle Modul verwendet.</span><span class="sxs-lookup"><span data-stu-id="08538-115">If this parameter is **NULL**, the current module will be used.</span></span>

</dd> <dt>

<span data-ttu-id="08538-116">*psrkresource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08538-116">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08538-117">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="08538-117">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="08538-118">Ein Zeiger auf die Ressource.</span><span class="sxs-lookup"><span data-stu-id="08538-118">Pointer to the resource.</span></span> <span data-ttu-id="08538-119">Dieser Parameter unterstützt Unicode-und ANSI-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="08538-119">This parameter supports both Unicode and ANSI strings.</span></span> <span data-ttu-id="08538-120">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="08538-120">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="08538-121">*pdefinitionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08538-121">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08538-122">Typ: **Konstanten [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="08538-122">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="08538-123">Ein optionales **null** terminiertes Array von [**D3DXMACRO**](d3dxmacro.md) -Strukturen, die Präprozessordefinitionen beschreiben.</span><span class="sxs-lookup"><span data-stu-id="08538-123">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="08538-124">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="08538-124">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="08538-125">*pinclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08538-125">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08538-126">Typ: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="08538-126">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="08538-127">Optionaler Schnittstellen Zeiger, [**ID3DXInclude**](id3dxinclude.md), der zum Verarbeiten von include-Direktiven verwendet werden soll \# .</span><span class="sxs-lookup"><span data-stu-id="08538-127">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="08538-128">Wenn dieser Wert **null** ist, \# wird includes bei der Kompilierung aus einer Datei berücksichtigt, oder es wird ein Fehler ausgelöst, wenn eine Kompilierung aus einer Ressource oder einem Arbeitsspeicher erfolgt.</span><span class="sxs-lookup"><span data-stu-id="08538-128">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="08538-129">*pskipkonstanten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08538-129">*pSkipConstants* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08538-130">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="08538-130">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="08538-131">Eine Zeichenfolge von Effekt Parametern, die vom Effektsystem ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="08538-131">A string of effect parameters that will be ignored by the effect system.</span></span> <span data-ttu-id="08538-132">Die Zeichenfolge muss **null** sein und muss den Namen jeder von der Anwendung verwalteten Konstante enthalten, die durch ein Semikolon getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="08538-132">The string must be **NULL** terminated, and needs to contain the name of each application-managed constant separated by a semicolon.</span></span>

</dd> <dt>

<span data-ttu-id="08538-133">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="08538-133">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08538-134">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="08538-134">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="08538-135">Wenn *psrkresource* einen Text Effekt enthält, können Flags eine Kombination aus [D3DXSHADER-Flags](d3dxshader-flags.md) und [D3DXFX](d3dxfx.md) -Flags sein. Andernfalls enthält *psrkresource* einen binären Effekt, und die einzigen Flags, die berücksichtigt werden, sind D3DXFX-Flags.</span><span class="sxs-lookup"><span data-stu-id="08538-135">If *pSrcResource* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *pSrcResource* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="08538-136">Der Direct3D 10 HLSL-Compiler ist nun der Standard.</span><span class="sxs-lookup"><span data-stu-id="08538-136">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="08538-137">Ausführliche Informationen finden Sie unter [Effect-Compiler-Tool](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="08538-137">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="08538-138">*ppool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08538-138">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08538-139">Typ: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="08538-139">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="08538-140">Zeiger auf ein [**ID3DXEffectPool**](id3dxeffectpool.md) -Objekt, das für freigegebene Parameter verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="08538-140">Pointer to an [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="08538-141">Wenn dieser Wert **null** ist, werden keine Parameter freigegeben.</span><span class="sxs-lookup"><span data-stu-id="08538-141">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="08538-142">*ppeer-ect* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="08538-142">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="08538-143">Typ: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="08538-143">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="08538-144">Gibt einen Puffer zurück, der den kompilierten Effekt enthält.</span><span class="sxs-lookup"><span data-stu-id="08538-144">Returns a buffer containing the compiled effect.</span></span>

</dd> <dt>

<span data-ttu-id="08538-145">*ppcompilationerrors* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="08538-145">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="08538-146">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="08538-146">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="08538-147">Gibt einen Puffer zurück, der eine Auflistung der Kompilierungsfehler enthält.</span><span class="sxs-lookup"><span data-stu-id="08538-147">Returns a buffer containing a listing of compile errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08538-148">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="08538-148">Return value</span></span>

<span data-ttu-id="08538-149">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="08538-149">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="08538-150">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="08538-150">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="08538-151">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="08538-151">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="08538-152">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08538-152">Remarks</span></span>

<span data-ttu-id="08538-153">Diese Funktion ist eine erweiterte Version von [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md) , mit der eine Anwendung angeben kann, welche Effekt Konstanten von der Anwendung verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="08538-153">This function is an extended version of [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md) that allows an application to specify which effect constants will be managed by the application.</span></span> <span data-ttu-id="08538-154">Eine Konstante, die von der Anwendung verwaltet wird, wird vom Effects-System ignoriert.</span><span class="sxs-lookup"><span data-stu-id="08538-154">A constant that is managed by the application is ignored by the effects system.</span></span> <span data-ttu-id="08538-155">Das heißt, die Anwendung ist dafür verantwortlich, die Konstante zu initialisieren und ihren Zustand zu speichern und wiederherzustellen, wenn dies angemessen ist.</span><span class="sxs-lookup"><span data-stu-id="08538-155">That is, the application is responsible for initializing the constant as well as saving and restoring its state whenever appropriate.</span></span>

<span data-ttu-id="08538-156">Diese Funktion überprüft jede Konstante in pskipkonstanten, um Folgendes anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="08538-156">This function checks each constant in pSkipConstants to see that:</span></span>

-   <span data-ttu-id="08538-157">Er ist an ein konstantes Register gebunden.</span><span class="sxs-lookup"><span data-stu-id="08538-157">It is bound to a constant register.</span></span>
-   <span data-ttu-id="08538-158">Sie wird nur im HLSL-Shader-Code verwendet.</span><span class="sxs-lookup"><span data-stu-id="08538-158">It is only used in HLSL shader code.</span></span>

<span data-ttu-id="08538-159">Wenn eine Konstante in der Zeichenfolge benannt wird, die nicht in der Auswirkung vorhanden ist, wird Sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="08538-159">If a constant is named in the string that is not present in the effect, it is ignored.</span></span>

<span data-ttu-id="08538-160">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="08538-160">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="08538-161">Andernfalls wird der LPCTSTR-Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="08538-161">Otherwise, the LPCTSTR data type resolves to LPCSTR.</span></span>

<span data-ttu-id="08538-162">Die Compilereinstellung bestimmt auch die Funktions Version.</span><span class="sxs-lookup"><span data-stu-id="08538-162">The compiler setting also determines the function version.</span></span> <span data-ttu-id="08538-163">Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXCreateEffectFromResourceW aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="08538-163">If Unicode is defined, the function call resolves to D3DXCreateEffectFromResourceW.</span></span> <span data-ttu-id="08538-164">Andernfalls wird der Funktions Aufruhe in D3DXCreateEffectFromResourceA aufgelöst, da ANSI-Zeichen folgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="08538-164">Otherwise, the function call resolves to D3DXCreateEffectFromResourceA because ANSI strings are being used.</span></span>

<span data-ttu-id="08538-165">D3DXCreateEffectFromResource lädt Daten aus einer Ressource vom Typ RT \_ RCDATA.</span><span class="sxs-lookup"><span data-stu-id="08538-165">D3DXCreateEffectFromResource loads data from a resource of type RT\_RCDATA.</span></span> <span data-ttu-id="08538-166">Weitere Informationen zu Windows-Ressourcen finden Sie in der MSDN-Website.</span><span class="sxs-lookup"><span data-stu-id="08538-166">See MSDN for more information about Windows resources.</span></span>

## <a name="requirements"></a><span data-ttu-id="08538-167">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="08538-167">Requirements</span></span>



| <span data-ttu-id="08538-168">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08538-168">Requirement</span></span> | <span data-ttu-id="08538-169">Wert</span><span class="sxs-lookup"><span data-stu-id="08538-169">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="08538-170">Header</span><span class="sxs-lookup"><span data-stu-id="08538-170">Header</span></span><br/>  | <dl> <span data-ttu-id="08538-171"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="08538-171"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="08538-172">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="08538-172">Library</span></span><br/> | <dl> <span data-ttu-id="08538-173"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="08538-173"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="08538-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08538-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08538-175">Effekt Funktionen</span><span class="sxs-lookup"><span data-stu-id="08538-175">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="08538-176">**D3DXCreateEffectEx**</span><span class="sxs-lookup"><span data-stu-id="08538-176">**D3DXCreateEffectEx**</span></span>](d3dxcreateeffectex.md)
</dt> <dt>

[<span data-ttu-id="08538-177">**D3DXCreateEffectFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="08538-177">**D3DXCreateEffectFromFileEx**</span></span>](d3dxcreateeffectfromfileex.md)
</dt> </dl>

 

 
