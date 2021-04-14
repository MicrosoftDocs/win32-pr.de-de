---
description: Erstellt eine Textur aus einer Datei.
ms.assetid: 247b0ee2-ee31-4090-b94c-41951b46675f
title: D3DXCreateTextureFromFile-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 19453986405ee4d46a3e72145c2117bb113663bd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394129"
---
# <a name="d3dxcreatetexturefromfile-function"></a><span data-ttu-id="79f12-103">D3DXCreateTextureFromFile-Funktion</span><span class="sxs-lookup"><span data-stu-id="79f12-103">D3DXCreateTextureFromFile function</span></span>

<span data-ttu-id="79f12-104">Erstellt eine Textur aus einer Datei.</span><span class="sxs-lookup"><span data-stu-id="79f12-104">Creates a texture from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="79f12-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="79f12-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureFromFile(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  LPCTSTR            pSrcFile,
  _Out_ LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="79f12-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="79f12-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79f12-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="79f12-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79f12-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="79f12-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="79f12-109">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das der Textur zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="79f12-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="79f12-110">*psrcfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="79f12-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79f12-111">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="79f12-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="79f12-112">Zeiger auf eine Zeichenfolge, die den Dateinamen angibt.</span><span class="sxs-lookup"><span data-stu-id="79f12-112">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="79f12-113">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="79f12-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="79f12-114">Andernfalls wird der String-Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="79f12-114">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="79f12-115">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="79f12-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="79f12-116">*pptexture* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="79f12-116">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79f12-117">Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="79f12-117">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="79f12-118">Adresse eines Zeigers auf eine [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Schnittstelle, die das erstellte Textur Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="79f12-118">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79f12-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="79f12-119">Return value</span></span>

<span data-ttu-id="79f12-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="79f12-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="79f12-121">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="79f12-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="79f12-122">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ NotAvailable, D3DERR \_ ouesfvideomemory, D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="79f12-122">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="79f12-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="79f12-123">Remarks</span></span>

<span data-ttu-id="79f12-124">Die Compilereinstellung bestimmt auch die Funktions Version.</span><span class="sxs-lookup"><span data-stu-id="79f12-124">The compiler setting also determines the function version.</span></span> <span data-ttu-id="79f12-125">Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXCreateTextureFromFileW aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="79f12-125">If Unicode is defined, the function call resolves to D3DXCreateTextureFromFileW.</span></span> <span data-ttu-id="79f12-126">Andernfalls wird der Funktions Aufruhe in D3DXCreateTextureFromFileA aufgelöst, da ANSI-Zeichen folgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="79f12-126">Otherwise, the function call resolves to D3DXCreateTextureFromFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="79f12-127">Diese Funktion unterstützt die folgenden Dateiformate: BMP,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm und. TGA.</span><span class="sxs-lookup"><span data-stu-id="79f12-127">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="79f12-128">Siehe [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="79f12-128">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="79f12-129">Die-Funktion entspricht D3DXCreateTextureFromFileEx (pdevice, psrcfile, D3DX \_ Default, D3DX \_ Default, D3DX \_ Default, 0, D3DFMT \_ unknown, D3DPOOL \_ Managed, D3DX \_ Default, D3DX \_ Default, 0, **null**, **null**, pptexture).</span><span class="sxs-lookup"><span data-stu-id="79f12-129">The function is equivalent to D3DXCreateTextureFromFileEx(pDevice, pSrcFile, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppTexture).</span></span>

<span data-ttu-id="79f12-130">Für mipzugeordnete Texturen ist jede Ebene automatisch mit der geladenen Textur gefüllt.</span><span class="sxs-lookup"><span data-stu-id="79f12-130">Mipmapped textures automatically have each level filled with the loaded texture.</span></span>

<span data-ttu-id="79f12-131">Beim Laden von Bildern in mipzugeordnete Texturen können einige Geräte nicht zu einem 1 x1-Bild wechseln, und diese Funktion schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="79f12-131">When loading images into mipmapped textures, some devices are unable to go to a 1x1 image and this function will fail.</span></span> <span data-ttu-id="79f12-132">Wenn dies der Fall ist, müssen die Images manuell geladen werden.</span><span class="sxs-lookup"><span data-stu-id="79f12-132">If this happens, the images need to be loaded manually.</span></span>

<span data-ttu-id="79f12-133">Beachten Sie, dass eine mit dieser Funktion erstellte Ressource in der Speicher Klasse platziert wird, die von D3DPOOL Managed angegeben wird \_ .</span><span class="sxs-lookup"><span data-stu-id="79f12-133">Note that a resource created with this function will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span>

<span data-ttu-id="79f12-134">Filter werden automatisch auf eine Textur angewendet, die mit dieser Methode erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="79f12-134">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="79f12-135">Die Filterung entspricht D3DX \_ Filter \_ Dreieck \| D3DX \_ Filter \_ Dither in [D3DX \_ Filter](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="79f12-135">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

<span data-ttu-id="79f12-136">Optimale Leistung bei der Verwendung von **D3DXCreateTextureFromFile**:</span><span class="sxs-lookup"><span data-stu-id="79f12-136">For the best performance when using **D3DXCreateTextureFromFile**:</span></span>

1.  <span data-ttu-id="79f12-137">Die Bildskalierung und die Formatkonvertierung zur Ladezeit können langsam sein.</span><span class="sxs-lookup"><span data-stu-id="79f12-137">Doing image scaling and format conversion at load time can be slow.</span></span> <span data-ttu-id="79f12-138">Speichern Sie Images im Format und in der Lösung, die Sie verwenden werden.</span><span class="sxs-lookup"><span data-stu-id="79f12-138">Store images in the format and resolution they will be used.</span></span> <span data-ttu-id="79f12-139">Wenn die Zielhardware eine Potenz von zwei Dimensionen erfordert, erstellen und speichern Sie Images mit zwei Dimensionen.</span><span class="sxs-lookup"><span data-stu-id="79f12-139">If the target hardware requires power of two dimensions, create and store images using power of two dimensions.</span></span>
2.  <span data-ttu-id="79f12-140">Verwenden Sie ggf. DirectDraw Surface (DDS)-Dateien.</span><span class="sxs-lookup"><span data-stu-id="79f12-140">Consider using DirectDraw surface (DDS) files.</span></span> <span data-ttu-id="79f12-141">Da DDS-Dateien verwendet werden können, um ein beliebiges Direct3D 9-Textur Format darzustellen, sind Sie für D3DX sehr leicht lesbar.</span><span class="sxs-lookup"><span data-stu-id="79f12-141">Because DDS files can be used to represent any Direct3D 9 texture format, they are very easy for D3DX to read.</span></span> <span data-ttu-id="79f12-142">Außerdem können Sie MipMaps speichern, sodass alle MipMap-Generierungs Algorithmen zum Erstellen der Images verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="79f12-142">Also, they can store mipmaps, so any mipmap-generation algorithms can be used to author the images.</span></span>

## <a name="requirements"></a><span data-ttu-id="79f12-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79f12-143">Requirements</span></span>



| <span data-ttu-id="79f12-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="79f12-144">Requirement</span></span> | <span data-ttu-id="79f12-145">Wert</span><span class="sxs-lookup"><span data-stu-id="79f12-145">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="79f12-146">Header</span><span class="sxs-lookup"><span data-stu-id="79f12-146">Header</span></span><br/>  | <dl> <span data-ttu-id="79f12-147"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="79f12-147"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="79f12-148">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="79f12-148">Library</span></span><br/> | <dl> <span data-ttu-id="79f12-149"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="79f12-149"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="79f12-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79f12-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79f12-151">**D3DXCreateTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="79f12-151">**D3DXCreateTextureFromFileEx**</span></span>](d3dxcreatetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="79f12-152">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="79f12-152">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
