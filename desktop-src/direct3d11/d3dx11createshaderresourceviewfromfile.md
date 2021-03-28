---
title: D3DX11CreateShaderResourceViewFromFile-Funktion (D3DX11tex. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Beachten Sie anstelle dieser Funktion, dass Sie diese directxtk-Bibliothek (Runtime), die Datei "anatexxxtexturefromfile" (wobei xxx DDS oder WIC ist) directxtex Library (Tools), loadfromxxxfile (wobei xxx WIC, DDS oder TGA ist) verwenden. Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele), dann erstellt "anateshaderresourceview" eine Shader-Ressourcen Ansicht aus einer Datei.
ms.assetid: c6a23503-f511-49dc-a0dc-19932cf8f313
keywords:
- D3DX11CreateShaderResourceViewFromFile-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateShaderResourceViewFromFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05e7d710b0b379f3027591c2ff9e52c2fdd0d7a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355347"
---
# <a name="d3dx11createshaderresourceviewfromfile-function"></a><span data-ttu-id="e4082-105">D3DX11CreateShaderResourceViewFromFile-Funktion</span><span class="sxs-lookup"><span data-stu-id="e4082-105">D3DX11CreateShaderResourceViewFromFile function</span></span>

> [!Note]  
> <span data-ttu-id="e4082-106">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e4082-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="e4082-107">Anstatt diese Funktion zu verwenden, empfiehlt es sich, diese zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="e4082-107">Instead of using this function, we recommend that you use these:</span></span>
>
> -   <span data-ttu-id="e4082-108">[Directxtk](https://github.com/Microsoft/DirectXTK) -Bibliothek (Laufzeit), " **kreatexxxtexturefromfile** " (wobei xxx DDS oder WIC ist)</span><span class="sxs-lookup"><span data-stu-id="e4082-108">[DirectXTK](https://github.com/Microsoft/DirectXTK) library (runtime), **CreateXXXTextureFromFile** (where XXX is DDS or WIC)</span></span>
> -   <span data-ttu-id="e4082-109">[Directxtex](https://github.com/Microsoft/DirectXTex) -Bibliothek (Tools), **loadfromxxxfile** (hierbei ist xxx WIC, DDS oder TGA). Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele) und dann " **kreateshaderresourceview** "</span><span class="sxs-lookup"><span data-stu-id="e4082-109">[DirectXTex](https://github.com/Microsoft/DirectXTex) library (tools), **LoadFromXXXFile** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then **CreateShaderResourceView**</span></span>

 

<span data-ttu-id="e4082-110">Erstellen Sie eine Shader-Ressourcen Ansicht aus einer Datei.</span><span class="sxs-lookup"><span data-stu-id="e4082-110">Create a shader-resource view from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4082-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4082-111">Syntax</span></span>


```C++
HRESULT D3DX11CreateShaderResourceViewFromFile(
  _In_  ID3D11Device             *pDevice,
  _In_  LPCTSTR                  pSrcFile,
  _In_  D3DX11_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX11ThreadPump        *pPump,
  _Out_ ID3D11ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="e4082-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4082-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4082-113">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4082-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4082-114">Typ: **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span><span class="sxs-lookup"><span data-stu-id="e4082-114">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***</span></span>

<span data-ttu-id="e4082-115">Ein Zeiger auf das Gerät (siehe [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)), von dem die Ressource verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e4082-115">A pointer to the device (see [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="e4082-116">*psrcfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4082-116">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4082-117">Typ: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e4082-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e4082-118">Der Name der Datei, die die Shader-Ressourcen Ansicht enthält.</span><span class="sxs-lookup"><span data-stu-id="e4082-118">Name of the file that contains the shader-resource view.</span></span> <span data-ttu-id="e4082-119">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="e4082-119">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="e4082-120">Andernfalls wird der Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="e4082-120">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="e4082-121">*ploadinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4082-121">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4082-122">Type: **[ **Bibliothek d3dx11 \_ Image \_ Load \_ Info**](d3dx11-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="e4082-122">Type: **[**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)\***</span></span>

<span data-ttu-id="e4082-123">Optional.</span><span class="sxs-lookup"><span data-stu-id="e4082-123">Optional.</span></span> <span data-ttu-id="e4082-124">Gibt die Merkmale einer Textur an (siehe [**Bibliothek d3dx11 \_ Image \_ Load \_ Info**](d3dx11-image-load-info.md)), wenn der Datenprozessor erstellt wird. Legen Sie diese Einstellung auf **null** fest, um die Merkmale einer Textur beim Laden der Textur zu lesen.</span><span class="sxs-lookup"><span data-stu-id="e4082-124">Identifies the characteristics of a texture (see [**D3DX11\_IMAGE\_LOAD\_INFO**](d3dx11-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="e4082-125">*ppump* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e4082-125">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4082-126">Typ: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="e4082-126">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\***</span></span>

<span data-ttu-id="e4082-127">Zeiger auf eine Thread-Pump-Schnittstelle (siehe [**ID3DX11ThreadPump-Schnittstelle**](id3dx11threadpump.md)).</span><span class="sxs-lookup"><span data-stu-id="e4082-127">Pointer to a thread-pump interface (see [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md)).</span></span> <span data-ttu-id="e4082-128">Wenn **null** angegeben wird, verhält sich diese Funktion synchron und wird erst nach Abschluss des Vorgangs zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e4082-128">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="e4082-129">*ppshaderresourceview* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e4082-129">*ppShaderResourceView* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4082-130">Typ: **[ **ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="e4082-130">Type: **[**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)\*\***</span></span>

<span data-ttu-id="e4082-131">Adresse eines Zeigers auf die Shader-Ressourcen Ansicht (siehe [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)).</span><span class="sxs-lookup"><span data-stu-id="e4082-131">Address of a pointer to the shader-resource view (see [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)).</span></span>

</dd> <dt>

<span data-ttu-id="e4082-132">*phresult* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e4082-132">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4082-133">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="e4082-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="e4082-134">Ein Zeiger auf den Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="e4082-134">A pointer to the return value.</span></span> <span data-ttu-id="e4082-135">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="e4082-135">May be **NULL**.</span></span> <span data-ttu-id="e4082-136">Wenn *ppump* nicht **null** ist, muss *phresult* eine gültige Speicheradresse sein, bis die asynchrone Ausführung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="e4082-136">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4082-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e4082-137">Return value</span></span>

<span data-ttu-id="e4082-138">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e4082-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e4082-139">Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="e4082-139">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e4082-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e4082-140">Remarks</span></span>

<span data-ttu-id="e4082-141">Eine Liste der unterstützten Bildformate finden Sie unter [**Bibliothek d3dx11 \_ Image \_ file \_ Format**](d3dx11-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="e4082-141">For a list of supported image formats, see [**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e4082-142">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="e4082-142">Requirements</span></span>



| <span data-ttu-id="e4082-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e4082-143">Requirement</span></span> | <span data-ttu-id="e4082-144">Wert</span><span class="sxs-lookup"><span data-stu-id="e4082-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4082-145">Header</span><span class="sxs-lookup"><span data-stu-id="e4082-145">Header</span></span><br/>  | <dl> <span data-ttu-id="e4082-146"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4082-146"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="e4082-147">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e4082-147">Library</span></span><br/> | <dl> <span data-ttu-id="e4082-148"><dt>Bibliothek d3dx11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e4082-148"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e4082-149">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e4082-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4082-150">D3DX-Funktionen</span><span class="sxs-lookup"><span data-stu-id="e4082-150">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

