---
title: Monikeranbieter
description: Monikeranbieter
ms.assetid: 4d4820d2-bf5f-4543-b318-59481dcc51de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde584e12daddacbc940b23b21a0386aa37de2c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710350"
---
# <a name="moniker-providers"></a><span data-ttu-id="f98f5-103">Monikeranbieter</span><span class="sxs-lookup"><span data-stu-id="f98f5-103">Moniker Providers</span></span>

<span data-ttu-id="f98f5-104">Im Allgemeinen sollte eine Komponente ein monikeranbieter sein, wenn Sie den Zugriff auf eines ihrer Objekte zulässt, während der Speicher des Objekts weiterhin gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="f98f5-104">In general, a component should be a moniker provider when it allows access to one of its objects, while still controlling the object's storage.</span></span> <span data-ttu-id="f98f5-105">Wenn eine Komponente Moniker weitergibt, die ihre Objekte identifizieren, muss Sie in der Lage sein, die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="f98f5-105">If a component is going to hand out monikers that identify its objects, it must be capable of performing the following tasks:</span></span>

-   <span data-ttu-id="f98f5-106">Erstellen Sie bei der Anforderung einen Moniker, der ein Objekt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f98f5-106">On request, create a moniker that identifies an object.</span></span>
-   <span data-ttu-id="f98f5-107">Aktivieren Sie den Moniker, der gebunden werden soll, wenn ein Client [**IMoniker:: bindjeobject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) darauf aufruft.</span><span class="sxs-lookup"><span data-stu-id="f98f5-107">Enable the moniker to be bound when a client calls [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) on it.</span></span>

<span data-ttu-id="f98f5-108">Ein monikeranbieter muss einen Moniker einer entsprechenden *Monikerklasse* erstellen, um ein Objekt zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f98f5-108">A moniker provider must create a moniker of an appropriate *moniker class* to identify an object.</span></span> <span data-ttu-id="f98f5-109">Die Monikerklasse verweist auf eine bestimmte Implementierung der [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) -Schnittstelle, die den Typ des erstellten Monikers definiert.</span><span class="sxs-lookup"><span data-stu-id="f98f5-109">The moniker class refers to a specific implementation of the [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) interface that defines the type of moniker created.</span></span> <span data-ttu-id="f98f5-110">Obwohl Sie **IMoniker** implementieren können, um eine neue Monikerklasse zu erstellen, ist dies häufig unnötig, da OLE Implementierungen mehrerer unterschiedlicher Moniker-Klassen bereitstellt, die jeweils über eine eigene CLSID verfügen.</span><span class="sxs-lookup"><span data-stu-id="f98f5-110">While you can implement **IMoniker** to create a new moniker class, it is frequently unnecessary because OLE provides implementations of several different moniker classes, each with its own CLSID.</span></span> <span data-ttu-id="f98f5-111">Unter [OLE-Monikerimplementierungen](ole-moniker-implementations.md) finden Sie Beschreibungen der Monikerklassen, die von OLE bereitstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f98f5-111">See [OLE Moniker Implementations](ole-moniker-implementations.md) for descriptions of moniker classes that OLE provides.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f98f5-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f98f5-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f98f5-113">Monikerclients</span><span class="sxs-lookup"><span data-stu-id="f98f5-113">Moniker Clients</span></span>](moniker-clients.md)
</dt> <dt>

[<span data-ttu-id="f98f5-114">OLE-Monikerimplementierungen</span><span class="sxs-lookup"><span data-stu-id="f98f5-114">OLE Moniker Implementations</span></span>](ole-moniker-implementations.md)
</dt> </dl>

 

 




