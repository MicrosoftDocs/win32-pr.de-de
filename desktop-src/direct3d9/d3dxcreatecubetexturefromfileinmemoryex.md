---
description: Erstellt eine cubetextur aus einer Datei im Arbeitsspeicher. Dies ist eine erweiterte Funktion als D3DXCreateCubeTextureFromFileInMemory.
ms.assetid: 598016eb-9ea9-4dca-a297-5708a957da6a
title: D3DXCreateCubeTextureFromFileInMemoryEx-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFileInMemoryEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7813d4532bbde18a5fc7fd7d1d090dc72eccd61f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104050920"
---
# <a name="d3dxcreatecubetexturefromfileinmemoryex-function"></a><span data-ttu-id="7b86f-104">D3DXCreateCubeTextureFromFileInMemoryEx-Funktion</span><span class="sxs-lookup"><span data-stu-id="7b86f-104">D3DXCreateCubeTextureFromFileInMemoryEx function</span></span>

<span data-ttu-id="7b86f-105">Erstellt eine cubetextur aus einer Datei im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="7b86f-105">Creates a cube texture from a file in memory.</span></span> <span data-ttu-id="7b86f-106">Dies ist eine erweiterte Funktion als [**D3DXCreateCubeTextureFromFileInMemory**](d3dxcreatecubetexturefromfileinmemory.md).</span><span class="sxs-lookup"><span data-stu-id="7b86f-106">This is a more advanced function than [**D3DXCreateCubeTextureFromFileInMemory**](d3dxcreatecubetexturefromfileinmemory.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7b86f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b86f-107">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTextureFromFileInMemoryEx(
  _In_    LPDIRECT3DDEVICE9      pDevice,
  _In_    LPCVOID                pSrcData,
  _In_    UINT                   SrcDataSize,
  _In_    UINT                   Size,
  _In_    UINT                   MipLevels,
  _In_    DWORD                  Usage,
  _In_    D3DFORMAT              Format,
  _In_    D3DPOOL                Pool,
  _In_    DWORD                  Filter,
  _In_    DWORD                  MipFilter,
  _In_    D3DCOLOR               ColorKey,
  _Inout_ D3DXIMAGE_INFO         *pSrcInfo,
  _Out_   PALETTEENTRY           *pPalette,
  _Out_   LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="7b86f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b86f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b86f-109">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b86f-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b86f-110">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="7b86f-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="7b86f-111">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das der cubetextur zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7b86f-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="7b86f-112">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b86f-112">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b86f-113">Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7b86f-113">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7b86f-114">Ein Zeiger auf die Datei im Arbeitsspeicher, von der die cubetextur erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7b86f-114">Pointer to the file in memory from which to create the cube texture.</span></span> <span data-ttu-id="7b86f-115">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="7b86f-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="7b86f-116">*Srcdatasize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b86f-116">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b86f-117">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7b86f-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7b86f-118">Größe der Datei im Arbeitsspeicher in Bytes.</span><span class="sxs-lookup"><span data-stu-id="7b86f-118">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="7b86f-119">*Größe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b86f-119">*Size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b86f-120">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7b86f-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7b86f-121">Breite (oder Höhe) in Pixel.</span><span class="sxs-lookup"><span data-stu-id="7b86f-121">Width (or height) in pixels.</span></span> <span data-ttu-id="7b86f-122">Wenn dieser Wert 0 (null) oder D3DX \_ Default ist, werden die Dimensionen aus der Datei entnommen.</span><span class="sxs-lookup"><span data-stu-id="7b86f-122">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="7b86f-123">*Miplevels* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b86f-123">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b86f-124">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7b86f-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7b86f-125">Anzahl der angeforderten Mip-Ebenen.</span><span class="sxs-lookup"><span data-stu-id="7b86f-125">Number of mip levels requested.</span></span> <span data-ttu-id="7b86f-126">Wenn dieser Wert 0 (null) oder D3DX \_ Default ist, wird eine komplette MipMap-Kette erstellt.</span><span class="sxs-lookup"><span data-stu-id="7b86f-126">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="7b86f-127">*Verwendung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b86f-127">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b86f-128">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7b86f-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7b86f-129">0, D3DUSAGE \_ renderTarget oder D3DUSAGE \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="7b86f-129">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="7b86f-130">Wenn dieses Flag auf D3DUSAGE \_ renderTarget festgelegt wird, wird angegeben, dass die Oberfläche als Renderziel verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7b86f-130">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="7b86f-131">Die Ressource kann dann an den *pnewrendertarget* -Parameter der Methode "Setup [**target**](/windows/desktop/api) " übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="7b86f-131">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="7b86f-132">Wenn D3DUSAGE \_ renderTarget angegeben ist, muss die Anwendung überprüfen, ob das Gerät diesen Vorgang durch Aufrufen von [**CheckDeviceFormat**](/windows/desktop/api)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7b86f-132">If D3DUSAGE\_RENDERTARGET is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="7b86f-133">Weitere Informationen zur Verwendung dynamischer Texturen finden Sie unter [Verwenden dynamischer Texturen](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="7b86f-133">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b86f-134">*Format* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b86f-134">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b86f-135">Typ: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="7b86f-135">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="7b86f-136">Member des [D3DFORMAT](d3dformat.md) -Enumerationstyps, der das angeforderte Pixel Format für die cubetextur beschreibt.</span><span class="sxs-lookup"><span data-stu-id="7b86f-136">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the cube texture.</span></span> <span data-ttu-id="7b86f-137">Die zurückgegebene Textur kann ein anderes Format aufweisen als das, das durch das *Format* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7b86f-137">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="7b86f-138">Anwendungen sollten das Format der zurückgegebenen Textur überprüfen.</span><span class="sxs-lookup"><span data-stu-id="7b86f-138">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="7b86f-139">Wenn [D3DFMT \_ Unknown](other-d3dx-constants.md)ist, wird das Format aus der Datei entnommen.</span><span class="sxs-lookup"><span data-stu-id="7b86f-139">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="7b86f-140">Wenn D3DFMT \_ from \_ File ist, wird das Format genau wie in der Datei erstellt, und der-Rückruf schlägt fehl, wenn dies die Gerätefunktionen verletzt.</span><span class="sxs-lookup"><span data-stu-id="7b86f-140">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="7b86f-141">*Pool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b86f-141">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b86f-142">Typ: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="7b86f-142">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="7b86f-143">Member des [**D3DPOOL**](./d3dpool.md) -Enumerationstyps, der die Speicher Klasse beschreibt, in der die Cubestruktur platziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7b86f-143">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the cube texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="7b86f-144">*Filter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b86f-144">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b86f-145">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7b86f-145">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7b86f-146">Eine Kombination aus einem oder mehreren [D3DX- \_ Filtern](d3dx-filter.md) , die Steuern, wie das Bild gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="7b86f-146">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="7b86f-147">Die Angabe \_ von D3DX default für diesen Parameter entspricht der Angabe von D3DX \_ Filter \_ Dreieck \| D3DX \_ Filter \_ Dither.</span><span class="sxs-lookup"><span data-stu-id="7b86f-147">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="7b86f-148">*MipFilter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b86f-148">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b86f-149">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7b86f-149">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7b86f-150">Eine Kombination aus einem oder mehreren [D3DX- \_ Filtern](d3dx-filter.md) , die Steuern, wie das Bild gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="7b86f-150">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="7b86f-151">Die Angabe \_ von D3DX default für diesen Parameter entspricht der Angabe von D3DX \_ Filter \_ Box.</span><span class="sxs-lookup"><span data-stu-id="7b86f-151">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="7b86f-152">Verwenden Sie außerdem Bits 27-31, um die Anzahl der MIP-Ebenen anzugeben, die (vom oberen Rand der MipMap-Kette) übersprungen werden sollen, wenn eine DDS-Textur in den Arbeitsspeicher geladen wird. Dies ermöglicht es Ihnen, bis zu 32 Ebenen zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="7b86f-152">In addition, use bits 27-31 to specify the number of mip levels to be skipped (from the top of the mipmap chain) when a .dds texture is loaded into memory; this allows you to skip up to 32 levels.</span></span>

</dd> <dt>

<span data-ttu-id="7b86f-153">*Colorkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7b86f-153">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b86f-154">Typ: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="7b86f-154">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="7b86f-155">[**D3DCOLOR**](d3dcolor.md) -Wert, der durch transparente schwarze ersetzt werden soll, oder 0, um den Colorkey zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="7b86f-155">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="7b86f-156">Dabei handelt es sich immer um eine 32-Bit-ARGB-Farbe, die unabhängig vom Quell Bildformat ist.</span><span class="sxs-lookup"><span data-stu-id="7b86f-156">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="7b86f-157">Alpha ist signifikant und sollte normalerweise für nicht transparente Farbtasten auf FF festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7b86f-157">Alpha is significant, and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="7b86f-158">Daher wäre der Wert für den Wert "0xFF000000" gleich.</span><span class="sxs-lookup"><span data-stu-id="7b86f-158">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="7b86f-159">*psrcinfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7b86f-159">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b86f-160">Type: **[ **D3DXIMAGE \_ Info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="7b86f-160">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="7b86f-161">Ein Zeiger auf eine [**D3DXIMAGE \_ Info**](d3dximage-info.md) -Struktur, die mit einer Beschreibung der Daten in der Quell Bilddatei gefüllt werden soll, oder **null**.</span><span class="sxs-lookup"><span data-stu-id="7b86f-161">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7b86f-162">*pPalette* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7b86f-162">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b86f-163">Typ: **[ **PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="7b86f-163">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="7b86f-164">Zeiger auf eine [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) -Struktur, die eine zu füllende 256-Farbpalette darstellt, oder **null**.</span><span class="sxs-lookup"><span data-stu-id="7b86f-164">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span> <span data-ttu-id="7b86f-165">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="7b86f-165">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="7b86f-166">*ppcubetexture* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7b86f-166">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b86f-167">Typ: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="7b86f-167">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="7b86f-168">Adresse eines Zeigers auf eine [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) -Schnittstelle, die das erstellte Cube-Textur Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="7b86f-168">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b86f-169">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7b86f-169">Return value</span></span>

<span data-ttu-id="7b86f-170">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7b86f-170">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7b86f-171">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7b86f-171">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7b86f-172">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcallable, D3DERR \_ NotAvailable, D3DERR \_ oudefvideomemory, D3DXERR \_ InvalidData, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="7b86f-172">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b86f-173">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7b86f-173">Remarks</span></span>

<span data-ttu-id="7b86f-174">Diese Funktion unterstützt die folgenden Dateiformate: BMP,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm und. TGA.</span><span class="sxs-lookup"><span data-stu-id="7b86f-174">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="7b86f-175">Siehe [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="7b86f-175">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="7b86f-176">Cube-Texturen unterscheiden sich von anderen Oberflächen darin, dass es sich um Auflistungen von</span><span class="sxs-lookup"><span data-stu-id="7b86f-176">Cube textures differ from other surfaces in that they are collections of surfaces.</span></span> <span data-ttu-id="7b86f-177">Um "\*" mit einer cubetextur aufzurufen, müssen Sie ein einzelnes Gesicht [**mithilfe von "**](/windows/desktop/api) [**getcubemapsurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) " auswählen und die resultierende Oberfläche an " **strendertarget** " übergeben.</span><span class="sxs-lookup"><span data-stu-id="7b86f-177">To call [**SetRenderTarget**](/windows/desktop/api) with a cube texture, you must select an individual face using [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) and pass the resulting surface to **SetRenderTarget** .</span></span>

<span data-ttu-id="7b86f-178">Diese Methode ist für das Laden von Bilddateien konzipiert, die als RT \_ RCDATA gespeichert werden. Dies ist eine Anwendungs definierte Ressource (Rohdaten).</span><span class="sxs-lookup"><span data-stu-id="7b86f-178">This method is designed to be used for loading image files stored as RT\_RCDATA, which is an application-defined resource (raw data).</span></span> <span data-ttu-id="7b86f-179">Andernfalls schlägt diese Methode fehl.</span><span class="sxs-lookup"><span data-stu-id="7b86f-179">Otherwise this method will fail.</span></span>

<span data-ttu-id="7b86f-180">Ausführliche Informationen zu [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)finden Sie unter Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="7b86f-180">For details on [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry), see the Platform SDK.</span></span> <span data-ttu-id="7b86f-181">Beachten Sie, dass der Member "Peer Flags" der **PaletteEntry** -Struktur ab DirectX 8,0 nicht wie im Platform SDK dokumentiert funktioniert.</span><span class="sxs-lookup"><span data-stu-id="7b86f-181">Note that as of DirectX 8.0, the peFlags member of the **PALETTEENTRY** structure does not function as documented in the Platform SDK.</span></span> <span data-ttu-id="7b86f-182">Der peflags-Member ist nun der Alphakanal für 8-Bit-Paletten-Formate.</span><span class="sxs-lookup"><span data-stu-id="7b86f-182">The peFlags member is now the alpha channel for 8-bit palettized formats.</span></span>

<span data-ttu-id="7b86f-183">**D3DXCreateCubeTextureFromFileInMemoryEx** verwendet das DDS-Dateiformat (DirectDraw Surface).</span><span class="sxs-lookup"><span data-stu-id="7b86f-183">**D3DXCreateCubeTextureFromFileInMemoryEx** uses the DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="7b86f-184">Mit dem DirectX-Textur-Editor (Dxtex.exe) können Sie eine cubemap aus anderen Dateiformaten generieren und im DDS-Dateiformat speichern.</span><span class="sxs-lookup"><span data-stu-id="7b86f-184">The DirectX Texture Editor (Dxtex.exe) enables you to generate a cube map from other file formats and save it in the DDS file format.</span></span> <span data-ttu-id="7b86f-185">Sie erhalten Dxtex.exe und erfahren mehr über das DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="7b86f-185">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="7b86f-186">Weitere Informationen zum DirectX SDK finden Sie unter [wo ist das DirectX SDK?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="7b86f-186">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

<span data-ttu-id="7b86f-187">Wenn Sie MipMap-Ebenen beim Laden einer DDS-Datei überspringen, verwenden \_ Sie das Makro D3DX Skip \_ DDS \_ MIP \_ Levels, um den MipFilter-Wert zu generieren.</span><span class="sxs-lookup"><span data-stu-id="7b86f-187">When skipping mipmap levels while loading a .dds file, use the D3DX\_SKIP\_DDS\_MIP\_LEVELS macro to generate the MipFilter value.</span></span> <span data-ttu-id="7b86f-188">Dieses Makro nimmt die Anzahl der zu über springenden Ebenen und den Filtertyp an und gibt den Filter Wert zurück, der dann an den MipFilter-Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="7b86f-188">This macro takes the number of levels to skip and the filter type and returns the filter value, which would then be passed into the MipFilter parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b86f-189">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b86f-189">Requirements</span></span>



| <span data-ttu-id="7b86f-190">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7b86f-190">Requirement</span></span> | <span data-ttu-id="7b86f-191">Wert</span><span class="sxs-lookup"><span data-stu-id="7b86f-191">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7b86f-192">Header</span><span class="sxs-lookup"><span data-stu-id="7b86f-192">Header</span></span><br/>  | <dl> <span data-ttu-id="7b86f-193"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b86f-193"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="7b86f-194">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7b86f-194">Library</span></span><br/> | <dl> <span data-ttu-id="7b86f-195"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7b86f-195"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="7b86f-196">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b86f-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b86f-197">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="7b86f-197">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
