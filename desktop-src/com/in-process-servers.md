---
title: In-Process Server
description: In-Process Server
ms.assetid: cc0c4350-fa75-4321-834f-711158776cb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4886932b9669aa2d3cdd49979324f9ccc6e03d44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206719"
---
# <a name="in-process-servers"></a><span data-ttu-id="df1eb-103">In-Process Server</span><span class="sxs-lookup"><span data-stu-id="df1eb-103">In-Process Servers</span></span>

<span data-ttu-id="df1eb-104">Wenn Sie eine OLE-Serveranwendung als in-Process-Server implementieren – eine DLL, die im Prozessbereich der Containeranwendung ausgeführt wird – anstelle eines lokalen Servers – eine exe-Datei, die in einem eigenen Prozessbereich ausgeführt wird – die Kommunikation zwischen Container und Server wird vereinfacht, da die Kommunikation zwischen den beiden die Form normaler Funktionsaufrufe annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="df1eb-104">If you implement an OLE server application as an in-process server — a DLL running in the process space of the container application — rather than as a local server — an EXE running in its own process space — communication between container and server is simplified because communication between the two can take the form of normal function calls.</span></span> <span data-ttu-id="df1eb-105">Remote Prozedur Aufrufe sind nicht erforderlich, da die beiden Anwendungen im gleichen Prozessbereich ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="df1eb-105">Remote procedure calls are not required because the two applications run in the same process space.</span></span> <span data-ttu-id="df1eb-106">Erwartungsgemäß sind die Objekte, die das Marshalling von Parametern verwalten, ebenfalls unnötig, obwohl Sie möglicherweise innerhalb der dll aggregiert werden, ohne die Kommunikation zwischen Container und Server zu beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="df1eb-106">As you would expect, the objects that manage the marshaling of parameters are also unnecessary, although they may be aggregated within the DLL without interfering with the communication between container and server.</span></span>

<span data-ttu-id="df1eb-107">Wenn eine OLE-Serveranwendung als Prozess interner Server implementiert wird, ist ein separater Objekt Handler nicht erforderlich, da sich der Server selbst im Prozessbereich des Clients befindet.</span><span class="sxs-lookup"><span data-stu-id="df1eb-107">When an OLE server application is implemented as an in-process server, a separate object handler is not required because the server itself lives in the client's process space.</span></span> <span data-ttu-id="df1eb-108">Der Hauptunterschied zwischen einem in-Process-Server und einem Objekt Handler besteht darin, dass der Server das Objekt im Zustand "wird ausgeführt" verwalten kann, während der Handler dies nicht zulässt.</span><span class="sxs-lookup"><span data-stu-id="df1eb-108">The main difference between an in-process server and object handler is that the server is able to manage the object in a running state while the handler cannot.</span></span> <span data-ttu-id="df1eb-109">Eine Folge dieses Unterschieds besteht darin, dass ein Server eine Benutzeroberfläche für die Bearbeitung des laufenden Objekts bereitstellen muss, während ein Handler diese Anforderung an den Server des Objekts delegiert.</span><span class="sxs-lookup"><span data-stu-id="df1eb-109">One consequence of this difference is that a server must provide a user interface for manipulating the running object, while a handler delegates this requirement to the object's server.</span></span> <span data-ttu-id="df1eb-110">Beim Erstellen eines in-Process-Servers können Sie den OLE-Standard Handler aggregieren, sodass grundlegende Aufgaben wie Anzeige, Speicherung und Benachrichtigungen behandelt werden können, während Sie nur die Dienste implementieren, die der Handler entweder nicht bereitstellt oder nicht auf die gewünschte Weise implementiert.</span><span class="sxs-lookup"><span data-stu-id="df1eb-110">In creating an in-process server, you can aggregate on the OLE default handler, letting it handle basic chores, such as display, storage, and notifications while you implement only those services that the handler either does not provide or does not implement in the way you require.</span></span>

<span data-ttu-id="df1eb-111">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="df1eb-111">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="df1eb-112">Vorteile</span><span class="sxs-lookup"><span data-stu-id="df1eb-112">Advantages</span></span>](advantages.md)
-   [<span data-ttu-id="df1eb-113">Nachteile</span><span class="sxs-lookup"><span data-stu-id="df1eb-113">Disadvantages</span></span>](disadvantages.md)

## <a name="related-topics"></a><span data-ttu-id="df1eb-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="df1eb-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df1eb-115">Verbund Dokumente</span><span class="sxs-lookup"><span data-stu-id="df1eb-115">Compound Documents</span></span>](compound-documents.md)
</dt> </dl>

 

 




