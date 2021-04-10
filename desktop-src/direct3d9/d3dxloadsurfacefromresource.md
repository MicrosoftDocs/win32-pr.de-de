---
description: Lädt eine Oberfläche aus einer Ressource.
ms.assetid: 16d49f61-8c84-4e15-aacc-1d26099e65e0
title: D3DXLoadSurfaceFromResource-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ae802a1b7e18ce5f2b0a11c6679628ea1deb25aa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961552"
---
# <a name="d3dxloadsurfacefromresource-function"></a><span data-ttu-id="26715-103">D3DXLoadSurfaceFromResource-Funktion</span><span class="sxs-lookup"><span data-stu-id="26715-103">D3DXLoadSurfaceFromResource function</span></span>

<span data-ttu-id="26715-104">Lädt eine Oberfläche aus einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="26715-104">Loads a surface from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="26715-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="26715-105">Syntax</span></span>


```C++
HRESULT D3DXLoadSurfaceFromResource(
  _In_          LPDIRECT3DSURFACE9 pDestSurface,
  _In_    const PALETTEENTRY       *pDestPalette,
  _In_    const RECT               *pDestRect,
  _In_          HMODULE            hSrcModule,
  _In_          LPCTSTR            pSrcResource,
  _In_    const RECT               *pSrcRect,
  _In_          DWORD              Filter,
  _In_          D3DCOLOR           ColorKey,
  _Inout_       D3DXIMAGE_INFO     *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="26715-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="26715-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26715-107">*pdestsurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="26715-107">*pDestSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26715-108">Typ: **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="26715-108">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="26715-109">Zeiger auf eine [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="26715-109">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface.</span></span> <span data-ttu-id="26715-110">Gibt die Ziel Oberfläche an, die das Bild empfängt.</span><span class="sxs-lookup"><span data-stu-id="26715-110">Specifies the destination surface, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="26715-111">*pdestpalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="26715-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26715-112">Typ: **Konstanten [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="26715-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="26715-113">Zeiger auf eine [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) -Struktur, die Ziel Palette von 256 Farben oder **null**.</span><span class="sxs-lookup"><span data-stu-id="26715-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="26715-114">*pdestrect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="26715-114">*pDestRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26715-115">Typ: Konstante **[**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="26715-115">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="26715-116">Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="26715-116">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="26715-117">Gibt das Ziel Rechteck an.</span><span class="sxs-lookup"><span data-stu-id="26715-117">Specifies the destination rectangle.</span></span> <span data-ttu-id="26715-118">Legen Sie diesen Parameter auf **null** fest, um die gesamte Oberfläche anzugeben.</span><span class="sxs-lookup"><span data-stu-id="26715-118">Set this parameter to **NULL** to specify the entire surface.</span></span>

</dd> <dt>

<span data-ttu-id="26715-119">*hsrcmodule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="26715-119">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26715-120">Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="26715-120">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="26715-121">Handle für das Modul, in dem sich die Ressource befindet, oder **null** für das Modul, das dem Image zugeordnet ist, mit dem das Betriebssystem den aktuellen Prozess erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="26715-121">Handle to the module where the resource is located, or **NULL** for module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="26715-122">*psrkresource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="26715-122">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26715-123">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="26715-123">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="26715-124">Zeiger auf eine Zeichenfolge, die den Ressourcennamen angibt.</span><span class="sxs-lookup"><span data-stu-id="26715-124">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="26715-125">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="26715-125">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="26715-126">Andernfalls wird der String-Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="26715-126">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="26715-127">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="26715-127">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="26715-128">*psrcrect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="26715-128">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26715-129">Typ: Konstante **[**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="26715-129">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="26715-130">Zeiger auf eine [**Rect**](/previous-versions//dd162897(v=vs.85)) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="26715-130">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="26715-131">Gibt das Quell Rechteck an.</span><span class="sxs-lookup"><span data-stu-id="26715-131">Specifies the source rectangle.</span></span> <span data-ttu-id="26715-132">Legen Sie diesen Parameter auf **null** fest, um das gesamte Bild anzugeben.</span><span class="sxs-lookup"><span data-stu-id="26715-132">Set this parameter to **NULL** to specify the entire image.</span></span>

</dd> <dt>

<span data-ttu-id="26715-133">*Filter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="26715-133">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26715-134">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="26715-134">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="26715-135">Kombination aus einem oder mehreren [D3DX- \_ Filtern](d3dx-filter.md) , die Steuern, wie das Bild gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="26715-135">Combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="26715-136">Die Angabe \_ von D3DX default für diesen Parameter entspricht der Angabe von D3DX \_ Filter \_ Dreieck \| D3DX \_ Filter \_ Dither.</span><span class="sxs-lookup"><span data-stu-id="26715-136">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="26715-137">*Colorkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="26715-137">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26715-138">Typ: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="26715-138">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="26715-139">[**D3DCOLOR**](d3dcolor.md) -Wert, der durch transparente schwarze ersetzt werden soll, oder 0, um den Colorkey zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="26715-139">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="26715-140">Dabei handelt es sich immer um eine 32-Bit-ARGB-Farbe, die unabhängig vom Quell Bildformat ist.</span><span class="sxs-lookup"><span data-stu-id="26715-140">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="26715-141">Alpha ist signifikant und sollte in der Regel für nicht transparente Farbtasten auf FF festgelegt werden. Daher wäre der Wert für den Wert 0xFF000000 gleich.</span><span class="sxs-lookup"><span data-stu-id="26715-141">Alpha is significant and should usually be set to FF for opaque color keys Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="26715-142">*psrcinfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="26715-142">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="26715-143">Type: **[ **D3DXIMAGE \_ Info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="26715-143">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="26715-144">Ein Zeiger auf eine [**D3DXIMAGE \_ Info**](d3dximage-info.md) -Struktur, die mit einer Beschreibung der Daten in der Quell Bilddatei gefüllt werden soll, oder **null**.</span><span class="sxs-lookup"><span data-stu-id="26715-144">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26715-145">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="26715-145">Return value</span></span>

<span data-ttu-id="26715-146">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="26715-146">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="26715-147">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="26715-147">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="26715-148">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="26715-148">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="26715-149">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="26715-149">Remarks</span></span>

<span data-ttu-id="26715-150">Die Compilereinstellung bestimmt auch die Funktions Version.</span><span class="sxs-lookup"><span data-stu-id="26715-150">The compiler setting also determines the function version.</span></span> <span data-ttu-id="26715-151">Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXLoadSurfaceFromResourceW aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="26715-151">If Unicode is defined, the function call resolves to D3DXLoadSurfaceFromResourceW.</span></span> <span data-ttu-id="26715-152">Andernfalls wird der Funktions Aufruhe in D3DXLoadSurfaceFromResourceA aufgelöst, da ANSI-Zeichen folgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="26715-152">Otherwise, the function call resolves to D3DXLoadSurfaceFromResourceA because ANSI strings are being used.</span></span>

<span data-ttu-id="26715-153">Die Ressource, die geladen wird, muss den Typ RT \_ Bitmap oder RT \_ RCDATA aufweisen.</span><span class="sxs-lookup"><span data-stu-id="26715-153">The resource being loaded must be of type RT\_BITMAP or RT\_RCDATA.</span></span> <span data-ttu-id="26715-154">Der Ressourcentyp RT \_ RCDATA dient zum Laden von anderen Formaten als Bitmaps (z. b. TGA, JPG und DDS).</span><span class="sxs-lookup"><span data-stu-id="26715-154">Resource type RT\_RCDATA is used to load formats other than bitmaps (such as .tga, .jpg, and .dds).</span></span>

<span data-ttu-id="26715-155">Diese Funktion übernimmt die Konvertierung in und aus komprimierten Textur Formaten.</span><span class="sxs-lookup"><span data-stu-id="26715-155">This function handles conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="26715-156">Das Schreiben in eine Oberfläche ohne Ebene bewirkt nicht, dass das geänderte Rechteck aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="26715-156">Writing to a non-level-zero surface will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="26715-157">Wenn [**D3DXLoadSurfaceFromFile**](d3dxloadsurfacefromfile.md) aufgerufen wird und die Oberfläche nicht bereits geändert wurde (Dies ist unwahrscheinlich in normalen Verwendungs Szenarien), muss die Anwendung [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) explizit auf der-Oberfläche aufrufen.</span><span class="sxs-lookup"><span data-stu-id="26715-157">If [**D3DXLoadSurfaceFromFile**](d3dxloadsurfacefromfile.md) is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) on the surface.</span></span>

## <a name="requirements"></a><span data-ttu-id="26715-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26715-158">Requirements</span></span>



| <span data-ttu-id="26715-159">Anforderung</span><span class="sxs-lookup"><span data-stu-id="26715-159">Requirement</span></span> | <span data-ttu-id="26715-160">Wert</span><span class="sxs-lookup"><span data-stu-id="26715-160">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="26715-161">Header</span><span class="sxs-lookup"><span data-stu-id="26715-161">Header</span></span><br/>  | <dl> <span data-ttu-id="26715-162"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="26715-162"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="26715-163">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="26715-163">Library</span></span><br/> | <dl> <span data-ttu-id="26715-164"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="26715-164"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="26715-165">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26715-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26715-166">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="26715-166">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
