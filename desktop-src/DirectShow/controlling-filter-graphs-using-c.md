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
# <a name="controlling-filter-graphs-using-c"></a><span data-ttu-id="07aac-103">Steuern von Filter Diagrammen mithilfe von C</span><span class="sxs-lookup"><span data-stu-id="07aac-103">Controlling Filter Graphs Using C</span></span>

<span data-ttu-id="07aac-104">Wenn Sie eine DirectShow-Anwendung in C (anstatt C++) schreiben, müssen Sie einen vtable-Zeiger verwenden, um Methoden aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="07aac-104">If you are writing a DirectShow application in C (rather than C++), you must use a vtable pointer to call methods.</span></span> <span data-ttu-id="07aac-105">Im folgenden Beispiel wird veranschaulicht, wie die **IUnknown:: QueryInterface** -Methode von einer in C geschriebenen Anwendung aufgerufen wird:</span><span class="sxs-lookup"><span data-stu-id="07aac-105">The following example illustrates how to call the **IUnknown::QueryInterface** method from an application written in C:</span></span>


```C++
pGraph->lpVtbl->QueryInterface(pGraph, &IID_IMediaEvent, (void **)&pEvent);
```



<span data-ttu-id="07aac-106">Das folgende Beispiel zeigt den entsprechenden-Befehl in C++:</span><span class="sxs-lookup"><span data-stu-id="07aac-106">The following shows the equivalent call in C++:</span></span>


```C++
pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
```



<span data-ttu-id="07aac-107">In C werden COM-Schnittstellen als Strukturen definiert.</span><span class="sxs-lookup"><span data-stu-id="07aac-107">In C, COM interfaces are defined as structures.</span></span> <span data-ttu-id="07aac-108">Der **lpvtbl** -Member ist ein Zeiger auf eine Tabelle mit Schnittstellen Methoden (der vtable).</span><span class="sxs-lookup"><span data-stu-id="07aac-108">The **lpVtbl** member is a pointer to a table of interface methods (the vtable).</span></span> <span data-ttu-id="07aac-109">Alle Methoden akzeptieren einen zusätzlichen Parameter, der ein Zeiger auf die-Schnittstelle ist.</span><span class="sxs-lookup"><span data-stu-id="07aac-109">All methods take an additional parameter, which is a pointer to the interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="07aac-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="07aac-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07aac-111">Anhänge</span><span class="sxs-lookup"><span data-stu-id="07aac-111">Appendixes</span></span>](appendixes.md)
</dt> </dl>

 

 



