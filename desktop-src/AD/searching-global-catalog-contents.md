---
title: Durchsuchen des globalen Katalogs
description: Active Directory Domain Services auch über einen globalen Katalog (GC) verfügen, der ein partielles Replikat aller Objekte im Verzeichnis enthält.
ms.assetid: 83970563-1a56-4671-b264-56e29939e369
ms.tgt_platform: multiple
keywords:
- Durchsuchen des globalen Katalog Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a057330309c12df6d18a209fc3d2adaf42b03005
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707559"
---
# <a name="searching-the-global-catalog"></a><span data-ttu-id="0d58a-104">Durchsuchen des globalen Katalogs</span><span class="sxs-lookup"><span data-stu-id="0d58a-104">Searching the Global Catalog</span></span>

<span data-ttu-id="0d58a-105">Active Directory Domain Services auch über einen globalen Katalog (GC) verfügen, der ein partielles Replikat aller Objekte im Verzeichnis enthält.</span><span class="sxs-lookup"><span data-stu-id="0d58a-105">Active Directory Domain Services also have a global catalog (GC), which contains a partial replica of all objects in the directory.</span></span> <span data-ttu-id="0d58a-106">Sie enthält außerdem partielle Replikate des Schemas und der Konfigurations Container.</span><span class="sxs-lookup"><span data-stu-id="0d58a-106">It also contains partial replicas of the schema and configuration containers.</span></span> <span data-ttu-id="0d58a-107">Mindestens ein Domänen Controller in einer Domäne kann eine Kopie des globalen Katalogs enthalten.</span><span class="sxs-lookup"><span data-stu-id="0d58a-107">One or more domain controllers in a domain can hold a copy of the global catalog.</span></span> <span data-ttu-id="0d58a-108">Weitere Informationen zum Binden an einen globalen Katalog finden Sie unter [binden an den globalen Katalog](binding-to-the-global-catalog.md).</span><span class="sxs-lookup"><span data-stu-id="0d58a-108">For more information about binding to a global catalog, see [Binding to the Global Catalog](binding-to-the-global-catalog.md).</span></span>

<span data-ttu-id="0d58a-109">Der globale Katalog enthält ein Replikat aller Objekte in Active Directory Domain Services, aber nur mit einer kleinen Anzahl von Attributen.</span><span class="sxs-lookup"><span data-stu-id="0d58a-109">The global catalog holds a replica of every object in Active Directory Domain Services, but with only a small number of their attributes.</span></span> <span data-ttu-id="0d58a-110">Bei Such Vorgängen werden die Attribute im globalen Katalog häufig verwendet, z. b. die vor-und Nachnamen eines Benutzers, Anmelde Namen usw.</span><span class="sxs-lookup"><span data-stu-id="0d58a-110">The attributes in the global catalog are those most frequently used in search operations, such as a user's first and last names, login names, and so on.</span></span> <span data-ttu-id="0d58a-111">Die Attribute des globalen Katalogs enthalten außerdem diejenigen, die zum Auffinden eines vollständigen Replikats des Objekts erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="0d58a-111">The global catalog attributes also include those required to locate a full replica of the object.</span></span> <span data-ttu-id="0d58a-112">Der globale Katalog ermöglicht Benutzern das schnelle Auffinden von interessanten Objekten, ohne zu wissen, welche Domäne Sie enthält und ohne dass ein zusammenhängender erweiterter Namespace im Unternehmen erforderlich ist. Das heißt, Sie können die gesamte Gesamtstruktur durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="0d58a-112">The global catalog allows users to quickly find objects of interest without knowing what domain holds them and without requiring a contiguous extended namespace in the enterprise; that is, you can search the entire forest.</span></span>

<span data-ttu-id="0d58a-113">Wenn Sie also eine Bindung zu einem Objekt im globalen Katalog herstellen, Durchsuchen Sie dieses Objekt und die gesamte Hierarchie darunter –, ohne zu einem anderen Server wechseln zu müssen.</span><span class="sxs-lookup"><span data-stu-id="0d58a-113">So, if you bind to an object in the global catalog, you will search that object and the entire hierarchy below it — without having to go to any other server.</span></span> <span data-ttu-id="0d58a-114">Allerdings kann bei der Suche nur ein Abfrage Filter mit Eigenschaften im globalen Katalog verwendet werden, und es können nur Eigenschaften im globalen Katalog abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="0d58a-114">However, the search can only use a query filter containing properties in the global catalog and can retrieve only properties in the global catalog.</span></span>

<span data-ttu-id="0d58a-115">Das Durchsuchen des globalen Katalogs bietet die folgenden Vorteile:</span><span class="sxs-lookup"><span data-stu-id="0d58a-115">Searching the global catalog has the following benefits:</span></span>

-   <span data-ttu-id="0d58a-116">Der globale Katalog ermöglicht es Ihnen, die gesamte Gesamtstruktur oder einen beliebigen Teil der Gesamtstruktur sowie das Schema und die Konfigurations Container zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="0d58a-116">Global catalog enables you to search the entire forest or any part of the forest as well as the schema and configuration containers.</span></span>
-   <span data-ttu-id="0d58a-117">Der globale Katalog ermöglicht es Ihnen, eine vollständige Suche auf einem einzelnen Server auszuführen.</span><span class="sxs-lookup"><span data-stu-id="0d58a-117">Global catalog enables you to perform a complete search on a single server.</span></span> <span data-ttu-id="0d58a-118">Es sind keine Verweise oder eine Verweis Verfolgung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0d58a-118">No referrals or referral chasing is required.</span></span>

<span data-ttu-id="0d58a-119">Das Durchsuchen des globalen Katalogs hat folgende Nachteile:</span><span class="sxs-lookup"><span data-stu-id="0d58a-119">Searching the global catalog has the following disadvantages:</span></span>

-   <span data-ttu-id="0d58a-120">Der globale Katalog enthält eine kleine Teilmenge der Eigenschaften für jedes Objekt.</span><span class="sxs-lookup"><span data-stu-id="0d58a-120">Global catalog contains a small subset of the properties on each object.</span></span> <span data-ttu-id="0d58a-121">Wenn der Abfrage Filtereigenschaften enthält, die nicht im globalen Katalog enthalten sind, wertet die Abfrage die Ausdrücke, die diese Eigenschaften enthalten, als false aus.</span><span class="sxs-lookup"><span data-stu-id="0d58a-121">If your query filter includes properties that are not in the global catalog, the query will evaluate the expressions containing those properties as false.</span></span> <span data-ttu-id="0d58a-122">Wenn Sie in der Liste der Eigenschaften, die Sie zurückgeben möchten, nicht globale Katalog Eigenschaften angeben, werden diese Eigenschaften nicht abgerufen.</span><span class="sxs-lookup"><span data-stu-id="0d58a-122">If you specify non-global catalog properties in the list of properties to return, those properties are not retrieved.</span></span>
-   <span data-ttu-id="0d58a-123">Ein Domänen Controller, der einen globalen Katalog enthält, muss verfügbar sein, um den globalen Katalog zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="0d58a-123">To search the global catalog, a domain controller that contains a global catalog must be available.</span></span> <span data-ttu-id="0d58a-124">Wenn eine solche nicht verfügbar ist, können Sie keine globale Katalog Suche durchführen.</span><span class="sxs-lookup"><span data-stu-id="0d58a-124">If one is not available, you cannot perform a global catalog search.</span></span>
-   <span data-ttu-id="0d58a-125">Der globale Katalog ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="0d58a-125">The global catalog is read-only.</span></span> <span data-ttu-id="0d58a-126">Dies bedeutet, dass Sie keine Bindung an ein Objekt im globalen Katalog vornehmen können, um-Objekte zu erstellen, zu ändern oder zu löschen.</span><span class="sxs-lookup"><span data-stu-id="0d58a-126">This means you cannot bind to an object in the global catalog to create, modify, or delete objects.</span></span>

 

 




