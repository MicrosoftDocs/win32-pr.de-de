---
description: Erstellen Sie einen Effekt aus einer Datei.
ms.assetid: 1418857e-bda1-4ffb-bbb9-dfa3709313b1
title: D3DX10CreateEffectFromFile-Funktion (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateEffectFromFile
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 60bc52e5b149a2fa69cc4a16f12900b12ab81db8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364382"
---
# <a name="d3dx10createeffectfromfile-function"></a><span data-ttu-id="57684-103">D3DX10CreateEffectFromFile-Funktion</span><span class="sxs-lookup"><span data-stu-id="57684-103">D3DX10CreateEffectFromFile function</span></span>

<span data-ttu-id="57684-104">Erstellen Sie einen Effekt aus einer Datei.</span><span class="sxs-lookup"><span data-stu-id="57684-104">Create an effect from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="57684-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="57684-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateEffectFromFile(
  _In_        LPCTSTR            pFileName,
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



## <a name="parameters"></a><span data-ttu-id="57684-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="57684-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57684-107">*pfilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57684-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57684-108">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="57684-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="57684-109">Der Name der ASCII-Effekt Datei.</span><span class="sxs-lookup"><span data-stu-id="57684-109">Name of the ASCII effect file.</span></span> <span data-ttu-id="57684-110">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="57684-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="57684-111">Andernfalls wird der Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="57684-111">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="57684-112">*pdefinitionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57684-112">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57684-113">Type: **Konstanten [**D3D \_ Shader- \_ Makro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="57684-113">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="57684-114">Ein mit Null endendes Array von Shader-Makros (siehe [**D3D \_ Shader \_ Macro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); legen Sie diese Einstellung auf **null** fest, um keine Makros anzugeben.</span><span class="sxs-lookup"><span data-stu-id="57684-114">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="57684-115">*pinclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57684-115">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57684-116">Typ: **[ **ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="57684-116">Type: **[**ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))\***</span></span>

<span data-ttu-id="57684-117">Ein Zeiger auf eine include-Schnittstelle (siehe [**ID3D10Include-Schnittstelle**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="57684-117">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="57684-118">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="57684-118">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="57684-119">*pprofile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57684-119">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57684-120">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="57684-120">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="57684-121">Eine Zeichenfolge, die das [Shader-Profil](../direct3dhlsl/dx-graphics-hlsl-models.md)oder Shader-Modell angibt.</span><span class="sxs-lookup"><span data-stu-id="57684-121">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md), or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="57684-122">*Hlslflags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57684-122">*HLSLFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57684-123">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="57684-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="57684-124">HLSL-Kompilierungsoptionen (siehe [d3d10 \_ Shader Konstanten](d3d10-shader.md)).</span><span class="sxs-lookup"><span data-stu-id="57684-124">HLSL compile options (see [D3D10\_SHADER Constants](d3d10-shader.md)).</span></span>

</dd> <dt>

<span data-ttu-id="57684-125">*Fxflags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57684-125">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57684-126">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="57684-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="57684-127">Effekt Kompilierungsoptionen (siehe [Kompilierungs-und Wirkungs Flags](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="57684-127">Effect compile options (see [Compile and Effect Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="57684-128">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57684-128">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57684-129">Typ: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="57684-129">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="57684-130">Ein Zeiger auf das Gerät (siehe [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)), von dem die Ressourcen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="57684-130">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="57684-131">"Peer"- *Pool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57684-131">*pEffectPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57684-132">Typ: **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span><span class="sxs-lookup"><span data-stu-id="57684-132">Type: **[**ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span></span>

<span data-ttu-id="57684-133">Zeiger auf einen Effekt Pool (siehe [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) für die Freigabe von Variablen zwischen Effekten.</span><span class="sxs-lookup"><span data-stu-id="57684-133">Pointer to an effect pool (see [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) for sharing variables between effects.</span></span>

</dd> <dt>

<span data-ttu-id="57684-134">*ppump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57684-134">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57684-135">Typ: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="57684-135">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="57684-136">Ein Zeiger auf eine Thread-Pump Schnittstelle (siehe [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="57684-136">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="57684-137">Verwenden Sie **null** , um anzugeben, dass diese Funktion erst zurückgegeben werden soll, wenn Sie abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="57684-137">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="57684-138">*ppeer-ect* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="57684-138">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57684-139">Typ: **[ **ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)\*\***</span><span class="sxs-lookup"><span data-stu-id="57684-139">Type: **[**ID3D10Effect**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)\*\***</span></span>

<span data-ttu-id="57684-140">Adresse eines Zeigers auf den Effekt (siehe [**ID3D10Effect Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)), der erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="57684-140">Address of a pointer to the effect (see [**ID3D10Effect Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effect)) that is created.</span></span>

</dd> <dt>

<span data-ttu-id="57684-141">*pperroren* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="57684-141">*ppErrors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57684-142">Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="57684-142">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="57684-143">Die Adresse eines Zeigers auf den Speicher (siehe [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)), die Auswirkungen auf Kompilierungsfehler enthält (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="57684-143">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="57684-144">*phresult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="57684-144">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57684-145">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="57684-145">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="57684-146">Ein Zeiger auf den Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="57684-146">A pointer to the return value.</span></span> <span data-ttu-id="57684-147">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="57684-147">May be **NULL**.</span></span> <span data-ttu-id="57684-148">Wenn *ppump* nicht **null** ist, muss *phresult* eine gültige Speicheradresse sein, bis die asynchrone Ausführung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="57684-148">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57684-149">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="57684-149">Return value</span></span>

<span data-ttu-id="57684-150">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="57684-150">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="57684-151">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="57684-151">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="57684-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="57684-152">Requirements</span></span>



| <span data-ttu-id="57684-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="57684-153">Requirement</span></span> | <span data-ttu-id="57684-154">Wert</span><span class="sxs-lookup"><span data-stu-id="57684-154">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="57684-155">Header</span><span class="sxs-lookup"><span data-stu-id="57684-155">Header</span></span><br/> | <dl> <span data-ttu-id="57684-156"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="57684-156"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57684-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="57684-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57684-158">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="57684-158">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
