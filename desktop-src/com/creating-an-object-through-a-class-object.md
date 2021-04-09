---
title: Erstellen eines Objekts über ein Klassenobjekt
description: Erstellen eines Objekts über ein Klassenobjekt
ms.assetid: cecf21b0-e509-425f-8dd6-ca6b1ac04f5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38787e7bc32151446cda6ff0a4cfe3f23a0f6eda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948067"
---
# <a name="creating-an-object-through-a-class-object"></a><span data-ttu-id="64b8a-103">Erstellen eines Objekts über ein Klassenobjekt</span><span class="sxs-lookup"><span data-stu-id="64b8a-103">Creating an Object Through a Class Object</span></span>

<span data-ttu-id="64b8a-104">Mit der zunehmenden Wichtigkeit von Computernetzwerken ist es erforderlich, dass Clients und Server problemlos und effizient interagieren, unabhängig davon, ob Sie sich auf demselben Computer oder in einem Netzwerk befinden.</span><span class="sxs-lookup"><span data-stu-id="64b8a-104">With the increasing importance of computer networks, it has become necessary for clients and servers to interact easily and efficiently, whether they reside on the same machine or across a network.</span></span> <span data-ttu-id="64b8a-105">Wichtig hierfür ist die Fähigkeit eines Clients, einen Server zu starten, eine Instanz des Server Objekts zu erstellen und Zugriff auf die Methoden der Schnittstellen für das Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="64b8a-105">Crucial to this is a client's ability to launch a server, create an instance of the server's object, and have access to the methods of the interfaces on the object.</span></span>

<span data-ttu-id="64b8a-106">Com stellt Erweiterungen für diesen grundlegenden com-Prozess bereit, der ihn praktisch nahtlos über ein Netzwerk hinweg ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="64b8a-106">COM provides extensions to this basic COM process that make it virtually seamless across a network.</span></span> <span data-ttu-id="64b8a-107">Wenn ein Client den Server über seine CLSID identifizieren kann, ermöglicht das Aufrufen einiger einfacher Funktionen com das Auffinden und Starten des Servers und das Aktivieren des Objekts.</span><span class="sxs-lookup"><span data-stu-id="64b8a-107">If a client is able to identify the server through its CLSID, calling a few simple functions permit COM to do all the work of locating and launching the server and activating the object.</span></span> <span data-ttu-id="64b8a-108">Unterschlüssel in der Registrierung ermöglichen es Remote Servern, ihren Speicherort zu registrieren, sodass der Client diese Informationen nicht benötigt.</span><span class="sxs-lookup"><span data-stu-id="64b8a-108">Subkeys in the registry allow remote servers to register their location, so the client does not require that information.</span></span> <span data-ttu-id="64b8a-109">Für Anwendungen, die Netzwerk Features nutzen möchten, können Sie mit den COM-Objekt Erstellungs Funktionen mehr Flexibilität und Effizienz erzielen.</span><span class="sxs-lookup"><span data-stu-id="64b8a-109">For applications that want to take advantage of networking features, the COM object creation functions allow more flexibility and efficiency.</span></span>

<span data-ttu-id="64b8a-110">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="64b8a-110">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="64b8a-111">COM-Klassen Objekte und CLSIDs</span><span class="sxs-lookup"><span data-stu-id="64b8a-111">COM Class Objects and CLSIDs</span></span>](com-class-objects-and-clsids.md)
-   [<span data-ttu-id="64b8a-112">Suchen eines Remote Objekts</span><span class="sxs-lookup"><span data-stu-id="64b8a-112">Locating a Remote Object</span></span>](locating-a-remote-object.md)
-   [<span data-ttu-id="64b8a-113">Hilfsfunktionen für die Instanzerstellung</span><span class="sxs-lookup"><span data-stu-id="64b8a-113">Instance Creation Helper Functions</span></span>](instance-creation-helper-functions.md)

## <a name="related-topics"></a><span data-ttu-id="64b8a-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="64b8a-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64b8a-115">COM-Clients und-Server</span><span class="sxs-lookup"><span data-stu-id="64b8a-115">COM Clients and Servers</span></span>](com-clients-and-servers.md)
</dt> </dl>

 

 




