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
ms.openlocfilehash: 4b777bd729810b6fd63bd71def9858203b2ac559
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107948"
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

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="remarks"></a>Bemerkungen

Diese Methode multipliziert die gegebene Matrix mit der aktuellen Matrix (die Transformation bezieht sich auf den lokalen Ursprung des Objekts).


```
m_pstack[m_currentPos] = (*pMat) * m_pstack[m_currentPos];
```



Diese Methode fügt dem Stapel kein Element hinzu, sondern ersetzt die aktuelle Matrix durch das Produkt der angegebenen Matrix und der aktuellen Matrix.

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

 

 
