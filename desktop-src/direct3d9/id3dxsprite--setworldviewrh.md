---
description: Legt die rechtshändige Weltansichtstransformation für einen Sprite fest. Vor dem Aufstellen oder Sortieren von Sprites ist ein Aufruf dieser Methode erforderlich.
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

Legt die rechtshändige Weltansichtstransformation für einen Sprite fest. Vor dem Aufstellen oder Sortieren von Sprites ist ein Aufruf dieser Methode erforderlich.

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

Zeiger auf eine [**D3DXMATRIX,die**](d3dxmatrix.md) eine Welttransformation enthält. Bei **NULL** wird die Identitätsmatrix für die Welttransformation verwendet.

</dd> <dt>

*pView* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Zeiger auf eine [**D3DXMATRIX-Datei,**](d3dxmatrix.md) die eine Ansichtstransformation enthält. Null gibt an, dass die Identitätsmatrix für die Ansichtstransformation verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Hinweise

Ein Aufruf dieser Methode (oder [**von ID3DXSprite::SetWorldViewLH)**](id3dxsprite--setworldviewlh.md)ist erforderlich, wenn der Sprite mit dem [D3DXSprite-FLAG, \_ \_](d3dxsprite.md)D3DXSprite \_ \_ SORT DEPTH \_ \_ FRONTTOBACK oder D3DXSprite \_ \_ SORT DEPTH \_ \_ BACKTOFRONT-Flagwert in [**ID3DXSprite::Begin**](id3dxsprite--begin.md)gerendert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> </dl>

 

 




