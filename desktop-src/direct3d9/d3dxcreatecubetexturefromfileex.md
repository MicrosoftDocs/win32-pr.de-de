---
description: Erstellt eine cubetextur aus einer Datei. Dies ist eine erweiterte Funktion als D3DXCreateCubeTextureFromFile.
ms.assetid: 77e64b33-9282-42fa-978c-a93fa9ba11fc
title: D3DXCreateCubeTextureFromFileEx-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFileEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b4f56ad3f8e314f7ceb5f4efb07562257efab5fa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353395"
---
# <a name="d3dxcreatecubetexturefromfileex-function"></a><span data-ttu-id="21178-104">D3DXCreateCubeTextureFromFileEx-Funktion</span><span class="sxs-lookup"><span data-stu-id="21178-104">D3DXCreateCubeTextureFromFileEx function</span></span>

<span data-ttu-id="21178-105">Erstellt eine cubetextur aus einer Datei.</span><span class="sxs-lookup"><span data-stu-id="21178-105">Creates a cube texture from a file.</span></span> <span data-ttu-id="21178-106">Dies ist eine erweiterte Funktion als [**D3DXCreateCubeTextureFromFile**](d3dxcreatecubetexturefromfile.md).</span><span class="sxs-lookup"><span data-stu-id="21178-106">This is a more advanced function than [**D3DXCreateCubeTextureFromFile**](d3dxcreatecubetexturefromfile.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="21178-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="21178-107">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTextureFromFileEx(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  LPCTSTR                pSrcFile,
  _In_  UINT                   Size,
  _In_  UINT                   MipLevels,
  _In_  DWORD                  Usage,
  _In_  D3DFORMAT              Format,
  _In_  D3DPOOL                Pool,
  _In_  DWORD                  Filter,
  _In_  DWORD                  MipFilter,
  _In_  D3DCOLOR               ColorKey,
  _Out_ D3DXIMAGE_INFO         *pSrcInfo,
  _Out_ PALETTEENTRY           *pPalette,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="21178-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="21178-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21178-109">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21178-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21178-110">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="21178-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="21178-111">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das der cubetextur zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="21178-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="21178-112">*psrcfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21178-112">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21178-113">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="21178-113">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="21178-114">Zeiger auf eine Zeichenfolge, die den Dateinamen angibt.</span><span class="sxs-lookup"><span data-stu-id="21178-114">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="21178-115">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="21178-115">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="21178-116">Andernfalls wird der String-Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="21178-116">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="21178-117">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="21178-117">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="21178-118">*Größe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21178-118">*Size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21178-119">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="21178-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="21178-120">Breite und Höhe der cubetextur in Pixel.</span><span class="sxs-lookup"><span data-stu-id="21178-120">Width and height of the cube texture, in pixels.</span></span> <span data-ttu-id="21178-121">Wenn es sich bei der cubetextur z. b. um einen 8-Pixel-Cube mit 8 Pixel handelt, sollte der Wert für diesen Parameter 8 lauten.</span><span class="sxs-lookup"><span data-stu-id="21178-121">For example, if the cube texture is an 8-pixel by 8-pixel cube, the value for this parameter should be 8.</span></span> <span data-ttu-id="21178-122">Wenn dieser Wert 0 oder D3DX \_ Default ist, werden die Dimensionen aus der Datei entnommen.</span><span class="sxs-lookup"><span data-stu-id="21178-122">If this value is 0 or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="21178-123">*Miplevels* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21178-123">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21178-124">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="21178-124">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="21178-125">Anzahl der angeforderten Mip-Ebenen.</span><span class="sxs-lookup"><span data-stu-id="21178-125">Number of mip levels requested.</span></span> <span data-ttu-id="21178-126">Wenn dieser Wert 0 (null) oder D3DX \_ Default ist, wird eine komplette MipMap-Kette erstellt.</span><span class="sxs-lookup"><span data-stu-id="21178-126">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="21178-127">*Verwendung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21178-127">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21178-128">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="21178-128">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="21178-129">0 oder D3DUSAGE \_ renderTarget oder D3DUSAGE \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="21178-129">0 or D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="21178-130">Wenn dieses Flag auf D3DUSAGE \_ renderTarget festgelegt wird, wird angegeben, dass die Oberfläche als Renderziel verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="21178-130">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="21178-131">Die Ressource kann dann an den *pnewrendertarget* -Parameter der Methode "Setup [**target**](/windows/desktop/api) " übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="21178-131">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="21178-132">Wenn D3DUSAGE \_ renderTarget angegeben ist, muss die Anwendung überprüfen, ob das Gerät diesen Vorgang durch Aufrufen von [**CheckDeviceFormat**](/windows/desktop/api)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="21178-132">If D3DUSAGE\_RENDERTARGET is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="21178-133">D3DUSAGE \_ Dynamic gibt an, dass die Oberfläche dynamisch behandelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="21178-133">D3DUSAGE\_DYNAMIC indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="21178-134">Weitere Informationen zur Verwendung dynamischer Texturen finden Sie unter [Verwenden dynamischer Texturen](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="21178-134">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="21178-135">*Format* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21178-135">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21178-136">Typ: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="21178-136">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="21178-137">Member des [D3DFORMAT](d3dformat.md) -Enumerationstyps, der das angeforderte Pixel Format für die cubetextur beschreibt.</span><span class="sxs-lookup"><span data-stu-id="21178-137">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the cube texture.</span></span> <span data-ttu-id="21178-138">Die zurückgegebene cubetextur kann ein anderes Format aufweisen als das, das durch das *Format* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="21178-138">The returned cube texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="21178-139">Anwendungen sollten das Format der zurückgegebenen cubetextur überprüfen.</span><span class="sxs-lookup"><span data-stu-id="21178-139">Applications should check the format of the returned cube texture.</span></span> <span data-ttu-id="21178-140">Wenn [D3DFMT \_ Unknown](other-d3dx-constants.md)ist, wird das Format aus der Datei entnommen.</span><span class="sxs-lookup"><span data-stu-id="21178-140">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="21178-141">Wenn D3DFMT \_ from \_ File ist, wird das Format genau wie in der Datei erstellt, und der-Rückruf schlägt fehl, wenn dies die Gerätefunktionen verletzt.</span><span class="sxs-lookup"><span data-stu-id="21178-141">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="21178-142">*Pool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21178-142">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21178-143">Typ: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="21178-143">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="21178-144">Member des [**D3DPOOL**](./d3dpool.md) -Enumerationstyps, der die Speicher Klasse beschreibt, in der die Cubestruktur platziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="21178-144">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the cube texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="21178-145">*Filter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21178-145">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21178-146">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="21178-146">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="21178-147">Eine Kombination aus einer oder mehreren [D3DX \_ Filter](d3dx-filter.md) Konstanten, die die Filterung des Bilds steuern.</span><span class="sxs-lookup"><span data-stu-id="21178-147">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) constants, controlling how the image is filtered.</span></span> <span data-ttu-id="21178-148">Die Angabe \_ von D3DX default für diesen Parameter entspricht der Angabe von D3DX \_ Filter \_ Dreieck \| D3DX \_ Filter \_ Dither.</span><span class="sxs-lookup"><span data-stu-id="21178-148">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="21178-149">*MipFilter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21178-149">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21178-150">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="21178-150">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="21178-151">Eine Kombination aus einer oder mehreren [D3DX \_ Filter](d3dx-filter.md) -Konstanten, die Steuern, wie das Bild gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="21178-151">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) constants controlling how the image is filtered.</span></span> <span data-ttu-id="21178-152">Die Angabe \_ von D3DX default für diesen Parameter entspricht der Angabe von D3DX \_ Filter \_ Box.</span><span class="sxs-lookup"><span data-stu-id="21178-152">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="21178-153">Verwenden Sie außerdem Bits 27-31, um die Anzahl der MIP-Ebenen anzugeben, die (vom oberen Rand der MipMap-Kette) übersprungen werden sollen, wenn eine DDS-Textur in den Arbeitsspeicher geladen wird. Dies ermöglicht es Ihnen, bis zu 32 Ebenen zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="21178-153">In addition, use bits 27-31 to specify the number of mip levels to be skipped (from the top of the mipmap chain) when a .dds texture is loaded into memory; this allows you to skip up to 32 levels.</span></span>

</dd> <dt>

<span data-ttu-id="21178-154">*Colorkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21178-154">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21178-155">Typ: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="21178-155">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="21178-156">[**D3DCOLOR**](d3dcolor.md) -Wert, der durch transparente schwarze ersetzt werden soll, oder 0, um den Colorkey zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="21178-156">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="21178-157">Dabei handelt es sich immer um eine 32-Bit-ARGB-Farbe, die unabhängig vom Quell Bildformat ist.</span><span class="sxs-lookup"><span data-stu-id="21178-157">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="21178-158">Alpha ist signifikant und sollte normalerweise für nicht transparente Farbtasten auf FF festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="21178-158">Alpha is significant, and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="21178-159">Daher wäre der Wert für den Wert "0xFF000000" gleich.</span><span class="sxs-lookup"><span data-stu-id="21178-159">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="21178-160">*psrcinfo* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="21178-160">*pSrcInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21178-161">Type: **[ **D3DXIMAGE \_ Info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="21178-161">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="21178-162">Ein Zeiger auf eine [**D3DXIMAGE \_ Info**](d3dximage-info.md) -Struktur, die mit einer Beschreibung der Daten in der Quell Bilddatei gefüllt werden soll, oder **null**.</span><span class="sxs-lookup"><span data-stu-id="21178-162">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="21178-163">*pPalette* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="21178-163">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21178-164">Typ: **[ **PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="21178-164">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="21178-165">Zeiger auf eine [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) -Struktur, die eine zu füllende 256-Farbpalette darstellt, oder **null**.</span><span class="sxs-lookup"><span data-stu-id="21178-165">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="21178-166">*ppcubetexture* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="21178-166">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="21178-167">Typ: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="21178-167">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="21178-168">Adresse eines Zeigers auf eine [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) -Schnittstelle, die das erstellte Cube-Textur Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="21178-168">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21178-169">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="21178-169">Return value</span></span>

<span data-ttu-id="21178-170">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="21178-170">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="21178-171">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="21178-171">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="21178-172">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcallable, D3DERR \_ NotAvailable, D3DERR \_ oudefvideomemory, D3DXERR \_ InvalidData, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="21178-172">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="21178-173">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="21178-173">Remarks</span></span>

<span data-ttu-id="21178-174">Die Compilereinstellung bestimmt auch die Funktions Version.</span><span class="sxs-lookup"><span data-stu-id="21178-174">The compiler setting also determines the function version.</span></span> <span data-ttu-id="21178-175">Wenn Unicode definiert ist, wird der Funktions aufrufin **D3DXCreateCubeTextureFromFileExW** aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="21178-175">If Unicode is defined, the function call resolves to **D3DXCreateCubeTextureFromFileExW**.</span></span> <span data-ttu-id="21178-176">Andernfalls wird der Funktions Aufruhe in **D3DXCreateCubeTextureFromFileExA** aufgelöst, da ANSI-Zeichen folgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="21178-176">Otherwise, the function call resolves to **D3DXCreateCubeTextureFromFileExA** because ANSI strings are being used.</span></span>

<span data-ttu-id="21178-177">Diese Funktion unterstützt die folgenden Dateiformate: BMP,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm und. TGA.</span><span class="sxs-lookup"><span data-stu-id="21178-177">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="21178-178">Siehe [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="21178-178">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="21178-179">Cube-Texturen unterscheiden sich von anderen Oberflächen darin, dass es sich um Auflistungen von</span><span class="sxs-lookup"><span data-stu-id="21178-179">Cube textures differ from other surfaces in that they are collections of surfaces.</span></span> <span data-ttu-id="21178-180">Um "\*" mit einer cubetextur aufzurufen, müssen Sie ein einzelnes Gesicht [**mithilfe von "**](/windows/desktop/api) [**getcubemapsurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) " auswählen und die resultierende Oberfläche an " **strendertarget**" übergeben.</span><span class="sxs-lookup"><span data-stu-id="21178-180">To call [**SetRenderTarget**](/windows/desktop/api) with a cube texture, you must select an individual face using [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) and pass the resulting surface to **SetRenderTarget**.</span></span>

<span data-ttu-id="21178-181">**D3DXCreateCubeTextureFromFileEx** verwendet das DDS-Dateiformat (DirectDraw Surface).</span><span class="sxs-lookup"><span data-stu-id="21178-181">**D3DXCreateCubeTextureFromFileEx** uses the DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="21178-182">Mit dem DirectX-Textur-Editor (Dxtex.exe) können Sie eine cubemap aus anderen Dateiformaten generieren und im DDS-Dateiformat speichern.</span><span class="sxs-lookup"><span data-stu-id="21178-182">The DirectX Texture Editor (Dxtex.exe) enables you to generate a cube map from other file formats and save it in the DDS file format.</span></span> <span data-ttu-id="21178-183">Sie erhalten Dxtex.exe und erfahren mehr über das DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="21178-183">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="21178-184">Weitere Informationen zum DirectX SDK finden Sie unter [wo ist das DirectX SDK?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="21178-184">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

<span data-ttu-id="21178-185">Wenn Sie MipMap-Ebenen beim Laden einer DDS-Datei überspringen, verwenden \_ Sie das Makro D3DX Skip \_ DDS \_ MIP \_ Levels, um den MipFilter-Wert zu generieren.</span><span class="sxs-lookup"><span data-stu-id="21178-185">When skipping mipmap levels while loading a .dds file, use the D3DX\_SKIP\_DDS\_MIP\_LEVELS macro to generate the MipFilter value.</span></span> <span data-ttu-id="21178-186">Dieses Makro nimmt die Anzahl der zu über springenden Ebenen und den Filtertyp an und gibt den Filter Wert zurück, der dann an den MipFilter-Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="21178-186">This macro takes the number of levels to skip and the filter type and returns the filter value, which would then be passed into the MipFilter parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="21178-187">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21178-187">Requirements</span></span>



| <span data-ttu-id="21178-188">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21178-188">Requirement</span></span> | <span data-ttu-id="21178-189">Wert</span><span class="sxs-lookup"><span data-stu-id="21178-189">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="21178-190">Header</span><span class="sxs-lookup"><span data-stu-id="21178-190">Header</span></span><br/>  | <dl> <span data-ttu-id="21178-191"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="21178-191"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="21178-192">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="21178-192">Library</span></span><br/> | <dl> <span data-ttu-id="21178-193"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="21178-193"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="21178-194">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21178-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21178-195">**D3DXCreateCubeTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="21178-195">**D3DXCreateCubeTextureFromFile**</span></span>](d3dxcreatecubetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="21178-196">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="21178-196">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
