---
description: Erstellt eine Textur aus einer Ressource. Dies ist eine erweiterte Funktion als D3DXCreateTextureFromResource.
ms.assetid: 6015e2fa-9deb-4e6a-a401-f10fb05f40b7
title: D3DXCreateTextureFromResourceEx-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromResourceEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 26298f8a63ccfde2171578c27e9208011c16dd28
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530914"
---
# <a name="d3dxcreatetexturefromresourceex-function"></a><span data-ttu-id="fb40b-104">D3DXCreateTextureFromResourceEx-Funktion</span><span class="sxs-lookup"><span data-stu-id="fb40b-104">D3DXCreateTextureFromResourceEx function</span></span>

<span data-ttu-id="fb40b-105">Erstellt eine Textur aus einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="fb40b-105">Creates a texture from a resource.</span></span> <span data-ttu-id="fb40b-106">Dies ist eine erweiterte Funktion als [**D3DXCreateTextureFromResource**](d3dxcreatetexturefromresource.md).</span><span class="sxs-lookup"><span data-stu-id="fb40b-106">This is a more advanced function than [**D3DXCreateTextureFromResource**](d3dxcreatetexturefromresource.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fb40b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb40b-107">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureFromResourceEx(
  _In_    LPDIRECT3DDEVICE9  pDevice,
  _In_    HMODULE            hSrcModule,
  _In_    LPCTSTR            pSrcResource,
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



## <a name="parameters"></a><span data-ttu-id="fb40b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb40b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb40b-109">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb40b-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb40b-110">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="fb40b-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="fb40b-111">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das der Textur zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fb40b-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="fb40b-112">*hsrcmodule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb40b-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb40b-113">Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fb40b-113">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fb40b-114">Handle für das Modul, in dem sich die Ressource befindet, oder **null** für das Modul, das dem Image zugeordnet ist, mit dem das Betriebssystem den aktuellen Prozess erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="fb40b-114">Handle to the module where the resource is located, or **NULL** for module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="fb40b-115">*psrkresource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb40b-115">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb40b-116">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fb40b-116">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fb40b-117">Zeiger auf eine Zeichenfolge, die den Ressourcennamen angibt.</span><span class="sxs-lookup"><span data-stu-id="fb40b-117">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="fb40b-118">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="fb40b-118">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="fb40b-119">Andernfalls wird der String-Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="fb40b-119">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="fb40b-120">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="fb40b-120">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="fb40b-121">*Breite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb40b-121">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb40b-122">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fb40b-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fb40b-123">Breite in Pixel.</span><span class="sxs-lookup"><span data-stu-id="fb40b-123">Width in pixels.</span></span> <span data-ttu-id="fb40b-124">Wenn dieser Wert 0 (null) oder D3DX \_ Default ist, werden die Dimensionen aus der Datei entnommen.</span><span class="sxs-lookup"><span data-stu-id="fb40b-124">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="fb40b-125">*Höhe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb40b-125">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb40b-126">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fb40b-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fb40b-127">Höhe in Pixel.</span><span class="sxs-lookup"><span data-stu-id="fb40b-127">Height, in pixels.</span></span> <span data-ttu-id="fb40b-128">Wenn dieser Wert 0 (null) oder D3DX \_ Default ist, werden die Dimensionen aus der Datei entnommen.</span><span class="sxs-lookup"><span data-stu-id="fb40b-128">If this value is zero or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="fb40b-129">*Miplevels* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb40b-129">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb40b-130">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fb40b-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fb40b-131">Anzahl der angeforderten Mip-Ebenen.</span><span class="sxs-lookup"><span data-stu-id="fb40b-131">Number of mip levels requested.</span></span> <span data-ttu-id="fb40b-132">Wenn dieser Wert 0 (null) oder D3DX \_ Default ist, wird eine komplette MipMap-Kette erstellt.</span><span class="sxs-lookup"><span data-stu-id="fb40b-132">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="fb40b-133">*Verwendung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb40b-133">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb40b-134">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fb40b-134">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fb40b-135">0, D3DUSAGE \_ renderTarget oder D3DUSAGE \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="fb40b-135">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="fb40b-136">Wenn dieses Flag auf D3DUSAGE \_ renderTarget festgelegt wird, wird angegeben, dass die Oberfläche als Renderziel verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fb40b-136">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="fb40b-137">Die Ressource kann dann an den *pnewrendertarget* -Parameter der Methode "Setup [**target**](/windows/desktop/api) " übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="fb40b-137">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="fb40b-138">Wenn entweder D3DUSAGE \_ renderTarget oder D3DUSAGE angegeben ist, muss der *Pool* auf D3DPOOL Default festgelegt werden \_ , und die Anwendung sollte überprüfen, ob das Gerät diesen Vorgang durch Aufrufen von [**CheckDeviceFormat**](/windows/desktop/api)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fb40b-138">If either D3DUSAGE\_RENDERTARGET or D3DUSAGE is specified, *Pool* must be set to D3DPOOL\_DEFAULT, and the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="fb40b-139">D3DUSAGE \_ Dynamic gibt an, dass die Oberfläche dynamisch behandelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fb40b-139">D3DUSAGE\_DYNAMIC indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="fb40b-140">Weitere Informationen zur Verwendung dynamischer Texturen finden Sie unter [Leistungsoptimierungen (Direct3D 9)](performance-optimizations.md)mithilfe dynamischer Texturen.</span><span class="sxs-lookup"><span data-stu-id="fb40b-140">For more information about using dynamic textures, see [Performance Optimizations (Direct3D 9)](performance-optimizations.md)Using Dynamic Textures.</span></span>

</dd> <dt>

<span data-ttu-id="fb40b-141">*Format* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb40b-141">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb40b-142">Typ: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="fb40b-142">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="fb40b-143">Ein Member des [D3DFORMAT](d3dformat.md) -Enumerationstyps, der das angeforderte Pixel Format für die Textur beschreibt.</span><span class="sxs-lookup"><span data-stu-id="fb40b-143">A member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="fb40b-144">Die zurückgegebene Textur kann ein anderes Format aufweisen als das, das durch das *Format* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fb40b-144">The returned texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="fb40b-145">Anwendungen sollten das Format der zurückgegebenen Textur überprüfen.</span><span class="sxs-lookup"><span data-stu-id="fb40b-145">Applications should check the format of the returned texture.</span></span> <span data-ttu-id="fb40b-146">Wenn [D3DFMT \_ Unknown](other-d3dx-constants.md)ist, wird das Format aus der Datei entnommen.</span><span class="sxs-lookup"><span data-stu-id="fb40b-146">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="fb40b-147">Wenn D3DFMT \_ from \_ File ist, wird das Format genau wie in der Datei erstellt, und der-Rückruf schlägt fehl, wenn dies die Gerätefunktionen verletzt.</span><span class="sxs-lookup"><span data-stu-id="fb40b-147">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="fb40b-148">*Pool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb40b-148">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb40b-149">Typ: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="fb40b-149">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="fb40b-150">Member des [**D3DPOOL**](./d3dpool.md) -Enumerationstyps, der die Speicher Klasse beschreibt, in der die Textur platziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="fb40b-150">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="fb40b-151">*Filter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb40b-151">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb40b-152">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fb40b-152">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fb40b-153">Eine Kombination aus einem oder mehreren [D3DX- \_ Filtern](d3dx-filter.md) , die Steuern, wie das Bild gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="fb40b-153">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="fb40b-154">Die Angabe \_ von D3DX default für diesen Parameter entspricht der Angabe von D3DX \_ Filter \_ Dreieck \| D3DX \_ Filter \_ Dither.</span><span class="sxs-lookup"><span data-stu-id="fb40b-154">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="fb40b-155">*MipFilter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb40b-155">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb40b-156">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fb40b-156">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fb40b-157">Eine Kombination aus einem oder mehreren [D3DX- \_ Filtern](d3dx-filter.md) , die Steuern, wie das Bild gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="fb40b-157">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="fb40b-158">Die Angabe \_ von D3DX default für diesen Parameter entspricht der Angabe von D3DX \_ Filter \_ Box.</span><span class="sxs-lookup"><span data-stu-id="fb40b-158">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span>

</dd> <dt>

<span data-ttu-id="fb40b-159">*Colorkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb40b-159">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb40b-160">Typ: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="fb40b-160">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="fb40b-161">[**D3DCOLOR**](d3dcolor.md) -Wert, der durch transparente schwarze ersetzt werden soll, oder 0, um den Colorkey zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="fb40b-161">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="fb40b-162">Dabei handelt es sich immer um eine 32-Bit-ARGB-Farbe, die unabhängig vom Quell Bildformat ist.</span><span class="sxs-lookup"><span data-stu-id="fb40b-162">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="fb40b-163">Alpha ist signifikant und sollte normalerweise für nicht transparente Farbtasten auf FF festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="fb40b-163">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="fb40b-164">Daher wäre der Wert für den Wert "0xFF000000" gleich.</span><span class="sxs-lookup"><span data-stu-id="fb40b-164">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="fb40b-165">*psrcinfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fb40b-165">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb40b-166">Type: **[ **D3DXIMAGE \_ Info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="fb40b-166">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="fb40b-167">Ein Zeiger auf eine [**D3DXIMAGE \_ Info**](d3dximage-info.md) -Struktur, die mit einer Beschreibung der Daten in der Quell Bilddatei gefüllt werden soll, oder **null**.</span><span class="sxs-lookup"><span data-stu-id="fb40b-167">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fb40b-168">*pPalette* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fb40b-168">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb40b-169">Typ: **[ **PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="fb40b-169">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="fb40b-170">Zeiger auf eine [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) -Struktur, die eine 256-farbige Palette darstellt, die ausgefüllt werden soll, oder **null**.</span><span class="sxs-lookup"><span data-stu-id="fb40b-170">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fb40b-171">*pptexture* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fb40b-171">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb40b-172">Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="fb40b-172">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="fb40b-173">Adresse eines Zeigers auf eine [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Schnittstelle, die das erstellte Textur Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="fb40b-173">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb40b-174">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fb40b-174">Return value</span></span>

<span data-ttu-id="fb40b-175">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fb40b-175">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fb40b-176">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fb40b-176">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fb40b-177">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ NotAvailable, D3DERR \_ ouesfvideomemory, D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="fb40b-177">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb40b-178">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb40b-178">Remarks</span></span>

<span data-ttu-id="fb40b-179">Die Compilereinstellung bestimmt auch die Funktions Version.</span><span class="sxs-lookup"><span data-stu-id="fb40b-179">The compiler setting also determines the function version.</span></span> <span data-ttu-id="fb40b-180">Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXCreateTextureFromResourceExW aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="fb40b-180">If Unicode is defined, the function call resolves to D3DXCreateTextureFromResourceExW.</span></span> <span data-ttu-id="fb40b-181">Andernfalls wird der Funktions Aufruhe in D3DXCreateTextureFromResourceExA aufgelöst, da ANSI-Zeichen folgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fb40b-181">Otherwise, the function call resolves to D3DXCreateTextureFromResourceExA because ANSI strings are being used.</span></span>

<span data-ttu-id="fb40b-182">Die Ressource, die geladen wird, muss den Typ RT \_ Bitmap oder RT \_ RCDATA aufweisen.</span><span class="sxs-lookup"><span data-stu-id="fb40b-182">The resource being loaded must be of type RT\_BITMAP or RT\_RCDATA.</span></span> <span data-ttu-id="fb40b-183">Der Ressourcentyp RT \_ RCDATA dient zum Laden von anderen Formaten als Bitmaps (z. b. TGA, JPG und DDS).</span><span class="sxs-lookup"><span data-stu-id="fb40b-183">Resource type RT\_RCDATA is used to load formats other than bitmaps (such as .tga, .jpg, and .dds).</span></span>

<span data-ttu-id="fb40b-184">Diese Funktion unterstützt die folgenden Dateiformate: BMP,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm und. TGA.</span><span class="sxs-lookup"><span data-stu-id="fb40b-184">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="fb40b-185">Siehe [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="fb40b-185">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fb40b-186">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb40b-186">Requirements</span></span>



| <span data-ttu-id="fb40b-187">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fb40b-187">Requirement</span></span> | <span data-ttu-id="fb40b-188">Wert</span><span class="sxs-lookup"><span data-stu-id="fb40b-188">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fb40b-189">Header</span><span class="sxs-lookup"><span data-stu-id="fb40b-189">Header</span></span><br/>  | <dl> <span data-ttu-id="fb40b-190"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb40b-190"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="fb40b-191">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fb40b-191">Library</span></span><br/> | <dl> <span data-ttu-id="fb40b-192"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb40b-192"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="fb40b-193">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb40b-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb40b-194">**D3DXCreateTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="fb40b-194">**D3DXCreateTextureFromResource**</span></span>](d3dxcreatetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="fb40b-195">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="fb40b-195">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
