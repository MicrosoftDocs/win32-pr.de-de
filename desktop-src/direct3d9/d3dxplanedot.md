---
description: Berechnet das Punktprodukt einer Ebene und einen 4D-Vektor.
ms.assetid: e6232ca8-52cc-472d-8bdb-4f8dfc520d4f
title: D3DXPlaneDot-Funktion (D3dx9math. h)
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
ms.openlocfilehash: b6f33e591df364151a7090e5b4a9dd0773f5788a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357217"
---
# <a name="d3dxplanedot-function"></a>D3DXPlaneDot-Funktion

Berechnet das Punktprodukt einer Ebene und einen 4D-Vektor.

## <a name="syntax"></a>Syntax


```C++
FLOAT D3DXPlaneDot(
  _In_ const D3DXPLANE   *pP,
  _In_ const D3DXVECTOR4 *pV
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

Typ: **Konstanten [**D3DXVECTOR4**](d3dxvector4.md) \***

Zeiger auf eine [**D3DXVECTOR4**](d3dxvector4.md) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **float**](../winprog/windows-data-types.md)**

Das Punktprodukt der Ebene und des 4D-Vektors.

## <a name="remarks"></a>Bemerkungen

Wenn eine Ebene (a, b, c, d) und ein 4D-Vektor (x, y, z, w) angegeben wird, ist der Rückgabewert dieser Funktion ein \* x + b \* y + c \* z + d \* w. Die **D3DXPlaneDot** -Funktion ist nützlich, um die Beziehung der Ebene mit einer homogenen Koordinate zu bestimmen. Diese Funktion kann z. b. verwendet werden, um zu bestimmen, ob sich eine bestimmte Koordinate auf einer bestimmten Ebene befindet oder auf welcher Seite einer bestimmten Ebene eine bestimmte Koordinate liegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXPlaneDotCoord**](d3dxplanedotcoord.md)
</dt> <dt>

[**D3DXPlaneDotNormal**](d3dxplanedotnormal.md)
</dt> </dl>

 

 
