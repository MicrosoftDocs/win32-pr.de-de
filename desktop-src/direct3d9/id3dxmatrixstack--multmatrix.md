---
description: Bestimmt das Produkt der aktuellen Matrix und der angegebenen Matrix.
ms.assetid: a673ce82-6fed-4a3f-8c37-d0db11195f06
title: 'ID3DXMATRIXStack:: mehrtmatrix-Methode (D3dx9math. h)'
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
ms.openlocfilehash: fc9b3fb49387e354645c8a3c09c7572b4da80109
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361848"
---
# <a name="id3dxmatrixstackmultmatrix-method-d3dx9mathh"></a>ID3DXMATRIXStack:: mehrtmatrix-Methode (D3dx9math. h)

Bestimmt das Produkt der aktuellen Matrix und der angegebenen Matrix.

## <a name="syntax"></a>Syntax


```C++
HRESULT MultMatrix(
  [in] const D3DXMATRIX *pMat
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmat* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***

Ein Zeiger auf die [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die mit der aktuellen Matrix multipliziert werden soll.

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
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack:: mehrtmatrixlocal**](id3dxmatrixstack--multmatrixlocal.md)
</dt> </dl>

 

 




