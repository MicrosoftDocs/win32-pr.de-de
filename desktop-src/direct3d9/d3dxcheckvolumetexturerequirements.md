---
description: Überprüft Parameter zur volumetextur Erstellung.
ms.assetid: 1a02cb99-2582-4d8f-aacf-67ed75f6deb8
title: D3DXCheckVolumeTextureRequirements-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckVolumeTextureRequirements
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4940cab936ed14c847e7224c9f619244c6e422a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394153"
---
# <a name="d3dxcheckvolumetexturerequirements-function"></a><span data-ttu-id="e746b-103">D3DXCheckVolumeTextureRequirements-Funktion</span><span class="sxs-lookup"><span data-stu-id="e746b-103">D3DXCheckVolumeTextureRequirements function</span></span>

<span data-ttu-id="e746b-104">Überprüft Parameter zur volumetextur Erstellung.</span><span class="sxs-lookup"><span data-stu-id="e746b-104">Checks volume-texture-creation parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="e746b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e746b-105">Syntax</span></span>


```C++
HRESULT D3DXCheckVolumeTextureRequirements(
  _In_    LPDIRECT3DDEVICE9 pDevice,
  _Inout_ UINT              *pWidth,
  _Inout_ UINT              *pHeight,
  _Inout_ UINT              *pDepth,
  _Inout_ UINT              *pNumMipLevels,
  _In_    DWORD             Usage,
  _Inout_ D3DFORMAT         *pFormat,
  _In_    D3DPOOL           Pool
);
```



## <a name="parameters"></a><span data-ttu-id="e746b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e746b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e746b-107">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e746b-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e746b-108">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="e746b-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="e746b-109">Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, die das Gerät darstellt, das der volumetextur zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e746b-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device to be associated with the volume texture.</span></span>

</dd> <dt>

<span data-ttu-id="e746b-110">*pWidth* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e746b-110">*pWidth* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e746b-111">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e746b-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e746b-112">Ein Zeiger auf die angeforderte Breite in Pixel oder **null**.</span><span class="sxs-lookup"><span data-stu-id="e746b-112">Pointer to the requested width in pixels, or **NULL**.</span></span> <span data-ttu-id="e746b-113">Gibt die korrigierte Größe zurück.</span><span class="sxs-lookup"><span data-stu-id="e746b-113">Returns the corrected size.</span></span>

</dd> <dt>

<span data-ttu-id="e746b-114">*pHeight* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e746b-114">*pHeight* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e746b-115">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e746b-115">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e746b-116">Ein Zeiger auf die angeforderte Höhe in Pixel oder **null**.</span><span class="sxs-lookup"><span data-stu-id="e746b-116">Pointer to the requested height in pixels, or **NULL**.</span></span> <span data-ttu-id="e746b-117">Gibt die korrigierte Größe zurück.</span><span class="sxs-lookup"><span data-stu-id="e746b-117">Returns the corrected size.</span></span>

</dd> <dt>

<span data-ttu-id="e746b-118">*ptiefe* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e746b-118">*pDepth* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e746b-119">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e746b-119">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e746b-120">Ein Zeiger auf die angeforderte Tiefe in Pixel oder **null**.</span><span class="sxs-lookup"><span data-stu-id="e746b-120">Pointer to the requested depth in pixels, or **NULL**.</span></span> <span data-ttu-id="e746b-121">Gibt die korrigierte Größe zurück.</span><span class="sxs-lookup"><span data-stu-id="e746b-121">Returns the corrected size.</span></span>

</dd> <dt>

<span data-ttu-id="e746b-122">*pnummiplevels* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e746b-122">*pNumMipLevels* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e746b-123">Typ: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e746b-123">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e746b-124">Ein Zeiger auf die Anzahl der angeforderten MipMap-Ebenen oder **null**.</span><span class="sxs-lookup"><span data-stu-id="e746b-124">Pointer to the number of requested mipmap levels, or **NULL**.</span></span> <span data-ttu-id="e746b-125">Gibt die korrigierte Anzahl von MipMap-Ebenen zurück.</span><span class="sxs-lookup"><span data-stu-id="e746b-125">Returns the corrected number of mipmap levels.</span></span>

</dd> <dt>

<span data-ttu-id="e746b-126">*Verwendung* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e746b-126">*Usage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e746b-127">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e746b-127">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e746b-128">Wird derzeit nicht verwendet, auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e746b-128">Currently not used, set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="e746b-129">*pformat* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e746b-129">*pFormat* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e746b-130">Typ: **[D3DFORMAT](d3dformat.md)\***</span><span class="sxs-lookup"><span data-stu-id="e746b-130">Type: **[D3DFORMAT](d3dformat.md)\***</span></span>

<span data-ttu-id="e746b-131">Zeiger auf einen Member des [D3DFORMAT](d3dformat.md) -enumerierten Typs.</span><span class="sxs-lookup"><span data-stu-id="e746b-131">Pointer to a member of the [D3DFORMAT](d3dformat.md) enumerated type.</span></span> <span data-ttu-id="e746b-132">Gibt das gewünschte Pixel Format oder **null** an.</span><span class="sxs-lookup"><span data-stu-id="e746b-132">Specifies the desired pixel format, or **NULL**.</span></span> <span data-ttu-id="e746b-133">Gibt das korrigierte Format zurück.</span><span class="sxs-lookup"><span data-stu-id="e746b-133">Returns the corrected format.</span></span>

</dd> <dt>

<span data-ttu-id="e746b-134">*Pool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e746b-134">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e746b-135">Typ: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="e746b-135">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

<span data-ttu-id="e746b-136">Member des [**D3DPOOL**](./d3dpool.md) -Enumerationstyps, der die Speicher Klasse beschreibt, in die die volumetextur eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e746b-136">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, describing the memory class into which the volume texture should be placed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e746b-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e746b-137">Return value</span></span>

<span data-ttu-id="e746b-138">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e746b-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e746b-139">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e746b-139">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e746b-140">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ NotAvailable, D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="e746b-140">If the function fails, the return value can be one of the following: D3DERR\_NOTAVAILABLE, D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="e746b-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e746b-141">Remarks</span></span>

<span data-ttu-id="e746b-142">Wenn die Parameter dieser Funktion ungültig sind, gibt diese Funktion korrigierte Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="e746b-142">If parameters to this function are invalid, this function returns corrected parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="e746b-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e746b-143">Requirements</span></span>



| <span data-ttu-id="e746b-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e746b-144">Requirement</span></span> | <span data-ttu-id="e746b-145">Wert</span><span class="sxs-lookup"><span data-stu-id="e746b-145">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e746b-146">Header</span><span class="sxs-lookup"><span data-stu-id="e746b-146">Header</span></span><br/>  | <dl> <span data-ttu-id="e746b-147"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="e746b-147"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="e746b-148">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e746b-148">Library</span></span><br/> | <dl> <span data-ttu-id="e746b-149"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e746b-149"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e746b-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e746b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e746b-151">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="e746b-151">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
