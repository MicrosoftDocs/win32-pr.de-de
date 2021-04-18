---
description: Rückruffunktion für uvatlas.
ms.assetid: a605ae27-10c9-49b4-98fe-8c788c2c0752
title: LPD3DXUVATLASCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbda7c58ef001a936b01f3af2027f9207c3d2770
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344172"
---
# <a name="lpd3dxuvatlascb"></a>LPD3DXUVATLASCB

Rückruffunktion für uvatlas.

## <a name="syntax"></a>Syntax


```
typedef HRESULT (*LPD3DXUVATLASCB ( 
    FLOAT fPercentDone,
    LPVOID lpUserContext
);
```



## <a name="parameters"></a>Parameter

\[Out \] -vollständig: Gleit Komma Zahl zwischen 0 und 1,0, die den Prozentsatz der abgeschlossenen Berechnungen darstellt (zwischen 0 und 100 Prozent).

\[in \] lpusercontext: Zeiger auf einen benutzerdefinierten Wert, der an die Rückruffunktion übergeben wird. wird in der Regel von einer Anwendung verwendet, um einen Zeiger auf eine Datenstruktur zu übergeben, die Kontextinformationen für die Rückruffunktion bereitstellt.

## <a name="return-value"></a>Rückgabewert

Diese Funktion muss implementiert werden, damit S OK zurückgegeben wird \_ , um den Simulator weiterhin ausführen zu können. Jeder andere Wert hält den Simulator an.

## <a name="remarks"></a>Bemerkungen

Achten Sie darauf, beim Deklarieren der Rückruffunktion die Aufruf Konvention für [**Windows-Datentypen**](../winprog/windows-data-types.md) anzugeben. Andernfalls können Stapel Überläufe auftreten.



|                          |             |
|--------------------------|-------------|
| Header                   | d3dx9mesh. h |
| Importbibliothek           | d3dx9. lib   |
| Mindestens Betriebs System | Windows 98  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rückruffunktionen](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
