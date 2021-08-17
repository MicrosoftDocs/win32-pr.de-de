---
description: 'ID3DXMATRIXStack::Translate-Methode (D3dx9math.h): Bestimmt das Produkt der aktuellen Matrix und der berechneten Übersetzungsmatrix, die durch die angegebenen Faktoren (x, y und z) bestimmt wird.'
ms.assetid: e0ac72a2-9970-433e-9026-aa79edc8261c
title: ID3DXMATRIXStack::Translate-Methode (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Translate
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6f51ed86569d29488f93a661999821c3f27bd5f17ed9ba2e552a2604f804c305
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987220"
---
# <a name="id3dxmatrixstacktranslate-method-d3dx9mathh"></a>ID3DXMATRIXStack::Translate-Methode (D3dx9math.h)

Bestimmt das Produkt der aktuellen Matrix und der berechneten Übersetzungsmatrix, die durch die angegebenen Faktoren (x, y und z) bestimmt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT Translate(
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

Mit dieser Methode wird die aktuelle Matrix mit der berechneten Übersetzungsmatrix rechts multipliziert (bei der Transformation geht es um den aktuellen Ursprung der Welt).


```
D3DXMATRIX tmp;
D3DXMatrixTranslation( &tmp, x, y, z );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack::TranslateLocal**](id3dxmatrixstack--translatelocal.md)
</dt> </dl>

 

 
