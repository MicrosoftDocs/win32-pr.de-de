---
description: 'ID3DXMATRIXStack::TranslateLocal-Methode (D3DX10.h): Bestimmt das Produkt der berechneten Übersetzungsmatrix, die durch die angegebenen Faktoren (x, y und z) und die aktuelle Matrix bestimmt wird.'
ms.assetid: 96399801-dd80-4e9a-a5c3-c5d41eb9368a
title: ID3DXMATRIXStack::TranslateLocal-Methode (D3DX10.h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 80fabea58bd30b0db9b3ff41b522614007fe4b7d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107748"
---
# <a name="id3dxmatrixstacktranslatelocal-method-d3dx10h"></a>ID3DXMATRIXStack::TranslateLocal-Methode (D3DX10.h)

Bestimmt das Produkt der berechneten Übersetzungsmatrix, die durch die angegebenen Faktoren (x, y und z) und die aktuelle Matrix bestimmt wird.

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

Der Übersetzungsfaktor in der y-Richtung.

</dd> <dt>

*z* \[ in\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Der Übersetzungsfaktor in der Z-Richtung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK.

## <a name="remarks"></a>Bemerkungen

Diese Methode multipliziert die aktuelle Matrix mit der berechneten Übersetzungsmatrix (die Transformation bezieht sich auf den lokalen Ursprung des Objekts).


```
D3DXMATRIX tmp;
D3DXMatrixTranslation(&tmp, x, y, z );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



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

 

 
