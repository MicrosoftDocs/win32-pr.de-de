---
title: Persistentes Objektstatus
description: Persistentes Objektstatus
ms.assetid: 731fef03-d204-48e7-b33a-801e97a9d2c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c08d4dd1175b5a7681f79fa9049772af245a031
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309531"
---
# <a name="persistent-object-state"></a><span data-ttu-id="56429-103">Persistentes Objektstatus</span><span class="sxs-lookup"><span data-stu-id="56429-103">Persistent Object State</span></span>

<span data-ttu-id="56429-104">Einige COM-Objekte können Ihren internen Zustand speichern, wenn Sie von einem Client angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="56429-104">Some COM objects can save their internal state when asked to do so by a client.</span></span>

<span data-ttu-id="56429-105">COM definiert Standards, über die Clients anfordern können, dass Objekte initialisiert, geladen und in und aus einem Datenspeicher (z. b. Flatfile, strukturierter Speicher oder Arbeitsspeicher) gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="56429-105">COM defines standards through which clients can request objects to be initialized, loaded, and saved to and from a data store (for example, flat file, structured storage, or memory).</span></span> <span data-ttu-id="56429-106">Der Client ist dafür verantwortlich, den Speicherort zu verwalten, an dem die persistenten Daten des Objekts gespeichert werden, aber nicht das Format der Daten.</span><span class="sxs-lookup"><span data-stu-id="56429-106">It is the client's responsibility to manage the location where the object's persistent data is stored but not the format of the data.</span></span> <span data-ttu-id="56429-107">COM-Objekte, die diesen Standards entsprechen, werden als *persistente Objekte* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="56429-107">COM objects that adhere to these standards are called *persistent objects*.</span></span>

<span data-ttu-id="56429-108">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="56429-108">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="56429-109">Persistente Objekt Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="56429-109">Persistent Object Interfaces</span></span>](persistent-object-interfaces.md)
-   [<span data-ttu-id="56429-110">Initialisieren von persistenten Objekten</span><span class="sxs-lookup"><span data-stu-id="56429-110">Initializing Persistent Objects</span></span>](initializing-persistent-objects.md)

## <a name="related-topics"></a><span data-ttu-id="56429-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="56429-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56429-112">COM-Clients und-Server</span><span class="sxs-lookup"><span data-stu-id="56429-112">COM Clients and Servers</span></span>](com-clients-and-servers.md)
</dt> </dl>

 

 




