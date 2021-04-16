---
description: 'Ruft ID3DXSprite:: Flush auf und stellt den Gerätezustand vor dem Aufrufen von ID3DXSprite:: begin wieder her.'
ms.assetid: 603c69f7-13a8-4646-b367-6f2d21b1a2a0
title: 'ID3DXSprite:: End-Methode (D3dx9core. h)'
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
ms.openlocfilehash: f2991cb8a4ae62b5d9ec71450d8e55fbdcdce050
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394185"
---
# <a name="id3dxspriteend-method"></a>ID3DXSprite:: End-Methode

Ruft [**ID3DXSprite:: Flush**](id3dxsprite--flush.md) auf und stellt den Gerätezustand vor dem Aufrufen von [**ID3DXSprite:: begin**](id3dxsprite--begin.md) wieder her.

## <a name="syntax"></a>Syntax


```C++
HRESULT End();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben. D3DERR \_ invalidcall

## <a name="remarks"></a>Bemerkungen

**ID3DXSprite:: End** kann nicht als Ersatz für [**IDirect3DDevice9:: EndScene**](/windows/desktop/api) oder [**ID3DXRenderToSurface:: EndScene**](id3dxrendertosurface--endscene.md)verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[**ID3DXSprite:: begin**](id3dxsprite--begin.md)
</dt> </dl>

 

 




