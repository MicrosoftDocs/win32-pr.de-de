---
description: Erstellen Sie einen Sprite zum Zeichnen einer 2D-Textur. Hinweis Anstatt diese Funktion zu verwenden, wird empfohlen, Direct2D und die DirectXTK-Bibliothek SpriteBatch-Klasse zu verwenden.
ms.assetid: 64efb8e4-da0b-4e67-874a-e0bb0083961c
title: D3DX10CreateSprite-Funktion (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateSprite
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 6f67a0a6e0be8a3ea71ff1eef46d72b6cf080d028e7cc32f72a52db6a209cea4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118541059"
---
# <a name="d3dx10createsprite-function"></a>D3DX10CreateSprite-Funktion

Erstellen Sie einen Sprite zum Zeichnen einer 2D-Textur.

> [!Note]  
> Anstatt diese Funktion zu verwenden, wird empfohlen, [Direct2D](../direct2d/direct2d-portal.md) und die [DirectXTK-Bibliothek](https://github.com/Microsoft/DirectXTK) **SpriteBatch-Klasse** zu verwenden.

 

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX10CreateSprite(
  _In_  ID3D10Device   *pDevice,
  _In_  UINT           cDeviceBufferSize,
  _Out_ LPD3DX10SPRITE *ppSprite
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDevice* \[ In\]
</dt> <dd>

Typ: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Ein Zeiger auf das Gerät (siehe [**ID3D10Device-Schnittstelle),**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)das den Sprite zeichnet.

</dd> <dt>

*cDeviceBufferSize* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Die Größe des Scheitelpunktpuffers in der Anzahl von Sprites, die an das Gerät gesendet wird, wenn [**ID3DX10Sprite::Flush**](id3dx10sprite-flush.md) oder [**ID3DX10Sprite::D rawSpritesImmediate**](id3dx10sprite-drawspritesimmediate.md) aufgerufen wird. Dies sollte eine kleine Zahl sein, wenn Sie wissen, dass Sie eine kleine Anzahl von Sprites gleichzeitig rendern (um Arbeitsspeicher zu sparen), und eine große Zahl, wenn Sie wissen, dass Sie eine große Anzahl von Sprites gleichzeitig rendern werden. Der Höchstwert ist 4096. Wenn 0 angegeben wird, wird die Vertexpuffergröße automatisch auf 4096 festgelegt.

</dd> <dt>

*ppSprite* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DX10SPRITE**](id3dx10sprite.md)\***

Die Adresse eines Zeigers auf eine Sprite-Schnittstelle (siehe [**ID3DX10Sprite-Schnittstelle).**](id3dx10sprite.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert S \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Universell Functions](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
