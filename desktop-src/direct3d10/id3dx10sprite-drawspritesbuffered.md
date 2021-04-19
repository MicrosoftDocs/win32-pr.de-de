---
description: Fügen Sie dem Batch von Sprites, die gerendert werden sollen, ein Array von Sprites hinzu.
ms.assetid: e6a9f806-7244-4139-b47e-c46dfab38a31
title: ID3DX10Sprite::D rawspritesbuffered-Methode (d3dx10. h)
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
ms.openlocfilehash: 72893f6a8c3cf82c67f014b4bdbb9a92453de319
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364015"
---
# <a name="id3dx10spritedrawspritesbuffered-method"></a>ID3DX10Sprite::D rawspritesbuffered-Methode

Fügen Sie dem Batch von Sprites, die gerendert werden sollen, ein Array von Sprites hinzu. Dies muss zwischen Aufrufen von [**ID3DX10Sprite:: begin**](id3dx10sprite-begin.md) und [**ID3DX10Sprite:: End**](id3dx10sprite-end.md)aufgerufen werden, und [**ID3DX10Sprite:: Flush**](id3dx10sprite-flush.md) muss vor Ende aufgerufen werden, um alle Batch Sprites zum Rendering an das Gerät zu senden. Diese Draw-Methode ist besonders nützlich, wenn Sie eine kleine Anzahl von Sprites zeichnen möchten, die Sie in einem großen Batch, wie z. b. Schriftarten, gepuffert werden

## <a name="syntax"></a>Syntax


```C++
HRESULT DrawSpritesBuffered(
  [in] D3DX10_SPRITE *pSprites,
  [in] UINT          cSprites
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

 

 
