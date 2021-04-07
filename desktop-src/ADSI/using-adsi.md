---
title: Verwenden von Active Directory Dienst Schnittstellen
description: Mit Active Directory Service Interfaces (ADSI) können Client Anwendungen von Verzeichnisdiensten einen Satz von Schnittstellen für die Kommunikation mit einem beliebigen Namespace verwenden, der eine ADSI-Implementierung bereitstellt.
ms.assetid: 58bde1ea-30d1-4601-a6fb-df0bb837e2ab
ms.tgt_platform: multiple
keywords:
- Verwenden von Active Directory Dienst Schnittstellen ADSI
- ADSI ADSI, using
- Active Directory Dienst Schnittstellen ADSI, using
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e500044ec755c393f8c8287528fee7f935751fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855235"
---
# <a name="using-active-directory-service-interfaces"></a><span data-ttu-id="f0159-106">Verwenden von Active Directory Dienst Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f0159-106">Using Active Directory Service Interfaces</span></span>

<span data-ttu-id="f0159-107">Mit Active Directory Service Interfaces (ADSI) können Client Anwendungen von Verzeichnisdiensten einen Satz von Schnittstellen für die Kommunikation mit einem beliebigen Namespace verwenden, der eine ADSI-Implementierung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="f0159-107">Active Directory Service Interfaces (ADSI) provides the means for client applications of directory services to use one set of interfaces to communicate with any namespace that provides an ADSI implementation.</span></span> <span data-ttu-id="f0159-108">ADSI-Clients verwenden die klar definierten Active Directory Dienst Schnittstellen anstelle der Netzwerk spezifischen API-Aufrufe, um einen einfacheren Zugriff auf die Dienste für einen Namespace zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f0159-108">ADSI clients use the well-defined Active Directory Service Interfaces in place of the network-specific API calls to gain simpler access to the services for a namespace.</span></span>

<span data-ttu-id="f0159-109">Active Directory Dienst Schnittstellen entsprechen den Component Object Model (com) und unterstützen com-Standard Features.</span><span class="sxs-lookup"><span data-stu-id="f0159-109">Active Directory Service Interfaces conform to the Component Object Model (COM) and support standard COM features.</span></span>

<span data-ttu-id="f0159-110">ADSI bietet Schnittstellen, die mit der Automatisierung für namens gebundene Controller wie Java, Microsoft Visual Basic Development System und Visual Basic Scripting Edition (VBScript) kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="f0159-110">ADSI supplies interfaces that are compliant with Automation for name-bound controllers like Java, Microsoft Visual Basic development system, and Visual Basic Scripting Edition (VBScript).</span></span> <span data-ttu-id="f0159-111">ADSI kann auch eine Schnittstelle bereitstellen, mit der die Leistung für Schnittstellen optimiert werden kann, die nicht mit der Automatisierung kompatibel sind und in sprach Umgebungen wie C und C++ verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="f0159-111">ADSI can also provide an interface that can optimize performance for interfaces that are not compliant with Automation, to use with language environments like C and C++.</span></span>

<span data-ttu-id="f0159-112">ADSI bietet auch die nicht Automatisierungs Schnittstellen [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) und [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), um die Verwaltung von Verzeichnis Objekten und Abfragen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="f0159-112">ADSI also provides the non-automation interfaces, [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) and [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch), to support directory object management and queries.</span></span>

<span data-ttu-id="f0159-113">Außerdem stellt ADSI einen eigenen OLE DB Anbieter bereit, sodass alle Clients, die bereits OLE DB verwenden, einschließlich derjenigen, die ActiveX Data Objects verwenden, Verzeichnisdienste direkt abfragen können.</span><span class="sxs-lookup"><span data-stu-id="f0159-113">In addition, ADSI supplies its own OLE DB provider, so that any client already using OLE DB, including those using ActiveX Data Objects, can query directory services directly.</span></span>

<span data-ttu-id="f0159-114">Webanwendungen, die Active Server Seiten verwenden, können auch den Zugriff auf Verzeichnisdienste über ADSI programmieren.</span><span class="sxs-lookup"><span data-stu-id="f0159-114">Web applications using Active Server Pages also can program access to directory services through ADSI.</span></span>

<span data-ttu-id="f0159-115">ADSI-Clients können alle ADSI-Anbieter an einem Standort Programm gesteuert ermitteln und die gleichen Schnittstellen für die Kommunikation mit den einzelnen Namespaces verwenden.</span><span class="sxs-lookup"><span data-stu-id="f0159-115">ADSI clients can programmatically discover all the ADSI providers at a site and use the same interfaces to communicate with each namespace.</span></span> <span data-ttu-id="f0159-116">Wenn zusätzliche Anbieter installiert sind, können die ADSI-Clients auch ohne Neukompilieren mit den neuen Namespaces kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="f0159-116">As additional providers are installed, the ADSI clients can communicate, without recompiling, with the new namespaces as well.</span></span>

<span data-ttu-id="f0159-117">In diesem Programmier Handbuch wird beschrieben, wie ADSI funktioniert, und es werden Informationen zum Ausführen bestimmter Aufgaben in ADSI bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="f0159-117">This programming guide describes how ADSI works and provides information for performing specific tasks in ADSI.</span></span> <span data-ttu-id="f0159-118">Die folgenden Themen werden erörtert:</span><span class="sxs-lookup"><span data-stu-id="f0159-118">The following topics are discussed:</span></span>

-   [<span data-ttu-id="f0159-119">Binden an ein ADSI-Objekt</span><span class="sxs-lookup"><span data-stu-id="f0159-119">Binding to an ADSI Object</span></span>](binding-to-an-adsi-object.md)
-   [<span data-ttu-id="f0159-120">Erstellen und Löschen von Objekten</span><span class="sxs-lookup"><span data-stu-id="f0159-120">Creating and Deleting Objects</span></span>](creating-and-deleting-objects.md)
-   [<span data-ttu-id="f0159-121">Zugreifen auf und Bearbeiten von Daten mit ADSI</span><span class="sxs-lookup"><span data-stu-id="f0159-121">Accessing and Manipulating Data with ADSI</span></span>](accessing-and-manipulating-data-with-adsi.md)
-   [<span data-ttu-id="f0159-122">Verwenden des ADSI-Schemas</span><span class="sxs-lookup"><span data-stu-id="f0159-122">Using the ADSI Schema</span></span>](using-the-adsi-schema.md)
-   [<span data-ttu-id="f0159-123">Sammlungen und Gruppen</span><span class="sxs-lookup"><span data-stu-id="f0159-123">Collections and Groups</span></span>](collections-and-groups.md)
-   [<span data-ttu-id="f0159-124">Auflisten von ADSI-Objekten</span><span class="sxs-lookup"><span data-stu-id="f0159-124">Enumerating ADSI Objects</span></span>](enumerating-adsi-objects.md)
-   [<span data-ttu-id="f0159-125">Such Active Directory</span><span class="sxs-lookup"><span data-stu-id="f0159-125">Searching Active Directory</span></span>](searching-active-directory.md)
-   [<span data-ttu-id="f0159-126">ADSI-Sicherheitsmodell</span><span class="sxs-lookup"><span data-stu-id="f0159-126">ADSI Security Model</span></span>](adsi-security-model.md)
-   [<span data-ttu-id="f0159-127">ADSI-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="f0159-127">ADSI Extensions</span></span>](adsi-extensions.md)
-   [<span data-ttu-id="f0159-128">Verwenden von ADSI mit Exchange</span><span class="sxs-lookup"><span data-stu-id="f0159-128">Using ADSI with Exchange</span></span>](using-adsi-with-exchange.md)
-   [<span data-ttu-id="f0159-129">ADSI Utility-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f0159-129">ADSI Utility Interfaces</span></span>](adsi-utility-interfaces.md)
-   [<span data-ttu-id="f0159-130">Programmieren von ADSI mit Java/com</span><span class="sxs-lookup"><span data-stu-id="f0159-130">Programming ADSI with Java/COM</span></span>](programming-adsi-with-javacom.md)

 

 




