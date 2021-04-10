---
description: Erstellt eine volumetextur aus einer Ressource, die durch eine Zeichenfolge angegeben wird. Dies ist eine erweiterte Funktion als D3DXCreateVolumeTextureFromResource.
ms.assetid: 02f2cb9e-4750-4854-aa74-202426427af5
title: D3DXCreateVolumeTextureFromResourceEx-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromResourceEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 44d842df2da1d5c3db374e838e0ffd2492683961
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961606"
---
# <a name="d3dxcreatevolumetexturefromresourceex-function"></a><span data-ttu-id="e16ab-104">D3DXCreateVolumeTextureFromResourceEx-Funktion</span><span class="sxs-lookup"><span data-stu-id="e16ab-104">D3DXCreateVolumeTextureFromResourceEx function</span></span>

<span data-ttu-id="e16ab-105">Erstellt eine volumetextur aus einer Ressource, die durch eine Zeichenfolge angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e16ab-105">Creates a volume texture from a resource specified by a string.</span></span> <span data-ttu-id="e16ab-106">Dies ist eine erweiterte Funktion als [**D3DXCreateVolumeTextureFromResource**](d3dxcreatevolumetexturefromresource.md).</span><span class="sxs-lookup"><span data-stu-id="e16ab-106">This is a more advanced function than [**D3DXCreateVolumeTextureFromResource**](d3dxcreatevolumetexturefromresource.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e16ab-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e16ab-107">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTextureFromResourceEx(
  _In_    LPDIRECT3DDEVICE9        pDevice,
  _In_    HMODULE                  hSrcModule,
  _In_    LPCTSTR                  pSrcResource,
  _In_    UINT                     Width,
  _In_    UINT                     Height,
  _In_    UINT                     Depth,
  _In_    UINT                     MipLevels,
  _In_    DWORD                    Usage,
  _In_    D3DFORMAT                Format,
  _In_    D3DPOOL                  Pool,
  _In_    DWORD                    Filter,
  _In_    DWORD                    MipFilter,
  _In_    D3DCOLOR                 ColorKey,
  _Inout_ D3DXIMAGE_INFO           *pSrcInfo,
  _Out_   PALETTEENTRY             *pPalette,
  _Out_   LPDIRECT3DVOLUMETEXTURE9 *ppVolumeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="e16ab-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e16ab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e16ab-109">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e16ab-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e16ab-110">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="e16ab-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="e16ab-111">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das der Textur zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e16ab-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="e16ab-112">*hsrcmodule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e16ab-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e16ab-113">Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e16ab-113">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e16ab-114">Handle für das Modul, in dem sich die Ressource befindet, oder **null** für das Modul, das dem Image zugeordnet ist, mit dem das Betriebssystem den aktuellen Prozess erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="e16ab-114">Handle to the module where the resource is located, or **NULL** for module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="e16ab-115">*psrkresource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e16ab-115">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e16ab-116">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e16ab-116">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e16ab-117">Zeiger auf eine Zeichenfolge, die den Ressourcennamen angibt.</span><span class="sxs-lookup"><span data-stu-id="e16ab-117">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="e16ab-118">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="e16ab-118">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="e16ab-119">Andernfalls wird der String-Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="e16ab-119">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="e16ab-120">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="e16ab-120">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="e16ab-121">*Breite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e16ab-121">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e16ab-122">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e16ab-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e16ab-123">Breite in Pixel.</span><span class="sxs-lookup"><span data-stu-id="e16ab-123">Width in pixels.</span></span> <span data-ttu-id="e16ab-124">Wenn dieser Wert 0 (null) oder D3DX \_ Default ist, werden die Dimensionen aus der Datei entnommen.</span><span class="sxs-lookup"><span data-stu-id="e16ab-124">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="e16ab-125">Die maximale Dimension, die ein Treiber unterstützt (für Breite, Höhe und Tiefe), ist in maxvolumeblock in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)zu finden.</span><span class="sxs-lookup"><span data-stu-id="e16ab-125">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="e16ab-126">*Höhe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e16ab-126">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e16ab-127">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e16ab-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e16ab-128">Höhe in Pixel.</span><span class="sxs-lookup"><span data-stu-id="e16ab-128">Height, in pixels.</span></span> <span data-ttu-id="e16ab-129">Wenn dieser Wert 0 (null) oder D3DX \_ Default ist, werden die Dimensionen aus der Datei entnommen.</span><span class="sxs-lookup"><span data-stu-id="e16ab-129">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="e16ab-130">Die maximale Dimension, die ein Treiber unterstützt (für Breite, Höhe und Tiefe), ist in maxvolumeblock in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)zu finden.</span><span class="sxs-lookup"><span data-stu-id="e16ab-130">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="e16ab-131">*Tiefe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e16ab-131">*Depth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e16ab-132">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e16ab-132">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e16ab-133">Tiefe in Pixel.</span><span class="sxs-lookup"><span data-stu-id="e16ab-133">Depth, in pixels.</span></span> <span data-ttu-id="e16ab-134">Wenn dieser Wert 0 (null) oder D3DX \_ Default ist, werden die Dimensionen aus der Datei entnommen.</span><span class="sxs-lookup"><span data-stu-id="e16ab-134">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span> <span data-ttu-id="e16ab-135">Die maximale Dimension, die ein Treiber unterstützt (für Breite, Höhe und Tiefe), ist in maxvolumeblock in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)zu finden.</span><span class="sxs-lookup"><span data-stu-id="e16ab-135">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="e16ab-136">*Miplevels* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e16ab-136">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e16ab-137">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e16ab-137">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e16ab-138">Anzahl der angeforderten Mip-Ebenen.</span><span class="sxs-lookup"><span data-stu-id="e16ab-138">Number of mip levels requested.</span></span> <span data-ttu-id="e16ab-139">Wenn dieser Wert 0 (null) oder D3DX \_ Default ist, wird eine komplette MipMap-Kette erstellt.</span><span class="sxs-lookup"><span data-stu-id="e16ab-139">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="e16ab-140">*Verwendung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e16ab-140">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e16ab-141">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e16ab-141">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e16ab-142">0, D3DUSAGE \_ renderTarget oder D3DUSAGE \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="e16ab-142">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="e16ab-143">Wenn dieses Flag auf D3DUSAGE \_ renderTarget festgelegt wird, wird angegeben, dass die Oberfläche als Renderziel verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e16ab-143">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="e16ab-144">Die Ressource kann dann an den *pnewrendertarget* -Parameter der Methode "Setup [**target**](/windows/desktop/api) " übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="e16ab-144">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="e16ab-145">Wenn entweder D3DUSAGE \_ renderTarget oder D3DUSAGE \_ Dynamic angegeben ist, muss der *Pool* auf D3DPOOL Default festgelegt werden \_ , und die Anwendung sollte überprüfen, ob das Gerät diesen Vorgang durch Aufrufen von [**CheckDeviceFormat**](/windows/desktop/api)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e16ab-145">If either D3DUSAGE\_RENDERTARGET or D3DUSAGE\_DYNAMIC is specified, *Pool* must be set to D3DPOOL\_DEFAULT, and the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="e16ab-146">D3DUSAGE \_ Dynamic gibt an, dass die Oberfläche dynamisch behandelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e16ab-146">D3DUSAGE\_DYNAMIC indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="e16ab-147">Weitere Informationen zur Verwendung dynamischer Texturen finden Sie unter [Verwenden dynamischer Texturen](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="e16ab-147">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="e16ab-148">*Format* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e16ab-148">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e16ab-149">Typ: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="e16ab-149">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="e16ab-150">Member des [D3DFORMAT](d3dformat.md) -Enumerationstyps, der das angeforderte Pixel Format für die Textur beschreibt.</span><span class="sxs-lookup"><span data-stu-id="e16ab-150">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="e16ab-151">Die zurückgegebene Textur kann ein anderes Format aufweisen als das, das durch das *Format* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e16ab-151">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="e16ab-152">Anwendungen sollten das Format der zurückgegebenen Textur überprüfen.</span><span class="sxs-lookup"><span data-stu-id="e16ab-152">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="e16ab-153">Wenn [D3DFMT \_ Unknown](other-d3dx-constants.md)ist, wird das Format aus der Datei entnommen.</span><span class="sxs-lookup"><span data-stu-id="e16ab-153">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="e16ab-154">Wenn D3DFMT \_ from \_ File ist, wird das Format genau wie in der Datei erstellt, und der-Rückruf schlägt fehl, wenn dies die Gerätefunktionen verletzt.</span><span class="sxs-lookup"><span data-stu-id="e16ab-154">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="e16ab-155">*Pool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e16ab-155">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e16ab-156">Typ: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="e16ab-156">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="e16ab-157">Member des [**D3DPOOL**](./d3dpool.md) -Enumerationstyps, der die Speicher Klasse beschreibt, in der die Textur platziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e16ab-157">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="e16ab-158">*Filter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e16ab-158">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e16ab-159">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e16ab-159">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e16ab-160">Eine Kombination aus einem oder mehreren [D3DX- \_ Filtern](d3dx-filter.md) , die Steuern, wie das Bild gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="e16ab-160">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="e16ab-161">Die Angabe \_ von D3DX default für diesen Parameter entspricht der Angabe von D3DX \_ Filter \_ Dreieck \| D3DX \_ Filter \_ Dither.</span><span class="sxs-lookup"><span data-stu-id="e16ab-161">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="e16ab-162">*MipFilter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e16ab-162">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e16ab-163">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e16ab-163">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e16ab-164">Eine Kombination aus einem oder mehreren [D3DX- \_ Filtern](d3dx-filter.md) , die Steuern, wie das Bild gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="e16ab-164">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="e16ab-165">Die Angabe \_ von D3DX default für diesen Parameter entspricht der Angabe von D3DX \_ Filter \_ Box.</span><span class="sxs-lookup"><span data-stu-id="e16ab-165">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span>

</dd> <dt>

<span data-ttu-id="e16ab-166">*Colorkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e16ab-166">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e16ab-167">Typ: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="e16ab-167">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="e16ab-168">[**D3DCOLOR**](d3dcolor.md) -Wert, der durch transparente schwarze ersetzt werden soll, oder 0, um den Colorkey zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="e16ab-168">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="e16ab-169">Dabei handelt es sich immer um eine 32-Bit-ARGB-Farbe, die unabhängig vom Quell Bildformat ist.</span><span class="sxs-lookup"><span data-stu-id="e16ab-169">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="e16ab-170">Alpha ist signifikant und sollte normalerweise für nicht transparente Farbtasten auf FF festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e16ab-170">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="e16ab-171">Daher wäre der Wert für den Wert "0xFF000000" gleich.</span><span class="sxs-lookup"><span data-stu-id="e16ab-171">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="e16ab-172">*psrcinfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e16ab-172">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e16ab-173">Type: **[ **D3DXIMAGE \_ Info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="e16ab-173">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="e16ab-174">Ein Zeiger auf eine [**D3DXIMAGE \_ Info**](d3dximage-info.md) -Struktur, die mit einer Beschreibung der Daten in der Quell Bilddatei ausgefüllt werden soll, oder **null**.</span><span class="sxs-lookup"><span data-stu-id="e16ab-174">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled in with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e16ab-175">*pPalette* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e16ab-175">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e16ab-176">Typ: **[ **PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="e16ab-176">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="e16ab-177">Zeiger auf eine [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) -Struktur, die eine zu füllende 256-Farbpalette darstellt, oder **null**.</span><span class="sxs-lookup"><span data-stu-id="e16ab-177">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e16ab-178">*ppvolumetexture* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e16ab-178">*ppVolumeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e16ab-179">Typ: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="e16ab-179">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span></span>

<span data-ttu-id="e16ab-180">Adresse eines Zeigers auf eine [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) -Schnittstelle, die das erstellte Textur Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="e16ab-180">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e16ab-181">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e16ab-181">Return value</span></span>

<span data-ttu-id="e16ab-182">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e16ab-182">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e16ab-183">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e16ab-183">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e16ab-184">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ NotAvailable, D3DERR \_ ouesfvideomemory, D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="e16ab-184">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="e16ab-185">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e16ab-185">Remarks</span></span>

<span data-ttu-id="e16ab-186">Die Compilereinstellung bestimmt auch die Funktions Version.</span><span class="sxs-lookup"><span data-stu-id="e16ab-186">The compiler setting also determines the function version.</span></span> <span data-ttu-id="e16ab-187">Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXCreateVolumeTextureFromResourceExW aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="e16ab-187">If Unicode is defined, the function call resolves to D3DXCreateVolumeTextureFromResourceExW.</span></span> <span data-ttu-id="e16ab-188">Andernfalls wird der Funktions Aufruhe in D3DXCreateVolumeTextureFromResourceExA aufgelöst, da ANSI-Zeichen folgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e16ab-188">Otherwise, the function call resolves to D3DXCreateVolumeTextureFromResourceExA because ANSI strings are being used.</span></span>

<span data-ttu-id="e16ab-189">Die Ressource, die geladen wird, muss eine von der Anwendung definierte Ressource (RT \_ RCDATA) sein.</span><span class="sxs-lookup"><span data-stu-id="e16ab-189">The resource being loaded must be an application-defined resource (RT\_RCDATA).</span></span>

<span data-ttu-id="e16ab-190">Diese Funktion unterstützt die folgenden Dateiformate: BMP,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm und. TGA.</span><span class="sxs-lookup"><span data-stu-id="e16ab-190">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="e16ab-191">Siehe [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="e16ab-191">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e16ab-192">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e16ab-192">Requirements</span></span>



| <span data-ttu-id="e16ab-193">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e16ab-193">Requirement</span></span> | <span data-ttu-id="e16ab-194">Wert</span><span class="sxs-lookup"><span data-stu-id="e16ab-194">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e16ab-195">Header</span><span class="sxs-lookup"><span data-stu-id="e16ab-195">Header</span></span><br/>  | <dl> <span data-ttu-id="e16ab-196"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="e16ab-196"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="e16ab-197">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e16ab-197">Library</span></span><br/> | <dl> <span data-ttu-id="e16ab-198"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e16ab-198"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e16ab-199">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e16ab-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e16ab-200">**D3DXCreateVolumeTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="e16ab-200">**D3DXCreateVolumeTextureFromFile**</span></span>](d3dxcreatevolumetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="e16ab-201">**D3DXCreateVolumeTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="e16ab-201">**D3DXCreateVolumeTextureFromFileEx**</span></span>](d3dxcreatevolumetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="e16ab-202">**D3DXCreateVolumeTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="e16ab-202">**D3DXCreateVolumeTextureFromFileInMemory**</span></span>](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="e16ab-203">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="e16ab-203">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span></span>](d3dxcreatevolumetexturefromfileinmemoryex.md)
</dt> <dt>

[<span data-ttu-id="e16ab-204">**D3DXCreateVolumeTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="e16ab-204">**D3DXCreateVolumeTextureFromResource**</span></span>](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="e16ab-205">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="e16ab-205">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
