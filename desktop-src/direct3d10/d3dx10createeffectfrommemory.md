---
description: Erstellen Sie einen Effekt aus dem Arbeitsspeicher.
ms.assetid: 6903a695-bb87-45fe-9913-25beeaf17233
title: D3DX10CreateEffectFromMemory-Funktion (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectFromMemory
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 03cbbc70e633f8289f99e094602cb1a912b711c5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353738"
---
# <a name="d3dx10createeffectfrommemory-function"></a><span data-ttu-id="36656-103">D3DX10CreateEffectFromMemory-Funktion</span><span class="sxs-lookup"><span data-stu-id="36656-103">D3DX10CreateEffectFromMemory function</span></span>

<span data-ttu-id="36656-104">Erstellen Sie einen Effekt aus dem Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="36656-104">Create an effect from memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="36656-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="36656-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateEffectFromMemory(
  _In_        LPCVOID            pData,
  _In_        SIZE_T             DataLength,
  _In_        LPCSTR             pSrcFileName,
  _In_  const D3D_SHADER_MACRO *pDefines,
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



## <a name="parameters"></a><span data-ttu-id="36656-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="36656-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36656-107">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36656-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36656-108">Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="36656-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="36656-109">Zeiger auf den Effekt im Speicher.</span><span class="sxs-lookup"><span data-stu-id="36656-109">Pointer to the effect in memory.</span></span>

</dd> <dt>

<span data-ttu-id="36656-110">*DATALENGTH* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36656-110">*DataLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36656-111">Typ: **[ **Größe \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="36656-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="36656-112">Größe des Effekts im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="36656-112">Size of the effect in memory.</span></span>

</dd> <dt>

<span data-ttu-id="36656-113">*psrcfilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36656-113">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36656-114">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="36656-114">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="36656-115">Der Name der Effekt Datei im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="36656-115">Name of the effect file in memory.</span></span>

</dd> <dt>

<span data-ttu-id="36656-116">*pdefinitionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36656-116">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36656-117">Type: **Konstanten [**D3D \_ Shader- \_ Makro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="36656-117">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="36656-118">Ein mit Null endendes Array von Shader-Makros (siehe [**D3D \_ Shader \_ Macro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); legen Sie diese Einstellung auf **null** fest, um keine Makros anzugeben.</span><span class="sxs-lookup"><span data-stu-id="36656-118">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="36656-119">*pinclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36656-119">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36656-120">Typ: **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="36656-120">Type: **[**ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span></span>

<span data-ttu-id="36656-121">Ein Zeiger auf eine include-Schnittstelle (siehe [**ID3D10Include-Schnittstelle**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="36656-121">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="36656-122">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="36656-122">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="36656-123">*pprofile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36656-123">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36656-124">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="36656-124">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="36656-125">Eine Zeichenfolge, die das [Shader-Profil](../direct3dhlsl/dx-graphics-hlsl-models.md)oder Shader-Modell angibt.</span><span class="sxs-lookup"><span data-stu-id="36656-125">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md), or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="36656-126">*Hlslflags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36656-126">*HLSLFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36656-127">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="36656-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="36656-128">HLSL-Kompilierungsoptionen (siehe [d3d10 \_ Shader Konstanten](d3d10-shader.md)).</span><span class="sxs-lookup"><span data-stu-id="36656-128">HLSL compile options (see [D3D10\_SHADER Constants](d3d10-shader.md)).</span></span>

</dd> <dt>

<span data-ttu-id="36656-129">*Fxflags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36656-129">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36656-130">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="36656-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="36656-131">Effekt Kompilierungsoptionen (siehe [d3d10 \_ Effect Konstanten](d3d10-effect.md)).</span><span class="sxs-lookup"><span data-stu-id="36656-131">Effect compile options (see [D3D10\_EFFECT Constants](d3d10-effect.md)).</span></span>

</dd> <dt>

<span data-ttu-id="36656-132">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36656-132">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36656-133">Typ: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="36656-133">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="36656-134">Ein Zeiger auf das Gerät (siehe [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)), von dem die Ressourcen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="36656-134">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="36656-135">"Peer"- *Pool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36656-135">*pEffectPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36656-136">Typ: **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span><span class="sxs-lookup"><span data-stu-id="36656-136">Type: **[**ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span></span>

<span data-ttu-id="36656-137">Zeiger auf einen Effekt Pool (siehe [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) für die Freigabe von Variablen zwischen Effekten.</span><span class="sxs-lookup"><span data-stu-id="36656-137">Pointer to an effect pool (see [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) for sharing variables between effects.</span></span>

</dd> <dt>

<span data-ttu-id="36656-138">*ppump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="36656-138">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36656-139">Typ: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="36656-139">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="36656-140">Ein Zeiger auf eine Thread-Pump Schnittstelle (siehe [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="36656-140">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="36656-141">Verwenden Sie **null** , um anzugeben, dass diese Funktion erst zurückgegeben werden soll, wenn Sie abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="36656-141">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="36656-142">*ppeer-ect* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="36656-142">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36656-143">Typ: **[ **ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)\*\***</span><span class="sxs-lookup"><span data-stu-id="36656-143">Type: **[**ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)\*\***</span></span>

<span data-ttu-id="36656-144">Adresse eines Zeigers auf den Effekt (siehe [**ID3D10Effect Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)), der erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="36656-144">Address of a pointer to the effect (see [**ID3D10Effect Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)) that is created.</span></span>

</dd> <dt>

<span data-ttu-id="36656-145">*pperroren* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="36656-145">*ppErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36656-146">Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="36656-146">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="36656-147">Die Adresse eines Zeigers auf den Speicher (siehe [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)), die Auswirkungen auf Kompilierungsfehler enthält (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="36656-147">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="36656-148">*phresult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="36656-148">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36656-149">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="36656-149">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="36656-150">Ein Zeiger auf den Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="36656-150">A pointer to the return value.</span></span> <span data-ttu-id="36656-151">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="36656-151">May be **NULL**.</span></span> <span data-ttu-id="36656-152">Wenn *ppump* nicht **null** ist, muss *phresult* eine gültige Speicheradresse sein, bis die asynchrone Ausführung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="36656-152">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36656-153">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="36656-153">Return value</span></span>

<span data-ttu-id="36656-154">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="36656-154">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="36656-155">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="36656-155">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="36656-156">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="36656-156">Requirements</span></span>



| <span data-ttu-id="36656-157">Anforderung</span><span class="sxs-lookup"><span data-stu-id="36656-157">Requirement</span></span> | <span data-ttu-id="36656-158">Wert</span><span class="sxs-lookup"><span data-stu-id="36656-158">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="36656-159">Header</span><span class="sxs-lookup"><span data-stu-id="36656-159">Header</span></span><br/> | <dl> <span data-ttu-id="36656-160"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="36656-160"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36656-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="36656-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36656-162">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="36656-162">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
