---
description: 'ID3DXMATRIXStack::MultMatrixLocal-Methode (D3dx9math.h): Bestimmt das Produkt der angegebenen Matrix und der aktuellen Matrix.'
ms.assetid: 6f909b38-821c-4173-aba9-fd4392f70551
title: ID3DXMATRIXStack::MultMatrixLocal-Methode (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.MultMatrixLocal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b08a50f6477be6106ce6eaf82c0111f805ed00472259283429e1f638579c91a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120814"
---
# <a name="id3dxmatrixstackmultmatrixlocal-method-d3dx9mathh"></a>ID3DXMATRIXStack::MultMatrixLocal-Methode (D3dx9math.h)

Bestimmt das Produkt der angegebenen Matrix und der aktuellen Matrix.

## <a name="syntax"></a>Syntax


```C++
HRESULT MultMatrixLocal(
  [in] const D3DXMATRIX *pMat
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pMat* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Zeiger auf die [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die mit der aktuellen Matrix multipliziert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="remarks"></a>Hinweise

Diese Methode multipliziert die gegebene Matrix mit der aktuellen Matrix (die Transformation bezieht sich auf den lokalen Ursprung des Objekts).


```
m_pstack[m_currentPos] = (*pMat) * m_pstack[m_currentPos];
```



Diese Methode fügt dem Stapel kein Element hinzu, sondern ersetzt die aktuelle Matrix durch das Produkt der angegebenen Matrix und der aktuellen Matrix.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack::MultMatrix**](id3dxmatrixstack--multmatrix.md)
</dt> </dl>

 

 




