---
description: Konvertiert eine Höhen Zuordnung in eine normale Karte. Die Komponenten (x, y, z) der einzelnen normalen werden den Kanälen (r, g, b) der Ausgabe Textur zugeordnet.
ms.assetid: ed9053c0-b1df-4f74-bdee-627c0f60d942
title: D3DXComputeNormalMap-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeNormalMap
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6e22418f5a023dbe70fee8ea0fba8a449abbcc8d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350714"
---
# <a name="d3dxcomputenormalmap-function"></a><span data-ttu-id="c25ef-104">D3DXComputeNormalMap-Funktion</span><span class="sxs-lookup"><span data-stu-id="c25ef-104">D3DXComputeNormalMap function</span></span>

<span data-ttu-id="c25ef-105">Konvertiert eine Höhen Zuordnung in eine normale Karte.</span><span class="sxs-lookup"><span data-stu-id="c25ef-105">Converts a height map into a normal map.</span></span> <span data-ttu-id="c25ef-106">Die Komponenten (x, y, z) der einzelnen normalen werden den Kanälen (r, g, b) der Ausgabe Textur zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c25ef-106">The (x,y,z) components of each normal are mapped to the (r,g,b) channels of the output texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="c25ef-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c25ef-107">Syntax</span></span>


```C++
HRESULT D3DXComputeNormalMap(
  _Out_       LPDIRECT3DTEXTURE9 pTexture,
  _In_        LPDIRECT3DTEXTURE9 pSrcTexture,
  _In_  const PALETTEENTRY       *pSrcPalette,
  _In_        DWORD              Flags,
  _In_        DWORD              Channel,
  _In_        FLOAT              Amplitude
);
```



## <a name="parameters"></a><span data-ttu-id="c25ef-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c25ef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c25ef-109">*ptexture* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c25ef-109">*pTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c25ef-110">Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="c25ef-110">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="c25ef-111">Zeiger auf eine [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Schnittstelle, die die Ziel Textur darstellt.</span><span class="sxs-lookup"><span data-stu-id="c25ef-111">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the destination texture.</span></span>

</dd> <dt>

<span data-ttu-id="c25ef-112">*psrctexture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c25ef-112">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c25ef-113">Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="c25ef-113">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="c25ef-114">Ein Zeiger auf eine [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Schnittstelle, die die Textur der Quell Höhe darstellt.</span><span class="sxs-lookup"><span data-stu-id="c25ef-114">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the source height-map texture.</span></span>

</dd> <dt>

<span data-ttu-id="c25ef-115">*psrcpalette* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c25ef-115">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c25ef-116">Typ: **Konstanten [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="c25ef-116">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="c25ef-117">Zeiger auf einen [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) -Typ, der die Quell Palette von 256 Farben oder **null** enthält.</span><span class="sxs-lookup"><span data-stu-id="c25ef-117">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) type that contains the source palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c25ef-118">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="c25ef-118">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c25ef-119">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c25ef-119">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c25ef-120">Ein oder mehrere [D3DX \_ normalmap](d3dx-normalmap.md) -Flags, die die Generierung normaler Karten steuern.</span><span class="sxs-lookup"><span data-stu-id="c25ef-120">One or more [D3DX\_NORMALMAP](d3dx-normalmap.md) flags that control generation of normal maps.</span></span>

</dd> <dt>

<span data-ttu-id="c25ef-121">*Channel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c25ef-121">*Channel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c25ef-122">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c25ef-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c25ef-123">Ein [D3DX- \_ kanalflag](d3dx-channel.md) , das die Quelle der Höheninformationen angibt.</span><span class="sxs-lookup"><span data-stu-id="c25ef-123">One [D3DX\_CHANNEL](d3dx-channel.md) flag specifying the source of height information.</span></span>

</dd> <dt>

<span data-ttu-id="c25ef-124">*Amplitude* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c25ef-124">*Amplitude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c25ef-125">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c25ef-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c25ef-126">Konstanter Wert Multiplikator, der die Werte in der normalen Zuordnung vergrößert (oder verringert).</span><span class="sxs-lookup"><span data-stu-id="c25ef-126">Constant value multiplier that increases (or decreases) the values in the normal map.</span></span> <span data-ttu-id="c25ef-127">Höhere Werte machen in der Regel zu Leistungseinbußen, niedrigere Werte werden in der Regel weniger sichtbar.</span><span class="sxs-lookup"><span data-stu-id="c25ef-127">Higher values usually make bumps more visible, lower values usually make bumps less visible.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c25ef-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c25ef-128">Return value</span></span>

<span data-ttu-id="c25ef-129">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c25ef-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c25ef-130">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c25ef-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c25ef-131">Wenn die Funktion fehlschlägt, kann der Rückgabewert der folgende Wert sein: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="c25ef-131">If the function fails, the return value can be the following value: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c25ef-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c25ef-132">Remarks</span></span>

<span data-ttu-id="c25ef-133">Diese Methode berechnet die normale, indem der zentrale Unterschied mit einer Kernel Größe von 3X3 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c25ef-133">This method computes the normal by using the central difference with a kernel size of 3x3.</span></span> <span data-ttu-id="c25ef-134">Der zentrale Differenzierungs Nenner, der verwendet wird, ist 2,0.</span><span class="sxs-lookup"><span data-stu-id="c25ef-134">The central differencing denominator used is 2.0.</span></span> <span data-ttu-id="c25ef-135">RGB-Kanäle im Ziel enthalten unausgewogene (x, y, z) Komponenten der normalen.</span><span class="sxs-lookup"><span data-stu-id="c25ef-135">RGB channels in the destination contain biased (x,y,z) components of the normal.</span></span>

## <a name="requirements"></a><span data-ttu-id="c25ef-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c25ef-136">Requirements</span></span>



| <span data-ttu-id="c25ef-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c25ef-137">Requirement</span></span> | <span data-ttu-id="c25ef-138">Wert</span><span class="sxs-lookup"><span data-stu-id="c25ef-138">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c25ef-139">Header</span><span class="sxs-lookup"><span data-stu-id="c25ef-139">Header</span></span><br/>  | <dl> <span data-ttu-id="c25ef-140"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="c25ef-140"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="c25ef-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c25ef-141">Library</span></span><br/> | <dl> <span data-ttu-id="c25ef-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c25ef-142"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="c25ef-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c25ef-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c25ef-144">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="c25ef-144">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
