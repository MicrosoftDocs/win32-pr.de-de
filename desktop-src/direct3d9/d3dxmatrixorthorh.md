---
description: 'D3DXMatrixOrthoRH-Funktion (D3dx9math.h): Erstellt eine rechtshändige orthografische Projektionsmatrix.'
ms.assetid: 6b9b50d5-0307-4fc7-a28d-8f42d2a21bf0
title: D3DXMatrixOrthoRH-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoRH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 060a195dfee7457f671177a756e67d1c3953a16aa7d59394f96eb05e43cfc93c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044848"
---
# <a name="d3dxmatrixorthorh-function-d3dx9mathh"></a>D3DXMatrixOrthoRH-Funktion (D3dx9math.h)

Erstellt eine rechtshändige orthografische Projektionsmatrix.

## <a name="syntax"></a>Syntax


```C++
D3DXMATRIX* D3DXMatrixOrthoRH(
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

Minimaler Z-Wert des Ansichtsvolumes.

</dd> <dt>

*NSDR* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Maximaler Z-Wert des Ansichtsvolumes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Zeiger auf die resultierende [**D3DXMATRIX.**](../direct3d10/d3d10-d3dxmatrix.md)

## <a name="remarks"></a>Hinweise

Alle Parameter der **D3DXMatrixOrthoRH-Funktion** sind Entfernungen im Kameraraum. Die Parameter beschreiben die Dimensionen des Ansichtsvolumes.

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter* zurückgegeben wird. Auf diese Weise kann die **D3DXMatrixOrthoRH-Funktion** als Parameter für eine andere Funktion verwendet werden.

Diese Funktion verwendet die folgende Formel, um die zurückgegebene Matrix zu berechnen.


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zn-zf)   0
0    0    zn/(zn-zf)  1
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixOrthoLH**](d3dxmatrixortholh.md)
</dt> <dt>

[**D3DXMatrixOrthoOffCenterRH**](d3dxmatrixorthooffcenterrh.md)
</dt> <dt>

[**D3DXMatrixOrthoOffCenterLH**](d3dxmatrixorthooffcenterlh.md)
</dt> </dl>

 

 
