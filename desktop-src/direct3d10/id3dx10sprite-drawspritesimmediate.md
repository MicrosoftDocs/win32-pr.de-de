---
description: Zeichnen sie ein Array von Sprites.
ms.assetid: 3fcc7705-0d59-450e-b137-c9cb7ec6b1ea
title: ID3DX10Sprite::D rawSpritesImmediate-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.DrawSpritesImmediate
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0a3295d64efc3f3ff05b39e0866a15fb7eed9ba2d8c580fe2c7b219d36708e02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046898"
---
# <a name="id3dx10spritedrawspritesimmediate-method"></a>ID3DX10Sprite::D rawSpritesImmediate-Methode

Zeichnen sie ein Array von Sprites. Dadurch werden die Sprites sofort zum Rendern an das Gerät gesendet, das sich von [**ID3DX10Sprite::D rawSpritesBuffered**](id3dx10sprite-drawspritesbuffered.md) unterscheidet und nur ein Array von Sprites zu einem Batch von Sprites hinzufügt, die gerendert werden sollen, wenn [**ID3DX10Sprite::Flush**](id3dx10sprite-flush.md) aufgerufen wird. Diese Draw-Methode ist besonders nützlich beim Zeichnen einer großen Anzahl von Sprites, die bereits auf der CPU sortiert wurden (oder nicht sortiert werden müssen), z. B. in einem Partikelsystem. Dies muss zwischen Aufrufen von [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md) und [**ID3DX10Sprite::End**](id3dx10sprite-end.md)aufgerufen werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT DrawSpritesImmediate(
  [in] D3DX10_SPRITE *pSprites,
  [in] UINT          cSprites,
  [in] UINT          cbSprite,
  [in] UINT          flags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSprites* \[ In\]
</dt> <dd>

Typ: **[ **D3DX10 \_ SPRITE**](d3dx10-sprite.md)\***

Das Zu zeichnende Array von Sprites. Siehe [**D3DX10 \_ SPRITE**](d3dx10-sprite.md).

</dd> <dt>

*cSprites* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Die Anzahl der Sprites in pSprites.

</dd> <dt>

*cbSprite* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Die Größe der Spritestruktur, die Sie an pSprites übergeben. Das Übergeben von 0 entspricht der Übergabe von sizeof(D3DX10 \_ SPRITE).

</dd> <dt>

*Flags* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10Sprite](id3dx10sprite.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
