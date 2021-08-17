---
description: Legt die rechtshändige World View-Transformation für ein Sprite fest. Ein Aufruf dieser Methode ist erforderlich, bevor Sprites umgezweigt oder sortiert werden.
ms.assetid: 83654e9a-8991-49ec-ab28-cf9063126dbe
title: ID3DXSprite::SetWorldViewRH-Methode (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.SetWorldViewRH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 54da854fff0aeb2001e674218a7e7868971a6cf43af7bc00606b124c3f082b9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118800418"
---
# <a name="id3dxspritesetworldviewrh-method"></a>ID3DXSprite::SetWorldViewRH-Methode

Legt die rechtshändige World View-Transformation für ein Sprite fest. Ein Aufruf dieser Methode ist erforderlich, bevor Sprites umgezweigt oder sortiert werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetWorldViewRH(
  [in] const D3DXMATRIX *pWorld,
  [in] const D3DXMATRIX *pView
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pWorld* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Zeiger auf eine [**D3DXMATRIX, die**](d3dxmatrix.md) eine Welttransformation enthält. Bei **NULL** wird die Identitätsmatrix für die Welttransformation verwendet.

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

Ein Aufruf dieser Methode (oder von [**ID3DXSprite::SetWorldViewLH**](id3dxsprite--setworldviewlh.md)) ist erforderlich, wenn das Sprite mit dem [Flagwert D3DXSprite \_ \_ ALPHABET,](d3dxsprite.md)D3DXSprite \_ \_ SORT DEPTH \_ FRONTTOBACK oder \_ D3DXSprite \_ \_ SORT DEPTH \_ \_ BACKTOFRONT in [**ID3DXSprite::Begin**](id3dxsprite--begin.md)gerendert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> </dl>

 

 




