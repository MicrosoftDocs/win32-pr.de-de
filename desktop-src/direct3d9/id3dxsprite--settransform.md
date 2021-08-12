---
description: Legt die Spritetransformation fest.
ms.assetid: 87dfc169-b647-4a96-897d-abbe765ea9e2
title: ID3DXSprite::SetTransform-Methode (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.SetTransform
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fba7c21d0ba0e99aefc5c4d5dfd69301bb706f804e736badcbe0227d58aca81a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118292617"
---
# <a name="id3dxspritesettransform-method"></a>ID3DXSprite::SetTransform-Methode

Legt die Spritetransformation fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetTransform(
  [in] const D3DXMATRIX *pTransform
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pTransform* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Zeiger auf ein [**D3DXMATRIX,das**](d3dxmatrix.md) eine Transformation des Sprite aus dem ursprünglichen Weltraum enthält. Verwenden Sie diese Transformation, um den Sprite zu skalieren, zu drehen oder zu transformieren.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben. D3DERR \_ INVALIDCALL

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[Transformationen (Direct3D 9)](transforms.md)
</dt> </dl>

 

 




