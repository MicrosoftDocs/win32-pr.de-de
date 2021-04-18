---
description: Erstellen Sie einen Effekt Pool aus einem Effekt in den Arbeitsspeicher.
ms.assetid: 634bcb23-a73f-4493-b805-e2aa5420fa2a
title: D3DX10CreateEffectPoolFromMemory-Funktion (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectPoolFromMemory
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 7dc93b7e73f336e75432debfe9bde6659ea4707c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351940"
---
# <a name="d3dx10createeffectpoolfrommemory-function"></a><span data-ttu-id="1b4e1-103">D3DX10CreateEffectPoolFromMemory-Funktion</span><span class="sxs-lookup"><span data-stu-id="1b4e1-103">D3DX10CreateEffectPoolFromMemory function</span></span>

<span data-ttu-id="1b4e1-104">Erstellen Sie einen Effekt Pool aus einem Effekt in den Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="1b4e1-104">Create an effect pool from an effect in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b4e1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b4e1-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateEffectPoolFromMemory(
  _In_        LPCVOID            pData,
  _In_        SIZE_T             DataLength,
  _In_        LPCSTR             pSrcFileName,
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



## <a name="parameters"></a><span data-ttu-id="1b4e1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b4e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b4e1-107">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b4e1-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b4e1-108">Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1b4e1-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1b4e1-109">Ein Zeiger auf den Effekt.</span><span class="sxs-lookup"><span data-stu-id="1b4e1-109">A pointer to the effect.</span></span>

</dd> <dt>

<span data-ttu-id="1b4e1-110">*DATALENGTH* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b4e1-110">*DataLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b4e1-111">Typ: **[ **Größe \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1b4e1-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1b4e1-112">Die Größe des Effekts.</span><span class="sxs-lookup"><span data-stu-id="1b4e1-112">The size of the effect.</span></span>

</dd> <dt>

<span data-ttu-id="1b4e1-113">*psrcfilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b4e1-113">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b4e1-114">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1b4e1-114">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1b4e1-115">Der Name der Effekt Datei.</span><span class="sxs-lookup"><span data-stu-id="1b4e1-115">The name of the effect file.</span></span>

</dd> <dt>

<span data-ttu-id="1b4e1-116">*pdefinitionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b4e1-116">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b4e1-117">Type: **Konstanten [**D3D \_ Shader- \_ Makro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="1b4e1-117">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="1b4e1-118">Ein mit Null endendes Array von Shader-Makros (siehe [**D3D \_ Shader \_ Macro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); legen Sie diese Einstellung auf **null** fest, um keine Makros anzugeben.</span><span class="sxs-lookup"><span data-stu-id="1b4e1-118">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="1b4e1-119">*pinclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b4e1-119">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b4e1-120">Typ: **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="1b4e1-120">Type: **[**ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span></span>

<span data-ttu-id="1b4e1-121">Ein Zeiger auf eine include-Schnittstelle (siehe [**ID3D10Include-Schnittstelle**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="1b4e1-121">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="1b4e1-122">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="1b4e1-122">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1b4e1-123">*pprofile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b4e1-123">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b4e1-124">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1b4e1-124">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1b4e1-125">Eine Zeichenfolge, die das [Shader-Profil](../direct3dhlsl/dx-graphics-hlsl-models.md)oder Shader-Modell angibt.</span><span class="sxs-lookup"><span data-stu-id="1b4e1-125">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md), or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="1b4e1-126">*Hlslflags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b4e1-126">*HLSLFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b4e1-127">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1b4e1-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1b4e1-128">HLSL-Kompilierungsoptionen (siehe [d3d10 \_ Shader Konstanten](d3d10-shader.md)).</span><span class="sxs-lookup"><span data-stu-id="1b4e1-128">HLSL compile options (see [D3D10\_SHADER Constants](d3d10-shader.md)).</span></span>

</dd> <dt>

<span data-ttu-id="1b4e1-129">*Fxflags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b4e1-129">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b4e1-130">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1b4e1-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1b4e1-131">Effekt Kompilierungsoptionen (siehe [Kompilierungs-und Wirkungs Flags](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="1b4e1-131">Effect compile options (see [Compile and Effect Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="1b4e1-132">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b4e1-132">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b4e1-133">Typ: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="1b4e1-133">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="1b4e1-134">Ein Zeiger auf das Gerät (siehe [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)), von dem die Ressourcen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1b4e1-134">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="1b4e1-135">*ppump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b4e1-135">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b4e1-136">Typ: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="1b4e1-136">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="1b4e1-137">Ein Zeiger auf eine Thread-Pump Schnittstelle (siehe [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="1b4e1-137">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="1b4e1-138">Verwenden Sie **null** , um anzugeben, dass diese Funktion erst zurückgegeben werden soll, wenn Sie abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="1b4e1-138">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="1b4e1-139">*ppeer-ectpool* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1b4e1-139">*ppEffectPool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b4e1-140">Typ: **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***</span><span class="sxs-lookup"><span data-stu-id="1b4e1-140">Type: **[**ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\*\***</span></span>

<span data-ttu-id="1b4e1-141">Die Adresse eines Zeigers auf den Effekt Pool (siehe [**ID3D10EffectPool-Schnittstelle**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)).</span><span class="sxs-lookup"><span data-stu-id="1b4e1-141">The address of a pointer to the effect pool (see [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)).</span></span>

</dd> <dt>

<span data-ttu-id="1b4e1-142">*pperroren* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1b4e1-142">*ppErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b4e1-143">Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="1b4e1-143">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="1b4e1-144">Die Adresse eines Zeigers auf den Speicher (siehe [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)), die Auswirkungen auf Kompilierungsfehler enthält (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="1b4e1-144">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="1b4e1-145">*phresult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1b4e1-145">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b4e1-146">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="1b4e1-146">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="1b4e1-147">Ein Zeiger auf den Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="1b4e1-147">A pointer to the return value.</span></span> <span data-ttu-id="1b4e1-148">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="1b4e1-148">May be **NULL**.</span></span> <span data-ttu-id="1b4e1-149">Wenn *ppump* nicht **null** ist, muss *phresult* eine gültige Speicheradresse sein, bis die asynchrone Ausführung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="1b4e1-149">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b4e1-150">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1b4e1-150">Return value</span></span>

<span data-ttu-id="1b4e1-151">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1b4e1-151">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1b4e1-152">Gibt einen der folgenden [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="1b4e1-152">Returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1b4e1-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1b4e1-153">Requirements</span></span>



| <span data-ttu-id="1b4e1-154">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b4e1-154">Requirement</span></span> | <span data-ttu-id="1b4e1-155">Wert</span><span class="sxs-lookup"><span data-stu-id="1b4e1-155">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b4e1-156">Header</span><span class="sxs-lookup"><span data-stu-id="1b4e1-156">Header</span></span><br/> | <dl> <span data-ttu-id="1b4e1-157"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b4e1-157"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b4e1-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b4e1-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b4e1-159">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="1b4e1-159">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
