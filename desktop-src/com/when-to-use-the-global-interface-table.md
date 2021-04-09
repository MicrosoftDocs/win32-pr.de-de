---
title: Verwendungszwecke der globalen Schnittstellen Tabelle
description: Verwendungszwecke der globalen Schnittstellen Tabelle
ms.assetid: def8f7f8-9d0d-49a4-9d5c-40233903eea5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f89bbd7437b65c85abe89e8d647cbd73555c2d6a
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039651"
---
# <a name="when-to-use-the-global-interface-table"></a><span data-ttu-id="ba27c-103">Verwendungszwecke der globalen Schnittstellen Tabelle</span><span class="sxs-lookup"><span data-stu-id="ba27c-103">When to Use the Global Interface Table</span></span>

<span data-ttu-id="ba27c-104">Wenn Sie einen Schnittstellen Zeiger mehrmals zwischen den Apartments in einem Prozess wieder verwenden, können Sie die [**iglobalinterfaketable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) -Schnittstelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="ba27c-104">If you are unmarshaling an interface pointer multiple times between apartments in a process, you might use the [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) interface.</span></span> <span data-ttu-id="ba27c-105">Bei anderen Techniken müssten Sie jedes Mal einen erneuten Mars Hall durchsetzen.</span><span class="sxs-lookup"><span data-stu-id="ba27c-105">With other techniques, you would have to remarshal each time.</span></span>

> [!Note]  
> <span data-ttu-id="ba27c-106">Wenn der Schnittstellen Zeiger nur einmal gemarshallt wird, können Sie die [**comarshalinterthreadinterfakeinstream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="ba27c-106">If the interface pointer is unmarshaled only once, you may want to use the [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) function.</span></span> <span data-ttu-id="ba27c-107">Sie kann auch verwendet werden, um einen Schnittstellen Zeiger von einem Thread an einen anderen Thread im gleichen Prozess zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="ba27c-107">It can also be used to pass an interface pointer from one thread to another thread in the same process.</span></span>

 

<span data-ttu-id="ba27c-108">Die [**iglobalinterfaketable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) -Schnittstelle macht auch ein anderes, bisher schwieriges Problem für den Programmierer einfacher.</span><span class="sxs-lookup"><span data-stu-id="ba27c-108">The [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) interface also makes another previously difficult problem simpler for the programmer.</span></span> <span data-ttu-id="ba27c-109">Dieses Problem tritt auf, wenn die folgenden Bedingungen zutreffen:</span><span class="sxs-lookup"><span data-stu-id="ba27c-109">This problem occurs when the following conditions apply:</span></span>

-   <span data-ttu-id="ba27c-110">Ein in-Process-Agile-Objekt aggregiert den frei Thread-Mars Haller.</span><span class="sxs-lookup"><span data-stu-id="ba27c-110">An in-process agile object aggregates the free-threaded marshaler.</span></span>
-   <span data-ttu-id="ba27c-111">Das gleiche Agile-Objekt enthält auch (als Element Variablen) Schnittstellen Zeiger auf andere Objekte, die nicht agil sind und den Freethread-Mars Haller nicht aggregieren.</span><span class="sxs-lookup"><span data-stu-id="ba27c-111">This same agile object also holds (as member variables) interface pointers to other objects that are not agile and do not aggregate the free-threaded marshaler.</span></span>

<span data-ttu-id="ba27c-112">Wenn das äußere Objekt in diesem Fall an ein anderes Apartment gemarshallt wird und die Anwendung darauf aufruft, und das Objekt versucht, für einen seiner Member-Variablen Schnittstellen Zeiger aufzurufen, die nicht frei Thread sind oder für Objekte in anderen Apartments Proxys sind, erhalten Sie möglicherweise falsche Ergebnisse oder den falschen RPC-Fehler \_ \_ \_ Thread.</span><span class="sxs-lookup"><span data-stu-id="ba27c-112">In this situation, if the outer object gets marshaled to another apartment and the application calls on it, and the object tries to call on any of its member variable interface pointers that are not free-threaded or are proxies to objects in other apartments, it might get incorrect results or the error RPC\_E\_WRONG\_THREAD.</span></span> <span data-ttu-id="ba27c-113">Dieser Fehler tritt auf, weil die innere Schnittstelle nur von dem Apartment aus aufgerufen werden kann, in dem Sie zuerst in der Element Variablen gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="ba27c-113">This error occurs because the inner interface is designed to be callable only from the apartment in which it was first stored in the member variable.</span></span>

<span data-ttu-id="ba27c-114">Um dieses Problem zu beheben, sollte das äußere Objekt, das den Freethread-Mars Haller aggregiert, [**iglobalinterfaketable:: registerinterfakeinglobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) auf der inneren Schnittstelle aufrufen und das resultierende Cookie in seiner Member-Variablen speichern, anstatt den eigentlichen Schnittstellen Zeiger zu speichern.</span><span class="sxs-lookup"><span data-stu-id="ba27c-114">To solve this problem, the outer object aggregating the free-threaded marshaler should call [**IGlobalInterfaceTable::RegisterInterfaceInGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) on the inner interface and store the resulting cookie in its member variable, instead of storing the actual interface pointer.</span></span> <span data-ttu-id="ba27c-115">Wenn das äußere Objekt für den Schnittstellen Zeiger eines inneren Objekts aufrufen möchte, sollte es [**iglobalinterfaketable:: getinterfakefromglobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal)aufrufen, den zurückgegebenen Schnittstellen Zeiger verwenden und es dann freigeben.</span><span class="sxs-lookup"><span data-stu-id="ba27c-115">When the outer object wants to call on an inner object's interface pointer, it should call [**IGlobalInterfaceTable::GetInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal), use the returned interface pointer, and then release it.</span></span> <span data-ttu-id="ba27c-116">Wenn das äußere Objekt entfernt wird, sollte es [**iglobalinterfaketable:: revokeinterfakefromglobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) aufgerufen werden, um die Schnittstelle aus der globalen Schnittstellen Tabelle zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="ba27c-116">When the outer object goes away, it should call [**IGlobalInterfaceTable::RevokeInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) to remove the interface from the global interface table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba27c-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ba27c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba27c-118">Erstellen der globalen Schnittstellen Tabelle</span><span class="sxs-lookup"><span data-stu-id="ba27c-118">Creating the Global Interface Table</span></span>](creating-the-global-interface-table.md)
</dt> </dl>

 

 