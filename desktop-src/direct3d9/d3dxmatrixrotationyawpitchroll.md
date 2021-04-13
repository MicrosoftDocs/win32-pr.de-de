---
description: Erstellt eine Matrix mit einem angegebenen Yaw, einer angegebenen Tonhöhe und einem angegebenen Rollout.
ms.assetid: efaab508-34ed-4373-a8d0-3bc459d75f39
title: D3DXMatrixRotationYawPitchRoll-Funktion (D3dx9math. h)
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
ms.openlocfilehash: 2a8d6a531592ce49342dae0d0ecd6b3ace995bf5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219439"
---
# <a name="d3dxmatrixrotationyawpitchroll-function-d3dx9mathh"></a>D3DXMatrixRotationYawPitchRoll-Funktion (D3dx9math. h)

Erstellt eine Matrix mit einem angegebenen Yaw, einer angegebenen Tonhöhe und einem angegebenen Rollout.

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

*Pout* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Ein Zeiger auf die [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die das Ergebnis des Vorgangs ist.

</dd> <dt>

Nicht im  \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Um die y-Achse im Bogenmaße herum.

</dd> <dt>

*Tonhöhe* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Die Höhe um die x-Achse im Bogenmaße.

</dd> <dt>

*Rollout* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Führen Sie ein Rollback für die z-Achse im Bogenmaße durch.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur mit dem angegebenen "Yaw", "Pitch" und "Roll".

## <a name="remarks"></a>Bemerkungen

Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird. Auf diese Weise kann die **D3DXMatrixRotationYawPitchRoll** -Funktion als Parameter für eine andere Funktion verwendet werden.

Die Reihenfolge der Transformationen lautet zuerst "Roll First", dann "Pitch" und "Yaw". Relativ zur lokalen Koordinatenachse des Objekts entspricht dies der Drehung um die z-Achse, gefolgt von der Drehung um die x-Achse, gefolgt von der Drehung um die y-Achse, wie in der folgenden Abbildung dargestellt.

![Abbildung von "Roll", "Pitch" und "Yaw" als Drehung um die drei Achsen](images/pitchyawroll.png)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

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

 

 
