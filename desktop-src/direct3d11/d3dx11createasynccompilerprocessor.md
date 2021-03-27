---
title: D3DX11CreateAsyncCompilerProcessor-Funktion (D3DX11async. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Siehe Hinweise. Erstellen eines asynchronen Daten Prozessors für einen Shader.
ms.assetid: 90756ac3-946d-49fa-9f97-70dc5da812c6
keywords:
- D3DX11CreateAsyncCompilerProcessor-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncCompilerProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 533e487e65640b8c17a0ff8d061388e8b5a6c0f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996051"
---
# <a name="d3dx11createasynccompilerprocessor-function"></a><span data-ttu-id="75140-106">D3DX11CreateAsyncCompilerProcessor-Funktion</span><span class="sxs-lookup"><span data-stu-id="75140-106">D3DX11CreateAsyncCompilerProcessor function</span></span>

> [!Note]  
> <span data-ttu-id="75140-107">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="75140-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="75140-108">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="75140-108">See Remarks.</span></span>

 

<span data-ttu-id="75140-109">Erstellen eines asynchronen Daten Prozessors für einen Shader.</span><span class="sxs-lookup"><span data-stu-id="75140-109">Create an asynchronous-data processor for a shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="75140-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="75140-110">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncCompilerProcessor(
  _In_        LPCSTR               pFileName,
  _In_  const D3D11_SHADER_MACRO   *pDefines,
  _In_        LPD3D10INCLUDE       pInclude,
  _In_        LPCSTR               pFunctionName,
  _In_        LPCSTR               pProfile,
  _In_        UINT                 Flags1,
  _In_        UINT                 Flags2,
  _Out_       ID3D10Blob           **ppCompiledShader,
  _Out_       ID3D10Blob           **ppErrorBuffer,
  _Out_       ID3DX11DataProcessor **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="75140-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="75140-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75140-112">*pfilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75140-112">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75140-113">Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="75140-113">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="75140-114">Eine Zeichenfolge, die den Shader-Dateinamen enthält.</span><span class="sxs-lookup"><span data-stu-id="75140-114">A string that contains the shader filename.</span></span>

</dd> <dt>

<span data-ttu-id="75140-115">*pdefinitionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75140-115">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75140-116">Type: **Konstanten D3D11 \_ Shader- \_ Makro \***</span><span class="sxs-lookup"><span data-stu-id="75140-116">Type: **const D3D11\_SHADER\_MACRO\***</span></span>

<span data-ttu-id="75140-117">Ein mit Null endendes Array von Shader-Makros. Legen Sie diese Einstellung auf **null** fest, um keine Makros anzugeben.</span><span class="sxs-lookup"><span data-stu-id="75140-117">A NULL-terminated array of shader macros; set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="75140-118">*pinclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75140-118">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75140-119">Typ: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="75140-119">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="75140-120">Ein Zeiger auf eine include-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="75140-120">A pointer to an include interface.</span></span> <span data-ttu-id="75140-121">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="75140-121">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="75140-122">*pfunctionname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75140-122">*pFunctionName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75140-123">Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="75140-123">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="75140-124">Der Name der Shader-Einstiegspunkt Funktion, bei der die Shader-Ausführung beginnt.</span><span class="sxs-lookup"><span data-stu-id="75140-124">Name of the shader-entry point function where shader execution begins.</span></span> <span data-ttu-id="75140-125">Wenn Sie einen Effekt kompilieren,  ignoriert D3DX11CreateAsyncCompilerProcessor *pfunctionname*;. Es wird empfohlen, *pfunctionname* auf **null** festzulegen, da es eine gute Programmierpraxis ist, einen Zeiger Parameter auf **null** festzulegen, wenn die aufgerufene Funktion ihn nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="75140-125">When you compile an effect, **D3DX11CreateAsyncCompilerProcessor** ignores *pFunctionName*; we recommend that you set *pFunctionName* to **NULL** because it is good programming practice to set a pointer parameter to **NULL** if the called function will not use it..</span></span>

</dd> <dt>

<span data-ttu-id="75140-126">*pprofile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75140-126">*pProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75140-127">Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="75140-127">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="75140-128">Eine Zeichenfolge, die das Shader-Profil oder Shader-Modell angibt. kann ein beliebiges Profil in Shader Model 2, Shader Model 3, Shader Model 4 oder Shader Model 5 sein.</span><span class="sxs-lookup"><span data-stu-id="75140-128">A string that specifies the shader profile or shader model; can be any profile in shader model 2, shader model 3, shader model 4, or shader model 5.</span></span> <span data-ttu-id="75140-129">Das Profil kann auch für den Typ "Effect" (z \_ . b. FX 4 \_ 1) sein.</span><span class="sxs-lookup"><span data-stu-id="75140-129">The profile can also be for effect type (for example, fx\_4\_1).</span></span>

</dd> <dt>

<span data-ttu-id="75140-130">*Flags1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75140-130">*Flags1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75140-131">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="75140-131">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="75140-132">Shader-Kompilierungs Flags.</span><span class="sxs-lookup"><span data-stu-id="75140-132">Shader compile flags.</span></span>

</dd> <dt>

<span data-ttu-id="75140-133">*Flags2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75140-133">*Flags2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75140-134">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="75140-134">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="75140-135">Effekt Kompilierungs Flags.</span><span class="sxs-lookup"><span data-stu-id="75140-135">Effect compile flags.</span></span> <span data-ttu-id="75140-136">Wenn Sie einen Shader und keine Effekt Datei kompilieren, ignoriert **D3DX11CreateAsyncCompilerProcessor** *Flags2*; Es wird empfohlen, *Flags2* auf NULL festzulegen, da es eine gute Programmierpraxis ist, einen Typ-Parameter auf 0 (null) festzulegen, wenn die aufgerufene Funktion ihn nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="75140-136">When you compile a shader and not an effect file, **D3DX11CreateAsyncCompilerProcessor** ignores *Flags2*; we recommend that you set *Flags2* to zero because it is good programming practice to set a nonpointer parameter to zero if the called function will not use it.</span></span>

</dd> <dt>

<span data-ttu-id="75140-137">*ppcompiledshader* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="75140-137">*ppCompiledShader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75140-138">Typ: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="75140-138">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="75140-139">Adresse eines Zeigers auf den kompilierten Effekt.</span><span class="sxs-lookup"><span data-stu-id="75140-139">Address of a pointer to the compiled effect.</span></span>

</dd> <dt>

<span data-ttu-id="75140-140">*pperrorbuffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="75140-140">*ppErrorBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75140-141">Typ: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="75140-141">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="75140-142">Adresse eines Zeigers auf Kompilierungsfehler.</span><span class="sxs-lookup"><span data-stu-id="75140-142">Address of a pointer to compile errors.</span></span>

</dd> <dt>

<span data-ttu-id="75140-143">*ppdataprocessor* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="75140-143">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75140-144">Typ: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="75140-144">Type: **[**ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***</span></span>

<span data-ttu-id="75140-145">Adresse eines Zeigers auf einen Puffer, der den erstellten Datenprozessor enthält (siehe [**ID3DX11DataProcessor-Schnittstelle**](id3dx11dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="75140-145">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX11DataProcessor Interface**](id3dx11dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75140-146">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="75140-146">Return value</span></span>

<span data-ttu-id="75140-147">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="75140-147">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="75140-148">Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="75140-148">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="75140-149">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="75140-149">Remarks</span></span>

<span data-ttu-id="75140-150">Es gibt keine Implementierung des Async-Lade Moduls außerhalb von D3DX 10 und D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="75140-150">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="75140-151">Für Windows Store-Apps enthalten die DirectX-Beispiele (z. b. das [Direct3D-tutorialbeispiel](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) das **basicloader** -Modul, das das asynchrone Programmiermodell ([**asyncbase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))) Windows-Runtime verwendet.</span><span class="sxs-lookup"><span data-stu-id="75140-151">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="75140-152">Für Win32-Desktop-Apps können Sie den [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) verwenden, um etwas ähnliches wie das Windows-Runtime asynchrone Programmiermodell zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="75140-152">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="75140-153">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="75140-153">Requirements</span></span>



| <span data-ttu-id="75140-154">Anforderung</span><span class="sxs-lookup"><span data-stu-id="75140-154">Requirement</span></span> | <span data-ttu-id="75140-155">Wert</span><span class="sxs-lookup"><span data-stu-id="75140-155">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="75140-156">Header</span><span class="sxs-lookup"><span data-stu-id="75140-156">Header</span></span><br/>  | <dl> <span data-ttu-id="75140-157"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="75140-157"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="75140-158">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="75140-158">Library</span></span><br/> | <dl> <span data-ttu-id="75140-159"><dt>Bibliothek d3dx11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="75140-159"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="75140-160">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="75140-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75140-161">D3DX-Funktionen</span><span class="sxs-lookup"><span data-stu-id="75140-161">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

