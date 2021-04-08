---
description: Lädt eine Oberfläche aus einer Datei im Arbeitsspeicher.
ms.assetid: 436a6151-2819-44eb-bd56-1b3777f709e5
title: D3DXLoadSurfaceFromFileInMemory-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a447c4c5b65e3085d84e26ef202283cf0c31c6b5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762333"
---
# <a name="d3dxloadsurfacefromfileinmemory-function"></a><span data-ttu-id="da38e-103">D3DXLoadSurfaceFromFileInMemory-Funktion</span><span class="sxs-lookup"><span data-stu-id="da38e-103">D3DXLoadSurfaceFromFileInMemory function</span></span>

<span data-ttu-id="da38e-104">Lädt eine Oberfläche aus einer Datei im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="da38e-104">Loads a surface from a file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="da38e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="da38e-105">Syntax</span></span>


```C++
HRESULT D3DXLoadSurfaceFromFileInMemory(
  _In_          LPDIRECT3DSURFACE9 pDestSurface,
  _In_    const PALETTEENTRY       *pDestPalette,
  _In_    const RECT               *pDestRect,
  _In_          LPCVOID            pSrcData,
  _In_          UINT               SrcData,
  _In_    const RECT               *pSrcRect,
  _In_          DWORD              Filter,
  _In_          D3DCOLOR           ColorKey,
  _Inout_       D3DXIMAGE_INFO     *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="da38e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="da38e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da38e-107">*pdestsurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da38e-107">*pDestSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da38e-108">Typ: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="da38e-108">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="da38e-109">Zeiger auf eine [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="da38e-109">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface.</span></span> <span data-ttu-id="da38e-110">Gibt die Ziel Oberfläche an, die das Bild empfängt.</span><span class="sxs-lookup"><span data-stu-id="da38e-110">Specifies the destination surface, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="da38e-111">*pdestpalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da38e-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da38e-112">Typ: **Konstanten [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="da38e-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="da38e-113">Zeiger auf eine [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) -Struktur, die Ziel Palette von 256 Farben oder **null**.</span><span class="sxs-lookup"><span data-stu-id="da38e-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="da38e-114">*pdestrect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da38e-114">*pDestRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da38e-115">Typ: Konstante **[**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="da38e-115">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="da38e-116">Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="da38e-116">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="da38e-117">Gibt das Ziel Rechteck an.</span><span class="sxs-lookup"><span data-stu-id="da38e-117">Specifies the destination rectangle.</span></span> <span data-ttu-id="da38e-118">Legen Sie diesen Parameter auf **null** fest, um die gesamte Oberfläche anzugeben.</span><span class="sxs-lookup"><span data-stu-id="da38e-118">Set this parameter to **NULL** to specify the entire surface.</span></span>

</dd> <dt>

<span data-ttu-id="da38e-119">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da38e-119">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da38e-120">Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="da38e-120">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="da38e-121">Ein Zeiger auf die Datei im Arbeitsspeicher, von der die-Oberfläche geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="da38e-121">Pointer to the file in memory from which to load the surface.</span></span>

</dd> <dt>

<span data-ttu-id="da38e-122">*Srcdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da38e-122">*SrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da38e-123">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="da38e-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="da38e-124">Größe der Datei im Arbeitsspeicher in Bytes.</span><span class="sxs-lookup"><span data-stu-id="da38e-124">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="da38e-125">*psrcrect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da38e-125">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da38e-126">Typ: Konstante **[**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="da38e-126">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="da38e-127">Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="da38e-127">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="da38e-128">Gibt das Quell Rechteck an.</span><span class="sxs-lookup"><span data-stu-id="da38e-128">Specifies the source rectangle.</span></span> <span data-ttu-id="da38e-129">Legen Sie diesen Parameter auf **null** fest, um das gesamte Bild anzugeben.</span><span class="sxs-lookup"><span data-stu-id="da38e-129">Set this parameter to **NULL** to specify the entire image.</span></span>

</dd> <dt>

<span data-ttu-id="da38e-130">*Filter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da38e-130">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da38e-131">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="da38e-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="da38e-132">Eine Kombination aus einem oder mehreren [D3DX- \_ Filtern](d3dx-filter.md) , die Steuern, wie das Bild gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="da38e-132">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="da38e-133">Die Angabe \_ von D3DX default für diesen Parameter entspricht der Angabe von D3DX \_ Filter \_ Dreieck \| D3DX \_ Filter \_ Dither.</span><span class="sxs-lookup"><span data-stu-id="da38e-133">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="da38e-134">*Colorkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da38e-134">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da38e-135">Typ: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="da38e-135">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="da38e-136">[**D3DCOLOR**](d3dcolor.md) -Wert, der durch transparente schwarze ersetzt werden soll, oder 0, um den Colorkey zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="da38e-136">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="da38e-137">Dabei handelt es sich immer um eine 32-Bit-ARGB-Farbe, die unabhängig vom Quell Bildformat ist.</span><span class="sxs-lookup"><span data-stu-id="da38e-137">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="da38e-138">Alpha ist signifikant und sollte normalerweise für nicht transparente Farbtasten auf FF festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="da38e-138">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="da38e-139">Daher wäre der Wert für den Wert "0xFF000000" gleich.</span><span class="sxs-lookup"><span data-stu-id="da38e-139">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="da38e-140">*psrcinfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="da38e-140">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="da38e-141">Type: **[ **D3DXIMAGE \_ Info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="da38e-141">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="da38e-142">Zeiger auf eine [**D3DXIMAGE \_ Info**](d3dximage-info.md) -Struktur, die mit einer Beschreibung der Daten in der Quell Bilddatei oder **null** aufgefüllt werden soll.</span><span class="sxs-lookup"><span data-stu-id="da38e-142">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da38e-143">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="da38e-143">Return value</span></span>

<span data-ttu-id="da38e-144">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="da38e-144">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="da38e-145">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="da38e-145">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="da38e-146">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="da38e-146">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="da38e-147">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="da38e-147">Remarks</span></span>

<span data-ttu-id="da38e-148">Diese Funktion verarbeitet die Konvertierung in und aus komprimierten Textur Formaten und unterstützt die folgenden Dateiformate: BMP,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm und. TGA.</span><span class="sxs-lookup"><span data-stu-id="da38e-148">This function handles conversion to and from compressed texture formats and supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="da38e-149">Siehe [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="da38e-149">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="da38e-150">Das Schreiben in eine Oberfläche ohne Ebene bewirkt nicht, dass das geänderte Rechteck aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="da38e-150">Writing to a non-level-zero surface will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="da38e-151">Wenn **D3DXLoadSurfaceFromFileInMemory** aufgerufen wird und die Oberfläche nicht bereits geändert wurde (Dies ist unwahrscheinlich in normalen Verwendungs Szenarien), muss die Anwendung [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) explizit auf der-Oberfläche aufrufen.</span><span class="sxs-lookup"><span data-stu-id="da38e-151">If **D3DXLoadSurfaceFromFileInMemory** is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) on the surface.</span></span>

## <a name="requirements"></a><span data-ttu-id="da38e-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da38e-152">Requirements</span></span>



| <span data-ttu-id="da38e-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da38e-153">Requirement</span></span> | <span data-ttu-id="da38e-154">Wert</span><span class="sxs-lookup"><span data-stu-id="da38e-154">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="da38e-155">Header</span><span class="sxs-lookup"><span data-stu-id="da38e-155">Header</span></span><br/>  | <dl> <span data-ttu-id="da38e-156"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="da38e-156"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="da38e-157">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="da38e-157">Library</span></span><br/> | <dl> <span data-ttu-id="da38e-158"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="da38e-158"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="da38e-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da38e-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da38e-160">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="da38e-160">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
