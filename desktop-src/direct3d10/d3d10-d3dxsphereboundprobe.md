---
description: 'D3DXSphereBoundProbe-Funktion (D3DX10math.h): Bestimmt, ob ein Strahl das Volumen des umgebenden Felds einer Kugel überschneidet.'
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
ms.openlocfilehash: fb5a329e39631dff626ff1c7945ad4b05f9dcd58
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108468"
---
# <a name="d3dxsphereboundprobe-function-d3dx10mathh"></a>D3DXSphereBoundProbe-Funktion (D3DX10math.h)

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

Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3d10-d3dxvector3.md) die die Mittelpunktkoordinate der Kugel angibt.

</dd> <dt>

*Radius* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Radius der Kugel.

</dd> <dt>

*pRayPosition* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3d10-d3dxvector3.md) die die Ursprungskoordinate des Strahls angibt.

</dd> <dt>

*pRayDirection* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Zeiger auf eine [**D3DXVECTOR3-Struktur,**](d3d10-d3dxvector3.md) die die Richtung des Strahls angibt. Dieser Vektor sollte nicht (0,0,0) sein, muss aber nicht normalisiert werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

Gibt **TRUE** zurück, wenn der Strahl das Volumen des umgebenden Felds der Kugel überschneidet. Andernfalls gibt **FALSE** zurück.

## <a name="remarks"></a>Bemerkungen

**D3DXSphereBoundProbe** bestimmt, ob der Strahl das Volumen des Begrenzungsfelds der Kugel überschneidet, nicht nur die Oberfläche der Kugel.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mesh-Funktionen](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
