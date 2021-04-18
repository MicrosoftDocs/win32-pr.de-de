---
description: Kompilieren Sie einen Shader, und erstellen Sie asynchron einen Datenprozessor.
ms.assetid: 842db48b-51a7-4f32-8ea6-44247f2619b0
title: D3DX10CreateAsyncShaderCompilerProcessor-Funktion (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncShaderCompilerProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 2a1cd663827cc32b868c9c6c9b74fbc3c21b8ee6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394094"
---
# <a name="d3dx10createasyncshadercompilerprocessor-function"></a><span data-ttu-id="ae9f0-103">D3DX10CreateAsyncShaderCompilerProcessor-Funktion</span><span class="sxs-lookup"><span data-stu-id="ae9f0-103">D3DX10CreateAsyncShaderCompilerProcessor function</span></span>

<span data-ttu-id="ae9f0-104">Kompilieren Sie einen Shader, und erstellen Sie asynchron einen Datenprozessor.</span><span class="sxs-lookup"><span data-stu-id="ae9f0-104">Compile a shader and create a data processor asynchronously.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae9f0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae9f0-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncShaderCompilerProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pFunctionName,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags,
  _Out_       ID3D10Blob           **ppCompiledShader,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="ae9f0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae9f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae9f0-107">*pfilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae9f0-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae9f0-108">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ae9f0-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ae9f0-109">Eine Zeichenfolge, die den Shader-Dateinamen enthält.</span><span class="sxs-lookup"><span data-stu-id="ae9f0-109">A string that contains the shader filename.</span></span>

</dd> <dt>

<span data-ttu-id="ae9f0-110">*pdefinitionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae9f0-110">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae9f0-111">Type: **Konstanten [**D3D \_ Shader- \_ Makro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="ae9f0-111">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="ae9f0-112">Ein mit Null endendes Array von Shader-Makros (siehe [**D3D \_ Shader \_ Macro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); legen Sie diese Einstellung auf **null** fest, um keine Makros anzugeben.</span><span class="sxs-lookup"><span data-stu-id="ae9f0-112">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="ae9f0-113">*pinclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae9f0-113">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae9f0-114">Typ: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="ae9f0-114">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="ae9f0-115">Ein Zeiger auf eine include-Schnittstelle (siehe [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); Legen Sie dies auf **null** fest, um anzugeben, dass keine Includedatei vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ae9f0-115">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="ae9f0-116">*pfunctionname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae9f0-116">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae9f0-117">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ae9f0-117">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ae9f0-118">Der Name der Einstiegspunkt Funktion für den Shader.</span><span class="sxs-lookup"><span data-stu-id="ae9f0-118">Name of the entry point function for the shader.</span></span>

</dd> <dt>

<span data-ttu-id="ae9f0-119">*pprofile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae9f0-119">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae9f0-120">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ae9f0-120">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ae9f0-121">Eine Zeichenfolge, die das [Shader-Profil](../direct3dhlsl/dx-graphics-hlsl-models.md) oder Shader-Modell angibt.</span><span class="sxs-lookup"><span data-stu-id="ae9f0-121">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md) or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="ae9f0-122">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="ae9f0-122">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae9f0-123">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ae9f0-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ae9f0-124">HLSL-Kompilierungsoptionen (siehe [Shader-Flags](d3d10-graphics-reference-effect-constants.md)).</span><span class="sxs-lookup"><span data-stu-id="ae9f0-124">HLSL compile options (see [Shader Flags](d3d10-graphics-reference-effect-constants.md)).</span></span>

</dd> <dt>

<span data-ttu-id="ae9f0-125">*ppcompiledshader* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ae9f0-125">*ppCompiledShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae9f0-126">Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="ae9f0-126">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="ae9f0-127">Adresse eines Zeigers auf den kompilierten Shader.</span><span class="sxs-lookup"><span data-stu-id="ae9f0-127">Address of a pointer to the compiled shader.</span></span> <span data-ttu-id="ae9f0-128">Siehe [**ID3D10Blob-Schnittstelle**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob).</span><span class="sxs-lookup"><span data-stu-id="ae9f0-128">See [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob).</span></span>

</dd> <dt>

<span data-ttu-id="ae9f0-129">*pperrorbuffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ae9f0-129">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae9f0-130">Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="ae9f0-130">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="ae9f0-131">Adresse eines Zeigers auf einen Puffer, der Kompilierungsfehler enthält (siehe [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span><span class="sxs-lookup"><span data-stu-id="ae9f0-131">Address of a pointer to a buffer that contains compile errors (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span></span>

</dd> <dt>

<span data-ttu-id="ae9f0-132">*ppdataprocessor* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ae9f0-132">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae9f0-133">Typ: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="ae9f0-133">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="ae9f0-134">Adresse eines Zeigers auf einen Puffer, der den erstellten Datenprozessor enthält (siehe [**ID3DX10DataProcessor-Schnittstelle**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="ae9f0-134">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae9f0-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ae9f0-135">Return value</span></span>

<span data-ttu-id="ae9f0-136">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ae9f0-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ae9f0-137">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="ae9f0-137">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ae9f0-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ae9f0-138">Requirements</span></span>



| <span data-ttu-id="ae9f0-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ae9f0-139">Requirement</span></span> | <span data-ttu-id="ae9f0-140">Wert</span><span class="sxs-lookup"><span data-stu-id="ae9f0-140">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae9f0-141">Header</span><span class="sxs-lookup"><span data-stu-id="ae9f0-141">Header</span></span><br/> | <dl> <span data-ttu-id="ae9f0-142"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae9f0-142"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae9f0-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ae9f0-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae9f0-144">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="ae9f0-144">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
