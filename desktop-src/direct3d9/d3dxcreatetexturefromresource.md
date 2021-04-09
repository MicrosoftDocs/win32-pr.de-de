---
description: Erstellt eine Textur aus einer Ressource.
ms.assetid: 7c841f21-5565-4923-a2fe-bbd618616f87
title: D3DXCreateTextureFromResource-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4ce9101caed2a60dc3be7fe0039a1e391423f1fe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870103"
---
# <a name="d3dxcreatetexturefromresource-function"></a><span data-ttu-id="95dd2-103">D3DXCreateTextureFromResource-Funktion</span><span class="sxs-lookup"><span data-stu-id="95dd2-103">D3DXCreateTextureFromResource function</span></span>

<span data-ttu-id="95dd2-104">Erstellt eine Textur aus einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="95dd2-104">Creates a texture from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="95dd2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="95dd2-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureFromResource(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  HMODULE            hSrcModule,
  _In_  LPCTSTR            pSrcResource,
  _Out_ LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="95dd2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="95dd2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95dd2-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95dd2-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95dd2-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="95dd2-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="95dd2-109">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das der Textur zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="95dd2-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="95dd2-110">*hsrcmodule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95dd2-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95dd2-111">Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="95dd2-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="95dd2-112">Handle für das Modul, in dem sich die Ressource befindet, oder **null** für das Modul, das dem Image zugeordnet ist, mit dem das Betriebssystem den aktuellen Prozess erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="95dd2-112">Handle to the module where the resource is located, or **NULL** for module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="95dd2-113">*psrkresource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95dd2-113">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95dd2-114">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="95dd2-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="95dd2-115">Zeiger auf eine Zeichenfolge, die den Ressourcennamen angibt.</span><span class="sxs-lookup"><span data-stu-id="95dd2-115">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="95dd2-116">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="95dd2-116">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="95dd2-117">Andernfalls wird der String-Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="95dd2-117">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="95dd2-118">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="95dd2-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="95dd2-119">*pptexture* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="95dd2-119">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95dd2-120">Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="95dd2-120">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="95dd2-121">Adresse eines Zeigers auf eine [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Schnittstelle, die das erstellte Textur Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="95dd2-121">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95dd2-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="95dd2-122">Return value</span></span>

<span data-ttu-id="95dd2-123">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="95dd2-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="95dd2-124">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="95dd2-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="95dd2-125">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ NotAvailable, D3DERR \_ ouesfvideomemory, D3DERR \_ invalidcall, D3DXERR \_ InvalidData, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="95dd2-125">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="95dd2-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95dd2-126">Remarks</span></span>

<span data-ttu-id="95dd2-127">Die Compilereinstellung bestimmt auch die Funktions Version.</span><span class="sxs-lookup"><span data-stu-id="95dd2-127">The compiler setting also determines the function version.</span></span> <span data-ttu-id="95dd2-128">Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXCreateTextureFromResourceW aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="95dd2-128">If Unicode is defined, the function call resolves to D3DXCreateTextureFromResourceW.</span></span> <span data-ttu-id="95dd2-129">Andernfalls wird der Funktions Aufruhe in D3DXCreateTextureFromResourceA aufgelöst, da ANSI-Zeichen folgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="95dd2-129">Otherwise, the function call resolves to D3DXCreateTextureFromResourceA because ANSI strings are being used.</span></span>

<span data-ttu-id="95dd2-130">Die-Funktion entspricht D3DXCreateTextureFromResourceEx (pdevice, hsrcmodule, psrkresource, D3DX \_ Default, D3DX \_ Default, D3DX \_ Default, 0, D3DFMT \_ unknown, D3DPOOL \_ Managed, D3DX \_ Default, D3DX \_ Default, 0, **null**, **null**, pptexture).</span><span class="sxs-lookup"><span data-stu-id="95dd2-130">The function is equivalent to D3DXCreateTextureFromResourceEx(pDevice, hSrcModule, pSrcResource, D3DX\_DEFAULT, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppTexture).</span></span>

<span data-ttu-id="95dd2-131">Die Ressource, die geladen wird, muss den Typ RT \_ Bitmap oder RT \_ RCDATA aufweisen.</span><span class="sxs-lookup"><span data-stu-id="95dd2-131">The resource being loaded must be of type RT\_BITMAP or RT\_RCDATA.</span></span> <span data-ttu-id="95dd2-132">Der Ressourcentyp RT \_ RCDATA dient zum Laden von anderen Formaten als Bitmaps (z. b. TGA, JPG und DDS).</span><span class="sxs-lookup"><span data-stu-id="95dd2-132">Resource type RT\_RCDATA is used to load formats other than bitmaps (such as .tga, .jpg, and .dds).</span></span>

<span data-ttu-id="95dd2-133">Diese Funktion unterstützt die folgenden Dateiformate: BMP,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm und. TGA.</span><span class="sxs-lookup"><span data-stu-id="95dd2-133">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="95dd2-134">Siehe [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="95dd2-134">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="95dd2-135">Beachten Sie, dass eine Ressource, die mit dieser Funktion erstellt wird, wenn Sie von einem IDirect3DDevice9-Objekt aufgerufen wird, in der Speicher Klasse platziert wird, die von D3DPOOL \_ verwaltet wird</span><span class="sxs-lookup"><span data-stu-id="95dd2-135">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="95dd2-136">Wenn diese Methode von einem IDirect3DDevice9Ex-Objekt aufgerufen wird, wird die Ressource in der Speicher Klasse platziert, die durch D3DPOOL default angegeben wird \_ .</span><span class="sxs-lookup"><span data-stu-id="95dd2-136">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="95dd2-137">Filter werden automatisch auf eine Textur angewendet, die mit dieser Methode erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="95dd2-137">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="95dd2-138">Die Filterung entspricht D3DX \_ Filter \_ Dreieck \| D3DX \_ Filter \_ Dither in [D3DX \_ Filter](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="95dd2-138">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="95dd2-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95dd2-139">Requirements</span></span>



| <span data-ttu-id="95dd2-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95dd2-140">Requirement</span></span> | <span data-ttu-id="95dd2-141">Wert</span><span class="sxs-lookup"><span data-stu-id="95dd2-141">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95dd2-142">Header</span><span class="sxs-lookup"><span data-stu-id="95dd2-142">Header</span></span><br/>  | <dl> <span data-ttu-id="95dd2-143"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="95dd2-143"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="95dd2-144">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="95dd2-144">Library</span></span><br/> | <dl> <span data-ttu-id="95dd2-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="95dd2-145"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="95dd2-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95dd2-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95dd2-147">**D3DXCreateTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="95dd2-147">**D3DXCreateTextureFromResourceEx**</span></span>](d3dxcreatetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="95dd2-148">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="95dd2-148">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
