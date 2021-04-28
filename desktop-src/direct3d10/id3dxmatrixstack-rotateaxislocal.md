---
description: 'ID3DXMATRIXStack::RotateAxisLocal-Methode (D3DX10.h): Rotiert (relativ zum lokalen Koordinatenraum des Objekts) um eine beliebige Achse.'
ms.assetid: 90837762-9bfe-4065-94b3-1ca61184a78e
title: ID3DXMATRIXStack::RotateAxisLocal-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateAxisLocal
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8a81a4c4bd9a2f738274f98ce925799b34986fbb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107878"
---
# <a name="id3dxmatrixstackrotateaxislocal-method-d3dx10h"></a>ID3DXMATRIXStack::RotateAxisLocal-Methode (D3DX10.h)

Dreht (relativ zum lokalen Koordinatenraum des Objekts) um eine beliebige Achse.

## <a name="syntax"></a>Syntax


```C++
HRESULT RotateAxisLocal(
  [in] const D3DXVECTOR3 *pV,
  [in]       FLOAT       Angle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pV* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Zeiger auf die beliebige Drehachse. Siehe [**D3DXVECTOR3**](d3d10-d3dxvector3.md).

</dd> <dt>

*Winkel* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Drehwinkel um die beliebige Achse im Bogenmaß. Winkel werden gegen den Uhrzeigersinn gemessen, wenn entlang der beliebigen Achse zum Ursprung gesucht wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="remarks"></a>Bemerkungen

Diese Methode fügt die Drehung dem Matrixstapel mit der berechneten Rotationsmatrix ähnlich der folgenden hinzu:


```
D3DXMATRIX tmp;
D3DXMatrixRotationAxis( &tmp, pV, angle );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



Da die Drehung links multipliziert mit dem Matrixstapel ist, ist die Drehung relativ zum lokalen Koordinatenraum des Objekts.

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

 

 
