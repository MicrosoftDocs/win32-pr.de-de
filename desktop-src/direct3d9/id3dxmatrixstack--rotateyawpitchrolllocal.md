---
description: Rotiert (relativ zum lokalen Koordinaten Bereich des Objekts) um eine beliebige Achse.
ms.assetid: c69f5ea7-5d14-4187-9405-1ceff8230185
title: 'ID3DXMATRIXStack:: rotateyawpitchrolllocal-Methode (D3dx9math. h)'
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
ms.openlocfilehash: cffacf4129a711dece35fd581f6cfc9bc12c2f99
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354327"
---
# <a name="id3dxmatrixstackrotateyawpitchrolllocal-method-d3dx9mathh"></a>ID3DXMATRIXStack:: rotateyawpitchrolllocal-Methode (D3dx9math. h)

Rotiert (relativ zum lokalen Koordinaten Bereich des Objekts) um eine beliebige Achse.

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

Nicht im  \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Die-Achse um die y-Achse im Bogenmaße.

</dd> <dt>

*Tonhöhe* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Die Tonhöhe um die x-Achse im Bogenmaße.

</dd> <dt>

*Rollout* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Der rollenum die z-Achse im Bogenmaße.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.

## <a name="remarks"></a>Bemerkungen

Diese Methode fügt die Drehung dem Matrix Stapel mit der berechneten Rotations Matrix hinzu, die der folgenden ähnelt:


```
D3DXMATRIX tmp;
D3DXMatrixRotationYawPitchRoll( &tmp, yaw, pitch, roll );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



Da die Drehung linksbündig mit dem Matrix Stapel multipliziert wird, ist die Drehung relativ zum lokalen Koordinaten Bereich des Objekts.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**D3DXMatrixRotationAxis**](d3dxmatrixrotationaxis.md)
</dt> <dt>

[**ID3DXMATRIXStack:: rotateaxis**](id3dxmatrixstack--rotateaxis.md)
</dt> <dt>

[**ID3DXMATRIXStack:: rotateaxislocal**](id3dxmatrixstack--rotateaxislocal.md)
</dt> <dt>

[**ID3DXMATRIXStack:: rotateyawpitchroll**](id3dxmatrixstack--rotateyawpitchroll.md)
</dt> </dl>

 

 
