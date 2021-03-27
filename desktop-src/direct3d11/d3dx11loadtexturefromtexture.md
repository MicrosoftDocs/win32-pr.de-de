---
title: D3DX11LoadTextureFromTexture-Funktion (D3DX11tex. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Beachten Sie anstelle dieser Funktion, dass Sie die directxtex-Bibliothek verwenden, die Größe, die Konvertierung, die Komprimierung, die Dekomprimierung und/oder das copyrechteck. Lädt eine Textur aus einer Textur.
ms.assetid: 4e673f73-531d-4df8-8542-798e4e70c481
keywords:
- D3DX11LoadTextureFromTexture-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11LoadTextureFromTexture
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 246429433dea11fddfd4396f3e59677877081592
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982323"
---
# <a name="d3dx11loadtexturefromtexture-function"></a><span data-ttu-id="b280d-106">D3DX11LoadTextureFromTexture-Funktion</span><span class="sxs-lookup"><span data-stu-id="b280d-106">D3DX11LoadTextureFromTexture function</span></span>

> [!Note]  
> <span data-ttu-id="b280d-107">Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b280d-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

> [!Note]  
> <span data-ttu-id="b280d-108">Anstatt diese Funktion zu verwenden, empfiehlt es sich, die [directxtex](https://github.com/Microsoft/DirectXTex) -Bibliothek zu verwenden, die **Größe zu ändern**, zu **konvertieren**, zu **komprimieren**, zu **dekomprimieren** und/oder **copyrechteck**.</span><span class="sxs-lookup"><span data-stu-id="b280d-108">Instead of using this function, we recommend that you use the [DirectXTex](https://github.com/Microsoft/DirectXTex) library, **Resize**, **Convert**, **Compress**, **Decompress**, and/or **CopyRectangle**.</span></span>

 

<span data-ttu-id="b280d-109">Lädt eine Textur aus einer Textur.</span><span class="sxs-lookup"><span data-stu-id="b280d-109">Load a texture from a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="b280d-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="b280d-110">Syntax</span></span>


```C++
HRESULT D3DX11LoadTextureFromTexture(
   ID3D11DeviceContext      *pContext,
   ID3D11Resource           *pSrcTexture,
   D3DX11_TEXTURE_LOAD_INFO *pLoadInfo,
   ID3D11Resource           *pDstTexture
);
```



## <a name="parameters"></a><span data-ttu-id="b280d-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b280d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b280d-112">*pContext*</span><span class="sxs-lookup"><span data-stu-id="b280d-112">*pContext*</span></span> 
</dt> <dd>

<span data-ttu-id="b280d-113">Typ: **[ **Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="b280d-113">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="b280d-114">Ein Zeiger auf ein [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="b280d-114">A pointer to an [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>

</dd> <dt>

<span data-ttu-id="b280d-115">*psrctexture*</span><span class="sxs-lookup"><span data-stu-id="b280d-115">*pSrcTexture*</span></span> 
</dt> <dd>

<span data-ttu-id="b280d-116">Typ: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span><span class="sxs-lookup"><span data-stu-id="b280d-116">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span></span>

<span data-ttu-id="b280d-117">Ein Zeiger auf die Quell Textur.</span><span class="sxs-lookup"><span data-stu-id="b280d-117">Pointer to the source texture.</span></span> <span data-ttu-id="b280d-118">Siehe [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span><span class="sxs-lookup"><span data-stu-id="b280d-118">See [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span></span>

</dd> <dt>

<span data-ttu-id="b280d-119">*ploadinfo*</span><span class="sxs-lookup"><span data-stu-id="b280d-119">*pLoadInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="b280d-120">Type: **[ **Bibliothek d3dx11 \_ Texture \_ Load \_ Info**](d3dx11-texture-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="b280d-120">Type: **[**D3DX11\_TEXTURE\_LOAD\_INFO**](d3dx11-texture-load-info.md)\***</span></span>

<span data-ttu-id="b280d-121">Zeiger auf Textur Lade Parameter.</span><span class="sxs-lookup"><span data-stu-id="b280d-121">Pointer to texture loading parameters.</span></span> <span data-ttu-id="b280d-122">Weitere Informationen finden Sie unter [**Bibliothek d3dx11 \_ Texture \_ Load \_ Info**](d3dx11-texture-load-info.md).</span><span class="sxs-lookup"><span data-stu-id="b280d-122">See [**D3DX11\_TEXTURE\_LOAD\_INFO**](d3dx11-texture-load-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="b280d-123">*pdsttexture*</span><span class="sxs-lookup"><span data-stu-id="b280d-123">*pDstTexture*</span></span> 
</dt> <dd>

<span data-ttu-id="b280d-124">Typ: **[ **ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span><span class="sxs-lookup"><span data-stu-id="b280d-124">Type: **[**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource)\***</span></span>

<span data-ttu-id="b280d-125">Ein Zeiger auf die Ziel Textur.</span><span class="sxs-lookup"><span data-stu-id="b280d-125">Pointer to the destination texture.</span></span> <span data-ttu-id="b280d-126">Siehe [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span><span class="sxs-lookup"><span data-stu-id="b280d-126">See [**ID3D11Resource**](/windows/desktop/api/D3D11/nn-d3d11-id3d11resource).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b280d-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b280d-127">Return value</span></span>

<span data-ttu-id="b280d-128">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b280d-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b280d-129">Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="b280d-129">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b280d-130">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="b280d-130">Requirements</span></span>



| <span data-ttu-id="b280d-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b280d-131">Requirement</span></span> | <span data-ttu-id="b280d-132">Wert</span><span class="sxs-lookup"><span data-stu-id="b280d-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b280d-133">Header</span><span class="sxs-lookup"><span data-stu-id="b280d-133">Header</span></span><br/>  | <dl> <span data-ttu-id="b280d-134"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="b280d-134"><dt>D3DX11tex.h</dt></span></span> </dl> |
| <span data-ttu-id="b280d-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b280d-135">Library</span></span><br/> | <dl> <span data-ttu-id="b280d-136"><dt>Bibliothek d3dx11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b280d-136"><dt>D3DX11.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b280d-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b280d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b280d-138">D3DX-Funktionen</span><span class="sxs-lookup"><span data-stu-id="b280d-138">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

 





