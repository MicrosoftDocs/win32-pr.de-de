---
title: Registrieren von com-Servern
description: Registrieren von com-Servern
ms.assetid: aaa09a1b-deb8-424f-a911-ae22d39919d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefaa47d159d776a3c931ca48de0dd3161c29913
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102378"
---
# <a name="registering-com-servers"></a><span data-ttu-id="76d8b-103">Registrieren von com-Servern</span><span class="sxs-lookup"><span data-stu-id="76d8b-103">Registering COM Servers</span></span>

<span data-ttu-id="76d8b-104">Nachdem Sie eine Klasse im Code definiert (um sicherzustellen, dass Sie [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) oder [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)implementiert) und ihr eine CLSID zugewiesen haben, müssen Sie Informationen in die Registrierung einfügen, die com bei Anforderung eines Clients mit der CLSID ermöglicht, Instanzen der zugehörigen Objekte zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="76d8b-104">After you have defined a class in code (ensuring that it implements [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) or [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)) and assigned it a CLSID, you need to put information in the registry that will allow COM, on request of a client with the CLSID, to create instances of its objects.</span></span> <span data-ttu-id="76d8b-105">Diese Informationen informieren das System für eine bestimmte CLSID, in der sich der DLL-oder exe-Code für diese Klasse befindet und wie Sie gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="76d8b-105">This information tells the system, for a given CLSID, where the DLL or EXE code for that class is located and how it is to be launched.</span></span>

<span data-ttu-id="76d8b-106">Es gibt mehr als eine Möglichkeit, eine Klasse in der Registrierung zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="76d8b-106">There is more than one way of registering a class in the registry.</span></span> <span data-ttu-id="76d8b-107">Außerdem gibt es andere Möglichkeiten, eine Klasse beim System zu registrieren, wenn Sie ausgeführt wird, damit das System weiß, dass sich ein aktuell laufendes Objekt im System befindet.</span><span class="sxs-lookup"><span data-stu-id="76d8b-107">In addition, there are other ways of "registering" a class with the system when it is running, so that the system is aware that a running object is currently in the system.</span></span>

<span data-ttu-id="76d8b-108">Weitere Informationen zum Registrieren von finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="76d8b-108">See the following topics for more information about registering:</span></span>

-   [<span data-ttu-id="76d8b-109">Registrieren einer Klasse bei der Installation</span><span class="sxs-lookup"><span data-stu-id="76d8b-109">Registering a Class at Installation</span></span>](registering-a-class-at-installation.md)
-   [<span data-ttu-id="76d8b-110">Registrieren eines ausführenden exe-Servers</span><span class="sxs-lookup"><span data-stu-id="76d8b-110">Registering a Running EXE Server</span></span>](registering-a-running-exe-server.md)
-   [<span data-ttu-id="76d8b-111">Registrieren von Objekten in der rot</span><span class="sxs-lookup"><span data-stu-id="76d8b-111">Registering Objects in the ROT</span></span>](registering-objects-in-the-rot.md)
-   [<span data-ttu-id="76d8b-112">Selbstregistrierung</span><span class="sxs-lookup"><span data-stu-id="76d8b-112">Self-Registration</span></span>](self-registration.md)
-   [<span data-ttu-id="76d8b-113">Installieren von als Dienst Anwendung</span><span class="sxs-lookup"><span data-stu-id="76d8b-113">Installing as a Service Application</span></span>](installing-as-a-service-application.md)

## <a name="related-topics"></a><span data-ttu-id="76d8b-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="76d8b-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76d8b-115">Zuständigkeiten von com-Servern</span><span class="sxs-lookup"><span data-stu-id="76d8b-115">COM Server Responsibilities</span></span>](com-server-responsibilities.md)
</dt> </dl>

 

 