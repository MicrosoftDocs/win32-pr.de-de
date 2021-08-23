---
description: 'D3DXMatrixPerspectiveFovLH-Funktion (D3dx9math.h): Erstellt eine linkshändige Projektionsmatrix basierend auf einem Sichtfeld.'
ms.assetid: 90328798-f124-4b61-90a9-971946066b02
title: D3DXMatrixPerspectiveFovLH-Funktion (D3dx9math.h)
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
ms.openlocfilehash: cc530d4e0d977bac7df89f040d63552a4f0ca852c4e04ba0724f408daef10829
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122890"
---
# <a name="d3dxmatrixperspectivefovlh-function-d3dx9mathh"></a>D3DXMatrixPerspectiveFovLH-Funktion (D3dx9math.h)

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

*pOut* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Zeiger auf die [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die das Ergebnis des Vorgangs ist.

</dd> <dt>

*fovy* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Sichtfeld in y-Richtung, im Bogenmaß.

</dd> <dt>

*Aspekt* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Seitenverhältnis, definiert als Ansichtsraumbreite dividiert durch Höhe.

</dd> <dt>

*zn* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Z-Wert der Near View-Plane.

</dd> <dt>

*NSDR* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Z-Wert der fernen Ansichtsebene.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die eine linkshändige perspektivische Projektionsmatrix ist.

## <a name="remarks"></a>Hinweise

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter* zurückgegeben wird. Auf diese Weise kann die **D3DXMatrixPerspectiveFovLH-Funktion** als Parameter für eine andere Funktion verwendet werden.

Um die Seitenverhältnisachse zu ändern, verwenden Sie die Berechnungsformel: fovy = 2 * math.atan(math.tan(fovy * 0,5) / aspect). Fügen Sie alternativ X- und Y-Seitenverhältnisvariablen in der Struktur hinzu, um den vertikalen Ansichtsbereich zu skalieren: fovy = 2 * math.atan(math.tan(fovy * 0,5) / aspectY), aspect = aspectX * aspect Y.

Diese Funktion berechnet die zurückgegebene Matrix wie folgt:


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
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

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

 

 
