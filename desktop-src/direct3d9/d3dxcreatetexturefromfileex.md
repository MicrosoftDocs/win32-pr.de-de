---
description: Erstellt eine Textur aus einer Datei. Dies ist eine erweiterte Funktion als D3DXCreateTextureFromFile.
ms.assetid: 820bbd77-98af-4051-a22e-825fa4dd87d8
title: D3DXCreateTextureFromFileEx-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromFileEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f4dba1424f98389a9282fdebf9dae55c7e1601f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870104"
---
# <a name="d3dxcreatetexturefromfileex-function"></a><span data-ttu-id="c984e-104">D3DXCreateTextureFromFileEx-Funktion</span><span class="sxs-lookup"><span data-stu-id="c984e-104">D3DXCreateTextureFromFileEx function</span></span>

<span data-ttu-id="c984e-105">Erstellt eine Textur aus einer Datei.</span><span class="sxs-lookup"><span data-stu-id="c984e-105">Creates a texture from a file.</span></span> <span data-ttu-id="c984e-106">Dies ist eine erweiterte Funktion als [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md).</span><span class="sxs-lookup"><span data-stu-id="c984e-106">This is a more advanced function than [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c984e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c984e-107">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureFromFileEx(
  _In_    LPDIRECT3DDEVICE9  pDevice,
  _In_    LPCTSTR            pSrcFile,
  _In_    UINT               Width,
  _In_    UINT               Height,
  _In_    UINT               MipLevels,
  _In_    DWORD              Usage,
  _In_    D3DFORMAT          Format,
  _In_    D3DPOOL            Pool,
  _In_    DWORD              Filter,
  _In_    DWORD              MipFilter,
  _In_    D3DCOLOR           ColorKey,
  _Inout_ D3DXIMAGE_INFO     *pSrcInfo,
  _Out_   PALETTEENTRY       *pPalette,
  _Out_   LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="c984e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c984e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c984e-109">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c984e-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c984e-110">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="c984e-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="c984e-111">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das der Textur zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c984e-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="c984e-112">*psrcfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c984e-112">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c984e-113">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c984e-113">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c984e-114">Zeiger auf eine Zeichenfolge, die den Dateinamen angibt.</span><span class="sxs-lookup"><span data-stu-id="c984e-114">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="c984e-115">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="c984e-115">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="c984e-116">Andernfalls wird der String-Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="c984e-116">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="c984e-117">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="c984e-117">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="c984e-118">*Breite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c984e-118">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c984e-119">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c984e-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c984e-120">Breite in Pixel.</span><span class="sxs-lookup"><span data-stu-id="c984e-120">Width in pixels.</span></span> <span data-ttu-id="c984e-121">Wenn dieser Wert 0 (null) oder D3DX \_ Default ist, werden die Dimensionen aus der Datei entnommen und auf eine Potenz von zwei aufgerundet.</span><span class="sxs-lookup"><span data-stu-id="c984e-121">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file and rounded up to a power of two.</span></span> <span data-ttu-id="c984e-122">Wenn das Gerät eine nicht-Potenz von 2 Texturen unterstützt und [D3DX \_ Default \_ NONPOW2](other-d3dx-constants.md) angegeben ist, wird die Größe nicht gerundet.</span><span class="sxs-lookup"><span data-stu-id="c984e-122">If the device supports non-power of 2 textures and [D3DX\_DEFAULT\_NONPOW2](other-d3dx-constants.md) is specified, the size will not be rounded.</span></span>

</dd> <dt>

<span data-ttu-id="c984e-123">*Höhe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c984e-123">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c984e-124">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c984e-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c984e-125">Höhe in Pixel.</span><span class="sxs-lookup"><span data-stu-id="c984e-125">Height, in pixels.</span></span> <span data-ttu-id="c984e-126">Wenn dieser Wert 0 (null) oder D3DX \_ Default ist, werden die Dimensionen aus der Datei entnommen und auf eine Potenz von zwei aufgerundet.</span><span class="sxs-lookup"><span data-stu-id="c984e-126">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file and rounded up to a power of two.</span></span> <span data-ttu-id="c984e-127">Wenn das Gerät eine nicht-Potenz von 2 Texturen und [D3DX \_ Standard \_ NONPOW2](other-d3dx-constants.md) unterstützt, wird die Größe nicht gerundet.</span><span class="sxs-lookup"><span data-stu-id="c984e-127">If the device supports non-power of 2 textures and [D3DX\_DEFAULT\_NONPOW2](other-d3dx-constants.md) is sepcified, the size will not be rounded.</span></span>

</dd> <dt>

<span data-ttu-id="c984e-128">*Miplevels* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c984e-128">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c984e-129">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c984e-129">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c984e-130">Anzahl der angeforderten Mip-Ebenen.</span><span class="sxs-lookup"><span data-stu-id="c984e-130">Number of mip levels requested.</span></span> <span data-ttu-id="c984e-131">Wenn dieser Wert 0 (null) oder D3DX \_ Default ist, wird eine komplette MipMap-Kette erstellt.</span><span class="sxs-lookup"><span data-stu-id="c984e-131">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span> <span data-ttu-id="c984e-132">Wenn D3DX \_ from \_ File, wird die Größe genau so wie in der Datei erstellt, und der-Rückruf schlägt fehl, wenn dies gegen Gerätefunktionen verstößt.</span><span class="sxs-lookup"><span data-stu-id="c984e-132">If D3DX\_FROM\_FILE, the size will be taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="c984e-133">*Verwendung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c984e-133">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c984e-134">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c984e-134">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c984e-135">0, [**D3DUSAGE \_ renderTarget**](d3dusage.md)oder **D3DUSAGE \_ Dynamic**.</span><span class="sxs-lookup"><span data-stu-id="c984e-135">0, [**D3DUSAGE\_RENDERTARGET**](d3dusage.md), or **D3DUSAGE\_DYNAMIC**.</span></span> <span data-ttu-id="c984e-136">Wenn dieses Flag auf **D3DUSAGE \_ renderTarget** festgelegt wird, wird angegeben, dass die Oberfläche als Renderziel verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c984e-136">Setting this flag to **D3DUSAGE\_RENDERTARGET** indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="c984e-137">Die Ressource kann dann an den *pnewrendertarget* -Parameter der Methode "Setup [**target**](/windows/desktop/api) " übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="c984e-137">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="c984e-138">Wenn entweder **D3DUSAGE \_ renderTarget** oder **D3DUSAGE \_ Dynamic** angegeben ist, muss der *Pool* auf D3DPOOL Default festgelegt werden \_ , und die Anwendung sollte überprüfen, ob das Gerät diesen Vorgang durch Aufrufen von [**CheckDeviceFormat**](/windows/desktop/api)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c984e-138">If either **D3DUSAGE\_RENDERTARGET** or **D3DUSAGE\_DYNAMIC** is specified, *Pool* must be set to D3DPOOL\_DEFAULT, and the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="c984e-139">**D3DUSAGE \_ Dynamic** gibt an, dass die Oberfläche dynamisch behandelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c984e-139">**D3DUSAGE\_DYNAMIC** indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="c984e-140">Siehe [Verwenden dynamischer Texturen](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="c984e-140">See [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="c984e-141">*Format* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c984e-141">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c984e-142">Typ: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="c984e-142">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="c984e-143">Member des [D3DFORMAT](d3dformat.md) -Enumerationstyps, der das angeforderte Pixel Format für die Textur beschreibt.</span><span class="sxs-lookup"><span data-stu-id="c984e-143">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="c984e-144">Die zurückgegebene Textur kann ein anderes Format aufweisen als das, das durch das *Format* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c984e-144">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="c984e-145">Anwendungen sollten das Format der zurückgegebenen Textur überprüfen.</span><span class="sxs-lookup"><span data-stu-id="c984e-145">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="c984e-146">Wenn D3DFMT \_ Unknown ist, wird das Format aus der Datei entnommen.</span><span class="sxs-lookup"><span data-stu-id="c984e-146">If D3DFMT\_UNKNOWN, the format is taken from the file.</span></span> <span data-ttu-id="c984e-147">Wenn D3DFMT \_ from \_ File ist, wird das Format genau wie in der Datei erstellt, und der-Rückruf schlägt fehl, wenn dies die Gerätefunktionen verletzt.</span><span class="sxs-lookup"><span data-stu-id="c984e-147">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="c984e-148">*Pool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c984e-148">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c984e-149">Typ: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="c984e-149">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="c984e-150">Member des [**D3DPOOL**](./d3dpool.md) -Enumerationstyps, der die Speicher Klasse beschreibt, in der die Textur platziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c984e-150">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="c984e-151">*Filter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c984e-151">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c984e-152">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c984e-152">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c984e-153">Eine Kombination aus einer oder mehreren [D3DX \_ Filter](d3dx-filter.md) -Konstanten, die Steuern, wie das Bild gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="c984e-153">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) constants controlling how the image is filtered.</span></span> <span data-ttu-id="c984e-154">Die Angabe von [D3DX \_ default](other-d3dx-constants.md) für diesen Parameter entspricht der Angabe von D3DX \_ Filter \_ Dreieck \| D3DX \_ Filter \_ Dither.</span><span class="sxs-lookup"><span data-stu-id="c984e-154">Specifying [D3DX\_DEFAULT](other-d3dx-constants.md) for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="c984e-155">*MipFilter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c984e-155">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c984e-156">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c984e-156">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c984e-157">Eine Kombination aus einer oder mehreren [D3DX \_ Filter](d3dx-filter.md) -Konstanten, die Steuern, wie das Bild gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="c984e-157">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) constants controlling how the image is filtered.</span></span> <span data-ttu-id="c984e-158">Die Angabe \_ von D3DX default für diesen Parameter entspricht der Angabe von D3DX \_ Filter \_ Box.</span><span class="sxs-lookup"><span data-stu-id="c984e-158">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="c984e-159">Verwenden Sie außerdem Bits 27-31, um die Anzahl der MIP-Ebenen anzugeben, die (vom oberen Rand der MipMap-Kette) übersprungen werden sollen, wenn eine DDS-Textur in den Arbeitsspeicher geladen wird. Dies ermöglicht es Ihnen, bis zu 32 Ebenen zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="c984e-159">In addition, use bits 27-31 to specify the number of mip levels to be skipped (from the top of the mipmap chain) when a .dds texture is loaded into memory; this allows you to skip up to 32 levels.</span></span>

</dd> <dt>

<span data-ttu-id="c984e-160">*Colorkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c984e-160">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c984e-161">Typ: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="c984e-161">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="c984e-162">[**D3DCOLOR**](d3dcolor.md) -Wert, der durch transparente schwarze ersetzt werden soll, oder 0, um den Farbschlüssel zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="c984e-162">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the color key.</span></span> <span data-ttu-id="c984e-163">Dabei handelt es sich immer um eine 32-Bit-ARGB-Farbe, die unabhängig vom Quell Bildformat ist.</span><span class="sxs-lookup"><span data-stu-id="c984e-163">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="c984e-164">Alpha ist signifikant und sollte normalerweise für nicht transparente Farbtasten auf FF festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c984e-164">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="c984e-165">Daher wäre der Wert für den Wert "0xFF000000" gleich.</span><span class="sxs-lookup"><span data-stu-id="c984e-165">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="c984e-166">*psrcinfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c984e-166">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c984e-167">Type: **[ **D3DXIMAGE \_ Info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="c984e-167">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="c984e-168">Ein Zeiger auf eine [**D3DXIMAGE \_ Info**](d3dximage-info.md) -Struktur, die mit einer Beschreibung der Daten in der Quell Bilddatei ausgefüllt werden soll, oder **null**.</span><span class="sxs-lookup"><span data-stu-id="c984e-168">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled in with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c984e-169">*pPalette* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c984e-169">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c984e-170">Typ: **[ **PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="c984e-170">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="c984e-171">Zeiger auf eine [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) -Struktur, die eine zu füllende 256-Farbpalette darstellt, oder **null**.</span><span class="sxs-lookup"><span data-stu-id="c984e-171">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c984e-172">*pptexture* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c984e-172">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c984e-173">Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="c984e-173">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="c984e-174">Adresse eines Zeigers auf eine [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Schnittstelle, die das erstellte Textur Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="c984e-174">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c984e-175">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c984e-175">Return value</span></span>

<span data-ttu-id="c984e-176">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c984e-176">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c984e-177">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c984e-177">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c984e-178">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcallable, D3DERR \_ NotAvailable, D3DERR \_ oudefvideomemory, D3DXERR \_ InvalidData, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="c984e-178">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="c984e-179">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c984e-179">Remarks</span></span>

<span data-ttu-id="c984e-180">Die Compilereinstellung bestimmt auch die Funktions Version.</span><span class="sxs-lookup"><span data-stu-id="c984e-180">The compiler setting also determines the function version.</span></span> <span data-ttu-id="c984e-181">Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXCreateTextureFromFileExW aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="c984e-181">If Unicode is defined, the function call resolves to D3DXCreateTextureFromFileExW.</span></span> <span data-ttu-id="c984e-182">Andernfalls wird der Funktions Aufruhe in D3DXCreateTextureFromFileExA aufgelöst, da ANSI-Zeichen folgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c984e-182">Otherwise, the function call resolves to D3DXCreateTextureFromFileExA because ANSI strings are being used.</span></span>

<span data-ttu-id="c984e-183">Verwenden Sie [**D3DXCheckTextureRequirements**](d3dxchecktexturerequirements.md) , um zu bestimmen, ob das Gerät die Textur unter Berücksichtigung des aktuellen Zustands unterstützen kann.</span><span class="sxs-lookup"><span data-stu-id="c984e-183">Use [**D3DXCheckTextureRequirements**](d3dxchecktexturerequirements.md) to determine if your device can support the texture given the current state.</span></span>

<span data-ttu-id="c984e-184">Diese Funktion unterstützt die folgenden Dateiformate: BMP,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm und. TGA.</span><span class="sxs-lookup"><span data-stu-id="c984e-184">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="c984e-185">Siehe [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="c984e-185">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="c984e-186">Für mipzugeordnete Texturen ist jede Ebene automatisch mit der geladenen Textur gefüllt.</span><span class="sxs-lookup"><span data-stu-id="c984e-186">Mipmapped textures automatically have each level filled with the loaded texture.</span></span> <span data-ttu-id="c984e-187">Beim Laden von Bildern in mipzugeordnete Texturen können einige Geräte nicht zu einem 1 x1-Bild wechseln, und diese Funktion schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="c984e-187">When loading images into mipmapped textures, some devices are unable to go to a 1x1 image and this function will fail.</span></span> <span data-ttu-id="c984e-188">Wenn dies der Fall ist, müssen die Images manuell geladen werden.</span><span class="sxs-lookup"><span data-stu-id="c984e-188">If this happens, then the images need to be loaded manually.</span></span>

<span data-ttu-id="c984e-189">Optimale Leistung bei der Verwendung von **D3DXCreateTextureFromFileEx**:</span><span class="sxs-lookup"><span data-stu-id="c984e-189">For the best performance when using **D3DXCreateTextureFromFileEx**:</span></span>

1.  <span data-ttu-id="c984e-190">Die Bildskalierung und die Formatkonvertierung zur Ladezeit können langsam sein.</span><span class="sxs-lookup"><span data-stu-id="c984e-190">Doing image scaling and format conversion at load time can be slow.</span></span> <span data-ttu-id="c984e-191">Speichern Sie Images im Format und in der Lösung, die Sie verwenden werden.</span><span class="sxs-lookup"><span data-stu-id="c984e-191">Store images in the format and resolution they will be used.</span></span> <span data-ttu-id="c984e-192">Wenn die Zielhardware eine Potenz von 2 Dimensionen erfordert, erstellen und speichern Sie Images mit zwei Dimensionen.</span><span class="sxs-lookup"><span data-stu-id="c984e-192">If the target hardware requires power of 2 dimensions, then create and store images using power of 2 dimensions.</span></span>
2.  <span data-ttu-id="c984e-193">Filtern Sie zum Erstellen von MipMap-Bildern zur Ladezeit mithilfe des [D3DX \_ Filter \_ ](d3dx-filter.md)Felds.</span><span class="sxs-lookup"><span data-stu-id="c984e-193">For mipmap image creation at load time, filter using [D3DX\_FILTER\_BOX](d3dx-filter.md).</span></span> <span data-ttu-id="c984e-194">Ein Feld Filter ist viel schneller als andere Filtertypen, z \_ . b. D3DX Filter \_ Dreieck.</span><span class="sxs-lookup"><span data-stu-id="c984e-194">A box filter is much faster than other filter types such as D3DX\_FILTER\_TRIANGLE.</span></span>
3.  <span data-ttu-id="c984e-195">Verwenden Sie ggf. DDS-Dateien.</span><span class="sxs-lookup"><span data-stu-id="c984e-195">Consider using DDS files.</span></span> <span data-ttu-id="c984e-196">Da DDS-Dateien verwendet werden können, um ein beliebiges Direct3D 9-Textur Format darzustellen, sind Sie für D3DX sehr leicht lesbar.</span><span class="sxs-lookup"><span data-stu-id="c984e-196">Since DDS files can be used to represent any Direct3D 9 texture format, they are very easy for D3DX to read.</span></span> <span data-ttu-id="c984e-197">Außerdem können Sie MipMaps speichern, sodass alle MipMap-Generierungs Algorithmen zum Erstellen der Images verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="c984e-197">Also, they can store mipmaps, so any mipmap-generation algorithms can be used to author the images.</span></span>

<span data-ttu-id="c984e-198">Wenn Sie MipMap-Ebenen beim Laden einer DDS-Datei überspringen, verwenden \_ Sie das Makro D3DX Skip \_ DDS \_ MIP \_ Levels, um den MipFilter-Wert zu generieren.</span><span class="sxs-lookup"><span data-stu-id="c984e-198">When skipping mipmap levels while loading a .dds file, use the D3DX\_SKIP\_DDS\_MIP\_LEVELS macro to generate the MipFilter value.</span></span> <span data-ttu-id="c984e-199">Dieses Makro nimmt die Anzahl der zu über springenden Ebenen und den Filtertyp an und gibt den Filter Wert zurück, der dann an den MipFilter-Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="c984e-199">This macro takes the number of levels to skip and the filter type and returns the filter value, which would then be passed into the MipFilter parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="c984e-200">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c984e-200">Requirements</span></span>



| <span data-ttu-id="c984e-201">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c984e-201">Requirement</span></span> | <span data-ttu-id="c984e-202">Wert</span><span class="sxs-lookup"><span data-stu-id="c984e-202">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c984e-203">Header</span><span class="sxs-lookup"><span data-stu-id="c984e-203">Header</span></span><br/>  | <dl> <span data-ttu-id="c984e-204"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="c984e-204"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="c984e-205">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c984e-205">Library</span></span><br/> | <dl> <span data-ttu-id="c984e-206"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c984e-206"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="c984e-207">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c984e-207">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c984e-208">**D3DXCreateTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="c984e-208">**D3DXCreateTextureFromFile**</span></span>](d3dxcreatetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="c984e-209">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="c984e-209">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
