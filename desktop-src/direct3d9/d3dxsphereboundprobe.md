---
description: 'D3DXSphereBoundProbe-Funktion (D3DX9Mesh.h): Bestimmt, ob ein Strahl das Volumen des umgebenden Felds einer Kugel überschneidet.'
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
ms.openlocfilehash: e2d3ea263d7ad8bc50b936fd1010c352c0c01783
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093848"
---
# <a name="d3dxsphereboundprobe-function-d3dx9meshh"></a>D3DXSphereBoundProbe-Funktion (D3DX9Mesh.h)

Bestimmt, ob ein Strahl das Volumen des umgebenden Felds einer Kugel überschneidet.

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

Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die die Mittelpunktkoordinate der Kugel angibt.

</dd> <dt>

*Radius* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Radius der Kugel.

</dd> <dt>

*pRayPosition* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die die Ursprungskoordinate des Strahls angibt.

</dd> <dt>

*pRayDirection* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3dxvector3.md) die die Richtung des Strahls angibt. Dieser Vektor sollte nicht (0,0,0) sein, muss aber nicht normalisiert werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

Gibt **TRUE** zurück, wenn der Strahl das Volumen des umgebenden Felds der Kugel überschneidet. Andernfalls gibt **FALSE** zurück.

## <a name="remarks"></a>Bemerkungen

**D3DXSphereBoundProbe** bestimmt, ob der Strahl das Volumen des Begrenzungsfelds der Kugel überschneidet, nicht nur die Oberfläche der Kugel.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
