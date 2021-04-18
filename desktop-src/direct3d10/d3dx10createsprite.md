---
description: Erstellen Sie ein Sprite zum Zeichnen einer 2D-Textur. Beachten Sie, dass Sie anstelle dieser Funktion die Verwendung von Direct2D und der directxtk-Bibliothek, SpriteBatch Class, empfehlen.
ms.assetid: 64efb8e4-da0b-4e67-874a-e0bb0083961c
title: D3DX10CreateSprite-Funktion (d3dx10. h)
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
ms.openlocfilehash: cf40e303cb616f35ea5cd3526c263e3bd12ae428
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365299"
---
# <a name="d3dx10createsprite-function"></a>D3DX10CreateSprite-Funktion

Erstellen Sie ein Sprite zum Zeichnen einer 2D-Textur.

> [!Note]  
> Anstatt diese Funktion zu verwenden, empfehlen wir die Verwendung von [Direct2D](../direct2d/direct2d-portal.md) und der [directxtk](https://github.com/Microsoft/DirectXTK) -Bibliothek, **SpriteBatch** Class.

 

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

*pdevice* \[ in\]
</dt> <dd>

Typ: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Ein Zeiger auf das Gerät (siehe [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)), mit dem das Sprite gezeichnet wird.

</dd> <dt>

*cdevicebuffersize* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die Größe des Scheitelpunkt Puffers (in Anzahl von Sprites), die an das Gerät gesendet wird, wenn [**ID3DX10Sprite:: Flush**](id3dx10sprite-flush.md) oder [**ID3DX10Sprite::D rawspritesimvermittler**](id3dx10sprite-drawspritesimmediate.md) aufgerufen wird. Dies sollte eine kleine Zahl sein, wenn Sie wissen, dass Sie jeweils nur eine kleine Anzahl von Sprites Rendern (um Speicherplatz zu sparen), und eine große Zahl, wenn Sie wissen, dass Sie eine große Anzahl von Sprites gleichzeitig rendern werden. Der Höchstwert ist 4096. Wenn 0 angegeben wird, wird die Vertex-Puffergröße automatisch auf 4096 festgelegt.

</dd> <dt>

*ppsprite* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DX10SPRITE**](id3dx10sprite.md)\***

Die Adresse eines Zeigers auf eine Sprite-Schnittstelle (siehe [**ID3DX10Sprite-Schnittstelle**](id3dx10sprite.md)).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx10. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Universell Funktionen](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
