---
description: 'D3DXCreateVolumeTextureFromFileEx-Funktion: Erstellt eine Volumetextur aus einer Datei.'
ms.assetid: fa11706a-83cc-4795-957d-6d0e1faf2a8f
title: D3DXCreateVolumeTextureFromFileEx-Funktion (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromFileEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 11be9da24be7fc9a03bab8e761e55a601715bd75
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102748"
---
# <a name="d3dxcreatevolumetexturefromfileex-function"></a><span data-ttu-id="e8c10-103">D3DXCreateVolumeTextureFromFileEx-Funktion</span><span class="sxs-lookup"><span data-stu-id="e8c10-103">D3DXCreateVolumeTextureFromFileEx function</span></span>

<span data-ttu-id="e8c10-104">Erstellt eine Volumetextur aus einer Datei.</span><span class="sxs-lookup"><span data-stu-id="e8c10-104">Creates a volume texture from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8c10-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8c10-105">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTextureFromFileEx(
  _In_    LPDIRECT3DDEVICE9        pDevice,
  _In_    LPCTSTR                  pSrcFile,
  _In_    UINT                     Width,
  _In_    UINT                     Height,
  _In_    UINT                     Depth,
  _In_    UINT                     MipLevels,
  _In_    DWORD                    Usage,
          D3DFORMAT                Format,
  _In_    D3DPOOL                  Pool,
  _In_    DWORD                    Filter,
  _In_    DWORD                    MipFilter,
  _In_    D3DCOLOR                 ColorKey,
  _Inout_ D3DXIMAGE_INFO           *pSrcInfo,
  _Out_   PALETTEENTRY             *pPalette,
  _Out_   LPDIRECT3DVOLUMETEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="e8c10-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8c10-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8c10-107">*pDevice* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="e8c10-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8c10-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="e8c10-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="e8c10-109">Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) die das Gerät darstellt, das der Textur zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e8c10-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="e8c10-110">*pSrcFile* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="e8c10-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8c10-111">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e8c10-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e8c10-112">Zeiger auf eine Zeichenfolge, die den Dateinamen angibt.</span><span class="sxs-lookup"><span data-stu-id="e8c10-112">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="e8c10-113">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="e8c10-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="e8c10-114">Andernfalls wird der Zeichenfolgendatentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="e8c10-114">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="e8c10-115">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="e8c10-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="e8c10-116">*Breite* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="e8c10-116">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8c10-117">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e8c10-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e8c10-118">Breite in Pixel.</span><span class="sxs-lookup"><span data-stu-id="e8c10-118">Width in pixels.</span></span> <span data-ttu-id="e8c10-119">Wenn dieser Wert 0 (null) oder D3DX \_ DEFAULT ist, werden die Dimensionen aus der Datei übernommen.</span><span class="sxs-lookup"><span data-stu-id="e8c10-119">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="e8c10-120">Die maximale Dimension, die ein Treiber unterstützt (für Breite, Höhe und Tiefe), finden Sie unter MaxVolumeExtent in [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)</span><span class="sxs-lookup"><span data-stu-id="e8c10-120">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="e8c10-121">*Höhe* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="e8c10-121">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8c10-122">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e8c10-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e8c10-123">Höhe in Pixel.</span><span class="sxs-lookup"><span data-stu-id="e8c10-123">Height, in pixels.</span></span> <span data-ttu-id="e8c10-124">Wenn dieser Wert 0 (null) oder D3DX \_ DEFAULT ist, werden die Dimensionen aus der Datei übernommen.</span><span class="sxs-lookup"><span data-stu-id="e8c10-124">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="e8c10-125">Die maximale Dimension, die ein Treiber unterstützt (für Breite, Höhe und Tiefe), finden Sie in MaxVolumeExtent in [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)</span><span class="sxs-lookup"><span data-stu-id="e8c10-125">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="e8c10-126">*Tiefe* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="e8c10-126">*Depth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8c10-127">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e8c10-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e8c10-128">Tiefe in Pixel.</span><span class="sxs-lookup"><span data-stu-id="e8c10-128">Depth, in pixels.</span></span> <span data-ttu-id="e8c10-129">Wenn dieser Wert 0 (null) oder D3DX \_ DEFAULT ist, werden die Dimensionen aus der Datei übernommen.</span><span class="sxs-lookup"><span data-stu-id="e8c10-129">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="e8c10-130">Die maximale Dimension, die ein Treiber unterstützt (für Breite, Höhe und Tiefe), finden Sie in MaxVolumeExtent in [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)</span><span class="sxs-lookup"><span data-stu-id="e8c10-130">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="e8c10-131">*MipLevels* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="e8c10-131">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8c10-132">Typ: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e8c10-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e8c10-133">Anzahl der angeforderten MIP-Ebenen.</span><span class="sxs-lookup"><span data-stu-id="e8c10-133">Number of mip levels requested.</span></span> <span data-ttu-id="e8c10-134">Wenn dieser Wert 0 (null) oder D3DX \_ DEFAULT ist, wird eine vollständige Mipmapkette erstellt.</span><span class="sxs-lookup"><span data-stu-id="e8c10-134">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="e8c10-135">*Verwendung* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="e8c10-135">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8c10-136">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e8c10-136">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e8c10-137">0, D3DUSAGE \_ RENDERTARGET oder D3DUSAGE \_ DYNAMIC.</span><span class="sxs-lookup"><span data-stu-id="e8c10-137">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="e8c10-138">Das Festlegen dieses Flags auf D3DUSAGE RENDERTARGET gibt an, dass die Oberfläche \_ als Renderziel verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e8c10-138">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="e8c10-139">Die Ressource kann dann an den *pNewRenderTarget-Parameter* der [**SetRenderTarget-Methode übergeben**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) werden.</span><span class="sxs-lookup"><span data-stu-id="e8c10-139">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) method.</span></span> <span data-ttu-id="e8c10-140">Wenn entweder D3DUSAGE RENDERTARGET oder D3DUSAGE DYNAMIC angegeben ist, muss Pool auf D3DPOOL DEFAULT festgelegt werden, und die Anwendung sollte überprüfen, ob das Gerät diesen Vorgang unterstützt, indem \_ \_  \_ [**CheckDeviceFormat aufruft.**](/windows/desktop/api)</span><span class="sxs-lookup"><span data-stu-id="e8c10-140">If either D3DUSAGE\_RENDERTARGET or D3DUSAGE\_DYNAMIC is specified, *Pool* must be set to D3DPOOL\_DEFAULT, and the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="e8c10-141">D3DUSAGE \_ DYNAMIC gibt an, dass die Oberfläche dynamisch behandelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e8c10-141">D3DUSAGE\_DYNAMIC indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="e8c10-142">Weitere Informationen zur Verwendung dynamischer Texturen finden Sie unter [Verwenden von dynamischen Texturen.](performance-optimizations.md)</span><span class="sxs-lookup"><span data-stu-id="e8c10-142">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="e8c10-143">*Format*</span><span class="sxs-lookup"><span data-stu-id="e8c10-143">*Format*</span></span> 
</dt> <dd>

<span data-ttu-id="e8c10-144">Typ: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="e8c10-144">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="e8c10-145">Member des [D3DFORMAT-Enumerationstyps,](d3dformat.md) der das angeforderte Pixelformat für die Textur beschreibt.</span><span class="sxs-lookup"><span data-stu-id="e8c10-145">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="e8c10-146">Die zurückgegebene Textur hat möglicherweise ein anderes Format als das von *Format* angegebene Format.</span><span class="sxs-lookup"><span data-stu-id="e8c10-146">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="e8c10-147">Anwendungen sollten das Format der zurückgegebenen Textur überprüfen.</span><span class="sxs-lookup"><span data-stu-id="e8c10-147">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="e8c10-148">Wenn [D3DFMT \_ UNKNOWN](other-d3dx-constants.md)ist, wird das Format aus der Datei übernommen.</span><span class="sxs-lookup"><span data-stu-id="e8c10-148">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="e8c10-149">Wenn D3DFMT \_ FROM \_ FILE verwendet wird, wird das Format genau wie in der Datei verwendet, und der Aufruf schlägt fehl, wenn dies gegen die Gerätefunktionen verstößt.</span><span class="sxs-lookup"><span data-stu-id="e8c10-149">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="e8c10-150">*Pool* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="e8c10-150">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8c10-151">Typ: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="e8c10-151">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="e8c10-152">Member des [**D3DPOOL-Enumerationstyps,**](./d3dpool.md) der die Speicherklasse beschreibt, in die die Textur platziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e8c10-152">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="e8c10-153">*Filterung* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="e8c10-153">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8c10-154">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e8c10-154">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e8c10-155">Eine Kombination aus einem oder mehreren [ \_ D3DX-FILTERN,](d3dx-filter.md) die steuern, wie das Bild gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="e8c10-155">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="e8c10-156">Die Angabe von D3DX \_ DEFAULT für diesen Parameter entspricht der Angabe von D3DX FILTER TRIANGLE \_ \_ \| D3DX \_ FILTER \_ DITHER.</span><span class="sxs-lookup"><span data-stu-id="e8c10-156">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="e8c10-157">*MipFilter* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="e8c10-157">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8c10-158">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e8c10-158">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e8c10-159">Eine Kombination aus einem oder mehreren [ \_ D3DX-FILTERN,](d3dx-filter.md) die steuern, wie das Bild gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="e8c10-159">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="e8c10-160">Die Angabe von D3DX \_ DEFAULT für diesen Parameter entspricht der Angabe von D3DX FILTER \_ \_ BOX.</span><span class="sxs-lookup"><span data-stu-id="e8c10-160">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="e8c10-161">Verwenden Sie außerdem die Bits 27 bis 31, um die Anzahl der Mip-Ebenen anzugeben, die übersprungen werden sollen (von oben in der Mipmapkette), wenn eine DDS-Textur in den Arbeitsspeicher geladen wird. Dadurch können Sie bis zu 32 Ebenen überspringen.</span><span class="sxs-lookup"><span data-stu-id="e8c10-161">In addition, use bits 27-31 to specify the number of mip levels to be skipped (from the top of the mipmap chain) when a .dds texture is loaded into memory; this allows you to skip up to 32 levels.</span></span>

</dd> <dt>

<span data-ttu-id="e8c10-162">*ColorKey* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="e8c10-162">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8c10-163">Typ: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="e8c10-163">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="e8c10-164">[**D3DCOLOR-Wert,**](d3dcolor.md) der durch transparentes Schwarz ersetzt werden soll, oder 0, um den Farbschlüssel zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="e8c10-164">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="e8c10-165">Dies ist immer eine 32-Bit-ARGB-Farbe, unabhängig vom Quellbildformat.</span><span class="sxs-lookup"><span data-stu-id="e8c10-165">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="e8c10-166">Alpha ist wichtig und sollte in der Regel für nicht transparente Farbschlüssel auf FF festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e8c10-166">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="e8c10-167">Daher wäre der Wert für nicht transparentes Schwarz gleich 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="e8c10-167">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="e8c10-168">*pSrcInfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e8c10-168">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8c10-169">Typ: **[ **D3DXIMAGE \_ INFO**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="e8c10-169">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="e8c10-170">Zeiger auf eine [**D3DXIMAGE \_ INFO-Struktur,**](d3dximage-info.md) die mit einer Beschreibung der Daten in der Quellimagedatei ausgefüllt werden soll, oder **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e8c10-170">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled in with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e8c10-171">*pPalette* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e8c10-171">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8c10-172">Typ: **[ **PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="e8c10-172">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="e8c10-173">Zeiger auf eine [**PALETTEENTRY-Struktur,**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) die eine zu füllende 256-Farbpalette darstellt, oder **NULL.**</span><span class="sxs-lookup"><span data-stu-id="e8c10-173">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e8c10-174">*ppTexture* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e8c10-174">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8c10-175">Typ: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="e8c10-175">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span></span>

<span data-ttu-id="e8c10-176">Adresse eines Zeigers auf eine [**IDirect3DVolumeTexture9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) die das erstellte Texturobjekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="e8c10-176">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8c10-177">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e8c10-177">Return value</span></span>

<span data-ttu-id="e8c10-178">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e8c10-178">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e8c10-179">Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e8c10-179">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e8c10-180">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="e8c10-180">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8c10-181">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e8c10-181">Remarks</span></span>

<span data-ttu-id="e8c10-182">Die Compilereinstellung bestimmt auch die Funktionsversion.</span><span class="sxs-lookup"><span data-stu-id="e8c10-182">The compiler setting also determines the function version.</span></span> <span data-ttu-id="e8c10-183">Wenn Unicode definiert ist, wird der Funktionsaufruf in D3DXCreateVolumeTextureFromFileExW aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="e8c10-183">If Unicode is defined, the function call resolves to D3DXCreateVolumeTextureFromFileExW.</span></span> <span data-ttu-id="e8c10-184">Andernfalls wird der Funktionsaufruf in D3DXCreateVolumeTextureFromFileExA aufgelöst, da ANSI-Zeichenfolgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e8c10-184">Otherwise, the function call resolves to D3DXCreateVolumeTextureFromFileExA because ANSI strings are being used.</span></span>

<span data-ttu-id="e8c10-185">Diese Funktion unterstützt die folgenden Dateiformate: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm und .tga.</span><span class="sxs-lookup"><span data-stu-id="e8c10-185">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="e8c10-186">Siehe [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="e8c10-186">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="e8c10-187">Bei Mipmappentexturen wird jede Ebene automatisch mit der geladenen Volumetextur gefüllt.</span><span class="sxs-lookup"><span data-stu-id="e8c10-187">Mipmapped textures automatically have each level filled with the loaded volume texture.</span></span> <span data-ttu-id="e8c10-188">Beim Laden von Bildern in mipmapped-Texturen können einige Geräte nicht zu einem 1x1-Bild wechseln, und diese Funktion wird fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="e8c10-188">When loading images into mipmapped textures, some devices are unable to go to a 1x1 image and this function will fail.</span></span> <span data-ttu-id="e8c10-189">In diesem Fall müssen die Images manuell geladen werden.</span><span class="sxs-lookup"><span data-stu-id="e8c10-189">If this happens, then the images need to be loaded manually.</span></span>

<span data-ttu-id="e8c10-190">Wenn Sie Mipmapebenen beim Laden einer DDS-Datei überspringen, verwenden Sie das D3DX SKIP DDS MIP LEVELS-Makro, um den \_ \_ \_ \_ *MipFilter-Wert zu* generieren.</span><span class="sxs-lookup"><span data-stu-id="e8c10-190">When skipping mipmap levels while loading a .dds file, use the D3DX\_SKIP\_DDS\_MIP\_LEVELS macro to generate the *MipFilter* value.</span></span> <span data-ttu-id="e8c10-191">Dieses Makro verwendet die Anzahl der zu überspringenden Ebenen und den Filtertyp und gibt den Filterwert zurück, der dann an den *MipFilter-Parameter übergeben* wird.</span><span class="sxs-lookup"><span data-stu-id="e8c10-191">This macro takes the number of levels to skip and the filter type and returns the filter value, which would then be passed into the *MipFilter* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8c10-192">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e8c10-192">Requirements</span></span>



| <span data-ttu-id="e8c10-193">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e8c10-193">Requirement</span></span> | <span data-ttu-id="e8c10-194">Wert</span><span class="sxs-lookup"><span data-stu-id="e8c10-194">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e8c10-195">Header</span><span class="sxs-lookup"><span data-stu-id="e8c10-195">Header</span></span><br/>  | <dl> <span data-ttu-id="e8c10-196"><dt>D3dx9tex.h</dt></span><span class="sxs-lookup"><span data-stu-id="e8c10-196"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="e8c10-197">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e8c10-197">Library</span></span><br/> | <dl> <span data-ttu-id="e8c10-198"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e8c10-198"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e8c10-199">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e8c10-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8c10-200">**D3DXCreateVolumeTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="e8c10-200">**D3DXCreateVolumeTextureFromFile**</span></span>](d3dxcreatevolumetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="e8c10-201">**D3DXCreateVolumeTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="e8c10-201">**D3DXCreateVolumeTextureFromFileInMemory**</span></span>](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="e8c10-202">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="e8c10-202">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span></span>](d3dxcreatevolumetexturefromfileinmemoryex.md)
</dt> <dt>

[<span data-ttu-id="e8c10-203">**D3DXCreateVolumeTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="e8c10-203">**D3DXCreateVolumeTextureFromResource**</span></span>](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="e8c10-204">**D3DXCreateVolumeTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="e8c10-204">**D3DXCreateVolumeTextureFromResourceEx**</span></span>](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="e8c10-205">Texturfunktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="e8c10-205">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
