---
description: Lädt ein Volume aus einer Ressource.
ms.assetid: 3fa1243b-5e31-4737-8d3c-08852d6528d9
title: D3DXLoadVolumeFromResource-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9d57ce492db24ac9920662d4de5baed4650dd801
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365070"
---
# <a name="d3dxloadvolumefromresource-function"></a><span data-ttu-id="2180a-103">D3DXLoadVolumeFromResource-Funktion</span><span class="sxs-lookup"><span data-stu-id="2180a-103">D3DXLoadVolumeFromResource function</span></span>

<span data-ttu-id="2180a-104">Lädt ein Volume aus einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="2180a-104">Loads a volume from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="2180a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2180a-105">Syntax</span></span>


```C++
HRESULT D3DXLoadVolumeFromResource(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       HMODULE           hSrcModule,
  _In_       LPCSTR            pSrcResource,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey,
  _In_       D3DXIMAGE_INFO    *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="2180a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2180a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2180a-107">*pdestvolume* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2180a-107">*pDestVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2180a-108">Typ: **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="2180a-108">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="2180a-109">Zeiger auf eine [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="2180a-109">Pointer to an [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface.</span></span> <span data-ttu-id="2180a-110">Gibt das Ziel Volume an.</span><span class="sxs-lookup"><span data-stu-id="2180a-110">Specifies the destination volume.</span></span>

</dd> <dt>

<span data-ttu-id="2180a-111">*pdestpalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2180a-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2180a-112">Typ: **Konstanten [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="2180a-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="2180a-113">Zeiger auf eine [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) -Struktur, die Ziel Palette von 256 Farben oder **null**.</span><span class="sxs-lookup"><span data-stu-id="2180a-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="2180a-114">*pdestbox* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2180a-114">*pDestBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2180a-115">Typ: **Konstanten [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="2180a-115">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="2180a-116">Zeiger auf eine [**D3DBOX**](d3dbox.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="2180a-116">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="2180a-117">Gibt das Zielfeld an.</span><span class="sxs-lookup"><span data-stu-id="2180a-117">Specifies the destination box.</span></span> <span data-ttu-id="2180a-118">Legen Sie diesen Parameter auf **null** fest, um das gesamte Volume anzugeben.</span><span class="sxs-lookup"><span data-stu-id="2180a-118">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="2180a-119">*hsrcmodule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2180a-119">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2180a-120">Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2180a-120">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2180a-121">Handle für das Modul, in dem sich die Ressource befindet, oder **null** für das Modul, das dem Image zugeordnet ist, mit dem das Betriebssystem den aktuellen Prozess erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="2180a-121">Handle to the module where the resource is located, or **NULL** for module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="2180a-122">*psrkresource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2180a-122">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2180a-123">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2180a-123">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2180a-124">Ein Zeiger auf eine Zeichenfolge, die den Dateinamen des Quell Bilds angibt.</span><span class="sxs-lookup"><span data-stu-id="2180a-124">Pointer to a string that specifies the file name of the source image.</span></span> <span data-ttu-id="2180a-125">Wenn Unicode oder \_ Unicode definiert ist, ist dieser Parametertyp LPCWSTR; andernfalls lautet der Typ LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="2180a-125">If UNICODE or \_UNICODE are defined, this parameter type is LPCWSTR, otherwise, the type is LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="2180a-126">*psrcbox* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2180a-126">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2180a-127">Typ: **Konstanten [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="2180a-127">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="2180a-128">Zeiger auf eine [**D3DBOX**](d3dbox.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="2180a-128">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="2180a-129">Gibt das Quellfeld an.</span><span class="sxs-lookup"><span data-stu-id="2180a-129">Specifies the source box.</span></span> <span data-ttu-id="2180a-130">Legen Sie diesen Parameter auf **null** fest, um das gesamte Volume anzugeben.</span><span class="sxs-lookup"><span data-stu-id="2180a-130">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="2180a-131">*Filter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2180a-131">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2180a-132">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2180a-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2180a-133">Kombination aus einem oder mehreren [D3DX- \_ Filtern](d3dx-filter.md), um die Filterung des Bilds zu steuern.</span><span class="sxs-lookup"><span data-stu-id="2180a-133">Combination of one or more [D3DX\_FILTER](d3dx-filter.md), controlling how the image is filtered.</span></span> <span data-ttu-id="2180a-134">Die Angabe \_ von D3DX default für diesen Parameter entspricht der Angabe von D3DX \_ Filter \_ Dreieck \| D3DX \_ Filter \_ Dither.</span><span class="sxs-lookup"><span data-stu-id="2180a-134">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="2180a-135">*Colorkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2180a-135">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2180a-136">Typ: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="2180a-136">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="2180a-137">[**D3DCOLOR**](d3dcolor.md) -Wert, der durch transparente schwarze ersetzt werden soll, oder 0, um den Colorkey zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="2180a-137">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="2180a-138">Dabei handelt es sich immer um eine 32-Bit-ARGB-Farbe, die unabhängig vom Quell Bildformat ist.</span><span class="sxs-lookup"><span data-stu-id="2180a-138">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="2180a-139">Alpha ist signifikant und sollte normalerweise für nicht transparente Farbtasten auf FF festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="2180a-139">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="2180a-140">Daher wäre der Wert für den Wert "0xFF000000" gleich.</span><span class="sxs-lookup"><span data-stu-id="2180a-140">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="2180a-141">*psrcinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2180a-141">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2180a-142">Type: **[ **D3DXIMAGE \_ Info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="2180a-142">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="2180a-143">Ein Zeiger auf eine [**D3DXIMAGE \_ Info**](d3dximage-info.md) -Struktur, die mit einer Beschreibung der Daten in der Quell Bilddatei gefüllt werden soll, oder **null**.</span><span class="sxs-lookup"><span data-stu-id="2180a-143">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2180a-144">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2180a-144">Return value</span></span>

<span data-ttu-id="2180a-145">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2180a-145">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2180a-146">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2180a-146">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2180a-147">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="2180a-147">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="2180a-148">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2180a-148">Remarks</span></span>

<span data-ttu-id="2180a-149">Die Ressource, die geladen wird, muss eine Bitmap-Ressource (RT \_ Bitmap) sein.</span><span class="sxs-lookup"><span data-stu-id="2180a-149">The resource being loaded must be a bitmap resource(RT\_BITMAP).</span></span>

<span data-ttu-id="2180a-150">Diese Funktion übernimmt die Konvertierung in und aus komprimierten Textur Formaten.</span><span class="sxs-lookup"><span data-stu-id="2180a-150">This function handles conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="2180a-151">Das Schreiben auf eine Oberfläche ohne Ebene der volumetextur bewirkt nicht, dass das geänderte Rechteck aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="2180a-151">Writing to a non-level-zero surface of the volume texture will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="2180a-152">Wenn [**D3DXLoadVolumeFromFile**](d3dxloadvolumefromfile.md) aufgerufen wird und die Textur nicht bereits geändert wurde (Dies ist unwahrscheinlich in normalen Verwendungs Szenarien), muss die Anwendung [**IDirect3DVolumeTexture9:: adddirtybox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) explizit auf der volumetextur aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2180a-152">If [**D3DXLoadVolumeFromFile**](d3dxloadvolumefromfile.md) is called and the texture was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) on the volume texture.</span></span>

<span data-ttu-id="2180a-153">Diese Funktion unterstützt sowohl Unicode-als auch ANSI-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="2180a-153">This function supports both Unicode and ANSI strings.</span></span>

## <a name="requirements"></a><span data-ttu-id="2180a-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2180a-154">Requirements</span></span>



| <span data-ttu-id="2180a-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2180a-155">Requirement</span></span> | <span data-ttu-id="2180a-156">Wert</span><span class="sxs-lookup"><span data-stu-id="2180a-156">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2180a-157">Header</span><span class="sxs-lookup"><span data-stu-id="2180a-157">Header</span></span><br/>  | <dl> <span data-ttu-id="2180a-158"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="2180a-158"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="2180a-159">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2180a-159">Library</span></span><br/> | <dl> <span data-ttu-id="2180a-160"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2180a-160"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="2180a-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2180a-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2180a-162">**D3DXLoadVolumeFromFile**</span><span class="sxs-lookup"><span data-stu-id="2180a-162">**D3DXLoadVolumeFromFile**</span></span>](d3dxloadvolumefromfile.md)
</dt> <dt>

[<span data-ttu-id="2180a-163">**D3DXLoadVolumeFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="2180a-163">**D3DXLoadVolumeFromFileInMemory**</span></span>](d3dxloadvolumefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="2180a-164">**D3DXLoadVolumeFromMemory**</span><span class="sxs-lookup"><span data-stu-id="2180a-164">**D3DXLoadVolumeFromMemory**</span></span>](d3dxloadvolumefrommemory.md)
</dt> <dt>

[<span data-ttu-id="2180a-165">**D3DXLoadVolumeFromVolume**</span><span class="sxs-lookup"><span data-stu-id="2180a-165">**D3DXLoadVolumeFromVolume**</span></span>](d3dxloadvolumefromvolume.md)
</dt> <dt>

[<span data-ttu-id="2180a-166">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="2180a-166">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
