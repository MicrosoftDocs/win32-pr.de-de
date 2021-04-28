---
description: ID3DXMATRIXStack::RotateYawPitchRoll-Methode (D3dx9math.h) – Rotiert (relativ zum Weltkoordinatenraum) um eine beliebige Achse.
ms.assetid: 25a7eff4-a575-4ddb-85eb-ef3fa2d6ae3b
title: ID3DXMATRIXStack::RotateYawPitchRoll-Methode (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8bb516e759e781ca3784e49253eeaddac68075bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107378"
---
# <a name="id3dxmatrixstackrotateyawpitchroll-method-d3dx9mathh"></a>ID3DXMATRIXStack::RotateYawPitchRoll-Methode (D3dx9math.h)

Dreht (relativ zum Weltkoordinatenraum) um eine beliebige Achse.

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
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



Da die Drehung rechts multipliziert mit dem Matrixstapel ist, ist die Drehung relativ zum Weltkoordinatenraum.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**D3DXMatrixRotationAxis**](d3dxmatrixrotationaxis.md)
</dt> <dt>

[**ID3DXMATRIXStack::RotateAxis**](id3dxmatrixstack--rotateaxis.md)
</dt> <dt>

[**ID3DXMATRIXStack::RotateAxisLocal**](id3dxmatrixstack--rotateaxislocal.md)
</dt> <dt>

[**ID3DXMATRIXStack::RotateYawPitchRollLocal**](id3dxmatrixstack--rotateyawpitchrolllocal.md)
</dt> </dl>

 

 
