---
description: 'D3DXMatrixOrthoLH-Funktion (D3dx9math.h): Erstellt eine linkshändige orthografische Projektionsmatrix.'
ms.assetid: e42151bd-2302-491b-a211-7d5a4b8e437f
title: D3DXMatrixOrthoLH-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5492a6caba87025d83562c0327ac0e1f5a76f269
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107498"
---
# <a name="d3dxmatrixortholh-function-d3dx9mathh"></a>D3DXMatrixOrthoLH-Funktion (D3dx9math.h)

Erstellt eine linkshändige orthografische Projektionsmatrix.

## <a name="syntax"></a>Syntax


```C++
D3DXMATRIX* D3DXMatrixOrthoLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Zeiger auf die resultierende [**D3DXMATRIX.**](../direct3d10/d3d10-d3dxmatrix.md)

</dd> <dt>

*w* \[ in\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Breite des Ansichtsvolumes.

</dd> <dt>

*h* \[ in\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Höhe des Ansichtsvolumes.

</dd> <dt>

*zn* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Der minimale Z-Wert des Ansichtsvolumes, der als z-near bezeichnet wird.

</dd> <dt>

*NSD* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Maximaler Z-Wert des Ansichtsvolumes, der als z-far bezeichnet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Zeiger auf die resultierende [**D3DXMATRIX.**](../direct3d10/d3d10-d3dxmatrix.md)

## <a name="remarks"></a>Bemerkungen

Alle Parameter der **D3DXMatrixOrthoLH-Funktion** sind Abstände im Kameraraum. Die Parameter beschreiben die Dimensionen des Ansichtsvolumens.

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter zurückgegeben* wird. Auf diese Weise kann die **D3DXMatrixOrthoLH-Funktion** als Parameter für eine andere Funktion verwendet werden.

Diese Funktion verwendet die folgende Formel, um die zurückgegebene Matrix zu berechnen.


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zf-zn)   0
0    0   -zn/(zf-zn)  1
```



## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixOrthoRH**](d3dxmatrixorthorh.md)
</dt> <dt>

[**D3DXMatrixOrthoOffCenterRH**](d3dxmatrixorthooffcenterrh.md)
</dt> <dt>

[**D3DXMatrixOrthoOffCenterLH**](d3dxmatrixorthooffcenterlh.md)
</dt> </dl>

 

 
