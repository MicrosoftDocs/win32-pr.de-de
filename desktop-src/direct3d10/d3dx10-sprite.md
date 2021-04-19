---
description: Definiert Positions-, Textur-und Farbinformationen zu einem Sprite.
ms.assetid: 4b8d1ed1-75d5-418c-b809-410c6a44d425
title: D3DX10_SPRITE-Struktur (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_SPRITE
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: b896b8158e84caa841addbac7abae8c972c06acd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370460"
---
# <a name="d3dx10_sprite-structure"></a><span data-ttu-id="9ce59-103">D3dx10 \_ Sprite-Struktur</span><span class="sxs-lookup"><span data-stu-id="9ce59-103">D3DX10\_SPRITE structure</span></span>

<span data-ttu-id="9ce59-104">Definiert Positions-, Textur-und Farbinformationen zu einem Sprite.</span><span class="sxs-lookup"><span data-stu-id="9ce59-104">Defines position, texture, and color information about a sprite.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ce59-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ce59-105">Syntax</span></span>


```C++
typedef struct D3DX10_SPRITE {
  D3DXMATRIX               matWorld;
  D3DXVECTOR2              TexCoord;
  D3DXVECTOR2              TexSize;
  D3DXCOLOR                ColorModulate;
  ID3D10ShaderResourceView *pTexture;
  UINT                     TextureIndex;
} D3DX10_SPRITE;
```



## <a name="members"></a><span data-ttu-id="9ce59-106">Member</span><span class="sxs-lookup"><span data-stu-id="9ce59-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9ce59-107">**matworld**</span><span class="sxs-lookup"><span data-stu-id="9ce59-107">**matWorld**</span></span>
</dt> <dd>

<span data-ttu-id="9ce59-108">Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)**</span><span class="sxs-lookup"><span data-stu-id="9ce59-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9ce59-109">Die Transformation für das Modell der Sprite-Welt.</span><span class="sxs-lookup"><span data-stu-id="9ce59-109">The sprite's model-world transformation.</span></span> <span data-ttu-id="9ce59-110">Dadurch werden die Position und Ausrichtung des Sprite im Raum der Welt definiert.</span><span class="sxs-lookup"><span data-stu-id="9ce59-110">This defines the position and orientation of the sprite in world space.</span></span>

</dd> <dt>

<span data-ttu-id="9ce59-111">**Texcoord**</span><span class="sxs-lookup"><span data-stu-id="9ce59-111">**TexCoord**</span></span>
</dt> <dd>

<span data-ttu-id="9ce59-112">Typ: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**</span><span class="sxs-lookup"><span data-stu-id="9ce59-112">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9ce59-113">Der Offset von der oberen linken Ecke der Textur, die angibt, wo das Sprite-Bild in der Textur beginnen soll.</span><span class="sxs-lookup"><span data-stu-id="9ce59-113">Offset from the upper-left corner of the texture indicating where the sprite image should start in the texture.</span></span> <span data-ttu-id="9ce59-114">**Texcoord** ist in Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="9ce59-114">**TexCoord** is in texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="9ce59-115">**Texsize**</span><span class="sxs-lookup"><span data-stu-id="9ce59-115">**TexSize**</span></span>
</dt> <dd>

<span data-ttu-id="9ce59-116">Typ: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**</span><span class="sxs-lookup"><span data-stu-id="9ce59-116">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9ce59-117">Ein Vektor, der die Breite und Höhe des Sprite in Texturkoordinaten enthält.</span><span class="sxs-lookup"><span data-stu-id="9ce59-117">A vector containing the width and height of the sprite in texture coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="9ce59-118">**Colormodulate**</span><span class="sxs-lookup"><span data-stu-id="9ce59-118">**ColorModulate**</span></span>
</dt> <dd>

<span data-ttu-id="9ce59-119">Typ: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="9ce59-119">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9ce59-120">Eine Farbe, die vor dem Rendering mit der Pixelfarbe multipliziert wird.</span><span class="sxs-lookup"><span data-stu-id="9ce59-120">A color that will be multiplied with the pixel color before rendering.</span></span>

</dd> <dt>

<span data-ttu-id="9ce59-121">**ptexture**</span><span class="sxs-lookup"><span data-stu-id="9ce59-121">**pTexture**</span></span>
</dt> <dd>

<span data-ttu-id="9ce59-122">Typ: **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\***</span><span class="sxs-lookup"><span data-stu-id="9ce59-122">Type: **[**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\***</span></span>

</dd> <dd>

<span data-ttu-id="9ce59-123">Ein Zeiger auf eine Shader-Ressourcen Ansicht, die die Struktur des Sprite darstellt.</span><span class="sxs-lookup"><span data-stu-id="9ce59-123">Pointer to a shader-resource view representing the sprite's texture.</span></span> <span data-ttu-id="9ce59-124">Siehe [**ID3D10ShaderResourceView-Schnittstelle**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="9ce59-124">See [**ID3D10ShaderResourceView Interface**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview).</span></span>

</dd> <dt>

<span data-ttu-id="9ce59-125">**Textureindex**</span><span class="sxs-lookup"><span data-stu-id="9ce59-125">**TextureIndex**</span></span>
</dt> <dd>

<span data-ttu-id="9ce59-126">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9ce59-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9ce59-127">Der Index der Textur.</span><span class="sxs-lookup"><span data-stu-id="9ce59-127">The index of the texture.</span></span> <span data-ttu-id="9ce59-128">Wenn ptexture kein Textur Array darstellt, sollte dies 0 sein.</span><span class="sxs-lookup"><span data-stu-id="9ce59-128">If pTexture does not represent a texture array, then this should be 0.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9ce59-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ce59-129">Requirements</span></span>



| <span data-ttu-id="9ce59-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ce59-130">Requirement</span></span> | <span data-ttu-id="9ce59-131">Wert</span><span class="sxs-lookup"><span data-stu-id="9ce59-131">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9ce59-132">Header</span><span class="sxs-lookup"><span data-stu-id="9ce59-132">Header</span></span><br/> | <dl> <span data-ttu-id="9ce59-133"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ce59-133"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ce59-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ce59-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ce59-135">D3DX-Strukturen</span><span class="sxs-lookup"><span data-stu-id="9ce59-135">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
