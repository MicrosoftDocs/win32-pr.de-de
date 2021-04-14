---
title: Zuständigkeiten von com-Servern
description: Zuständigkeiten von com-Servern
ms.assetid: 9853bbf5-b989-45b7-8fa8-8cd2f0d48d3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86b9d3104af80a7b2dca49dbbd5b55e66a613ee7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391064"
---
# <a name="com-server-responsibilities"></a><span data-ttu-id="59d39-103">Zuständigkeiten von com-Servern</span><span class="sxs-lookup"><span data-stu-id="59d39-103">COM Server Responsibilities</span></span>

<span data-ttu-id="59d39-104">Eine der wichtigsten Möglichkeiten für einen Client, einen Zeiger auf ein Objekt zu erhalten, besteht darin, dass der Client fragt, ob ein Server gestartet und eine Instanz des vom Server bereitgestellten Objekts erstellt und aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="59d39-104">One of the most important ways for a client to get a pointer to an object is for the client to ask that a server be launched and that an instance of the object provided by the server be created and activated.</span></span> <span data-ttu-id="59d39-105">Es liegt in der Verantwortung des Servers, sicherzustellen, dass dies ordnungsgemäß erfolgt.</span><span class="sxs-lookup"><span data-stu-id="59d39-105">It is the responsibility of the server to ensure that this happens properly.</span></span> <span data-ttu-id="59d39-106">Hierfür gibt es mehrere wichtige Teile.</span><span class="sxs-lookup"><span data-stu-id="59d39-106">There are several important parts to this.</span></span>

<span data-ttu-id="59d39-107">Der Server muss Code für ein Klassenobjekt über eine Implementierung der [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) -oder [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="59d39-107">The server must implement code for a class object through an implementation of either the [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) or [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) interface.</span></span>

<span data-ttu-id="59d39-108">Der Server muss seine CLSID in der Systemregistrierung auf dem Computer, auf dem er sich befindet, registrieren und die Möglichkeit haben, seinen Computer Speicherort auf anderen Systemen in einem Netzwerk zu veröffentlichen, damit Clients ihn anrufen können, ohne dass der Client den Standort des Servers kennen muss.</span><span class="sxs-lookup"><span data-stu-id="59d39-108">The server must register its CLSID in the system registry on the machine on which it resides and further, has the option of publishing its machine location to other systems on a network to allow clients to call it without requiring the client to know the server's location.</span></span>

<span data-ttu-id="59d39-109">Der Server ist hauptsächlich für die Sicherheit verantwortlich. der Server bestimmt zum größten Teil, ob er einen Zeiger auf eines seiner Objekte auf einen Client bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="59d39-109">The server is primarily responsible for security; that is, for the most part, the server determines whether it will provide a pointer to one of its objects to a client.</span></span>

<span data-ttu-id="59d39-110">Prozess interne Server müssen bestimmte Funktionen implementieren und exportieren, die es dem Client Prozess ermöglichen, Sie zu instanziieren.</span><span class="sxs-lookup"><span data-stu-id="59d39-110">In-process servers should implement and export certain functions that allow the client process to instantiate them.</span></span>

<span data-ttu-id="59d39-111">In den folgenden Themen werden die Zuständigkeiten des COM-Servers ausführlich erläutert:</span><span class="sxs-lookup"><span data-stu-id="59d39-111">The following topics detail the responsibilities of the COM server:</span></span>

-   [<span data-ttu-id="59d39-112">Implementieren von IClassFactory</span><span class="sxs-lookup"><span data-stu-id="59d39-112">Implementing IClassFactory</span></span>](implementing-iclassfactory.md)
-   [<span data-ttu-id="59d39-113">Lizenzierung und IClassFactory2</span><span class="sxs-lookup"><span data-stu-id="59d39-113">Licensing and IClassFactory2</span></span>](licensing-and-iclassfactory2.md)
-   [<span data-ttu-id="59d39-114">Registrieren von com-Servern</span><span class="sxs-lookup"><span data-stu-id="59d39-114">Registering COM Servers</span></span>](registering-com-servers.md)
-   [<span data-ttu-id="59d39-115">Hilfshilfsprogramme für die Out-of-Process-Server Implementierung</span><span class="sxs-lookup"><span data-stu-id="59d39-115">Out-of-Process Server Implementation Helpers</span></span>](out-of-process-server-implementation-helpers.md)
-   [<span data-ttu-id="59d39-116">GUID-Erstellung und-Optimierungen</span><span class="sxs-lookup"><span data-stu-id="59d39-116">GUID Creation and Optimizations</span></span>](guid-creation-and-optimizations.md)

## <a name="related-topics"></a><span data-ttu-id="59d39-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="59d39-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59d39-118">COM-Clients und-Server</span><span class="sxs-lookup"><span data-stu-id="59d39-118">COM Clients and Servers</span></span>](com-clients-and-servers.md)
</dt> </dl>

 

 