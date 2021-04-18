---
description: Erstellt eine cubetextur aus einer Datei.
ms.assetid: 7ff3b051-568c-4c77-b8a6-b626ba156eb1
title: D3DXCreateCubeTextureFromFile-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2071a1d1e16e769d1a0623138e24c2e0fbab85e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351965"
---
# <a name="d3dxcreatecubetexturefromfile-function"></a><span data-ttu-id="2867b-103">D3DXCreateCubeTextureFromFile-Funktion</span><span class="sxs-lookup"><span data-stu-id="2867b-103">D3DXCreateCubeTextureFromFile function</span></span>

<span data-ttu-id="2867b-104">Erstellt eine cubetextur aus einer Datei.</span><span class="sxs-lookup"><span data-stu-id="2867b-104">Creates a cube texture from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="2867b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2867b-105">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTextureFromFile(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  LPCTSTR                pSrcFile,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="2867b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2867b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2867b-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2867b-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2867b-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="2867b-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="2867b-109">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das der cubetextur zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2867b-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="2867b-110">*psrcfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2867b-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2867b-111">Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2867b-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2867b-112">Zeiger auf eine Zeichenfolge, die den Dateinamen angibt.</span><span class="sxs-lookup"><span data-stu-id="2867b-112">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="2867b-113">Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="2867b-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="2867b-114">Andernfalls wird der String-Datentyp in LPCSTR aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="2867b-114">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="2867b-115">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="2867b-115">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2867b-116">*ppcubetexture* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2867b-116">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2867b-117">Typ: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="2867b-117">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="2867b-118">Adresse eines Zeigers auf eine [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) -Schnittstelle, die das erstellte Cube-Textur Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="2867b-118">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2867b-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2867b-119">Return value</span></span>

<span data-ttu-id="2867b-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2867b-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2867b-121">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2867b-121">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2867b-122">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcallcenter, D3DERR \_ NotAvailable, D3DERR \_ oudefvideomemory, D3DXERR \_ InvalidData, E \_ ouyfmemory.</span><span class="sxs-lookup"><span data-stu-id="2867b-122">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="2867b-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2867b-123">Remarks</span></span>

<span data-ttu-id="2867b-124">Die Compilereinstellung bestimmt auch die Funktions Version.</span><span class="sxs-lookup"><span data-stu-id="2867b-124">The compiler setting also determines the function version.</span></span> <span data-ttu-id="2867b-125">Wenn Unicode definiert ist, wird der Funktions aufrufin **D3DXCreateCubeTextureFromFileW** aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="2867b-125">If Unicode is defined, the function call resolves to **D3DXCreateCubeTextureFromFileW**.</span></span> <span data-ttu-id="2867b-126">Andernfalls wird der Funktions Aufruhe in **D3DXCreateCubeTextureFromFileA** aufgelöst, da ANSI-Zeichen folgen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2867b-126">Otherwise, the function call resolves to **D3DXCreateCubeTextureFromFileA** because ANSI strings are being used.</span></span>

<span data-ttu-id="2867b-127">Die-Funktion entspricht D3DXCreateCubeTextureFromFileEx (pdevice, psrcfile, D3DX \_ Default, D3DX \_ Default, 0, D3DFMT \_ unknown, D3DPOOL \_ Managed, D3DX \_ Default, D3DX \_ Default, 0, **null**, **null**, ppcubetexture).</span><span class="sxs-lookup"><span data-stu-id="2867b-127">The function is equivalent to D3DXCreateCubeTextureFromFileEx(pDevice, pSrcFile, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, D3DFMT\_UNKNOWN, D3DPOOL\_MANAGED, D3DX\_DEFAULT, D3DX\_DEFAULT, 0, **NULL**, **NULL**, ppCubeTexture).</span></span>

<span data-ttu-id="2867b-128">Diese Funktion unterstützt die folgenden Dateiformate: BMP,. DDS,. DIB,. HDR,. jpg,. PFM,. png,. ppm und. TGA.</span><span class="sxs-lookup"><span data-stu-id="2867b-128">This function supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="2867b-129">Siehe [**D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="2867b-129">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="2867b-130">Beachten Sie, dass eine Ressource, die mit dieser Funktion erstellt wird, wenn Sie von einem IDirect3DDevice9-Objekt aufgerufen wird, in der Speicher Klasse platziert wird, die von D3DPOOL \_ verwaltet wird</span><span class="sxs-lookup"><span data-stu-id="2867b-130">Note that a resource created with this function when called from a IDirect3DDevice9 object will be placed in the memory class denoted by D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="2867b-131">Wenn diese Methode von einem IDirect3DDevice9Ex-Objekt aufgerufen wird, wird die Ressource in der Speicher Klasse platziert, die durch D3DPOOL default angegeben wird \_ .</span><span class="sxs-lookup"><span data-stu-id="2867b-131">When this method is called from a IDirect3DDevice9Ex object the resource will be placed in the memory class denoted by D3DPOOL\_DEFAULT.</span></span>

<span data-ttu-id="2867b-132">Filter werden automatisch auf eine Textur angewendet, die mit dieser Methode erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="2867b-132">Filtering is automatically applied to a texture created using this method.</span></span> <span data-ttu-id="2867b-133">Die Filterung entspricht D3DX \_ Filter \_ Dreieck \| D3DX \_ Filter \_ Dither in [D3DX \_ Filter](d3dx-filter.md).</span><span class="sxs-lookup"><span data-stu-id="2867b-133">The filtering is equivalent to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER in [D3DX\_FILTER](d3dx-filter.md).</span></span>

<span data-ttu-id="2867b-134">**D3DXCreateCubeTextureFromFile** verwendet das DDS-Dateiformat (DirectDraw Surface).</span><span class="sxs-lookup"><span data-stu-id="2867b-134">**D3DXCreateCubeTextureFromFile** uses the DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="2867b-135">Mit dem DirectX-Textur-Editor (Dxtex.exe) können Sie eine cubemap aus anderen Dateiformaten generieren und im DDS-Dateiformat speichern.</span><span class="sxs-lookup"><span data-stu-id="2867b-135">The DirectX Texture Editor (Dxtex.exe) enables you to generate a cube map from other file formats and save it in the DDS file format.</span></span> <span data-ttu-id="2867b-136">Sie erhalten Dxtex.exe und erfahren mehr über das DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="2867b-136">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="2867b-137">Weitere Informationen zum DirectX SDK finden Sie unter [wo ist das DirectX SDK?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="2867b-137">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2867b-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2867b-138">Requirements</span></span>



| <span data-ttu-id="2867b-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2867b-139">Requirement</span></span> | <span data-ttu-id="2867b-140">Wert</span><span class="sxs-lookup"><span data-stu-id="2867b-140">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2867b-141">Header</span><span class="sxs-lookup"><span data-stu-id="2867b-141">Header</span></span><br/>  | <dl> <span data-ttu-id="2867b-142"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="2867b-142"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="2867b-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2867b-143">Library</span></span><br/> | <dl> <span data-ttu-id="2867b-144"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2867b-144"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="2867b-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2867b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2867b-146">**D3DXCreateCubeTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="2867b-146">**D3DXCreateCubeTextureFromFileEx**</span></span>](d3dxcreatecubetexturefromfileex.md)
</dt> <dt>

[<span data-ttu-id="2867b-147">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="2867b-147">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
