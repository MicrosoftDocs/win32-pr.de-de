---
description: Erstellt einen Effekt aus einer Beschreibung des ASCII-oder binären Effekts. Diese Funktion ist eine erweiterte Version von D3DXCreateEffect, mit der eine Anwendung steuern kann, welche Parameter vom Effects-System ignoriert werden.
ms.assetid: b08f727e-6061-4e78-8243-08c4ccab342d
title: D3DXCreateEffectEx-Funktion (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectEx
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 979b09f852e692b4c25414607f79cd8792342755
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357243"
---
# <a name="d3dxcreateeffectex-function"></a><span data-ttu-id="031ee-104">D3DXCreateEffectEx-Funktion</span><span class="sxs-lookup"><span data-stu-id="031ee-104">D3DXCreateEffectEx function</span></span>

<span data-ttu-id="031ee-105">Erstellt einen Effekt aus einer Beschreibung des ASCII-oder binären Effekts.</span><span class="sxs-lookup"><span data-stu-id="031ee-105">Creates an effect from an ASCII or binary effect description.</span></span> <span data-ttu-id="031ee-106">Diese Funktion ist eine erweiterte Version von [**D3DXCreateEffect**](d3dxcreateeffect.md) , mit der eine Anwendung steuern kann, welche Parameter vom Effects-System ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="031ee-106">This function is an extended version of [**D3DXCreateEffect**](d3dxcreateeffect.md) that allows an application to control which parameters are ignored by the effects system.</span></span>

## <a name="syntax"></a><span data-ttu-id="031ee-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="031ee-107">Syntax</span></span>


```C++
HRESULT D3DXCreateEffectEx(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        LPCVOID           pSrcData,
  _In_        UINT              SrcDataLen,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        LPCSTR            pSkipConstants,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a><span data-ttu-id="031ee-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="031ee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="031ee-109">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="031ee-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="031ee-110">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="031ee-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="031ee-111">Zeiger auf das Gerät, das den Effekt erzeugt.</span><span class="sxs-lookup"><span data-stu-id="031ee-111">Pointer to the device that will create the effect.</span></span> <span data-ttu-id="031ee-112">Siehe [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="031ee-112">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> <dt>

<span data-ttu-id="031ee-113">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="031ee-113">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="031ee-114">Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="031ee-114">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="031ee-115">Zeiger auf einen Puffer, der eine Beschreibung des Effekts enthält.</span><span class="sxs-lookup"><span data-stu-id="031ee-115">Pointer to a buffer containing an effect description.</span></span>

</dd> <dt>

<span data-ttu-id="031ee-116">*Srcdatalen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="031ee-116">*SrcDataLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="031ee-117">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="031ee-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="031ee-118">Länge der Effekt Daten in Bytes.</span><span class="sxs-lookup"><span data-stu-id="031ee-118">Length of the effect data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="031ee-119">*pdefinitionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="031ee-119">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="031ee-120">Typ: **Konstanten [**D3DXMACRO**](d3dxmacro.md) \***</span><span class="sxs-lookup"><span data-stu-id="031ee-120">Type: **const [**D3DXMACRO**](d3dxmacro.md)\***</span></span>

<span data-ttu-id="031ee-121">Ein optionales **null** terminiertes Array von [**D3DXMACRO**](d3dxmacro.md) -Strukturen, die Präprozessordefinitionen beschreiben.</span><span class="sxs-lookup"><span data-stu-id="031ee-121">An optional **NULL**-terminated array of [**D3DXMACRO**](d3dxmacro.md) structures that describe preprocessor definitions.</span></span> <span data-ttu-id="031ee-122">Dieser Wert kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="031ee-122">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="031ee-123">*pinclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="031ee-123">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="031ee-124">Typ: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**</span><span class="sxs-lookup"><span data-stu-id="031ee-124">Type: **[**LPD3DXINCLUDE**](id3dxinclude.md)**</span></span>

<span data-ttu-id="031ee-125">Optionaler Schnittstellen Zeiger, [**ID3DXInclude**](id3dxinclude.md), der zum Verarbeiten von include-Direktiven verwendet werden soll \# .</span><span class="sxs-lookup"><span data-stu-id="031ee-125">Optional interface pointer, [**ID3DXInclude**](id3dxinclude.md), to use for handling \#include directives.</span></span> <span data-ttu-id="031ee-126">Wenn dieser Wert **null** ist, \# wird includes bei der Kompilierung aus einer Datei berücksichtigt, oder es wird ein Fehler ausgelöst, wenn eine Kompilierung aus einer Ressource oder einem Arbeitsspeicher erfolgt.</span><span class="sxs-lookup"><span data-stu-id="031ee-126">If this value is **NULL**, \#includes will either be honored when compiling from a file or will cause an error when compiled from a resource or memory.</span></span>

</dd> <dt>

<span data-ttu-id="031ee-127">*pskipkonstanten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="031ee-127">*pSkipConstants* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="031ee-128">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="031ee-128">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="031ee-129">Eine Zeichenfolge von Effekt Parametern, die vom Effektsystem ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="031ee-129">A string of effect parameters that will be ignored by the effect system.</span></span> <span data-ttu-id="031ee-130">Die Zeichenfolge muss **null** sein und muss den Namen jeder von der Anwendung verwalteten Konstante enthalten, die durch ein Semikolon getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="031ee-130">The string must be **NULL** terminated, and needs to contain the name of each application-managed constant separated by a semicolon.</span></span>

</dd> <dt>

<span data-ttu-id="031ee-131">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="031ee-131">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="031ee-132">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="031ee-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="031ee-133">Wenn *pSrcData* einen Text Effekt enthält, können Flags eine Kombination aus [D3DXSHADER-Flags](d3dxshader-flags.md) und [D3DXFX](d3dxfx.md) -Flags sein. Andernfalls enthält *pSrcData* einen binären Effekt, und die einzigen Flags, die berücksichtigt werden, sind D3DXFX-Flags.</span><span class="sxs-lookup"><span data-stu-id="031ee-133">If *pSrcData* contains a text effect, flags can be a combination of [D3DXSHADER Flags](d3dxshader-flags.md) and [D3DXFX](d3dxfx.md) flags; otherwise, *pSrcData* contains a binary effect and the only flags honored are D3DXFX flags.</span></span> <span data-ttu-id="031ee-134">Der Direct3D 10 HLSL-Compiler ist nun der Standard.</span><span class="sxs-lookup"><span data-stu-id="031ee-134">The Direct3D 10 HLSL compiler is now the default.</span></span> <span data-ttu-id="031ee-135">Ausführliche Informationen finden Sie unter [Effect-Compiler-Tool](../direct3dtools/fxc.md) .</span><span class="sxs-lookup"><span data-stu-id="031ee-135">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

</dd> <dt>

<span data-ttu-id="031ee-136">*ppool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="031ee-136">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="031ee-137">Typ: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span><span class="sxs-lookup"><span data-stu-id="031ee-137">Type: **[**LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**</span></span>

<span data-ttu-id="031ee-138">Zeiger auf ein [**ID3DXEffectPool**](id3dxeffectpool.md) -Objekt, das für freigegebene Parameter verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="031ee-138">Pointer to an [**ID3DXEffectPool**](id3dxeffectpool.md) object to use for shared parameters.</span></span> <span data-ttu-id="031ee-139">Wenn dieser Wert **null** ist, werden keine Parameter freigegeben.</span><span class="sxs-lookup"><span data-stu-id="031ee-139">If this value is **NULL**, no parameters will be shared.</span></span>

</dd> <dt>

<span data-ttu-id="031ee-140">*ppeer-ect* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="031ee-140">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="031ee-141">Typ: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="031ee-141">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="031ee-142">Gibt einen Zeiger auf eine [**ID3DXEffect**](id3dxeffect.md) -Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="031ee-142">Returns a pointer to an [**ID3DXEffect**](id3dxeffect.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="031ee-143">*ppcompilationerrors* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="031ee-143">*ppCompilationErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="031ee-144">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="031ee-144">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="031ee-145">Gibt einen Puffer zurück, der eine Liste mit Kompilierungs Fehlern enthält.</span><span class="sxs-lookup"><span data-stu-id="031ee-145">Returns a buffer containing a list of compile errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="031ee-146">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="031ee-146">Return value</span></span>

<span data-ttu-id="031ee-147">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="031ee-147">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="031ee-148">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="031ee-148">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="031ee-149">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ oudefmemory.</span><span class="sxs-lookup"><span data-stu-id="031ee-149">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="031ee-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="031ee-150">Remarks</span></span>

<span data-ttu-id="031ee-151">Diese Funktion ist eine erweiterte Version von [**D3DXCreateEffect**](d3dxcreateeffect.md) , mit der eine Anwendung angeben kann, welche Effekt Konstanten von der Anwendung verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="031ee-151">This function is an extended version of [**D3DXCreateEffect**](d3dxcreateeffect.md) that allows an application to specify which effect constants will be managed by the application.</span></span> <span data-ttu-id="031ee-152">Eine Konstante, die von der Anwendung verwaltet wird, wird vom Effects-System ignoriert.</span><span class="sxs-lookup"><span data-stu-id="031ee-152">A constant that is managed by the application is ignored by the effects system.</span></span> <span data-ttu-id="031ee-153">Das heißt, die Anwendung ist dafür verantwortlich, die Konstante zu initialisieren und ihren Zustand zu speichern und wiederherzustellen, wenn dies angemessen ist.</span><span class="sxs-lookup"><span data-stu-id="031ee-153">That is, the application is responsible for initializing the constant as well as saving and restoring its state whenever appropriate.</span></span>

<span data-ttu-id="031ee-154">Diese Funktion überprüft jede Konstante in pskipkonstanten, um Folgendes anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="031ee-154">This function checks each constant in pSkipConstants to see that:</span></span>

-   <span data-ttu-id="031ee-155">Er ist an ein konstantes Register gebunden.</span><span class="sxs-lookup"><span data-stu-id="031ee-155">It is bound to a constant register.</span></span>
-   <span data-ttu-id="031ee-156">Sie wird nur im HLSL-Shader-Code verwendet.</span><span class="sxs-lookup"><span data-stu-id="031ee-156">It is only used in HLSL shader code.</span></span>

<span data-ttu-id="031ee-157">Wenn eine Konstante in der Zeichenfolge benannt wird, die nicht in der Auswirkung vorhanden ist, wird Sie ignoriert.</span><span class="sxs-lookup"><span data-stu-id="031ee-157">If a constant is named in the string that is not present in the effect, it is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="031ee-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="031ee-158">Requirements</span></span>



| <span data-ttu-id="031ee-159">Anforderung</span><span class="sxs-lookup"><span data-stu-id="031ee-159">Requirement</span></span> | <span data-ttu-id="031ee-160">Wert</span><span class="sxs-lookup"><span data-stu-id="031ee-160">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="031ee-161">Header</span><span class="sxs-lookup"><span data-stu-id="031ee-161">Header</span></span><br/>  | <dl> <span data-ttu-id="031ee-162"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="031ee-162"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="031ee-163">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="031ee-163">Library</span></span><br/> | <dl> <span data-ttu-id="031ee-164"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="031ee-164"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="031ee-165">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="031ee-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="031ee-166">Effekt Funktionen</span><span class="sxs-lookup"><span data-stu-id="031ee-166">Effect Functions</span></span>](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[<span data-ttu-id="031ee-167">**D3DXCreateEffectFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="031ee-167">**D3DXCreateEffectFromFileEx**</span></span>](d3dxcreateeffectfromfileex.md)
</dt> <dt>

[<span data-ttu-id="031ee-168">**D3DXCreateEffectFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="031ee-168">**D3DXCreateEffectFromResourceEx**</span></span>](d3dxcreateeffectfromresourceex.md)
</dt> </dl>

 

 
