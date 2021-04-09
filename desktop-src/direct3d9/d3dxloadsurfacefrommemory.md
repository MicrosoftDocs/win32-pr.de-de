---
description: Lädt eine Oberfläche aus dem Arbeitsspeicher.
ms.assetid: 9a36e395-fd00-47fe-8df1-cda8c80182ef
title: D3DXLoadSurfaceFromMemory-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ffb7be05301ae807505242153be902ab30eecf14
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050836"
---
# <a name="d3dxloadsurfacefrommemory-function"></a><span data-ttu-id="38369-103">D3DXLoadSurfaceFromMemory-Funktion</span><span class="sxs-lookup"><span data-stu-id="38369-103">D3DXLoadSurfaceFromMemory function</span></span>

<span data-ttu-id="38369-104">Lädt eine Oberfläche aus dem Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="38369-104">Loads a surface from memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="38369-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="38369-105">Syntax</span></span>


```C++
HRESULT D3DXLoadSurfaceFromMemory(
  _In_       LPDIRECT3DSURFACE9 pDestSurface,
  _In_ const PALETTEENTRY       *pDestPalette,
  _In_ const RECT               *pDestRect,
  _In_       LPCVOID            pSrcMemory,
  _In_       D3DFORMAT          SrcFormat,
  _In_       UINT               SrcPitch,
  _In_ const PALETTEENTRY       *pSrcPalette,
  _In_ const RECT               *pSrcRect,
  _In_       DWORD              Filter,
  _In_       D3DCOLOR           ColorKey
);
```



## <a name="parameters"></a><span data-ttu-id="38369-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="38369-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38369-107">*pdestsurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38369-107">*pDestSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38369-108">Typ: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="38369-108">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="38369-109">Zeiger auf eine [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="38369-109">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface.</span></span> <span data-ttu-id="38369-110">Gibt die Ziel Oberfläche an, die das Bild empfängt.</span><span class="sxs-lookup"><span data-stu-id="38369-110">Specifies the destination surface, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="38369-111">*pdestpalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38369-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38369-112">Typ: **Konstanten [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="38369-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="38369-113">Zeiger auf eine [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) -Struktur, die Ziel Palette von 256 Farben oder **null**.</span><span class="sxs-lookup"><span data-stu-id="38369-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="38369-114">*pdestrect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38369-114">*pDestRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38369-115">Typ: Konstante **[**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="38369-115">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="38369-116">Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="38369-116">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="38369-117">Gibt das Ziel Rechteck an.</span><span class="sxs-lookup"><span data-stu-id="38369-117">Specifies the destination rectangle.</span></span> <span data-ttu-id="38369-118">Legen Sie diesen Parameter auf **null** fest, um die gesamte Oberfläche anzugeben.</span><span class="sxs-lookup"><span data-stu-id="38369-118">Set this parameter to **NULL** to specify the entire surface.</span></span>

</dd> <dt>

<span data-ttu-id="38369-119">*psrcmemory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38369-119">*pSrcMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38369-120">Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="38369-120">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="38369-121">Ein Zeiger auf die linke obere Ecke des Quell Bilds im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="38369-121">Pointer to the upper left corner of the source image in memory.</span></span>

</dd> <dt>

<span data-ttu-id="38369-122">*Srcformat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38369-122">*SrcFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38369-123">Typ: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="38369-123">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="38369-124">Member des [D3DFORMAT](d3dformat.md) -Enumerationstyps, das Pixel Format des Quell Bilds.</span><span class="sxs-lookup"><span data-stu-id="38369-124">Member of the [D3DFORMAT](d3dformat.md) enumerated type, the pixel format of the source image.</span></span>

</dd> <dt>

<span data-ttu-id="38369-125">*Srcpitch* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38369-125">*SrcPitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38369-126">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="38369-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="38369-127">Die Darstellung des Quell Bilds in Bytes.</span><span class="sxs-lookup"><span data-stu-id="38369-127">Pitch of source image, in bytes.</span></span> <span data-ttu-id="38369-128">Bei DXT-Formaten sollte diese Zahl die Breite einer Zellen Zelle in Bytes darstellen.</span><span class="sxs-lookup"><span data-stu-id="38369-128">For DXT formats, this number should represent the width of one row of cells, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="38369-129">*psrcpalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38369-129">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38369-130">Typ: **Konstanten [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="38369-130">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="38369-131">Zeiger auf eine [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) -Struktur, die Quell Palette von 256 Farben oder **null**.</span><span class="sxs-lookup"><span data-stu-id="38369-131">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the source palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="38369-132">*psrcrect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38369-132">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38369-133">Typ: Konstante **[**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="38369-133">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="38369-134">Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="38369-134">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="38369-135">Gibt die Dimensionen des Quell Bilds im Arbeitsspeicher an.</span><span class="sxs-lookup"><span data-stu-id="38369-135">Specifies the dimensions of the source image in memory.</span></span> <span data-ttu-id="38369-136">Dieser Wert darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="38369-136">This value cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="38369-137">*Filter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38369-137">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38369-138">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="38369-138">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="38369-139">Kombination aus einem oder mehreren [D3DX- \_ Filtern](d3dx-filter.md) , die Steuern, wie das Bild gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="38369-139">Combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="38369-140">Die Angabe \_ von D3DX default für diesen Parameter entspricht der Angabe von D3DX \_ Filter \_ Dreieck \| D3DX \_ Filter \_ Dither.</span><span class="sxs-lookup"><span data-stu-id="38369-140">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="38369-141">*Colorkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38369-141">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38369-142">Typ: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="38369-142">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="38369-143">[**D3DCOLOR**](d3dcolor.md) -Wert, der durch transparente schwarze ersetzt werden soll, oder 0, um den Colorkey zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="38369-143">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="38369-144">Dabei handelt es sich immer um eine 32-Bit-ARGB-Farbe, die unabhängig vom Quell Bildformat ist.</span><span class="sxs-lookup"><span data-stu-id="38369-144">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="38369-145">Alpha ist signifikant und sollte normalerweise für nicht transparente Farbtasten auf FF festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="38369-145">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="38369-146">Daher wäre der Wert für den Wert "0xFF000000" gleich.</span><span class="sxs-lookup"><span data-stu-id="38369-146">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38369-147">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="38369-147">Return value</span></span>

<span data-ttu-id="38369-148">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="38369-148">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="38369-149">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="38369-149">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="38369-150">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="38369-150">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="38369-151">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="38369-151">Remarks</span></span>

<span data-ttu-id="38369-152">Diese Funktion übernimmt die Konvertierung in und aus komprimierten Textur Formaten.</span><span class="sxs-lookup"><span data-stu-id="38369-152">This function handles conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="38369-153">Das Schreiben in eine Oberfläche ohne Ebene bewirkt nicht, dass das geänderte Rechteck aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="38369-153">Writing to a non-level-zero surface will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="38369-154">Wenn **D3DXLoadSurfaceFromMemory** aufgerufen wird und die Oberfläche nicht bereits geändert wurde (Dies ist unwahrscheinlich in normalen Verwendungs Szenarien), muss die Anwendung [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) explizit auf der-Oberfläche aufrufen.</span><span class="sxs-lookup"><span data-stu-id="38369-154">If **D3DXLoadSurfaceFromMemory** is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) on the surface.</span></span>

## <a name="requirements"></a><span data-ttu-id="38369-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="38369-155">Requirements</span></span>



| <span data-ttu-id="38369-156">Anforderung</span><span class="sxs-lookup"><span data-stu-id="38369-156">Requirement</span></span> | <span data-ttu-id="38369-157">Wert</span><span class="sxs-lookup"><span data-stu-id="38369-157">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="38369-158">Header</span><span class="sxs-lookup"><span data-stu-id="38369-158">Header</span></span><br/>  | <dl> <span data-ttu-id="38369-159"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="38369-159"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="38369-160">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="38369-160">Library</span></span><br/> | <dl> <span data-ttu-id="38369-161"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="38369-161"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="38369-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="38369-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38369-163">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="38369-163">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
