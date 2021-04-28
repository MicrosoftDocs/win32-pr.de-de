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
ms.openlocfilehash: eec478fec30567fbf301054ddfa60f1689bfee8e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118348"
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

Z-Wert der ansichtsnahen Ebene.

</dd> <dt>

*NSD* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

Z-Wert der fernen Ansichtsebene.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Zeiger auf eine [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) bei der es sich um eine linkshändige Projektionsmatrix handelt.

## <a name="remarks"></a>Bemerkungen

Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter* zurückgegeben wird. Auf diese Weise kann die **D3DXMatrixPerspectiveFovLH-Funktion** als Parameter für eine andere Funktion verwendet werden.

Um die Seitenverhältnisachse zu ändern, verwenden Sie die Berechnungsformel: fovy = 2 * math.atan(math.tan(fovy * 0,5) / aspect). Fügen Sie alternativ X- und Y-Seitenverhältnisvariablen in der Struktur hinzu, um den vertikalen Ansichtsbereich zu skalieren: fovy = 2 * math.atan(math.tan(fovy * 0,5) / aspectY), aspect = aspectX * aspect Y.

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



| Anforderungen | Wert |
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

 

 
