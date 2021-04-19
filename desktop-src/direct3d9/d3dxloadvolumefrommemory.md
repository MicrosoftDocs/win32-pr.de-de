---
description: Lädt ein Volume aus dem Arbeitsspeicher.
ms.assetid: 9f74fcc0-f935-4466-865b-e798711a1f2f
title: D3DXLoadVolumeFromMemory-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7d6c3f1bdfe40f19eeb57b4f0d8a38c40a239404
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355781"
---
# <a name="d3dxloadvolumefrommemory-function"></a><span data-ttu-id="1cae6-103">D3DXLoadVolumeFromMemory-Funktion</span><span class="sxs-lookup"><span data-stu-id="1cae6-103">D3DXLoadVolumeFromMemory function</span></span>

<span data-ttu-id="1cae6-104">Lädt ein Volume aus dem Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="1cae6-104">Loads a volume from memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cae6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1cae6-105">Syntax</span></span>


```C++
HRESULT D3DXLoadVolumeFromMemory(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       LPCVOID           pSrcMemory,
  _In_       D3DFORMAT         SrcFormat,
  _In_       UINT              SrcRowPitch,
  _In_       UINT              SrcSlicePitch,
  _In_ const PALETTEENTRY      *pSrcPalette,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey
);
```



## <a name="parameters"></a><span data-ttu-id="1cae6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1cae6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cae6-107">*pdestvolume* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1cae6-107">*pDestVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cae6-108">Typ: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="1cae6-108">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="1cae6-109">Zeiger auf eine [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="1cae6-109">Pointer to an [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface.</span></span> <span data-ttu-id="1cae6-110">Gibt das Ziel Volume an, das das Abbild empfängt.</span><span class="sxs-lookup"><span data-stu-id="1cae6-110">Specifies the destination volume, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="1cae6-111">*pdestpalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1cae6-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cae6-112">Typ: **Konstanten [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="1cae6-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="1cae6-113">Zeiger auf eine [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) -Struktur, die Ziel Palette von 256 Farben oder **null**.</span><span class="sxs-lookup"><span data-stu-id="1cae6-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1cae6-114">*pdestbox* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1cae6-114">*pDestBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cae6-115">Typ: **Konstanten [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="1cae6-115">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="1cae6-116">Zeiger auf eine [**D3DBOX**](d3dbox.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="1cae6-116">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="1cae6-117">Gibt das Zielfeld an.</span><span class="sxs-lookup"><span data-stu-id="1cae6-117">Specifies the destination box.</span></span> <span data-ttu-id="1cae6-118">Legen Sie diesen Parameter auf **null** fest, um das gesamte Volume anzugeben.</span><span class="sxs-lookup"><span data-stu-id="1cae6-118">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="1cae6-119">*psrcmemory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1cae6-119">*pSrcMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cae6-120">Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1cae6-120">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1cae6-121">Zeiger auf die linke obere Ecke des Quell Volumes im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="1cae6-121">Pointer to the top-left corner of the source volume in memory.</span></span>

</dd> <dt>

<span data-ttu-id="1cae6-122">*Srcformat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1cae6-122">*SrcFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cae6-123">Typ: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="1cae6-123">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="1cae6-124">Member des [D3DFORMAT](d3dformat.md) -Enumerationstyps, das Pixel Format des Quell Volume.</span><span class="sxs-lookup"><span data-stu-id="1cae6-124">Member of the [D3DFORMAT](d3dformat.md) enumerated type, the pixel format of the source volume.</span></span>

</dd> <dt>

<span data-ttu-id="1cae6-125">*Srcrowpitch* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1cae6-125">*SrcRowPitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cae6-126">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1cae6-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1cae6-127">Die Darstellung des Quell Bilds in Bytes.</span><span class="sxs-lookup"><span data-stu-id="1cae6-127">Pitch of source image, in bytes.</span></span> <span data-ttu-id="1cae6-128">Bei DXT-Formaten (komprimierte Textur Formate) sollte diese Zahl die Größe einer Zellen Zelle in Bytes darstellen.</span><span class="sxs-lookup"><span data-stu-id="1cae6-128">For DXT formats (compressed texture formats), this number should represent the size of one row of cells, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="1cae6-129">*Srcslicepitch* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1cae6-129">*SrcSlicePitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cae6-130">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1cae6-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1cae6-131">Die Darstellung des Quell Bilds in Bytes.</span><span class="sxs-lookup"><span data-stu-id="1cae6-131">Pitch of source image, in bytes.</span></span> <span data-ttu-id="1cae6-132">Bei DXT-Formaten (komprimierte Textur Formate) sollte diese Zahl die Größe eines Slice von Zellen in Bytes darstellen.</span><span class="sxs-lookup"><span data-stu-id="1cae6-132">For DXT formats (compressed texture formats), this number should represent the size of one slice of cells, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="1cae6-133">*psrcpalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1cae6-133">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cae6-134">Typ: **Konstanten [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="1cae6-134">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="1cae6-135">Zeiger auf eine [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) -Struktur, die Quell Palette von 256 Farben oder **null**.</span><span class="sxs-lookup"><span data-stu-id="1cae6-135">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the source palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1cae6-136">*psrcbox* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1cae6-136">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cae6-137">Typ: **Konstanten [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="1cae6-137">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="1cae6-138">Zeiger auf eine [**D3DBOX**](d3dbox.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="1cae6-138">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="1cae6-139">Gibt das Quellfeld an.</span><span class="sxs-lookup"><span data-stu-id="1cae6-139">Specifies the source box.</span></span> <span data-ttu-id="1cae6-140">**Null** ist kein gültiger Wert für diesen Parameter.</span><span class="sxs-lookup"><span data-stu-id="1cae6-140">**NULL** is not a valid value for this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1cae6-141">*Filter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1cae6-141">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cae6-142">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1cae6-142">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1cae6-143">Eine Kombination aus einem oder mehreren [D3DX- \_ Filtern](d3dx-filter.md) , die Steuern, wie das Bild gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="1cae6-143">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="1cae6-144">Die Angabe \_ von D3DX default für diesen Parameter entspricht der Angabe von D3DX \_ Filter \_ Dreieck \| D3DX \_ Filter \_ Dither.</span><span class="sxs-lookup"><span data-stu-id="1cae6-144">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="1cae6-145">*Colorkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1cae6-145">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cae6-146">Typ: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="1cae6-146">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="1cae6-147">[**D3DCOLOR**](d3dcolor.md) -Wert, der durch transparente schwarze ersetzt werden soll, oder 0, um den Colorkey zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="1cae6-147">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="1cae6-148">Dabei handelt es sich immer um eine 32-Bit-ARGB-Farbe, die unabhängig vom Quell Bildformat ist.</span><span class="sxs-lookup"><span data-stu-id="1cae6-148">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="1cae6-149">Alpha ist signifikant und sollte normalerweise für nicht transparente Farbtasten auf FF festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1cae6-149">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="1cae6-150">Daher wäre der Wert für den Wert "0xFF000000" gleich.</span><span class="sxs-lookup"><span data-stu-id="1cae6-150">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cae6-151">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1cae6-151">Return value</span></span>

<span data-ttu-id="1cae6-152">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1cae6-152">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1cae6-153">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1cae6-153">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1cae6-154">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="1cae6-154">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cae6-155">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1cae6-155">Remarks</span></span>

<span data-ttu-id="1cae6-156">Das Schreiben auf eine Oberfläche ohne Ebene der volumetextur bewirkt nicht, dass das geänderte Rechteck aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="1cae6-156">Writing to a non-level-zero surface of the volume texture will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="1cae6-157">Wenn **D3DXLoadVolumeFromMemory** aufgerufen wird und die Textur nicht bereits geändert wurde (Dies ist unwahrscheinlich in normalen Verwendungs Szenarien), muss die Anwendung [**IDirect3DVolumeTexture9:: adddirtybox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) explizit auf der volumetextur aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1cae6-157">If **D3DXLoadVolumeFromMemory** is called and the texture was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) on the volume texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cae6-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1cae6-158">Requirements</span></span>



| <span data-ttu-id="1cae6-159">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1cae6-159">Requirement</span></span> | <span data-ttu-id="1cae6-160">Wert</span><span class="sxs-lookup"><span data-stu-id="1cae6-160">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1cae6-161">Header</span><span class="sxs-lookup"><span data-stu-id="1cae6-161">Header</span></span><br/>  | <dl> <span data-ttu-id="1cae6-162"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cae6-162"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="1cae6-163">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1cae6-163">Library</span></span><br/> | <dl> <span data-ttu-id="1cae6-164"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1cae6-164"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="1cae6-165">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1cae6-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cae6-166">**D3DXLoadVolumeFromFile**</span><span class="sxs-lookup"><span data-stu-id="1cae6-166">**D3DXLoadVolumeFromFile**</span></span>](d3dxloadvolumefromfile.md)
</dt> <dt>

[<span data-ttu-id="1cae6-167">**D3DXLoadVolumeFromResource**</span><span class="sxs-lookup"><span data-stu-id="1cae6-167">**D3DXLoadVolumeFromResource**</span></span>](d3dxloadvolumefromresource.md)
</dt> <dt>

[<span data-ttu-id="1cae6-168">**D3DXLoadVolumeFromVolume**</span><span class="sxs-lookup"><span data-stu-id="1cae6-168">**D3DXLoadVolumeFromVolume**</span></span>](d3dxloadvolumefromvolume.md)
</dt> <dt>

[<span data-ttu-id="1cae6-169">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="1cae6-169">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
