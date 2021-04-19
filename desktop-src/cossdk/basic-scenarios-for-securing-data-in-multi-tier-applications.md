---
description: In diesem Thema werden einige Baustein Szenarien vorgestellt, in denen die Kriterien erläutert werden, die unter entscheiden, wo Sicherheit erzwungen werden soll.
ms.assetid: e9820e53-8891-4bff-a333-00ad2dbb03a4
title: Grundlegende Szenarien zum Sichern von Daten in Anwendungen mit mehreren Ebenen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7929bcfeba96b43b7ec91513b42ffb7f46266613
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346240"
---
# <a name="basic-scenarios-for-securing-data-in-multi-tier-applications"></a><span data-ttu-id="945f5-103">Grundlegende Szenarien zum Sichern von Daten in Anwendungen mit mehreren Ebenen</span><span class="sxs-lookup"><span data-stu-id="945f5-103">Basic Scenarios for Securing Data in Multi-Tier Applications</span></span>

<span data-ttu-id="945f5-104">In diesem Thema werden einige Baustein Szenarien vorgestellt, in denen die Kriterien erläutert werden, die unter [entscheiden, wo Sicherheit](deciding-where-to-enforce-security.md)erzwungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="945f5-104">This topic presents a few building-block scenarios, illustrating the criteria discussed in [Deciding Where to Enforce Security](deciding-where-to-enforce-security.md).</span></span>

## <a name="trusted-server-scenario"></a><span data-ttu-id="945f5-105">Szenario des vertrauenswürdigen Servers</span><span class="sxs-lookup"><span data-stu-id="945f5-105">Trusted Server Scenario</span></span>

-   <span data-ttu-id="945f5-106">Die-Datenbank vertraut der com+-Anwendung vollständig, um Endbenutzern den Zugriff auf Daten in der Datenbank zu authentifizieren und zu autorisieren.</span><span class="sxs-lookup"><span data-stu-id="945f5-106">The database fully trusts the COM+ application to authenticate and authorize end users to access data in the database.</span></span>
-   <span data-ttu-id="945f5-107">Vorzugsweise ist die Datenbank vor allen Zugriffen geschützt, außer über die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="945f5-107">Preferably, the database is secured against any access except through the application.</span></span>
-   <span data-ttu-id="945f5-108">Die COM+-Anwendung verwendet rollenbasierte Sicherheit, um Benutzer zu autorisieren.</span><span class="sxs-lookup"><span data-stu-id="945f5-108">The COM+ application uses role-based security to authorize users.</span></span>
-   <span data-ttu-id="945f5-109">Verbindungen werden unter der com+-Anwendungs Identität geöffnet und können vollständig gebündelt werden.</span><span class="sxs-lookup"><span data-stu-id="945f5-109">Connections are opened under the COM+ application's identity and are fully poolable.</span></span>
-   <span data-ttu-id="945f5-110">Überwachung und Protokollierung können von der com+-Anwendung ausgeführt werden, oder diese Informationen können von der Anwendung an die Datenbank übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="945f5-110">Auditing and logging can be done by the COM+ application, or this information can be passed into the database by the application.</span></span>

<span data-ttu-id="945f5-111">Dieses Szenario eignet sich am besten für Daten, auf die über vorhersagbare Benutzer Kategorien zugegriffen werden kann, die in Rollen gekapselt werden können.</span><span class="sxs-lookup"><span data-stu-id="945f5-111">This scenario works best for data that can be accessed by predictable categories of users that can be encapsulated in roles.</span></span> <span data-ttu-id="945f5-112">Beispielsweise haben nur "Manager", "Kassierer" und "Buchhaltung" Berechtigungen für den Zugriff auf Konten.</span><span class="sxs-lookup"><span data-stu-id="945f5-112">For example, only "Managers," "Tellers," and "Accountants" have permission to access accounts.</span></span> <span data-ttu-id="945f5-113">Die Geschäftslogik, für die genau jede aktiviert ist, wird in der mittleren Ebene erzwungen.</span><span class="sxs-lookup"><span data-stu-id="945f5-113">The business logic of what precisely each is enabled to do is enforced in the middle tier.</span></span>

## <a name="impersonation-scenario"></a><span data-ttu-id="945f5-114">Identitätswechsel Szenario</span><span class="sxs-lookup"><span data-stu-id="945f5-114">Impersonation Scenario</span></span>

-   <span data-ttu-id="945f5-115">Die Datenbank übernimmt eine eigene Authentifizierung und Autorisierung von Endbenutzern, um den Zugriff auf Daten in der Datenbank einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="945f5-115">The database does its own authentication and authorization of end users to help limit access to data in the database.</span></span>
-   <span data-ttu-id="945f5-116">Die COM+-Anwendung nimmt die Identität der Clients an, wenn Sie auf die Datenbank zugreift.</span><span class="sxs-lookup"><span data-stu-id="945f5-116">The COM+ application impersonates clients whenever it is accessing the database.</span></span>
-   <span data-ttu-id="945f5-117">Verbindungen werden pro Rückruf hergestellt und können nicht wieder verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="945f5-117">Connections are made on a per-call basis and can't be reused.</span></span>

<span data-ttu-id="945f5-118">Dieses Szenario eignet sich am besten für Daten, die eng an sehr kleine Benutzer Klassen gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="945f5-118">This scenario works best for data that is closely bound to very small classes of users.</span></span> <span data-ttu-id="945f5-119">Beispielsweise kann jeder Mitarbeiter nur auf seine eigene Personal Datei zugreifen, und jeder Manager kann nur auf die Personaldateien der Berichte zugreifen.</span><span class="sxs-lookup"><span data-stu-id="945f5-119">For example, each employee can access only his own personnel file, and each manager can access only the personnel files of her reports.</span></span>

## <a name="hybrid-scenario"></a><span data-ttu-id="945f5-120">Hybrid Szenario</span><span class="sxs-lookup"><span data-stu-id="945f5-120">Hybrid Scenario</span></span>

<span data-ttu-id="945f5-121">Eine Kombination der beiden vorangehenden Szenarien, bei denen der Identitätswechsel nur bei Bedarf verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="945f5-121">A combination of the preceding two scenarios, where impersonation is used only when it is needed.</span></span>

<span data-ttu-id="945f5-122">Dieses Szenario funktioniert am besten in Situationen, in denen Sie über hybride Benutzerdaten Beziehungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="945f5-122">This scenario works best in situations where you have hybrid user-data relationships.</span></span> <span data-ttu-id="945f5-123">Sie haben z. b. "Manager", "Kassierer", "Buchhaltung" und Tausende von einzelnen Webclients, die nur auf Ihre eigenen Konten zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="945f5-123">For example, you have "Managers," "Tellers," "Accountants," and thousands of individual Web clients who can access just their own accounts.</span></span> <span data-ttu-id="945f5-124">Sie können Logik Pfade durch die Anwendung, möglicherweise mit separaten Komponenten, trennen, um die letztgenannte Benutzerklasse zu verarbeiten, insbesondere dann, wenn sich die Leistungs Annahmen für diese Benutzer unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="945f5-124">You can separate logic paths through the application, potentially with separate components, to handle the latter class of users, particularly where performance assumptions for those users are different.</span></span>

## <a name="trusted-scenario-using-microsoft-sql-server-roles"></a><span data-ttu-id="945f5-125">Vertrauenswürdiges Szenario mit Microsoft SQL Server Rollen</span><span class="sxs-lookup"><span data-stu-id="945f5-125">Trusted Scenario Using Microsoft SQL Server Roles</span></span>

-   <span data-ttu-id="945f5-126">Microsoft SQL Server 7,0 und höher kann den Zugriff auf bestimmte Zeilen mithilfe von Rollen autorisieren, vertraut jedoch der com+-Anwendung, um Benutzer zu authentifizieren und zu autorisieren und Sie den richtigen Rollen in der Datenbank zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="945f5-126">Microsoft SQL Server 7.0 and later can authorize access to specific rows using roles but trusts the COM+ application to authenticate and authorize users and to map them to the correct roles in the database.</span></span>
-   <span data-ttu-id="945f5-127">Die COM+-Anwendung autorisiert Benutzer mithilfe der rollenbasierten Sicherheit, und die Anwendungs Rollen entsprechen den Daten bankrollen.</span><span class="sxs-lookup"><span data-stu-id="945f5-127">The COM+ application authorizes users using role-based security, and the application roles correspond well to database roles.</span></span>
-   <span data-ttu-id="945f5-128">Verbindungen können für eine bestimmte Daten Bank Rolle geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="945f5-128">Connections can be opened that are specific to a particular database role.</span></span> <span data-ttu-id="945f5-129">Diese Verbindungen können wieder verwendet werden, wenn Sie von in einem Pool zusammengefassten Objekten in den COM+-Anwendungen aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="945f5-129">These connections can be reused if they are held by pooled objects in the COM+ applications.</span></span> <span data-ttu-id="945f5-130">Weitere Informationen hierzu finden Sie unter [com+-Objekt Pooling](com--object-pooling.md).</span><span class="sxs-lookup"><span data-stu-id="945f5-130">For details on how to do this, see [COM+ Object Pooling](com--object-pooling.md).</span></span>
-   <span data-ttu-id="945f5-131">Überwachung und Protokollierung können von der com+-Anwendung durchgeführt werden, oder diese Informationen können von der Anwendung an die Datenbank übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="945f5-131">Auditing and logging can be done by the COM+ application, or this information can be passed in to the database by the application.</span></span>

<span data-ttu-id="945f5-132">Dieses Szenario eignet sich am besten für dieselben Benutzer und Daten wie für das erste vertrauenswürdige Server Szenario, da die COM+-Anwendung immer noch vertrauenswürdig ist, um die Autorisierung ordnungsgemäß zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="945f5-132">This scenario works best for generally the same kinds of users and data as in the first trusted server scenario because the COM+ application is still being largely trusted to handle authorization correctly.</span></span> <span data-ttu-id="945f5-133">Allerdings schützt Sie die Datenbank vor nicht autorisiertem Zugriff und ermöglicht gleichzeitig den Zugriff von mehreren Quellen außerhalb der com+-Anwendung, ohne dass die Skalierungs-und Leistungseinbußen beim Identitätswechsel Szenario anfallen.</span><span class="sxs-lookup"><span data-stu-id="945f5-133">However, it does help protect the database against unauthorized access while allowing access potentially from multiple sources outside the COM+ application, without incurring the scaling and performance penalties present with the impersonation scenario.</span></span>

## <a name="related-topics"></a><span data-ttu-id="945f5-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="945f5-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="945f5-135">Festlegen der Erzwingung der Sicherheit</span><span class="sxs-lookup"><span data-stu-id="945f5-135">Deciding Where to Enforce Security</span></span>](deciding-where-to-enforce-security.md)
</dt> <dt>

[<span data-ttu-id="945f5-136">Multi-Tier-Anwendungssicherheit</span><span class="sxs-lookup"><span data-stu-id="945f5-136">Multi-Tier Application Security</span></span>](multi-tier-application-security.md)
</dt> </dl>

 

 



