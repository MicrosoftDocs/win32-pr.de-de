---
description: 'D3DXQuaternionRotationYawPitchRoll-Funktion (D3dx9math.h): Erstellt eine Quaternion mit dem angegebenen Yaw, Pitch und Roll.'
ms.assetid: be4a3bd5-114b-4652-8e0a-e51338317c16
title: D3DXQuaternionRotationYawPitchRoll-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationYawPitchRoll
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 954fee40015b558b10ba83ef12b1555d06896413c6396ca12ed6e4374131caeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988432"
---
# <a name="d3dxquaternionrotationyawpitchroll-function-d3dx9mathh"></a>D3DXQuaternionRotationYawPitchRoll-Funktion (D3dx9math.h)

Erstellt eine Quaternion mit dem angegebenen Yaw, Pitch und Roll.

## <a name="syntax"></a>Syntax


```C++
D3DXQUATERNION* D3DXQuaternionRotationYawPitchRoll(
  _Inout_ D3DXQUATERNION *pOut,
  _In_    FLOAT          Yaw,
  _In_    FLOAT          Pitch,
  _In_    FLOAT          Roll
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Zeiger auf die [**D3DXQUATERNION-Struktur,**](d3dxquaternion.md) die das Ergebnis des Vorgangs ist.

</dd> <dt>

*Yaw* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Yaw um die y-Achse im Bogenmaß.

</dd> <dt>

*Tonhöhe* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Tonhöhe um die x-Achse im Bogenmaß.

</dd> <dt>

*Roll* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Rolling um die Z-Achse im Bogenmaß.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Zeiger auf eine [**D3DXQUATERNION-Struktur**](d3dxquaternion.md) mit dem angegebenen Yaw, Pitch und Roll.

## <a name="remarks"></a>Hinweise

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter* zurückgegeben wird. Auf diese Weise kann die **D3DXQuaternionRotationYawPitchRoll-Funktion** als Parameter für eine andere Funktion verwendet werden.

Verwenden Sie [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) für alle Quaternioneingaben, die noch nicht normalisiert sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXQuaternionRotationAxis**](d3dxquaternionrotationaxis.md)
</dt> <dt>

[**D3DXQuaternionRotationMatrix**](d3dxquaternionrotationmatrix.md)
</dt> </dl>

 

 
