---
title: Bestimmen des Orts für die Suche
description: In diesem Thema werden die verschiedenen Suchvorgänge erläutert, die in Active Directory Domain Services ausgeführt werden können.
ms.assetid: 4b7428c8-c246-41fc-8811-892220c4270f
ms.tgt_platform: multiple
keywords:
- Auswählen des Orts für die Suche in AD
- Active Directory AD, suchen und entscheiden, wo gesucht werden soll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f24baccd55e263c4d5b677996589ba57c1301e8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104314595"
---
# <a name="deciding-where-to-search"></a><span data-ttu-id="3e2b8-105">Bestimmen des Orts für die Suche</span><span class="sxs-lookup"><span data-stu-id="3e2b8-105">Deciding Where to Search</span></span>

<span data-ttu-id="3e2b8-106">In diesem Thema werden die verschiedenen Suchvorgänge erläutert, die in Active Directory Domain Services ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="3e2b8-106">This topic explains the different searches that can be performed in Active Directory Domain Services.</span></span>

<span data-ttu-id="3e2b8-107">Alle Suchvorgänge werden in einem der folgenden Namenskontexte ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="3e2b8-107">All searches are performed in one of the following naming contexts:</span></span>

-   <span data-ttu-id="3e2b8-108">Domäne, einschließlich Anwendungsverzeichnis Partitionen</span><span class="sxs-lookup"><span data-stu-id="3e2b8-108">Domain, including application directory partitions</span></span>
-   <span data-ttu-id="3e2b8-109">Schema Container</span><span class="sxs-lookup"><span data-stu-id="3e2b8-109">Schema container</span></span>
-   <span data-ttu-id="3e2b8-110">Konfigurations Container</span><span class="sxs-lookup"><span data-stu-id="3e2b8-110">Configuration container</span></span>
-   <span data-ttu-id="3e2b8-111">Globaler Katalog</span><span class="sxs-lookup"><span data-stu-id="3e2b8-111">Global catalog</span></span>

## <a name="searching-a-domain"></a><span data-ttu-id="3e2b8-112">Suchen einer Domäne</span><span class="sxs-lookup"><span data-stu-id="3e2b8-112">Searching a Domain</span></span>

<span data-ttu-id="3e2b8-113">Domänen enthalten die meisten der stark verwendeten Objekte, wie z. b. Benutzer, Kontakte, Gruppen, Organisationseinheiten, Computer usw.</span><span class="sxs-lookup"><span data-stu-id="3e2b8-113">Domains contain most of the highly used objects such as users, contacts, groups, organizational units, computers, and so on.</span></span> <span data-ttu-id="3e2b8-114">Bei den meisten Abfragen wird eine Domäne durchsucht.</span><span class="sxs-lookup"><span data-stu-id="3e2b8-114">Most queries will search a domain.</span></span> <span data-ttu-id="3e2b8-115">Weitere Informationen zum Durchsuchen von Domänen Inhalten finden Sie unter durch [Suchen von Domänen Inhalten](searching-domain-contents.md).</span><span class="sxs-lookup"><span data-stu-id="3e2b8-115">For more information about searching a domain, see [Searching Domain Contents](searching-domain-contents.md).</span></span>

## <a name="searching-the-schema-container"></a><span data-ttu-id="3e2b8-116">Durchsuchen des Schema Containers</span><span class="sxs-lookup"><span data-stu-id="3e2b8-116">Searching the Schema Container</span></span>

<span data-ttu-id="3e2b8-117">Der Schema Container enthält die [**classSchema**](/windows/desktop/ADSchema/c-classschema) -und [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) -Objekte, die die formale Definition aller Klassen und Attribute bereitstellen, die in Active Directory Domain Services vorhanden sein können.</span><span class="sxs-lookup"><span data-stu-id="3e2b8-117">The schema container contains the [**classSchema**](/windows/desktop/ADSchema/c-classschema) and [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) objects that provide the formal definition of every class and attribute that can exist in Active Directory Domain Services.</span></span> <span data-ttu-id="3e2b8-118">Um im Schema Container nach Objekten zu suchen, binden Sie an einen beliebigen Domänen Controller an den Schema Container.</span><span class="sxs-lookup"><span data-stu-id="3e2b8-118">To search for objects in the schema container, bind to the schema container on any domain controller.</span></span> <span data-ttu-id="3e2b8-119">Der Schema Container ist auf allen Domänen Controllern verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3e2b8-119">The schema container is available on all domain controllers.</span></span> <span data-ttu-id="3e2b8-120">Der Distinguished Name des Schema Containers wird aus dem **schemaNamingContext** -Attribut von RootDSE abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3e2b8-120">The distinguished name of the schema container is obtained from the **schemaNamingContext** attribute from rootDSE.</span></span> <span data-ttu-id="3e2b8-121">Weitere Informationen zu RootDSE und zum **schemaNamingContext** -Attribut finden Sie unter [Server lose Bindung und RootDSE](serverless-binding-and-rootdse.md).</span><span class="sxs-lookup"><span data-stu-id="3e2b8-121">For more information about rootDSE and the **schemaNamingContext** attribute, see [Serverless Binding and RootDSE](serverless-binding-and-rootdse.md).</span></span>

<span data-ttu-id="3e2b8-122">Weitere Informationen zum Lesen aus dem Schema oder dem abstrakten Schema Container finden [Sie unter Richtlinien für die Bindung an das Schema](guidelines-for-binding-to-the-schema.md).</span><span class="sxs-lookup"><span data-stu-id="3e2b8-122">For more information about reading from the schema or abstract schema container, see [Guidelines for Binding to the Schema](guidelines-for-binding-to-the-schema.md).</span></span>

## <a name="searching-the-configuration-container"></a><span data-ttu-id="3e2b8-123">Durchsuchen des Konfigurations Containers</span><span class="sxs-lookup"><span data-stu-id="3e2b8-123">Searching the Configuration Container</span></span>

<span data-ttu-id="3e2b8-124">Der Konfigurations Container enthält Konfigurationsinformationen, z. b. Standorte, Dienste und Anzeige spezifiken, für die gesamte Gesamtstruktur.</span><span class="sxs-lookup"><span data-stu-id="3e2b8-124">The configuration container contains configuration information, such as sites, services and display specifiers, for the entire forest.</span></span> <span data-ttu-id="3e2b8-125">Um im Konfigurations Container nach Objekten zu suchen, binden Sie an den Konfigurations Container auf einem beliebigen Domänen Controller.</span><span class="sxs-lookup"><span data-stu-id="3e2b8-125">To search for objects in the configuration container, bind to the configuration container on any domain controller.</span></span> <span data-ttu-id="3e2b8-126">Der Konfigurations Container ist auf allen Domänen Controllern verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3e2b8-126">The configuration container is available on all domain controllers.</span></span> <span data-ttu-id="3e2b8-127">Der Distinguished Name des Konfigurations Containers wird aus dem **configurationNamingContext** -Attribut von RootDSE abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3e2b8-127">The distinguished name of the configuration container is obtained from the **configurationNamingContext** attribute from rootDSE.</span></span> <span data-ttu-id="3e2b8-128">Weitere Informationen zu RootDSE und zum **configurationNamingContext** -Attribut finden Sie unter [Server lose Bindung und RootDSE](serverless-binding-and-rootdse.md).</span><span class="sxs-lookup"><span data-stu-id="3e2b8-128">For more information about rootDSE and the **configurationNamingContext** attribute, see [Serverless Binding and RootDSE](serverless-binding-and-rootdse.md).</span></span>

## <a name="searching-the-global-catalog"></a><span data-ttu-id="3e2b8-129">Durchsuchen des globalen Katalogs</span><span class="sxs-lookup"><span data-stu-id="3e2b8-129">Searching the Global Catalog</span></span>

<span data-ttu-id="3e2b8-130">Der globale Katalog enthält ein Replikat aller Objekte in Active Directory Domain Services, aber nur mit einer kleinen Anzahl von Attributen.</span><span class="sxs-lookup"><span data-stu-id="3e2b8-130">The global catalog holds a replica of every object in Active Directory Domain Services, but with only a small number of their attributes.</span></span> <span data-ttu-id="3e2b8-131">Bei Such Vorgängen werden die Attribute im globalen Katalog häufig verwendet, z. b. die vor-und Nachnamen eines Benutzers, Anmelde Namen usw.</span><span class="sxs-lookup"><span data-stu-id="3e2b8-131">The attributes in the global catalog are those most frequently used in search operations, such as a user's first and last names, login names, and so on.</span></span> <span data-ttu-id="3e2b8-132">Weitere Informationen zum Durchsuchen des globalen Katalogs finden Sie unter durch [Suchen des globalen Katalogs](searching-global-catalog-contents.md).</span><span class="sxs-lookup"><span data-stu-id="3e2b8-132">For more information about searching the global catalog, see [Searching the Global Catalog](searching-global-catalog-contents.md).</span></span>

 

 