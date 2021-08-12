---
description: Bereiten Sie ein Gerät für das Zeichnen von Sprites vor.
ms.assetid: cffe5ac3-eeee-4ece-afcc-04a476b75863
title: ID3DX10Sprite::Begin-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.Begin
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e23ff3e4b8be62ac97f2874aa398770936bd84ab1c330c94efb87146046db847
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118302405"
---
# <a name="id3dx10spritebegin-method"></a>ID3DX10Sprite::Begin-Methode

Bereiten Sie ein Gerät für das Zeichnen von Sprites vor.

## <a name="syntax"></a>Syntax


```C++
HRESULT Begin(
  [in] UINT flags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Flags, die steuern, wie die Sprites gezeichnet werden. Siehe [**D3DX10 \_ \_ SPRITE-FLAG**](d3dx10-sprite-flag.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert einer der folgenden Sein: D3DERR \_ INVALIDCALL, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Hinweise

Jeder Aufruf von Begin muss mit einem Aufruf von [**ID3DX10Sprite::End übereinstimmen.**](id3dx10sprite-end.md)

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

 

 
