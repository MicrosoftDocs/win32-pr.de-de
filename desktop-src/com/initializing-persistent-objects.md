---
title: Initialisieren persistenter Objekte
description: Initialisieren persistenter Objekte
ms.assetid: 790cf133-ce86-4d02-b177-a538b4ee3f8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e29bcb32bc049b5e0d5c2dab13e5ded6a743957e
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549196"
---
# <a name="initializing-persistent-objects"></a><span data-ttu-id="9e50f-103">Initialisieren persistenter Objekte</span><span class="sxs-lookup"><span data-stu-id="9e50f-103">Initializing Persistent Objects</span></span>

<span data-ttu-id="9e50f-104">Einige der persistenten [**Objektschnittstellen, IPersistStreamInit,**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) [**IPersistStorage,**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage) [IPersistMemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))und [IPersistPropertyBag,](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag)ermöglichen Clients das Initialisieren von Objekten in einen "fresh"- oder "default"-Zustand.</span><span class="sxs-lookup"><span data-stu-id="9e50f-104">Several of the persistent object interfaces, [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [IPersistMemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), and [IPersistPropertyBag](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag), allow clients to initialize objects to a "fresh" or "default" state.</span></span> <span data-ttu-id="9e50f-105">Dieser Anfangszustand ist anders als bei einem neu erstellten Objekt, das keinen Zustand auf hat.</span><span class="sxs-lookup"><span data-stu-id="9e50f-105">This initial state is different from that of a newly created object, which has no state.</span></span>

<span data-ttu-id="9e50f-106">Das Initialisieren des Zustands eines Objekts, selbst in den Standardzustand, kann ein rechen- oder ressourcenintensiver Vorgang sein.</span><span class="sxs-lookup"><span data-stu-id="9e50f-106">Initializing an object's state, even to the default state, may be a compute-intensive or resource-intensive operation.</span></span> <span data-ttu-id="9e50f-107">Durch die Trennung der Erstellung von der Initialisierung kann die Initialisierung nur ausgeführt werden, wenn sie tatsächlich benötigt wird, und Clients können das Initialisieren von Objekten in den Standardzustand vermeiden, um zuvor gespeicherte Daten sofort zu laden.</span><span class="sxs-lookup"><span data-stu-id="9e50f-107">By separating creation from initialization, the initialization can be performed only when it is actually needed and clients can avoid initializing objects to the default state only to immediately load previously stored data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e50f-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9e50f-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e50f-109">Persistente Objektschnittstellen</span><span class="sxs-lookup"><span data-stu-id="9e50f-109">Persistent Object Interfaces</span></span>](persistent-object-interfaces.md)
</dt> </dl>

 

 