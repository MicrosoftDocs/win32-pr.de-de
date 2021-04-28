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
ms.openlocfilehash: 509aff4dd21f62033dc1e4672d29aad57445f9ee
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093518"
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

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="remarks"></a>Bemerkungen

Diese Methode multipliziert die angegebene Matrix links mit der aktuellen Matrix (die Transformation geht um den lokalen Ursprung des Objekts).


```
m_pstack[m_currentPos] = (*pMat) * m_pstack[m_currentPos];
```



Diese Methode fügt dem Stapel kein Element hinzu. Sie ersetzt die aktuelle Matrix durch das Produkt der angegebenen Matrix und der aktuellen Matrix.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack::MultMatrix**](id3dxmatrixstack--multmatrix.md)
</dt> </dl>

 

 




