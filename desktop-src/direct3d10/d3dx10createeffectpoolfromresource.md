---
description: Erstellen Sie einen Effekt Pool aus einer Ressource.
ms.assetid: 594ab788-fd96-4ea9-ad93-ef02fefa5d61
title: D3DX10CreateEffectPoolFromResource-Funktion (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectPoolFromResource
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 1fccc9c399a4573440318b92d1157738589da8a4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365077"
---
# <a name="d3dx10createeffectpoolfromresource-function"></a><span data-ttu-id="46ed4-103">D3DX10CreateEffectPoolFromResource-Funktion</span><span class="sxs-lookup"><span data-stu-id="46ed4-103">D3DX10CreateEffectPoolFromResource function</span></span>

<span data-ttu-id="46ed4-104">Erstellen Sie einen Effekt Pool aus einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="46ed4-104">Create an effect pool from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="46ed4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="46ed4-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateEffectPoolFromResource(
  _In_        HMODULE            hModule,
  _In_        LPCTSTR            pResourceName,
  _In_        LPCTSTR            pSrcFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        ID3D10Include      *pInclude,
  _In_        LPCSTR             pProfile,
  _In_        UINT               HLSLFlags,
  _In_        UINT               FXFlags,
  _In_        ID3D10Device       *pDevice,
  _In_        ID3DX10ThreadPump  *pPump,
  _In_        ID3D10EffectPool   **ppEffectPool,
  _In_        ID3D10Blob         **ppErrors,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="46ed4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="46ed4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46ed4-107">*HMODULE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46ed4-107">*hModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46ed4-108">Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46ed4-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46ed4-109">Ein Handle für das Ressourcen Modul, das den Effekt enthält.</span><span class="sxs-lookup"><span data-stu-id="46ed4-109">A handle to the resource module containing the effect.</span></span> <span data-ttu-id="46ed4-110">HMODULE kann mit der [GetModuleHandle-Funktion](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="46ed4-110">HMODULE can be obtained with [GetModuleHandle Function](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="46ed4-111">*presourcename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46ed4-111">*pResourceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46ed4-112">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46ed4-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46ed4-113">Der Name der Ressource in HMODULE.</span><span class="sxs-lookup"><span data-stu-id="46ed4-113">The name of the resource in hModule.</span></span> <span data-ttu-id="46ed4-114">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="46ed4-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="46ed4-115">Andernfalls wird der Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="46ed4-115">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="46ed4-116">*psrcfilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46ed4-116">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46ed4-117">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46ed4-117">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46ed4-118">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="46ed4-118">Optional.</span></span> <span data-ttu-id="46ed4-119">Der Effekt Dateiname, der nur für Fehlermeldungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="46ed4-119">Effect file name, which is used for error messages only.</span></span> <span data-ttu-id="46ed4-120">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="46ed4-120">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="46ed4-121">*pdefinitionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46ed4-121">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46ed4-122">Type: **Konstanten [**D3D \_ Shader- \_ Makro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="46ed4-122">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="46ed4-123">Ein mit Null endendes Array von Shader-Makros (siehe [**D3D \_ Shader \_ Macro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); legen Sie diese Einstellung auf **null** fest, um keine Makros anzugeben.</span><span class="sxs-lookup"><span data-stu-id="46ed4-123">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="46ed4-124">*pinclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46ed4-124">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46ed4-125">Typ: **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="46ed4-125">Type: **[**ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span></span>

<span data-ttu-id="46ed4-126">Ein Zeiger auf eine include-Schnittstelle (siehe [**ID3D10Include-Schnittstelle**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="46ed4-126">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="46ed4-127">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="46ed4-127">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="46ed4-128">*pprofile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46ed4-128">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46ed4-129">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46ed4-129">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46ed4-130">Eine Zeichenfolge, die das [Shader-Profil](../direct3dhlsl/dx-graphics-hlsl-models.md)oder Shader-Modell angibt.</span><span class="sxs-lookup"><span data-stu-id="46ed4-130">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md), or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="46ed4-131">*Hlslflags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46ed4-131">*HLSLFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46ed4-132">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46ed4-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46ed4-133">HLSL-Kompilierungsoptionen (siehe [d3d10 \_ Shader Konstanten](d3d10-shader.md)).</span><span class="sxs-lookup"><span data-stu-id="46ed4-133">HLSL compile options (see [D3D10\_SHADER Constants](d3d10-shader.md)).</span></span>

</dd> <dt>

<span data-ttu-id="46ed4-134">*Fxflags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46ed4-134">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46ed4-135">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="46ed4-135">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="46ed4-136">Effekt Kompilierungsoptionen (siehe [Kompilierungs-und Wirkungs Flags](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="46ed4-136">Effect compile options (see [Compile and Effect Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="46ed4-137">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46ed4-137">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46ed4-138">Typ: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="46ed4-138">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="46ed4-139">Ein Zeiger auf das Gerät (siehe [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)), von dem die Ressourcen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="46ed4-139">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="46ed4-140">*ppump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46ed4-140">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46ed4-141">Typ: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="46ed4-141">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="46ed4-142">Ein Zeiger auf eine Thread-Pump Schnittstelle (siehe [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="46ed4-142">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="46ed4-143">Verwenden Sie **null** , um anzugeben, dass diese Funktion erst zurückgegeben werden soll, wenn Sie abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="46ed4-143">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="46ed4-144">*ppeer-ectpool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46ed4-144">*ppEffectPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46ed4-145">Typ: **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***</span><span class="sxs-lookup"><span data-stu-id="46ed4-145">Type: **[**ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***</span></span>

<span data-ttu-id="46ed4-146">Die Adresse eines Zeigers auf den Effekt Pool (siehe [**ID3D10EffectPool-Schnittstelle**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)).</span><span class="sxs-lookup"><span data-stu-id="46ed4-146">The address of a pointer to the effect pool (see [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)).</span></span>

</dd> <dt>

<span data-ttu-id="46ed4-147">*pperroren* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46ed4-147">*ppErrors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46ed4-148">Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="46ed4-148">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="46ed4-149">Die Adresse eines Zeigers auf den Speicher (siehe [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)), die Auswirkungen auf Kompilierungsfehler enthält (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="46ed4-149">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="46ed4-150">*phresult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="46ed4-150">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46ed4-151">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="46ed4-151">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="46ed4-152">Ein Zeiger auf den Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="46ed4-152">A pointer to the return value.</span></span> <span data-ttu-id="46ed4-153">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="46ed4-153">May be **NULL**.</span></span> <span data-ttu-id="46ed4-154">Wenn *ppump* nicht **null** ist, muss *phresult* eine gültige Speicheradresse sein, bis die asynchrone Ausführung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="46ed4-154">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46ed4-155">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="46ed4-155">Return value</span></span>

<span data-ttu-id="46ed4-156">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="46ed4-156">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="46ed4-157">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="46ed4-157">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="46ed4-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46ed4-158">Requirements</span></span>



| <span data-ttu-id="46ed4-159">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46ed4-159">Requirement</span></span> | <span data-ttu-id="46ed4-160">Wert</span><span class="sxs-lookup"><span data-stu-id="46ed4-160">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="46ed4-161">Header</span><span class="sxs-lookup"><span data-stu-id="46ed4-161">Header</span></span><br/> | <dl> <span data-ttu-id="46ed4-162"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="46ed4-162"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46ed4-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46ed4-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46ed4-164">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="46ed4-164">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
