---
description: Erstellt eine leere cubetextur und passt die aufrufenden Parameter nach Bedarf an.
ms.assetid: 96cf3fc1-9efc-4b97-a082-2956386145c7
title: D3DXCreateCubeTexture-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8fa31945cea5e65cdf00eae512059308090bcbab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367478"
---
# <a name="d3dxcreatecubetexture-function"></a><span data-ttu-id="2ba6d-103">D3DXCreateCubeTexture-Funktion</span><span class="sxs-lookup"><span data-stu-id="2ba6d-103">D3DXCreateCubeTexture function</span></span>

<span data-ttu-id="2ba6d-104">Erstellt eine leere cubetextur und passt die aufrufenden Parameter nach Bedarf an.</span><span class="sxs-lookup"><span data-stu-id="2ba6d-104">Creates an empty cube texture, adjusting the calling parameters as needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ba6d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ba6d-105">Syntax</span></span>


```C++
HRESULT D3DXCreateCubeTexture(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  UINT                   Size,
  _In_  UINT                   MipLevels,
  _In_  DWORD                  Usage,
  _In_  D3DFORMAT              Format,
  _In_  D3DPOOL                Pool,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="2ba6d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ba6d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ba6d-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ba6d-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ba6d-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="2ba6d-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="2ba6d-109">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das der Textur zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2ba6d-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="2ba6d-110">*Größe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ba6d-110">*Size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ba6d-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ba6d-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2ba6d-112">Breite und Höhe der cubetextur in Pixel.</span><span class="sxs-lookup"><span data-stu-id="2ba6d-112">Width and height of the cube texture, in pixels.</span></span> <span data-ttu-id="2ba6d-113">Wenn es sich bei der cubetextur z. b. um einen 8-Pixel-Cube mit 8 Pixel handelt, sollte der Wert für diesen Parameter 8 lauten.</span><span class="sxs-lookup"><span data-stu-id="2ba6d-113">For example, if the cube texture is an 8-pixel by 8-pixel cube, the value for this parameter should be 8.</span></span>

</dd> <dt>

<span data-ttu-id="2ba6d-114">*Miplevels* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ba6d-114">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ba6d-115">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ba6d-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2ba6d-116">Anzahl der angeforderten Mip-Ebenen.</span><span class="sxs-lookup"><span data-stu-id="2ba6d-116">Number of mip levels requested.</span></span> <span data-ttu-id="2ba6d-117">Wenn dieser Wert 0 (null) oder D3DX \_ Default ist, wird eine komplette MipMap-Kette erstellt.</span><span class="sxs-lookup"><span data-stu-id="2ba6d-117">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="2ba6d-118">*Verwendung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ba6d-118">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ba6d-119">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ba6d-119">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2ba6d-120">0, D3DUSAGE \_ renderTarget oder D3DUSAGE \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="2ba6d-120">0, D3DUSAGE\_RENDERTARGET, or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="2ba6d-121">Wenn dieses Flag auf D3DUSAGE \_ renderTarget festgelegt wird, wird angegeben, dass die Oberfläche als Renderziel verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2ba6d-121">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="2ba6d-122">Die Ressource kann dann an den *pnewrendertarget* -Parameter der Methode "Setup [**target**](/windows/desktop/api) " übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="2ba6d-122">The resource can then be passed to the *pNewRenderTarget* parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="2ba6d-123">Wenn D3DUSAGE \_ renderTarget angegeben ist, muss die Anwendung überprüfen, ob das Gerät diesen Vorgang durch Aufrufen von [**CheckDeviceFormat**](/windows/desktop/api)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2ba6d-123">If D3DUSAGE\_RENDERTARGET is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="2ba6d-124">Weitere Informationen zur Verwendung dynamischer Texturen finden Sie unter [Verwenden dynamischer Texturen](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="2ba6d-124">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="2ba6d-125">*Format* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ba6d-125">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ba6d-126">Typ: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="2ba6d-126">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="2ba6d-127">Member des [D3DFORMAT](d3dformat.md) -Enumerationstyps, der das angeforderte Pixel Format für die cubetextur beschreibt.</span><span class="sxs-lookup"><span data-stu-id="2ba6d-127">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the cube texture.</span></span> <span data-ttu-id="2ba6d-128">Die zurückgegebene cubetextur kann ein anderes Format aufweisen als das, das durch das *Format* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2ba6d-128">The returned cube texture might have a different format from that specified by *Format*.</span></span> <span data-ttu-id="2ba6d-129">Anwendungen sollten das Format der zurückgegebenen cubetextur überprüfen.</span><span class="sxs-lookup"><span data-stu-id="2ba6d-129">Applications should check the format of the returned cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="2ba6d-130">*Pool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ba6d-130">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ba6d-131">Typ: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="2ba6d-131">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="2ba6d-132">Member des [**D3DPOOL**](./d3dpool.md) -Enumerationstyps, der die Speicher Klasse beschreibt, in der die Cubestruktur platziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="2ba6d-132">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the cube texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="2ba6d-133">*ppcubetexture* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2ba6d-133">*ppCubeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ba6d-134">Typ: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="2ba6d-134">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***</span></span>

<span data-ttu-id="2ba6d-135">Adresse eines Zeigers auf eine [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) -Schnittstelle, die das erstellte Cube-Textur Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="2ba6d-135">Address of a pointer to an [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) interface, representing the created cube texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ba6d-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2ba6d-136">Return value</span></span>

<span data-ttu-id="2ba6d-137">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2ba6d-137">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2ba6d-138">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2ba6d-138">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2ba6d-139">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcallable, D3DERR \_ NotAvailable, D3DERR \_ oudefvideomemory, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="2ba6d-139">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ba6d-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2ba6d-140">Remarks</span></span>

<span data-ttu-id="2ba6d-141">Cube-Texturen unterscheiden sich von anderen Oberflächen darin, dass es sich um Auflistungen von</span><span class="sxs-lookup"><span data-stu-id="2ba6d-141">Cube textures differ from other surfaces in that they are collections of surfaces.</span></span>

<span data-ttu-id="2ba6d-142">Intern verwendet D3DXCreateCubeTexture [**D3DXCheckCubeTextureRequirements**](d3dxcheckcubetexturerequirements.md) , um die aufrufenden Parameter anzupassen.</span><span class="sxs-lookup"><span data-stu-id="2ba6d-142">Internally, D3DXCreateCubeTexture uses [**D3DXCheckCubeTextureRequirements**](d3dxcheckcubetexturerequirements.md) to adjust the calling parameters.</span></span> <span data-ttu-id="2ba6d-143">Daher sind Aufrufe von D3DXCreateCubeTexture oft erfolgreich, wenn Aufrufe von " [**anatecubetexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) " fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="2ba6d-143">Therefore, calls to D3DXCreateCubeTexture will often succeed where calls to [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) would fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ba6d-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ba6d-144">Requirements</span></span>



| <span data-ttu-id="2ba6d-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2ba6d-145">Requirement</span></span> | <span data-ttu-id="2ba6d-146">Wert</span><span class="sxs-lookup"><span data-stu-id="2ba6d-146">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2ba6d-147">Header</span><span class="sxs-lookup"><span data-stu-id="2ba6d-147">Header</span></span><br/>  | <dl> <span data-ttu-id="2ba6d-148"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ba6d-148"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="2ba6d-149">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2ba6d-149">Library</span></span><br/> | <dl> <span data-ttu-id="2ba6d-150"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ba6d-150"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="2ba6d-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2ba6d-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ba6d-152">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="2ba6d-152">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
