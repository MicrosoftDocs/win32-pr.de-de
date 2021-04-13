---
title: Initialisieren von persistenten Objekten
description: Initialisieren von persistenten Objekten
ms.assetid: 790cf133-ce86-4d02-b177-a538b4ee3f8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 211d9d89b7a8f36ab06d9930e45f365e0fb5d4dc
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391058"
---
# <a name="initializing-persistent-objects"></a><span data-ttu-id="468e6-103">Initialisieren von persistenten Objekten</span><span class="sxs-lookup"><span data-stu-id="468e6-103">Initializing Persistent Objects</span></span>

<span data-ttu-id="468e6-104">Einige der persistenten Objekt Schnittstellen ( [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [ipersistmemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))und [IPersistPropertyBag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85))) ermöglichen Clients die Initialisierung von Objekten mit dem Zustand "neu" oder "Standard".</span><span class="sxs-lookup"><span data-stu-id="468e6-104">Several of the persistent object interfaces, [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [IPersistMemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), and [IPersistPropertyBag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85)), allow clients to initialize objects to a "fresh" or "default" state.</span></span> <span data-ttu-id="468e6-105">Dieser Anfangszustand unterscheidet sich von dem eines neu erstellten Objekts, das keinen Status aufweist.</span><span class="sxs-lookup"><span data-stu-id="468e6-105">This initial state is different from that of a newly created object, which has no state.</span></span>

<span data-ttu-id="468e6-106">Die Initialisierung des Zustands eines Objekts, auch im Standardzustand, kann ein Rechen intensiver oder ressourcenintensiver Vorgang sein.</span><span class="sxs-lookup"><span data-stu-id="468e6-106">Initializing an object's state, even to the default state, may be a compute-intensive or resource-intensive operation.</span></span> <span data-ttu-id="468e6-107">Durch die Trennung der Erstellung von der Initialisierung kann die Initialisierung nur ausgeführt werden, wenn Sie tatsächlich benötigt wird. Clients können die Initialisierung von Objekten nur im Standardzustand vermeiden, um zuvor gespeicherte Daten sofort zu laden.</span><span class="sxs-lookup"><span data-stu-id="468e6-107">By separating creation from initialization, the initialization can be performed only when it is actually needed and clients can avoid initializing objects to the default state only to immediately load previously stored data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="468e6-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="468e6-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="468e6-109">Persistente Objekt Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="468e6-109">Persistent Object Interfaces</span></span>](persistent-object-interfaces.md)
</dt> </dl>

 

 