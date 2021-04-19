---
description: Bestimmt, ob ein Strahl das Volume des Begrenzungs Rahmens einer Kugel schneidet.
ms.assetid: fa2e9ecf-7905-4a62-ba48-774bd522525a
title: D3DXSphereBoundProbe-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSphereBoundProbe
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bbab8a49165a87f73037ae25230d67b02222fc15
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363133"
---
# <a name="d3dxsphereboundprobe-function-d3dx9meshh"></a>D3DXSphereBoundProbe-Funktion (D3DX9Mesh. h)

Bestimmt, ob ein Strahl das Volume des Begrenzungs Rahmens einer Kugel schneidet.

## <a name="syntax"></a>Syntax


```C++
BOOL D3DXSphereBoundProbe(
  _In_ const D3DXVECTOR3 *pCenter,
  _In_       FLOAT       Radius,
  _In_ const D3DXVECTOR3 *pRayPosition,
  _In_ const D3DXVECTOR3 *pRayDirection
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcenter* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die die Mittelpunkt Koordinate der Kugel angibt.

</dd> <dt>

*RADIUS* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Der Radius der Kugel.

</dd> <dt>

" *prayposition* \[ " in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die die Ursprungs Koordinate des Strahls angibt.

</dd> <dt>

" *praydirection* \[ " in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3**](d3dxvector3.md) -Struktur, die die Richtung des Strahls angibt. Dieser Vektor sollte nicht (0, 0, 0) sein, muss jedoch nicht normalisiert werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **bool**](../winprog/windows-data-types.md)**

Gibt **true** zurück, wenn der Strahl das Volume des umgebenden Felds der Kugel schneidet. Andernfalls wird **false** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

**D3DXSphereBoundProbe** bestimmt, ob der Strahl das Volume des umgebenden Felds der Kugel schneidet, nicht nur die Oberfläche der Kugel.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
