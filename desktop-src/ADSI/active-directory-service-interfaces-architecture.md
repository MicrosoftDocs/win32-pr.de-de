---
title: Architektur von Active Directory-Dienst Schnittstellen
description: Viele Verzeichnisdienste sind hierarchisch und eignen sich daher für ein hierarchisches Objektmodell. In diesem Abschnitt werden COM-Objekt Darstellungen verwendet, um verschiedene ADSI-Features zu veranschaulichen.
ms.assetid: ef545aea-a7a5-4f65-9133-e68b94a86311
ms.tgt_platform: multiple
keywords:
- Active Directory Dienst Schnittstellen Architektur ADSI
- ADSI ADSI, Info, Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce59d8d6281aa99bd96efa38166ef658972a5f54
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707494"
---
# <a name="active-directory-service-interfaces-architecture"></a><span data-ttu-id="6d90e-106">Architektur von Active Directory-Dienst Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="6d90e-106">Active Directory Service Interfaces Architecture</span></span>

<span data-ttu-id="6d90e-107">Viele Verzeichnisdienste sind hierarchisch und eignen sich daher für ein hierarchisches Objektmodell.</span><span class="sxs-lookup"><span data-stu-id="6d90e-107">Many directory services are hierarchical and thus lend themselves to a hierarchical object model.</span></span> <span data-ttu-id="6d90e-108">In diesem Abschnitt werden COM-Objekt Darstellungen verwendet, um verschiedene ADSI-Features zu veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="6d90e-108">This section uses COM object representations to illustrate various ADSI features.</span></span>

<span data-ttu-id="6d90e-109">In der folgenden Objektmodell Abbildung enthält ein Systemobjekt der obersten Ebene ein Namespace Objekt für jeden installierten ADSI-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="6d90e-109">In the following object model figure, a top-level system object contains one Namespace object for every installed ADSI provider.</span></span>

![Namespaces-Container Objekt](images/ds2top.png)

<span data-ttu-id="6d90e-111">Jedes der Namespace-Objekte ist selbst ein Container, der die Stamm Knoten der obersten Ebene jedes Servers, der Domäne oder alle anderen Arten von Verzeichnis System Objekten enthält, die in jedem Verzeichnisdienst als Stämme definiert sind.</span><span class="sxs-lookup"><span data-stu-id="6d90e-111">Each of the Namespace objects is itself a container that contains the top-level root nodes of every server, domain, or whatever other kinds of directory-system objects are defined as roots in each directory service.</span></span>

<span data-ttu-id="6d90e-112">ADSI stellt einen Satz vordefinierter Objekte und Schnittstellen bereit, damit Client Anwendungen mit Verzeichnisdiensten interagieren können, indem Sie einen einheitlichen Satz von Methoden verwenden.</span><span class="sxs-lookup"><span data-stu-id="6d90e-112">ADSI supplies a set of predefined objects and interfaces so that client applications can interact with directory services using a uniform set of methods.</span></span> <span data-ttu-id="6d90e-113">ADSI bietet jedoch möglicherweise keinen Zugriff auf alle Funktionen eines Verzeichnis Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="6d90e-113">However, ADSI may not provide access to all features of a directory service.</span></span> <span data-ttu-id="6d90e-114">Um den vollständigen Featuresatz der einzelnen Verzeichnisdienste besser nutzen zu können, stellt ADSI ein Schema Modell bereit, das von Verzeichnis Dienstanbietern und Drittanbieter-Softwareanbietern zum Erweitern von Features über die in ADSI bereitgestellten Schnittstellen hinaus verwendet werden kann</span><span class="sxs-lookup"><span data-stu-id="6d90e-114">To better use the full feature set of each directory service, ADSI supplies a schema model that directory service providers and third-party software vendors can use to extend features beyond the interfaces provided in ADSI.</span></span>

<span data-ttu-id="6d90e-115">Die Stamm Knoten Container-Objekte, die sich innerhalb des Namespace Objekts eines Anbieters befinden, enthalten ein ADSI-Schema Container Objekt.</span><span class="sxs-lookup"><span data-stu-id="6d90e-115">The root-node container objects, found within each provider Namespace object, include an ADSI schema container object.</span></span> <span data-ttu-id="6d90e-116">Dieses Objekt enthält die Definition aller Features für diesen Anbieter.</span><span class="sxs-lookup"><span data-stu-id="6d90e-116">This object contains the definition of all features for that provider.</span></span> <span data-ttu-id="6d90e-117">Weitere Informationen finden Sie unter [ADSI-Schema Modell](adsi-schema-model.md).</span><span class="sxs-lookup"><span data-stu-id="6d90e-117">For more information, see [ADSI Schema Model](adsi-schema-model.md).</span></span>

<span data-ttu-id="6d90e-118">Dieser Abschnitt schließt folgende Themen ein:</span><span class="sxs-lookup"><span data-stu-id="6d90e-118">This section includes the following topics:</span></span>

-   [<span data-ttu-id="6d90e-119">Active Directory von Dienst Schnittstellen Objekten</span><span class="sxs-lookup"><span data-stu-id="6d90e-119">Active Directory Service Interfaces Objects</span></span>](active-directory-service-interfaces-objects.md)
-   [<span data-ttu-id="6d90e-120">Namespaces</span><span class="sxs-lookup"><span data-stu-id="6d90e-120">Namespaces</span></span>](namespaces.md)
-   [<span data-ttu-id="6d90e-121">Anbieter für Active Directory-Dienst Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="6d90e-121">Active Directory Service Interfaces Provider</span></span>](active-directory-service-interfaces-provider.md)
-   [<span data-ttu-id="6d90e-122">ADSI-Schema Modell</span><span class="sxs-lookup"><span data-stu-id="6d90e-122">ADSI Schema Model</span></span>](adsi-schema-model.md)

 

 




