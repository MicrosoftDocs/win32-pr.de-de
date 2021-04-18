---
description: Erstellen Sie einen Effekt Pool aus einer Effekt Datei.
ms.assetid: be738374-a91e-43d3-9cec-14882e6317ee
title: D3DX10CreateEffectPoolFromFile-Funktion (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectPoolFromFile
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 418ea287b9bbf2021f3b2e5379b209cf87745a69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365300"
---
# <a name="d3dx10createeffectpoolfromfile-function"></a><span data-ttu-id="64925-103">D3DX10CreateEffectPoolFromFile-Funktion</span><span class="sxs-lookup"><span data-stu-id="64925-103">D3DX10CreateEffectPoolFromFile function</span></span>

<span data-ttu-id="64925-104">Erstellen Sie einen Effekt Pool aus einer Effekt Datei.</span><span class="sxs-lookup"><span data-stu-id="64925-104">Create an effect pool from an effect file.</span></span>

## <a name="syntax"></a><span data-ttu-id="64925-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="64925-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateEffectPoolFromFile(
  _In_        LPCTSTR            pFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
  _In_        ID3D10Include      *pInclude,
  _In_        LPCSTR             pProfile,
  _In_        UINT               HLSLFlags,
  _In_        UINT               FXFlags,
  _In_        ID3D10Device       *pDevice,
  _In_        ID3DX10ThreadPump  *pPump,
  _Out_       ID3D10EffectPool   **ppEffectPool,
  _Out_       ID3D10Blob         **ppErrors,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="64925-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="64925-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64925-107">*pfilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64925-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64925-108">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="64925-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="64925-109">Der Effekt Dateiname.</span><span class="sxs-lookup"><span data-stu-id="64925-109">The effect filename.</span></span> <span data-ttu-id="64925-110">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="64925-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="64925-111">Andernfalls wird der Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="64925-111">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="64925-112">*pdefinitionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64925-112">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64925-113">Type: **Konstanten [**D3D \_ Shader- \_ Makro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="64925-113">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="64925-114">Ein mit Null endendes Array von Shader-Makros (siehe [**D3D \_ Shader \_ Macro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); legen Sie diese Einstellung auf **null** fest, um keine Makros anzugeben.</span><span class="sxs-lookup"><span data-stu-id="64925-114">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="64925-115">*pinclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64925-115">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64925-116">Typ: **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="64925-116">Type: **[**ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span></span>

<span data-ttu-id="64925-117">Ein Zeiger auf eine include-Schnittstelle (siehe [**ID3D10Include-Schnittstelle**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="64925-117">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="64925-118">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="64925-118">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="64925-119">*pprofile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64925-119">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64925-120">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="64925-120">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="64925-121">Eine Zeichenfolge, die das [Shader-Profil](../direct3dhlsl/dx-graphics-hlsl-models.md)oder Shader-Modell angibt.</span><span class="sxs-lookup"><span data-stu-id="64925-121">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md), or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="64925-122">*Hlslflags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64925-122">*HLSLFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64925-123">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="64925-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="64925-124">HLSL-Kompilierungsoptionen (siehe [d3d10 \_ Shader Konstanten](d3d10-shader.md)).</span><span class="sxs-lookup"><span data-stu-id="64925-124">HLSL compile options (see [D3D10\_SHADER Constants](d3d10-shader.md)).</span></span>

</dd> <dt>

<span data-ttu-id="64925-125">*Fxflags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64925-125">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64925-126">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="64925-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="64925-127">Effekt Kompilierungsoptionen (siehe [Kompilierungs-und Wirkungs Flags](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="64925-127">Effect compile options (see [Compile and Effect Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="64925-128">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64925-128">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64925-129">Typ: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="64925-129">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="64925-130">Ein Zeiger auf das Gerät (siehe [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)), von dem die Ressourcen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="64925-130">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="64925-131">*ppump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64925-131">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64925-132">Typ: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="64925-132">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="64925-133">Ein Zeiger auf eine Thread-Pump Schnittstelle (siehe [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="64925-133">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="64925-134">Verwenden Sie **null** , um anzugeben, dass diese Funktion erst zurückgegeben werden soll, wenn Sie abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="64925-134">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="64925-135">*ppeer-ectpool* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="64925-135">*ppEffectPool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64925-136">Typ: **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***</span><span class="sxs-lookup"><span data-stu-id="64925-136">Type: **[**ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***</span></span>

<span data-ttu-id="64925-137">Die Adresse eines Zeigers auf den Effekt Pool (siehe [**ID3D10EffectPool-Schnittstelle**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)).</span><span class="sxs-lookup"><span data-stu-id="64925-137">The address of a pointer to the effect pool (see [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)).</span></span>

</dd> <dt>

<span data-ttu-id="64925-138">*pperroren* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="64925-138">*ppErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64925-139">Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="64925-139">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="64925-140">Die Adresse eines Zeigers auf den Speicher (siehe [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)), die Auswirkungen auf Kompilierungsfehler enthält (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="64925-140">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="64925-141">*phresult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="64925-141">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64925-142">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="64925-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="64925-143">Ein Zeiger auf den Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="64925-143">A pointer to the return value.</span></span> <span data-ttu-id="64925-144">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="64925-144">May be **NULL**.</span></span> <span data-ttu-id="64925-145">Wenn *ppump* nicht **null** ist, muss *phresult* eine gültige Speicheradresse sein, bis die asynchrone Ausführung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="64925-145">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64925-146">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="64925-146">Return value</span></span>

<span data-ttu-id="64925-147">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="64925-147">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="64925-148">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="64925-148">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="64925-149">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64925-149">Remarks</span></span>

<span data-ttu-id="64925-150">In diesem Beispiel wird ein Effekt Pool aus dem Effekt erstellt, der im [BasicHLSL10-Beispiel](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="64925-150">This example creates an effect pool from the effect used in the [BasicHLSL10 Sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx).</span></span>


```
   
// Create an effect pool from an effect in memory
ID3D10EffectPool * l_pEffectPool = NULL;
ID3D10Blob* l_pBlob_Errors = NULL;
WCHAR str[MAX_PATH];
hr = DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );
hr = D3DX10CreateEffectPoolFromFile( str, 
    NULL, NULL, D3D10_SHADER_ENABLE_STRICTNESS, 
    0, pd3dDevice, NULL, &l_pEffectPool,
    &l_pBlob_Errors );
```



## <a name="requirements"></a><span data-ttu-id="64925-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="64925-151">Requirements</span></span>



| <span data-ttu-id="64925-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="64925-152">Requirement</span></span> | <span data-ttu-id="64925-153">Wert</span><span class="sxs-lookup"><span data-stu-id="64925-153">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="64925-154">Header</span><span class="sxs-lookup"><span data-stu-id="64925-154">Header</span></span><br/> | <dl> <span data-ttu-id="64925-155"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="64925-155"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64925-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64925-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64925-157">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="64925-157">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
