---
title: Objekt Handler
description: Objekt Handler
ms.assetid: a5b51e07-246d-42a2-b33f-2bd0c608f41a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7294ddd48d2acaa010ad15c0e2497fd33c7f071
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855644"
---
# <a name="object-handlers"></a><span data-ttu-id="5ef1b-103">Objekt Handler</span><span class="sxs-lookup"><span data-stu-id="5ef1b-103">Object Handlers</span></span>

<span data-ttu-id="5ef1b-104">Wenn eine OLE-Serveranwendung ein lokaler Server ist, was bedeutet, dass Sie in einem eigenen Prozessbereich ausgeführt wird, muss die Kommunikation zwischen Container und Server über Prozess Grenzen hinweg erfolgen.</span><span class="sxs-lookup"><span data-stu-id="5ef1b-104">If an OLE server application is a local server, meaning that it runs in its own process space, communication between container and server must occur across process boundaries.</span></span> <span data-ttu-id="5ef1b-105">Da dieser Prozess teuer ist, verwendet OLE ein Ersatzobjekt, das in den Prozessbereich des Containers geladen wird, um im Auftrag einer lokalen Serveranwendung zu agieren.</span><span class="sxs-lookup"><span data-stu-id="5ef1b-105">Because this process is expensive, OLE relies on a surrogate object loaded into the container's process space to act on behalf of a local server application.</span></span> <span data-ttu-id="5ef1b-106">Dieses Ersatzobjekt, das als *Objekt Handler* bezeichnet wird, verarbeitet Container Anforderungen, die keine Aufmerksamkeit der Serveranwendung erfordern, wie z. b. das Zeichnen von Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="5ef1b-106">This surrogate object, known as an *object handler*, services container requests that do not require the attention of the server application, such as requests for drawing.</span></span> <span data-ttu-id="5ef1b-107">Wenn ein Container etwas anfordert, das der Objekt Handler nicht bereitstellen kann, kommuniziert der Handler mit der Serveranwendung mithilfe des Out-of-Process-Kommunikationsmechanismus von com.</span><span class="sxs-lookup"><span data-stu-id="5ef1b-107">When a container requests something that the object handler cannot provide, the handler communicates with the server application using COM's out-of-process communication mechanism.</span></span>

<span data-ttu-id="5ef1b-108">Ein Objekt Handler ist für eine Objektklasse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="5ef1b-108">An object handler is unique to an object class.</span></span> <span data-ttu-id="5ef1b-109">Wenn Sie eine Instanz eines Handlers für eine Klasse erstellen, können Sie Sie nicht für eine andere Klasse verwenden.</span><span class="sxs-lookup"><span data-stu-id="5ef1b-109">When you create an instance of a handler for one class, you cannot use it for another.</span></span> <span data-ttu-id="5ef1b-110">Bei Verwendung für ein zusammengesetztes Dokument implementiert der Objekt Handler die Container seitigen Datenstrukturen, wenn auf Objekte einer bestimmten Klasse Remote zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="5ef1b-110">When used for a compound document, the object handler implements the container-side data structures when objects of a particular class are accessed remotely.</span></span>

<span data-ttu-id="5ef1b-111">OLE stellt einen Standard Objekt Handler bereit, der von lokalen Server Anwendungen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5ef1b-111">OLE provides a default object handler that local server applications can use.</span></span> <span data-ttu-id="5ef1b-112">Für Anwendungen, die ein spezielles Verhalten erfordern, können Entwickler einen benutzerdefinierten Handler implementieren, der entweder den Standard Handler ersetzt oder ihn verwendet, um bestimmte Standardverhalten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="5ef1b-112">For applications that require special behaviors, developers can implement a custom handler that either replaces the default handler or uses it to provide certain default behaviors.</span></span>

<span data-ttu-id="5ef1b-113">Ein Objekt Handler ist eine DLL, die mehrere interagierende Komponenten enthält.</span><span class="sxs-lookup"><span data-stu-id="5ef1b-113">An object handler is a DLL containing several interacting components.</span></span> <span data-ttu-id="5ef1b-114">Diese Komponenten umfassen Remoting-Komponenten zum Verwalten der Kommunikation zwischen dem Handler und seiner Serveranwendung, einem Cache zum Speichern der Daten eines Objekts sowie Informationen dazu, wie diese Daten formatiert und angezeigt werden sollen, sowie ein Steuerungsobjekt, das die Aktivitäten der anderen Komponenten der dll koordiniert.</span><span class="sxs-lookup"><span data-stu-id="5ef1b-114">These components include remoting pieces to manage communication between the handler and its server application, a cache for storing an object's data, along with information on how that data should be formatted and displayed, and a controlling object that coordinates the activities of the DLL's other components.</span></span> <span data-ttu-id="5ef1b-115">Wenn ein Objekt ein Link ist, enthält die dll außerdem eine Verknüpfungs Komponente oder ein *verknüpftes Objekt*, das den Namen und den Speicherort der Link Quelle nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="5ef1b-115">In addition, if an object is a link, the DLL also includes a linking component, or *linked object*, which keeps track of the name and location of the link source.</span></span>

<span data-ttu-id="5ef1b-116">Der *Cache* enthält Daten und Präsentationsinformationen, die für den Handler ausreichen, um ein geladenes, aber nicht ausgelaufetes Objekt in seinem Container anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5ef1b-116">The *cache* contains data and presentation information sufficient for the handler to display a loaded, but not running, object in its container.</span></span> <span data-ttu-id="5ef1b-117">OLE stellt eine Implementierung des Caches bereit, der von OLE-Standard Objekt Handler und dem Link-Objekt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5ef1b-117">OLE provides an implementation of the cache used by OLE's default object handler and the link object.</span></span> <span data-ttu-id="5ef1b-118">Der Cache speichert Daten in Formaten, die vom Objekt Handler benötigt werden, um Container Zeichnungs Anforderungen zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="5ef1b-118">The cache stores data in formats needed by the object handler to satisfy container draw requests.</span></span> <span data-ttu-id="5ef1b-119">Wenn sich die Daten eines Objekts ändern, sendet das Objekt eine Benachrichtigung an den Cache, damit ein Update erfolgen kann.</span><span class="sxs-lookup"><span data-stu-id="5ef1b-119">When an object's data changes, the object sends a notification to the cache so that an update can occur.</span></span> <span data-ttu-id="5ef1b-120">Weitere Informationen zum Cache finden Sie unter [View Caching (anzeigen](view-caching.md)der Zwischenspeicherung).</span><span class="sxs-lookup"><span data-stu-id="5ef1b-120">For more information on the cache, see [View Caching](view-caching.md).</span></span>

<span data-ttu-id="5ef1b-121">Weitere Informationen finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="5ef1b-121">For more information, see the following topic:</span></span>

-   [<span data-ttu-id="5ef1b-122">Der Standard Handler und benutzerdefinierte Handler</span><span class="sxs-lookup"><span data-stu-id="5ef1b-122">The Default Handler and Custom Handlers</span></span>](the-default-handler-and-custom-handlers.md)

## <a name="related-topics"></a><span data-ttu-id="5ef1b-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5ef1b-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ef1b-124">Verbund Dokumente</span><span class="sxs-lookup"><span data-stu-id="5ef1b-124">Compound Documents</span></span>](compound-documents.md)
</dt> </dl>

 

 




