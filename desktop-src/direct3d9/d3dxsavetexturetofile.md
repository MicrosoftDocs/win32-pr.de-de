---
description: Speichert eine Textur in einer Datei.
ms.assetid: b14dd893-e967-4be9-81e8-aeb52035d91c
title: D3DXSaveTextureToFile-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveTextureToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c11cc8b512527fb0610c288fdbaeba6c976604a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367364"
---
# <a name="d3dxsavetexturetofile-function"></a><span data-ttu-id="4e31b-103">D3DXSaveTextureToFile-Funktion</span><span class="sxs-lookup"><span data-stu-id="4e31b-103">D3DXSaveTextureToFile function</span></span>

<span data-ttu-id="4e31b-104">Speichert eine Textur in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="4e31b-104">Saves a texture to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e31b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e31b-105">Syntax</span></span>


```C++
HRESULT D3DXSaveTextureToFile(
  _In_       LPCTSTR                pDestFile,
  _In_       D3DXIMAGE_FILEFORMAT   DestFormat,
  _In_       LPDIRECT3DBASETEXTURE9 pSrcTexture,
  _In_ const PALETTEENTRY           *pSrcPalette
);
```



## <a name="parameters"></a><span data-ttu-id="4e31b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e31b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e31b-107">*pdestfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e31b-107">*pDestFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e31b-108">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4e31b-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4e31b-109">Ein Zeiger auf eine Zeichenfolge, die den Dateinamen des Ziel Bilds angibt.</span><span class="sxs-lookup"><span data-stu-id="4e31b-109">Pointer to a string that specifies the file name of the destination image.</span></span> <span data-ttu-id="4e31b-110">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="4e31b-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="4e31b-111">Andernfalls wird der String-Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="4e31b-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="4e31b-112">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="4e31b-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4e31b-113">*Destformat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e31b-113">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e31b-114">Type: **[ **D3DXIMAGE \_ File Format**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="4e31b-114">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

<span data-ttu-id="4e31b-115">[**D3DXIMAGE \_ Dateiformat**](./d3dximage-fileformat.md) , das das beim Speichern zu verwendende Dateiformat angibt.</span><span class="sxs-lookup"><span data-stu-id="4e31b-115">[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md) specifying the file format to use when saving.</span></span> <span data-ttu-id="4e31b-116">Diese Funktion unterstützt das Speichern in allen **D3DXIMAGE \_ File Format** -Formaten außer Portable pixmap (. ppm) und TARGA/Truevision Graphics Adapter (. TGA).</span><span class="sxs-lookup"><span data-stu-id="4e31b-116">This function supports saving to all **D3DXIMAGE\_FILEFORMAT** formats except Portable Pixmap (.ppm) and Targa/Truevision Graphics Adapter (.tga).</span></span>

</dd> <dt>

<span data-ttu-id="4e31b-117">*psrctexture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e31b-117">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e31b-118">Typ: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span><span class="sxs-lookup"><span data-stu-id="4e31b-118">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span></span>

<span data-ttu-id="4e31b-119">Zeiger auf die [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) -Schnittstelle, die die zu speichernde Textur enthält.</span><span class="sxs-lookup"><span data-stu-id="4e31b-119">Pointer to [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) interface, containing the texture to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="4e31b-120">*psrcpalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e31b-120">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e31b-121">Typ: **Konstanten [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="4e31b-121">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="4e31b-122">Ein Zeiger auf eine [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) -Struktur, die eine Palette von 256 Farben enthält.</span><span class="sxs-lookup"><span data-stu-id="4e31b-122">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure containing a palette of 256 colors.</span></span> <span data-ttu-id="4e31b-123">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="4e31b-123">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e31b-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4e31b-124">Return value</span></span>

<span data-ttu-id="4e31b-125">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4e31b-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4e31b-126">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4e31b-126">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4e31b-127">Wenn die Funktion fehlschlägt, kann der Rückgabewert wie folgt lauten: D3DERR \_ invalidcall</span><span class="sxs-lookup"><span data-stu-id="4e31b-127">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="4e31b-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e31b-128">Remarks</span></span>

<span data-ttu-id="4e31b-129">Die Compilereinstellung bestimmt auch die Funktions Version.</span><span class="sxs-lookup"><span data-stu-id="4e31b-129">The compiler setting also determines the function version.</span></span> <span data-ttu-id="4e31b-130">Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXSaveTextureToFileW aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="4e31b-130">If Unicode is defined, the function call resolves to D3DXSaveTextureToFileW.</span></span> <span data-ttu-id="4e31b-131">Andernfalls wird der Funktions Aufruhe in D3DXSaveTextureToFileA aufgelöst, da ANSI-Zeichen folgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4e31b-131">Otherwise, the function call resolves to D3DXSaveTextureToFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="4e31b-132">Diese Funktion übernimmt die Konvertierung in und aus komprimierten Textur Formaten.</span><span class="sxs-lookup"><span data-stu-id="4e31b-132">This function handles conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="4e31b-133">Wenn das Volume nicht dynamisch ist (weil ein Verwendungs Parameter bei der Erstellung auf 0 festgelegt ist) und sich im Videospeicher befindet (der auf D3DPOOL default festgelegte Speicherpool \_ ), schlägt **D3DXSaveTextureToFile** fehl, da D3DX nicht dynamische Volumes nicht sperren kann, die sich im Videospeicher befinden.</span><span class="sxs-lookup"><span data-stu-id="4e31b-133">If the volume is nondynamic (because of a usage parameter set to 0 at the creation) and located in video memory (the memory pool set to D3DPOOL\_DEFAULT), **D3DXSaveTextureToFile** will fail because D3DX cannot lock nondynamic volumes located in video memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e31b-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e31b-134">Requirements</span></span>



| <span data-ttu-id="4e31b-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4e31b-135">Requirement</span></span> | <span data-ttu-id="4e31b-136">Wert</span><span class="sxs-lookup"><span data-stu-id="4e31b-136">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4e31b-137">Header</span><span class="sxs-lookup"><span data-stu-id="4e31b-137">Header</span></span><br/>  | <dl> <span data-ttu-id="4e31b-138"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e31b-138"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="4e31b-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4e31b-139">Library</span></span><br/> | <dl> <span data-ttu-id="4e31b-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e31b-140"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="4e31b-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e31b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e31b-142">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="4e31b-142">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="4e31b-143">**D3DXSaveSurfaceToFile**</span><span class="sxs-lookup"><span data-stu-id="4e31b-143">**D3DXSaveSurfaceToFile**</span></span>](d3dxsavesurfacetofile.md)
</dt> <dt>

[<span data-ttu-id="4e31b-144">**D3DXSaveVolumeToFile**</span><span class="sxs-lookup"><span data-stu-id="4e31b-144">**D3DXSaveVolumeToFile**</span></span>](d3dxsavevolumetofile.md)
</dt> </dl>

 

 
