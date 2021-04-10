---
description: Der Funktionstyp, der von den Textur Füll Funktionen verwendet wird.
ms.assetid: faa2d610-cf85-42d0-833c-a46fb7fe3dbf
title: LPD3DXFILL2D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c8c9d9ef610ee10faa069841a05f43c17b0885c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213858"
---
# <a name="lpd3dxfill2d"></a>LPD3DXFILL2D

Der Funktionstyp, der von den Textur Füll Funktionen verwendet wird.

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

Pout-Zeiger auf einen Vektor, den die Funktion verwendet, um das Ergebnis zurückzugeben. X, Y, Z und W werden R, G, B bzw. zugeordnet.

ptexcoord-Zeiger auf einen Vektor, der die Koordinaten des Texels enthält, das derzeit ausgewertet wird. Texturkoordinaten Komponenten für Textur-und volumetexturen reichen von 0 bis 1. Texturkoordinaten Komponenten für cubetexturen reichen von-1 bis 1.

ptexelsize: Zeiger auf einen Vektor, der die Abmessungen des aktuellen Texels enthält.

pData-Zeiger auf Benutzerdaten.

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Achten Sie darauf, beim Deklarieren der Rückruffunktion die Aufruf Konvention für [**Windows-Datentypen**](../winprog/windows-data-types.md) anzugeben. Andernfalls können Stapel Überläufe auftreten.



|                          |            |
|--------------------------|------------|
| Header                   | d3dx9tex. h |
| Importbibliothek           | d3dx9. lib  |
| Mindestens Betriebs System | Windows 98 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rückruffunktionen](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> <dt>

[LPD3DXFILL3D](lpd3dxfill3d.md)
</dt> </dl>

 

 
