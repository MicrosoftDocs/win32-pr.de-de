---
description: Erstellt eine volumetextur aus einer Datei.
ms.assetid: e68ac4bb-a89a-41a1-b2ba-40a1ac519e3d
title: D3DXCreateVolumeTextureFromFile-Funktion (D3dx9tex. h)
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
ms.openlocfilehash: 51ee51f1aee7a69fbd86d7f9bb2ded894dde9ead
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353363"
---
# <a name="d3dxcreatevolumetexturefromfile-function"></a><span data-ttu-id="24a55-103">D3DXCreateVolumeTextureFromFile-Funktion</span><span class="sxs-lookup"><span data-stu-id="24a55-103">D3DXCreateVolumeTextureFromFile function</span></span>

<span data-ttu-id="24a55-104">Erstellt eine volumetextur aus einer Datei.</span><span class="sxs-lookup"><span data-stu-id="24a55-104">Creates a volume texture from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="24a55-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="24a55-105">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTextureFromFile(
  _In_  LPDIRECT3DDEVICE9        pDevice,
  _In_  LPCTSTR                  pSrcFile,
  _Out_ LPDIRECT3DVOLUMETEXTURE9 *ppVolumeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="24a55-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="24a55-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24a55-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="24a55-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24a55-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="24a55-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="24a55-109">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das der volumetextur zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="24a55-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="24a55-110">*psrcfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="24a55-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24a55-111">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="24a55-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="24a55-112">Zeiger auf eine Zeichenfolge, die den Dateinamen angibt.</span><span class="sxs-lookup"><span data-stu-id="24a55-112">Pointer to a string that specifies the file name.</span></span> <span data-ttu-id="24a55-113">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="24a55-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="24a55-114">Andernfalls wird der String-Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="24a55-114">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="24a55-115">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="24a55-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="24a55-116">*ppvolumetexture* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="24a55-116">*ppVolumeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="24a55-117">Typ: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="24a55-117">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span></span>

<span data-ttu-id="24a55-118">Adresse eines Zeigers auf eine [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) -Schnittstelle, die das erstellte Textur Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="24a55-118">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24a55-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="24a55-119">Return value</span></span>

<span data-ttu-id="24a55-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="24a55-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="24a55-121">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="24a55-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="24a55-122">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ NotAvailable, D3DERR \_ ouesfvideomemory, D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="24a55-122">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="24a55-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="24a55-123">Remarks</span></span>

<span data-ttu-id="24a55-124">Die Compilereinstellung bestimmt auch die Funktions Version.</span><span class="sxs-lookup"><span data-stu-id="24a55-124">The compiler setting also determines the function version.</span></span> <span data-ttu-id="24a55-125">Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXCreateVolumeTextureFromFileW aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="24a55-125">If Unicode is defined, the function call resolves to D3DXCreateVolumeTextureFromFileW.</span></span> <span data-ttu-id="24a55-126">Andernfalls wird der Funktions Aufruhe in D3DXCreateVolumeTextureFromFileA aufgelöst, da ANSI-Zeichen folgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="24a55-126">Otherwise, the function call resolves to D3DXCreateVolumeTextureFromFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="24a55-127">Die-Funktion entspricht D3DXCreateVolumeTextureFromFileEx (pdevice, psrcfile, D3DX \_ Default, D3DX \_ Default, D3DX \_ Default, D3DX \_ Default, 0, D3DFMT \_ unknown, D3DPOOL \_ Managed, D3DX \_ Default, D3DX \_ Default, 0, **null**, **null**, ppvolumetexture).</span><span class="sxs-lookup"><span data-stu-id="24a55-127">The function is equivalent to D3DXCreateVolumeTextureFromFileEx(pDevice, pSrcFile, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppVolumeTexture).</span></span>

<span data-ttu-id="24a55-128">Diese Funktion unterstützt die folgenden Dateiformate: BMP,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm und. TGA.</span><span class="sxs-lookup"><span data-stu-id="24a55-128">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="24a55-129">Siehe [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="24a55-129">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="24a55-130">Für mipzugeordnete Texturen ist jede Ebene automatisch mit der geladenen Textur gefüllt.</span><span class="sxs-lookup"><span data-stu-id="24a55-130">Mipmapped textures automatically have each level filled with the loaded texture.</span></span>

<span data-ttu-id="24a55-131">Beim Laden von Bildern in mipzugeordnete Texturen können einige Geräte nicht zu einem 1 x1-Bild wechseln, und diese Funktion schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="24a55-131">When loading images into mipmapped textures, some devices are unable to go to a 1x1 image and this function will fail.</span></span> <span data-ttu-id="24a55-132">Wenn dies der Fall ist, müssen die Images manuell geladen werden.</span><span class="sxs-lookup"><span data-stu-id="24a55-132">If this happens, then the images need to be loaded manually.</span></span>

<span data-ttu-id="24a55-133">Beachten Sie, dass eine Ressource, die mit dieser Funktion erstellt wird, wenn Sie von einem IDirect3DDevice9-Objekt aufgerufen wird, in der Speicher Klasse platziert wird, die von D3DPOOL \_ verwaltet wird</span><span class="sxs-lookup"><span data-stu-id="24a55-133">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="24a55-134">Wenn diese Methode von einem IDirect3DDevice9Ex-Objekt aufgerufen wird, wird die Ressource in der Speicher Klasse platziert, die durch D3DPOOL default angegeben wird \_ .</span><span class="sxs-lookup"><span data-stu-id="24a55-134">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="24a55-135">Filter werden automatisch auf eine Textur angewendet, die mit dieser Methode erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="24a55-135">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="24a55-136">Die Filterung entspricht D3DX \_ Filter \_ Dreieck \| D3DX \_ Filter \_ Dither in [D3DX \_ Filter](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="24a55-136">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="24a55-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="24a55-137">Requirements</span></span>



| <span data-ttu-id="24a55-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="24a55-138">Requirement</span></span> | <span data-ttu-id="24a55-139">Wert</span><span class="sxs-lookup"><span data-stu-id="24a55-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="24a55-140">Header</span><span class="sxs-lookup"><span data-stu-id="24a55-140">Header</span></span><br/>  | <dl> <span data-ttu-id="24a55-141"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="24a55-141"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="24a55-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="24a55-142">Library</span></span><br/> | <dl> <span data-ttu-id="24a55-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="24a55-143"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="24a55-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24a55-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24a55-145">**D3DXCreateVolumeTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="24a55-145">**D3DXCreateVolumeTextureFromFileEx**</span></span>](d3dxcreatevolumetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="24a55-146">**D3DXCreateVolumeTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="24a55-146">**D3DXCreateVolumeTextureFromFileInMemory**</span></span>](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="24a55-147">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="24a55-147">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span></span>](d3dxcreatevolumetexturefromfileinmemoryex.md)
</dt> <dt>

[<span data-ttu-id="24a55-148">**D3DXCreateVolumeTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="24a55-148">**D3DXCreateVolumeTextureFromResource**</span></span>](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="24a55-149">**D3DXCreateVolumeTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="24a55-149">**D3DXCreateVolumeTextureFromResourceEx**</span></span>](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="24a55-150">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="24a55-150">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
