---
title: Verwalten der Speicher Belegung
description: Verwalten der Speicher Belegung
ms.assetid: 8a189fe8-5555-44bb-968b-04408fa7fce4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2af04b4ecc5b8480230b17ae710b84ce8e6ce5d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391090"
---
# <a name="managing-memory-allocation"></a><span data-ttu-id="815d3-103">Verwalten der Speicher Belegung</span><span class="sxs-lookup"><span data-stu-id="815d3-103">Managing Memory Allocation</span></span>

<span data-ttu-id="815d3-104">In com werden viele, wenn nicht die meisten, Schnittstellen Methoden von Code aufgerufen, der von einer Programmier Organisation geschrieben und durch Code implementiert wird, der von einem anderen geschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="815d3-104">In COM, many, if not most, interface methods are called by code written by one programming organization and implemented by code written by another.</span></span> <span data-ttu-id="815d3-105">Viele Parameter und Rückgabewerte dieser Funktionen sind Typen, die als Wert umgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="815d3-105">Many of the parameters and return values of these functions are of types that can be passed around by value.</span></span> <span data-ttu-id="815d3-106">Manchmal ist es jedoch erforderlich, Datenstrukturen zu übergeben, für die dies nicht der Fall ist. Daher ist es erforderlich, dass sowohl der Aufrufer als auch der Aufruf einer kompatiblen Zuordnungs-und Aufhebung der Zuordnungs Richtlinie ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="815d3-106">Sometimes, however, it is necessary to pass data structures for which this is not the case, so it is necessary for both caller and called to have a compatible allocation and de-allocation policy.</span></span> <span data-ttu-id="815d3-107">COM definiert eine universelle Konvention für die Speicher Belegung, da dies sinnvoller ist als das Definieren von Regeln für die Groß-/Kleinschreibung und die Implementierung des com-remote Prozedur Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="815d3-107">COM defines a universal convention for memory allocation, because it is more reasonable than defining case-by-case rules and so that the COM remote procedure call implementation can correctly manage memory.</span></span>

<span data-ttu-id="815d3-108">Die Methoden einer COM-Schnittstelle bieten immer eine Speicherverwaltung von Zeigern auf die-Schnittstelle, indem die [**adressf**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) -und [**releasefunktionen**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) aufgerufen werden, die in der [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) -Schnittstelle gefunden werden, von der alle anderen com-</span><span class="sxs-lookup"><span data-stu-id="815d3-108">The methods of a COM interface always provide memory management of pointers to the interface by calling the [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) and [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) functions found in the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface, from which all other COM interfaces derive.</span></span> <span data-ttu-id="815d3-109">(Weitere Informationen finden Sie unter [Regeln zum Verwalten der Verweis Anzahl](rules-for-managing-reference-counts.md) .)</span><span class="sxs-lookup"><span data-stu-id="815d3-109">(See [Rules for Managing Reference Counts](rules-for-managing-reference-counts.md) for more information.)</span></span>

<span data-ttu-id="815d3-110">In diesem Abschnitt wird nur beschrieben, wie Arbeitsspeicher für Parameter belegt wird, die nicht als Wert weitergereicht werden – nicht als Zeiger auf Schnittstellen, sondern um mehr alltägliche Dinge, wie z. b. Zeichen folgen, Zeiger auf Strukturen usw.</span><span class="sxs-lookup"><span data-stu-id="815d3-110">This section describes only how to allocate memory for parameters that are not passed by value — not pointers to interfaces, but more mundane things like strings, pointers to structures, and so forth.</span></span>

<span data-ttu-id="815d3-111">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="815d3-111">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="815d3-112">Die OLE-Speicherzuweisung</span><span class="sxs-lookup"><span data-stu-id="815d3-112">The OLE Memory Allocator</span></span>](the-ole-memory-allocator.md)
-   [<span data-ttu-id="815d3-113">Speicher Verwaltungsregeln</span><span class="sxs-lookup"><span data-stu-id="815d3-113">Memory Management Rules</span></span>](memory-management-rules.md)
-   [<span data-ttu-id="815d3-114">Debugging von Speicher Belegungen</span><span class="sxs-lookup"><span data-stu-id="815d3-114">Debugging Memory Allocations</span></span>](debugging-memory-allocations.md)

 

 