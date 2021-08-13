---
description: Rückruffunktion für UVAtlas.
ms.assetid: a605ae27-10c9-49b4-98fe-8c788c2c0752
title: LPD3DXUVATLASCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4473134d7ecf98c50d0c3a69085e7f46344d1d57ff2650c1adbc54c43dba266
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119458714"
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

\[out fPercentDone: Gleitkommazahl zwischen 0 und 1,0, die den Prozentsatz der abgeschlossenen Berechnungen \] (zwischen 0 und 100 Prozent) darstellt.

\[in lpUserContext: Zeiger auf einen benutzerdefinierten Wert, der an die Rückruffunktion übergeben wird. Wird in der Regel von einer Anwendung verwendet, um einen Zeiger auf eine Datenstruktur zu übergeben, die Kontextinformationen für die Rückruffunktion \] bietet.

## <a name="return-value"></a>Rückgabewert

Diese Funktion muss implementiert werden, um S \_ OK zurück zu geben, um den Simulator weiter ausführen zu können. Jeder andere Wert hält den Simulator an.

## <a name="remarks"></a>Hinweise

Achten Sie darauf, die Windows [**Datentypen beim**](../winprog/windows-data-types.md) Deklarieren der Rückruffunktion anzugeben. Andernfalls können Stapelüberläufe auftreten.



| Anforderung                         | Wert            |
|--------------------------|-------------|
| Header                   | d3dx9mesh.h |
| Importbibliothek           | d3dx9.lib   |
| Mindestbetriebssystem | Windows 98  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rückruffunktionen](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
