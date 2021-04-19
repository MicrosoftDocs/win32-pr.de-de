---
description: Gibt die z-Komponente zurück, indem das Kreuz Produkt zweier 2D-Vektoren übernommen wird.
ms.assetid: daec19f2-cd0f-4a68-affc-9a42bda8912c
title: D3DXVec2CCW-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2CCW
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 71c6e14171a9e7d12d86c30f05885cecf50ce973
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355180"
---
# <a name="d3dxvec2ccw-function"></a>D3DXVec2CCW-Funktion

Gibt die z-Komponente zurück, indem das Kreuz Produkt zweier 2D-Vektoren übernommen wird.

## <a name="syntax"></a>Syntax


```C++
FLOAT D3DXVec2CCW(
  _In_ const D3DXVECTOR2 *pV1,
  _In_ const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pV1* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR2**](d3dxvector2.md) \***

Zeiger auf eine Quell- [**D3DXVECTOR2**](d3dxvector2.md) -Struktur.

</dd> <dt>

*pV2* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR2**](d3dxvector2.md) \***

Zeiger auf eine Quell- [**D3DXVECTOR2**](d3dxvector2.md) -Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **float**](../winprog/windows-data-types.md)**

Die z-Komponente.

## <a name="remarks"></a>Bemerkungen

Diese Funktion bestimmt die z-Komponente, indem Sie das Kreuz Produkt anhand der folgenden Formel bestimmt: ((x1, Y1, 0) Cross (x2, Y2, 0)). Oder wie im folgenden Beispiel gezeigt.


```
pV1->x * pV2->y - pV1->y * pV2->x
```



Wenn der Wert der z-Komponente positiv ist, wird der Vektor V2 gegen den Uhrzeigersinn vom Vektor v1 gegen den Uhrzeigersinn. Diese Informationen sind nützlich für die gegenseitige Erkennung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXVec2Dot**](d3dxvec2dot.md)
</dt> </dl>

 

 
