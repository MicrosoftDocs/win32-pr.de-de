---
description: 'D3DXPlaneFromPointNormal-Funktion (D3DX10Math.h): Erstellt eine Ebene aus einem Punkt und einer Normalen.'
ms.assetid: 93c644d2-ab8c-47a1-9a3b-8b9c6a13178b
title: D3DXPlaneFromPointNormal-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneFromPointNormal
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ab9f3fdd53b1fbad4fa0b6a92c07589a8c0fab41c162dc49939f0e7254bf99c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991190"
---
# <a name="d3dxplanefrompointnormal-function-d3dx10mathh"></a>D3DXPlaneFromPointNormal-Funktion (D3DX10Math.h)

Erstellt eine Ebene aus einem Punkt und einer Normalen.

## <a name="syntax"></a>Syntax


```C++
D3DXPLANE* D3DXPlaneFromPointNormal(
  _Inout_       D3DXPLANE   *pOut,
  _In_    const D3DXVECTOR3 *pPoint,
  _In_    const D3DXVECTOR3 *pNormal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Zeiger auf die [**D3DXPLANE,**](d3d10-d3dxplane.md) die das Ergebnis des Vorgangs ist.

</dd> <dt>

*pPoint* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Zeiger auf einen [**D3DXVECTOR3,**](d3d10-d3dxvector3.md)der den Punkt definiert, der zum Erstellen der Ebene verwendet wird.

</dd> <dt>

*pNormal* \[ In\]
</dt> <dd>

Typ: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***

Zeiger auf eine D3DXVECTOR3-Struktur, die den normalen definiert, der zum Erstellen der Ebene verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***

Zeiger auf die D3DXPLANE-Struktur, die vom Punkt und der Normalität erstellt wurde.

## <a name="remarks"></a>Hinweise

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird. Auf diese Weise kann die D3DXPlaneFromPointNormal-Funktion als Parameter für eine andere Funktion verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
