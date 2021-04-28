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
ms.openlocfilehash: 7361223e8fbcbae0f81641718b216c5903ff6319
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093528"
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

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="remarks"></a>Bemerkungen

Diese Methode multipliziert die gegebene Matrix mit der aktuellen Matrix (die Transformation bezieht sich auf den aktuellen Ursprung der Welt).


```
m_pstack[m_currentPos] = m_pstack[m_currentPos] * (*pMat);
```



Diese Methode fügt dem Stapel kein Element hinzu, sondern ersetzt die aktuelle Matrix durch das Produkt der aktuellen Matrix und der angegebenen Matrix.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack::MultMatrixLocal**](id3dxmatrixstack--multmatrixlocal.md)
</dt> </dl>

 

 




