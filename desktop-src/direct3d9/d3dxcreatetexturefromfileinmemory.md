---
description: Erstellt eine Textur aus einer Datei im Arbeitsspeicher.
ms.assetid: 3ea811be-7db8-4436-b138-f0102389bb4d
title: D3DXCreateTextureFromFileInMemory-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 743a944da52bc6d2ae13b045f854d95b4751712d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762066"
---
# <a name="d3dxcreatetexturefromfileinmemory-function"></a><span data-ttu-id="98af8-103">D3DXCreateTextureFromFileInMemory-Funktion</span><span class="sxs-lookup"><span data-stu-id="98af8-103">D3DXCreateTextureFromFileInMemory function</span></span>

<span data-ttu-id="98af8-104">Erstellt eine Textur aus einer Datei im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="98af8-104">Creates a texture from a file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="98af8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="98af8-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureFromFileInMemory(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  LPCVOID            pSrcData,
  _In_  UINT               SrcDataSize,
  _Out_ LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="98af8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="98af8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98af8-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="98af8-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98af8-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="98af8-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="98af8-109">Ein Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das der Textur zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="98af8-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="98af8-110">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="98af8-110">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98af8-111">Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="98af8-111">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="98af8-112">Ein Zeiger auf die Datei im Arbeitsspeicher, von der die Textur erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="98af8-112">Pointer to the file in memory from which to create the texture.</span></span>

</dd> <dt>

<span data-ttu-id="98af8-113">*Srcdatasize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="98af8-113">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="98af8-114">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="98af8-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="98af8-115">Größe der Datei in Bytes im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="98af8-115">Size in bytes of the file in memory.</span></span>

</dd> <dt>

<span data-ttu-id="98af8-116">*pptexture* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="98af8-116">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="98af8-117">Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="98af8-117">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="98af8-118">Adresse eines Zeigers auf eine [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Schnittstelle, die das erstellte Textur Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="98af8-118">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98af8-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="98af8-119">Return value</span></span>

<span data-ttu-id="98af8-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="98af8-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="98af8-121">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="98af8-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="98af8-122">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ NotAvailable, D3DERR \_ ouesfvideomemory, D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="98af8-122">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="98af8-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="98af8-123">Remarks</span></span>

<span data-ttu-id="98af8-124">Die-Funktion entspricht D3DXCreateTextureFromFileInMemoryEx (pdevice, pSrcData, srcdatasize, D3DX \_ Default, D3DX \_ Default, D3DX \_ Default, 0, D3DFMT \_ unknown, D3DPOOL \_ Managed, D3DX \_ Default, D3DX \_ Default, 0, **null**, **null**, pptexture).</span><span class="sxs-lookup"><span data-stu-id="98af8-124">The function is equivalent to D3DXCreateTextureFromFileInMemoryEx(pDevice, pSrcData, SrcDataSize, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppTexture).</span></span>

<span data-ttu-id="98af8-125">Diese Funktion unterstützt die folgenden Dateiformate: BMP,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm und. TGA.</span><span class="sxs-lookup"><span data-stu-id="98af8-125">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="98af8-126">Siehe [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="98af8-126">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="98af8-127">Beachten Sie, dass eine Ressource, die mit dieser Funktion erstellt wird, wenn Sie von einem IDirect3DDevice9-Objekt aufgerufen wird, in der Speicher Klasse platziert wird, die von D3DPOOL \_ verwaltet wird</span><span class="sxs-lookup"><span data-stu-id="98af8-127">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="98af8-128">Wenn diese Methode von einem IDirect3DDevice9Ex-Objekt aufgerufen wird, wird die Ressource in der Speicher Klasse platziert, die durch D3DPOOL default angegeben wird \_ .</span><span class="sxs-lookup"><span data-stu-id="98af8-128">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="98af8-129">Filter werden automatisch auf eine Textur angewendet, die mit dieser Methode erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="98af8-129">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="98af8-130">Die Filterung entspricht D3DX \_ Filter \_ Dreieck \| D3DX \_ Filter \_ Dither in [D3DX \_ Filter](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="98af8-130">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="98af8-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98af8-131">Requirements</span></span>



| <span data-ttu-id="98af8-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="98af8-132">Requirement</span></span> | <span data-ttu-id="98af8-133">Wert</span><span class="sxs-lookup"><span data-stu-id="98af8-133">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="98af8-134">Header</span><span class="sxs-lookup"><span data-stu-id="98af8-134">Header</span></span><br/>  | <dl> <span data-ttu-id="98af8-135"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="98af8-135"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="98af8-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="98af8-136">Library</span></span><br/> | <dl> <span data-ttu-id="98af8-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="98af8-137"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="98af8-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="98af8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98af8-139">**D3DXCreateTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="98af8-139">**D3DXCreateTextureFromFileInMemoryEx**</span></span>](d3dxcreatetexturefromfileinmemoryex.md)
</dt> <dt>

[<span data-ttu-id="98af8-140">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="98af8-140">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
