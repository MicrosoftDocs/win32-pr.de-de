---
description: Bestimmt, ob ein Strahl das Volume des Begrenzungs Rahmens einer Kugel schneidet.
ms.assetid: 5984a1a6-d36c-4a05-8c74-0ece7443356c
title: D3DXSphereBoundProbe-Funktion (D3DX10math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 09116e13582bbb75bc15ed04360ce02c4983f986
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762234"
---
# <a name="d3dxsphereboundprobe-function-d3dx10mathh"></a>D3DXSphereBoundProbe-Funktion (D3DX10math. h)

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

Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3**](d3d10-d3dxvector3.md) -Struktur, die die Mittelpunkt Koordinate der Kugel angibt.

</dd> <dt>

*RADIUS* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Der Radius der Kugel.

</dd> <dt>

" *prayposition* \[ " in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3**](d3d10-d3dxvector3.md) -Struktur, die die Ursprungs Koordinate des Strahls angibt.

</dd> <dt>

" *praydirection* \[ " in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3**](d3d10-d3dxvector3.md) -Struktur, die die Richtung des Strahls angibt. Dieser Vektor sollte nicht (0, 0, 0) sein, muss jedoch nicht normalisiert werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **bool**](../winprog/windows-data-types.md)**

Gibt **true** zurück, wenn der Strahl das Volume des umgebenden Felds der Kugel schneidet. Andernfalls wird **false** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

**D3DXSphereBoundProbe** bestimmt, ob der Strahl das Volume des umgebenden Felds der Kugel schneidet, nicht nur die Oberfläche der Kugel.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mesh-Funktionen](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
