---
description: Erstellt eine volumetextur aus einer Ressource.
ms.assetid: 82a0b7aa-69fa-450d-b0d2-769f05fd75ea
title: D3DXCreateVolumeTextureFromResource-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a5f0a0faf97f773c3174ced22ec7259091d6e07e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530908"
---
# <a name="d3dxcreatevolumetexturefromresource-function"></a><span data-ttu-id="d31ec-103">D3DXCreateVolumeTextureFromResource-Funktion</span><span class="sxs-lookup"><span data-stu-id="d31ec-103">D3DXCreateVolumeTextureFromResource function</span></span>

<span data-ttu-id="d31ec-104">Erstellt eine volumetextur aus einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="d31ec-104">Creates a volume texture from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="d31ec-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d31ec-105">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTextureFromResource(
  _In_  LPDIRECT3DDEVICE9        pDevice,
  _In_  HMODULE                  hSrcModule,
  _In_  LPCTSTR                  pSrcResource,
  _Out_ LPDIRECT3DVOLUMETEXTURE9 *ppVolumeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="d31ec-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d31ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d31ec-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d31ec-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d31ec-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="d31ec-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="d31ec-109">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das der volumetextur zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d31ec-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="d31ec-110">*hsrcmodule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d31ec-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d31ec-111">Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d31ec-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d31ec-112">Handle für das Modul, in dem sich die Ressource befindet, oder **null** für das Modul, das dem Image zugeordnet ist, das zum Erstellen des aktuellen Prozesses verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="d31ec-112">Handle to the module where the resource is located, or **NULL** for the module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="d31ec-113">*psrkresource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d31ec-113">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d31ec-114">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d31ec-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d31ec-115">Zeiger auf eine Zeichenfolge, die den Ressourcennamen angibt.</span><span class="sxs-lookup"><span data-stu-id="d31ec-115">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="d31ec-116">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="d31ec-116">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="d31ec-117">Andernfalls wird der String-Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="d31ec-117">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="d31ec-118">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="d31ec-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="d31ec-119">*ppvolumetexture* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d31ec-119">*ppVolumeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d31ec-120">Typ: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="d31ec-120">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span></span>

<span data-ttu-id="d31ec-121">Adresse eines Zeigers auf eine [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) -Schnittstelle, die das erstellte Textur Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="d31ec-121">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d31ec-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d31ec-122">Return value</span></span>

<span data-ttu-id="d31ec-123">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d31ec-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d31ec-124">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d31ec-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d31ec-125">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ NotAvailable, D3DERR \_ ouesfvideomemory, D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="d31ec-125">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="d31ec-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d31ec-126">Remarks</span></span>

<span data-ttu-id="d31ec-127">Die Compilereinstellung bestimmt auch die Funktions Version.</span><span class="sxs-lookup"><span data-stu-id="d31ec-127">The compiler setting also determines the function version.</span></span> <span data-ttu-id="d31ec-128">Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXCreateVolumeTextureFromResourceW aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="d31ec-128">If Unicode is defined, the function call resolves to D3DXCreateVolumeTextureFromResourceW.</span></span> <span data-ttu-id="d31ec-129">Andernfalls wird der Funktions Aufruhe in D3DXCreateVolumeTextureFromResourceA aufgelöst, da ANSI-Zeichen folgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d31ec-129">Otherwise, the function call resolves to D3DXCreateVolumeTextureFromResourceA because ANSI strings are being used.</span></span>

<span data-ttu-id="d31ec-130">Die-Funktion entspricht D3DXCreateVolumeTextureFromResourceEx (pdevice, hsrcmodule, psrkresource, D3DX \_ Default, D3DX \_ Default, D3DX \_ Default, D3DX \_ Default, 0, D3DFMT \_ unknown, D3DPOOL \_ Managed, D3DX \_ Default, D3DX \_ Default, 0, **null**, **null**, ppvolumetexture).</span><span class="sxs-lookup"><span data-stu-id="d31ec-130">The function is equivalent to D3DXCreateVolumeTextureFromResourceEx(pDevice, hSrcModule, pSrcResource, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppVolumeTexture).</span></span>

<span data-ttu-id="d31ec-131">Die Ressource, die geladen wird, muss eine von der Anwendung definierte Ressource (RT \_ RCDATA) sein.</span><span class="sxs-lookup"><span data-stu-id="d31ec-131">The resource being loaded must be an application-defined resource (RT\_RCDATA).</span></span>

<span data-ttu-id="d31ec-132">Diese Funktion unterstützt die folgenden Dateiformate: BMP,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm und. TGA.</span><span class="sxs-lookup"><span data-stu-id="d31ec-132">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="d31ec-133">Siehe [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="d31ec-133">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="d31ec-134">Beachten Sie, dass eine Ressource, die mit dieser Funktion erstellt wird, wenn Sie von einem IDirect3DDevice9-Objekt aufgerufen wird, in der Speicher Klasse platziert wird, die von D3DPOOL \_ verwaltet wird</span><span class="sxs-lookup"><span data-stu-id="d31ec-134">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="d31ec-135">Wenn diese Methode von einem IDirect3DDevice9Ex-Objekt aufgerufen wird, wird die Ressource in der Speicher Klasse platziert, die durch D3DPOOL default angegeben wird \_ .</span><span class="sxs-lookup"><span data-stu-id="d31ec-135">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="d31ec-136">Filter werden automatisch auf eine Textur angewendet, die mit dieser Methode erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d31ec-136">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="d31ec-137">Die Filterung entspricht D3DX \_ Filter \_ Dreieck \| D3DX \_ Filter \_ Dither in [D3DX \_ Filter](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="d31ec-137">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d31ec-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d31ec-138">Requirements</span></span>



| <span data-ttu-id="d31ec-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d31ec-139">Requirement</span></span> | <span data-ttu-id="d31ec-140">Wert</span><span class="sxs-lookup"><span data-stu-id="d31ec-140">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d31ec-141">Header</span><span class="sxs-lookup"><span data-stu-id="d31ec-141">Header</span></span><br/>  | <dl> <span data-ttu-id="d31ec-142"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="d31ec-142"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="d31ec-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d31ec-143">Library</span></span><br/> | <dl> <span data-ttu-id="d31ec-144"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d31ec-144"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="d31ec-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d31ec-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d31ec-146">**D3DXCreateVolumeTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="d31ec-146">**D3DXCreateVolumeTextureFromFile**</span></span>](d3dxcreatevolumetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="d31ec-147">**D3DXCreateVolumeTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="d31ec-147">**D3DXCreateVolumeTextureFromFileEx**</span></span>](d3dxcreatevolumetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="d31ec-148">**D3DXCreateVolumeTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="d31ec-148">**D3DXCreateVolumeTextureFromFileInMemory**</span></span>](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="d31ec-149">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="d31ec-149">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span></span>](d3dxcreatevolumetexturefromfileinmemoryex.md)
</dt> <dt>

[<span data-ttu-id="d31ec-150">**D3DXCreateVolumeTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="d31ec-150">**D3DXCreateVolumeTextureFromResourceEx**</span></span>](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="d31ec-151">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="d31ec-151">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
