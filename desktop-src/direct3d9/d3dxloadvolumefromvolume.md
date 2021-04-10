---
description: Lädt ein Volume von einem anderen Volume.
ms.assetid: bc162f91-feb7-4571-ae4a-abaa5e7953f6
title: D3DXLoadVolumeFromVolume-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromVolume
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: da2cedf42533fa1d170269e97a366f7e4a1a41f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961696"
---
# <a name="d3dxloadvolumefromvolume-function"></a><span data-ttu-id="a00e2-103">D3DXLoadVolumeFromVolume-Funktion</span><span class="sxs-lookup"><span data-stu-id="a00e2-103">D3DXLoadVolumeFromVolume function</span></span>

<span data-ttu-id="a00e2-104">Lädt ein Volume von einem anderen Volume.</span><span class="sxs-lookup"><span data-stu-id="a00e2-104">Loads a volume from another volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="a00e2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a00e2-105">Syntax</span></span>


```C++
HRESULT D3DXLoadVolumeFromVolume(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       LPDIRECT3DVOLUME9 pSrcVolume,
  _In_ const PALETTEENTRY      *pSrcPalette,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey
);
```



## <a name="parameters"></a><span data-ttu-id="a00e2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a00e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a00e2-107">*pdestvolume* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a00e2-107">*pDestVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a00e2-108">Typ: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="a00e2-108">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="a00e2-109">Zeiger auf eine [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="a00e2-109">Pointer to an [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface.</span></span> <span data-ttu-id="a00e2-110">Gibt das Ziel Volume an, das das Abbild empfängt.</span><span class="sxs-lookup"><span data-stu-id="a00e2-110">Specifies the destination volume, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="a00e2-111">*pdestpalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a00e2-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a00e2-112">Typ: **Konstanten [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="a00e2-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="a00e2-113">Zeiger auf eine [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) -Struktur, die Ziel Palette von 256 Farben oder **null**.</span><span class="sxs-lookup"><span data-stu-id="a00e2-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a00e2-114">*pdestbox* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a00e2-114">*pDestBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a00e2-115">Typ: **Konstanten [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="a00e2-115">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="a00e2-116">Zeiger auf eine [**D3DBOX**](d3dbox.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="a00e2-116">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="a00e2-117">Gibt das Zielfeld an.</span><span class="sxs-lookup"><span data-stu-id="a00e2-117">Specifies the destination box.</span></span> <span data-ttu-id="a00e2-118">Legen Sie diesen Parameter auf **null** fest, um das gesamte Volume anzugeben.</span><span class="sxs-lookup"><span data-stu-id="a00e2-118">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="a00e2-119">*psrcvolume* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a00e2-119">*pSrcVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a00e2-120">Typ: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="a00e2-120">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="a00e2-121">Ein Zeiger auf eine [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="a00e2-121">A Pointer to an [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface.</span></span> <span data-ttu-id="a00e2-122">Gibt das Quell Volume an.</span><span class="sxs-lookup"><span data-stu-id="a00e2-122">Specifies the source volume.</span></span>

</dd> <dt>

<span data-ttu-id="a00e2-123">*psrcpalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a00e2-123">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a00e2-124">Typ: **Konstanten [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="a00e2-124">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="a00e2-125">Zeiger auf eine [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) -Struktur, die Quell Palette von 256 Farben oder **null**.</span><span class="sxs-lookup"><span data-stu-id="a00e2-125">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the source palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a00e2-126">*psrcbox* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a00e2-126">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a00e2-127">Typ: **Konstanten [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="a00e2-127">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="a00e2-128">Zeiger auf eine [**D3DBOX**](d3dbox.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="a00e2-128">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="a00e2-129">Gibt das Quellfeld an.</span><span class="sxs-lookup"><span data-stu-id="a00e2-129">Specifies the source box.</span></span> <span data-ttu-id="a00e2-130">Legen Sie diesen Parameter auf **null** fest, um das gesamte Volume anzugeben.</span><span class="sxs-lookup"><span data-stu-id="a00e2-130">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="a00e2-131">*Filter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a00e2-131">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a00e2-132">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a00e2-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a00e2-133">Eine Kombination aus einem oder mehreren [D3DX- \_ Filtern](d3dx-filter.md), die steuert, wie das Bild gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="a00e2-133">A combination of one or more [D3DX\_FILTER](d3dx-filter.md), controlling how the image is filtered.</span></span> <span data-ttu-id="a00e2-134">Die Angabe \_ von D3DX default für diesen Parameter entspricht der Angabe von D3DX \_ Filter \_ Dreieck \| D3DX \_ Filter \_ Dither.</span><span class="sxs-lookup"><span data-stu-id="a00e2-134">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="a00e2-135">*Colorkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a00e2-135">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a00e2-136">Typ: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="a00e2-136">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="a00e2-137">[**D3DCOLOR**](d3dcolor.md) -Wert, der durch transparente schwarze ersetzt werden soll, oder 0, um den Colorkey zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="a00e2-137">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="a00e2-138">Dabei handelt es sich immer um eine 32-Bit-ARGB-Farbe, die unabhängig vom Quell Bildformat ist.</span><span class="sxs-lookup"><span data-stu-id="a00e2-138">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="a00e2-139">Alpha ist signifikant und sollte normalerweise für nicht transparente Farbtasten auf FF festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a00e2-139">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="a00e2-140">Daher wäre der Wert für den Wert "0xFF000000" gleich.</span><span class="sxs-lookup"><span data-stu-id="a00e2-140">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a00e2-141">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a00e2-141">Return value</span></span>

<span data-ttu-id="a00e2-142">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a00e2-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a00e2-143">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a00e2-143">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a00e2-144">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="a00e2-144">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="a00e2-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a00e2-145">Remarks</span></span>

<span data-ttu-id="a00e2-146">Das Schreiben auf eine Oberfläche ohne Ebene der volumetextur bewirkt nicht, dass das geänderte Rechteck aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="a00e2-146">Writing to a non-level-zero surface of the volume texture will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="a00e2-147">Wenn **D3DXLoadVolumeFromVolume** aufgerufen wird und die Oberfläche nicht bereits geändert wurde (Dies ist unwahrscheinlich in normalen Verwendungs Szenarien), muss die Anwendung [**IDirect3DVolumeTexture9:: adddirtybox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) explizit auf der-Oberfläche aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a00e2-147">If **D3DXLoadVolumeFromVolume** is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) on the surface.</span></span>

## <a name="requirements"></a><span data-ttu-id="a00e2-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a00e2-148">Requirements</span></span>



| <span data-ttu-id="a00e2-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a00e2-149">Requirement</span></span> | <span data-ttu-id="a00e2-150">Wert</span><span class="sxs-lookup"><span data-stu-id="a00e2-150">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a00e2-151">Header</span><span class="sxs-lookup"><span data-stu-id="a00e2-151">Header</span></span><br/>  | <dl> <span data-ttu-id="a00e2-152"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="a00e2-152"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="a00e2-153">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a00e2-153">Library</span></span><br/> | <dl> <span data-ttu-id="a00e2-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a00e2-154"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="a00e2-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a00e2-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a00e2-156">**D3DXLoadVolumeFromFile**</span><span class="sxs-lookup"><span data-stu-id="a00e2-156">**D3DXLoadVolumeFromFile**</span></span>](d3dxloadvolumefromfile.md)
</dt> <dt>

[<span data-ttu-id="a00e2-157">**D3DXLoadVolumeFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="a00e2-157">**D3DXLoadVolumeFromFileInMemory**</span></span>](d3dxloadvolumefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="a00e2-158">**D3DXLoadVolumeFromMemory**</span><span class="sxs-lookup"><span data-stu-id="a00e2-158">**D3DXLoadVolumeFromMemory**</span></span>](d3dxloadvolumefrommemory.md)
</dt> <dt>

[<span data-ttu-id="a00e2-159">**D3DXLoadVolumeFromResource**</span><span class="sxs-lookup"><span data-stu-id="a00e2-159">**D3DXLoadVolumeFromResource**</span></span>](d3dxloadvolumefromresource.md)
</dt> <dt>

[<span data-ttu-id="a00e2-160">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="a00e2-160">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
