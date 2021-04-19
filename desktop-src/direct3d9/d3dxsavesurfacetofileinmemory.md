---
description: Speichert eine Oberfläche in einer Bilddatei.
ms.assetid: 6320e5ed-e43d-43bf-a746-5478df42941d
title: D3DXSaveSurfaceToFileInMemory-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveSurfaceToFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8e8bbdd447b7154e150b3469a4b12180252ed516
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366458"
---
# <a name="d3dxsavesurfacetofileinmemory-function"></a><span data-ttu-id="e0701-103">D3DXSaveSurfaceToFileInMemory-Funktion</span><span class="sxs-lookup"><span data-stu-id="e0701-103">D3DXSaveSurfaceToFileInMemory function</span></span>

<span data-ttu-id="e0701-104">Speichert eine Oberfläche in einer Bilddatei.</span><span class="sxs-lookup"><span data-stu-id="e0701-104">Saves a surface to an image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0701-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0701-105">Syntax</span></span>


```C++
HRESULT D3DXSaveSurfaceToFileInMemory(
  _Out_       LPD3DXBUFFER         *ppDestBuf,
  _In_        D3DXIMAGE_FILEFORMAT DestFormat,
  _In_        LPDIRECT3DSURFACE9   pSrcSurface,
  _In_  const PALETTEENTRY         *pSrcPalette,
  _In_  const RECT                 *pSrcRect
);
```



## <a name="parameters"></a><span data-ttu-id="e0701-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0701-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0701-107">*ppdestbuf* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e0701-107">*ppDestBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0701-108">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="e0701-108">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="e0701-109">Adresse eines Zeigers auf eine [**ID3DXBuffer**](id3dxbuffer.md) , in der das Bild gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="e0701-109">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) that will store the image.</span></span>

</dd> <dt>

<span data-ttu-id="e0701-110">*Destformat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e0701-110">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0701-111">Type: **[ **D3DXIMAGE \_ File Format**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="e0701-111">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

<span data-ttu-id="e0701-112">[**D3DXIMAGE \_ Dateiformat**](./d3dximage-fileformat.md) , das das beim Speichern zu verwendende Dateiformat angibt.</span><span class="sxs-lookup"><span data-stu-id="e0701-112">[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md) specifying the file format to use when saving.</span></span> <span data-ttu-id="e0701-113">Diese Funktion unterstützt das Speichern in allen **D3DXIMAGE \_ File Format** -Formaten außer Portable pixmap (. ppm) und TARGA/Truevision Graphics Adapter (. TGA).</span><span class="sxs-lookup"><span data-stu-id="e0701-113">This function supports saving to all **D3DXIMAGE\_FILEFORMAT** formats except Portable Pixmap (.ppm) and Targa/Truevision Graphics Adapter (.tga).</span></span>

</dd> <dt>

<span data-ttu-id="e0701-114">*psrcsurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e0701-114">*pSrcSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0701-115">Typ: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="e0701-115">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="e0701-116">Zeiger auf die [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) -Schnittstelle, die das zu speichernde Bild enthält.</span><span class="sxs-lookup"><span data-stu-id="e0701-116">Pointer to [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface containing the image to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="e0701-117">*psrcpalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e0701-117">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0701-118">Typ: **Konstanten [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="e0701-118">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="e0701-119">Ein Zeiger auf eine [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) -Struktur, die eine Palette von 256 Farben enthält.</span><span class="sxs-lookup"><span data-stu-id="e0701-119">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure containing a palette of 256 colors.</span></span> <span data-ttu-id="e0701-120">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="e0701-120">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e0701-121">*psrcrect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e0701-121">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0701-122">Typ: Konstante **[**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="e0701-122">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="e0701-123">Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="e0701-123">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="e0701-124">Gibt das Quell Rechteck an.</span><span class="sxs-lookup"><span data-stu-id="e0701-124">Specifies the source rectangle.</span></span> <span data-ttu-id="e0701-125">Legen Sie diesen Parameter auf **null** fest, um das gesamte Bild anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e0701-125">Set this parameter to **NULL** to specify the entire image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0701-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e0701-126">Return value</span></span>

<span data-ttu-id="e0701-127">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e0701-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e0701-128">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e0701-128">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e0701-129">Wenn die Funktion fehlschlägt, kann der Rückgabewert wie folgt lauten: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="e0701-129">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0701-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0701-130">Remarks</span></span>

<span data-ttu-id="e0701-131">Diese Funktion übernimmt die Konvertierung in und aus komprimierten Textur Formaten.</span><span class="sxs-lookup"><span data-stu-id="e0701-131">This function handles conversion to and from compressed texture formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0701-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0701-132">Requirements</span></span>



| <span data-ttu-id="e0701-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e0701-133">Requirement</span></span> | <span data-ttu-id="e0701-134">Wert</span><span class="sxs-lookup"><span data-stu-id="e0701-134">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e0701-135">Header</span><span class="sxs-lookup"><span data-stu-id="e0701-135">Header</span></span><br/>  | <dl> <span data-ttu-id="e0701-136"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0701-136"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="e0701-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e0701-137">Library</span></span><br/> | <dl> <span data-ttu-id="e0701-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e0701-138"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e0701-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0701-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0701-140">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="e0701-140">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="e0701-141">**D3DXSaveVolumeToFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="e0701-141">**D3DXSaveVolumeToFileInMemory**</span></span>](d3dxsavevolumetofileinmemory.md)
</dt> </dl>

 

 
