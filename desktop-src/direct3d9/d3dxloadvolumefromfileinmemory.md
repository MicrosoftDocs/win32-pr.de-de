---
description: Lädt ein Volume aus einer Datei im Arbeitsspeicher.
ms.assetid: d450b652-3a74-45ea-9506-e05da87821d7
title: D3DXLoadVolumeFromFileInMemory-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 97ac67ab66a0072598bfea3b190bdf2c81ceba9a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961586"
---
# <a name="d3dxloadvolumefromfileinmemory-function"></a><span data-ttu-id="ca103-103">D3DXLoadVolumeFromFileInMemory-Funktion</span><span class="sxs-lookup"><span data-stu-id="ca103-103">D3DXLoadVolumeFromFileInMemory function</span></span>

<span data-ttu-id="ca103-104">Lädt ein Volume aus einer Datei im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="ca103-104">Loads a volume from a file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca103-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca103-105">Syntax</span></span>


```C++
HRESULT D3DXLoadVolumeFromFileInMemory(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       LPCVOID           pSrcData,
  _In_       UINT              SrcDataSize,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey,
  _In_       D3DXIMAGE_INFO    *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="ca103-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca103-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca103-107">*pdestvolume* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca103-107">*pDestVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca103-108">Typ: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="ca103-108">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="ca103-109">Zeiger auf eine [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="ca103-109">Pointer to an [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface.</span></span> <span data-ttu-id="ca103-110">Gibt das Ziel Volume an.</span><span class="sxs-lookup"><span data-stu-id="ca103-110">Specifies the destination volume.</span></span>

</dd> <dt>

<span data-ttu-id="ca103-111">*pdestpalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca103-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca103-112">Typ: **Konstanten [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="ca103-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="ca103-113">Zeiger auf eine [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) -Struktur, die Ziel Palette von 256 Farben oder **null**.</span><span class="sxs-lookup"><span data-stu-id="ca103-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ca103-114">*pdestbox* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca103-114">*pDestBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca103-115">Typ: **Konstanten [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="ca103-115">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="ca103-116">Zeiger auf eine [**D3DBOX**](d3dbox.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="ca103-116">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="ca103-117">Gibt das Zielfeld an.</span><span class="sxs-lookup"><span data-stu-id="ca103-117">Specifies the destination box.</span></span> <span data-ttu-id="ca103-118">Legen Sie diesen Parameter auf **null** fest, um das gesamte Volume anzugeben.</span><span class="sxs-lookup"><span data-stu-id="ca103-118">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="ca103-119">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca103-119">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca103-120">Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ca103-120">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ca103-121">Zeiger auf die Datei im Arbeitsspeicher, von der das Volume geladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ca103-121">Pointer to the file in memory from which to load the volume.</span></span>

</dd> <dt>

<span data-ttu-id="ca103-122">*Srcdatasize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca103-122">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca103-123">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ca103-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ca103-124">Größe der Datei in Bytes im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="ca103-124">Size in bytes of the file in memory.</span></span>

</dd> <dt>

<span data-ttu-id="ca103-125">*psrcbox* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca103-125">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca103-126">Typ: **Konstanten [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="ca103-126">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="ca103-127">Zeiger auf eine [**D3DBOX**](d3dbox.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="ca103-127">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="ca103-128">Gibt das Quellfeld an.</span><span class="sxs-lookup"><span data-stu-id="ca103-128">Specifies the source box.</span></span> <span data-ttu-id="ca103-129">Legen Sie diesen Parameter auf **null** fest, um das gesamte Volume anzugeben.</span><span class="sxs-lookup"><span data-stu-id="ca103-129">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="ca103-130">*Filter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca103-130">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca103-131">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ca103-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ca103-132">Kombination aus einem oder mehreren [D3DX- \_ Filtern](d3dx-filter.md), um die Filterung des Bilds zu steuern.</span><span class="sxs-lookup"><span data-stu-id="ca103-132">Combination of one or more [D3DX\_FILTER](d3dx-filter.md), controlling how the image is filtered.</span></span> <span data-ttu-id="ca103-133">Die Angabe \_ von D3DX default für diesen Parameter entspricht der Angabe von D3DX \_ Filter \_ Dreieck \| D3DX \_ Filter \_ Dither.</span><span class="sxs-lookup"><span data-stu-id="ca103-133">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="ca103-134">*Colorkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca103-134">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca103-135">Typ: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="ca103-135">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="ca103-136">[**D3DCOLOR**](d3dcolor.md) -Wert, der durch transparente schwarze ersetzt werden soll, oder 0, um den Colorkey zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="ca103-136">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="ca103-137">Dabei handelt es sich immer um eine 32-Bit-ARGB-Farbe, die unabhängig vom Quell Bildformat ist.</span><span class="sxs-lookup"><span data-stu-id="ca103-137">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="ca103-138">Alpha ist signifikant und sollte normalerweise für nicht transparente Farbtasten auf FF festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ca103-138">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="ca103-139">Daher wäre der Wert für den Wert "0xFF000000" gleich.</span><span class="sxs-lookup"><span data-stu-id="ca103-139">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="ca103-140">*psrcinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca103-140">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca103-141">Type: **[ **D3DXIMAGE \_ Info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="ca103-141">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="ca103-142">Ein Zeiger auf eine [**D3DXIMAGE \_ Info**](d3dximage-info.md) -Struktur, die mit einer Beschreibung der Daten in der Quell Bilddatei gefüllt werden soll, oder **null**.</span><span class="sxs-lookup"><span data-stu-id="ca103-142">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca103-143">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ca103-143">Return value</span></span>

<span data-ttu-id="ca103-144">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ca103-144">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ca103-145">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ca103-145">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ca103-146">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="ca103-146">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca103-147">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ca103-147">Remarks</span></span>

<span data-ttu-id="ca103-148">Diese Funktion verarbeitet die Konvertierung in und aus komprimierten Textur Formaten und unterstützt die folgenden Dateiformate: BMP,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm und. TGA.</span><span class="sxs-lookup"><span data-stu-id="ca103-148">This function handles conversion to and from compressed texture formats and supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="ca103-149">Siehe [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="ca103-149">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="ca103-150">Das Schreiben auf eine Oberfläche ohne Ebene der volumetextur bewirkt nicht, dass das geänderte Rechteck aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="ca103-150">Writing to a non-level-zero surface of the volume texture will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="ca103-151">Wenn **D3DXLoadVolumeFromFileInMemory** aufgerufen wird und die Textur nicht bereits geändert wurde (Dies ist unwahrscheinlich in normalen Verwendungs Szenarien), muss die Anwendung [**IDirect3DVolumeTexture9:: adddirtybox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) explizit auf der volumetextur aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ca103-151">If **D3DXLoadVolumeFromFileInMemory** is called and the texture was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) on the volume texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca103-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca103-152">Requirements</span></span>



| <span data-ttu-id="ca103-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca103-153">Requirement</span></span> | <span data-ttu-id="ca103-154">Wert</span><span class="sxs-lookup"><span data-stu-id="ca103-154">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ca103-155">Header</span><span class="sxs-lookup"><span data-stu-id="ca103-155">Header</span></span><br/>  | <dl> <span data-ttu-id="ca103-156"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca103-156"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="ca103-157">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ca103-157">Library</span></span><br/> | <dl> <span data-ttu-id="ca103-158"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ca103-158"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ca103-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca103-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca103-160">**D3DXLoadVolumeFromFile**</span><span class="sxs-lookup"><span data-stu-id="ca103-160">**D3DXLoadVolumeFromFile**</span></span>](d3dxloadvolumefromfile.md)
</dt> <dt>

[<span data-ttu-id="ca103-161">**D3DXLoadVolumeFromMemory**</span><span class="sxs-lookup"><span data-stu-id="ca103-161">**D3DXLoadVolumeFromMemory**</span></span>](d3dxloadvolumefrommemory.md)
</dt> <dt>

[<span data-ttu-id="ca103-162">**D3DXLoadVolumeFromResource**</span><span class="sxs-lookup"><span data-stu-id="ca103-162">**D3DXLoadVolumeFromResource**</span></span>](d3dxloadvolumefromresource.md)
</dt> <dt>

[<span data-ttu-id="ca103-163">**D3DXLoadVolumeFromVolume**</span><span class="sxs-lookup"><span data-stu-id="ca103-163">**D3DXLoadVolumeFromVolume**</span></span>](d3dxloadvolumefromvolume.md)
</dt> <dt>

[<span data-ttu-id="ca103-164">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="ca103-164">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
