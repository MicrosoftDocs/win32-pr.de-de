---
description: Bestimmt das Produkt der aktuellen Matrix und der angegebenen Matrix.
ms.assetid: 72388919-e474-4433-b219-41e2d312848e
title: 'ID3DXMATRIXStack:: mehrtmatrix-Methode (d3dx10. h)'
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
ms.openlocfilehash: 43f80ca26f615e02570f0855b1ba6c2435e11b5b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106360241"
---
# <a name="id3dxmatrixstackmultmatrix-method-d3dx10h"></a>ID3DXMATRIXStack:: mehrtmatrix-Methode (d3dx10. h)

Bestimmt das Produkt der aktuellen Matrix und der angegebenen Matrix.

## <a name="syntax"></a>Syntax


```C++
HRESULT MultMatrix(
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

Diese Methode multipliziert die angegebene Matrix nach rechts mit der aktuellen Matrix (die Transformation geht zum aktuellen Ursprung der Welt).


```
m_pstack[m_currentPos] = m_pstack[m_currentPos] * (*pMat);
```



Diese Methode fügt dem Stapel kein Element hinzu, sondern ersetzt die aktuelle Matrix durch das Produkt der aktuellen Matrix und der angegebenen Matrix.

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

 

 
