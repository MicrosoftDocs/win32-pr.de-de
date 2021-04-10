---
description: Erstellt eine Textur aus einer Datei im Arbeitsspeicher. Dies ist eine erweiterte Funktion als D3DXCreateTextureFromFileInMemory.
ms.assetid: e515697c-0e24-4d96-b58a-dc4f27683021
title: D3DXCreateTextureFromFileInMemoryEx-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromFileInMemoryEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: da85af9e70a7971ba0bab1f76e9c3d30c3cc2884
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961610"
---
# <a name="d3dxcreatetexturefromfileinmemoryex-function"></a><span data-ttu-id="253a6-104">D3DXCreateTextureFromFileInMemoryEx-Funktion</span><span class="sxs-lookup"><span data-stu-id="253a6-104">D3DXCreateTextureFromFileInMemoryEx function</span></span>

<span data-ttu-id="253a6-105">Erstellt eine Textur aus einer Datei im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="253a6-105">Creates a texture from a file in memory.</span></span> <span data-ttu-id="253a6-106">Dies ist eine erweiterte Funktion als [**D3DXCreateTextureFromFileInMemory**](d3dxcreatetexturefromfileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="253a6-106">This is a more advanced function than [**D3DXCreateTextureFromFileInMemory**](d3dxcreatetexturefromfileinmemory.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="253a6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="253a6-107">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureFromFileInMemoryEx(
  _In_    LPDIRECT3DDEVICE9  pDevice,
  _In_    LPCVOID            pSrcData,
  _In_    UINT               SrcDataSize,
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



## <a name="parameters"></a><span data-ttu-id="253a6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="253a6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="253a6-109">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="253a6-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="253a6-110">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="253a6-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="253a6-111">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das der Textur zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="253a6-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="253a6-112">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="253a6-112">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="253a6-113">Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="253a6-113">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="253a6-114">Ein Zeiger auf die Datei im Arbeitsspeicher, von der die Textur erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="253a6-114">Pointer to the file in memory from which to create the texture.</span></span>

</dd> <dt>

<span data-ttu-id="253a6-115">*Srcdatasize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="253a6-115">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="253a6-116">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="253a6-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="253a6-117">Größe der Datei im Arbeitsspeicher in Bytes.</span><span class="sxs-lookup"><span data-stu-id="253a6-117">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="253a6-118">*Breite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="253a6-118">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="253a6-119">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="253a6-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="253a6-120">Breite in Pixel.</span><span class="sxs-lookup"><span data-stu-id="253a6-120">Width in pixels.</span></span> <span data-ttu-id="253a6-121">Wenn dieser Wert 0 (null) oder D3DX \_ Default ist, werden die Dimensionen aus der Datei entnommen.</span><span class="sxs-lookup"><span data-stu-id="253a6-121">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="253a6-122">*Höhe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="253a6-122">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="253a6-123">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="253a6-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="253a6-124">Höhe in Pixel.</span><span class="sxs-lookup"><span data-stu-id="253a6-124">Height, in pixels.</span></span> <span data-ttu-id="253a6-125">Wenn dieser Wert 0 (null) oder D3DX \_ Default ist, werden die Dimensionen aus der Datei entnommen.</span><span class="sxs-lookup"><span data-stu-id="253a6-125">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="253a6-126">*Miplevels* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="253a6-126">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="253a6-127">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="253a6-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="253a6-128">Anzahl der angeforderten Mip-Ebenen.</span><span class="sxs-lookup"><span data-stu-id="253a6-128">Number of mip levels requested.</span></span> <span data-ttu-id="253a6-129">Wenn dieser Wert 0 (null) oder D3DX \_ Default ist, wird eine komplette MipMap-Kette erstellt.</span><span class="sxs-lookup"><span data-stu-id="253a6-129">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="253a6-130">*Verwendung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="253a6-130">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="253a6-131">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="253a6-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="253a6-132">0, D3DUSAGE \_ renderTarget oder D3DUSAGE \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="253a6-132">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="253a6-133">Wenn dieses Flag auf D3DUSAGE \_ renderTarget festgelegt wird, wird angegeben, dass die Oberfläche als Renderziel verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="253a6-133">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="253a6-134">Die Ressource kann dann an den *pnewrendertarget* -Parameter der Methode "Setup [**target**](/windows/desktop/api) " übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="253a6-134">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="253a6-135">Wenn entweder D3DUSAGE \_ renderTarget oder D3DUSAGE \_ Dynamic angegeben ist, muss der *Pool* auf D3DPOOL Default festgelegt werden \_ , und die Anwendung sollte überprüfen, ob das Gerät diesen Vorgang durch Aufrufen von [**CheckDeviceFormat**](/windows/desktop/api)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="253a6-135">If either D3DUSAGE\_RENDERTARGET or D3DUSAGE\_DYNAMIC is specified, *Pool* must be set to D3DPOOL\_DEFAULT, and the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="253a6-136">Weitere Informationen zur Verwendung dynamischer Texturen finden Sie unter [Verwenden dynamischer Texturen](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="253a6-136">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="253a6-137">*Format* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="253a6-137">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="253a6-138">Typ: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="253a6-138">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="253a6-139">Member des [D3DFORMAT](d3dformat.md) -Enumerationstyps, der das angeforderte Pixel Format für die Textur beschreibt.</span><span class="sxs-lookup"><span data-stu-id="253a6-139">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="253a6-140">Die zurückgegebene Textur kann ein anderes Format aufweisen als das, das durch das *Format* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="253a6-140">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="253a6-141">Anwendungen sollten das Format der zurückgegebenen Textur überprüfen.</span><span class="sxs-lookup"><span data-stu-id="253a6-141">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="253a6-142">Wenn [D3DFMT \_ Unknown](other-d3dx-constants.md)ist, wird das Format aus der Datei entnommen.</span><span class="sxs-lookup"><span data-stu-id="253a6-142">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="253a6-143">Wenn D3DFMT \_ from \_ File ist, wird das Format genau wie in der Datei erstellt, und der-Rückruf schlägt fehl, wenn dies die Gerätefunktionen verletzt.</span><span class="sxs-lookup"><span data-stu-id="253a6-143">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="253a6-144">*Pool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="253a6-144">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="253a6-145">Typ: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="253a6-145">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="253a6-146">Member des [**D3DPOOL**](./d3dpool.md) -Enumerationstyps, der die Speicher Klasse beschreibt, in der die Textur platziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="253a6-146">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="253a6-147">*Filter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="253a6-147">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="253a6-148">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="253a6-148">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="253a6-149">Eine Kombination aus einem oder mehreren Flags, die Steuern, wie das Bild gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="253a6-149">Combination of one or more flags controlling how the image is filtered.</span></span> <span data-ttu-id="253a6-150">Die Angabe \_ von D3DX default für diesen Parameter entspricht der Angabe von D3DX \_ Filter \_ Dreieck \| D3DX \_ Filter \_ Dither.</span><span class="sxs-lookup"><span data-stu-id="253a6-150">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span> <span data-ttu-id="253a6-151">Jeder gültige Filter muss eines der Flags in [D3DX \_ Filter](d3dx-filter.md)enthalten.</span><span class="sxs-lookup"><span data-stu-id="253a6-151">Each valid filter must contain one of the flags in [D3DX\_FILTER](d3dx-filter.md).</span></span>

</dd> <dt>

<span data-ttu-id="253a6-152">*MipFilter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="253a6-152">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="253a6-153">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="253a6-153">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="253a6-154">Eine Kombination aus einem oder mehreren Flags, die Steuern, wie das Bild gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="253a6-154">Combination of one or more flags controlling how the image is filtered.</span></span> <span data-ttu-id="253a6-155">Die Angabe \_ von D3DX default für diesen Parameter entspricht der Angabe von D3DX \_ Filter \_ Box.</span><span class="sxs-lookup"><span data-stu-id="253a6-155">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="253a6-156">Jeder gültige Filter muss eines der Flags in [D3DX \_ Filter](d3dx-filter.md)enthalten.</span><span class="sxs-lookup"><span data-stu-id="253a6-156">Each valid filter must contain one of the flags in [D3DX\_FILTER](d3dx-filter.md).</span></span> <span data-ttu-id="253a6-157">Verwenden Sie außerdem Bits 27-31, um die Anzahl der MIP-Ebenen anzugeben, die (vom oberen Rand der MipMap-Kette) übersprungen werden sollen, wenn eine DDS-Textur in den Arbeitsspeicher geladen wird. Dies ermöglicht es Ihnen, bis zu 32 Ebenen zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="253a6-157">In addition, use bits 27-31 to specify the number of mip levels to be skipped (from the top of the mipmap chain) when a .dds texture is loaded into memory; this allows you to skip up to 32 levels.</span></span>

</dd> <dt>

<span data-ttu-id="253a6-158">*Colorkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="253a6-158">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="253a6-159">Typ: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="253a6-159">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="253a6-160">[**D3DCOLOR**](d3dcolor.md) -Wert, der durch transparente schwarze ersetzt werden soll, oder 0, um den Colorkey zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="253a6-160">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="253a6-161">Dabei handelt es sich immer um eine 32-Bit-ARGB-Farbe, die unabhängig vom Quell Bildformat ist.</span><span class="sxs-lookup"><span data-stu-id="253a6-161">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="253a6-162">Alpha ist signifikant und sollte normalerweise für nicht transparente Farbtasten auf FF festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="253a6-162">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="253a6-163">Daher wäre der Wert für den Wert "0xFF000000" gleich.</span><span class="sxs-lookup"><span data-stu-id="253a6-163">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="253a6-164">*psrcinfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="253a6-164">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="253a6-165">Type: **[ **D3DXIMAGE \_ Info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="253a6-165">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="253a6-166">Ein Zeiger auf eine [**D3DXIMAGE \_ Info**](d3dximage-info.md) -Struktur, die mit einer Beschreibung der Daten in der Quell Bilddatei gefüllt werden soll, oder **null**.</span><span class="sxs-lookup"><span data-stu-id="253a6-166">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="253a6-167">*pPalette* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="253a6-167">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="253a6-168">Typ: **[ **PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="253a6-168">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="253a6-169">Zeiger auf eine [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) -Struktur, die eine zu füllende 256-Farbpalette darstellt, oder **null**.</span><span class="sxs-lookup"><span data-stu-id="253a6-169">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span> <span data-ttu-id="253a6-170">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="253a6-170">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="253a6-171">*pptexture* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="253a6-171">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="253a6-172">Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="253a6-172">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="253a6-173">Adresse eines Zeigers auf eine [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Schnittstelle, die das erstellte Textur Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="253a6-173">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="253a6-174">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="253a6-174">Return value</span></span>

<span data-ttu-id="253a6-175">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="253a6-175">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="253a6-176">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="253a6-176">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="253a6-177">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ NotAvailable, D3DERR \_ ouesfvideomemory, D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="253a6-177">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="253a6-178">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="253a6-178">Remarks</span></span>

<span data-ttu-id="253a6-179">Diese Funktion unterstützt die folgenden Dateiformate: BMP,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm und. TGA.</span><span class="sxs-lookup"><span data-stu-id="253a6-179">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="253a6-180">Siehe [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="253a6-180">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="253a6-181">Ausführliche Informationen zu [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)finden Sie unter Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="253a6-181">For details about [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry), see the Platform SDK.</span></span> <span data-ttu-id="253a6-182">Beachten Sie, dass der Member "Peer Flags" der **PaletteEntry** -Struktur ab DirectX 8,0 nicht wie im Platform SDK dokumentiert funktioniert.</span><span class="sxs-lookup"><span data-stu-id="253a6-182">Note that as of DirectX 8.0, the peFlags member of the **PALETTEENTRY** structure does not function as documented in the Platform SDK.</span></span> <span data-ttu-id="253a6-183">Der peflags-Member ist nun der Alphakanal für 8-Bit-Paletten-Formate.</span><span class="sxs-lookup"><span data-stu-id="253a6-183">The peFlags member is now the alpha channel for 8-bit palettized formats.</span></span>

<span data-ttu-id="253a6-184">Wenn Sie MipMap-Ebenen beim Laden einer DDS-Datei überspringen, verwenden \_ Sie das Makro D3DX Skip \_ DDS \_ MIP \_ Levels, um den MipFilter-Wert zu generieren.</span><span class="sxs-lookup"><span data-stu-id="253a6-184">When skipping mipmap levels while loading a .dds file, use the D3DX\_SKIP\_DDS\_MIP\_LEVELS macro to generate the MipFilter value.</span></span> <span data-ttu-id="253a6-185">Dieses Makro nimmt die Anzahl der zu über springenden Ebenen und den Filtertyp an und gibt den Filter Wert zurück, der dann an den MipFilter-Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="253a6-185">This macro takes the number of levels to skip and the filter type and returns the filter value, which would then be passed into the MipFilter parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="253a6-186">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="253a6-186">Requirements</span></span>



| <span data-ttu-id="253a6-187">Anforderung</span><span class="sxs-lookup"><span data-stu-id="253a6-187">Requirement</span></span> | <span data-ttu-id="253a6-188">Wert</span><span class="sxs-lookup"><span data-stu-id="253a6-188">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="253a6-189">Header</span><span class="sxs-lookup"><span data-stu-id="253a6-189">Header</span></span><br/>  | <dl> <span data-ttu-id="253a6-190"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="253a6-190"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="253a6-191">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="253a6-191">Library</span></span><br/> | <dl> <span data-ttu-id="253a6-192"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="253a6-192"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="253a6-193">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="253a6-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="253a6-194">**D3DXCreateTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="253a6-194">**D3DXCreateTextureFromFileInMemory**</span></span>](d3dxcreatetexturefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="253a6-195">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="253a6-195">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
