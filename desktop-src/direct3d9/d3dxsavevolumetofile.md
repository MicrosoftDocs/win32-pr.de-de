---
description: Speichert ein Volume in einer Datei auf dem Datenträger.
ms.assetid: 4d33fba5-e003-4385-b683-aff6723af2a5
title: D3DXSaveVolumeToFile-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveVolumeToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 36550cda8d9ef664f96e236d2770a82c88412772
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106373509"
---
# <a name="d3dxsavevolumetofile-function"></a><span data-ttu-id="dfcde-103">D3DXSaveVolumeToFile-Funktion</span><span class="sxs-lookup"><span data-stu-id="dfcde-103">D3DXSaveVolumeToFile function</span></span>

<span data-ttu-id="dfcde-104">Speichert ein Volume in einer Datei auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="dfcde-104">Saves a volume to a file on disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfcde-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dfcde-105">Syntax</span></span>


```C++
HRESULT D3DXSaveVolumeToFile(
  _In_       LPCTSTR              pDestFile,
  _In_       D3DXIMAGE_FILEFORMAT DestFormat,
  _In_       LPDIRECT3DVOLUME9    pSrcVolume,
  _In_ const PALETTEENTRY         *pSrcPalette,
  _In_ const D3DBOX               *pSrcBox
);
```



## <a name="parameters"></a><span data-ttu-id="dfcde-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dfcde-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfcde-107">*pdestfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dfcde-107">*pDestFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfcde-108">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dfcde-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dfcde-109">Ein Zeiger auf eine Zeichenfolge, die den Dateinamen des Ziel Bilds angibt.</span><span class="sxs-lookup"><span data-stu-id="dfcde-109">Pointer to a string that specifies the file name of the destination image.</span></span> <span data-ttu-id="dfcde-110">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="dfcde-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="dfcde-111">Andernfalls wird der String-Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="dfcde-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="dfcde-112">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="dfcde-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="dfcde-113">*Destformat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dfcde-113">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfcde-114">Type: **[ **D3DXIMAGE \_ File Format**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="dfcde-114">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

<span data-ttu-id="dfcde-115">[**D3DXIMAGE \_ Dateiformat**](./d3dximage-fileformat.md) , das das beim Speichern zu verwendende Dateiformat angibt.</span><span class="sxs-lookup"><span data-stu-id="dfcde-115">[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md) specifying the file format to use when saving.</span></span> <span data-ttu-id="dfcde-116">Diese Funktion unterstützt das Speichern in allen **D3DXIMAGE \_ File Format** -Formaten außer Portable pixmap (. ppm) und TARGA/Truevision Graphics Adapter (. TGA).</span><span class="sxs-lookup"><span data-stu-id="dfcde-116">This function supports saving to all **D3DXIMAGE\_FILEFORMAT** formats except Portable Pixmap (.ppm) and Targa/Truevision Graphics Adapter (.tga).</span></span>

</dd> <dt>

<span data-ttu-id="dfcde-117">*psrcvolume* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dfcde-117">*pSrcVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfcde-118">Typ: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="dfcde-118">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="dfcde-119">Zeiger auf die [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) -Schnittstelle, die das zu speichernde Bild enthält.</span><span class="sxs-lookup"><span data-stu-id="dfcde-119">Pointer to [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface containing the image to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="dfcde-120">*psrcpalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dfcde-120">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfcde-121">Typ: **Konstanten [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="dfcde-121">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="dfcde-122">Ein Zeiger auf eine [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) -Struktur, die eine Palette von 256 Farben enthält.</span><span class="sxs-lookup"><span data-stu-id="dfcde-122">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure containing a palette of 256 colors.</span></span> <span data-ttu-id="dfcde-123">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="dfcde-123">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="dfcde-124">*psrcbox* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dfcde-124">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfcde-125">Typ: **Konstanten [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="dfcde-125">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="dfcde-126">Zeiger auf eine [**D3DBOX**](d3dbox.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="dfcde-126">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="dfcde-127">Gibt das Quellfeld an.</span><span class="sxs-lookup"><span data-stu-id="dfcde-127">Specifies the source box.</span></span> <span data-ttu-id="dfcde-128">Legen Sie diesen Parameter auf **null** fest, um das gesamte Volume anzugeben.</span><span class="sxs-lookup"><span data-stu-id="dfcde-128">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfcde-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dfcde-129">Return value</span></span>

<span data-ttu-id="dfcde-130">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dfcde-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dfcde-131">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dfcde-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="dfcde-132">Wenn die Funktion fehlschlägt, kann der Rückgabewert wie folgt lauten: D3DERR \_ invalidcall</span><span class="sxs-lookup"><span data-stu-id="dfcde-132">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="dfcde-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dfcde-133">Remarks</span></span>

<span data-ttu-id="dfcde-134">Die Compilereinstellung bestimmt auch die Funktions Version.</span><span class="sxs-lookup"><span data-stu-id="dfcde-134">The compiler setting also determines the function version.</span></span> <span data-ttu-id="dfcde-135">Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXSaveVolumeToFileW aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="dfcde-135">If Unicode is defined, the function call resolves to D3DXSaveVolumeToFileW.</span></span> <span data-ttu-id="dfcde-136">Andernfalls wird der Funktions Aufruhe in >D3DXSaveVolumeToFileA aufgelöst, da ANSI-Zeichen folgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dfcde-136">Otherwise, the function call resolves to >D3DXSaveVolumeToFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="dfcde-137">Diese Funktion übernimmt die Konvertierung in und aus komprimierten Textur Formaten.</span><span class="sxs-lookup"><span data-stu-id="dfcde-137">This function handles conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="dfcde-138">Wenn das Volume nicht dynamisch ist (weil ein Verwendungs Parameter bei der Erstellung auf 0 festgelegt ist) und sich im Videospeicher befindet (der auf D3DPOOL default festgelegte Speicherpool \_ ), schlägt [**D3DXSaveTextureToFile**](d3dxsavetexturetofile.md) fehl, da D3DX nicht dynamische Volumes nicht sperren kann, die sich im Videospeicher befinden.</span><span class="sxs-lookup"><span data-stu-id="dfcde-138">If the volume is nondynamic (because of a usage parameter set to 0 at the creation) and located in video memory (the memory pool set to D3DPOOL\_DEFAULT), [**D3DXSaveTextureToFile**](d3dxsavetexturetofile.md) will fail because D3DX cannot lock nondynamic volumes located in video memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfcde-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dfcde-139">Requirements</span></span>



| <span data-ttu-id="dfcde-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dfcde-140">Requirement</span></span> | <span data-ttu-id="dfcde-141">Wert</span><span class="sxs-lookup"><span data-stu-id="dfcde-141">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dfcde-142">Header</span><span class="sxs-lookup"><span data-stu-id="dfcde-142">Header</span></span><br/>  | <dl> <span data-ttu-id="dfcde-143"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfcde-143"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="dfcde-144">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dfcde-144">Library</span></span><br/> | <dl> <span data-ttu-id="dfcde-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dfcde-145"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="dfcde-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dfcde-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfcde-147">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="dfcde-147">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="dfcde-148">**D3DXSaveSurfaceToFile**</span><span class="sxs-lookup"><span data-stu-id="dfcde-148">**D3DXSaveSurfaceToFile**</span></span>](d3dxsavesurfacetofile.md)
</dt> <dt>

[<span data-ttu-id="dfcde-149">**D3DXSaveTextureToFile**</span><span class="sxs-lookup"><span data-stu-id="dfcde-149">**D3DXSaveTextureToFile**</span></span>](d3dxsavetexturetofile.md)
</dt> <dt>

[<span data-ttu-id="dfcde-150">**D3DXSaveVolumeToFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="dfcde-150">**D3DXSaveVolumeToFileInMemory**</span></span>](d3dxsavevolumetofileinmemory.md)
</dt> </dl>

 

 
