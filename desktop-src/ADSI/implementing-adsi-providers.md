---
title: Implementieren von Active Directory Dienst Schnittstellen Anbietern
description: Bei Active Directory Service Interfaces (ADSI) handelt es sich um COM-Schnittstellen, mit denen Verzeichnisdienst Objekte in Verzeichnisdienst Clients verfügbar gemacht werden. Durch die Bereitstellung einer Implementierung von ADSI erweitern Sie Ihre Client Basis auf den Satz von ADSI-Client Anwendungen.
ms.assetid: f86f36f0-44ff-41b7-8cf6-b97b721a8572
ms.tgt_platform: multiple
keywords:
- Implementieren von Active Directory Dienst Schnittstellen Anbieter ADSI
- Implementieren von ADSI-Anbietern ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30bdd0da406d9e65af898664e76b5e455540ebeb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707415"
---
# <a name="implementing-active-directory-service-interfaces-providers"></a><span data-ttu-id="665d8-106">Implementieren von Active Directory Dienst Schnittstellen Anbietern</span><span class="sxs-lookup"><span data-stu-id="665d8-106">Implementing Active Directory Service Interfaces Providers</span></span>

<span data-ttu-id="665d8-107">Bei Active Directory Service Interfaces (ADSI) handelt es sich um COM-Schnittstellen, mit denen Verzeichnisdienst Objekte in Verzeichnisdienst Clients verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="665d8-107">Active Directory Service Interfaces (ADSI) are COM interfaces that wrap directory service objects to expose them to clients of directory services.</span></span> <span data-ttu-id="665d8-108">Durch die Bereitstellung einer Implementierung von ADSI erweitern Sie Ihre Client Basis auf den Satz von ADSI-Client Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="665d8-108">By supplying an implementation of ADSI, you expand your client-base to the set of ADSI client applications.</span></span>

<span data-ttu-id="665d8-109">Wie bei jeder com-Implementierung können Sie in vielen Sprachen einen ADSI-Anbieter schreiben.</span><span class="sxs-lookup"><span data-stu-id="665d8-109">As with any COM implementation, you can write an ADSI provider in many languages.</span></span> <span data-ttu-id="665d8-110">Die ADSI-COM-Schnittstellen werden als duale Schnittstellen definiert, die sowohl Lauf Zeit-als auch Kompilierzeit-Namensauflösung ermöglichen. Sie können von Automatisierungs kompatiblen Sprachen wie z. b. Visual Basic, Visual Basic Scripting Edition sowie den mehr Leistungs-und Effizienz bewussten Sprachen wie C und C++ aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="665d8-110">The ADSI COM interfaces are defined as dual interfaces that allow both run-time and compile-time name resolution and can be called by Automation-compliant languages such as Visual Basic, Visual Basic Scripting Edition, and also the more performance and efficiency-conscious languages such as C and C++.</span></span> <span data-ttu-id="665d8-111">ADSI-Clients enthalten auch Webanwendungen, die Active Server Seiten und Verwaltungs-Snap-Ins über die Microsoft Management Console verwenden.</span><span class="sxs-lookup"><span data-stu-id="665d8-111">ADSI clients also include web applications using Active Server Pages and administration snap-ins through the Microsoft Management Console.</span></span>

<span data-ttu-id="665d8-112">Da ADSI einen eigenen OLE DB Anbieter bereitstellt, ermöglicht die Implementierung der durch [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) definierten Suchfunktionen auch, dass ADSI-Clients ihren Verzeichnisdienst nach Daten Abfragen können.</span><span class="sxs-lookup"><span data-stu-id="665d8-112">Because ADSI supplies its own OLE DB provider, implementing the search features defined by [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) also enables ADSI clients to query your directory service for data.</span></span>

<span data-ttu-id="665d8-113">Alle Verzeichnisdienst Objekte können über ein generisches ADSI-Objekt dargestellt werden, das [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)unterstützt.</span><span class="sxs-lookup"><span data-stu-id="665d8-113">All directory service objects can be represented through a generic ADSI object supporting [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject).</span></span> <span data-ttu-id="665d8-114">ADSI stellt die Bausteine bereit, die für die Darstellung der Features und Dienste eines beliebigen Verzeichnis Diensts erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="665d8-114">ADSI supplies the building blocks necessary to represent the features and services of any directory service.</span></span>

<span data-ttu-id="665d8-115">Außerdem stellen die ADSI-metaschnittstellen gängige Objekte dar, die von Verzeichnis Administratoren verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="665d8-115">In addition, the ADSI meta-interfaces represent common objects used by directory administrators.</span></span> <span data-ttu-id="665d8-116">Sie ordnen die Eigenschaften der metaschnittstellen den Eigenschaften zu, die vom Verzeichnisdienst unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="665d8-116">You map the properties of the meta-interfaces to the properties supported by your directory service.</span></span> <span data-ttu-id="665d8-117">Die Programmierung von ADSI-Clients mit den Active Directory-Dienst Schnittstellen erhält Zugriff auf Ihren Verzeichnisdienst, sobald der Anbieter installiert und das System neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="665d8-117">ADSI clients programming to the Active Directory Service Interfaces gain access to your directory service as soon as the provider is installed and the system restarted.</span></span>

<span data-ttu-id="665d8-118">Wenn Ihr Verzeichnisdienst eine Schema Darstellung unterstützt, wird der Namespace durch Unterstützung der Schema Verwaltungs Schnittstellen direkt für Verzeichnisdienst Browser zugänglich gemacht.</span><span class="sxs-lookup"><span data-stu-id="665d8-118">If your directory service supports a schema representation, supporting the schema management interfaces makes your namespace directly accessible to directory service browsers.</span></span> <span data-ttu-id="665d8-119">Wenn Sie Ihre Features über das Schema veröffentlichen, können Clients ihren Verzeichnisdienst Online Abfragen und die von Ihnen angebotenen Dienste nutzen.</span><span class="sxs-lookup"><span data-stu-id="665d8-119">By publishing your features through the schema, clients can query your directory service online and take advantage of the services you offer.</span></span> <span data-ttu-id="665d8-120">Aufgrund der Online Schema Verfügbarkeit und des Vorteile der COM-Schnittstelle können Sie weiterhin neue Features für Ihre Client Software zur Verfügung stellen und gleichzeitig Versionen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="665d8-120">Because of the online schema availability and the COM interface advantage, you can continue to make new features available to your client software while supporting down-level versions.</span></span>

 

 




