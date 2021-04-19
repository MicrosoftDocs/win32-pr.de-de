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
# <a name="d3dx10_sprite-structure"></a>D3dx10 \_ Sprite-Struktur

Definiert Positions-, Textur-und Farbinformationen zu einem Sprite.

## <a name="syntax"></a>Syntax


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



## <a name="members"></a>Member

<dl> <dt>

**matworld**
</dt> <dd>

Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)**

</dd> <dd>

Die Transformation für das Modell der Sprite-Welt. Dadurch werden die Position und Ausrichtung des Sprite im Raum der Welt definiert.

</dd> <dt>

**Texcoord**
</dt> <dd>

Typ: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**

</dd> <dd>

Der Offset von der oberen linken Ecke der Textur, die angibt, wo das Sprite-Bild in der Textur beginnen soll. **Texcoord** ist in Texturkoordinaten.

</dd> <dt>

**Texsize**
</dt> <dd>

Typ: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**

</dd> <dd>

Ein Vektor, der die Breite und Höhe des Sprite in Texturkoordinaten enthält.

</dd> <dt>

**Colormodulate**
</dt> <dd>

Typ: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**

</dd> <dd>

Eine Farbe, die vor dem Rendering mit der Pixelfarbe multipliziert wird.

</dd> <dt>

**ptexture**
</dt> <dd>

Typ: **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\***

</dd> <dd>

Ein Zeiger auf eine Shader-Ressourcen Ansicht, die die Struktur des Sprite darstellt. Siehe [**ID3D10ShaderResourceView-Schnittstelle**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview).

</dd> <dt>

**Textureindex**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Der Index der Textur. Wenn ptexture kein Textur Array darstellt, sollte dies 0 sein.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx10. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
