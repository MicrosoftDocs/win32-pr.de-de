---
description: 'D3DXQuaternionToAxisAngle-Funktion (D3dx9math.h): Berechnet die Achse und den Drehwinkel einer Quaternion.'
ms.assetid: 6efd0a68-7641-403e-8ae2-c715b705b36e
title: D3DXQuaternionToAxisAngle-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionToAxisAngle
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8613a9d14c5e33b0f9f4e719a02ac9a6d70d1119
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117978"
---
# <a name="d3dxquaterniontoaxisangle-function-d3dx9mathh"></a>D3DXQuaternionToAxisAngle-Funktion (D3dx9math.h)

Berechnet die Achse und den Drehwinkel einer Quaternion.

## <a name="syntax"></a>Syntax


```C++
void D3DXQuaternionToAxisAngle(
  _In_    const D3DXQUATERNION *pQ,
  _Inout_       D3DXVECTOR3    *pAxis,
  _Inout_       FLOAT          *pAngle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pQ* \[ In\]
</dt> <dd>

Typ: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***

Zeiger auf die [**D3DXQUATERNION-Quellstruktur.**](d3dxquaternion.md)

</dd> <dt>

*pAxis* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Diese Funktion gibt einen Zeiger auf eine [**D3DXVECTOR3-Struktur**](d3dxvector3.md) zurück, die die Drehachse der Quaternion identifiziert.

</dd> <dt>

*pAngle* \[ in, out\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Diese Funktion gibt einen Zeiger auf einen FLOAT-Wert zurück, der den Drehwinkel der Quaternion im Bogenmaß identifiziert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) für alle Quaternioneingaben, die nicht bereits normalisiert sind.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
