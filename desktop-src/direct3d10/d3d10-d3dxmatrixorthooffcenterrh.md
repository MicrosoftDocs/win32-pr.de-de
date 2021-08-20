---
description: 'D3DXMatrixOrthoOffCenterRH-Funktion (D3DX10Math.h): Erstellt eine benutzerdefinierte, rechtshändige orthografische Projektionsmatrix.'
ms.assetid: 01d4d61e-de7b-4431-a168-68a50b1d6021
title: D3DXMatrixOrthoOffCenterRH-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixOrthoOffCenterRH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 79594b606124f6b3634e7b379bda0cb664cbec31b417112641d06f335a16ce04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118541241"
---
# <a name="d3dxmatrixorthooffcenterrh-function-d3dx10mathh"></a>D3DXMatrixOrthoOffCenterRH-Funktion (D3DX10Math.h)

Erstellt eine angepasste, rechtshändige orthografische Projektionsmatrix.

## <a name="syntax"></a>Syntax


```C++
D3DXMATRIX* D3DXMatrixOrthoOffCenterRH(
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

Zeiger auf die resultierende [**D3DXMATRIX.**](d3d10-d3dxmatrix.md)

## <a name="remarks"></a>Hinweise

Die [**D3DXMatrixOrthoRH-Funktion**](d3d10-d3dxmatrixorthorh.md) ist ein Sonderfall der D3DXMatrixOrthoOffCenterRH-Funktion. Um dieselbe Projektion mit D3DXMatrixOrthoOffCenterRH zu erstellen, verwenden Sie die folgenden Werte:

l = -w/2,

r = w/2,

b = -h/2 und

t = h/2.

Alle Parameter der D3DXMatrixOrthoOffCenterRH-Funktion sind Abstände im Kameraraum. Die Parameter beschreiben die Dimensionen des Ansichtsvolumens.

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird. Auf diese Weise kann die D3DXMatrixOrthoOffCenterRH-Funktion als Parameter für eine andere Funktion verwendet werden.

Diese Funktion verwendet die folgende Formel, um die zurückgegebene Matrix zu berechnen.


```
2/(r-l)      0            0           0
0            2/(t-b)      0           0
0            0            1/(zn-zf)   0
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

 

 
