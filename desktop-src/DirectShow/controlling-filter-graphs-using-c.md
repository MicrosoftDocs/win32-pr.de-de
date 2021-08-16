---
description: Steuern von Filterdiagrammen mit C
ms.assetid: 56e41f0a-2ea6-422c-8d3f-7849e91e3731
title: Steuern von Filterdiagrammen mit C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e234413f7642d7349c2bf378d1aded97b399e252117b0793f90335de8643912e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073754"
---
# <a name="controlling-filter-graphs-using-c"></a>Steuern von Filterdiagrammen mit C

Wenn Sie eine DirectShow-Anwendung in C (anstelle von C++) schreiben, müssen Sie zum Aufrufen von Methoden einen vtable-Zeiger verwenden. Im folgenden Beispiel wird veranschaulicht, wie sie die **IUnknown::QueryInterface-Methode** aus einer in C geschriebenen Anwendung aufruft:


```C++
pGraph->lpVtbl->QueryInterface(pGraph, &IID_IMediaEvent, (void **)&pEvent);
```



Das folgende Beispiel zeigt den entsprechenden Aufruf in C++:


```C++
pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
```



In C werden COM-Schnittstellen als Strukturen definiert. Der **lpVtbl-Member** ist ein Zeiger auf eine Tabelle von Schnittstellenmethoden (die vtable). Alle Methoden nehmen einen zusätzlichen Parameter an, der ein Zeiger auf die -Schnittstelle ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anhänge](appendixes.md)
</dt> </dl>

 

 



