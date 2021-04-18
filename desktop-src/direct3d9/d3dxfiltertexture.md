---
description: Filtert MipMap-Ebenen einer Textur.
ms.assetid: bfeae9b0-9480-4a26-a225-4a34780546ce
title: D3DXFilterTexture-Funktion (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFilterTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e8a0d1c211b50379451c8b04830e9c97fe988137
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355012"
---
# <a name="d3dxfiltertexture-function"></a><span data-ttu-id="9fb61-103">D3DXFilterTexture-Funktion</span><span class="sxs-lookup"><span data-stu-id="9fb61-103">D3DXFilterTexture function</span></span>

<span data-ttu-id="9fb61-104">Filtert MipMap-Ebenen einer Textur.</span><span class="sxs-lookup"><span data-stu-id="9fb61-104">Filters mipmap levels of a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fb61-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9fb61-105">Syntax</span></span>


```C++
HRESULT D3DXFilterTexture(
  _In_        LPDIRECT3DBASETEXTURE9 pBaseTexture,
  _Out_ const PALETTEENTRY           *pPalette,
  _In_        UINT                   SrcLevel,
  _In_        DWORD                  MipFilter
);
```



## <a name="parameters"></a><span data-ttu-id="9fb61-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9fb61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fb61-107">*pbasetexture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9fb61-107">*pBaseTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fb61-108">Typ: **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span><span class="sxs-lookup"><span data-stu-id="9fb61-108">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span></span>

<span data-ttu-id="9fb61-109">Zeiger auf eine [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) -Schnittstelle, die das zu filternde Textur Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="9fb61-109">Pointer to an [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) interface that represents the texture object to filter.</span></span>

</dd> <dt>

<span data-ttu-id="9fb61-110">*pPalette* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9fb61-110">*pPalette* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9fb61-111">Typ: **Konstanten [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="9fb61-111">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="9fb61-112">Ein Zeiger auf eine [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) -Struktur, die eine zu füllende 256-Farbpalette darstellt, oder **null** für nicht paletformatierte Formate.</span><span class="sxs-lookup"><span data-stu-id="9fb61-112">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure that represents a 256-color palette to fill in, or **NULL** for nonpalettized formats.</span></span> <span data-ttu-id="9fb61-113">Wenn keine Palette angegeben ist, wird die standardmäßige Direct3D-Palette (eine alle nicht transparenten weißen Palette) bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="9fb61-113">If a palette is not specified, the default Direct3D palette (an all opaque white palette) is provided.</span></span> <span data-ttu-id="9fb61-114">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="9fb61-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="9fb61-115">*Srclevel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9fb61-115">*SrcLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fb61-116">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9fb61-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9fb61-117">Ebene, mit deren Bild die nachfolgenden Ebenen generiert werden.</span><span class="sxs-lookup"><span data-stu-id="9fb61-117">Level whose image is used to generate the subsequent levels.</span></span> <span data-ttu-id="9fb61-118">Die Angabe \_ von D3DX default für diesen Parameter entspricht der Angabe von 0.</span><span class="sxs-lookup"><span data-stu-id="9fb61-118">Specifying D3DX\_DEFAULT for this parameter is equivalent to specifying 0.</span></span>

</dd> <dt>

<span data-ttu-id="9fb61-119">*MipFilter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9fb61-119">*MipFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fb61-120">Typ: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9fb61-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9fb61-121">Kombination aus einem oder mehreren [D3DX- \_ Filtern](d3dx-filter.md) , die Steuern, wie die MipMap gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="9fb61-121">Combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the mipmap is filtered.</span></span> <span data-ttu-id="9fb61-122">Das angeben \_ von D3DX default für diesen Parameter entspricht dem Angeben des \_ D3DX \_ -Filter Felds, wenn die Textur Größe eine Potenz von zwei ist, und D3DX \_ Filter \_ Box \| D3DX \_ filtert \_ andernfalls.</span><span class="sxs-lookup"><span data-stu-id="9fb61-122">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_BOX if the texture size is a power of two, and D3DX\_FILTER\_BOX \| D3DX\_FILTER\_DITHER otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fb61-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9fb61-123">Return value</span></span>

<span data-ttu-id="9fb61-124">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9fb61-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9fb61-125">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9fb61-125">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9fb61-126">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.</span><span class="sxs-lookup"><span data-stu-id="9fb61-126">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fb61-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9fb61-127">Remarks</span></span>

<span data-ttu-id="9fb61-128">Ein Filter wird rekursiv auf jede Textur Ebene angewendet, um die nächste Textur Ebene zu generieren.</span><span class="sxs-lookup"><span data-stu-id="9fb61-128">A filter is recursively applied to each texture level to generate the next texture level.</span></span>

<span data-ttu-id="9fb61-129">Das Schreiben in eine Oberfläche ohne Ebene der Textur bewirkt nicht, dass das geänderte Rechteck aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="9fb61-129">Writing to a non-level-zero surface of the texture will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="9fb61-130">Wenn **D3DXFilterTexture** aufgerufen wird und die Oberfläche nicht bereits geändert wurde (Dies ist unwahrscheinlich in normalen Verwendungs Szenarien), muss die Anwendung [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) explizit für die Textur aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9fb61-130">If **D3DXFilterTexture** is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) on the texture.</span></span>

<span data-ttu-id="9fb61-131">Texturen, die im Standard Pool (D3DPOOL \_ Default) erstellt werden, können nicht mit **D3DXFilterTexture** verwendet werden (es sei denn, Sie werden mit D3DUSAGE \_ Dynamic erstellt), da ein Sperr Vorgang für das Objekt erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="9fb61-131">Textures created in the default pool (D3DPOOL\_DEFAULT) cannot be used with **D3DXFilterTexture** (unless created with D3DUSAGE\_DYNAMIC) because a lock operation is needed on the object.</span></span> <span data-ttu-id="9fb61-132">Beachten Sie, dass Sperren für Texturen im Standard Pool nicht zulässig sind (es sei denn, Sie sind dynamisch).</span><span class="sxs-lookup"><span data-stu-id="9fb61-132">Note that locks are prohibited on textures in the default pool (unless they are dynamic).</span></span>

<span data-ttu-id="9fb61-133">Ausführliche Informationen zu [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)finden Sie unter Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="9fb61-133">For details on [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry), see the Platform SDK.</span></span> <span data-ttu-id="9fb61-134">Beachten Sie, dass der Member "Peer Flags" der **PaletteEntry** -Struktur ab DirectX 8,0 nicht wie im Platform SDK dokumentiert funktioniert.</span><span class="sxs-lookup"><span data-stu-id="9fb61-134">Note that as of DirectX 8.0, the peFlags member of the **PALETTEENTRY** structure does not function as documented in the Platform SDK.</span></span> <span data-ttu-id="9fb61-135">Der peflags-Member ist nun der Alphakanal für 8-Bit-Paletten-Formate.</span><span class="sxs-lookup"><span data-stu-id="9fb61-135">The peFlags member is now the alpha channel for 8-bit palettized formats.</span></span>

<span data-ttu-id="9fb61-136">Es gibt nur eine Textur Filterungs Funktion, aber zwei Makros, die diese Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="9fb61-136">There is only one texture filtering function, but two macros that call this method.</span></span>


```
#define D3DXFilterCubeTexture D3DXFilterTexture
#define D3DXFilterVolumeTexture D3DXFilterTexture
```



## <a name="requirements"></a><span data-ttu-id="9fb61-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9fb61-137">Requirements</span></span>



| <span data-ttu-id="9fb61-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9fb61-138">Requirement</span></span> | <span data-ttu-id="9fb61-139">Wert</span><span class="sxs-lookup"><span data-stu-id="9fb61-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9fb61-140">Header</span><span class="sxs-lookup"><span data-stu-id="9fb61-140">Header</span></span><br/>  | <dl> <span data-ttu-id="9fb61-141"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fb61-141"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="9fb61-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9fb61-142">Library</span></span><br/> | <dl> <span data-ttu-id="9fb61-143"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9fb61-143"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="9fb61-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9fb61-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fb61-145">Textur Funktionen in D3DX 9</span><span class="sxs-lookup"><span data-stu-id="9fb61-145">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
