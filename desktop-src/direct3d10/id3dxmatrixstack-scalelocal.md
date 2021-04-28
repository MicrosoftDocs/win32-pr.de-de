---
description: 'ID3DXMATRIXStack::ScaleLocal-Methode (D3DX10.h): Skaliert die aktuelle Matrix über den Objekt ursprung.'
ms.assetid: 748fce3a-a33c-4975-bbf0-dd3167a036f1
title: ID3DXMATRIXStack::ScaleLocal-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.ScaleLocal
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3961db0794703e3974dbd92d8eae8293173c2354
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107778"
---
# <a name="id3dxmatrixstackscalelocal-method-d3dx10h"></a>ID3DXMATRIXStack::ScaleLocal-Methode (D3DX10.h)

Skalieren Sie die aktuelle Matrix über den Objekt-Ursprung.

## <a name="syntax"></a>Syntax


```C++
HRESULT ScaleLocal(
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

Die Skalierungskomponente in x-Richtung.

</dd> <dt>

*y* \[ in\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Die Skalierungskomponente in y-Richtung.

</dd> <dt>

*z* \[ in\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Die Skalierungskomponente in Z-Richtung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK.

## <a name="remarks"></a>Bemerkungen

Diese Methode multipliziert die aktuelle Matrix mit der berechneten Skalierungsmatrix. Bei der Transformation geht es um den lokalen Ursprung des Objekts.


```
D3DXMATRIX tmp;
D3DXMatrixScaling(&tmp, x, y, z);
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

 

 
