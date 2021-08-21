---
description: 'ID3DXMATRIXStack::MultMatrixLocal-Methode (D3DX10.h): Bestimmt das Produkt der angegebenen Matrix und der aktuellen Matrix.'
ms.assetid: 4d374a7b-99e0-4313-970d-b0e7cf3e97ce
title: ID3DXMATRIXStack::MultMatrixLocal-Methode (D3DX10.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 52ca669b6b0136c0c1ae094958f3ffe4d27d5d86f291f3f203d8088a662cfd61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046858"
---
# <a name="id3dxmatrixstackmultmatrixlocal-method-d3dx10h"></a>ID3DXMATRIXStack::MultMatrixLocal-Methode (D3DX10.h)

Bestimmt das Produkt der angegebenen Matrix und der aktuellen Matrix.

## <a name="syntax"></a>Syntax


```C++
HRESULT MultMatrixLocal(
  [in] const D3DXMATRIX *pM
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pM* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Zeiger auf die D3DXMATRIX-Struktur, die mit der aktuellen Matrix multipliziert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="remarks"></a>Hinweise

Diese Methode multipliziert die angegebene Matrix links mit der aktuellen Matrix (die Transformation geht um den lokalen Ursprung des Objekts).


```
m_pstack[m_currentPos] = (*pMat) * m_pstack[m_currentPos];
```



Diese Methode fügt dem Stapel kein Element hinzu. Sie ersetzt die aktuelle Matrix durch das Produkt der angegebenen Matrix und der aktuellen Matrix.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXMatrixStack](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
