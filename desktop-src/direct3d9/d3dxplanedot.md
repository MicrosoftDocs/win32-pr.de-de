---
description: Berechnet das Punktprodukt einer Ebene und eines 4D-Vektors.
ms.assetid: e6232ca8-52cc-472d-8bdb-4f8dfc520d4f
title: D3DXPlaneDot-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneDot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4895a94ad50171682a8bd5247694c3b35a56d174b5477f5bbb2a621c1e74fa96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564630"
---
# <a name="d3dxplanedot-function"></a>D3DXPlaneDot-Funktion

Berechnet das Punktprodukt einer Ebene und eines 4D-Vektors.

## <a name="syntax"></a>Syntax


```C++
FLOAT D3DXPlaneDot(
  _In_ const D3DXPLANE   *pP,
  _In_ const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pP* \[ In\]
</dt> <dd>

Typ: **const [**D3DXPLANE**](d3dxplane.md) \***

Zeiger auf eine [**D3DXPLANE-Quellstruktur.**](d3dxplane.md)

</dd> <dt>

*pV* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR4**](d3dxvector4.md) \***

Zeiger auf eine [**D3DXVECTOR4-Struktur.**](d3dxvector4.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Das Punktprodukt der Ebene und des 4D-Vektors.

## <a name="remarks"></a>Hinweise

Bei einer Ebene (a, b, c, d) und einem 4D-Vektor (x, y, z, w) ist der Rückgabewert dieser Funktion \* ein x + b \* y + c z + d \* \* w. Die **D3DXPlaneDot-Funktion** ist nützlich, um die Beziehung der Ebene mit einer homogenen Koordinate zu bestimmen. Diese Funktion kann beispielsweise verwendet werden, um zu bestimmen, ob sich eine bestimmte Koordinate auf einer bestimmten Ebene befindet oder auf welcher Seite einer bestimmten Ebene eine bestimmte Koordinate liegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXPlaneDotCoord**](d3dxplanedotcoord.md)
</dt> <dt>

[**D3DXPlaneDotNormal**](d3dxplanedotnormal.md)
</dt> </dl>

 

 
