---
description: Erstellt eine cubetextur aus einer Ressource.
ms.assetid: 9153944a-af8b-4365-9e91-fc1136a84caa
title: D3DXCreateCubeTextureFromResource-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c0bd65799bada2df8a3c9e0b113db3c911a53536
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351964"
---
# <a name="d3dxcreatecubetexturefromresource-function"></a><span data-ttu-id="b0a47-103">D3DXCreateCubeTextureFromResource-Funktion</span><span class="sxs-lookup"><span data-stu-id="b0a47-103">D3DXCreateCubeTextureFromResource function</span></span>

<span data-ttu-id="b0a47-104">Erstellt eine cubetextur aus einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="b0a47-104">Creates a cube texture from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0a47-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0a47-105">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTextureFromResource(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  HMODULE                hSrcModule,
  _In_  LPCTSTR                pSrcResource,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="b0a47-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0a47-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0a47-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b0a47-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0a47-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="b0a47-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="b0a47-109">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das der cubetextur zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b0a47-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="b0a47-110">*hsrcmodule* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b0a47-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0a47-111">Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0a47-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b0a47-112">Handle für das Modul, in dem sich die Ressource befindet, oder **null** für das Modul, das dem Image zugeordnet ist, das zum Erstellen des aktuellen Prozesses verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="b0a47-112">Handle to the module where the resource is located, or **NULL** for the module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="b0a47-113">*psrkresource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b0a47-113">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0a47-114">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0a47-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b0a47-115">Zeiger auf eine Zeichenfolge, die den Ressourcennamen angibt.</span><span class="sxs-lookup"><span data-stu-id="b0a47-115">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="b0a47-116">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="b0a47-116">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="b0a47-117">Andernfalls wird der String-Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="b0a47-117">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="b0a47-118">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="b0a47-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="b0a47-119">*ppcubetexture* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b0a47-119">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0a47-120">Typ: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="b0a47-120">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="b0a47-121">Adresse eines Zeigers auf eine [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) -Schnittstelle, die das erstellte Cube-Textur Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="b0a47-121">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0a47-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b0a47-122">Return value</span></span>

<span data-ttu-id="b0a47-123">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b0a47-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b0a47-124">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b0a47-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b0a47-125">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcallcenter, D3DERR \_ NotAvailable, D3DERR \_ oudefvideomemory, D3DXERR \_ InvalidData, E \_ ouyfmemory.</span><span class="sxs-lookup"><span data-stu-id="b0a47-125">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0a47-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b0a47-126">Remarks</span></span>

<span data-ttu-id="b0a47-127">Die Compilereinstellung bestimmt die Funktions Version.</span><span class="sxs-lookup"><span data-stu-id="b0a47-127">The compiler setting determines the function version.</span></span> <span data-ttu-id="b0a47-128">Wenn Unicode definiert ist, wird der Funktions aufrufin **D3DXCreateCubeTextureFromResourceW** aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="b0a47-128">If Unicode is defined, the function call resolves to **D3DXCreateCubeTextureFromResourceW**.</span></span> <span data-ttu-id="b0a47-129">Andernfalls wird der Funktions Aufruhe in **D3DXCreateCubeTextureFromResourceA** aufgelöst, da ANSI-Zeichen folgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b0a47-129">Otherwise, the function call resolves to **D3DXCreateCubeTextureFromResourceA** because ANSI strings are being used.</span></span>

<span data-ttu-id="b0a47-130">Die-Funktion entspricht D3DXCreateCubeTextureFromResourceEx (pdevice, hsrcmodule, psrkresource, D3DX \_ Default, D3DX \_ Default, 0, D3DFMT \_ unknown, D3DPOOL \_ Managed, D3DX \_ Default, D3DX \_ Default, 0, **null**, **null**, ppcubetexture).</span><span class="sxs-lookup"><span data-stu-id="b0a47-130">The function is equivalent to D3DXCreateCubeTextureFromResourceEx(pDevice, hSrcModule, pSrcResource, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppCubeTexture).</span></span>

<span data-ttu-id="b0a47-131">Diese Funktion unterstützt die folgenden Dateiformate: BMP,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm und. TGA.</span><span class="sxs-lookup"><span data-stu-id="b0a47-131">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="b0a47-132">Siehe [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="b0a47-132">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="b0a47-133">Beachten Sie, dass eine Ressource, die mit dieser Funktion erstellt wird, wenn Sie von einem IDirect3DDevice9-Objekt aufgerufen wird, in der Speicher Klasse platziert wird, die von D3DPOOL \_ verwaltet wird</span><span class="sxs-lookup"><span data-stu-id="b0a47-133">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="b0a47-134">Wenn diese Methode von einem IDirect3DDevice9Ex-Objekt aufgerufen wird, wird die Ressource in der Speicher Klasse platziert, die durch D3DPOOL default angegeben wird \_ .</span><span class="sxs-lookup"><span data-stu-id="b0a47-134">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="b0a47-135">Filter werden automatisch auf eine Textur angewendet, die mit dieser Methode erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="b0a47-135">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="b0a47-136">Die Filterung entspricht D3DX \_ Filter \_ Dreieck \| D3DX \_ Filter \_ Dither in [D3DX \_ Filter](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="b0a47-136">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

<span data-ttu-id="b0a47-137">**D3DXCreateCubeTextureFromResource** verwendet das DDS-Dateiformat (DirectDraw Surface).</span><span class="sxs-lookup"><span data-stu-id="b0a47-137">**D3DXCreateCubeTextureFromResource** uses the DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="b0a47-138">Mit dem DirectX-Textur-Editor (Dxtex.exe) können Sie eine cubemap aus anderen Dateiformaten generieren und im DDS-Dateiformat speichern.</span><span class="sxs-lookup"><span data-stu-id="b0a47-138">The DirectX Texture Editor (Dxtex.exe) enables you to generate a cube map from other file formats and save it in the DDS file format.</span></span> <span data-ttu-id="b0a47-139">Sie erhalten Dxtex.exe und erfahren mehr über das DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="b0a47-139">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="b0a47-140">Weitere Informationen zum DirectX SDK finden Sie unter [wo ist das DirectX SDK?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="b0a47-140">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b0a47-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b0a47-141">Requirements</span></span>



| <span data-ttu-id="b0a47-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b0a47-142">Requirement</span></span> | <span data-ttu-id="b0a47-143">Wert</span><span class="sxs-lookup"><span data-stu-id="b0a47-143">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b0a47-144">Header</span><span class="sxs-lookup"><span data-stu-id="b0a47-144">Header</span></span><br/>  | <dl> <span data-ttu-id="b0a47-145"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0a47-145"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="b0a47-146">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b0a47-146">Library</span></span><br/> | <dl> <span data-ttu-id="b0a47-147"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b0a47-147"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b0a47-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0a47-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0a47-149">**D3DXCreateCubeTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="b0a47-149">**D3DXCreateCubeTextureFromResourceEx**</span></span>](d3dxcreatecubetexturefromresourceex.md)
</dt> <dt>

[<span data-ttu-id="b0a47-150">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="b0a47-150">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
