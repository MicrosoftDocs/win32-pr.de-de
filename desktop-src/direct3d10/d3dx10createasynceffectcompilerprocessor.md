---
description: Erstellen eines asynchronen Daten Prozessors für einen Effekt
ms.assetid: 90a0dcd1-e495-4068-9f28-e2645370b984
title: D3DX10CreateAsyncEffectCompilerProcessor-Funktion (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncEffectCompilerProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 9e1e5716228537d505adc4f48179ec7027b57198
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355024"
---
# <a name="d3dx10createasynceffectcompilerprocessor-function"></a><span data-ttu-id="1111c-103">D3DX10CreateAsyncEffectCompilerProcessor-Funktion</span><span class="sxs-lookup"><span data-stu-id="1111c-103">D3DX10CreateAsyncEffectCompilerProcessor function</span></span>

<span data-ttu-id="1111c-104">Erstellen eines asynchronen Daten Prozessors für einen Effekt</span><span class="sxs-lookup"><span data-stu-id="1111c-104">Create an asynchronous-data processor for an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="1111c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1111c-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncEffectCompilerProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        UINT                 Flags,
  _In_        UINT                 FXFlags,
  _Out_       ID3D10Blob           **ppCompiledShader,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="1111c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1111c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1111c-107">*pfilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1111c-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1111c-108">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1111c-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1111c-109">Eine Zeichenfolge, die den Effekt Dateiname enthält.</span><span class="sxs-lookup"><span data-stu-id="1111c-109">A string that contains the effect filename.</span></span>

</dd> <dt>

<span data-ttu-id="1111c-110">*pdefinitionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1111c-110">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1111c-111">Type: **Konstanten [**D3D \_ Shader- \_ Makro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="1111c-111">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="1111c-112">Ein mit Null endendes Array von Shader-Makros (siehe [**D3D \_ Shader \_ Macro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); legen Sie diese Einstellung auf **null** fest, um keine Makros anzugeben.</span><span class="sxs-lookup"><span data-stu-id="1111c-112">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="1111c-113">*pinclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1111c-113">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1111c-114">Typ: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="1111c-114">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="1111c-115">Ein Zeiger auf eine include-Schnittstelle (siehe [**ID3D10Include-Schnittstelle**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="1111c-115">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="1111c-116">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="1111c-116">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1111c-117">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="1111c-117">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1111c-118">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1111c-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1111c-119">[HLSL-Kompilierungsoptionen](d3d10-graphics-reference-effect-constants.md).</span><span class="sxs-lookup"><span data-stu-id="1111c-119">[HLSL compile options](d3d10-graphics-reference-effect-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="1111c-120">*Fxflags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1111c-120">*FXFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1111c-121">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1111c-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1111c-122">[Effekt Kompilierungsoptionen](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="1111c-122">[Effect compile options](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="1111c-123">*ppcompiledshader* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1111c-123">*ppCompiledShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1111c-124">Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="1111c-124">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="1111c-125">Adresse eines Zeigers auf den Puffer (siehe [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)), der den kompilierten Effekt enthält.</span><span class="sxs-lookup"><span data-stu-id="1111c-125">Address of a pointer to buffer (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains the compiled effect.</span></span>

</dd> <dt>

<span data-ttu-id="1111c-126">*pperrorbuffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1111c-126">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1111c-127">Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="1111c-127">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="1111c-128">Adresse eines Zeigers auf einen Puffer (siehe [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)), der Kompilierungsfehler enthält.</span><span class="sxs-lookup"><span data-stu-id="1111c-128">Address of a pointer to a buffer (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)) that contains compile errors.</span></span>

</dd> <dt>

<span data-ttu-id="1111c-129">*ppdataprocessor* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1111c-129">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1111c-130">Typ: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="1111c-130">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="1111c-131">Adresse eines Zeigers auf einen Puffer, der den erstellten Datenprozessor enthält (siehe [**ID3DX10DataProcessor-Schnittstelle**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="1111c-131">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1111c-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1111c-132">Return value</span></span>

<span data-ttu-id="1111c-133">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1111c-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1111c-134">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="1111c-134">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1111c-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1111c-135">Requirements</span></span>



| <span data-ttu-id="1111c-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1111c-136">Requirement</span></span> | <span data-ttu-id="1111c-137">Wert</span><span class="sxs-lookup"><span data-stu-id="1111c-137">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1111c-138">Header</span><span class="sxs-lookup"><span data-stu-id="1111c-138">Header</span></span><br/> | <dl> <span data-ttu-id="1111c-139"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="1111c-139"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1111c-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1111c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1111c-141">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="1111c-141">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
