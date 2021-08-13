---
description: Fügen Sie dem Zu rendernden Sprites-Batch ein Array von Sprites hinzu.
ms.assetid: e6a9f806-7244-4139-b47e-c46dfab38a31
title: ID3DX10Sprite::D rawSpritesBuffered-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.DrawSpritesBuffered
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: bee3fd9344e393d2b5b9ddf6162286507fac918ea15f9abde2abcc2f80a5b65d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118540037"
---
# <a name="id3dx10spritedrawspritesbuffered-method"></a>ID3DX10Sprite::D rawSpritesBuffered-Methode

Fügen Sie dem Zu rendernden Sprites-Batch ein Array von Sprites hinzu. Dies muss zwischen Aufrufen von [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md) und [**ID3DX10Sprite::End**](id3dx10sprite-end.md)aufgerufen werden, und [**ID3DX10Sprite::Flush**](id3dx10sprite-flush.md) muss vor End aufgerufen werden, um alle Batch-Sprites zum Rendern an das Gerät zu senden. Diese Draw-Methode ist besonders nützlich beim Zeichnen einer kleinen Anzahl von Sprites, die in einen großen Batch gepuffert werden sollen, z. B. Schriftarten.

## <a name="syntax"></a>Syntax


```C++
HRESULT DrawSpritesBuffered(
  [in] D3DX10_SPRITE *pSprites,
  [in] UINT          cSprites
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

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[ID3DX10Sprite](id3dx10sprite.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
