---
description: Erstellt eine leere Textur und passt die aufrufenden Parameter nach Bedarf an.
ms.assetid: ea028aa9-4f37-4625-9e07-9072ec1a61d0
title: D3DXCreateTexture-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ecbd5cbb94355af9c1e51e6c7e8fc31a862b03be
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530917"
---
# <a name="d3dxcreatetexture-function"></a><span data-ttu-id="53b88-103">D3DXCreateTexture-Funktion</span><span class="sxs-lookup"><span data-stu-id="53b88-103">D3DXCreateTexture function</span></span>

<span data-ttu-id="53b88-104">Erstellt eine leere Textur und passt die aufrufenden Parameter nach Bedarf an.</span><span class="sxs-lookup"><span data-stu-id="53b88-104">Creates an empty texture, adjusting the calling parameters as needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="53b88-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="53b88-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTexture(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  UINT               Width,
  _In_  UINT               Height,
  _In_  UINT               MipLevels,
  _In_  DWORD              Usage,
  _In_  D3DFORMAT          Format,
  _In_  D3DPOOL            Pool,
  _Out_ LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a><span data-ttu-id="53b88-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="53b88-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53b88-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53b88-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53b88-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="53b88-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="53b88-109">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das der Textur zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="53b88-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the texture.</span></span>

</dd> <dt>

<span data-ttu-id="53b88-110">*Breite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53b88-110">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53b88-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53b88-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="53b88-112">Breite in Pixel.</span><span class="sxs-lookup"><span data-stu-id="53b88-112">Width in pixels.</span></span> <span data-ttu-id="53b88-113">Wenn dieser Wert 0 ist, wird der Wert 1 verwendet.</span><span class="sxs-lookup"><span data-stu-id="53b88-113">If this value is 0, a value of 1 is used.</span></span> <span data-ttu-id="53b88-114">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="53b88-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="53b88-115">*Höhe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53b88-115">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53b88-116">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53b88-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="53b88-117">Höhe in Pixel.</span><span class="sxs-lookup"><span data-stu-id="53b88-117">Height in pixels.</span></span> <span data-ttu-id="53b88-118">Wenn dieser Wert 0 ist, wird der Wert 1 verwendet.</span><span class="sxs-lookup"><span data-stu-id="53b88-118">If this value is 0, a value of 1 is used.</span></span> <span data-ttu-id="53b88-119">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="53b88-119">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="53b88-120">*Miplevels* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53b88-120">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53b88-121">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53b88-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="53b88-122">Anzahl der angeforderten Mip-Ebenen.</span><span class="sxs-lookup"><span data-stu-id="53b88-122">Number of mip levels requested.</span></span> <span data-ttu-id="53b88-123">Wenn dieser Wert 0 (null) oder D3DX \_ Default ist, wird eine komplette MipMap-Kette erstellt.</span><span class="sxs-lookup"><span data-stu-id="53b88-123">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="53b88-124">*Verwendung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53b88-124">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53b88-125">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53b88-125">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="53b88-126">0, [**D3DUSAGE \_ renderTarget**](d3dusage.md)oder **D3DUSAGE \_ Dynamic**.</span><span class="sxs-lookup"><span data-stu-id="53b88-126">0, [**D3DUSAGE\_RENDERTARGET**](d3dusage.md), or **D3DUSAGE\_DYNAMIC**.</span></span> <span data-ttu-id="53b88-127">Wenn dieses Flag auf **D3DUSAGE \_ renderTarget** festgelegt wird, wird angegeben, dass die Oberfläche als Renderziel verwendet werden soll, indem die [**SetRenderTarget**](/windows/desktop/api) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="53b88-127">Setting this flag to **D3DUSAGE\_RENDERTARGET** indicates that the surface is to be used as a render target by calling the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="53b88-128">Wenn entweder **D3DUSAGE \_ renderTarget** oder **D3DUSAGE \_ Dynamic** angegeben ist, muss die Anwendung überprüfen, ob das Gerät diesen Vorgang durch Aufrufen von [**CheckDeviceFormat**](/windows/desktop/api)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="53b88-128">If either **D3DUSAGE\_RENDERTARGET** or **D3DUSAGE\_DYNAMIC** is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/desktop/api).</span></span> <span data-ttu-id="53b88-129">Weitere Informationen zur Verwendung dynamischer Texturen finden Sie unter [Verwenden dynamischer Texturen](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="53b88-129">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="53b88-130">*Format* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53b88-130">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53b88-131">Typ: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="53b88-131">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="53b88-132">Member des [D3DFORMAT](d3dformat.md) -Enumerationstyps, der das angeforderte Pixel Format für die Textur beschreibt.</span><span class="sxs-lookup"><span data-stu-id="53b88-132">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the texture.</span></span> <span data-ttu-id="53b88-133">Die zurückgegebene Textur kann ein anderes Format aufweisen als das angegebene Format, wenn das Gerät das angeforderte Format nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="53b88-133">The returned texture may be of a different format from that specified, if the device does not support the requested format.</span></span> <span data-ttu-id="53b88-134">Anwendungen sollten das Format der zurückgegebenen Textur überprüfen, um festzustellen, ob es mit dem angeforderten Format übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="53b88-134">Applications should check the format of the returned texture to see if it matches the format requested.</span></span>

</dd> <dt>

<span data-ttu-id="53b88-135">*Pool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53b88-135">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53b88-136">Typ: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="53b88-136">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="53b88-137">Member des [**D3DPOOL**](./d3dpool.md) -Enumerationstyps, der die Speicher Klasse beschreibt, in der die Textur platziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="53b88-137">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="53b88-138">*pptexture* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="53b88-138">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53b88-139">Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="53b88-139">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="53b88-140">Adresse eines Zeigers auf eine [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Schnittstelle, die das erstellte Textur Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="53b88-140">Address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53b88-141">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="53b88-141">Return value</span></span>

<span data-ttu-id="53b88-142">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="53b88-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="53b88-143">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="53b88-143">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="53b88-144">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcallable, D3DERR \_ NotAvailable, D3DERR \_ oudefvideomemory, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="53b88-144">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="53b88-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="53b88-145">Remarks</span></span>

<span data-ttu-id="53b88-146">Intern verwendet D3DXCreateTexture [**D3DXCheckTextureRequirements**](d3dxchecktexturerequirements.md) , um die aufrufenden Parameter anzupassen.</span><span class="sxs-lookup"><span data-stu-id="53b88-146">Internally, D3DXCreateTexture uses [**D3DXCheckTextureRequirements**](d3dxchecktexturerequirements.md) to adjust the calling parameters.</span></span> <span data-ttu-id="53b88-147">Daher sind Aufrufe von D3DXCreateTexture oft erfolgreich, wenn Aufrufe von " [**kreatetexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) " fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="53b88-147">Therefore, calls to D3DXCreateTexture will often succeed where calls to [**CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) would fail.</span></span>

<span data-ttu-id="53b88-148">Wenn sowohl Height als auch Width auf [D3DX \_ default](other-d3dx-constants.md)festgelegt ist, wird für beide Parameter der Wert 256 verwendet.</span><span class="sxs-lookup"><span data-stu-id="53b88-148">If both Height and Width are set to [D3DX\_DEFAULT](other-d3dx-constants.md), a value of 256 is used for both parameters.</span></span> <span data-ttu-id="53b88-149">Wenn entweder Height oder Width auf D3DX Default festgelegt ist \_ und der andere Parameter auf einen numerischen Wert festgelegt ist, ist die Textur quadratisch, wobei die Höhe und die Breite dem numerischen Wert entspricht.</span><span class="sxs-lookup"><span data-stu-id="53b88-149">If either Height or Width is set to D3DX\_DEFAULT And the other parameter is set to a numeric value, the texture will be square with both the height and width equal to the numeric value.</span></span>

## <a name="requirements"></a><span data-ttu-id="53b88-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53b88-150">Requirements</span></span>



| <span data-ttu-id="53b88-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="53b88-151">Requirement</span></span> | <span data-ttu-id="53b88-152">Wert</span><span class="sxs-lookup"><span data-stu-id="53b88-152">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="53b88-153">Header</span><span class="sxs-lookup"><span data-stu-id="53b88-153">Header</span></span><br/>  | <dl> <span data-ttu-id="53b88-154"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="53b88-154"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="53b88-155">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="53b88-155">Library</span></span><br/> | <dl> <span data-ttu-id="53b88-156"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53b88-156"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="53b88-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53b88-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53b88-158">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="53b88-158">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
