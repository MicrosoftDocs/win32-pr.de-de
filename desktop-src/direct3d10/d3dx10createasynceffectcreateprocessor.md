---
description: Erstellen Sie einen Effekt Pool asynchron.
ms.assetid: 50c55751-26de-4002-9a89-8e5ab59dda79
title: D3DX10CreateAsyncEffectCreateProcessor-Funktion (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncEffectCreateProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 573efc51214031afe66f6cfd552bbda634d15142
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366630"
---
# <a name="d3dx10createasynceffectcreateprocessor-function"></a><span data-ttu-id="a23f6-103">D3DX10CreateAsyncEffectCreateProcessor-Funktion</span><span class="sxs-lookup"><span data-stu-id="a23f6-103">D3DX10CreateAsyncEffectCreateProcessor function</span></span>

<span data-ttu-id="a23f6-104">Erstellen Sie einen Effekt Pool asynchron.</span><span class="sxs-lookup"><span data-stu-id="a23f6-104">Create an effect pool asynchronously.</span></span>

## <a name="syntax"></a><span data-ttu-id="a23f6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a23f6-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncEffectCreateProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags,
  _In_        UINT                 FXFlags,
  _In_        ID3D10Device         *pDevice,
  _In_        ID3D10EffectPool     *pPool,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="a23f6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a23f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a23f6-107">*pfilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a23f6-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a23f6-108">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a23f6-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a23f6-109">Eine Zeichenfolge, die den Effekt Dateiname enthält.</span><span class="sxs-lookup"><span data-stu-id="a23f6-109">A string that contains the effect filename.</span></span>

</dd> <dt>

<span data-ttu-id="a23f6-110">*pdefinitionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a23f6-110">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a23f6-111">Type: **Konstanten [**D3D \_ Shader- \_ Makro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="a23f6-111">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="a23f6-112">Ein mit Null endendes Array von Shader-Makros (siehe [**D3D \_ Shader \_ Macro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); legen Sie diese Einstellung auf **null** fest, um keine Makros anzugeben.</span><span class="sxs-lookup"><span data-stu-id="a23f6-112">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="a23f6-113">*pinclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a23f6-113">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a23f6-114">Typ: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="a23f6-114">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="a23f6-115">Ein Zeiger auf eine include-Schnittstelle (siehe [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); Legen Sie dies auf **null** fest, um anzugeben, dass keine Includedatei vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a23f6-115">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="a23f6-116">*pprofile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a23f6-116">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a23f6-117">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a23f6-117">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a23f6-118">Eine Zeichenfolge, die das [Shader-Profil](../direct3dhlsl/dx-graphics-hlsl-models.md) oder Shader-Modell angibt.</span><span class="sxs-lookup"><span data-stu-id="a23f6-118">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md) or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="a23f6-119">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="a23f6-119">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a23f6-120">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a23f6-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a23f6-121">HLSL-Kompilierungsoptionen (siehe [Shader-Flags](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="a23f6-121">HLSL compile options (see [Shader Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="a23f6-122">*Fxflags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a23f6-122">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a23f6-123">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a23f6-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a23f6-124">Effekt Kompilierungsoptionen (siehe [Kompilierungs-und Wirkungs Flags](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="a23f6-124">Effect compile options (see [Compile and Effect Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="a23f6-125">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a23f6-125">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a23f6-126">Typ: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="a23f6-126">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="a23f6-127">Ein Zeiger auf das Gerät (siehe [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)), von dem die Ressourcen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a23f6-127">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="a23f6-128">*ppool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a23f6-128">*pPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a23f6-129">Typ: **[ **ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span><span class="sxs-lookup"><span data-stu-id="a23f6-129">Type: **[**ID3D10EffectPool**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)\***</span></span>

<span data-ttu-id="a23f6-130">Ein Zeiger auf einen Effekt Pool (siehe [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) für die Freigabe von Variablen zwischen Effekten.</span><span class="sxs-lookup"><span data-stu-id="a23f6-130">A pointer to an effect pool (see [**ID3D10EffectPool Interface**](/windows/win32/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)) for sharing variables between effects.</span></span>

</dd> <dt>

<span data-ttu-id="a23f6-131">*pperrorbuffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a23f6-131">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a23f6-132">Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="a23f6-132">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="a23f6-133">Die Adresse eines Zeigers auf den Speicher (siehe [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)), die Auswirkungen auf Kompilierungsfehler enthält (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="a23f6-133">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="a23f6-134">*ppprocessor* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a23f6-134">*ppProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a23f6-135">Typ: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="a23f6-135">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="a23f6-136">Die Adresse eines Zeigers auf den asynchronen Datenprozessor (siehe [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="a23f6-136">The address of a pointer to the asynchronous-data processor (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a23f6-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a23f6-137">Return value</span></span>

<span data-ttu-id="a23f6-138">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a23f6-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a23f6-139">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="a23f6-139">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a23f6-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a23f6-140">Requirements</span></span>



| <span data-ttu-id="a23f6-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a23f6-141">Requirement</span></span> | <span data-ttu-id="a23f6-142">Wert</span><span class="sxs-lookup"><span data-stu-id="a23f6-142">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a23f6-143">Header</span><span class="sxs-lookup"><span data-stu-id="a23f6-143">Header</span></span><br/> | <dl> <span data-ttu-id="a23f6-144"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="a23f6-144"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a23f6-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a23f6-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a23f6-146">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="a23f6-146">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
