---
description: 'D3DXCreateVolumeTextureFromFile-Funktion: Erstellt eine Volumetextur aus einer Datei.'
ms.assetid: e68ac4bb-a89a-41a1-b2ba-40a1ac519e3d
title: D3DXCreateVolumeTextureFromFile-Funktion (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7c9355148c0b91a03aabe863fb20b3e312e30784
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094301"
---
# <a name="d3dxcreatevolumetexturefromfile-function"></a><span data-ttu-id="820dc-103">D3DXCreateVolumeTextureFromFile-Funktion</span><span class="sxs-lookup"><span data-stu-id="820dc-103">D3DXCreateVolumeTextureFromFile function</span></span>

<span data-ttu-id="820dc-104">Erstellt eine Volumetextur aus einer Datei.</span><span class="sxs-lookup"><span data-stu-id="820dc-104">Creates a volume texture from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="820dc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="820dc-105">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTextureFromFile(
  _In_  LPDIRECT3DDEVICE9        pDevice,
  _In_  LPCTSTR                  pSrcFile,
  _Out_ LPDIRECT3DVOLUMETEXTURE9 *ppVolumeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="820dc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="820dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="820dc-107">*pDevice* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="820dc-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="820dc-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="820dc-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="820dc-109">Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) die das Gerät darstellt, das der Volumetextur zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="820dc-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="820dc-110">*pSrcFile* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="820dc-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="820dc-111">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="820dc-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="820dc-112">Zeiger auf eine Zeichenfolge, die den Dateinamen angibt.</span><span class="sxs-lookup"><span data-stu-id="820dc-112">Pointer to a string that specifies the file name.</span></span> <span data-ttu-id="820dc-113">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR auflösen.</span><span class="sxs-lookup"><span data-stu-id="820dc-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="820dc-114">Andernfalls wird der Zeichenfolgendatentyp in LPCSTR auflösen.</span><span class="sxs-lookup"><span data-stu-id="820dc-114">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="820dc-115">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="820dc-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="820dc-116">*ppVolumeTexture* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="820dc-116">*ppVolumeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="820dc-117">Typ: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="820dc-117">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span></span>

<span data-ttu-id="820dc-118">Adresse eines Zeigers auf eine [**IDirect3DVolumeTexture9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) die das erstellte Texturobjekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="820dc-118">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="820dc-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="820dc-119">Return value</span></span>

<span data-ttu-id="820dc-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="820dc-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="820dc-121">Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="820dc-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="820dc-122">Wenn bei der Funktion ein Fehler auftritt, kann der Rückgabewert einen der folgenden Werte haben: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="820dc-122">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="820dc-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="820dc-123">Remarks</span></span>

<span data-ttu-id="820dc-124">Die Compilereinstellung bestimmt auch die Funktionsversion.</span><span class="sxs-lookup"><span data-stu-id="820dc-124">The compiler setting also determines the function version.</span></span> <span data-ttu-id="820dc-125">Wenn Unicode definiert ist, wird der Funktionsaufruf in D3DXCreateVolumeTextureFromFileW auflösen.</span><span class="sxs-lookup"><span data-stu-id="820dc-125">If Unicode is defined, the function call resolves to D3DXCreateVolumeTextureFromFileW.</span></span> <span data-ttu-id="820dc-126">Andernfalls wird der Funktionsaufruf in D3DXCreateVolumeTextureFromFileA aufgelöst, da ANSI-Zeichenfolgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="820dc-126">Otherwise, the function call resolves to D3DXCreateVolumeTextureFromFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="820dc-127">Die Funktion entspricht D3DXCreateVolumeTextureFromFileEx(pDevice, pSrcFile, D3DX \_ DEFAULT, D3DX \_ DEFAULT, D3DX \_ DEFAULT, D3DX \_ DEFAULT, 0, D3DFMT \_ UNKNOWN, D3DPOOL \_ MANAGED, D3DX \_ DEFAULT, D3DX \_ DEFAULT, 0, **NULL,** **NULL,** ppVolumeTexture).</span><span class="sxs-lookup"><span data-stu-id="820dc-127">The function is equivalent to D3DXCreateVolumeTextureFromFileEx(pDevice, pSrcFile, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppVolumeTexture).</span></span>

<span data-ttu-id="820dc-128">Diese Funktion unterstützt die folgenden Dateiformate: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm und .tga.</span><span class="sxs-lookup"><span data-stu-id="820dc-128">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="820dc-129">Siehe [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="820dc-129">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="820dc-130">Bei Mipmapped-Texturen wird jede Ebene automatisch mit der geladenen Textur gefüllt.</span><span class="sxs-lookup"><span data-stu-id="820dc-130">Mipmapped textures automatically have each level filled with the loaded texture.</span></span>

<span data-ttu-id="820dc-131">Beim Laden von Bildern in mipmapped Texturen können einige Geräte nicht zu einem 1x1-Bild wechseln, und diese Funktion schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="820dc-131">When loading images into mipmapped textures, some devices are unable to go to a 1x1 image and this function will fail.</span></span> <span data-ttu-id="820dc-132">In diesem Fall müssen die Images manuell geladen werden.</span><span class="sxs-lookup"><span data-stu-id="820dc-132">If this happens, then the images need to be loaded manually.</span></span>

<span data-ttu-id="820dc-133">Beachten Sie, dass eine Ressource, die mit dieser Funktion erstellt wird, wenn sie von einem IDirect3DDevice9-Objekt aufgerufen wird, in der Speicherklasse platziert wird, die von D3DPOOL MANAGED bezeichnet \_ wird.</span><span class="sxs-lookup"><span data-stu-id="820dc-133">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="820dc-134">Wenn diese Methode von einem IDirect3DDevice9Ex-Objekt aufgerufen wird, wird die Ressource in der Speicherklasse platziert, die durch D3DPOOL DEFAULT gekennzeichnet \_ wird.</span><span class="sxs-lookup"><span data-stu-id="820dc-134">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="820dc-135">Die Filterung wird automatisch auf eine Textur angewendet, die mit dieser Methode erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="820dc-135">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="820dc-136">Die Filterung entspricht D3DX \_ FILTER \_ TRIANGLE \| D3DX \_ FILTER \_ DITHER in [D3DX \_ FILTER](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="820dc-136">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="820dc-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="820dc-137">Requirements</span></span>



| <span data-ttu-id="820dc-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="820dc-138">Requirement</span></span> | <span data-ttu-id="820dc-139">Wert</span><span class="sxs-lookup"><span data-stu-id="820dc-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="820dc-140">Header</span><span class="sxs-lookup"><span data-stu-id="820dc-140">Header</span></span><br/>  | <dl> <span data-ttu-id="820dc-141"><dt>D3dx9tex.h</dt></span><span class="sxs-lookup"><span data-stu-id="820dc-141"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="820dc-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="820dc-142">Library</span></span><br/> | <dl> <span data-ttu-id="820dc-143"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="820dc-143"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="820dc-144">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="820dc-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="820dc-145">**D3DXCreateVolumeTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="820dc-145">**D3DXCreateVolumeTextureFromFileEx**</span></span>](d3dxcreatevolumetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="820dc-146">**D3DXCreateVolumeTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="820dc-146">**D3DXCreateVolumeTextureFromFileInMemory**</span></span>](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="820dc-147">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="820dc-147">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span></span>](d3dxcreatevolumetexturefromfileinmemoryex.md)
</dt> <dt>

[<span data-ttu-id="820dc-148">**D3DXCreateVolumeTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="820dc-148">**D3DXCreateVolumeTextureFromResource**</span></span>](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="820dc-149">**D3DXCreateVolumeTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="820dc-149">**D3DXCreateVolumeTextureFromResourceEx**</span></span>](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="820dc-150">Texturfunktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="820dc-150">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
