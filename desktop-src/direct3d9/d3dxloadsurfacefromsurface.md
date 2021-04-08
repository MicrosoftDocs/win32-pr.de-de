---
description: Lädt eine Oberfläche von einer anderen Oberfläche mit Farbkonvertierung.
ms.assetid: eddb420d-fd32-4c09-afec-435887c4e905
title: D3DXLoadSurfaceFromSurface-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromSurface
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7b5138ddf540c3e4a87fe65f29938cb3557b2360
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762186"
---
# <a name="d3dxloadsurfacefromsurface-function"></a><span data-ttu-id="23a89-103">D3DXLoadSurfaceFromSurface-Funktion</span><span class="sxs-lookup"><span data-stu-id="23a89-103">D3DXLoadSurfaceFromSurface function</span></span>

<span data-ttu-id="23a89-104">Lädt eine Oberfläche von einer anderen Oberfläche mit Farbkonvertierung.</span><span class="sxs-lookup"><span data-stu-id="23a89-104">Loads a surface from another surface with color conversion.</span></span>

## <a name="syntax"></a><span data-ttu-id="23a89-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="23a89-105">Syntax</span></span>


```C++
HRESULT D3DXLoadSurfaceFromSurface(
  _In_       LPDIRECT3DSURFACE9 pDestSurface,
  _In_ const PALETTEENTRY       *pDestPalette,
  _In_ const RECT               *pDestRect,
  _In_       LPDIRECT3DSURFACE9 pSrcSurface,
  _In_ const PALETTEENTRY       *pSrcPalette,
  _In_ const RECT               *pSrcRect,
  _In_       DWORD              Filter,
  _In_       D3DCOLOR           ColorKey
);
```



## <a name="parameters"></a><span data-ttu-id="23a89-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="23a89-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23a89-107">*pdestsurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="23a89-107">*pDestSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23a89-108">Typ: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="23a89-108">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="23a89-109">Zeiger auf eine [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="23a89-109">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface.</span></span> <span data-ttu-id="23a89-110">Gibt die Ziel Oberfläche an, die das Bild empfängt.</span><span class="sxs-lookup"><span data-stu-id="23a89-110">Specifies the destination surface, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="23a89-111">*pdestpalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="23a89-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23a89-112">Typ: **Konstanten [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="23a89-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="23a89-113">Zeiger auf eine [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) -Struktur, die Ziel Palette von 256 Farben oder **null**.</span><span class="sxs-lookup"><span data-stu-id="23a89-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="23a89-114">*pdestrect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="23a89-114">*pDestRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23a89-115">Typ: Konstante **[**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="23a89-115">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="23a89-116">Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="23a89-116">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="23a89-117">Gibt das Ziel Rechteck an.</span><span class="sxs-lookup"><span data-stu-id="23a89-117">Specifies the destination rectangle.</span></span> <span data-ttu-id="23a89-118">Legen Sie diesen Parameter auf **null** fest, um die gesamte Oberfläche anzugeben.</span><span class="sxs-lookup"><span data-stu-id="23a89-118">Set this parameter to **NULL** to specify the entire surface.</span></span>

</dd> <dt>

<span data-ttu-id="23a89-119">*psrcsurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="23a89-119">*pSrcSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23a89-120">Typ: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="23a89-120">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="23a89-121">Zeiger auf eine [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) -Schnittstelle, die die Quell Oberfläche darstellt.</span><span class="sxs-lookup"><span data-stu-id="23a89-121">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface, representing the source surface.</span></span>

</dd> <dt>

<span data-ttu-id="23a89-122">*psrcpalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="23a89-122">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23a89-123">Typ: **Konstanten [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="23a89-123">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="23a89-124">Zeiger auf eine [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) -Struktur, die Quell Palette von 256 Farben oder **null**.</span><span class="sxs-lookup"><span data-stu-id="23a89-124">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the source palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="23a89-125">*psrcrect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="23a89-125">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23a89-126">Typ: Konstante **[**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="23a89-126">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="23a89-127">Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="23a89-127">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="23a89-128">Gibt das Quell Rechteck an.</span><span class="sxs-lookup"><span data-stu-id="23a89-128">Specifies the source rectangle.</span></span> <span data-ttu-id="23a89-129">Legen Sie diesen Parameter auf **null** fest, um die gesamte Oberfläche anzugeben.</span><span class="sxs-lookup"><span data-stu-id="23a89-129">Set this parameter to **NULL** to specify the entire surface.</span></span>

</dd> <dt>

<span data-ttu-id="23a89-130">*Filter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="23a89-130">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23a89-131">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="23a89-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="23a89-132">Eine Kombination aus einem oder mehreren [D3DX- \_ Filtern](d3dx-filter.md), die steuert, wie das Bild gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="23a89-132">A combination of one or more [D3DX\_FILTER](d3dx-filter.md), controlling how the image is filtered.</span></span> <span data-ttu-id="23a89-133">Die Angabe \_ von D3DX default für diesen Parameter entspricht der Angabe von D3DX \_ Filter \_ Dreieck \| D3DX \_ Filter \_ Dither.</span><span class="sxs-lookup"><span data-stu-id="23a89-133">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="23a89-134">*Colorkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="23a89-134">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23a89-135">Typ: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="23a89-135">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="23a89-136">[**D3DCOLOR**](d3dcolor.md) -Wert, der durch transparente schwarze ersetzt werden soll, oder 0, um den Colorkey zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="23a89-136">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="23a89-137">Dabei handelt es sich immer um eine 32-Bit-ARGB-Farbe, die unabhängig vom Quell Bildformat ist.</span><span class="sxs-lookup"><span data-stu-id="23a89-137">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="23a89-138">Alpha ist signifikant und sollte normalerweise für nicht transparente Farbtasten auf FF festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="23a89-138">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="23a89-139">Daher wäre der Wert für den Wert "0xFF000000" gleich.</span><span class="sxs-lookup"><span data-stu-id="23a89-139">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23a89-140">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="23a89-140">Return value</span></span>

<span data-ttu-id="23a89-141">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="23a89-141">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="23a89-142">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="23a89-142">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="23a89-143">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="23a89-143">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="23a89-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="23a89-144">Remarks</span></span>

<span data-ttu-id="23a89-145">Diese Funktion übernimmt die Konvertierung in und aus komprimierten Textur Formaten.</span><span class="sxs-lookup"><span data-stu-id="23a89-145">This function handles conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="23a89-146">Das Schreiben in eine Oberfläche ohne Ebene bewirkt nicht, dass das geänderte Rechteck aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="23a89-146">Writing to a non-level-zero surface will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="23a89-147">Wenn **D3DXLoadSurfaceFromSurface** aufgerufen wird und die Oberfläche nicht bereits geändert wurde (Dies ist unwahrscheinlich in normalen Verwendungs Szenarien), muss die Anwendung [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) explizit auf der-Oberfläche aufrufen.</span><span class="sxs-lookup"><span data-stu-id="23a89-147">If **D3DXLoadSurfaceFromSurface** is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) on the surface.</span></span>

## <a name="requirements"></a><span data-ttu-id="23a89-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="23a89-148">Requirements</span></span>



| <span data-ttu-id="23a89-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="23a89-149">Requirement</span></span> | <span data-ttu-id="23a89-150">Wert</span><span class="sxs-lookup"><span data-stu-id="23a89-150">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="23a89-151">Header</span><span class="sxs-lookup"><span data-stu-id="23a89-151">Header</span></span><br/>  | <dl> <span data-ttu-id="23a89-152"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="23a89-152"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="23a89-153">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="23a89-153">Library</span></span><br/> | <dl> <span data-ttu-id="23a89-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="23a89-154"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="23a89-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="23a89-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23a89-156">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="23a89-156">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
