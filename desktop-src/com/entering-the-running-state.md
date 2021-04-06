---
title: Eingeben des Status "wird ausgeführt"
description: Eingeben des Status "wird ausgeführt"
ms.assetid: 2173eaa9-0e60-4411-81e4-dbabc5fe89b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 959038c8f64fe8750ab1bcf0f06b753371f04136
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947655"
---
# <a name="entering-the-running-state"></a><span data-ttu-id="78f4b-103">Eingeben des Status "wird ausgeführt"</span><span class="sxs-lookup"><span data-stu-id="78f4b-103">Entering the Running State</span></span>

<span data-ttu-id="78f4b-104">Wenn ein eingebettetes Objekt den Übergang in den Status "wird ausgeführt" durchführt, muss der Objekt Handler die Serveranwendung suchen und ausführen, um die Dienste zu nutzen, die nur der Server bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="78f4b-104">When an embedded object makes the transition to the running state, the object handler must locate and run the server application in order to utilize the services that only the server provides.</span></span> <span data-ttu-id="78f4b-105">Eingebettete Objekte werden entweder explizit durch eine Anforderung durch den Container in den Zustand wird ausgeführt versetzt, z. b. das Zeichnen eines Formats, das derzeit nicht zwischengespeichert ist, oder implizit durch OLE als Reaktion auf das Aufrufen eines Vorgangs, z. b. Wenn ein Benutzer des Containers auf das Objekt doppelklickt.</span><span class="sxs-lookup"><span data-stu-id="78f4b-105">Embedded objects are placed in the running state either explicitly through a request by the container, such as a need to draw a format not currently cached, or implicitly by OLE in response to invoking some operation, such as when a user of the container double-clicks the object.</span></span>

<span data-ttu-id="78f4b-106">Wenn ein verknüpftes Objekt den Übergang in den Status "wird ausgeführt" versetzt, wird der Prozess als *Bindung* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="78f4b-106">When a linked object makes the transition into the running state, the process is known as *binding*.</span></span> <span data-ttu-id="78f4b-107">Beim Bindungs Vorgang fragt der Objekt Handler seinen gespeicherten Moniker ab, um die Daten des Links zu finden, und führt dann die Serveranwendung aus.</span><span class="sxs-lookup"><span data-stu-id="78f4b-107">In the process of binding, the object handler asks its stored moniker to locate the link's data, then runs the server application.</span></span>

<span data-ttu-id="78f4b-108">Auf den ersten Blick scheint das Binden eines verknüpften Objekts nicht komplizierter als das Ausführen eines eingebetteten Objekts zu sein.</span><span class="sxs-lookup"><span data-stu-id="78f4b-108">At first glance, binding a linked object appears to be no more complicated than running an embedded object.</span></span> <span data-ttu-id="78f4b-109">Die folgenden Punkte erschweren jedoch den Prozess:</span><span class="sxs-lookup"><span data-stu-id="78f4b-109">However, the following points complicate the process:</span></span>

-   <span data-ttu-id="78f4b-110">Ein Link kann auf ein Objekt oder einen Teil davon verweisen, das in einen anderen Container eingebettet ist.</span><span class="sxs-lookup"><span data-stu-id="78f4b-110">A link can refer to an object, or a portion thereof, that is embedded in another container.</span></span> <span data-ttu-id="78f4b-111">Diese Funktion impliziert ein Potenzial für eingefügte Einbettungen.</span><span class="sxs-lookup"><span data-stu-id="78f4b-111">This capability implies a potential for nested embeddings.</span></span> <span data-ttu-id="78f4b-112">Das Auflösen von Verweisen auf eine solche Hierarchie erfordert rekursiv durchlaufen eines zusammen *gesetzten Monikers*, beginnend mit dem äußersten rechten Member.</span><span class="sxs-lookup"><span data-stu-id="78f4b-112">Resolving references to such a hierarchy requires recursively traversing a *composite moniker*, beginning with the rightmost member.</span></span>
-   <span data-ttu-id="78f4b-113">Wenn die Verknüpfungs Quelle ausgeführt wird, bindet OLE an die laufende Instanz des Objekts, anstatt eine andere Instanz zu betreiben.</span><span class="sxs-lookup"><span data-stu-id="78f4b-113">When the link source is running, OLE binds to the running instance of the object rather than running another instance.</span></span> <span data-ttu-id="78f4b-114">Im Fall von in einer Tabelle eingebetteten eingebetteten Objekten, von denen eine die Verknüpfungs Quelle ist, muss OLE an einem beliebigen Punkt an ein bereits laufendes Objekt gebunden werden können.</span><span class="sxs-lookup"><span data-stu-id="78f4b-114">In the case of nested embedded objects, one of which is the link source, OLE must be able to bind to an already running object at any point.</span></span>
-   <span data-ttu-id="78f4b-115">Das Ausführen eines Objekts erfordert den Zugriff auf den Speicherbereich für das Objekt.</span><span class="sxs-lookup"><span data-stu-id="78f4b-115">Running an object requires accessing the storage area for the object.</span></span> <span data-ttu-id="78f4b-116">Wenn ein eingebettetes Objekt ausgeführt wird, empfängt OLE einen Zeiger auf den Speicher während des Ladevorgangs, der an die OLE-Serveranwendung weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="78f4b-116">When an embedded object is run, OLE receives a pointer to the storage during the load process, which it passes on to the OLE server application.</span></span> <span data-ttu-id="78f4b-117">Für verknüpfte Objekte gibt es jedoch keine Standardschnittstelle für den Zugriff auf den Speicher.</span><span class="sxs-lookup"><span data-stu-id="78f4b-117">For linked objects, however, there is no standard interface for accessing storage.</span></span> <span data-ttu-id="78f4b-118">Die OLE Server-Anwendung kann die Dateisystem Schnittstelle oder einen anderen Mechanismus verwenden.</span><span class="sxs-lookup"><span data-stu-id="78f4b-118">The OLE server application may use the file system interface or some other mechanism.</span></span>

 

 




