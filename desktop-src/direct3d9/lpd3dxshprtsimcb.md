---
description: Rückruffunktion für die PRT-Simulation und-Komprimierung.
ms.assetid: 1d7e2149-d2ca-47da-be1f-8273fd9bd30a
title: LPD3DXSHPRTSIMCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 895d6fd3a7d9f93e858c08d1aaae416f1bf3abad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482086"
---
# <a name="lpd3dxshprtsimcb"></a>LPD3DXSHPRTSIMCB

Rückruffunktion für die PRT-Simulation und-Komprimierung.

## <a name="syntax"></a>Syntax


```
typedef HRESULT (WINAPI *LPD3DXSHPRTSIMCB)(
    FLOAT fPercentDone,
    LPVOID lpUserContext
);
```



## <a name="parameters"></a>Parameter

"vollständig": Gleit Komma Zahl zwischen 0 und 1,0, die den Prozentsatz der abgeschlossenen Berechnungen darstellt (zwischen 0 und 100 Prozent).

lpusercontext: Zeiger auf einen benutzerdefinierten Wert, der an die Rückruffunktion weitergeleitet wird. wird normalerweise von einer Anwendung verwendet, um einen Zeiger auf eine Datenstruktur zu übergeben, die Kontextinformationen für die Rückruffunktion bereitstellt.

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

 

 
