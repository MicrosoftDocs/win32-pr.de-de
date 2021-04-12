---
description: Erstellt eine linke orthografische Projektions Matrix.
ms.assetid: e42151bd-2302-491b-a211-7d5a4b8e437f
title: D3DXMatrixOrthoLH-Funktion (D3dx9math. h)
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
ms.openlocfilehash: 4aaf4a1a770ba0200a6afe389d37e248b9f4c7de
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355426"
---
# <a name="d3dxmatrixortholh-function-d3dx9mathh"></a>D3DXMatrixOrthoLH-Funktion (D3dx9math. h)

Erstellt eine linke orthografische Projektions Matrix.

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

*Pout* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Zeiger auf das resultierende [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).

</dd> <dt>

*w* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Breite des Ansichts Volumes.

</dd> <dt>

*h* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Höhe des Ansichts Volumes.

</dd> <dt>

*Zn* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Der minimale z-Wert des Ansichts Volumes, das als z-near bezeichnet wird.

</dd> <dt>

*ZF* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Maximaler z-Wert des Ansichts Volumes, das als "z-weit" bezeichnet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Zeiger auf das resultierende [**D3DXMATRIX**](../direct3d10/d3d10-d3dxmatrix.md).

## <a name="remarks"></a>Bemerkungen

Alle Parameter der **D3DXMatrixOrthoLH** -Funktion sind Abstände im Kamerabereich. Die Parameter beschreiben die Dimensionen des Ansichts Volumes.

Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird. Auf diese Weise kann die **D3DXMatrixOrthoLH** -Funktion als Parameter für eine andere Funktion verwendet werden.

Diese Funktion verwendet die folgende Formel, um die zurückgegebene Matrix zu berechnen.


```
2/w  0    0           0
0    2/h  0           0
0    0    1/(zf-zn)   0
0    0   -zn/(zf-zn)  1
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixOrthoRH**](d3dxmatrixorthorh.md)
</dt> <dt>

[**D3DXMatrixOrthoOffCenterRH**](d3dxmatrixorthooffcenterrh.md)
</dt> <dt>

[**D3DXMatrixOrthoOffCenterLH**](d3dxmatrixorthooffcenterlh.md)
</dt> </dl>

 

 
