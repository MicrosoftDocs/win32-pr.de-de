---
description: 'D3DXMatrixPerspectiveOffCenterLH-Funktion (D3DX10Math.h): Erstellt eine benutzerdefinierte, linkshändige perspektivische Projektionsmatrix.'
ms.assetid: 73616fcc-1799-4e65-92b9-2d8f500c326e
title: D3DXMatrixPerspectiveOffCenterLH-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveOffCenterLH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 99dc5c5b0806f119f3728facbb0d67c88884bb537e909daf0c7687392e20784a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858750"
---
# <a name="d3dxmatrixperspectiveoffcenterlh-function-d3dx10mathh"></a>D3DXMatrixPerspectiveOffCenterLH-Funktion (D3DX10Math.h)

Erstellt eine angepasste, linkshändige Perspektivprojektionsmatrix.

## <a name="syntax"></a>Syntax


```C++
D3DXMATRIX* D3DXMatrixPerspectiveOffCenterLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      l,
  _In_    FLOAT      r,
  _In_    FLOAT      b,
  _In_    FLOAT      t,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Zeiger auf die [**D3DXMATRIX-Struktur,**](d3d10-d3dxmatrix.md) die das Ergebnis des Vorgangs ist.

</dd> <dt>

*l* \[ in\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Minimaler x-Wert des Ansichtsvolumens.

</dd> <dt>

*r* \[ in\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Maximaler x-Wert des Ansichtsvolumens.

</dd> <dt>

*b* \[ in\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Minimaler y-Wert des Ansichtsvolumens.

</dd> <dt>

*t* \[ in\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Maximaler y-Wert des Ansichtsvolumens.

</dd> <dt>

*zn* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Minimaler Z-Wert des Ansichtsvolumens.

</dd> <dt>

*( )* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Maximaler Z-Wert des Ansichtsvolumens.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Zeiger auf eine D3DXMATRIX-Struktur, bei der es sich um eine benutzerdefinierte, linkshändige Perspektivprojektionsmatrix handelt.

## <a name="remarks"></a>Hinweise

Alle Parameter der D3DXMatrixPerspectiveOffCenterLH-Funktion sind Abstände im Kameraraum. Die Parameter beschreiben die Dimensionen des Ansichtsvolumens.

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird. Auf diese Weise kann die D3DXMatrixPerspectiveOffCenterLH-Funktion als Parameter für eine andere Funktion verwendet werden.

Diese Funktion verwendet die folgende Formel, um die zurückgegebene Matrix zu berechnen.


```
2*zn/(r-l)   0            0              0
0            2*zn/(t-b)   0              0
(l+r)/(l-r)  (t+b)/(b-t)  zf/(zf-zn)     1
0            0            zn*zf/(zn-zf)  0
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
