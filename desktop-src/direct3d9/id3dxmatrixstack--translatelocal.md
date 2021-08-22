---
description: 'ID3DXMATRIXStack::TranslateLocal-Methode (D3dx9math.h): Bestimmt das Produkt der berechneten Übersetzungsmatrix, das durch die angegebenen Faktoren (x, y und z) und die aktuelle Matrix bestimmt wird.'
ms.assetid: d4752a6c-2114-4016-a69f-dcc561d2c76b
title: ID3DXMATRIXStack::TranslateLocal-Methode (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.TranslateLocal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 39984fa20ab0fa84d9b22b86fade2eb59277dd6a919c5bfa8d8a52efd33b1cee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493120"
---
# <a name="id3dxmatrixstacktranslatelocal-method-d3dx9mathh"></a>ID3DXMATRIXStack::TranslateLocal-Methode (D3dx9math.h)

Bestimmt das Produkt der berechneten Übersetzungsmatrix, das durch die angegebenen Faktoren (x, y und z) und die aktuelle Matrix bestimmt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT TranslateLocal(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*x* \[ in\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Der Übersetzungsfaktor in x-Richtung.

</dd> <dt>

*y* \[ in\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Der Übersetzungsfaktor in y-Richtung.

</dd> <dt>

*z* \[ in\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Der Übersetzungsfaktor in z-Richtung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK.

## <a name="remarks"></a>Hinweise

Diese Methode multipliziert die aktuelle Matrix links mit der berechneten Übersetzungsmatrix (die Transformation geht um den lokalen Ursprung des Objekts).


```
    
D3DXMATRIX tmp;
D3DXMatrixTranslation( &tmp, x, y, z );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack::Translate**](id3dxmatrixstack--translate.md)
</dt> </dl>

 

 
