---
description: Ruft die Spritetransformation ab.
ms.assetid: d91f2776-ee87-42b3-998b-fccea178cee2
title: ID3DXSprite::GetTransform-Methode (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.GetTransform
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5bed9e7ae8cccca03654113ed48245b11124e1b6fd001a11074933ea4e34738a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118094052"
---
# <a name="id3dxspritegettransform-method"></a>ID3DXSprite::GetTransform-Methode

Ruft die Spritetransformation ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTransform(
  [in] D3DXMATRIX *pTransform
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pTransform* \[ In\]
</dt> <dd>

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Zeiger auf ein [**D3DXMATRIX,das**](d3dxmatrix.md) eine Transformation des Sprite aus dem ursprünglichen Weltraum enthält.

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
</dt> </dl>

 

 




