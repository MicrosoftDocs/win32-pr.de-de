---
title: Einschluss/Delegierung
description: Der häufigste Mechanismus für die Wiederverwendung von Objekten in com ist die Kapselung/Delegierung.
ms.assetid: 56396c11-889a-4f28-8fa7-9e48c805c501
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d26e0c1d1e48596cb9acef740405c797f6f0f46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311297"
---
# <a name="containmentdelegation"></a><span data-ttu-id="6102a-103">Einschluss/Delegierung</span><span class="sxs-lookup"><span data-stu-id="6102a-103">Containment/Delegation</span></span>

<span data-ttu-id="6102a-104">Der häufigste Mechanismus für die Wiederverwendung von Objekten in com ist die Kapselung */Delegierung*.</span><span class="sxs-lookup"><span data-stu-id="6102a-104">The most common mechanism for object reuse in COM is *containment/delegation*.</span></span> <span data-ttu-id="6102a-105">Diese Art der Wiederverwendung ist ein bekanntes Konzept, das in den meisten objektorientierten Sprachen und Systemen enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="6102a-105">This type of reuse is a familiar concept found in most object-oriented languages and systems.</span></span> <span data-ttu-id="6102a-106">Das äußere Objekt, das das innere Objekt verwenden muss, fungiert als Objekt Client für das innere Objekt.</span><span class="sxs-lookup"><span data-stu-id="6102a-106">The outer object, which needs to make use of the inner object, acts as an object client to the inner object.</span></span> <span data-ttu-id="6102a-107">Das äußere Objekt "enthält" das innere Objekt, und wenn das äußere Objekt die Dienste des inneren Objekts erfordert, delegiert das äußere Objekt die Implementierung explizit an die Methoden des inneren Objekts.</span><span class="sxs-lookup"><span data-stu-id="6102a-107">The outer object "contains" the inner object, and when the outer object requires the services of the inner object, the outer object explicitly delegates implementation to the inner object's methods.</span></span> <span data-ttu-id="6102a-108">Das heißt, das äußere Objekt verwendet die Dienste des inneren Objekts, um sich selbst zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="6102a-108">That is, the outer object uses the inner object's services to implement itself.</span></span>

<span data-ttu-id="6102a-109">Es ist nicht erforderlich, dass die äußeren und inneren Objekte die gleichen Schnittstellen unterstützen, obwohl es sicherlich sinnvoll ist, ein Objekt zu enthalten, das eine Schnittstelle implementiert, die das äußere Objekt nicht implementiert, und die Methoden des äußeren Objekts einfach als Aufrufe der entsprechenden Methoden im inneren Objekt implementiert.</span><span class="sxs-lookup"><span data-stu-id="6102a-109">It is not necessary for the outer and inner objects to support the same interfaces, although it certainly is reasonable to contain an object that implements an interface that the outer object does not and implement the methods of the outer object simply as calls to the corresponding methods in the inner object.</span></span> <span data-ttu-id="6102a-110">Wenn die Komplexität der äußeren und inneren Objekte stark abweicht, kann das äußere Objekt jedoch einige der Methoden der Schnittstellen implementieren, indem Aufrufe an Schnittstellen Methoden delegiert werden, die im inneren Objekt implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="6102a-110">When the complexity of the outer and inner objects differs greatly, however, the outer object may implement some of the methods of its interfaces by delegating calls to interface methods implemented in the inner object.</span></span>

<span data-ttu-id="6102a-111">Es ist einfach, die Kapselung für ein äußeres Objekt zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="6102a-111">It is simple to implement containment for an outer object.</span></span> <span data-ttu-id="6102a-112">Das äußere Objekt erstellt die inneren Objekte, die es für jeden anderen Client verwenden muss.</span><span class="sxs-lookup"><span data-stu-id="6102a-112">The outer object creates the inner objects it needs to use as any other client would.</span></span> <span data-ttu-id="6102a-113">Das ist nichts neues – der Prozess ähnelt einem C++-Objekt, das ein C++-Zeichen folgen Objekt enthält, das für die Ausführung bestimmter Zeichen folgen Funktionen verwendet wird. Dies gilt auch, wenn das äußere Objekt nicht als eigenes Zeichen folgen Objekt betrachtet wird.</span><span class="sxs-lookup"><span data-stu-id="6102a-113">This is nothing new—the process is like a C++ object that itself contains a C++ string object that it uses to perform certain string functions, even if the outer object is not considered a string object in its own right.</span></span> <span data-ttu-id="6102a-114">Wenn Sie dann den Zeiger auf das innere Objekt verwenden, generiert ein aufrufungs Methode im äußeren Objekt einen aufzurufenden inneren Objektmethode.</span><span class="sxs-lookup"><span data-stu-id="6102a-114">Then, using its pointer to the inner object, a call to a method in the outer object generates a call to an inner object method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6102a-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6102a-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6102a-116">Aggregation</span><span class="sxs-lookup"><span data-stu-id="6102a-116">Aggregation</span></span>](aggregation.md)
</dt> </dl>

 

 




