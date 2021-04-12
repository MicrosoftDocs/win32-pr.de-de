---
description: Speichert ein Volume in einem Puffer. Die-Methode erstellt einen ID3DXBuffer-Puffer zum Speichern der Daten und gibt dieses Objekt zurück.
ms.assetid: 4887ff1f-7904-4764-b284-b2c8e037f806
title: D3DXSaveVolumeToFileInMemory-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveVolumeToFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7daaa41e0cc87ea03a0aedc5fc2f7ca96653329f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219497"
---
# <a name="d3dxsavevolumetofileinmemory-function"></a><span data-ttu-id="6330b-104">D3DXSaveVolumeToFileInMemory-Funktion</span><span class="sxs-lookup"><span data-stu-id="6330b-104">D3DXSaveVolumeToFileInMemory function</span></span>

<span data-ttu-id="6330b-105">Speichert ein Volume in einem Puffer.</span><span class="sxs-lookup"><span data-stu-id="6330b-105">Saves a volume to a buffer.</span></span> <span data-ttu-id="6330b-106">Die-Methode erstellt einen [**ID3DXBuffer**](id3dxbuffer.md) -Puffer zum Speichern der Daten und gibt dieses Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="6330b-106">The method creates an [**ID3DXBuffer**](id3dxbuffer.md) buffer to store the data, and returns that object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6330b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6330b-107">Syntax</span></span>


```C++
HRESULT D3DXSaveVolumeToFileInMemory(
  _Out_       LPD3DXBUFFER         *ppDestBuf,
  _In_        D3DXIMAGE_FILEFORMAT DestFormat,
  _In_        LPDIRECT3DVOLUME9    pSrcVolume,
  _In_  const PALETTEENTRY         *pSrcPalette,
  _In_  const D3DBOX               *pSrcBox
);
```



## <a name="parameters"></a><span data-ttu-id="6330b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6330b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6330b-109">*ppdestbuf* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6330b-109">*ppDestBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6330b-110">Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="6330b-110">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="6330b-111">Adresse eines Zeigers auf einen [**ID3DXBuffer**](id3dxbuffer.md) -Puffer, in dem das Bild gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="6330b-111">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) buffer that will store the image.</span></span>

</dd> <dt>

<span data-ttu-id="6330b-112">*Destformat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6330b-112">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6330b-113">Type: **[ **D3DXIMAGE \_ File Format**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="6330b-113">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

<span data-ttu-id="6330b-114">[**D3DXIMAGE \_ Dateiformat**](./d3dximage-fileformat.md) , das das beim Speichern zu verwendende Dateiformat angibt.</span><span class="sxs-lookup"><span data-stu-id="6330b-114">[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md) specifying the file format to use when saving.</span></span> <span data-ttu-id="6330b-115">Diese Funktion unterstützt das Speichern in allen **D3DXIMAGE \_ File Format** -Formaten außer Portable pixmap (. ppm) und TARGA/Truevision Graphics Adapter (. TGA).</span><span class="sxs-lookup"><span data-stu-id="6330b-115">This function supports saving to all **D3DXIMAGE\_FILEFORMAT** formats except Portable Pixmap (.ppm) and Targa/Truevision Graphics Adapter (.tga).</span></span>

</dd> <dt>

<span data-ttu-id="6330b-116">*psrcvolume* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6330b-116">*pSrcVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6330b-117">Typ: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="6330b-117">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="6330b-118">Zeiger auf die [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) -Schnittstelle, die das zu speichernde Bild enthält.</span><span class="sxs-lookup"><span data-stu-id="6330b-118">Pointer to [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface containing the image to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="6330b-119">*psrcpalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6330b-119">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6330b-120">Typ: **Konstanten [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="6330b-120">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="6330b-121">Ein Zeiger auf eine [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) -Struktur, die eine Palette von 256 Farben enthält.</span><span class="sxs-lookup"><span data-stu-id="6330b-121">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure containing a palette of 256 colors.</span></span> <span data-ttu-id="6330b-122">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="6330b-122">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6330b-123">*psrcbox* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6330b-123">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6330b-124">Typ: **Konstanten [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="6330b-124">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="6330b-125">Zeiger auf eine [**D3DBOX**](d3dbox.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="6330b-125">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="6330b-126">Gibt das Quellfeld an.</span><span class="sxs-lookup"><span data-stu-id="6330b-126">Specifies the source box.</span></span> <span data-ttu-id="6330b-127">Legen Sie diesen Parameter auf **null** fest, um das gesamte Volume anzugeben.</span><span class="sxs-lookup"><span data-stu-id="6330b-127">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6330b-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6330b-128">Return value</span></span>

<span data-ttu-id="6330b-129">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6330b-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6330b-130">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6330b-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6330b-131">Wenn die Funktion fehlschlägt, kann der Rückgabewert wie folgt lauten: D3DERR \_ invalidcall</span><span class="sxs-lookup"><span data-stu-id="6330b-131">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="6330b-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6330b-132">Requirements</span></span>



| <span data-ttu-id="6330b-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6330b-133">Requirement</span></span> | <span data-ttu-id="6330b-134">Wert</span><span class="sxs-lookup"><span data-stu-id="6330b-134">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6330b-135">Header</span><span class="sxs-lookup"><span data-stu-id="6330b-135">Header</span></span><br/>  | <dl> <span data-ttu-id="6330b-136"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="6330b-136"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="6330b-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6330b-137">Library</span></span><br/> | <dl> <span data-ttu-id="6330b-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6330b-138"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="6330b-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6330b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6330b-140">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="6330b-140">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="6330b-141">**D3DXSaveVolumeToFile**</span><span class="sxs-lookup"><span data-stu-id="6330b-141">**D3DXSaveVolumeToFile**</span></span>](d3dxsavevolumetofile.md)
</dt> </dl>

 

 
