---
title: D3DX11PreprocessShaderFromMemory-Funktion (D3DX11async. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Beachten Sie, dass Sie die D3DPreprocess-API verwenden, anstatt diese Funktion zu verwenden. Erstellen Sie einen Shader aus dem Arbeitsspeicher, ohne ihn zu kompilieren.
ms.assetid: 3c646914-9334-44fe-a8a0-b84d0dc1a16e
keywords:
- D3DX11PreprocessShaderFromMemory-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11PreprocessShaderFromMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71a94633270fe0f4e462e60915de862be8693daa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995991"
---
# <a name="d3dx11preprocessshaderfrommemory-function"></a><span data-ttu-id="58934-106">D3DX11PreprocessShaderFromMemory-Funktion</span><span class="sxs-lookup"><span data-stu-id="58934-106">D3DX11PreprocessShaderFromMemory function</span></span>

> [!Note]  
> <span data-ttu-id="58934-107">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="58934-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="58934-108">Anstatt diese Funktion zu verwenden, empfiehlt es sich, die [**D3DPreprocess**](/windows/desktop/direct3dhlsl/d3dpreprocess) -API zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="58934-108">Instead of using this function, we recommend that you use the [**D3DPreprocess**](/windows/desktop/direct3dhlsl/d3dpreprocess) API.</span></span>

 

<span data-ttu-id="58934-109">Erstellen Sie einen Shader aus dem Arbeitsspeicher, ohne ihn zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="58934-109">Create a shader from memory without compiling it.</span></span>

## <a name="syntax"></a><span data-ttu-id="58934-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="58934-110">Syntax</span></span>


```C++
HRESULT D3DX11PreprocessShaderFromMemory(
  _In_        LPCSTR             pSrcData,
  _In_        SIZE_T             SrcDataSize,
  _In_        LPCSTR             pFileName,
  _In_  const D3D11_SHADER_MACRO *pDefines,
  _In_        LPD3D10INCLUDE     pInclude,
  _In_        ID3DX11ThreadPump  *pPump,
  _Out_       ID3D10Blob         **ppShaderText,
  _Out_       ID3D10Blob         **ppErrorMsgs,
  _Out_       HRESULT            *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="58934-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="58934-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58934-112">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58934-112">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58934-113">Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="58934-113">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="58934-114">Zeiger auf den Arbeitsspeicher, der den Shader enthält.</span><span class="sxs-lookup"><span data-stu-id="58934-114">Pointer to the memory containing the shader.</span></span>

</dd> <dt>

<span data-ttu-id="58934-115">*Srcdatasize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58934-115">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58934-116">Typ: **[ **Größe \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="58934-116">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="58934-117">Größe des Shaders.</span><span class="sxs-lookup"><span data-stu-id="58934-117">Size of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="58934-118">*pfilename* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58934-118">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58934-119">Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="58934-119">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="58934-120">Der Name des Shaders.</span><span class="sxs-lookup"><span data-stu-id="58934-120">Name of the shader.</span></span>

</dd> <dt>

<span data-ttu-id="58934-121">*pdefinitionen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58934-121">*pDefines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58934-122">Type: **Konstanten D3D11 \_ Shader- \_ Makro \***</span><span class="sxs-lookup"><span data-stu-id="58934-122">Type: **const D3D11\_SHADER\_MACRO\***</span></span>

<span data-ttu-id="58934-123">Ein mit Null endendes Array von Shader-Makros. Legen Sie diese Einstellung auf **null** fest, um keine Makros anzugeben.</span><span class="sxs-lookup"><span data-stu-id="58934-123">A NULL-terminated array of shader macros; set this to **NULL** to specify no macros.</span></span>

</dd> <dt>

<span data-ttu-id="58934-124">*pinclude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58934-124">*pInclude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58934-125">Typ: **[ **LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="58934-125">Type: **[**LPD3D10INCLUDE**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))**</span></span>

<span data-ttu-id="58934-126">Ein Zeiger auf eine include-Schnittstelle. Legen Sie dies auf **null** fest, um anzugeben, dass keine Includedatei vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="58934-126">A pointer to an include interface; set this to **NULL** to specify there is no include file.</span></span>

</dd> <dt>

<span data-ttu-id="58934-127">*ppump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58934-127">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58934-128">Typ: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="58934-128">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="58934-129">Ein Zeiger auf eine Thread-Pump Schnittstelle (siehe [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="58934-129">A pointer to a thread pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="58934-130">Verwenden Sie **null** , um anzugeben, dass diese Funktion erst zurückgegeben werden soll, wenn Sie abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="58934-130">Use **NULL** to specify that this function should not return until it is completed.</span></span>

</dd> <dt>

<span data-ttu-id="58934-131">*ppshadertext* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="58934-131">*ppShaderText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58934-132">Typ: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="58934-132">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="58934-133">Ein Zeiger auf den Arbeitsspeicher, der den nicht kompilierten Shader enthält.</span><span class="sxs-lookup"><span data-stu-id="58934-133">A pointer to memory that contains the uncompiled shader.</span></span>

</dd> <dt>

<span data-ttu-id="58934-134">*pperrormsgs* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="58934-134">*ppErrorMsgs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58934-135">Typ: **[ **ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="58934-135">Type: **[**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="58934-136">Die Adresse eines Zeigers auf den Arbeitsspeicher, der Fehler bei der Fehler Erstellung enthält (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="58934-136">The address of a pointer to memory that contains effect-creation errors, if any occurred.</span></span>

</dd> <dt>

<span data-ttu-id="58934-137">*phresult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="58934-137">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58934-138">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="58934-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="58934-139">Ein Zeiger auf den Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="58934-139">A pointer to the return value.</span></span> <span data-ttu-id="58934-140">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="58934-140">May be **NULL**.</span></span> <span data-ttu-id="58934-141">Wenn *ppump* nicht **null** ist, muss *phresult* eine gültige Speicheradresse sein, bis die asynchrone Ausführung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="58934-141">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58934-142">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="58934-142">Return value</span></span>

<span data-ttu-id="58934-143">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="58934-143">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="58934-144">Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="58934-144">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="58934-145">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="58934-145">Requirements</span></span>



| <span data-ttu-id="58934-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="58934-146">Requirement</span></span> | <span data-ttu-id="58934-147">Wert</span><span class="sxs-lookup"><span data-stu-id="58934-147">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="58934-148">Header</span><span class="sxs-lookup"><span data-stu-id="58934-148">Header</span></span><br/>  | <dl> <span data-ttu-id="58934-149"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="58934-149"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="58934-150">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="58934-150">Library</span></span><br/> | <dl> <span data-ttu-id="58934-151"><dt>Bibliothek d3dx11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="58934-151"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="58934-152">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="58934-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58934-153">D3DX-Funktionen</span><span class="sxs-lookup"><span data-stu-id="58934-153">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

