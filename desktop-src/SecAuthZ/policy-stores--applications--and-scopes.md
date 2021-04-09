---
description: Autorisierungs Richtlinien-Speicher,-Anwendungen und-Bereiche stellen verschiedene Organisationsebenen der Autorisierungs-Manager-Richtlinie dar.
ms.assetid: 235f236d-59c9-4a8c-aec6-60d1ddba4d5d
title: Richtlinien Speicher, Anwendungen und Bereiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4155d7bf60d34474d52c27efd50d2f53741fa73a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863027"
---
# <a name="policy-stores-applications-and-scopes"></a><span data-ttu-id="b0106-103">Richtlinien Speicher, Anwendungen und Bereiche</span><span class="sxs-lookup"><span data-stu-id="b0106-103">Policy Stores, Applications, and Scopes</span></span>

<span data-ttu-id="b0106-104">Autorisierungs Richtlinien-Speicher,-Anwendungen und-Bereiche stellen verschiedene Organisationsebenen der Autorisierungs-Manager-Richtlinie dar.</span><span class="sxs-lookup"><span data-stu-id="b0106-104">Authorization policy stores, applications, and scopes represent different levels of organization of Authorization Manager policy.</span></span> <span data-ttu-id="b0106-105">Ein Richtlinien Speicher kann eine oder mehrere Anwendungen enthalten, und eine Anwendung kann einen oder mehrere Bereiche enthalten.</span><span class="sxs-lookup"><span data-stu-id="b0106-105">A policy store can contain one or more applications, and an application can contain one or more scopes.</span></span>

-   [<span data-ttu-id="b0106-106">Autorisierungs Richtlinien Speicher</span><span class="sxs-lookup"><span data-stu-id="b0106-106">Authorization Policy Stores</span></span>](#authorization-policy-stores)
-   [<span data-ttu-id="b0106-107">Anwendungen</span><span class="sxs-lookup"><span data-stu-id="b0106-107">Applications</span></span>](#policy-stores-applications-and-scopes)
-   [<span data-ttu-id="b0106-108">Bereiche</span><span class="sxs-lookup"><span data-stu-id="b0106-108">Scopes</span></span>](#policy-stores-applications-and-scopes)
-   [<span data-ttu-id="b0106-109">Delegierung</span><span class="sxs-lookup"><span data-stu-id="b0106-109">Delegation</span></span>](#delegation)
-   [<span data-ttu-id="b0106-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b0106-110">Related topics</span></span>](#related-topics)

## <a name="authorization-policy-stores"></a><span data-ttu-id="b0106-111">Autorisierungs Richtlinien Speicher</span><span class="sxs-lookup"><span data-stu-id="b0106-111">Authorization Policy Stores</span></span>

<span data-ttu-id="b0106-112">In der Autorisierungs-Manager-API wird ein Autorisierungs Richtlinien Speicher durch ein [**IAzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) -Objekt dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b0106-112">In the Authorization Manager API, an authorization policy store is represented by an [**IAzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object.</span></span> <span data-ttu-id="b0106-113">Der Autorisierungs Richtlinien Speicher enthält Definitionen und Zuweisungen von Anwendungen, Bereichen, Vorgängen, Tasks, Rollen und Benutzergruppen.</span><span class="sxs-lookup"><span data-stu-id="b0106-113">The authorization policy store contains definitions and assignments of applications, scopes, operations, tasks, roles, and user groups.</span></span>

<span data-ttu-id="b0106-114">Ein Autorisierungs Richtlinien Speicher kann entweder als XML-Datei oder in Active Directory gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="b0106-114">An authorization policy store can be stored either as an XML file or in Active Directory.</span></span>

<span data-ttu-id="b0106-115">Eine Anwendung muss einen Autorisierungs Richtlinien Speicher initialisieren, bevor Sie Informationen im Speicher ändern oder die Store-Richtlinie verwenden, um den Client Zugriff auf Ressourcen zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="b0106-115">An application must initialize an authorization policy store before changing information in the store or using the store policy to check client access to resources.</span></span>

<span data-ttu-id="b0106-116">Ein Autorisierungs Richtlinien Speicher kann ein oder mehrere [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) -Objekte enthalten, die jeweils eine Autorisierungs Richtlinie für eine bestimmte Anwendung darstellen.</span><span class="sxs-lookup"><span data-stu-id="b0106-116">An authorization policy store can contain one or more [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) objects that each represent authorization policy for a specific application.</span></span>

## <a name="applications"></a><span data-ttu-id="b0106-117">Anwendungen</span><span class="sxs-lookup"><span data-stu-id="b0106-117">Applications</span></span>

<span data-ttu-id="b0106-118">In der Autorisierungs-Manager-API wird eine Anwendung durch ein [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) -Objekt dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b0106-118">In the Authorization Manager API, an application is represented by an [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) object.</span></span> <span data-ttu-id="b0106-119">Ein Autorisierungs Richtlinien Speicher kann Autorisierungs Richtlinien Informationen für viele Anwendungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="b0106-119">An authorization policy store can contain authorization policy information for many applications.</span></span> <span data-ttu-id="b0106-120">Mithilfe von **IAzApplication** -Objekten können Sie verschiedene Autorisierungs Richtlinien für unterschiedliche Anwendungen in einem einzelnen Richtlinien Speicher speichern.</span><span class="sxs-lookup"><span data-stu-id="b0106-120">Using **IAzApplication** objects allows you to store different authorization policy for different applications in a single policy store.</span></span>

<span data-ttu-id="b0106-121">Ein Autorisierungs Richtlinien Speicher muss mindestens eine Anwendung enthalten.</span><span class="sxs-lookup"><span data-stu-id="b0106-121">An authorization policy store must contain at least one application.</span></span>

## <a name="scopes"></a><span data-ttu-id="b0106-122">Bereiche</span><span class="sxs-lookup"><span data-stu-id="b0106-122">Scopes</span></span>

<span data-ttu-id="b0106-123">In der Autorisierungs-Manager-API wird ein Bereich durch ein [**iazscope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) -Objekt dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b0106-123">In the Authorization Manager API, a scope is represented by an [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) object.</span></span> <span data-ttu-id="b0106-124">Bereiche stellen eine zusätzliche, optionale Organisationsebene für eine Autorisierungs Richtlinie dar.</span><span class="sxs-lookup"><span data-stu-id="b0106-124">Scopes provide an additional, optional level of organization for an authorization policy.</span></span> <span data-ttu-id="b0106-125">Eine Anwendung kann einen oder mehrere Bereiche enthalten, muss jedoch keine enthalten (der Autorisierungs-Manager stellt einen standardmäßigen Anwendungs weiten Bereich bereit).</span><span class="sxs-lookup"><span data-stu-id="b0106-125">An application can contain one or more scopes, but need not contain any (Authorization Manager provides a default, application-wide scope).</span></span>

<span data-ttu-id="b0106-126">Ein Bereich ist eine Unterteilung innerhalb einer Anwendung, die Ressourcen von anderen Ressourcen trennt, die von dieser Anwendung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b0106-126">A scope is a subdivision within an application that separates resources from other resources that are used by that application.</span></span> <span data-ttu-id="b0106-127">Wenn Sie über Autorisierungs-Manager-Gruppen, Rollenzuweisungen, Rollen Definitionen oder Task Definitionen verfügen, die nicht auf eine gesamte Anwendung angewendet werden sollen, können Sie diese auf der Bereichs Ebene erstellen.</span><span class="sxs-lookup"><span data-stu-id="b0106-127">If you have Authorization Manager groups, role assignments, role definitions, or task definitions that you do not want to apply to an entire application, you can create them at the scope level.</span></span>

## <a name="delegation"></a><span data-ttu-id="b0106-128">Delegierung</span><span class="sxs-lookup"><span data-stu-id="b0106-128">Delegation</span></span>

<span data-ttu-id="b0106-129">In Active Directory gespeicherte Autorisierungs Richtlinien Speicher unterstützen die Delegierung der Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="b0106-129">Authorization policy stores that are stored in Active Directory support delegation of administration.</span></span> <span data-ttu-id="b0106-130">Die Verwaltung kann an Benutzer und Gruppen auf Geschäfts-, Anwendungs-oder Bereichs Ebene delegiert werden.</span><span class="sxs-lookup"><span data-stu-id="b0106-130">Administration can be delegated to users and groups at the store, application, or scope level.</span></span> <span data-ttu-id="b0106-131">Jede Ebene definiert administrative Rollen für die Richtlinie auf dieser Ebene.</span><span class="sxs-lookup"><span data-stu-id="b0106-131">Each level defines administrative roles for the policy at that level.</span></span> <span data-ttu-id="b0106-132">Wenn Sie die Steuerung an einen Benutzer oder eine Gruppe delegieren möchten, weisen Sie Sie der Administrator Rolle zu. damit ein Benutzer oder eine Gruppe die Richtlinie lesen kann, weisen Sie Sie der Rolle "Leser" zu.</span><span class="sxs-lookup"><span data-stu-id="b0106-132">To delegate control to a user or group, assign them to the administrator role; to allow a user or group to read the policy, assign them to the reader role.</span></span>

<span data-ttu-id="b0106-133">Administratoren eines Stores, einer Anwendung oder eines Bereichs können den Richtlinien Speicher auf der Delegierten Ebene lesen und ändern.</span><span class="sxs-lookup"><span data-stu-id="b0106-133">Administrators of a store, application, or scope can read and modify the policy store at the delegated level.</span></span> <span data-ttu-id="b0106-134">Leser können den Richtlinien Speicher auf der Delegierten Ebene lesen, den Speicher jedoch nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="b0106-134">Readers can read the policy store at the delegated level but cannot modify the store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0106-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b0106-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0106-136">Erstellen eines Autorisierungs Richtlinien-Speicher Objekts in C++</span><span class="sxs-lookup"><span data-stu-id="b0106-136">Creating an Authorization Policy Store Object in C++</span></span>](creating-an-authorization-policy-store-object-in-c--.md)
</dt> <dt>

[<span data-ttu-id="b0106-137">Erstellen eines Anwendungs Objekts in C++</span><span class="sxs-lookup"><span data-stu-id="b0106-137">Creating an Application Object in C++</span></span>](creating-an-application-object-in-c--.md)
</dt> <dt>

[<span data-ttu-id="b0106-138">Delegieren der definierenden Berechtigungen in C++</span><span class="sxs-lookup"><span data-stu-id="b0106-138">Delegating the Defining of Permissions in C++</span></span>](delegating-the-defining-of-permissions-in-c--.md)
</dt> </dl>

 

 



