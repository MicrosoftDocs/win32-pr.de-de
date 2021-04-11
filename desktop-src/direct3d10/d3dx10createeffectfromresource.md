---
description: Erstellen Sie einen Effekt aus einer Ressource.
ms.assetid: 239a3b14-9eea-4a0f-96b5-3959b7be3e19
title: D3DX10CreateEffectFromResource-Funktion (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectFromResource
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 6c5f7b7805e126f02c2658ddce6ec5029978de53
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355097"
---
# <a name="d3dx10createeffectfromresource-function"></a><span data-ttu-id="ee86e-103">D3DX10CreateEffectFromResource-Funktion</span><span class="sxs-lookup"><span data-stu-id="ee86e-103">D3DX10CreateEffectFromResource function</span></span>

<span data-ttu-id="ee86e-104">Erstellen Sie einen Effekt aus einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="ee86e-104">Create an effect from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee86e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee86e-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateEffectFromResource(
  _In_        HMODULE            hModule,
  _In_        LPCTSTR            pResourceName,
  _In_        LPCTSTR            pSrcFileName,
  _In_  const D3D10_SHADER_MACRO *pDefines,
  _In_        ID3D10Include      *pInclude,
  _In_        LPCSTR             pProfile,
  _In_        UINT               HLSLFlags,
  _In_        UINT               FXFlags,
  _In_        ID3D10Device       *pDevice,
  _In_        ID3D10EffectPool   *pEffectPool,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10Effect       **ppEffect,
  _Out_       ID3D10Blob         **ppErrors,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="ee86e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee86e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee86e-107">*HMODULE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ee86e-107">*hModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee86e-108">Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ee86e-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ee86e-109">Ein Handle für das Ressourcen Modul, das den Effekt enthält.</span><span class="sxs-lookup"><span data-stu-id="ee86e-109">A handle to the resource module containing the effect.</span></span> <span data-ttu-id="ee86e-110">HMODULE kann mit der [GetModuleHandle-Funktion](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ee86e-110">HMODULE can be obtained with [GetModuleHandle Function](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="ee86e-111">*presourcename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ee86e-111">*pResourceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee86e-112">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ee86e-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ee86e-113">Der Name der Ressource in HMODULE.</span><span class="sxs-lookup"><span data-stu-id="ee86e-113">Name of the resource in hModule.</span></span> <span data-ttu-id="ee86e-114">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="ee86e-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="ee86e-115">Andernfalls wird der Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="ee86e-115">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="ee86e-116">*psrcfilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ee86e-116">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee86e-117">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ee86e-117">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ee86e-118">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="ee86e-118">Optional.</span></span> <span data-ttu-id="ee86e-119">Der Effekt Dateiname, der nur für Fehlermeldungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ee86e-119">Effect file name, which is used for error messages only.</span></span> <span data-ttu-id="ee86e-120">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="ee86e-120">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ee86e-121">*pdefinitionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ee86e-121">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee86e-122">Type: **Konstanten [**D3D \_ Shader- \_ Makro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="ee86e-122">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="ee86e-123">Ein mit Null endendes Array von Shader-Makros (siehe [**D3D \_ Shader \_ Macro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); legen Sie diese Einstellung auf **null** fest, um keine Makros anzugeben.</span><span class="sxs-lookup"><span data-stu-id="ee86e-123">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="ee86e-124">*pinclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ee86e-124">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee86e-125">Typ: **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="ee86e-125">Type: **[**ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span></span>

<span data-ttu-id="ee86e-126">Ein Zeiger auf eine include-Schnittstelle (siehe [**ID3D10Include-Schnittstelle**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="ee86e-126">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="ee86e-127">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="ee86e-127">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ee86e-128">*pprofile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ee86e-128">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee86e-129">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ee86e-129">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ee86e-130">Eine Zeichenfolge, die das [Shader-Profil](../direct3dhlsl/dx-graphics-hlsl-models.md)oder Shader-Modell angibt.</span><span class="sxs-lookup"><span data-stu-id="ee86e-130">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md), or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="ee86e-131">*Hlslflags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ee86e-131">*HLSLFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee86e-132">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ee86e-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ee86e-133">HLSL-Kompilierungsoptionen (siehe [d3d10 \_ Shader Konstanten](d3d10-shader.md)).</span><span class="sxs-lookup"><span data-stu-id="ee86e-133">HLSL compile options (see [D3D10\_SHADER Constants](d3d10-shader.md)).</span></span>

</dd> <dt>

<span data-ttu-id="ee86e-134">*Fxflags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ee86e-134">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee86e-135">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ee86e-135">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ee86e-136">Effekt Kompilierungsoptionen (siehe [Kompilierungs-und Wirkungs Flags](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="ee86e-136">Effect compile options (see [Compile and Effect Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="ee86e-137">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ee86e-137">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee86e-138">Typ: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="ee86e-138">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="ee86e-139">Ein Zeiger auf das Gerät (siehe [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)), von dem die Ressourcen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ee86e-139">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="ee86e-140">"Peer"- *Pool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ee86e-140">*pEffectPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee86e-141">Typ: **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span><span class="sxs-lookup"><span data-stu-id="ee86e-141">Type: **[**ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span></span>

<span data-ttu-id="ee86e-142">Zeiger auf einen Effekt Pool (siehe [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) für die Freigabe von Variablen zwischen Effekten.</span><span class="sxs-lookup"><span data-stu-id="ee86e-142">Pointer to an effect pool (see [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) for sharing variables between effects.</span></span>

</dd> <dt>

<span data-ttu-id="ee86e-143">*ppump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ee86e-143">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee86e-144">Typ: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="ee86e-144">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="ee86e-145">Ein Zeiger auf eine Thread-Pump Schnittstelle (siehe [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="ee86e-145">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="ee86e-146">Verwenden Sie **null** , um anzugeben, dass diese Funktion erst zurückgegeben werden soll, wenn Sie abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="ee86e-146">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="ee86e-147">*ppeer-ect* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ee86e-147">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee86e-148">Typ: **[ **ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)\*\***</span><span class="sxs-lookup"><span data-stu-id="ee86e-148">Type: **[**ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)\*\***</span></span>

<span data-ttu-id="ee86e-149">Adresse eines Zeigers auf den Effekt (siehe [**ID3D10Effect Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)), der erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ee86e-149">Address of a pointer to the effect (see [**ID3D10Effect Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)) that is created.</span></span>

</dd> <dt>

<span data-ttu-id="ee86e-150">*pperroren* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ee86e-150">*ppErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee86e-151">Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="ee86e-151">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="ee86e-152">Die Adresse eines Zeigers auf den Speicher (siehe [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)), die Auswirkungen auf Kompilierungsfehler enthält (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="ee86e-152">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="ee86e-153">*phresult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ee86e-153">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee86e-154">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="ee86e-154">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="ee86e-155">Ein Zeiger auf den Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="ee86e-155">A pointer to the return value.</span></span> <span data-ttu-id="ee86e-156">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="ee86e-156">May be **NULL**.</span></span> <span data-ttu-id="ee86e-157">Wenn *ppump* nicht **null** ist, muss *phresult* eine gültige Speicheradresse sein, bis die asynchrone Ausführung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="ee86e-157">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee86e-158">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ee86e-158">Return value</span></span>

<span data-ttu-id="ee86e-159">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ee86e-159">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ee86e-160">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="ee86e-160">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ee86e-161">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ee86e-161">Requirements</span></span>



| <span data-ttu-id="ee86e-162">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ee86e-162">Requirement</span></span> | <span data-ttu-id="ee86e-163">Wert</span><span class="sxs-lookup"><span data-stu-id="ee86e-163">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee86e-164">Header</span><span class="sxs-lookup"><span data-stu-id="ee86e-164">Header</span></span><br/> | <dl> <span data-ttu-id="ee86e-165"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee86e-165"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee86e-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee86e-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee86e-167">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="ee86e-167">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
