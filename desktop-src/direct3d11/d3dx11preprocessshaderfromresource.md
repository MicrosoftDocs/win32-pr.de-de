---
title: D3DX11PreprocessShaderFromResource-Funktion (D3DX11async. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Beachten Sie, dass Sie die D3DPreprocess-API verwenden, anstatt diese Funktion zu verwenden. Erstellen Sie einen Shader aus einer Ressource, ohne ihn zu kompilieren.
ms.assetid: 13362ad6-f02e-4899-8962-4f7d4750ff69
keywords:
- D3DX11PreprocessShaderFromResource-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11PreprocessShaderFromResource
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 645d872e983cabbcd81aab05a59ee8f1f83cc403
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995986"
---
# <a name="d3dx11preprocessshaderfromresource-function"></a><span data-ttu-id="dc8da-106">D3DX11PreprocessShaderFromResource-Funktion</span><span class="sxs-lookup"><span data-stu-id="dc8da-106">D3DX11PreprocessShaderFromResource function</span></span>

> [!Note]  
> <span data-ttu-id="dc8da-107">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dc8da-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="dc8da-108">Anstatt diese Funktion zu verwenden, empfiehlt es sich, die [**D3DPreprocess**](/windows/desktop/direct3dhlsl/d3dpreprocess) -API zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="dc8da-108">Instead of using this function, we recommend that you use the [**D3DPreprocess**](/windows/desktop/direct3dhlsl/d3dpreprocess) API.</span></span>

 

<span data-ttu-id="dc8da-109">Erstellen Sie einen Shader aus einer Ressource, ohne ihn zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="dc8da-109">Create a shader from a resource without compiling it.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc8da-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc8da-110">Syntax</span></span>


```C++
HRESULT D3DX11PreprocessShaderFromResource(
  _In_        HMODULE            hModule,
  _In_        LPCTSTR            pResourceName,
  _In_        LPCTSTR            pSrcFileName,
  _In_  const D3D11_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX11ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="dc8da-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc8da-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc8da-112">*HMODULE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc8da-112">*hModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc8da-113">Typ: **[ **HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="dc8da-113">Type: **[**HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="dc8da-114">Handle für das Ressourcen Modul, das den Shader enthält.</span><span class="sxs-lookup"><span data-stu-id="dc8da-114">Handle to the resource module containing the shader.</span></span> <span data-ttu-id="dc8da-115">HMODULE kann mit der [GetModuleHandle-Funktion](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="dc8da-115">HMODULE can be obtained with [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="dc8da-116">*presourcename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc8da-116">*pResourceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc8da-117">Typ: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="dc8da-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="dc8da-118">Der Name der Ressource in Side HMODULE, die den Shader enthält.</span><span class="sxs-lookup"><span data-stu-id="dc8da-118">The name of the resource in side hModule containing the shader.</span></span> <span data-ttu-id="dc8da-119">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="dc8da-119">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="dc8da-120">Andernfalls wird der Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="dc8da-120">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="dc8da-121">*psrcfilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc8da-121">*pSrcFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc8da-122">Typ: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="dc8da-122">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="dc8da-123">Optional.</span><span class="sxs-lookup"><span data-stu-id="dc8da-123">Optional.</span></span> <span data-ttu-id="dc8da-124">Der Effekt Dateiname, der nur für Fehlermeldungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dc8da-124">Effect file name, which is used for error messages only.</span></span> <span data-ttu-id="dc8da-125">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="dc8da-125">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="dc8da-126">*pdefinitionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc8da-126">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc8da-127">Type: **Konstanten D3D11 \_ Shader- \_ Makro \***</span><span class="sxs-lookup"><span data-stu-id="dc8da-127">Type: **const D3D11\_SHADER\_MACRO\***</span></span>

<span data-ttu-id="dc8da-128">Ein mit Null endendes Array von Shader-Makros. Legen Sie diese Einstellung auf **null** fest, um keine Makros anzugeben.</span><span class="sxs-lookup"><span data-stu-id="dc8da-128">A NULL-terminated array of shader macros; set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="dc8da-129">*pinclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc8da-129">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc8da-130">Typ: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="dc8da-130">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="dc8da-131">Ein Zeiger auf eine include-Schnittstelle. Legen Sie dies auf **null** fest, um anzugeben, dass keine Includedatei vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="dc8da-131">A pointer to an include interface; set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="dc8da-132">*ppump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc8da-132">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc8da-133">Typ: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="dc8da-133">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="dc8da-134">Ein Zeiger auf eine Thread-Pump Schnittstelle (siehe [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="dc8da-134">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="dc8da-135">Verwenden Sie **null** , um anzugeben, dass diese Funktion erst zurückgegeben werden soll, wenn Sie abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="dc8da-135">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="dc8da-136">*ppshadertext* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="dc8da-136">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc8da-137">Typ: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="dc8da-137">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="dc8da-138">Ein Zeiger auf den Arbeitsspeicher, der den nicht kompilierten Shader enthält.</span><span class="sxs-lookup"><span data-stu-id="dc8da-138">A pointer to memory that contains the uncompiled shader.</span></span>

</dd> <dt>

<span data-ttu-id="dc8da-139">*pperrormsgs* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="dc8da-139">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc8da-140">Typ: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="dc8da-140">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="dc8da-141">Die Adresse eines Zeigers auf den Arbeitsspeicher, der Fehler bei der Fehler Erstellung enthält (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="dc8da-141">The address of a pointer to memory that contains effect-creation errors, if any occurred.</span></span>

</dd> <dt>

<span data-ttu-id="dc8da-142">*phresult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="dc8da-142">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc8da-143">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="dc8da-143">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="dc8da-144">Ein Zeiger auf den Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="dc8da-144">A pointer to the return value.</span></span> <span data-ttu-id="dc8da-145">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="dc8da-145">May be **NULL**.</span></span> <span data-ttu-id="dc8da-146">Wenn *ppump* nicht **null** ist, muss *phresult* eine gültige Speicheradresse sein, bis die asynchrone Ausführung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="dc8da-146">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc8da-147">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dc8da-147">Return value</span></span>

<span data-ttu-id="dc8da-148">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dc8da-148">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dc8da-149">Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="dc8da-149">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dc8da-150">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="dc8da-150">Requirements</span></span>



| <span data-ttu-id="dc8da-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dc8da-151">Requirement</span></span> | <span data-ttu-id="dc8da-152">Wert</span><span class="sxs-lookup"><span data-stu-id="dc8da-152">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc8da-153">Header</span><span class="sxs-lookup"><span data-stu-id="dc8da-153">Header</span></span><br/>  | <dl> <span data-ttu-id="dc8da-154"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc8da-154"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="dc8da-155">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dc8da-155">Library</span></span><br/> | <dl> <span data-ttu-id="dc8da-156"><dt>Bibliothek d3dx11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dc8da-156"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="dc8da-157">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="dc8da-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc8da-158">D3DX-Funktionen</span><span class="sxs-lookup"><span data-stu-id="dc8da-158">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

