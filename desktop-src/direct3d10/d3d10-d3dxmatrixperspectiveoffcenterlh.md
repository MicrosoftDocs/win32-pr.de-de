---
description: Erstellt eine angepasste, Links übergebene perspektivische Projektions Matrix.
ms.assetid: 73616fcc-1799-4e65-92b9-2d8f500c326e
title: D3DXMatrixPerspectiveOffCenterLH-Funktion (D3DX10Math. h)
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
ms.openlocfilehash: 2fb289c0dff148850b8174ccb04a3e3fbfa79d92
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367477"
---
# <a name="d3dxmatrixperspectiveoffcenterlh-function-d3dx10mathh"></a>D3DXMatrixPerspectiveOffCenterLH-Funktion (D3DX10Math. h)

Erstellt eine angepasste, Links übergebene perspektivische Projektions Matrix.

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

*Pout* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Ein Zeiger auf die [**D3DXMATRIX**](d3d10-d3dxmatrix.md) -Struktur, die das Ergebnis des Vorgangs ist.

</dd> <dt>

*l* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Minimaler x-Wert des Ansichts Volumes.

</dd> <dt>

*r* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Maximaler x-Wert des Ansichts Volumes.

</dd> <dt>

*b* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Minimaler y-Wert des Ansichts Volumes.

</dd> <dt>

*t* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Maximaler y-Wert des Ansichts Volumes.

</dd> <dt>

*Zn* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Der minimale z-Wert des Ansichts Volumes.

</dd> <dt>

*ZF* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Maximaler z-Wert des Ansichts Volumes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Zeiger auf eine D3DXMATRIX-Struktur, die eine angepasste, Links übergebene perspektivische Projektions Matrix ist.

## <a name="remarks"></a>Bemerkungen

Alle Parameter der D3DXMatrixPerspectiveOffCenterLH-Funktion sind Abstände im Kamerabereich. Die Parameter beschreiben die Dimensionen des Ansichts Volumes.

Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird. Auf diese Weise kann die D3DXMatrixPerspectiveOffCenterLH-Funktion als Parameter für eine andere Funktion verwendet werden.

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
| Header<br/>  | <dl> <dt>D3DX10Math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mathematische Funktionen](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
