---
description: Legt die linkshändige Weltansichtstransformation für ein Sprite fest. Ein Aufruf dieser Methode ist erforderlich, bevor Sprites umgezweigt oder sortiert werden.
ms.assetid: 70f1181d-41f9-4663-91e0-8df94bce4eed
title: ID3DXSprite::SetWorldViewLH-Methode (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.SetWorldViewLH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 67ee276b90629a18f93bd9a26879e8a7ad62d71ae46baf2d2c0a6bfba82a53a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118292572"
---
# <a name="id3dxspritesetworldviewlh-method"></a>ID3DXSprite::SetWorldViewLH-Methode

Legt die linkshändige Weltansichtstransformation für ein Sprite fest. Ein Aufruf dieser Methode ist erforderlich, bevor Sprites umgezweigt oder sortiert werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetWorldViewLH(
  [in] const D3DXMATRIX *pWorld,
  [in] const D3DXMATRIX *pView
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pWorld* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Zeiger auf eine [**D3DXMATRIX,**](d3dxmatrix.md) die eine Welttransformation enthält. Bei **NULL** wird die Identitätsmatrix für die Welttransformation verwendet.

</dd> <dt>

*pView* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Zeiger auf eine [**D3DXMATRIX, die**](d3dxmatrix.md) eine Ansichtstransformation enthält. Bei **NULL** wird die Identitätsmatrix für die Ansichtstransformation verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn bei der Methode ein Fehler auftritt, wird der folgende Wert zurückgegeben. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Hinweise

Ein Aufruf dieser Methode (oder von [**ID3DXSprite::SetWorldViewRH)**](id3dxsprite--setworldviewrh.md)ist erforderlich, wenn das Sprite mit dem [Flagwert D3DXSprite \_ \_ ALPHABET,](d3dxsprite.md)D3DXSprite \_ \_ SORT DEPTH \_ FRONTTOBACK oder \_ D3DXSprite \_ \_ SORT DEPTH \_ \_ BACKTOFRONT in [**ID3DXSprite::Begin**](id3dxsprite--begin.md)gerendert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> </dl>

 

 




