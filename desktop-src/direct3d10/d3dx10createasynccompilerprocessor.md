---
description: Erstellen eines asynchronen Daten Prozessors für einen Shader.
ms.assetid: e23290fa-ccd7-4703-ae6b-4fffe352875e
title: D3DX10CreateAsyncCompilerProcessor-Funktion (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncCompilerProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 1fa6a558efd56917832da3280df2aad4ac400def
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219475"
---
# <a name="d3dx10createasynccompilerprocessor-function"></a><span data-ttu-id="80deb-103">D3DX10CreateAsyncCompilerProcessor-Funktion</span><span class="sxs-lookup"><span data-stu-id="80deb-103">D3DX10CreateAsyncCompilerProcessor function</span></span>

<span data-ttu-id="80deb-104">Erstellen eines asynchronen Daten Prozessors für einen Shader.</span><span class="sxs-lookup"><span data-stu-id="80deb-104">Create an asynchronous-data processor for a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="80deb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="80deb-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncCompilerProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D10_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pFunctionName,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags1,
  _In_        UINT                 Flags2,
  _Out_       ID3D10Blob           **ppCompiledShader,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="80deb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="80deb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80deb-107">*pfilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80deb-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80deb-108">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="80deb-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="80deb-109">Eine Zeichenfolge, die den Shader-Dateinamen enthält.</span><span class="sxs-lookup"><span data-stu-id="80deb-109">A string that contains the shader filename.</span></span>

</dd> <dt>

<span data-ttu-id="80deb-110">*pdefinitionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80deb-110">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80deb-111">Type: **Konstanten [**D3D \_ Shader- \_ Makro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="80deb-111">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="80deb-112">Ein mit Null endendes Array von Shader-Makros (siehe [**D3D \_ Shader \_ Macro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); legen Sie diese Einstellung auf **null** fest, um keine Makros anzugeben.</span><span class="sxs-lookup"><span data-stu-id="80deb-112">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="80deb-113">*pinclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80deb-113">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80deb-114">Typ: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="80deb-114">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="80deb-115">Ein Zeiger auf eine include-Schnittstelle (siehe [**ID3D10Include-Schnittstelle**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="80deb-115">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))).</span></span> <span data-ttu-id="80deb-116">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="80deb-116">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="80deb-117">*pfunctionname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80deb-117">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80deb-118">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="80deb-118">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="80deb-119">Der Name der Shader-Einstiegspunkt Funktion, bei der die Shader-Ausführung beginnt.</span><span class="sxs-lookup"><span data-stu-id="80deb-119">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="80deb-120">Wenn Sie einen Effekt kompilieren,  ignoriert D3DX10CreateAsyncCompilerProcessor *pfunctionname*;. Es wird empfohlen, *pfunctionname* auf **null** festzulegen, da es eine gute Programmierpraxis ist, einen Zeiger Parameter auf **null** festzulegen, wenn die aufgerufene Funktion ihn nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="80deb-120">When you compile an effect, **D3DX10CreateAsyncCompilerProcessor** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="80deb-121">*pprofile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80deb-121">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80deb-122">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="80deb-122">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="80deb-123">Eine Zeichenfolge, die das [Shader-Profil](../direct3dhlsl/dx-graphics-hlsl-models.md) oder Shader-Modell angibt.</span><span class="sxs-lookup"><span data-stu-id="80deb-123">A string that specifies the [shader profile](../direct3dhlsl/dx-graphics-hlsl-models.md) or shader model.</span></span>

</dd> <dt>

<span data-ttu-id="80deb-124">*Flags1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80deb-124">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80deb-125">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="80deb-125">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="80deb-126">[Shader-Kompilierungs Flags](d3d10-shader.md).</span><span class="sxs-lookup"><span data-stu-id="80deb-126">[Shader compile flags](d3d10-shader.md).</span></span>

</dd> <dt>

<span data-ttu-id="80deb-127">*Flags2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80deb-127">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80deb-128">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="80deb-128">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="80deb-129">[Effekt Kompilierungs Flags](d3d10-graphics-reference-effect-constants.md).</span><span class="sxs-lookup"><span data-stu-id="80deb-129">[Effect compile flags](d3d10-graphics-reference-effect-constants.md).</span></span> <span data-ttu-id="80deb-130">Wenn Sie einen Shader und keine Effekt Datei kompilieren, ignoriert **D3DX10CreateAsyncCompilerProcessor** *Flags2*; Es wird empfohlen, *Flags2* auf NULL festzulegen, da es eine gute Programmierpraxis ist, einen Zeiger Parameter auf **null** festzulegen, wenn die aufgerufene Funktion ihn nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="80deb-130">When you compile a shader and not an effect file, **D3DX10CreateAsyncCompilerProcessor** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="80deb-131">*ppcompiledshader* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="80deb-131">*ppCompiledShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80deb-132">Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="80deb-132">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="80deb-133">Adresse eines Zeigers auf den kompilierten Effekt (siehe [**ID3D10Blob-Schnittstelle**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span><span class="sxs-lookup"><span data-stu-id="80deb-133">Address of a pointer to the compiled effect (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span></span>

</dd> <dt>

<span data-ttu-id="80deb-134">*pperrorbuffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="80deb-134">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80deb-135">Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="80deb-135">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="80deb-136">Adresse eines Zeigers auf Kompilierungsfehler (siehe [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span><span class="sxs-lookup"><span data-stu-id="80deb-136">Address of a pointer to compile errors (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span></span>

</dd> <dt>

<span data-ttu-id="80deb-137">*ppdataprocessor* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="80deb-137">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80deb-138">Typ: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="80deb-138">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="80deb-139">Adresse eines Zeigers auf einen Puffer, der den erstellten Datenprozessor enthält (siehe [**ID3DX10DataProcessor-Schnittstelle**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="80deb-139">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80deb-140">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="80deb-140">Return value</span></span>

<span data-ttu-id="80deb-141">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="80deb-141">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="80deb-142">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="80deb-142">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="80deb-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="80deb-143">Requirements</span></span>



| <span data-ttu-id="80deb-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="80deb-144">Requirement</span></span> | <span data-ttu-id="80deb-145">Wert</span><span class="sxs-lookup"><span data-stu-id="80deb-145">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="80deb-146">Header</span><span class="sxs-lookup"><span data-stu-id="80deb-146">Header</span></span><br/> | <dl> <span data-ttu-id="80deb-147"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="80deb-147"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80deb-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80deb-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80deb-149">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="80deb-149">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
