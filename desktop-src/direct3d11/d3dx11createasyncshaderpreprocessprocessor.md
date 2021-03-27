---
title: D3DX11CreateAsyncShaderPreprocessProcessor-Funktion (D3DX11async. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Siehe Hinweise. Erstellen Sie einen Datenprozessor für einen Shader asynchron.
ms.assetid: a7e9754b-acc1-49d0-bd8e-b116bc3c7e3a
keywords:
- D3DX11CreateAsyncShaderPreprocessProcessor-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncShaderPreprocessProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46e58b267f186e5fd0104b10e9f9423f407aaf13
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961684"
---
# <a name="d3dx11createasyncshaderpreprocessprocessor-function"></a><span data-ttu-id="e4d11-106">D3DX11CreateAsyncShaderPreprocessProcessor-Funktion</span><span class="sxs-lookup"><span data-stu-id="e4d11-106">D3DX11CreateAsyncShaderPreprocessProcessor function</span></span>

> [!Note]  
> <span data-ttu-id="e4d11-107">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e4d11-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="e4d11-108">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="e4d11-108">See Remarks.</span></span>

 

<span data-ttu-id="e4d11-109">Erstellen Sie einen Datenprozessor für einen Shader asynchron.</span><span class="sxs-lookup"><span data-stu-id="e4d11-109">Create a data processor for a shader asynchronously.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4d11-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4d11-110">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncShaderPreprocessProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D11_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _Out_       ID3D10Blob           **ppShaderText,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX11DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="e4d11-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4d11-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4d11-112">*pfilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4d11-112">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4d11-113">Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e4d11-113">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e4d11-114">Eine Zeichenfolge, die den Shader-Dateinamen enthält.</span><span class="sxs-lookup"><span data-stu-id="e4d11-114">A string that contains the shader filename.</span></span>

</dd> <dt>

<span data-ttu-id="e4d11-115">*pdefinitionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4d11-115">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4d11-116">Type: **Konstanten D3D11 \_ Shader- \_ Makro \***</span><span class="sxs-lookup"><span data-stu-id="e4d11-116">Type: **const D3D11\_SHADER\_MACRO\***</span></span>

<span data-ttu-id="e4d11-117">Ein mit Null endendes Array von Shader-Makros. Legen Sie diese Einstellung auf **null** fest, um keine Makros anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e4d11-117">A NULL-terminated array of shader macros; set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="e4d11-118">*pinclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4d11-118">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4d11-119">Typ: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="e4d11-119">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="e4d11-120">Ein Zeiger auf eine include-Schnittstelle. Legen Sie dies auf **null** fest, um anzugeben, dass keine Includedatei vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e4d11-120">A pointer to an include interface; set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="e4d11-121">*ppshadertext* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e4d11-121">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4d11-122">Typ: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="e4d11-122">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="e4d11-123">Adresse eines Zeigers auf einen Puffer, der den ASCII-Text des Shaders enthält.</span><span class="sxs-lookup"><span data-stu-id="e4d11-123">Address of a pointer to a buffer that contains the ASCII text of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="e4d11-124">*pperrorbuffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e4d11-124">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4d11-125">Typ: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="e4d11-125">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="e4d11-126">Adresse eines Zeigers auf einen Puffer, der Kompilierungsfehler enthält.</span><span class="sxs-lookup"><span data-stu-id="e4d11-126">Address of a pointer to a buffer that contains compile errors.</span></span>

</dd> <dt>

<span data-ttu-id="e4d11-127">*ppdataprocessor* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e4d11-127">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4d11-128">Typ: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="e4d11-128">Type: **[**ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span></span>

<span data-ttu-id="e4d11-129">Adresse eines Zeigers auf einen Puffer, der den erstellten Datenprozessor enthält (siehe [**ID3DX11DataProcessor-Schnittstelle**](id3dx11dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="e4d11-129">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX11DataProcessor Interface**](id3dx11dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4d11-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e4d11-130">Return value</span></span>

<span data-ttu-id="e4d11-131">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e4d11-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e4d11-132">Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="e4d11-132">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e4d11-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e4d11-133">Remarks</span></span>

<span data-ttu-id="e4d11-134">Es gibt keine Implementierung des Async-Lade Moduls außerhalb von D3DX 10 und D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="e4d11-134">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="e4d11-135">Für Windows Store-Apps enthalten die DirectX-Beispiele (z. b. das [Direct3D-tutorialbeispiel](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) das **basicloader** -Modul, das das asynchrone Programmiermodell ([**asyncbase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))) Windows-Runtime verwendet.</span><span class="sxs-lookup"><span data-stu-id="e4d11-135">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="e4d11-136">Für Win32-Desktop-Apps können Sie den [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) verwenden, um etwas ähnliches wie das Windows-Runtime asynchrone Programmiermodell zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="e4d11-136">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4d11-137">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="e4d11-137">Requirements</span></span>



| <span data-ttu-id="e4d11-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e4d11-138">Requirement</span></span> | <span data-ttu-id="e4d11-139">Wert</span><span class="sxs-lookup"><span data-stu-id="e4d11-139">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4d11-140">Header</span><span class="sxs-lookup"><span data-stu-id="e4d11-140">Header</span></span><br/>  | <dl> <span data-ttu-id="e4d11-141"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4d11-141"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="e4d11-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e4d11-142">Library</span></span><br/> | <dl> <span data-ttu-id="e4d11-143"><dt>Bibliothek d3dx11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e4d11-143"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="e4d11-144">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e4d11-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4d11-145">D3DX-Funktionen</span><span class="sxs-lookup"><span data-stu-id="e4d11-145">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

