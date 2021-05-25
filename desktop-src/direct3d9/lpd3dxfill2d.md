---
description: 'LPD3DXFILL2D: Funktionstyp, der von den Texturfüllfunktionen verwendet wird.'
ms.assetid: faa2d610-cf85-42d0-833c-a46fb7fe3dbf
title: LPD3DXFILL2D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c341ccfcbcc566d65e7139813c676e2286e25cf
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342845"
---
# <a name="lpd3dxfill2d"></a>LPD3DXFILL2D

Funktionstyp, der von den Texturfüllfunktionen verwendet wird.

## <a name="syntax"></a>Syntax


```
typedef VOID (WINAPI *LPD3DXFILL2D)(
    D3DXVECTOR4* pOut, 
    CONST D3DXVECTOR2* pTexCoord, 
    CONST D3DXVECTOR2* pTexelSize, 
    LPVOID pData,  
);
```



## <a name="parameters"></a>Parameter

pOut: Zeiger auf einen Vektor, der von der Funktion verwendet wird, um das Ergebnis zurückzugeben. X, Y, Z und W werden R, G, B bzw. A zugeordnet.

pTexCoord: Zeiger auf einen Vektor, der die Koordinaten des texel enthält, das gerade ausgewertet wird. Texturkoordinatenkomponenten für Textur- und Volumentexturen reichen von 0 bis 1. Texturkoordinatenkomponenten für Cubetexturen reichen von -1 bis 1.

pTexelSize: Zeiger auf einen Vektor, der die Abmessungen des aktuellen Texels enthält.

pData: Zeiger auf Benutzerdaten.

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Achten Sie darauf, beim Deklarieren der Rückruffunktion die Aufrufkonvention für [**Windows-Datentypen**](../winprog/windows-data-types.md) anzugeben. Andernfalls können Stapelüberläufe auftreten.



| Anforderung                         | Wert           |
|--------------------------|------------|
| Header                   | d3dx9tex.h |
| Importbibliothek           | d3dx9.lib  |
| Mindestbetriebssystem | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rückruffunktionen](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> <dt>

[LPD3DXFILL3D](lpd3dxfill3d.md)
</dt> </dl>

 

 
