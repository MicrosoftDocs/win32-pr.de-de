---
description: Zeichnen Sie ein Array von Sprites.
ms.assetid: 3fcc7705-0d59-450e-b137-c9cb7ec6b1ea
title: ID3DX10Sprite::D rawspritesimvermittler-Methode (d3dx10. h)
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
ms.openlocfilehash: 7fa4012f5f589c7bc0d1f789599da142194f6e08
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356117"
---
# <a name="id3dx10spritedrawspritesimmediate-method"></a>ID3DX10Sprite::D rawspritesimvermittler-Methode

Zeichnen Sie ein Array von Sprites. Dadurch werden die Sprites sofort zum Rendern an das Gerät gesendet. Dies unterscheidet sich von [**ID3DX10Sprite::D rawspritesbuffered**](id3dx10sprite-drawspritesbuffered.md) , das nur ein Array von Sprites zu einem Batch von Sprites hinzufügt, die gerendert werden, wenn [**ID3DX10Sprite:: Flush**](id3dx10sprite-flush.md) aufgerufen wird. Diese Draw-Methode ist besonders nützlich, wenn eine große Anzahl von Sprites gezeichnet wird, die bereits auf der CPU sortiert wurden (oder nicht sortiert werden müssen), z. b. in einem Partikelsystem. Dies muss zwischen Aufrufen von [**ID3DX10Sprite:: begin**](id3dx10sprite-begin.md) und [**ID3DX10Sprite:: End**](id3dx10sprite-end.md)aufgerufen werden.

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

*psprites* \[ in\]
</dt> <dd>

Typ: **[ **d3dx10 \_ Sprite**](d3dx10-sprite.md)\***

Das Array von Sprites, das gezeichnet werden soll. Siehe [**d3dx10 \_ Sprite**](d3dx10-sprite.md).

</dd> <dt>

*csprites* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die Anzahl der Sprites in psprites.

</dd> <dt>

*cbsprite* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die Größe der Sprite-Struktur, die an psprites übergeben wird. Das übergeben von 0 entspricht der Übergabe von sizeof (d3dx10 \_ Sprite).

</dd> <dt>

*Flags* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ InvalidData.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx10. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10Sprite](id3dx10sprite.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
