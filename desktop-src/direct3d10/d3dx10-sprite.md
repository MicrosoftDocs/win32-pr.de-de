---
description: Definiert Positions-, Textur- und Farbinformationen zu einem Sprite.
ms.assetid: 4b8d1ed1-75d5-418c-b809-410c6a44d425
title: D3DX10_SPRITE-Struktur (D3DX10.h)
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
ms.openlocfilehash: ec8b220d55d3ac55d2a8b68fa3b95398a395611da150235d03314114055214e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753510"
---
# <a name="d3dx10_sprite-structure"></a>D3DX10 \_ SPRITE-Struktur

Definiert Positions-, Textur- und Farbinformationen zu einem Sprite.

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

**matWorld**
</dt> <dd>

Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)**

</dd> <dd>

Die Modellwelttransformation des Sprite. Dies definiert die Position und Ausrichtung des Sprites im Weltraum.

</dd> <dt>

**TexCoord**
</dt> <dd>

Typ: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**

</dd> <dd>

Offset von der oberen linken Ecke der Textur, die angibt, wo das Spritebild in der Textur beginnen soll. **TexCoord** befindet sich in Texturkoordinaten.

</dd> <dt>

**TexSize**
</dt> <dd>

Typ: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**

</dd> <dd>

Ein Vektor, der die Breite und Höhe des Sprites in Texturkoordinaten enthält.

</dd> <dt>

**ColorModulate**
</dt> <dd>

Typ: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**

</dd> <dd>

Eine Farbe, die vor dem Rendern mit der Pixelfarbe multipliziert wird.

</dd> <dt>

**pTexture**
</dt> <dd>

Typ: **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\***

</dd> <dd>

Zeiger auf eine Shader-Ressourcenansicht, die die Textur des Sprite darstellt. Siehe [**ID3D10ShaderResourceView-Schnittstelle.**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)

</dd> <dt>

**TextureIndex**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Der Index der Textur. Wenn pTexture kein Texturarray darstellt, sollte dies 0 sein.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Strukturen](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
