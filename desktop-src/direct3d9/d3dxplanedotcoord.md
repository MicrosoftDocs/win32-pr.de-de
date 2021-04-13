---
description: Berechnet das Punktprodukt einer Ebene und einen 3D-Vektor. Der w-Parameter des Vektors wird als 1 angenommen.
ms.assetid: 634de6bc-b631-493d-a7a6-292a3c3253d6
title: D3DXPlaneDotCoord-Funktion (D3dx9math. h)
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
ms.openlocfilehash: 99ee9db7df541dcf74867b828a73ede80f11e22b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219434"
---
# <a name="d3dxplanedotcoord-function"></a>D3DXPlaneDotCoord-Funktion

Berechnet das Punktprodukt einer Ebene und einen 3D-Vektor. Der w-Parameter des Vektors wird als 1 angenommen.

## <a name="syntax"></a>Syntax


```C++
FLOAT D3DXPlaneDotCoord(
  _In_ const D3DXPLANE   *pP,
  _In_ const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PP* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXPLANE**](d3dxplane.md) \***

Zeiger auf eine Quell- [**D3DXPLANE**](d3dxplane.md) -Struktur.

</dd> <dt>

*PV* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine Quell- [**D3DXVECTOR3**](d3dxvector3.md) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **float**](../winprog/windows-data-types.md)**

Das Punktprodukt der Ebene und des 3D-Vektors.

## <a name="remarks"></a>Bemerkungen

Bei einer Ebene (a, b, c, d) und einem 3D-Vektor (x, y, z) ist der Rückgabewert dieser Funktion ein \* x + b \* y + c \* z + d \* 1. Die **D3DXPlaneDotCoord** -Funktion ist nützlich, um die Beziehung der Ebene mit einer Koordinate im 3D-Raum zu bestimmen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXPlaneDot**](d3dxplanedot.md)
</dt> <dt>

[**D3DXPlaneDotNormal**](d3dxplanedotnormal.md)
</dt> </dl>

 

 
