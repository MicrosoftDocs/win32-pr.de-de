---
description: Steuern von Filter Diagrammen mithilfe von C
ms.assetid: 56e41f0a-2ea6-422c-8d3f-7849e91e3731
title: Steuern von Filter Diagrammen mithilfe von C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ce6d78875c6b0d5f028ea89dfbd2b061285f1c1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392721"
---
# <a name="controlling-filter-graphs-using-c"></a>Steuern von Filter Diagrammen mithilfe von C

Wenn Sie eine DirectShow-Anwendung in C (anstatt C++) schreiben, müssen Sie einen vtable-Zeiger verwenden, um Methoden aufzurufen. Im folgenden Beispiel wird veranschaulicht, wie die **IUnknown:: QueryInterface** -Methode von einer in C geschriebenen Anwendung aufgerufen wird:


```C++
pGraph->lpVtbl->QueryInterface(pGraph, &IID_IMediaEvent, (void **)&pEvent);
```



Das folgende Beispiel zeigt den entsprechenden-Befehl in C++:


```C++
pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
```



In C werden COM-Schnittstellen als Strukturen definiert. Der **lpvtbl** -Member ist ein Zeiger auf eine Tabelle mit Schnittstellen Methoden (der vtable). Alle Methoden akzeptieren einen zusätzlichen Parameter, der ein Zeiger auf die-Schnittstelle ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anhänge](appendixes.md)
</dt> </dl>

 

 



