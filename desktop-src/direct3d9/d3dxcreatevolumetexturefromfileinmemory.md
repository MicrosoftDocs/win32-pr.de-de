---
description: Erstellt eine volumetextur aus einer Datei im Arbeitsspeicher.
ms.assetid: 8ea22209-6110-4bef-a0d6-667f59017adc
title: D3DXCreateVolumeTextureFromFileInMemory-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 380aadd9e26940b2a67c2064b3941a0965a782f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762060"
---
# <a name="d3dxcreatevolumetexturefromfileinmemory-function"></a><span data-ttu-id="47c4c-103">D3DXCreateVolumeTextureFromFileInMemory-Funktion</span><span class="sxs-lookup"><span data-stu-id="47c4c-103">D3DXCreateVolumeTextureFromFileInMemory function</span></span>

<span data-ttu-id="47c4c-104">Erstellt eine volumetextur aus einer Datei im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="47c4c-104">Creates a volume texture from a file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="47c4c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="47c4c-105">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTextureFromFileInMemory(
  _In_  LPDIRECT3DDEVICE9        pDevice,
  _In_  LPCVOID                  pSrcFile,
  _In_  UINT                     SrcData,
  _Out_ LPDIRECT3DVOLUMETEXTURE9 ppVolumeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="47c4c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="47c4c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47c4c-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="47c4c-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47c4c-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="47c4c-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="47c4c-109">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das der volumetextur zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="47c4c-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="47c4c-110">*psrcfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="47c4c-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47c4c-111">Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="47c4c-111">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="47c4c-112">Ein Zeiger auf die Datei im Arbeitsspeicher, von der die Volumestruktur erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="47c4c-112">Pointer to the file in memory from which to create the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="47c4c-113">*Srcdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="47c4c-113">*SrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47c4c-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="47c4c-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="47c4c-115">Größe der Datei im Arbeitsspeicher in Bytes.</span><span class="sxs-lookup"><span data-stu-id="47c4c-115">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="47c4c-116">*ppvolumetexture* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="47c4c-116">*ppVolumeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="47c4c-117">Typ: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**</span><span class="sxs-lookup"><span data-stu-id="47c4c-117">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)**</span></span>

<span data-ttu-id="47c4c-118">Adresse eines Zeigers auf eine [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) -Schnittstelle, die das erstellte Textur Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="47c4c-118">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47c4c-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="47c4c-119">Return value</span></span>

<span data-ttu-id="47c4c-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="47c4c-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="47c4c-121">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="47c4c-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="47c4c-122">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ NotAvailable, D3DERR \_ ouesfvideomemory, D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="47c4c-122">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="47c4c-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47c4c-123">Remarks</span></span>

<span data-ttu-id="47c4c-124">Diese Funktion unterstützt die folgenden Dateiformate: BMP,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm und. TGA.</span><span class="sxs-lookup"><span data-stu-id="47c4c-124">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="47c4c-125">Siehe [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="47c4c-125">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="47c4c-126">Die-Funktion entspricht D3DXCreateVolumeTextureFromFileInMemoryEx (pdevice, psrcfile, srcdata, D3DX \_ Default, D3DX \_ Default, D3DX \_ Default, D3DX \_ Default, 0, D3DFMT \_ unknown, D3DPOOL \_ Managed, D3DX \_ Default, D3DX \_ Default, 0, **null**, **null**, ppvolumetexture).</span><span class="sxs-lookup"><span data-stu-id="47c4c-126">The function is equivalent to D3DXCreateVolumeTextureFromFileInMemoryEx(pDevice, pSrcFile, SrcData, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppVolumeTexture).</span></span>

<span data-ttu-id="47c4c-127">Beachten Sie, dass eine Ressource, die mit dieser Funktion erstellt wird, wenn Sie von einem IDirect3DDevice9-Objekt aufgerufen wird, in der Speicher Klasse platziert wird, die von D3DPOOL \_ verwaltet wird</span><span class="sxs-lookup"><span data-stu-id="47c4c-127">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="47c4c-128">Wenn diese Methode von einem IDirect3DDevice9Ex-Objekt aufgerufen wird, wird die Ressource in der Speicher Klasse platziert, die durch D3DPOOL default angegeben wird \_ .</span><span class="sxs-lookup"><span data-stu-id="47c4c-128">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="47c4c-129">Filter werden automatisch auf eine Textur angewendet, die mit dieser Methode erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="47c4c-129">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="47c4c-130">Die Filterung entspricht D3DX \_ Filter \_ Dreieck \| D3DX \_ Filter \_ Dither in [D3DX \_ Filter](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="47c4c-130">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="47c4c-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="47c4c-131">Requirements</span></span>



| <span data-ttu-id="47c4c-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="47c4c-132">Requirement</span></span> | <span data-ttu-id="47c4c-133">Wert</span><span class="sxs-lookup"><span data-stu-id="47c4c-133">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="47c4c-134">Header</span><span class="sxs-lookup"><span data-stu-id="47c4c-134">Header</span></span><br/>  | <dl> <span data-ttu-id="47c4c-135"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="47c4c-135"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="47c4c-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="47c4c-136">Library</span></span><br/> | <dl> <span data-ttu-id="47c4c-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="47c4c-137"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="47c4c-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="47c4c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47c4c-139">**D3DXCreateVolumeTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="47c4c-139">**D3DXCreateVolumeTextureFromFile**</span></span>](d3dxcreatevolumetexturefromfile.md)
</dt> <dt>

[<span data-ttu-id="47c4c-140">**D3DXCreateVolumeTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="47c4c-140">**D3DXCreateVolumeTextureFromFileEx**</span></span>](d3dxcreatevolumetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="47c4c-141">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="47c4c-141">**D3DXCreateVolumeTextureFromFileInMemoryEx**</span></span>](d3dxcreatevolumetexturefromfileinmemoryex.md)
</dt> <dt>

[<span data-ttu-id="47c4c-142">**D3DXCreateVolumeTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="47c4c-142">**D3DXCreateVolumeTextureFromResource**</span></span>](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[<span data-ttu-id="47c4c-143">**D3DXCreateVolumeTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="47c4c-143">**D3DXCreateVolumeTextureFromResourceEx**</span></span>](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="47c4c-144">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="47c4c-144">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
