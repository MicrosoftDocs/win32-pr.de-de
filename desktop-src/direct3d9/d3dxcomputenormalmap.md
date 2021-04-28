---
description: 'D3DXComputeNormalMap-Funktion: Konvertiert eine Höhenkarte in eine normale Karte. Die (x,y,z)-Komponenten jedes Normals werden den (r,g,b)-Kanälen der Ausgabetextur zugeordnet.'
ms.assetid: ed9053c0-b1df-4f74-bdee-627c0f60d942
title: D3DXComputeNormalMap-Funktion (D3dx9tex.h)
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
ms.openlocfilehash: 920ad763f478a2e6bcb9fbe98cc7e2a677ebe783
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105228"
---
# <a name="d3dxcomputenormalmap-function"></a><span data-ttu-id="8fcf9-104">D3DXComputeNormalMap-Funktion</span><span class="sxs-lookup"><span data-stu-id="8fcf9-104">D3DXComputeNormalMap function</span></span>

<span data-ttu-id="8fcf9-105">Konvertiert eine Höhenkarte in eine normale Karte.</span><span class="sxs-lookup"><span data-stu-id="8fcf9-105">Converts a height map into a normal map.</span></span> <span data-ttu-id="8fcf9-106">Die (x,y,z)-Komponenten jedes Normals werden den (r,g,b)-Kanälen der Ausgabetextur zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="8fcf9-106">The (x,y,z) components of each normal are mapped to the (r,g,b) channels of the output texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fcf9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8fcf9-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="8fcf9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8fcf9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fcf9-109">*pTexture* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8fcf9-109">*pTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8fcf9-110">Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="8fcf9-110">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="8fcf9-111">Zeiger auf eine [**IDirect3DTexture9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) die die Zieltextur darstellt.</span><span class="sxs-lookup"><span data-stu-id="8fcf9-111">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the destination texture.</span></span>

</dd> <dt>

<span data-ttu-id="8fcf9-112">*pSrcTexture* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="8fcf9-112">*pSrcTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fcf9-113">Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="8fcf9-113">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="8fcf9-114">Zeiger auf eine [**IDirect3DTexture9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) die die Textur der Quellhöhenzuordnung darstellt.</span><span class="sxs-lookup"><span data-stu-id="8fcf9-114">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the source height-map texture.</span></span>

</dd> <dt>

<span data-ttu-id="8fcf9-115">*pSrcPalette* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="8fcf9-115">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fcf9-116">Typ: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="8fcf9-116">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="8fcf9-117">Zeiger auf einen [**PALETTEENTRY-Typ,**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) der die Quellpalette mit 256 Farben oder **NULL enthält.**</span><span class="sxs-lookup"><span data-stu-id="8fcf9-117">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) type that contains the source palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8fcf9-118">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="8fcf9-118">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fcf9-119">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8fcf9-119">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8fcf9-120">Mindestens ein [D3DX \_ NORMALMAP-Flag,](d3dx-normalmap.md) das die Generierung normaler Karten kontrolliert.</span><span class="sxs-lookup"><span data-stu-id="8fcf9-120">One or more [D3DX\_NORMALMAP](d3dx-normalmap.md) flags that control generation of normal maps.</span></span>

</dd> <dt>

<span data-ttu-id="8fcf9-121">*Kanal* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="8fcf9-121">*Channel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fcf9-122">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8fcf9-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8fcf9-123">Ein [D3DX \_ CHANNEL-Flag,](d3dx-channel.md) das die Quelle der Höheninformationen an gibt.</span><span class="sxs-lookup"><span data-stu-id="8fcf9-123">One [D3DX\_CHANNEL](d3dx-channel.md) flag specifying the source of height information.</span></span>

</dd> <dt>

<span data-ttu-id="8fcf9-124">*Amplitude* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="8fcf9-124">*Amplitude* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fcf9-125">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8fcf9-125">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8fcf9-126">Konstanter Wertmultiplikator, der die Werte in der normalen Zuordnung erhöht (oder verringert).</span><span class="sxs-lookup"><span data-stu-id="8fcf9-126">Constant value multiplier that increases (or decreases) the values in the normal map.</span></span> <span data-ttu-id="8fcf9-127">Höhere Werte machen Bumps in der Regel sichtbarer, niedrigere Werte machen Bumps in der Regel weniger sichtbar.</span><span class="sxs-lookup"><span data-stu-id="8fcf9-127">Higher values usually make bumps more visible, lower values usually make bumps less visible.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fcf9-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8fcf9-128">Return value</span></span>

<span data-ttu-id="8fcf9-129">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8fcf9-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8fcf9-130">Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8fcf9-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8fcf9-131">Wenn die Funktion fehlschlägt, kann der Rückgabewert der folgende Wert sein: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="8fcf9-131">If the function fails, the return value can be the following value: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fcf9-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8fcf9-132">Remarks</span></span>

<span data-ttu-id="8fcf9-133">Diese Methode berechnet die Normalität mithilfe des zentralen Unterschieds mit einer Kernelgröße von 3x3.</span><span class="sxs-lookup"><span data-stu-id="8fcf9-133">This method computes the normal by using the central difference with a kernel size of 3x3.</span></span> <span data-ttu-id="8fcf9-134">Der zentrale differenzierende Nenner ist 2.0.</span><span class="sxs-lookup"><span data-stu-id="8fcf9-134">The central differencing denominator used is 2.0.</span></span> <span data-ttu-id="8fcf9-135">RGB-Kanäle im Ziel enthalten voreingenommene (x,y,z)-Komponenten der Normalen.</span><span class="sxs-lookup"><span data-stu-id="8fcf9-135">RGB channels in the destination contain biased (x,y,z) components of the normal.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fcf9-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8fcf9-136">Requirements</span></span>



| <span data-ttu-id="8fcf9-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8fcf9-137">Requirement</span></span> | <span data-ttu-id="8fcf9-138">Wert</span><span class="sxs-lookup"><span data-stu-id="8fcf9-138">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8fcf9-139">Header</span><span class="sxs-lookup"><span data-stu-id="8fcf9-139">Header</span></span><br/>  | <dl> <span data-ttu-id="8fcf9-140"><dt>D3dx9tex.h</dt></span><span class="sxs-lookup"><span data-stu-id="8fcf9-140"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="8fcf9-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8fcf9-141">Library</span></span><br/> | <dl> <span data-ttu-id="8fcf9-142"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="8fcf9-142"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="8fcf9-143">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8fcf9-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fcf9-144">Texturfunktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="8fcf9-144">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
