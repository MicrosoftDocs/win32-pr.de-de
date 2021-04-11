---
title: Registrieren von com-Anwendungen
description: Registrieren von com-Anwendungen
ms.assetid: 64ab5b42-2fdb-4d06-bd58-fd76f27f7da4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e115c4a8445e701809a7f418e0ce4ef72226eb0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310944"
---
# <a name="registering-com-applications"></a><span data-ttu-id="af8d3-103">Registrieren von com-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="af8d3-103">Registering COM Applications</span></span>

<span data-ttu-id="af8d3-104">Die Registrierung ist eine-Systemdatenbank, die Informationen zur Konfiguration von System Hardware und-Software sowie zu den Benutzern des Systems enthält.</span><span class="sxs-lookup"><span data-stu-id="af8d3-104">The registry is a system database that contains information about the configuration of system hardware and software as well as about users of the system.</span></span> <span data-ttu-id="af8d3-105">Alle Windows-basierten Programme können der Registrierung Informationen hinzufügen und Informationen aus der Registrierung lesen.</span><span class="sxs-lookup"><span data-stu-id="af8d3-105">Any Windows-based program can add information to the registry and read information back from the registry.</span></span> <span data-ttu-id="af8d3-106">Clients durchsuchen die Registrierung nach interessanten Komponenten, die verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="af8d3-106">Clients search the registry for interesting components to use.</span></span>

<span data-ttu-id="af8d3-107">Die Registrierung verwaltet Informationen zu allen COM-Objekten, die im System installiert sind.</span><span class="sxs-lookup"><span data-stu-id="af8d3-107">The registry maintains information about all the COM objects installed in the system.</span></span> <span data-ttu-id="af8d3-108">Jedes Mal, wenn eine Anwendung eine Instanz einer COM-Komponente erstellt, wird die Registrierung so abgefragt, dass entweder die CLSID oder ProgID der Komponente in den Pfadnamen der Server-DLL oder der exe-Datei aufgelöst wird, in der Sie enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="af8d3-108">Whenever an application creates an instance of a COM component, the registry is consulted to resolve either the CLSID or ProgID of the component into the pathname of the server DLL or EXE that contains it.</span></span> <span data-ttu-id="af8d3-109">Nachdem der Server der Komponente ermittelt wurde, lädt Windows entweder den Server in den Prozessbereich der Client Anwendung (Prozess interne Komponenten) oder startet den Server im eigenen Prozessbereich (lokale Server und Remote Server).</span><span class="sxs-lookup"><span data-stu-id="af8d3-109">After determining the component's server, Windows either loads the server into the process space of the client application (in-process components) or starts the server in its own process space (local and remote servers).</span></span> <span data-ttu-id="af8d3-110">Der Server erstellt eine Instanz der Komponente und kehrt zum Client einen Verweis auf eine der Schnittstellen der Komponente zurück.</span><span class="sxs-lookup"><span data-stu-id="af8d3-110">The server creates an instance of the component and returns to the client a reference to one of the component's interfaces.</span></span>

<span data-ttu-id="af8d3-111">Weitere Informationen zur Windows-Registrierung finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="af8d3-111">For more information about the Windows registry, see the following topics:</span></span>

-   [<span data-ttu-id="af8d3-112">Registrierungs Hierarchie</span><span class="sxs-lookup"><span data-stu-id="af8d3-112">Registry Hierarchy</span></span>](registry-hierarchy.md)
-   [<span data-ttu-id="af8d3-113">Klassen und Server</span><span class="sxs-lookup"><span data-stu-id="af8d3-113">Classes and Servers</span></span>](classes-and-servers.md)
-   [<span data-ttu-id="af8d3-114">Klassifizierender Komponenten</span><span class="sxs-lookup"><span data-stu-id="af8d3-114">Classifying Components</span></span>](classifying-components.md)
-   [<span data-ttu-id="af8d3-115">Verwenden von OLEVIEW</span><span class="sxs-lookup"><span data-stu-id="af8d3-115">Using OleView</span></span>](using-oleview.md)
-   [<span data-ttu-id="af8d3-116">Registrieren von Komponenten</span><span class="sxs-lookup"><span data-stu-id="af8d3-116">Registering Components</span></span>](registering-components.md)
-   [<span data-ttu-id="af8d3-117">Registrierung wird überprüft</span><span class="sxs-lookup"><span data-stu-id="af8d3-117">Checking Registration</span></span>](checking-registration.md)
-   [<span data-ttu-id="af8d3-118">Unbekannte Benutzer Typen</span><span class="sxs-lookup"><span data-stu-id="af8d3-118">Unknown User Types</span></span>](unknown-user-types.md)
-   [<span data-ttu-id="af8d3-119">COM-Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="af8d3-119">COM Registry Keys</span></span>](com-registry-keys.md)

 

 




