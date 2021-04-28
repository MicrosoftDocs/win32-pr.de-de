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
ms.openlocfilehash: 51f704aa839ff210b3c2de57767cb32ec609232f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108698"
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

## <a name="remarks"></a>Bemerkungen

Verwenden Sie [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) für alle Quaternioneingaben, die nicht bereits normalisiert sind.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
