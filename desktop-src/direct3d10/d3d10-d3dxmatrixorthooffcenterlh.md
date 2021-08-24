---
description: 'D3DXMatrixOrthoOffCenterLH-Funktion (D3DX10Math.h): Erstellt eine angepasste, linkshändige orthografische Projektionsmatrix.'
ms.assetid: 84175c08-5a0b-4183-afe2-8aecafd73897
title: D3DXMatrixOrthoOffCenterLH-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoOffCenterLH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4396f060d33efef454e87d8594c2b4ca29e46cbcbc08151cacaa76a7a4965735
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852850"
---
# <a name="d3dxmatrixorthooffcenterlh-function-d3dx10mathh"></a>D3DXMatrixOrthoOffCenterLH-Funktion (D3DX10Math.h)

Erstellt eine angepasste, linkshändige orthografische Projektionsmatrix.

## <a name="syntax"></a>Syntax


```C++
D3DXMATRIX* D3DXMatrixOrthoOffCenterLH(
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

Zeiger auf die resultierende [**D3DXMATRIX.**](d3d10-d3dxmatrix.md)

</dd> <dt>

*l* \[ in\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Minimaler x-Wert des Ansichtsvolumes.

</dd> <dt>

*r* \[ in\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Maximaler x-Wert des Ansichtsvolumes.

</dd> <dt>

*b* \[ in\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Minimaler y-Wert des Anzeigevolumes.

</dd> <dt>

*t* \[ in\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Maximaler y-Wert des Anzeigevolumes.

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

Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Zeiger auf die resultierende [**D3DXMATRIX.**](d3d10-d3dxmatrix.md)

## <a name="remarks"></a>Hinweise

[**D3DXMatrixOrthoLH**](d3d10-d3dxmatrixortholh.md) ist ein Sonderfall der D3DXMatrixOrthoOffCenterLH-Funktion. Verwenden Sie die folgenden Werte, um dieselbe Projektion mit D3DXMatrixOrthoOffCenterLH zu erstellen:

l = -w/2,

r = w/2,

b = -h/2 und

t = h/2.

Alle Parameter der D3DXMatrixOrthoOffCenterLH-Funktion sind Entfernungen im Kameraraum. Die Parameter beschreiben die Dimensionen des Ansichtsvolumes.

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird. Auf diese Weise kann die D3DXMatrixOrthoOffCenterLH-Funktion als Parameter für eine andere Funktion verwendet werden.

Diese Funktion verwendet die folgende Formel, um die zurückgegebene Matrix zu berechnen.


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zf-zn)   0
(l+r)/(l-r)  (t+b)/(b-t)  zn/(zn-zf)  1
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
