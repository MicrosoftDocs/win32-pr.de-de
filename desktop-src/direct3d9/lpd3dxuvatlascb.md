---
description: Rückruffunktion für UVAtlas.
ms.assetid: a605ae27-10c9-49b4-98fe-8c788c2c0752
title: LPD3DXUVATLASCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfe073b5e6a798ccb74421d42502b089d59be11f
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342795"
---
# <a name="lpd3dxuvatlascb"></a>LPD3DXUVATLASCB

Rückruffunktion für UVAtlas.

## <a name="syntax"></a>Syntax


```
typedef HRESULT (*LPD3DXUVATLASCB ( 
    FLOAT fPercentDone,
    LPVOID lpUserContext
);
```



## <a name="parameters"></a>Parameter

\[out \] fPercentDone: Gleitkommazahl zwischen 0 und 1,0, die den Prozentsatz der abgeschlossenen Berechnungen darstellt (zwischen 0 und 100 Prozent).

\[in \] lpUserContext: Zeiger auf einen benutzerdefinierten Wert, der an die Rückruffunktion übergeben wird. Wird in der Regel von einer Anwendung verwendet, um einen Zeiger auf eine Datenstruktur zu übergeben, die Kontextinformationen für die Rückruffunktion bereitstellt.

## <a name="return-value"></a>Rückgabewert

Diese Funktion muss implementiert werden, um S \_ OK zurückzugeben, um den Simulator weiter auszuführen. Jeder andere Wert hält den Simulator an.

## <a name="remarks"></a>Hinweise

Achten Sie darauf, beim Deklarieren der Rückruffunktion die Aufrufkonvention für [**Windows-Datentypen**](../winprog/windows-data-types.md) anzugeben. Andernfalls können Stapelüberläufe auftreten.



| Anforderung                         | Wert            |
|--------------------------|-------------|
| Header                   | d3dx9mesh.h |
| Importbibliothek           | d3dx9.lib   |
| Mindestbetriebssystem | Windows 98  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rückruffunktionen](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
