---
description: 'D3DXMatrixRotationYawPitchRoll-Funktion (D3dx9math.h): Erstellt eine Matrix mit einem angegebenen Yaw, Pitch und Roll.'
ms.assetid: efaab508-34ed-4373-a8d0-3bc459d75f39
title: D3DXMatrixRotationYawPitchRoll-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationYawPitchRoll
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 789812b6e94efd40ff71209348f0c9727088c253
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118148"
---
# <a name="d3dxmatrixrotationyawpitchroll-function-d3dx9mathh"></a>D3DXMatrixRotationYawPitchRoll-Funktion (D3dx9math.h)

Erstellt eine Matrix mit einem angegebenen Yaw, einer angegebenen Tonhöhe und einem angegebenen Roll.

## <a name="syntax"></a>Syntax


```C++
D3DXMATRIX* D3DXMatrixRotationYawPitchRoll(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Yaw,
  _In_    FLOAT      Pitch,
  _In_    FLOAT      Roll
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Zeiger auf die [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die das Ergebnis des Vorgangs ist.

</dd> <dt>

*Yaw* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Gieren Sie um die y-Achse im Bogenmaß.

</dd> <dt>

*Pitch* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Tonhöhe um die X-Achse im Bogenmaß.

</dd> <dt>

*Roll* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Rollieren Sie um die Z-Achse im Bogenmaß.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Zeiger auf eine [**D3DXMATRIX-Struktur**](d3dxmatrix.md) mit dem angegebenen Yaw, Pitch und Roll.

## <a name="remarks"></a>Bemerkungen

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter zurückgegeben* wird. Auf diese Weise kann die **D3DXMatrixRotationYawPitchRoll-Funktion** als Parameter für eine andere Funktion verwendet werden.

Die Reihenfolge der Transformationen ist zuerst roll, dann pitch und yaw. Relativ zur lokalen Koordinatenachse des Objekts entspricht dies der Drehung um die Z-Achse, gefolgt von der Drehung um die x-Achse und der Drehung um die y-Achse, wie in der folgenden Abbildung dargestellt.

![Abbildung von Roll, Pitch und YAW als Drehungen um die drei Achsen](images/pitchyawroll.png)

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixRotationAxis**](d3dxmatrixrotationaxis.md)
</dt> <dt>

[**D3DXMatrixRotationQuaternion**](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[**D3DXMatrixRotationX**](d3dxmatrixrotationx.md)
</dt> <dt>

[**D3DXMatrixRotationY**](d3dxmatrixrotationy.md)
</dt> <dt>

[**D3DXMatrixRotationZ**](d3dxmatrixrotationz.md)
</dt> </dl>

 

 
