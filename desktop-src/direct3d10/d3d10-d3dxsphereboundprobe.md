---
description: 'D3DXSphereBoundProbe-Funktion (D3DX10math.h): Bestimmt, ob ein Strahl das Volumen des Begrenzungsfelds einer Kugel schneidet.'
ms.assetid: 5984a1a6-d36c-4a05-8c74-0ece7443356c
title: D3DXSphereBoundProbe-Funktion (D3DX10math.h)
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
ms.openlocfilehash: 39e2b3871365cddd70b942f6d9d9f0fc9af85eca23944f388e3afd6ad9b4fc63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989960"
---
# <a name="d3dxsphereboundprobe-function-d3dx10mathh"></a>D3DXSphereBoundProbe-Funktion (D3DX10math.h)

Bestimmt, ob ein Strahl das Volumen des Begrenzungsfelds einer Kugel schneidet.

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

*pCenter* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Struktur**](d3d10-d3dxvector3.md) unter Angabe der Mittelpunktkoordinate der Kugel.

</dd> <dt>

*Radius* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Radius der Kugel.

</dd> <dt>

*pRayPosition* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Struktur**](d3d10-d3dxvector3.md) unter Angabe der Ursprungskoordinate des Strahls.

</dd> <dt>

*pRayDirection* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Struktur**](d3d10-d3dxvector3.md) unter Angabe der Richtung des Strahls. Dieser Vektor sollte nicht (0,0,0) sein, muss aber nicht normalisiert werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

Gibt **TRUE zurück,** wenn der Strahl das Volumen des Begrenzungsfelds der Kugel schneidet. Andernfalls wird **FALSE zurückgegeben.**

## <a name="remarks"></a>Hinweise

**D3DXSphereBoundProbe** bestimmt, ob der Strahl das Volumen des Begrenzungsfelds der Kugel überschneidet, nicht nur die Oberfläche der Kugel.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mesh-Funktionen](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
