---
description: Bestimmt das Produkt der angegebenen Matrix und der aktuellen Matrix.
ms.assetid: 4d374a7b-99e0-4313-970d-b0e7cf3e97ce
title: 'ID3DXMATRIXStack:: multmatrixlocal-Methode (d3dx10. h)'
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
ms.openlocfilehash: 095882c98169159beaca0ef6c98d13fe03b9aed2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219705"
---
# <a name="id3dxmatrixstackmultmatrixlocal-method-d3dx10h"></a>ID3DXMATRIXStack:: multmatrixlocal-Methode (d3dx10. h)

Bestimmt das Produkt der angegebenen Matrix und der aktuellen Matrix.

## <a name="syntax"></a>Syntax


```C++
HRESULT MultMatrixLocal(
  [in] const D3DXMATRIX *pM
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pm* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***

Ein Zeiger auf die D3DXMATRIX-Struktur, die mit der aktuellen Matrix multipliziert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.

## <a name="remarks"></a>Bemerkungen

Diese Methode multipliziert die angegebene Matrix Links mit der aktuellen Matrix (die Transformation ist der lokale Ursprung des Objekts).


```
m_pstack[m_currentPos] = (*pMat) * m_pstack[m_currentPos];
```



Diese Methode fügt dem Stapel kein Element hinzu, sondern ersetzt die aktuelle Matrix durch das Produkt der angegebenen Matrix und der aktuellen Matrix.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx10. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXMatrixStack](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
