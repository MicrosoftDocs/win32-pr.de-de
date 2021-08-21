---
description: Rückruffunktion für die PrT-Simulation und -Komprimierung (Precomputed Radiance Transfer).
ms.assetid: 1d7e2149-d2ca-47da-be1f-8273fd9bd30a
title: LPD3DXSHPRTSIMCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c81e510808dd2e14af1de0d9618591d8ea3b8587bb4015e72a3e01fa33157b5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118799333"
---
# <a name="lpd3dxshprtsimcb"></a>LPD3DXSHPRTSIMCB

Rückruffunktion für die PrT-Simulation und -Komprimierung (Precomputed Radiance Transfer).

## <a name="syntax"></a>Syntax


```
typedef HRESULT (WINAPI *LPD3DXSHPRTSIMCB)(
    FLOAT fPercentDone,
    LPVOID lpUserContext
);
```



## <a name="parameters"></a>Parameter

fPercentDone: Gleitkommazahl zwischen 0 und 1,0, die den Prozentsatz der abgeschlossenen Berechnungen (zwischen 0 und 100 Prozent) darstellt.

lpUserContext: Zeiger auf einen benutzerdefinierten Wert, der an die Rückruffunktion übergeben wird; Wird in der Regel von einer Anwendung verwendet, um einen Zeiger auf eine Datenstruktur zu übergeben, die Kontextinformationen für die Rückruffunktion enthält.

## <a name="return-value"></a>Rückgabewert

Diese Funktion muss implementiert werden, um S \_ OK zurück zu geben, um den Simulator weiter ausführen zu können. Jeder andere Wert hält den Simulator an.

## <a name="remarks"></a>Hinweise

Achten Sie darauf, die Windows [**Datentypen**](../winprog/windows-data-types.md) beim Deklarieren der Rückruffunktion anzugeben. Andernfalls können Stapelüberläufe auftreten.



| Anforderung                         | Wert            |
|--------------------------|-------------|
| Header                   | d3dx9mesh.h |
| Importbibliothek           | d3dx9.lib   |
| Mindestbetriebssystem | Windows 98  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rückruffunktionen](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
