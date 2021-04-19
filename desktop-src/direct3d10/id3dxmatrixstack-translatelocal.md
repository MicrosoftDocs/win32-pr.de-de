---
description: Bestimmt das Produkt der berechneten Übersetzungs Matrix, die durch die angegebenen Faktoren (x, y und z) und die aktuelle Matrix bestimmt wird.
ms.assetid: 96399801-dd80-4e9a-a5c3-c5d41eb9368a
title: 'ID3DXMATRIXStack:: translatelocal-Methode (d3dx10. h)'
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
ms.openlocfilehash: 65a627141f552107d88c3f43988daa0d316a0bef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367400"
---
# <a name="id3dxmatrixstacktranslatelocal-method-d3dx10h"></a>ID3DXMATRIXStack:: translatelocal-Methode (d3dx10. h)

Bestimmt das Produkt der berechneten Übersetzungs Matrix, die durch die angegebenen Faktoren (x, y und z) und die aktuelle Matrix bestimmt wird.

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

Mit dieser Methode wird die aktuelle Matrix mit der berechneten Übersetzungs Matrix Links multipliziert (die Transformation ist der lokale Ursprung des Objekts).


```
D3DXMATRIX tmp;
D3DXMatrixTranslation(&tmp, x, y, z );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
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

 

 
