---
description: Erstellt eine cubetextur aus einer Datei im Arbeitsspeicher.
ms.assetid: f7e99d5a-5479-4f0b-b040-bb07e7e37666
title: D3DXCreateCubeTextureFromFileInMemory-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3f1d6de3fba0dcbda959a2811ec665ebc4a6541c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353735"
---
# <a name="d3dxcreatecubetexturefromfileinmemory-function"></a><span data-ttu-id="ed676-103">D3DXCreateCubeTextureFromFileInMemory-Funktion</span><span class="sxs-lookup"><span data-stu-id="ed676-103">D3DXCreateCubeTextureFromFileInMemory function</span></span>

<span data-ttu-id="ed676-104">Erstellt eine cubetextur aus einer Datei im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="ed676-104">Creates a cube texture from a file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed676-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed676-105">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTextureFromFileInMemory(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  LPCVOID                pSrcData,
  _In_  UINT                   SrcDataSize,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="ed676-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed676-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed676-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed676-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed676-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="ed676-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="ed676-109">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das der cubetextur zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed676-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="ed676-110">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed676-110">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed676-111">Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed676-111">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed676-112">Zeiger auf die Datei im Arbeitsspeicher, von der die cubemap erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed676-112">Pointer to the file in memory from which to create the cubemap.</span></span> <span data-ttu-id="ed676-113">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="ed676-113">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ed676-114">*Srcdatasize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed676-114">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed676-115">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ed676-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ed676-116">Größe der Datei im Arbeitsspeicher in Bytes.</span><span class="sxs-lookup"><span data-stu-id="ed676-116">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ed676-117">*ppcubetexture* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ed676-117">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed676-118">Typ: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="ed676-118">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="ed676-119">Adresse eines Zeigers auf eine [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) -Schnittstelle, die das erstellte Cube-Textur Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="ed676-119">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed676-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ed676-120">Return value</span></span>

<span data-ttu-id="ed676-121">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ed676-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ed676-122">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ed676-122">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ed676-123">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcallable, D3DERR \_ NotAvailable, D3DERR \_ oudefvideomemory, D3DXERR \_ InvalidData, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="ed676-123">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed676-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ed676-124">Remarks</span></span>

<span data-ttu-id="ed676-125">Diese Funktion unterstützt die folgenden Dateiformate: BMP,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm und. TGA.</span><span class="sxs-lookup"><span data-stu-id="ed676-125">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="ed676-126">Siehe [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="ed676-126">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="ed676-127">Die-Funktion entspricht D3DXCreateCubeTextureFromFileInMemoryEx (pdevice, pSrcData, srcdatasize, D3DX \_ Default, D3DX \_ Default, 0, D3DFMT \_ unknown, D3DPOOL \_ Managed, D3DX \_ Default, D3DX \_ Default, 0, **null**, **null**, ppcubetexture).</span><span class="sxs-lookup"><span data-stu-id="ed676-127">The function is equivalent to D3DXCreateCubeTextureFromFileInMemoryEx(pDevice, pSrcData, SrcDataSize, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppCubeTexture).</span></span>

<span data-ttu-id="ed676-128">Beachten Sie, dass eine Ressource, die mit dieser Funktion erstellt wird, wenn Sie von einem IDirect3DDevice9-Objekt aufgerufen wird, in der Speicher Klasse platziert wird, die von D3DPOOL \_ verwaltet wird</span><span class="sxs-lookup"><span data-stu-id="ed676-128">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="ed676-129">Wenn diese Methode von einem IDirect3DDevice9Ex-Objekt aufgerufen wird, wird die Ressource in der Speicher Klasse platziert, die durch D3DPOOL default angegeben wird \_ .</span><span class="sxs-lookup"><span data-stu-id="ed676-129">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="ed676-130">Diese Methode ist für das Laden von Bilddateien konzipiert, die als RT \_ RCDATA gespeichert werden. Dies ist eine Anwendungs definierte Ressource (Rohdaten).</span><span class="sxs-lookup"><span data-stu-id="ed676-130">This method is designed to be used for loading image files stored as RT\_RCDATA, which is an application-defined resource (raw data).</span></span> <span data-ttu-id="ed676-131">Andernfalls schlägt diese Methode fehl.</span><span class="sxs-lookup"><span data-stu-id="ed676-131">Otherwise this method will fail.</span></span>

<span data-ttu-id="ed676-132">Filter werden automatisch auf eine Textur angewendet, die mit dieser Methode erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="ed676-132">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="ed676-133">Die Filterung entspricht D3DX \_ Filter \_ Dreieck \| D3DX \_ Filter \_ Dither in [D3DX \_ Filter](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="ed676-133">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

<span data-ttu-id="ed676-134">**D3DXCreateCubeTextureFromFileInMemory** verwendet das DDS-Dateiformat (DirectDraw Surface).</span><span class="sxs-lookup"><span data-stu-id="ed676-134">**D3DXCreateCubeTextureFromFileInMemory** uses the DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="ed676-135">Mit dem DirectX-Textur-Editor (Dxtex.exe) können Sie eine cubemap aus anderen Dateiformaten generieren und im DDS-Dateiformat speichern.</span><span class="sxs-lookup"><span data-stu-id="ed676-135">The DirectX Texture Editor (Dxtex.exe) enables you to generate a cube map from other file formats and save it in the DDS file format.</span></span> <span data-ttu-id="ed676-136">Sie erhalten Dxtex.exe und erfahren mehr über das DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="ed676-136">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="ed676-137">Weitere Informationen zum DirectX SDK finden Sie unter [wo ist das DirectX SDK?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="ed676-137">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ed676-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed676-138">Requirements</span></span>



| <span data-ttu-id="ed676-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed676-139">Requirement</span></span> | <span data-ttu-id="ed676-140">Wert</span><span class="sxs-lookup"><span data-stu-id="ed676-140">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ed676-141">Header</span><span class="sxs-lookup"><span data-stu-id="ed676-141">Header</span></span><br/>  | <dl> <span data-ttu-id="ed676-142"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed676-142"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="ed676-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ed676-143">Library</span></span><br/> | <dl> <span data-ttu-id="ed676-144"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ed676-144"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ed676-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed676-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed676-146">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="ed676-146">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
