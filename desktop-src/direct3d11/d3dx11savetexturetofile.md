---
title: D3DX11SaveTextureToFile-Funktion (D3DX11tex. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Beachten Sie anstelle dieser Funktion, dass Sie die directxtex-Bibliothek, capturetexture und savetoxxxfile (mit XXX ist WIC, DDS oder TGA) verwenden. Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele). Für das vereinfachte Szenario der Erstellung eines Screenshots aus einer renderzieltextur empfiehlt es sich, die directxtk-Bibliothek "saveddstexturedefile" oder "savewictexturedefile" zu verwenden. Speichert eine Textur in einer Datei.
ms.assetid: da161268-fb68-42dd-ba31-b090a993f369
keywords:
- D3DX11SaveTextureToFile-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11SaveTextureToFile
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d87188c3e58a8bea36b1cffb675c229aed71677
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982317"
---
# <a name="d3dx11savetexturetofile-function"></a><span data-ttu-id="11682-107">D3DX11SaveTextureToFile-Funktion</span><span class="sxs-lookup"><span data-stu-id="11682-107">D3DX11SaveTextureToFile function</span></span>

> [!Note]  
> <span data-ttu-id="11682-108">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="11682-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="11682-109">Anstatt diese Funktion zu verwenden, empfiehlt es sich, dass Sie die [directxtex](https://github.com/Microsoft/DirectXTex) -Bibliothek **capturetexture** und **savetoxxxfile** verwenden (wobei xxx gleich WIC, DDS oder TGA ist). Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele).</span><span class="sxs-lookup"><span data-stu-id="11682-109">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **CaptureTexture** then **SaveToXXXFile** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span> <span data-ttu-id="11682-110">Für das vereinfachte Szenario der Erstellung eines Screenshots aus einer renderzieltextur empfiehlt es sich, die [directxtk](https://github.com/Microsoft/DirectXTK) -Bibliothek " **saveddstexturedefile** " oder " **savewictexturedefile**" zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="11682-110">For the simplified scenario of creating a screen shot from a render target texture, we recommend that you use the [DirectXTK](https://github.com/Microsoft/DirectXTK) library, **SaveDDSTextureToFile** or **SaveWICTextureToFile**.</span></span>

 

<span data-ttu-id="11682-111">Speichert eine Textur in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="11682-111">Save a texture to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="11682-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="11682-112">Syntax</span></span>


```C++
HRESULT D3DX11SaveTextureToFile(
       ID3D11DeviceContext      *pContext,
  _In_ ID3D11Resource           *pSrcTexture,
  _In_ D3DX11_IMAGE_FILE_FORMAT DestFormat,
  _In_ LPCTSTR                  pDestFile
);
```



## <a name="parameters"></a><span data-ttu-id="11682-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="11682-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11682-114">*pContext*</span><span class="sxs-lookup"><span data-stu-id="11682-114">*pContext*</span></span> 
</dt> <dd>

<span data-ttu-id="11682-115">Typ: **[ **Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="11682-115">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="11682-116">Ein Zeiger auf ein [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="11682-116">A pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>

</dd> <dt>

<span data-ttu-id="11682-117">*psrctexture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11682-117">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11682-118">Typ: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span><span class="sxs-lookup"><span data-stu-id="11682-118">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span></span>

<span data-ttu-id="11682-119">Zeiger auf die zu speichernde Textur.</span><span class="sxs-lookup"><span data-stu-id="11682-119">Pointer to the texture to be saved.</span></span> <span data-ttu-id="11682-120">Siehe [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span><span class="sxs-lookup"><span data-stu-id="11682-120">See [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span></span>

</dd> <dt>

<span data-ttu-id="11682-121">*Destformat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11682-121">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11682-122">Type: **[ **Bibliothek d3dx11 \_ Image \_ file \_ Format**](d3dx11-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="11682-122">Type: **[**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md)**</span></span>

<span data-ttu-id="11682-123">Das Format, in dem die Textur gespeichert wird (siehe [**Bibliothek d3dx11 \_ Image \_ file \_ Format**](d3dx11-image-file-format.md)).</span><span class="sxs-lookup"><span data-stu-id="11682-123">The format the texture will be saved as (see [**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md)).</span></span> <span data-ttu-id="11682-124">Bibliothek d3dx11 \_ IFF \_ DDS ist das bevorzugte Format, da es die einzige Option ist, die alle Formate im [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="11682-124">D3DX11\_IFF\_DDS is the preferred format since it is the only option that supports all the formats in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

</dd> <dt>

<span data-ttu-id="11682-125">*pdestfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11682-125">*pDestFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11682-126">Typ: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="11682-126">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="11682-127">Der Name der Ziel Ausgabedatei, in der die Textur gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="11682-127">Name of the destination output file where the texture will be saved.</span></span> <span data-ttu-id="11682-128">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="11682-128">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="11682-129">Andernfalls wird der Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="11682-129">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11682-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="11682-130">Return value</span></span>

<span data-ttu-id="11682-131">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="11682-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="11682-132">Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind. Verwenden Sie den Rückgabewert, um festzustellen, ob *destformat* unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="11682-132">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md); use the return value to see if the *DestFormat* is supported.</span></span>

## <a name="remarks"></a><span data-ttu-id="11682-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="11682-133">Remarks</span></span>

<span data-ttu-id="11682-134">**D3DX11SaveTextureToFile** schreibt die zusätzliche [**DDS- \_ Header \_ DXT10**](/windows/desktop/direct3ddds/dds-header-dxt10) -Struktur nur bei Bedarf für die Eingabe Textur (z. b. weil die Eingabe Textur im Standard-RGB-Format (sRGB) vorliegt).</span><span class="sxs-lookup"><span data-stu-id="11682-134">**D3DX11SaveTextureToFile** writes out the extra [**DDS\_HEADER\_DXT10**](/windows/desktop/direct3ddds/dds-header-dxt10) structure for the input texture only if necessary (for example, because the input texture is in standard RGB (sRGB) format).</span></span> <span data-ttu-id="11682-135">Wenn **D3DX11SaveTextureToFile** die **DDS- \_ Header \_ DXT10** -Struktur ausgibt, wird der **dwfourcc** -Member der [**DDS- \_ Pixel Format**](/windows/desktop/direct3ddds/dds-pixelformat) -Struktur für die Textur auf **DX10** festgelegt, um die präscense des **DDS- \_ Headers \_ DXT10** Extended-Header anzugeben.</span><span class="sxs-lookup"><span data-stu-id="11682-135">If **D3DX11SaveTextureToFile** writes out the **DDS\_HEADER\_DXT10** structure, it sets the **dwFourCC** member of the [**DDS\_PIXELFORMAT**](/windows/desktop/direct3ddds/dds-pixelformat) structure for the texture to **DX10** to indicate the prescense of the **DDS\_HEADER\_DXT10** extended header.</span></span>

## <a name="requirements"></a><span data-ttu-id="11682-136">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="11682-136">Requirements</span></span>



| <span data-ttu-id="11682-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11682-137">Requirement</span></span> | <span data-ttu-id="11682-138">Wert</span><span class="sxs-lookup"><span data-stu-id="11682-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="11682-139">Header</span><span class="sxs-lookup"><span data-stu-id="11682-139">Header</span></span><br/>  | <dl> <span data-ttu-id="11682-140"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="11682-140"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="11682-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="11682-141">Library</span></span><br/> | <dl> <span data-ttu-id="11682-142"><dt>Bibliothek d3dx11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11682-142"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="11682-143">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="11682-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11682-144">D3DX-Funktionen</span><span class="sxs-lookup"><span data-stu-id="11682-144">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

