---
description: 'ID3DXMATRIXStack::MultMatrix-Methode (D3DX10.h): Bestimmt das Produkt der aktuellen Matrix und der angegebenen Matrix.'
ms.assetid: 72388919-e474-4433-b219-41e2d312848e
title: ID3DXMATRIXStack::MultMatrix-Methode (D3DX10.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 969cdebcee34add15cbf6bbcfbb1048387b2d7e8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107968"
---
# <a name="id3dxmatrixstackmultmatrix-method-d3dx10h"></a>ID3DXMATRIXStack::MultMatrix-Methode (D3DX10.h)

Bestimmt das Produkt der aktuellen Matrix und der angegebenen Matrix.

## <a name="syntax"></a>Syntax


```C++
HRESULT MultMatrix(
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

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="remarks"></a>Bemerkungen

Diese Methode multipliziert die gegebene Matrix mit der aktuellen Matrix (die Transformation bezieht sich auf den aktuellen Ursprung der Welt).


```
m_pstack[m_currentPos] = m_pstack[m_currentPos] * (*pMat);
```



Diese Methode fügt dem Stapel kein Element hinzu, sondern ersetzt die aktuelle Matrix durch das Produkt der aktuellen Matrix und der angegebenen Matrix.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXMatrixStack](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
