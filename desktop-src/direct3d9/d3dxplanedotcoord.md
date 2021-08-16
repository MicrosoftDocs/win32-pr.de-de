---
description: Berechnet das Punktprodukt einer Ebene und eines 3D-Vektors. Der w-Parameter des Vektors wird als 1 angenommen.
ms.assetid: 634de6bc-b631-493d-a7a6-292a3c3253d6
title: D3DXPlaneDotCoord-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneDotCoord
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 30f04ec310ce66dc43073e724b08c358cd8fc6f24f0b3840475a1abc61544503
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524927"
---
# <a name="d3dxplanedotcoord-function"></a>D3DXPlaneDotCoord-Funktion

Berechnet das Punktprodukt einer Ebene und eines 3D-Vektors. Der w-Parameter des Vektors wird als 1 angenommen.

## <a name="syntax"></a>Syntax


```C++
FLOAT D3DXPlaneDotCoord(
  _In_ const D3DXPLANE   *pP,
  _In_ const D3DXVECTOR3 *pV
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

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Quellstruktur.**](d3dxvector3.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Das Punktprodukt der Ebene und des 3D-Vektors.

## <a name="remarks"></a>Hinweise

Bei einer Ebene (a, b, c, d) und einem 3D-Vektor (x, y, z) ist der Rückgabewert dieser Funktion \* ein x + b \* y + c z + d \* \* 1. Die **D3DXPlaneDotCoord-Funktion** ist nützlich, um die Beziehung der Ebene mit einer Koordinate im 3D-Raum zu bestimmen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXPlaneDot**](d3dxplanedot.md)
</dt> <dt>

[**D3DXPlaneDotNormal**](d3dxplanedotnormal.md)
</dt> </dl>

 

 
