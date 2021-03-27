---
title: D3DX11SaveTextureToMemory-Funktion (D3DX11tex. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Beachten Sie anstelle dieser Funktion, dass Sie die directxtex-Bibliothek, capturetexture und savetoxxxmemory (xxx ist WIC, DDS oder TGA) verwenden. Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele). Speichert eine Textur im Speicher.
ms.assetid: 3b54d8e1-6474-48fd-8348-a3baac406101
keywords:
- D3DX11SaveTextureToMemory-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11SaveTextureToMemory
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4718f32f8d8288f83b30e3d742ebbe619421dc48
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219626"
---
# <a name="d3dx11savetexturetomemory-function"></a><span data-ttu-id="e2c8a-106">D3DX11SaveTextureToMemory-Funktion</span><span class="sxs-lookup"><span data-stu-id="e2c8a-106">D3DX11SaveTextureToMemory function</span></span>

> [!Note]  
> <span data-ttu-id="e2c8a-107">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e2c8a-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="e2c8a-108">Anstatt diese Funktion zu verwenden, empfiehlt es sich, dass Sie die [directxtex](https://github.com/Microsoft/DirectXTex) -Bibliothek **capturetexture** , dann **savetoxxxmemory** (xxx ist WIC, DDS oder TGA) verwenden. Die WIC unterstützt DDS und TGA nicht. D3DX 9 unterstützte TGA als gängiges Kunst Quellformat für Spiele).</span><span class="sxs-lookup"><span data-stu-id="e2c8a-108">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **CaptureTexture** then **SaveToXXXMemory** (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>

 

<span data-ttu-id="e2c8a-109">Speichert eine Textur im Speicher.</span><span class="sxs-lookup"><span data-stu-id="e2c8a-109">Save a texture to memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2c8a-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2c8a-110">Syntax</span></span>


```C++
HRESULT D3DX11SaveTextureToMemory(
        ID3D11DeviceContext      *pContext,
  _In_  ID3D11Resource           *pSrcTexture,
  _In_  D3DX11_IMAGE_FILE_FORMAT DestFormat,
  _Out_ LPD3D10BLOB              *ppDestBuf,
  _In_  UINT                     Flags
);
```



## <a name="parameters"></a><span data-ttu-id="e2c8a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2c8a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2c8a-112">*pContext*</span><span class="sxs-lookup"><span data-stu-id="e2c8a-112">*pContext*</span></span> 
</dt> <dd>

<span data-ttu-id="e2c8a-113">Typ: **[ **Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="e2c8a-113">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="e2c8a-114">Ein Zeiger auf ein [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="e2c8a-114">A pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>

</dd> <dt>

<span data-ttu-id="e2c8a-115">*psrctexture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2c8a-115">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2c8a-116">Typ: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span><span class="sxs-lookup"><span data-stu-id="e2c8a-116">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span></span>

<span data-ttu-id="e2c8a-117">Zeiger auf die zu speichernde Textur.</span><span class="sxs-lookup"><span data-stu-id="e2c8a-117">Pointer to the texture to be saved.</span></span> <span data-ttu-id="e2c8a-118">Siehe [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span><span class="sxs-lookup"><span data-stu-id="e2c8a-118">See [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span></span>

</dd> <dt>

<span data-ttu-id="e2c8a-119">*Destformat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e2c8a-119">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2c8a-120">Type: **[ **Bibliothek d3dx11 \_ Image \_ file \_ Format**](d3dx11-image-file-format.md)**</span><span class="sxs-lookup"><span data-stu-id="e2c8a-120">Type: **[**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md)**</span></span>

<span data-ttu-id="e2c8a-121">Das Format, in dem die Textur gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="e2c8a-121">The format the texture will be saved as.</span></span> <span data-ttu-id="e2c8a-122">Siehe [**Bibliothek d3dx11 \_ Image \_ file \_ Format**](d3dx11-image-file-format.md).</span><span class="sxs-lookup"><span data-stu-id="e2c8a-122">See [**D3DX11\_IMAGE\_FILE\_FORMAT**](d3dx11-image-file-format.md).</span></span>

</dd> <dt>

<span data-ttu-id="e2c8a-123">*ppdestbuf* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e2c8a-123">*ppDestBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2c8a-124">Typ: **[ **LPD3D10BLOB**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\***</span><span class="sxs-lookup"><span data-stu-id="e2c8a-124">Type: **[**LPD3D10BLOB**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob)\***</span></span>

<span data-ttu-id="e2c8a-125">Adresse eines Zeigers auf den Speicher, der die gespeicherte Textur enthält.</span><span class="sxs-lookup"><span data-stu-id="e2c8a-125">Address of a pointer to the memory containing the saved texture.</span></span>

</dd> <dt>

<span data-ttu-id="e2c8a-126">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="e2c8a-126">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2c8a-127">Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e2c8a-127">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e2c8a-128">Optional.</span><span class="sxs-lookup"><span data-stu-id="e2c8a-128">Optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2c8a-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2c8a-129">Return value</span></span>

<span data-ttu-id="e2c8a-130">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e2c8a-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e2c8a-131">Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="e2c8a-131">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e2c8a-132">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="e2c8a-132">Requirements</span></span>



| <span data-ttu-id="e2c8a-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2c8a-133">Requirement</span></span> | <span data-ttu-id="e2c8a-134">Wert</span><span class="sxs-lookup"><span data-stu-id="e2c8a-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2c8a-135">Header</span><span class="sxs-lookup"><span data-stu-id="e2c8a-135">Header</span></span><br/>  | <dl> <span data-ttu-id="e2c8a-136"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2c8a-136"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="e2c8a-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e2c8a-137">Library</span></span><br/> | <dl> <span data-ttu-id="e2c8a-138"><dt>Bibliothek d3dx11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e2c8a-138"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e2c8a-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e2c8a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2c8a-140">D3DX-Funktionen</span><span class="sxs-lookup"><span data-stu-id="e2c8a-140">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

