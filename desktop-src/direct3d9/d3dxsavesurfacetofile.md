---
description: Speichert eine-Oberfläche in einer Datei.
ms.assetid: 28bbf728-afde-4d25-8562-9d6a957aab2d
title: D3DXSaveSurfaceToFile-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveSurfaceToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cd19e0a8f7b9557b6bcbe6c71afcdca7c9037b70
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361863"
---
# <a name="d3dxsavesurfacetofile-function"></a><span data-ttu-id="60f61-103">D3DXSaveSurfaceToFile-Funktion</span><span class="sxs-lookup"><span data-stu-id="60f61-103">D3DXSaveSurfaceToFile function</span></span>

<span data-ttu-id="60f61-104">Speichert eine-Oberfläche in einer Datei.</span><span class="sxs-lookup"><span data-stu-id="60f61-104">Saves a surface to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="60f61-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="60f61-105">Syntax</span></span>


```C++
HRESULT D3DXSaveSurfaceToFile(
  _In_       LPCTSTR              pDestFile,
  _In_       D3DXIMAGE_FILEFORMAT DestFormat,
  _In_       LPDIRECT3DSURFACE9   pSrcSurface,
  _In_ const PALETTEENTRY         *pSrcPalette,
  _In_ const RECT                 *pSrcRect
);
```



## <a name="parameters"></a><span data-ttu-id="60f61-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="60f61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60f61-107">*pdestfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="60f61-107">*pDestFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60f61-108">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="60f61-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="60f61-109">Ein Zeiger auf eine Zeichenfolge, die den Dateinamen des Ziel Bilds angibt.</span><span class="sxs-lookup"><span data-stu-id="60f61-109">Pointer to a string that specifies the file name of the destination image.</span></span> <span data-ttu-id="60f61-110">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="60f61-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="60f61-111">Andernfalls wird der String-Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="60f61-111">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="60f61-112">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="60f61-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="60f61-113">*Destformat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="60f61-113">*DestFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60f61-114">Type: **[ **D3DXIMAGE \_ File Format**](./d3dximage-fileformat.md)**</span><span class="sxs-lookup"><span data-stu-id="60f61-114">Type: **[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md)**</span></span>

<span data-ttu-id="60f61-115">[**D3DXIMAGE \_ Dateiformat**](./d3dximage-fileformat.md) , das das beim Speichern zu verwendende Dateiformat angibt.</span><span class="sxs-lookup"><span data-stu-id="60f61-115">[**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md) specifying the file format to use when saving.</span></span> <span data-ttu-id="60f61-116">Diese Funktion unterstützt das Speichern in allen **D3DXIMAGE \_ File Format** -Formaten außer Portable pixmap (. ppm) und TARGA/Truevision Graphics Adapter (. TGA).</span><span class="sxs-lookup"><span data-stu-id="60f61-116">This function supports saving to all **D3DXIMAGE\_FILEFORMAT** formats except Portable Pixmap (.ppm) and Targa/Truevision Graphics Adapter (.tga).</span></span>

</dd> <dt>

<span data-ttu-id="60f61-117">*psrcsurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="60f61-117">*pSrcSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60f61-118">Typ: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="60f61-118">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="60f61-119">Ein Zeiger auf die [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) -Schnittstelle, die das zu speichernde Bild enthält.</span><span class="sxs-lookup"><span data-stu-id="60f61-119">Pointer to [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface, containing the image to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="60f61-120">*psrcpalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="60f61-120">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60f61-121">Typ: **Konstanten [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="60f61-121">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="60f61-122">Ein Zeiger auf eine [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) -Struktur, die eine Palette von 256 Farben enthält.</span><span class="sxs-lookup"><span data-stu-id="60f61-122">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure containing a palette of 256 colors.</span></span> <span data-ttu-id="60f61-123">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="60f61-123">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="60f61-124">*psrcrect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="60f61-124">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60f61-125">Typ: Konstante **[**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="60f61-125">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="60f61-126">Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="60f61-126">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="60f61-127">Gibt das Quell Rechteck an.</span><span class="sxs-lookup"><span data-stu-id="60f61-127">Specifies the source rectangle.</span></span> <span data-ttu-id="60f61-128">Legen Sie diesen Parameter auf **null** fest, um das gesamte Bild anzugeben.</span><span class="sxs-lookup"><span data-stu-id="60f61-128">Set this parameter to **NULL** to specify the entire image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60f61-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="60f61-129">Return value</span></span>

<span data-ttu-id="60f61-130">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="60f61-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="60f61-131">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="60f61-131">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="60f61-132">Wenn die Funktion fehlschlägt, kann der Rückgabewert wie folgt lauten: D3DERR \_ invalidcall</span><span class="sxs-lookup"><span data-stu-id="60f61-132">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="60f61-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60f61-133">Remarks</span></span>

<span data-ttu-id="60f61-134">Die Compilereinstellung bestimmt auch die Funktions Version.</span><span class="sxs-lookup"><span data-stu-id="60f61-134">The compiler setting also determines the function version.</span></span> <span data-ttu-id="60f61-135">Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXSaveSurfaceToFileW aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="60f61-135">If Unicode is defined, the function call resolves to D3DXSaveSurfaceToFileW.</span></span> <span data-ttu-id="60f61-136">Andernfalls wird der Funktions Aufruhe in D3DXSaveSurfaceToFileA aufgelöst, da ANSI-Zeichen folgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60f61-136">Otherwise, the function call resolves to D3DXSaveSurfaceToFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="60f61-137">Diese Funktion übernimmt die Konvertierung in und aus komprimierten Textur Formaten.</span><span class="sxs-lookup"><span data-stu-id="60f61-137">This function handles conversion to and from compressed texture formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="60f61-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60f61-138">Requirements</span></span>



| <span data-ttu-id="60f61-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60f61-139">Requirement</span></span> | <span data-ttu-id="60f61-140">Wert</span><span class="sxs-lookup"><span data-stu-id="60f61-140">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="60f61-141">Header</span><span class="sxs-lookup"><span data-stu-id="60f61-141">Header</span></span><br/>  | <dl> <span data-ttu-id="60f61-142"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="60f61-142"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="60f61-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="60f61-143">Library</span></span><br/> | <dl> <span data-ttu-id="60f61-144"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="60f61-144"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="60f61-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60f61-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60f61-146">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="60f61-146">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="60f61-147">**D3DXSaveTextureToFile**</span><span class="sxs-lookup"><span data-stu-id="60f61-147">**D3DXSaveTextureToFile**</span></span>](d3dxsavetexturetofile.md)
</dt> <dt>

[<span data-ttu-id="60f61-148">**D3DXSaveVolumeToFile**</span><span class="sxs-lookup"><span data-stu-id="60f61-148">**D3DXSaveVolumeToFile**</span></span>](d3dxsavevolumetofile.md)
</dt> </dl>

 

 
