---
description: ID3DXMATRIXStack::RotateYawPitchRollLocal-Methode (D3DX10.h) – Rotiert (relativ zum lokalen Koordinatenraum des Objekts) um eine beliebige Achse.
ms.assetid: da023816-5176-460d-ab6b-909b89cc46cd
title: ID3DXMATRIXStack::RotateYawPitchRollLocal-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.RotateYawPitchRollLocal
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 726a6d7092b95f53d17625f68884b92d347de3a6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107838"
---
# <a name="id3dxmatrixstackrotateyawpitchrolllocal-method-d3dx10h"></a>ID3DXMATRIXStack::RotateYawPitchRollLocal-Methode (D3DX10.h)

Dreht (relativ zum lokalen Koordinatenraum des Objekts) um eine beliebige Achse.

## <a name="syntax"></a>Syntax


```C++
HRESULT RotateYawPitchRollLocal(
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

Das Gieren um die y-Achse im Bogenmaß.

</dd> <dt>

*Pitch* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Die Tonhöhe um die X-Achse im Bogenmaß.

</dd> <dt>

*Roll* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Der Roll um die Z-Achse im Bogenmaß.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK.

## <a name="remarks"></a>Bemerkungen

Diese Methode fügt die Drehung dem Matrixstapel mit der berechneten Rotationsmatrix ähnlich der folgenden hinzu:


```
D3DXMATRIX tmp;
D3DXMatrixRotationYawPitchRoll( &tmp, yaw, pitch, roll );
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

 

 
