---
description: Bestimmt das Produkt der aktuellen Matrix und die berechnete Übersetzungs Matrix, die durch die angegebenen Faktoren (x, y und z) bestimmt wird.
ms.assetid: d6e347a5-bb66-451d-b66e-49ea8eff70b3
title: 'ID3DXMATRIXStack:: Translation-Methode (d3dx10. h)'
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 159e1dc6b3dabeb92b32798cbe318f6c72c01d70
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367401"
---
# <a name="id3dxmatrixstacktranslate-method-d3dx10h"></a>ID3DXMATRIXStack:: Translation-Methode (d3dx10. h)

Bestimmt das Produkt der aktuellen Matrix und die berechnete Übersetzungs Matrix, die durch die angegebenen Faktoren (x, y und z) bestimmt wird.

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

Typ: **[ **float**](../winprog/windows-data-types.md)**

Der Übersetzungs Faktor in der x-Richtung.

</dd> <dt>

*j* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Der Übersetzungs Faktor in y-Richtung.

</dd> <dt>

*z* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Der Übersetzungs Faktor in der z-Richtung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.

## <a name="remarks"></a>Bemerkungen

Mit dieser Methode wird die aktuelle Matrix mit der berechneten Übersetzungs Matrix nach rechts multipliziert (die Transformation geht um den aktuellen Ursprung der Welt).


```
D3DXMATRIX tmp;
D3DXMatrixTranslation( &tmp, x, y, z );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



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

 

 
