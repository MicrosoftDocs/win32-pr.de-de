---
description: 'D3DXSphereBoundProbe-Funktion (D3DX9Mesh.h): Bestimmt, ob ein Strahl das Volumen des Begrenzungsfelds einer Kugel schneidet.'
ms.assetid: fa2e9ecf-7905-4a62-ba48-774bd522525a
title: D3DXSphereBoundProbe-Funktion (D3DX9Mesh.h)
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
ms.openlocfilehash: 85dbd46233176d65e7e7abbf0eb266c81868ceba7e67e3257bf902d1775d6a90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117731153"
---
# <a name="d3dxsphereboundprobe-function-d3dx9meshh"></a>D3DXSphereBoundProbe-Funktion (D3DX9Mesh.h)

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

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Struktur**](d3dxvector3.md) unter Angabe der Mittelpunktkoordinate der Kugel.

</dd> <dt>

*Radius* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Radius der Kugel.

</dd> <dt>

*pRayPosition* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Struktur**](d3dxvector3.md) unter Angabe der Ursprungskoordinate des Strahls.

</dd> <dt>

*pRayDirection* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Struktur**](d3dxvector3.md) unter Angabe der Richtung des Strahls. Dieser Vektor sollte nicht (0,0,0) sein, muss aber nicht normalisiert werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

Gibt **TRUE zurück,** wenn der Strahl das Volumen des Begrenzungsfelds der Kugel schneidet. Andernfalls wird **FALSE zurückgegeben.**

## <a name="remarks"></a>Hinweise

**D3DXSphereBoundProbe** bestimmt, ob der Strahl das Volumen des Begrenzungsfelds der Kugel überschneidet, nicht nur die Oberfläche der Kugel.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
