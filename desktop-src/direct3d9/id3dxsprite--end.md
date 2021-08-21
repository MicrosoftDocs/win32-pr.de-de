---
description: Ruft ID3DXSprite::Flush auf und stellt den Zustand des Geräts wieder her, wie er vor dem Aufruf von ID3DXSprite::Begin war.
ms.assetid: 603c69f7-13a8-4646-b367-6f2d21b1a2a0
title: ID3DXSprite::End-Methode (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.End
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: aeade03ea423d08e412fe35f7c710c9d449cd74c3ed742627ed62954c6011f0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118094122"
---
# <a name="id3dxspriteend-method"></a>ID3DXSprite::End-Methode

Ruft [**ID3DXSprite::Flush**](id3dxsprite--flush.md) auf und stellt den Zustand des Geräts wieder her, wie er vor dem Aufruf von [**ID3DXSprite::Begin**](id3dxsprite--begin.md) war.

## <a name="syntax"></a>Syntax


```C++
HRESULT End();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Hinweise

**ID3DXSprite::End** kann nicht als Ersatz für [**IDirect3DDevice9::EndScene**](/windows/desktop/api) oder [**ID3DXRenderToSurface::EndScene**](id3dxrendertosurface--endscene.md)verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[**ID3DXSprite::Begin**](id3dxsprite--begin.md)
</dt> </dl>

 

 




