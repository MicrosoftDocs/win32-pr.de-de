---
description: 'ID3DXMATRIXStack::MultMatrix-Methode (D3dx9math.h): Bestimmt das Produkt der aktuellen Matrix und der angegebenen Matrix.'
ms.assetid: a673ce82-6fed-4a3f-8c37-d0db11195f06
title: ID3DXMATRIXStack::MultMatrix-Methode (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.MultMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d9d0808f1b23475b823ea43f55d93f8dacb01e4e491957fa34100110946fa72e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856460"
---
# <a name="id3dxmatrixstackmultmatrix-method-d3dx9mathh"></a>ID3DXMATRIXStack::MultMatrix-Methode (D3dx9math.h)

Bestimmt das Produkt der aktuellen Matrix und der angegebenen Matrix.

## <a name="syntax"></a>Syntax


```C++
HRESULT MultMatrix(
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

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="remarks"></a>Hinweise

Diese Methode multipliziert die angegebene Matrix rechts mit der aktuellen Matrix (die Transformation geht um den aktuellen Ursprung der Welt).


```
m_pstack[m_currentPos] = m_pstack[m_currentPos] * (*pMat);
```



Diese Methode fügt dem Stapel kein Element hinzu. Sie ersetzt die aktuelle Matrix durch das Produkt der aktuellen Matrix und der angegebenen Matrix.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack::MultMatrixLocal**](id3dxmatrixstack--multmatrixlocal.md)
</dt> </dl>

 

 




