---
description: Speichert eine Textur in einer Bilddatei.
ms.assetid: 8dcfd58a-ae1e-43c3-8ff1-94e3fa398b0f
title: D3DXSaveTextureToFileInMemory-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveTextureToFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c58da1663abc5295e8ce17c500bd46d6c365a2d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132329"
---
# <a name="d3dxsavetexturetofileinmemory-function"></a><span data-ttu-id="68875-103">D3DXSaveTextureToFileInMemory-Funktion</span><span class="sxs-lookup"><span data-stu-id="68875-103">D3DXSaveTextureToFileInMemory function</span></span>

<span data-ttu-id="68875-104">Speichert eine Textur in einer Bilddatei.</span><span class="sxs-lookup"><span data-stu-id="68875-104">Saves a texture to an image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="68875-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="68875-105">Syntax</span></span>


```C++
HRESULT D3DXSaveTextureToFileInMemory(
  _Out_       LPD3DXBUFFER           *ppDestBuf,
  _In_        D3DXIMAGE_FILEFORMAT   DestFormat,
  _In_        LPDIRECT3DBASETEXTURE9 pSrcTexture,
  _In_  const PALETTEENTRY           *pSrcPalette
);
```



## <a name="parameters"></a><span data-ttu-id="68875-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="68875-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68875-107">*ppdestbuf* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="68875-107">*ppDestBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68875-108">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="68875-108">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="68875-109">Adresse eines Zeigers auf eine [**ID3DXBuffer**](id3dxbuffer.md) , in der das Bild gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="68875-109">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) that will store the image.</span></span>

</dd> <dt>

<span data-ttu-id="68875-110">*Destformat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="68875-110">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68875-111">Type: **[ **D3DXIMAGE \_ File Format**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="68875-111">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

<span data-ttu-id="68875-112">[**D3DXIMAGE \_ Dateiformat**](./d3dximage-fileformat.md) , das das beim Speichern zu verwendende Dateiformat angibt.</span><span class="sxs-lookup"><span data-stu-id="68875-112">[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md) specifying the file format to use when saving.</span></span> <span data-ttu-id="68875-113">Diese Funktion unterstützt das Speichern in allen **D3DXIMAGE \_ File Format** -Formaten außer Portable pixmap (. ppm) und TARGA/Truevision Graphics Adapter (. TGA).</span><span class="sxs-lookup"><span data-stu-id="68875-113">This function supports saving to all **D3DXIMAGE\_FILEFORMAT** formats except Portable Pixmap (.ppm) and Targa/Truevision Graphics Adapter (.tga).</span></span>

</dd> <dt>

<span data-ttu-id="68875-114">*psrctexture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="68875-114">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68875-115">Typ: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span><span class="sxs-lookup"><span data-stu-id="68875-115">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span></span>

<span data-ttu-id="68875-116">Zeiger auf die [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) -Schnittstelle, die das zu speichernde Bild enthält.</span><span class="sxs-lookup"><span data-stu-id="68875-116">Pointer to [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) interface containing the image to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="68875-117">*psrcpalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="68875-117">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68875-118">Typ: **Konstanten [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="68875-118">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="68875-119">Ein Zeiger auf eine [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) -Struktur, die eine Palette von 256 Farben enthält.</span><span class="sxs-lookup"><span data-stu-id="68875-119">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure containing a palette of 256 colors.</span></span> <span data-ttu-id="68875-120">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="68875-120">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68875-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="68875-121">Return value</span></span>

<span data-ttu-id="68875-122">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="68875-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="68875-123">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="68875-123">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="68875-124">Wenn die Funktion fehlschlägt, kann der Rückgabewert wie folgt lauten: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="68875-124">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="68875-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="68875-125">Remarks</span></span>

<span data-ttu-id="68875-126">Diese Funktion übernimmt die Konvertierung in und aus komprimierten Textur Formaten.</span><span class="sxs-lookup"><span data-stu-id="68875-126">This function handles conversion to and from compressed texture formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="68875-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68875-127">Requirements</span></span>



| <span data-ttu-id="68875-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="68875-128">Requirement</span></span> | <span data-ttu-id="68875-129">Wert</span><span class="sxs-lookup"><span data-stu-id="68875-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="68875-130">Header</span><span class="sxs-lookup"><span data-stu-id="68875-130">Header</span></span><br/>  | <dl> <span data-ttu-id="68875-131"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="68875-131"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="68875-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="68875-132">Library</span></span><br/> | <dl> <span data-ttu-id="68875-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="68875-133"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="68875-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68875-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68875-135">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="68875-135">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="68875-136">**D3DXSaveSurfaceToFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="68875-136">**D3DXSaveSurfaceToFileInMemory**</span></span>](d3dxsavesurfacetofileinmemory.md)
</dt> <dt>

[<span data-ttu-id="68875-137">**D3DXSaveVolumeToFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="68875-137">**D3DXSaveVolumeToFileInMemory**</span></span>](d3dxsavevolumetofileinmemory.md)
</dt> </dl>

 

 
