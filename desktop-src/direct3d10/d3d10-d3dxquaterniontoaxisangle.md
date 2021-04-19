---
description: Berechnet die Achse und den Drehwinkel einer Quaternion.
ms.assetid: 1e81b88b-071d-46f1-b640-c70d063a14d1
title: D3DXQuaternionToAxisAngle-Funktion (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0fabba670bbfe83a3032e5a6fa78f5db16c89b3c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370449"
---
# <a name="d3dxquaterniontoaxisangle-function-d3dx10mathh"></a>D3DXQuaternionToAxisAngle-Funktion (D3DX10Math. h)

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

*PQ* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Zeiger auf den Quell- [**D3DXQUATERNION**](d3d10-d3dxquaternion.md).

</dd> <dt>

ein-.  \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Diese Funktion gibt einen Zeiger auf einen [**D3DXVECTOR3**](d3d10-d3dxvector3.md) -Wert zurück, der die Achse der Drehung der Quaternion identifiziert.

</dd> <dt>

*Schwenken* \[ in, out\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)\***

Diese Funktion gibt einen Zeiger auf einen float-Wert zurück, der den Drehwinkel der Quaternion im Bogenmaße identifiziert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) für eine beliebige Quaternion-Eingabe, die nicht bereits normalisiert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
