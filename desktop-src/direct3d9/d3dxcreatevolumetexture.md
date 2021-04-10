---
description: Erstellt eine leere volumetextur und passt die aufrufenden Parameter nach Bedarf an.
ms.assetid: 8fc515cd-2fb3-40c7-8192-a41d93ac1e99
title: D3DXCreateVolumeTexture-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 50baf125d2e5375bddb63a41a0d10ae063a57b78
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961607"
---
# <a name="d3dxcreatevolumetexture-function"></a><span data-ttu-id="d5b74-103">D3DXCreateVolumeTexture-Funktion</span><span class="sxs-lookup"><span data-stu-id="d5b74-103">D3DXCreateVolumeTexture function</span></span>

<span data-ttu-id="d5b74-104">Erstellt eine leere volumetextur und passt die aufrufenden Parameter nach Bedarf an.</span><span class="sxs-lookup"><span data-stu-id="d5b74-104">Creates an empty volume texture, adjusting the calling parameters as needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5b74-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5b74-105">Syntax</span></span>


```C++
HRESULT D3DXCreateVolumeTexture(
  _In_  LPDIRECT3DDEVICE9        pDevice,
  _In_  UINT                     Width,
  _In_  UINT                     Height,
  _In_  UINT                     Depth,
  _In_  UINT                     MipLevels,
  _In_  DWORD                    Usage,
  _In_  D3DFORMAT                Format,
  _In_  D3DPOOL                  Pool,
  _Out_ LPDIRECT3DVOLUMETEXTURE9 *ppVolumeTexture
);
```



## <a name="parameters"></a><span data-ttu-id="d5b74-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5b74-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5b74-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5b74-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5b74-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="d5b74-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="d5b74-109">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das der volumetextur zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d5b74-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="d5b74-110">*Breite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5b74-110">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5b74-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d5b74-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d5b74-112">Breite in Pixel.</span><span class="sxs-lookup"><span data-stu-id="d5b74-112">Width in pixels.</span></span> <span data-ttu-id="d5b74-113">Dieser Wert darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="d5b74-113">This value must be nonzero.</span></span> <span data-ttu-id="d5b74-114">Die maximale Dimension, die ein Treiber unterstützt (für Breite, Höhe und Tiefe), ist in maxvolumeblock in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)zu finden.</span><span class="sxs-lookup"><span data-stu-id="d5b74-114">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="d5b74-115">*Höhe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5b74-115">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5b74-116">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d5b74-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d5b74-117">Höhe in Pixel.</span><span class="sxs-lookup"><span data-stu-id="d5b74-117">Height in pixels.</span></span> <span data-ttu-id="d5b74-118">Dieser Wert darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="d5b74-118">This value must be nonzero.</span></span> <span data-ttu-id="d5b74-119">Die maximale Dimension, die ein Treiber unterstützt (für Breite, Höhe und Tiefe), ist in maxvolumeblock in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)zu finden.</span><span class="sxs-lookup"><span data-stu-id="d5b74-119">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="d5b74-120">*Tiefe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5b74-120">*Depth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5b74-121">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d5b74-121">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d5b74-122">Tiefe in Pixel.</span><span class="sxs-lookup"><span data-stu-id="d5b74-122">Depth in pixels.</span></span> <span data-ttu-id="d5b74-123">Dieser Wert darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="d5b74-123">This value must be nonzero.</span></span> <span data-ttu-id="d5b74-124">Die maximale Dimension, die ein Treiber unterstützt (für Breite, Höhe und Tiefe), ist in maxvolumeblock in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)zu finden.</span><span class="sxs-lookup"><span data-stu-id="d5b74-124">The maximum dimension that a driver supports (for width, height, and depth) can be found in MaxVolumeExtent in [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="d5b74-125">*Miplevels* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5b74-125">*MipLevels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5b74-126">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d5b74-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d5b74-127">Anzahl der angeforderten Mip-Ebenen.</span><span class="sxs-lookup"><span data-stu-id="d5b74-127">Number of mip levels requested.</span></span> <span data-ttu-id="d5b74-128">Wenn dieser Wert 0 (null) oder D3DX \_ Default ist, wird eine komplette MipMap-Kette erstellt.</span><span class="sxs-lookup"><span data-stu-id="d5b74-128">If this value is zero or D3DX\_DEFAULT, a complete mipmap chain is created.</span></span>

</dd> <dt>

<span data-ttu-id="d5b74-129">*Verwendung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5b74-129">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5b74-130">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d5b74-130">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d5b74-131">0 oder D3DUSAGE \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="d5b74-131">0 or D3DUSAGE\_DYNAMIC.</span></span> <span data-ttu-id="d5b74-132">Weitere Informationen zur Verwendung dynamischer Texturen finden Sie unter [Verwenden dynamischer Texturen](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="d5b74-132">For more information about using dynamic textures, see [Using Dynamic Textures](performance-optimizations.md).</span></span>

</dd> <dt>

<span data-ttu-id="d5b74-133">*Format* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5b74-133">*Format* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5b74-134">Typ: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="d5b74-134">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="d5b74-135">Member des [D3DFORMAT](d3dformat.md) -Enumerationstyps, der das angeforderte Pixel Format für die volumetextur beschreibt.</span><span class="sxs-lookup"><span data-stu-id="d5b74-135">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the requested pixel format for the volume texture.</span></span> <span data-ttu-id="d5b74-136">Die zurückgegebene volumetextur kann ein anderes Format aufweisen als das, das durch das Format angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d5b74-136">The returned volume texture might have a different format from that specified by Format.</span></span> <span data-ttu-id="d5b74-137">Anwendungen sollten das Format der zurückgegebenen volumetextur überprüfen.</span><span class="sxs-lookup"><span data-stu-id="d5b74-137">Applications should check the format of the returned volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="d5b74-138">*Pool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5b74-138">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5b74-139">Typ: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="d5b74-139">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="d5b74-140">Member des [**D3DPOOL**](./d3dpool.md) -Enumerationstyps, der die Speicher Klasse beschreibt, in die die volumetextur eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d5b74-140">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the volume texture should be placed.</span></span>

</dd> <dt>

<span data-ttu-id="d5b74-141">*ppvolumetexture* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d5b74-141">*ppVolumeTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5b74-142">Typ: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span><span class="sxs-lookup"><span data-stu-id="d5b74-142">Type: **[**LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***</span></span>

<span data-ttu-id="d5b74-143">Adresse eines Zeigers auf eine [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) -Schnittstelle, die das erstellte volumetextur-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="d5b74-143">Address of a pointer to an [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) interface, representing the created volume texture object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5b74-144">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d5b74-144">Return value</span></span>

<span data-ttu-id="d5b74-145">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d5b74-145">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d5b74-146">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d5b74-146">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d5b74-147">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ NotAvailable, D3DERR \_ ouesfvideomemory, D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="d5b74-147">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_OUTOFVIDEOMEMORY, D3DERR\_INVALIDCALL, E\_OUTOFMEMORY .</span></span>

## <a name="remarks"></a><span data-ttu-id="d5b74-148">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d5b74-148">Remarks</span></span>

<span data-ttu-id="d5b74-149">Intern verwendet D3DXCreateVolumeTexture [**D3DXCheckVolumeTextureRequirements**](d3dxcheckvolumetexturerequirements.md) , um die aufrufenden Parameter anzupassen.</span><span class="sxs-lookup"><span data-stu-id="d5b74-149">Internally, D3DXCreateVolumeTexture uses [**D3DXCheckVolumeTextureRequirements**](d3dxcheckvolumetexturerequirements.md) to adjust the calling parameters.</span></span> <span data-ttu-id="d5b74-150">Daher sind Aufrufe von D3DXCreateVolumeTexture oft erfolgreich, wenn Aufrufe von " [**kreatevolumetexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture) " fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="d5b74-150">Therefore, calls to D3DXCreateVolumeTexture will often succeed where calls to [**CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture) would fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5b74-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d5b74-151">Requirements</span></span>



| <span data-ttu-id="d5b74-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d5b74-152">Requirement</span></span> | <span data-ttu-id="d5b74-153">Wert</span><span class="sxs-lookup"><span data-stu-id="d5b74-153">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d5b74-154">Header</span><span class="sxs-lookup"><span data-stu-id="d5b74-154">Header</span></span><br/>  | <dl> <span data-ttu-id="d5b74-155"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5b74-155"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="d5b74-156">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d5b74-156">Library</span></span><br/> | <dl> <span data-ttu-id="d5b74-157"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5b74-157"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="d5b74-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d5b74-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5b74-159">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="d5b74-159">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
