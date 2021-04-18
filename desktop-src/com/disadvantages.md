---
title: Nachteile
description: Nachteile
ms.assetid: ce6885d9-7056-42bc-85d1-27ce32b1be5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a22e409414a1df60e2dd9dff3adbfc6000b953a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516005"
---
# <a name="disadvantages"></a><span data-ttu-id="e59a7-103">Nachteile</span><span class="sxs-lookup"><span data-stu-id="e59a7-103">Disadvantages</span></span>

<span data-ttu-id="e59a7-104">In-Process-Server bieten den Vorteil der Geschwindigkeit und Größe eines Objekt Handlers mit der Bearbeitungsfunktion eines lokalen Servers.</span><span class="sxs-lookup"><span data-stu-id="e59a7-104">In-process servers provide the speed and size advantage of an object handler with the editing capability of a local server.</span></span> <span data-ttu-id="e59a7-105">Warum sollten Sie sich also entscheiden, Ihre OLE-Anwendung als lokalen Server und nicht als Prozess interner Server zu implementieren?</span><span class="sxs-lookup"><span data-stu-id="e59a7-105">So why would you ever choose to implement your OLE application as a local server rather than an in-process server?</span></span> <span data-ttu-id="e59a7-106">Es gibt mehrere Gründe:</span><span class="sxs-lookup"><span data-stu-id="e59a7-106">There are several reasons:</span></span>

-   <span data-ttu-id="e59a7-107">Sicherheit.</span><span class="sxs-lookup"><span data-stu-id="e59a7-107">Security.</span></span> <span data-ttu-id="e59a7-108">Nur ein lokaler Server hat seinen Adressraum isoliert von dem des Clients.</span><span class="sxs-lookup"><span data-stu-id="e59a7-108">Only a local server has its address space isolated from that of the client.</span></span> <span data-ttu-id="e59a7-109">Ein Prozess interner Server nutzt den Adressraum und den Prozess Kontext des Clients und kann daher bei Fehlern oder böswilliger Programmierung weniger robust sein.</span><span class="sxs-lookup"><span data-stu-id="e59a7-109">An in-process server shares the address space and process context of the client and can therefore be less robust in the face of faults or malicious programming.</span></span>
-   <span data-ttu-id="e59a7-110">Granularität.</span><span class="sxs-lookup"><span data-stu-id="e59a7-110">Granularity.</span></span> <span data-ttu-id="e59a7-111">Ein lokaler Server kann mehrere Instanzen seines Objekts über viele verschiedene Clients hinweg hosten, wobei der Serverstatus zwischen Objekten in mehreren Clients auf eine Weise freigegeben werden kann, die schwierig oder unmöglich wäre, wenn er als Prozess interner Server implementiert wird. dabei handelt es sich einfach um eine DLL, die in jeden Client geladen wird.</span><span class="sxs-lookup"><span data-stu-id="e59a7-111">A local server can host multiple instances of its object across many different clients, sharing server state between objects in multiple clients in ways that would be difficult or impossible if implemented as an in-process server, which is simply a DLL loaded into each client.</span></span>
-   <span data-ttu-id="e59a7-112">Kompatibilität.</span><span class="sxs-lookup"><span data-stu-id="e59a7-112">Compatibility.</span></span> <span data-ttu-id="e59a7-113">Wenn Sie sich für die Implementierung eines in-Process-Servers entscheiden, wird die Kompatibilität mit OLE 1 aufgegeben, das solche Server nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e59a7-113">If you choose to implement an in-process server, you relinquish compatibility with OLE 1, which does not support such servers.</span></span> <span data-ttu-id="e59a7-114">Dies ist für viele Entwickler nicht zu berücksichtigen, aber wenn dies der Fall ist, ist es von entscheidender Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="e59a7-114">This will not be a consideration for many developers, but if it is, then it is of critical concern.</span></span>
-   <span data-ttu-id="e59a7-115">Keine Unterstützung von Links.</span><span class="sxs-lookup"><span data-stu-id="e59a7-115">Inability to support links.</span></span> <span data-ttu-id="e59a7-116">Ein Prozess interner Server kann nicht als Verknüpfungs Quelle fungieren.</span><span class="sxs-lookup"><span data-stu-id="e59a7-116">An in-process server cannot serve as a link source.</span></span> <span data-ttu-id="e59a7-117">Da eine DLL nicht eigenständig ausgeführt werden kann, kann Sie kein Datei Objekt erstellen, mit dem eine Verknüpfung erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="e59a7-117">Since a DLL cannot run by itself, it cannot create a file object to be linked to.</span></span>

<span data-ttu-id="e59a7-118">Trotz dieser Nachteile kann ein Prozess interner Server eine hervorragende Wahl für seine Geschwindigkeit und Größe sein – wenn er alle Ihre anderen Anforderungen erfüllt.</span><span class="sxs-lookup"><span data-stu-id="e59a7-118">Despite these disadvantages, an in-process server can be an excellent choice for its speed and size — if it fits all your other requirements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e59a7-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e59a7-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e59a7-120">Vorteile</span><span class="sxs-lookup"><span data-stu-id="e59a7-120">Advantages</span></span>](advantages.md)
</dt> <dt>

[<span data-ttu-id="e59a7-121">Prozess interne Server</span><span class="sxs-lookup"><span data-stu-id="e59a7-121">In-Process Servers</span></span>](in-process-servers.md)
</dt> </dl>

 

 




