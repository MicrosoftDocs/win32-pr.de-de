---
description: Erstellen Sie einen Datenprozessor für einen Shader asynchron.
ms.assetid: f5521e55-5f20-422d-979e-98b70efd3b13
title: D3DX10CreateAsyncShaderPreprocessProcessor-Funktion (D3DX10Async.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncShaderPreprocessProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 14afdb899d99b7c0278d3042fbc9a108f446c692
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366678"
---
# <a name="d3dx10createasyncshaderpreprocessprocessor-function"></a><span data-ttu-id="31f00-103">D3DX10CreateAsyncShaderPreprocessProcessor-Funktion</span><span class="sxs-lookup"><span data-stu-id="31f00-103">D3DX10CreateAsyncShaderPreprocessProcessor function</span></span>

<span data-ttu-id="31f00-104">Erstellen Sie einen Datenprozessor für einen Shader asynchron.</span><span class="sxs-lookup"><span data-stu-id="31f00-104">Create a data processor for a shader asynchronously.</span></span>

## <a name="syntax"></a><span data-ttu-id="31f00-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="31f00-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncShaderPreprocessProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _Out_       ID3D10Blob           **ppShaderText,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX10DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="31f00-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="31f00-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31f00-107">*pfilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="31f00-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31f00-108">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31f00-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="31f00-109">Eine Zeichenfolge, die den Shader-Dateinamen enthält.</span><span class="sxs-lookup"><span data-stu-id="31f00-109">A string that contains the shader filename.</span></span>

</dd> <dt>

<span data-ttu-id="31f00-110">*pdefinitionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="31f00-110">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31f00-111">Type: **Konstanten [**D3D \_ Shader- \_ Makro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) \***</span><span class="sxs-lookup"><span data-stu-id="31f00-111">Type: **const [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)\***</span></span>

<span data-ttu-id="31f00-112">Ein mit Null endendes Array von Shader-Makros (siehe [**D3D \_ Shader \_ Macro**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); legen Sie diese Einstellung auf **null** fest, um keine Makros anzugeben.</span><span class="sxs-lookup"><span data-stu-id="31f00-112">A NULL-terminated array of shader macros (see [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)); set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="31f00-113">*pinclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="31f00-113">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31f00-114">Typ: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="31f00-114">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="31f00-115">Ein Zeiger auf eine include-Schnittstelle (siehe [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); Legen Sie dies auf **null** fest, um anzugeben, dass keine Includedatei vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="31f00-115">A pointer to an include interface (see [**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))); set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="31f00-116">*ppshadertext* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="31f00-116">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31f00-117">Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="31f00-117">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="31f00-118">Adresse eines Zeigers auf einen Puffer, der den ASCII-Text des Shader enthält (siehe [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span><span class="sxs-lookup"><span data-stu-id="31f00-118">Address of a pointer to a buffer that contains the ASCII text of the shader (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span></span>

</dd> <dt>

<span data-ttu-id="31f00-119">*pperrorbuffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="31f00-119">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31f00-120">Typ: **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="31f00-120">Type: **[**ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="31f00-121">Adresse eines Zeigers auf einen Puffer, der Kompilierungsfehler enthält (siehe [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span><span class="sxs-lookup"><span data-stu-id="31f00-121">Address of a pointer to a buffer that contains compile errors (see [**ID3D10Blob Interface**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)).</span></span>

</dd> <dt>

<span data-ttu-id="31f00-122">*ppdataprocessor* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="31f00-122">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31f00-123">Typ: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="31f00-123">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="31f00-124">Adresse eines Zeigers auf einen Puffer, der den erstellten Datenprozessor enthält (siehe [**ID3DX10DataProcessor-Schnittstelle**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="31f00-124">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31f00-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="31f00-125">Return value</span></span>

<span data-ttu-id="31f00-126">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="31f00-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="31f00-127">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="31f00-127">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="31f00-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31f00-128">Requirements</span></span>



| <span data-ttu-id="31f00-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="31f00-129">Requirement</span></span> | <span data-ttu-id="31f00-130">Wert</span><span class="sxs-lookup"><span data-stu-id="31f00-130">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="31f00-131">Header</span><span class="sxs-lookup"><span data-stu-id="31f00-131">Header</span></span><br/> | <dl> <span data-ttu-id="31f00-132"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="31f00-132"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31f00-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31f00-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31f00-134">Universell Funktionen</span><span class="sxs-lookup"><span data-stu-id="31f00-134">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
