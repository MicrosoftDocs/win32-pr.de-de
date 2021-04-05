---
title: COM-Objekte und-Schnittstellen
description: COM-Objekte und-Schnittstellen
ms.assetid: a3b78086-0f02-4b3f-a856-46bfcf4457f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8c2b74f2b9741e41e7fe23226041f4c225bd85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707787"
---
# <a name="com-objects-and-interfaces"></a><span data-ttu-id="f7250-103">COM-Objekte und-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f7250-103">COM Objects and Interfaces</span></span>

<span data-ttu-id="f7250-104">COM ist eine Technologie, mit der Objekte innerhalb eines einzelnen Prozesses über Prozess-und Computer Grenzen hinweg interagieren können.</span><span class="sxs-lookup"><span data-stu-id="f7250-104">COM is a technology that allows objects to interact across process and computer boundaries as easily as within a single process.</span></span> <span data-ttu-id="f7250-105">COM ermöglicht dies durch Angabe, dass die einzige Möglichkeit zum Bearbeiten der einem Objekt zugeordneten Daten über eine *Schnittstelle* des Objekts ist.</span><span class="sxs-lookup"><span data-stu-id="f7250-105">COM enables this by specifying that the only way to manipulate the data associated with an object is through an *interface* on the object.</span></span> <span data-ttu-id="f7250-106">Wenn dieser Begriff in dieser Dokumentation verwendet wird, bezieht er sich auf eine Implementierung im Code einer Binär-kompatiblen com-Schnittstelle, die einem Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f7250-106">When this term is used in this documentation, it refers to an implementation in code of a COM binary-compliant interface that is associated with an object.</span></span>

<span data-ttu-id="f7250-107">COM verwendet die Word- *Schnittstelle* in einem anderen Sinne als das, das normalerweise in Visual C++ Programmierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f7250-107">COM uses the word *interface* in a sense different from that typically used in Visual C++ programming.</span></span> <span data-ttu-id="f7250-108">Eine C++-Schnittstelle bezieht sich auf alle Funktionen, die von einer Klasse unterstützt werden, und die Clients eines Objekts können aufzurufen, um mit ihm zu interagieren.</span><span class="sxs-lookup"><span data-stu-id="f7250-108">A C++ interface refers to all of the functions that a class supports and that clients of an object can call to interact with it.</span></span> <span data-ttu-id="f7250-109">Eine COM-Schnittstelle verweist auf eine vordefinierte Gruppe verwandter Funktionen, die eine COM-Klasse implementiert, aber eine bestimmte Schnittstelle stellt nicht notwendigerweise alle Funktionen dar, die von der Klasse unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="f7250-109">A COM interface refers to a predefined group of related functions that a COM class implements, but a specific interface does not necessarily represent all the functions that the class supports.</span></span>

<span data-ttu-id="f7250-110">Das verweisen auf ein *Objekt,* das eine-Schnittstelle implementiert, bedeutet, dass das-Objektcode verwendet, der jede Methode der Schnittstelle implementiert und com-Binär-kompatible Zeiger auf diese Funktionen der com-Bibliothek bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="f7250-110">Referring to an object *implementing* an interface means that the object uses code that implements each method of the interface and provides COM binary-compliant pointers to those functions to the COM library.</span></span> <span data-ttu-id="f7250-111">COM stellt diese Funktionen dann jedem Client zur Verfügung, der einen Zeiger auf die-Schnittstelle anfordert, unabhängig davon, ob sich der Client innerhalb oder außerhalb des Prozesses befindet, der diese Funktionen implementiert.</span><span class="sxs-lookup"><span data-stu-id="f7250-111">COM then makes those functions available to any client who asks for a pointer to the interface, whether the client is inside or outside of the process that implements those functions.</span></span>

<span data-ttu-id="f7250-112">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="f7250-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="f7250-113">Schnittstellen und Schnittstellen Implementierungen</span><span class="sxs-lookup"><span data-stu-id="f7250-113">Interfaces and Interface Implementations</span></span>](interfaces-and-interface-implementations.md)
-   [<span data-ttu-id="f7250-114">Interface Pointers and Interfaces (Schnittstellenzeiger und Schnittstellen)</span><span class="sxs-lookup"><span data-stu-id="f7250-114">Interface Pointers and Interfaces</span></span>](interface-pointers-and-interfaces.md)
-   [<span data-ttu-id="f7250-115">IUnknown und Schnittstellen Vererbung</span><span class="sxs-lookup"><span data-stu-id="f7250-115">IUnknown and Interface Inheritance</span></span>](iunknown-and-interface-inheritance.md)

## <a name="related-topics"></a><span data-ttu-id="f7250-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f7250-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7250-117">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f7250-117">Interfaces</span></span>](interfaces.md)
</dt> </dl>

 

 




