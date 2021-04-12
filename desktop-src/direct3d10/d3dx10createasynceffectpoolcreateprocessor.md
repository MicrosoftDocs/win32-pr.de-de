---
description: Erstellen Sie einen asynchronen Datenprozessor für einen Speicherpool.
ms.assetid: 3985a5e5-492e-4003-9d10-6e34620de69f
title: D3DX10CreateAsyncEffectPoolCreateProcessor-Funktion (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncEffectPoolCreateProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 32e7c60f28a823c624b3866a8cdd46db659f8a49
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219572"
---
# <a name="d3dx10createasynceffectpoolcreateprocessor-function"></a><span data-ttu-id="c5dba-103">D3DX10CreateAsyncEffectPoolCreateProcessor-Funktion</span><span class="sxs-lookup"><span data-stu-id="c5dba-103">D3DX10CreateAsyncEffectPoolCreateProcessor function</span></span>

<span data-ttu-id="c5dba-104">Erstellen Sie einen asynchronen Datenprozessor für einen Speicherpool.</span><span class="sxs-lookup"><span data-stu-id="c5dba-104">Create an asynchronous-data processor for a memory pool.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5dba-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5dba-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncEffectPoolCreateProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags,
  _In_        UINT                 FXFlags,
  _In_        ID3D10Device         *pDevice,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="c5dba-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5dba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5dba-107">*pfilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5dba-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5dba-108">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5dba-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c5dba-109">Eine Zeichenfolge, die den Effekt Dateiname enthält.</span><span class="sxs-lookup"><span data-stu-id="c5dba-109">A string that contains the effect filename.</span></span>

</dd> <dt>

<span data-ttu-id="c5dba-110">*pdefinitionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5dba-110">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5dba-111">Type: **Konstanten [**D3D \_ Shader- \_ Makro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="c5dba-111">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="c5dba-112">Ein mit Null endendes Array von Shader-Makros (siehe [**D3D \_ Shader \_ Macro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); legen Sie diese Einstellung auf **null** fest, um keine Makros anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c5dba-112">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="c5dba-113">*pinclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5dba-113">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5dba-114">Typ: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="c5dba-114">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="c5dba-115">Ein Zeiger auf eine include-Schnittstelle (siehe [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); Legen Sie dies auf **null** fest, um anzugeben, dass keine Includedatei vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c5dba-115">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="c5dba-116">*pprofile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5dba-116">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5dba-117">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5dba-117">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c5dba-118">Eine Zeichenfolge, die das [Shader-Profil](../direct3dhlsl/dx-graphics-hlsl-models.md) oder Shader-Modell angibt.</span><span class="sxs-lookup"><span data-stu-id="c5dba-118">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md) or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="c5dba-119">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="c5dba-119">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5dba-120">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5dba-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c5dba-121">HLSL-Kompilierungsoptionen (siehe [Shader-Flags](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="c5dba-121">HLSL compile options (see [Shader Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="c5dba-122">*Fxflags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5dba-122">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5dba-123">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5dba-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c5dba-124">Effekt Kompilierungsoptionen (siehe [Kompilierungs-und Wirkungs Flags](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="c5dba-124">Effect compile options (see [Compile and Effect Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="c5dba-125">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5dba-125">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5dba-126">Typ: **[ **ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="c5dba-126">Type: **[**ID3D10Device**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="c5dba-127">Ein Zeiger auf das Gerät (siehe [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)), von dem die Ressourcen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c5dba-127">A pointer to the device (see [**ID3D10Device Interface**](/windows/win32/api/D3D10/nn-d3d10-id3d10device)) that will use the resources.</span></span>

</dd> <dt>

<span data-ttu-id="c5dba-128">*pperrorbuffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c5dba-128">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5dba-129">Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="c5dba-129">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="c5dba-130">Die Adresse eines Zeigers auf den Speicher (siehe [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)), die Auswirkungen auf Kompilierungsfehler enthält (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="c5dba-130">The address of a pointer to memory (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains effect compile errors, if there were any.</span></span>

</dd> <dt>

<span data-ttu-id="c5dba-131">*ppdataprocessor* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c5dba-131">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5dba-132">Typ: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="c5dba-132">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="c5dba-133">Adresse eines Zeigers auf einen Puffer, der den erstellten Datenprozessor enthält (siehe [**ID3DX10DataProcessor-Schnittstelle**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="c5dba-133">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5dba-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c5dba-134">Return value</span></span>

<span data-ttu-id="c5dba-135">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c5dba-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c5dba-136">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="c5dba-136">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c5dba-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5dba-137">Requirements</span></span>



| <span data-ttu-id="c5dba-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c5dba-138">Requirement</span></span> | <span data-ttu-id="c5dba-139">Wert</span><span class="sxs-lookup"><span data-stu-id="c5dba-139">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5dba-140">Header</span><span class="sxs-lookup"><span data-stu-id="c5dba-140">Header</span></span><br/> | <dl> <span data-ttu-id="c5dba-141"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5dba-141"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5dba-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5dba-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5dba-143">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="c5dba-143">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
