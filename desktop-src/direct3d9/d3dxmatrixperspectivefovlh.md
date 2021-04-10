---
description: Erstellt eine linkshändige perspektivische Projektionsmatrix auf der Grundlage eines Sichtfelds.
ms.assetid: 90328798-f124-4b61-90a9-971946066b02
title: D3DXMatrixPerspectiveFovLH-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveFovLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 91b25a2e319236485c2c290b55acb94954a4791d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219635"
---
# <a name="d3dxmatrixperspectivefovlh-function-d3dx9mathh"></a>D3DXMatrixPerspectiveFovLH-Funktion (D3dx9math. h)

Erstellt eine linkshändige perspektivische Projektionsmatrix auf der Grundlage eines Sichtfelds.

## <a name="syntax"></a>Syntax


```C++
D3DXMATRIX* D3DXMatrixPerspectiveFovLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      fovy,
  _In_    FLOAT      Aspect,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pout* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Ein Zeiger auf die [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die das Ergebnis des Vorgangs ist.

</dd> <dt>

*fovy* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Feld der Ansicht in y-Richtung im Bogenmaße.

</dd> <dt>

*Aspekt* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Seitenverhältnis, definiert als Breite des Ansichts Raums dividiert durch Höhe.

</dd> <dt>

*Zn* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Z-Wert der nahen Ansichts Ebene.

</dd> <dt>

*ZF* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)**

Z-Wert der weit entfernten Ansichts Ebene.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, bei der es sich um eine Perspektiven Projektions Matrix mit linker Übergabe handelt.

## <a name="remarks"></a>Bemerkungen

Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird. Auf diese Weise kann die **D3DXMatrixPerspectiveFovLH** -Funktion als Parameter für eine andere Funktion verwendet werden.

Verwenden Sie zum Ändern der Seitenverhältnis Achse die Berechnungsformel: fovy = 2 * Math. Atan (Math. Tan (fovy * 0,5)/Aspekt). Fügen Sie alternativ die Variablen X und Y-Seitenverhältnis in der Struktur hinzu, um den vertikalen Ansichts Bereich zu skalieren: fovy = 2 * Math. Atan (Math. Tan (fovy * 0,5)/aspecty), Aspekt = aspectx * Aspekt Y.

Diese Funktion berechnet die zurückgegebene Matrix wie gezeigt:


```
xScale     0          0               0
0        yScale       0               0
0          0       zf/(zf-zn)         1
0          0       -zn*zf/(zf-zn)     0
where:
yScale = cot(fovY/2)

xScale = yScale / aspect ratio
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

[**D3DXMatrixPerspectiveRH**](d3dxmatrixperspectiverh.md)
</dt> <dt>

[**D3DXMatrixPerspectiveLH**](d3dxmatrixperspectivelh.md)
</dt> <dt>

[**D3DXMatrixPerspectiveFovRH**](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[**D3DXMatrixPerspectiveOffCenterRH**](d3dxmatrixperspectiveoffcenterrh.md)
</dt> <dt>

[**D3DXMatrixPerspectiveOffCenterLH**](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
