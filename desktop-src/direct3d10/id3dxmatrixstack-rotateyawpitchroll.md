---
description: 'ID3DXMATRIXStack::RotateYawPitchRoll-Methode (D3DX10.h): Rotiert (relativ zum Weltkoordinatenraum) um eine beliebige Achse.'
ms.assetid: 35e237f6-40f2-4001-adb0-f489d61f64e7
title: ID3DXMATRIXStack::RotateYawPitchRoll-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateYawPitchRoll
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8c4f167f769a1ed46404028916477d6784e4a436
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107828"
---
# <a name="id3dxmatrixstackrotateyawpitchroll-method-d3dx10h"></a>ID3DXMATRIXStack::RotateYawPitchRoll-Methode (D3DX10.h)

Rotiert (relativ zum Weltkoordinatenraum) um eine beliebige Achse.

## <a name="syntax"></a>Syntax


```C++
HRESULT RotateYawPitchRoll(
  [in] FLOAT Yaw,
  [in] FLOAT Pitch,
  [in] FLOAT Roll
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Yaw* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Das Gähnen um die y-Achse im Bogenmaß.

</dd> <dt>

*Tonhöhe* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Die Tonhöhe um die x-Achse im Bogenmaß.

</dd> <dt>

*Roll* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Das Rollback um die Z-Achse im Bogenmaß.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK.

## <a name="remarks"></a>Bemerkungen

Diese Methode fügt die Drehung dem Matrixstapel mit der berechneten Drehungsmatrix ähnlich der folgenden hinzu:


```
D3DXMATRIX tmp;
D3DXMatrixRotationYawPitchRoll( &tmp, yaw, pitch, roll );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



Da die Drehung mit dem Matrixstapel rechts multipliziert wird, ist die Drehung relativ zum Weltkoordinatenraum.

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

 

 
