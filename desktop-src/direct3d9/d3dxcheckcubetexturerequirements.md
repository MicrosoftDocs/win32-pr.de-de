---
description: Überprüft Parameter für die cubetextur-Erstellung.
ms.assetid: 56ced947-1142-4d05-95e3-ca6a26b147d4
title: D3DXCheckCubeTextureRequirements-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckCubeTextureRequirements
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9f800617920c5d79361b5e6da291fd88b5b963b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762351"
---
# <a name="d3dxcheckcubetexturerequirements-function"></a><span data-ttu-id="8ee17-103">D3DXCheckCubeTextureRequirements-Funktion</span><span class="sxs-lookup"><span data-stu-id="8ee17-103">D3DXCheckCubeTextureRequirements function</span></span>

<span data-ttu-id="8ee17-104">Überprüft Parameter für die cubetextur-Erstellung.</span><span class="sxs-lookup"><span data-stu-id="8ee17-104">Checks cube-texture-creation parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ee17-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ee17-105">Syntax</span></span>


```C++
HRESULT D3DXCheckCubeTextureRequirements(
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Inout_ UINT              *pSize,
  _Inout_ UINT              *pNumMipLevels,
  _In_    DWORD             Usage,
  _Inout_ D3DFORMAT         *pFormat,
  _In_    D3DPOOL           Pool
);
```



## <a name="parameters"></a><span data-ttu-id="8ee17-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ee17-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ee17-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ee17-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ee17-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="8ee17-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="8ee17-109">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das der cubetextur zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8ee17-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the cube texture.</span></span>

</dd> <dt>

<span data-ttu-id="8ee17-110">*Psize* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8ee17-110">*pSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ee17-111">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8ee17-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8ee17-112">Zeiger auf die angeforderte Breite und Höhe in Pixel oder **null**.</span><span class="sxs-lookup"><span data-stu-id="8ee17-112">Pointer to the requested width and height in pixels, or **NULL**.</span></span> <span data-ttu-id="8ee17-113">Gibt die korrigierte Größe zurück.</span><span class="sxs-lookup"><span data-stu-id="8ee17-113">Returns the corrected size.</span></span>

</dd> <dt>

<span data-ttu-id="8ee17-114">*pnummiplevels* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8ee17-114">*pNumMipLevels* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ee17-115">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8ee17-115">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8ee17-116">Ein Zeiger auf die Anzahl der angeforderten MipMap-Ebenen oder **null**.</span><span class="sxs-lookup"><span data-stu-id="8ee17-116">Pointer to the number of requested mipmap levels, or **NULL**.</span></span> <span data-ttu-id="8ee17-117">Gibt die korrigierte Anzahl von MipMap-Ebenen zurück.</span><span class="sxs-lookup"><span data-stu-id="8ee17-117">Returns the corrected number of mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="8ee17-118">*Verwendung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ee17-118">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ee17-119">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ee17-119">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8ee17-120">0 oder D3DUSAGE \_ renderTarget.</span><span class="sxs-lookup"><span data-stu-id="8ee17-120">0 or D3DUSAGE\_RENDERTARGET.</span></span> <span data-ttu-id="8ee17-121">Wenn dieses Flag auf D3DUSAGE \_ renderTarget festgelegt wird, wird angegeben, dass die Oberfläche als Renderziel verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8ee17-121">Setting this flag to D3DUSAGE\_RENDERTARGET indicates that the surface is to be used as a render target.</span></span> <span data-ttu-id="8ee17-122">Die Ressource kann dann an den pnewrendertarget-Parameter der Methode "Setup [**target**](/windows/desktop/api) " übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="8ee17-122">The resource can then be passed to the pNewRenderTarget parameter of the [**SetRenderTarget**](/windows/desktop/api) method.</span></span> <span data-ttu-id="8ee17-123">Wenn D3DUSAGE \_ renderTarget angegeben ist, muss die Anwendung überprüfen, ob das Gerät diesen Vorgang durch Aufrufen von [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8ee17-123">If D3DUSAGE\_RENDERTARGET is specified, the application should check that the device supports this operation by calling [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).</span></span>

</dd> <dt>

<span data-ttu-id="8ee17-124">*pformat* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8ee17-124">*pFormat* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ee17-125">Typ: **[D3DFORMAT](d3dformat.md)\***</span><span class="sxs-lookup"><span data-stu-id="8ee17-125">Type: **[D3DFORMAT](d3dformat.md)\***</span></span>

<span data-ttu-id="8ee17-126">Zeiger auf einen Member des [D3DFORMAT](d3dformat.md) -enumerierten Typs.</span><span class="sxs-lookup"><span data-stu-id="8ee17-126">Pointer to a member of the [D3DFORMAT](d3dformat.md) enumerated type.</span></span> <span data-ttu-id="8ee17-127">Gibt das gewünschte Pixel Format oder **null** an.</span><span class="sxs-lookup"><span data-stu-id="8ee17-127">Specifies the desired pixel format, or **NULL**.</span></span> <span data-ttu-id="8ee17-128">Gibt das korrigierte Format zurück.</span><span class="sxs-lookup"><span data-stu-id="8ee17-128">Returns the corrected format.</span></span>

</dd> <dt>

<span data-ttu-id="8ee17-129">*Pool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ee17-129">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ee17-130">Typ: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="8ee17-130">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="8ee17-131">Member des [**D3DPOOL**](./d3dpool.md) -Enumerationstyps, der die Speicher Klasse beschreibt, in der die Textur platziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8ee17-131">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the texture should be placed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ee17-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8ee17-132">Return value</span></span>

<span data-ttu-id="8ee17-133">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8ee17-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8ee17-134">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8ee17-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8ee17-135">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ NotAvailable, D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="8ee17-135">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ee17-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8ee17-136">Remarks</span></span>

<span data-ttu-id="8ee17-137">Wenn die Parameter dieser Funktion ungültig sind, gibt diese Funktion korrigierte Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="8ee17-137">If parameters to this function are invalid, this function returns corrected parameters.</span></span>

<span data-ttu-id="8ee17-138">Cube-Texturen unterscheiden sich von anderen Oberflächen darin, dass es sich um Auflistungen von</span><span class="sxs-lookup"><span data-stu-id="8ee17-138">Cube textures differ from other surfaces in that they are collections of surfaces.</span></span> <span data-ttu-id="8ee17-139">Um "\*" mit einer cubetextur aufzurufen, müssen Sie ein einzelnes Gesicht [**mithilfe von "**](/windows/desktop/api) [**getcubemapsurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) " auswählen und die resultierende Oberfläche an " **strendertarget**" übergeben.</span><span class="sxs-lookup"><span data-stu-id="8ee17-139">To call [**SetRenderTarget**](/windows/desktop/api) with a cube texture, you must select an individual face using [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) and pass the resulting surface to **SetRenderTarget**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ee17-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8ee17-140">Requirements</span></span>



| <span data-ttu-id="8ee17-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8ee17-141">Requirement</span></span> | <span data-ttu-id="8ee17-142">Wert</span><span class="sxs-lookup"><span data-stu-id="8ee17-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8ee17-143">Header</span><span class="sxs-lookup"><span data-stu-id="8ee17-143">Header</span></span><br/>  | <dl> <span data-ttu-id="8ee17-144"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ee17-144"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="8ee17-145">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8ee17-145">Library</span></span><br/> | <dl> <span data-ttu-id="8ee17-146"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ee17-146"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="8ee17-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ee17-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ee17-148">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="8ee17-148">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
