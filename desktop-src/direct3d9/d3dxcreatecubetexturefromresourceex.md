---
description: Erstellt eine cubetextur aus einer Ressource, die durch eine Zeichenfolge angegeben wird. Dies ist eine erweiterte Funktion als D3DXCreateCubeTextureFromResource.
ms.assetid: 4d263386-8270-4967-8ef5-e9ac69e502a5
title: D3DXCreateCubeTextureFromResourceEx-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromResourceEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4ed77556681e2ad43302b8608dc213b3ad0f0209
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355676"
---
# <a name="d3dxcreatecubetexturefromresourceex-function"></a><span data-ttu-id="5b078-104">D3DXCreateCubeTextureFromResourceEx-Funktion</span><span class="sxs-lookup"><span data-stu-id="5b078-104">D3DXCreateCubeTextureFromResourceEx function</span></span>

<span data-ttu-id="5b078-105">Erstellt eine cubetextur aus einer Ressource, die durch eine Zeichenfolge angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5b078-105">Creates a cube texture from a resource specified by a string.</span></span> <span data-ttu-id="5b078-106">Dies ist eine erweiterte Funktion als [**D3DXCreateCubeTextureFromResource**](d3dxcreatecubetexturefromresource.md).</span><span class="sxs-lookup"><span data-stu-id="5b078-106">This is a more advanced function than [**D3DXCreateCubeTextureFromResource**](d3dxcreatecubetexturefromresource.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5b078-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b078-107">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTextureFromResourceEx(
  _In_    LPDIRECT3DDEVICE9      pDevice,
  _In_    HMODULE                hSrcModule,
  _In_    LPCTSTR                pSrcResource,
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



## <a name="parameters"></a><span data-ttu-id="5b078-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b078-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b078-109">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b078-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b078-110">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="5b078-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="5b078-111">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das der cubetextur zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5b078-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="5b078-112">*hsrcmodule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b078-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b078-113">Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5b078-113">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5b078-114">Handle für das Modul, in dem sich die Ressource befindet, oder **null** für das Modul, das dem Image zugeordnet ist, das zum Erstellen des aktuellen Prozesses verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="5b078-114">Handle to the module where the resource is located, or **NULL** for the module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="5b078-115">*psrkresource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b078-115">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b078-116">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5b078-116">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5b078-117">Zeiger auf eine Zeichenfolge, die den Ressourcennamen angibt.</span><span class="sxs-lookup"><span data-stu-id="5b078-117">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="5b078-118">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="5b078-118">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="5b078-119">Andernfalls wird der String-Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="5b078-119">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="5b078-120">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="5b078-120">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5b078-121">*Größe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b078-121">*Size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b078-122">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5b078-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5b078-123">Breite und Höhe der cubetextur in Pixel.</span><span class="sxs-lookup"><span data-stu-id="5b078-123">Width and height of the cube texture, in pixels.</span></span> <span data-ttu-id="5b078-124">Wenn es sich bei der cubetextur z. b. um einen 8-Pixel-Cube mit 8 Pixel handelt, sollte der Wert für diesen Parameter 8 lauten.</span><span class="sxs-lookup"><span data-stu-id="5b078-124">For example, if the cube texture is an 8-pixel by 8-pixel cube, the value for this parameter should be 8.</span></span> <span data-ttu-id="5b078-125">Wenn dieser Wert 0 oder D3DX \_ Default ist, werden die Dimensionen aus der Datei entnommen.</span><span class="sxs-lookup"><span data-stu-id="5b078-125">If this value is 0 or D3DX\_DEFAULT, the dimensions are taken from the file.</span></span>

</dd> <dt>

<span data-ttu-id="5b078-126">*Miplevels* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b078-126">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b078-127">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5b078-127">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5b078-128">Anzahl der angeforderten Mip-Ebenen.</span><span class="sxs-lookup"><span data-stu-id="5b078-128">Number of mip levels requested.</span></span> <span data-ttu-id="5b078-129">Wenn dieser Wert 0 (null) oder D3DX \_ Default ist, wird eine komplette MipMap-Kette erstellt.</span><span class="sxs-lookup"><span data-stu-id="5b078-129">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="5b078-130">*Verwendung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b078-130">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b078-131">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5b078-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5b078-132">0 oder D3DUSAGE \_ renderTarget oder D3DUSAGE \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="5b078-132">0 or D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="5b078-133">Wenn dieses Flag auf D3DUSAGE \_ renderTarget festgelegt wird, wird angegeben, dass die Oberfläche als Renderziel verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5b078-133">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="5b078-134">Die Ressource kann dann an den *pnewrendertarget* -Parameter der Methode "Setup [**target**](/windows/desktop/api) " übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="5b078-134">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="5b078-135">Wenn D3DUSAGE \_ renderTarget angegeben ist, muss die Anwendung überprüfen, ob das Gerät diesen Vorgang durch Aufrufen von [**CheckDeviceFormat**](/windows/desktop/api)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5b078-135">If D3DUSAGE\_RENDERTARGET is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="5b078-136">D3DUSAGE \_ Dynamic gibt an, dass die Oberfläche dynamisch behandelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5b078-136">D3DUSAGE\_DYNAMIC indicates that the surface should be handled dynamically.</span></span> <span data-ttu-id="5b078-137">Weitere Informationen zur Verwendung dynamischer Texturen finden Sie unter [Verwenden dynamischer Texturen](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="5b078-137">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b078-138">*Format* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b078-138">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b078-139">Typ: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="5b078-139">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="5b078-140">Member des [D3DFORMAT](d3dformat.md) -Enumerationstyps, der das angeforderte Pixel Format für die cubetextur beschreibt.</span><span class="sxs-lookup"><span data-stu-id="5b078-140">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the cube texture.</span></span> <span data-ttu-id="5b078-141">Die zurückgegebene cubetextur kann ein anderes Format aufweisen als das, das durch das *Format* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5b078-141">The returned cube texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="5b078-142">Anwendungen sollten das Format der zurückgegebenen cubetextur überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5b078-142">Applications should check the format of the returned cube texture.</span></span> <span data-ttu-id="5b078-143">Wenn [D3DFMT \_ Unknown](other-d3dx-constants.md)ist, wird das Format aus der Datei entnommen.</span><span class="sxs-lookup"><span data-stu-id="5b078-143">If [D3DFMT\_UNKNOWN](other-d3dx-constants.md), the format is taken from the file.</span></span> <span data-ttu-id="5b078-144">Wenn D3DFMT \_ from \_ File ist, wird das Format genau wie in der Datei erstellt, und der-Rückruf schlägt fehl, wenn dies die Gerätefunktionen verletzt.</span><span class="sxs-lookup"><span data-stu-id="5b078-144">If D3DFMT\_FROM\_FILE, the format is taken exactly as it is in the file, and the call will fail if this violates device capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="5b078-145">*Pool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b078-145">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b078-146">Typ: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="5b078-146">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="5b078-147">Member des [**D3DPOOL**](./d3dpool.md) -Enumerationstyps, der die Speicher Klasse beschreibt, in der die Cubestruktur platziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5b078-147">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the cube texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="5b078-148">*Filter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b078-148">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b078-149">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5b078-149">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5b078-150">Eine Kombination aus einem oder mehreren [D3DX- \_ Filtern](d3dx-filter.md), die steuert, wie das Bild gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="5b078-150">A combination of one or more [D3DX\_FILTER](d3dx-filter.md), controlling how the image is filtered.</span></span> <span data-ttu-id="5b078-151">Die Angabe \_ von D3DX default für diesen Parameter entspricht der Angabe von D3DX \_ Filter \_ Dreieck \| D3DX \_ Filter \_ Dither.</span><span class="sxs-lookup"><span data-stu-id="5b078-151">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="5b078-152">*MipFilter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b078-152">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b078-153">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5b078-153">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5b078-154">Eine Kombination aus einem oder mehreren [D3DX- \_ Filtern](d3dx-filter.md) , die Steuern, wie das Bild gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="5b078-154">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="5b078-155">Die Angabe \_ von D3DX default für diesen Parameter entspricht der Angabe von D3DX \_ Filter \_ Box.</span><span class="sxs-lookup"><span data-stu-id="5b078-155">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX.</span></span>

</dd> <dt>

<span data-ttu-id="5b078-156">*Colorkey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b078-156">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b078-157">Typ: **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="5b078-157">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="5b078-158">[**D3DCOLOR**](d3dcolor.md) -Wert, der durch transparente schwarze ersetzt werden soll, oder 0, um den Colorkey zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="5b078-158">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="5b078-159">Dabei handelt es sich immer um eine 32-Bit-ARGB-Farbe, die unabhängig vom Quell Bildformat ist.</span><span class="sxs-lookup"><span data-stu-id="5b078-159">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="5b078-160">Alpha ist signifikant und sollte normalerweise für nicht transparente Farbtasten auf FF festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="5b078-160">Alpha is significant, and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="5b078-161">Daher wäre der Wert für den Wert "0xFF000000" gleich.</span><span class="sxs-lookup"><span data-stu-id="5b078-161">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="5b078-162">*psrcinfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5b078-162">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b078-163">Type: **[ **D3DXIMAGE \_ Info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="5b078-163">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="5b078-164">Ein Zeiger auf eine [**D3DXIMAGE \_ Info**](d3dximage-info.md) -Struktur, die mit einer Beschreibung der Daten in der Quell Bilddatei gefüllt werden soll, oder **null**.</span><span class="sxs-lookup"><span data-stu-id="5b078-164">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5b078-165">*pPalette* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5b078-165">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b078-166">Typ: **[ **PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span><span class="sxs-lookup"><span data-stu-id="5b078-166">Type: **[**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="5b078-167">Zeiger auf eine [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) -Struktur, die eine 256-farbige Palette darstellt, die ausgefüllt werden soll, oder **null**.</span><span class="sxs-lookup"><span data-stu-id="5b078-167">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, representing a 256-color palette to fill in or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5b078-168">*ppcubetexture* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5b078-168">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b078-169">Typ: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="5b078-169">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="5b078-170">Adresse eines Zeigers auf eine [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) -Schnittstelle, die das erstellte Cube-Textur Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="5b078-170">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b078-171">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5b078-171">Return value</span></span>

<span data-ttu-id="5b078-172">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5b078-172">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5b078-173">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5b078-173">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5b078-174">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcallable, D3DERR \_ NotAvailable, D3DERR \_ oudefvideomemory, D3DXERR \_ InvalidData, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="5b078-174">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b078-175">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b078-175">Remarks</span></span>

<span data-ttu-id="5b078-176">Die Compilereinstellung bestimmt die Funktions Version.</span><span class="sxs-lookup"><span data-stu-id="5b078-176">The compiler setting determines the function version.</span></span> <span data-ttu-id="5b078-177">Wenn Unicode definiert ist, wird der Funktions aufrufin **D3DXCreateCubeTextureFromResourceExW** aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="5b078-177">If Unicode is defined, the function call resolves to **D3DXCreateCubeTextureFromResourceExW**.</span></span> <span data-ttu-id="5b078-178">Andernfalls wird der Funktions Aufruhe in **D3DXCreateCubeTextureFromResourceExA** aufgelöst, da ANSI-Zeichen folgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5b078-178">Otherwise, the function call resolves to **D3DXCreateCubeTextureFromResourceExA** because ANSI strings are being used.</span></span>

<span data-ttu-id="5b078-179">Diese Funktion unterstützt die folgenden Dateiformate: BMP,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm und. TGA.</span><span class="sxs-lookup"><span data-stu-id="5b078-179">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="5b078-180">Siehe [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="5b078-180">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="5b078-181">Cube-Texturen unterscheiden sich von anderen Oberflächen darin, dass es sich um Auflistungen von</span><span class="sxs-lookup"><span data-stu-id="5b078-181">Cube textures differ from other surfaces in that they are collections of surfaces.</span></span> <span data-ttu-id="5b078-182">Um "\*" mit einer cubetextur aufzurufen, müssen Sie ein einzelnes Gesicht [**mithilfe von "**](/windows/desktop/api) [**getcubemapsurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) " auswählen und die resultierende Oberfläche an " **strendertarget**" übergeben.</span><span class="sxs-lookup"><span data-stu-id="5b078-182">To call [**SetRenderTarget**](/windows/desktop/api) with a cube texture, you must select an individual face using [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) and pass the resulting surface to **SetRenderTarget**.</span></span>

<span data-ttu-id="5b078-183">**D3DXCreateCubeTextureFromResourceEx** verwendet das DDS-Dateiformat (DirectDraw Surface).</span><span class="sxs-lookup"><span data-stu-id="5b078-183">**D3DXCreateCubeTextureFromResourceEx** uses the DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="5b078-184">Mit dem DirectX-Textur-Editor (Dxtex.exe) können Sie eine cubemap aus anderen Dateiformaten generieren und im DDS-Dateiformat speichern.</span><span class="sxs-lookup"><span data-stu-id="5b078-184">The DirectX Texture Editor (Dxtex.exe) enables you to generate a cube map from other file formats and save it in the DDS file format.</span></span> <span data-ttu-id="5b078-185">Sie erhalten Dxtex.exe und erfahren mehr über das DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="5b078-185">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="5b078-186">Weitere Informationen zum DirectX SDK finden Sie unter [wo ist das DirectX SDK?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="5b078-186">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5b078-187">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5b078-187">Requirements</span></span>



| <span data-ttu-id="5b078-188">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5b078-188">Requirement</span></span> | <span data-ttu-id="5b078-189">Wert</span><span class="sxs-lookup"><span data-stu-id="5b078-189">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5b078-190">Header</span><span class="sxs-lookup"><span data-stu-id="5b078-190">Header</span></span><br/>  | <dl> <span data-ttu-id="5b078-191"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b078-191"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="5b078-192">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5b078-192">Library</span></span><br/> | <dl> <span data-ttu-id="5b078-193"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5b078-193"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="5b078-194">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b078-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b078-195">**D3DXCreateCubeTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="5b078-195">**D3DXCreateCubeTextureFromResource**</span></span>](d3dxcreatecubetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="5b078-196">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="5b078-196">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
