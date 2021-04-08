---
description: Lädt eine-Oberfläche aus einer Datei.
ms.assetid: cbd360b6-6cee-418b-8c45-506e190eb2f6
title: D3DXLoadSurfaceFromFile-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f53343e436ac78b93bcee30c7da5c9d8eb2dc415
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762336"
---
# <a name="d3dxloadsurfacefromfile-function"></a><span data-ttu-id="2687d-103">D3DXLoadSurfaceFromFile-Funktion</span><span class="sxs-lookup"><span data-stu-id="2687d-103">D3DXLoadSurfaceFromFile function</span></span>

<span data-ttu-id="2687d-104">Lädt eine-Oberfläche aus einer Datei.</span><span class="sxs-lookup"><span data-stu-id="2687d-104">Loads a surface from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="2687d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2687d-105">Syntax</span></span>


```C++
HRESULT D3DXLoadSurfaceFromFile(
  _In_          LPDIRECT3DSURFACE9 pDestSurface,
  _In_    const PALETTEENTRY       *pDestPalette,
  _In_    const RECT               *pDestRect,
  _In_          LPCTSTR            pSrcFile,
  _In_    const RECT               *pSrcRect,
  _In_          DWORD              Filter,
  _In_          D3DCOLOR           ColorKey,
  _Inout_       D3DXIMAGE_INFO     *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="2687d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2687d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2687d-107">*pdestsurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2687d-107">*pDestSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2687d-108">Typ: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="2687d-108">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="2687d-109">Zeiger auf eine [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="2687d-109">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface.</span></span> <span data-ttu-id="2687d-110">Gibt die Ziel Oberfläche an, die das Bild empfängt.</span><span class="sxs-lookup"><span data-stu-id="2687d-110">Specifies the destination surface, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="2687d-111">*pdestpalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2687d-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2687d-112">Typ: **Konstanten [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="2687d-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="2687d-113">Zeiger auf eine [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) -Struktur, die Ziel Palette von 256 Farben oder **null**.</span><span class="sxs-lookup"><span data-stu-id="2687d-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2687d-114">*pdestrect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2687d-114">*pDestRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2687d-115">Typ: Konstante **[**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="2687d-115">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="2687d-116">Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="2687d-116">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="2687d-117">Gibt das Ziel Rechteck an.</span><span class="sxs-lookup"><span data-stu-id="2687d-117">Specifies the destination rectangle.</span></span> <span data-ttu-id="2687d-118">Legen Sie diesen Parameter auf **null** fest, um die gesamte Oberfläche anzugeben.</span><span class="sxs-lookup"><span data-stu-id="2687d-118">Set this parameter to **NULL** to specify the entire surface.</span></span>

</dd> <dt>

<span data-ttu-id="2687d-119">*psrcfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2687d-119">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2687d-120">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2687d-120">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2687d-121">Zeiger auf eine Zeichenfolge, die den Dateinamen angibt.</span><span class="sxs-lookup"><span data-stu-id="2687d-121">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="2687d-122">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="2687d-122">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="2687d-123">Andernfalls wird der String-Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="2687d-123">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="2687d-124">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="2687d-124">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2687d-125">*psrcrect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2687d-125">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2687d-126">Typ: Konstante **[**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="2687d-126">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="2687d-127">Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="2687d-127">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="2687d-128">Gibt das Quell Rechteck an.</span><span class="sxs-lookup"><span data-stu-id="2687d-128">Specifies the source rectangle.</span></span> <span data-ttu-id="2687d-129">Legen Sie diesen Parameter auf **null** fest, um das gesamte Bild anzugeben.</span><span class="sxs-lookup"><span data-stu-id="2687d-129">Set this parameter to **NULL** to specify the entire image.</span></span>

</dd> <dt>

<span data-ttu-id="2687d-130">*Filter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2687d-130">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2687d-131">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2687d-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2687d-132">Kombination aus einem oder mehreren [D3DX- \_ Filtern](d3dx-filter.md) , die Steuern, wie das Bild gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="2687d-132">Combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="2687d-133">Die Angabe \_ von D3DX default für diesen Parameter entspricht der Angabe von D3DX \_ Filter \_ Dreieck \| D3DX \_ Filter \_ Dither.</span><span class="sxs-lookup"><span data-stu-id="2687d-133">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="2687d-134">*Colorkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2687d-134">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2687d-135">Typ: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="2687d-135">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="2687d-136">[**D3DCOLOR**](d3dcolor.md) -Wert, der durch transparente schwarze ersetzt werden soll, oder 0, um den Colorkey zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="2687d-136">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="2687d-137">Dabei handelt es sich immer um eine 32-Bit-ARGB-Farbe, die unabhängig vom Quell Bildformat ist.</span><span class="sxs-lookup"><span data-stu-id="2687d-137">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="2687d-138">Alpha ist signifikant und sollte in der Regel für nicht transparente Farbtasten auf FF festgelegt werden. Daher wäre der Wert für den Wert 0xFF000000 gleich.</span><span class="sxs-lookup"><span data-stu-id="2687d-138">Alpha is significant and should usually be set to FF for opaque color keys Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="2687d-139">*psrcinfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2687d-139">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2687d-140">Type: **[ **D3DXIMAGE \_ Info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="2687d-140">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="2687d-141">Ein Zeiger auf eine [**D3DXIMAGE \_ Info**](d3dximage-info.md) -Struktur, die mit einer Beschreibung der Daten in der Quell Bilddatei gefüllt werden soll, oder **null**.</span><span class="sxs-lookup"><span data-stu-id="2687d-141">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2687d-142">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2687d-142">Return value</span></span>

<span data-ttu-id="2687d-143">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2687d-143">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2687d-144">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2687d-144">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2687d-145">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="2687d-145">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="2687d-146">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2687d-146">Remarks</span></span>

<span data-ttu-id="2687d-147">Die Compilereinstellung bestimmt auch die Funktions Version.</span><span class="sxs-lookup"><span data-stu-id="2687d-147">The compiler setting also determines the function version.</span></span> <span data-ttu-id="2687d-148">Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXLoadSurfaceFromFileW aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="2687d-148">If Unicode is defined, the function call resolves to D3DXLoadSurfaceFromFileW.</span></span> <span data-ttu-id="2687d-149">Andernfalls wird der Funktions Aufruhe in D3DXLoadSurfaceFromFileA aufgelöst, da ANSI-Zeichen folgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2687d-149">Otherwise, the function call resolves to D3DXLoadSurfaceFromFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="2687d-150">Diese Funktion verarbeitet die Konvertierung in und aus komprimierten Textur Formaten und unterstützt die folgenden Dateiformate: BMP,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm und. TGA.</span><span class="sxs-lookup"><span data-stu-id="2687d-150">This function handles conversion to and from compressed texture formats and supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="2687d-151">Siehe [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="2687d-151">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="2687d-152">Das Schreiben in eine Oberfläche ohne Ebene bewirkt nicht, dass das geänderte Rechteck aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="2687d-152">Writing to a non-level-zero surface will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="2687d-153">Wenn **D3DXLoadSurfaceFromFile** aufgerufen wird und die Oberfläche nicht bereits geändert wurde (Dies ist unwahrscheinlich in normalen Verwendungs Szenarien), muss die Anwendung [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) explizit auf der-Oberfläche aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2687d-153">If **D3DXLoadSurfaceFromFile** is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) on the surface.</span></span>

## <a name="requirements"></a><span data-ttu-id="2687d-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2687d-154">Requirements</span></span>



| <span data-ttu-id="2687d-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2687d-155">Requirement</span></span> | <span data-ttu-id="2687d-156">Wert</span><span class="sxs-lookup"><span data-stu-id="2687d-156">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2687d-157">Header</span><span class="sxs-lookup"><span data-stu-id="2687d-157">Header</span></span><br/>  | <dl> <span data-ttu-id="2687d-158"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="2687d-158"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="2687d-159">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2687d-159">Library</span></span><br/> | <dl> <span data-ttu-id="2687d-160"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2687d-160"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="2687d-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2687d-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2687d-162">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="2687d-162">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
