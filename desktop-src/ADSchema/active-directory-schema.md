---
title: Active Directory Schema (AD-Schema)
description: Das Microsoft Active Directory Schema enthält formale Definitionen für jede Objektklasse, die in einer Active Directory Gesamtstruktur erstellt werden kann.
ms.assetid: b3da4519-d0c6-47eb-9455-ada653ad5c9e
ms.tgt_platform: multiple
keywords:
- Active Directory-Schema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b4c3393a6da1b8d1bd2c2418084c8f7fc657732
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106337422"
---
# <a name="active-directory-schema-ad-schema"></a><span data-ttu-id="68417-104">Active Directory Schema (AD-Schema)</span><span class="sxs-lookup"><span data-stu-id="68417-104">Active Directory Schema (AD Schema)</span></span>

<span data-ttu-id="68417-105">Das Microsoft Active Directory Schema enthält formale Definitionen für jede Objektklasse, die in einer Active Directory Gesamtstruktur erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="68417-105">The Microsoft Active Directory schema contains formal definitions of every object class that can be created in an Active Directory forest.</span></span> <span data-ttu-id="68417-106">Das Schema enthält außerdem formale Definitionen für jedes Attribut, das in einem Active Directory Objekt vorhanden sein kann.</span><span class="sxs-lookup"><span data-stu-id="68417-106">The schema also contains formal definitions of every attribute that can exist in an Active Directory object.</span></span> <span data-ttu-id="68417-107">Dieser Abschnitt enthält die Referenz für jedes Schema Objekt und bietet eine kurze Erläuterung der Attribute, Klassen und anderen Objekte, aus denen das Active Directory Schema besteht.</span><span class="sxs-lookup"><span data-stu-id="68417-107">This section provides the reference for each schema object and provides a brief explanation of the attributes, classes, and other objects that make up the Active Directory schema.</span></span>

> [!Note]  
> <span data-ttu-id="68417-108">In der folgenden Dokumentation ist die Programmier Referenz für Active Directory Schema enthalten.</span><span class="sxs-lookup"><span data-stu-id="68417-108">The following documentation contains the programming reference for Active Directory schema.</span></span> <span data-ttu-id="68417-109">Wenn Sie ein Drucker Fehler debuggen möchten, versuchen Sie, auf der [Microsoft Community-Website](https://answers.microsoft.com)zu suchen.</span><span class="sxs-lookup"><span data-stu-id="68417-109">If you are an end-user attempting to debug a printer error, try searching on the [Microsoft community site](https://answers.microsoft.com).</span></span> <span data-ttu-id="68417-110">Wenn Sie ein Entwickler sind, der eine allgemeine Übersicht über Active Directory Schema sucht, finden Sie weitere Informationen in den Themen [Active Directory Schema](/windows/desktop/AD/active-directory-schema) Übersicht.</span><span class="sxs-lookup"><span data-stu-id="68417-110">If you are a developer looking for a general overview of Active Directory schema, see the [Active Directory Schema](/windows/desktop/AD/active-directory-schema) overview topics.</span></span> <span data-ttu-id="68417-111">Wenn Sie nach Programmier Richtlinien zum Aktualisieren oder Ändern des Schemas suchen, finden Sie weitere Informationen zum Erweitern und Anpassen des Schemas unter [Erweitern des Schemas](/windows/desktop/AD/extending-the-schema)sowie zahlreiche Themen in den Programmier Handbüchern [Active Directory Domain Services](/windows/desktop/AD/active-directory-domain-services) und [Active Directory Lightweight Directory Services](/previous-versions/windows/desktop/adam/active-directory-lightweight-directory-services) .</span><span class="sxs-lookup"><span data-stu-id="68417-111">If you are looking for programming guidelines for updating or modifying the schema, For more information about extending and customizing the schema, see [Extending the Schema](/windows/desktop/AD/extending-the-schema), as well as many of the topics in the [Active Directory Domain Services](/windows/desktop/AD/active-directory-domain-services) and [Active Directory Lightweight Directory Services](/previous-versions/windows/desktop/adam/active-directory-lightweight-directory-services) programming guides.</span></span>

 

<span data-ttu-id="68417-112">In jedem der Referenz Themen gibt es einen Abschnitt für jedes Betriebssystem, für das das Thema gilt.</span><span class="sxs-lookup"><span data-stu-id="68417-112">In each of the reference topics, there is a section for each operating system that the topic applies to.</span></span> <span data-ttu-id="68417-113">Derzeit werden die folgenden Betriebssysteme unterstützt.</span><span class="sxs-lookup"><span data-stu-id="68417-113">The following operating systems are currently supported.</span></span> 

| <span data-ttu-id="68417-114">Plattform</span><span class="sxs-lookup"><span data-stu-id="68417-114">Platform</span></span>                                                      | <span data-ttu-id="68417-115">Name in Topic</span><span class="sxs-lookup"><span data-stu-id="68417-115">Name in topic</span></span>                               |
|---------------------------------------------------------------|---------------------------------------------|
| <span data-ttu-id="68417-116">Microsoft Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="68417-116">Microsoft Windows Server 2003</span></span><br/>                      | <span data-ttu-id="68417-117">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="68417-117">Windows Server 2003</span></span><br/>              |
| <span data-ttu-id="68417-118">Microsoft Active Directory-Anwendungsmodus (Adam)</span><span class="sxs-lookup"><span data-stu-id="68417-118">Microsoft Active Directory Application Mode (ADAM)</span></span><br/> | <span data-ttu-id="68417-119">Adam</span><span class="sxs-lookup"><span data-stu-id="68417-119">ADAM</span></span><br/>                             |
| <span data-ttu-id="68417-120">Microsoft Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="68417-120">Microsoft Windows Server 2003 R2</span></span><br/>                   | <span data-ttu-id="68417-121">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="68417-121">Windows Server 2003 R2</span></span><br/>           |
| <span data-ttu-id="68417-122">Microsoft Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68417-122">Microsoft Windows Server 2008</span></span><br/>                      | <span data-ttu-id="68417-123">Microsoft Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68417-123">Microsoft Windows Server 2008</span></span><br/>    |
| <span data-ttu-id="68417-124">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="68417-124">Microsoft Windows Server 2008 R2</span></span><br/>                   | <span data-ttu-id="68417-125">Microsoft Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="68417-125">Microsoft Windows Server 2008 R2</span></span><br/> |
| <span data-ttu-id="68417-126">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="68417-126">Microsoft Windows Server 2012</span></span><br/>                      | <span data-ttu-id="68417-127">Microsoft Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="68417-127">Microsoft Windows Server 2012</span></span><br/>    |



 

<span data-ttu-id="68417-128">Wenn ein Betriebssystem nicht im Thema aufgeführt ist, wird das Thema unter diesem Betriebssystem nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="68417-128">If an operating system is not listed in the topic, the topic is not supported on that operating system.</span></span> <span data-ttu-id="68417-129">Wenn beispielsweise ein Thema nur Windows Server 2003 und Adam auflistet, gilt das Thema nicht für Windows Server 2003 R2.</span><span class="sxs-lookup"><span data-stu-id="68417-129">For example, if a topic only lists Windows Server 2003 and ADAM, then the topic does not apply to Windows Server 2003 R2.</span></span>

<span data-ttu-id="68417-130">Die folgenden Abschnitte enthalten ausführliche Informationen zu den Active Directory Schema Elementen.</span><span class="sxs-lookup"><span data-stu-id="68417-130">The following sections contain detailed information about the Active Directory schema elements.</span></span>

-   [<span data-ttu-id="68417-131">Active Directory Schema-Terminologie</span><span class="sxs-lookup"><span data-stu-id="68417-131">Active Directory Schema Terminology</span></span>](active-directory-schema-site.md)
-   [<span data-ttu-id="68417-132">Klassen</span><span class="sxs-lookup"><span data-stu-id="68417-132">Classes</span></span>](classes.md)
-   [<span data-ttu-id="68417-133">Attribute</span><span class="sxs-lookup"><span data-stu-id="68417-133">Attributes</span></span>](attributes.md)
-   [<span data-ttu-id="68417-134">Syntaxen</span><span class="sxs-lookup"><span data-stu-id="68417-134">Syntaxes</span></span>](syntaxes.md)
-   [<span data-ttu-id="68417-135">Zugriffsrechte Steuern</span><span class="sxs-lookup"><span data-stu-id="68417-135">Control Access Rights</span></span>](control-access-rights.md)
-   [<span data-ttu-id="68417-136">RootDSE</span><span class="sxs-lookup"><span data-stu-id="68417-136">RootDSE</span></span>](rootdse.md)

 

