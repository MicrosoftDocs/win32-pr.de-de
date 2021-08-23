---
description: 'D3DXQuaternionToAxisAngle-Funktion (D3DX10Math.h): Berechnet die Achse und den Drehwinkel einer Quaternion.'
ms.assetid: 1e81b88b-071d-46f1-b640-c70d063a14d1
title: D3DXQuaternionToAxisAngle-Funktion (D3DX10Math.h)
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
ms.openlocfilehash: db53d399f269b48ae96558af6037b646ca19ce7de831897f672b3df4b7bbc7d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990990"
---
# <a name="d3dxquaterniontoaxisangle-function-d3dx10mathh"></a>D3DXQuaternionToAxisAngle-Funktion (D3DX10Math.h)

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

Typ: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***

Zeiger auf die Quelle [**D3DXQUATERNION**](d3d10-d3dxquaternion.md).

</dd> <dt>

*pAxis* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

Diese Funktion gibt einen Zeiger auf einen [**D3DXVECTOR3**](d3d10-d3dxvector3.md) zurück, der die Drehachse der Quaternion identifiziert.

</dd> <dt>

*pAngle* \[ in, out\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Diese Funktion gibt einen Zeiger auf einen FLOAT-Wert zurück, der den Drehwinkel der Quaternion im Bogenmaß identifiziert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Verwenden Sie [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) für alle Quaternioneingaben, die noch nicht normalisiert sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
