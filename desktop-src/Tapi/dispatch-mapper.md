---
description: Der dispatchmapper wird mit com cokreateinstance erstellt und macht eine Schnittstelle, itdispatchmapper, verfügbar.
ms.assetid: 435034e1-d90c-4bad-8758-8a627d88875f
title: Dispatchzuordnung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ed0a3a6cbc906861f5e95694bfd75aec6f5791f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349208"
---
# <a name="dispatch-mapper"></a><span data-ttu-id="e38fc-103">Dispatchzuordnung</span><span class="sxs-lookup"><span data-stu-id="e38fc-103">Dispatch Mapper</span></span>

<span data-ttu-id="e38fc-104">Der dispatchmapper wird mit com **cokreateinstance** erstellt und macht eine Schnittstelle, [**itdispatchmapper**](/windows/desktop/api/tapi3if/nn-tapi3if-itdispatchmapper), verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e38fc-104">The Dispatch Mapper is created using COM **CoCreateInstance** and exposes one interface, [**ITDispatchMapper**](/windows/desktop/api/tapi3if/nn-tapi3if-itdispatchmapper).</span></span> <span data-ttu-id="e38fc-105">Diese Schnittstelle ermöglicht es einer Anwendung, den Dispatch-Zeiger einer anderen Schnittstelle für ein Objekt abzurufen, wenn der Dispatch-Zeiger einer Schnittstelle und die GUID eines anderen Objekts ist.</span><span class="sxs-lookup"><span data-stu-id="e38fc-105">This interface allows an application to retrieve the dispatch pointer of another interface on an object, given the dispatch pointer of one interface and the GUID of another.</span></span> <span data-ttu-id="e38fc-106">Diese Schnittstelle wird bereitgestellt, um Programmierer bei der Verwendung von Skript Anwendungen zu unterstützen, die keine Möglichkeit bieten, die Schnittstellen eines Objekts schnell abzufragen.</span><span class="sxs-lookup"><span data-stu-id="e38fc-106">This interface is provided to assist programmers using scripting applications which do not provide a means of readily polling the interfaces on an object.</span></span>

<span data-ttu-id="e38fc-107">Der dispatchmapper verwendet die **iobjecgs** -Schnittstelle eines Objekts, um sicherzustellen, dass das Objekt für die Skripterstellung auf der angeforderten Schnittstelle sicher ist.</span><span class="sxs-lookup"><span data-stu-id="e38fc-107">The Dispatch Mapper uses an object's **IObjectSafety** interface to make sure the object is safe for scripting on the requested interface.</span></span> <span data-ttu-id="e38fc-108">Wenn das Objekt **iobjeczafety** nicht implementiert, oder wenn das Objekt an dieser speziellen Schnittstelle nicht sicher ist, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="e38fc-108">If the object does not implement **IObjectSafety**, or if the object is not safe on this particular interface, the call will fail.</span></span>

 

 



