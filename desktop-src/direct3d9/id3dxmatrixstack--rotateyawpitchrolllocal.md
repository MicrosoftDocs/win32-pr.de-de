---
description: ID3DXMATRIXStack::RotateYawPitchRollLocal-Methode (D3dx9math.h) – Rotiert (relativ zum lokalen Koordinatenraum des Objekts) um eine beliebige Achse.
ms.assetid: c69f5ea7-5d14-4187-9405-1ceff8230185
title: ID3DXMATRIXStack::RotateYawPitchRollLocal-Methode (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3cd1355039a570f0ef0e3546150cb9d8ebed5900b88ba14b6640f3d8a1799150
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493189"
---
# <a name="id3dxmatrixstackrotateyawpitchrolllocal-method-d3dx9mathh"></a>ID3DXMATRIXStack::RotateYawPitchRollLocal-Methode (D3dx9math.h)

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

## <a name="remarks"></a>Hinweise

Diese Methode fügt die Drehung dem Matrixstapel mit der berechneten Rotationsmatrix ähnlich der folgenden hinzu:


```
D3DXMATRIX tmp;
D3DXMatrixRotationYawPitchRoll( &tmp, yaw, pitch, roll );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



Da die Drehung links multipliziert mit dem Matrixstapel ist, ist die Drehung relativ zum lokalen Koordinatenraum des Objekts.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**D3DXMatrixRotationAxis**](d3dxmatrixrotationaxis.md)
</dt> <dt>

[**ID3DXMATRIXStack::RotateAxis**](id3dxmatrixstack--rotateaxis.md)
</dt> <dt>

[**ID3DXMATRIXStack::RotateAxisLocal**](id3dxmatrixstack--rotateaxislocal.md)
</dt> <dt>

[**ID3DXMATRIXStack::RotateYawPitchRoll**](id3dxmatrixstack--rotateyawpitchroll.md)
</dt> </dl>

 

 
