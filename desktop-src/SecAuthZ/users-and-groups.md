---
description: Erläutert die Definition von Benutzern und Gruppen in der Autorisierungs-Manager-API.
ms.assetid: 783be0b2-7894-4780-900d-98918f824a04
title: Benutzer und Gruppen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7c40ee9234fa8d6259282855011cfc3fc008d6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355447"
---
# <a name="users-and-groups"></a><span data-ttu-id="e95ea-103">Benutzer und Gruppen</span><span class="sxs-lookup"><span data-stu-id="e95ea-103">Users and Groups</span></span>

<span data-ttu-id="e95ea-104">Im Autorisierungs-Manager werden die Empfänger der Autorisierungs Richtlinie durch die folgenden Gruppen dargestellt:</span><span class="sxs-lookup"><span data-stu-id="e95ea-104">In Authorization Manager, recipients of authorization policy are represented by the following groups:</span></span>

-   <span data-ttu-id="e95ea-105">Windows-Benutzer und-Gruppen</span><span class="sxs-lookup"><span data-stu-id="e95ea-105">Windows Users and Groups</span></span>

    <span data-ttu-id="e95ea-106">Zu diesen Gruppen gehören Benutzer, Computer und integrierte Gruppen für Sicherheits Prinzipale.</span><span class="sxs-lookup"><span data-stu-id="e95ea-106">These groups include users, computers, and built-in groups for security principals.</span></span>

-   <span data-ttu-id="e95ea-107">LDAP-Abfrage Gruppen</span><span class="sxs-lookup"><span data-stu-id="e95ea-107">LDAP Query Groups</span></span>

    <span data-ttu-id="e95ea-108">Die Mitgliedschaft in diesen Gruppen wird nach Bedarf dynamisch in LDAP-Abfragen (Lightweight Directory Access Protocol) berechnet.</span><span class="sxs-lookup"><span data-stu-id="e95ea-108">Membership in these groups is dynamically calculated as needed from Lightweight Directory Access Protocol (LDAP) queries.</span></span> <span data-ttu-id="e95ea-109">Eine LDAP-Abfrage Gruppe ist ein Typ von Anwendungs Gruppe.</span><span class="sxs-lookup"><span data-stu-id="e95ea-109">An LDAP query group is a type of application group.</span></span>

-   <span data-ttu-id="e95ea-110">Grundlegende Anwendungs Gruppen</span><span class="sxs-lookup"><span data-stu-id="e95ea-110">Basic Application Groups</span></span>

    <span data-ttu-id="e95ea-111">Diese Gruppen bestehen aus LDAP-Abfrage Gruppen, Windows-Benutzern und-Gruppen und anderen grundlegenden Anwendungs Gruppen.</span><span class="sxs-lookup"><span data-stu-id="e95ea-111">These groups consist of LDAP query groups, Windows users and groups, and other basic application groups.</span></span>

## <a name="windows-users-and-groups"></a><span data-ttu-id="e95ea-112">Windows-Benutzer und-Gruppen</span><span class="sxs-lookup"><span data-stu-id="e95ea-112">Windows Users and Groups</span></span>

<span data-ttu-id="e95ea-113">Diese sind identisch mit den Benutzern und Gruppen, die im gesamten Windows-Betriebssystem verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e95ea-113">These are the same as the users and groups used throughout the Windows operating system.</span></span>

## <a name="ldap-query-groups"></a><span data-ttu-id="e95ea-114">LDAP-Abfrage Gruppen</span><span class="sxs-lookup"><span data-stu-id="e95ea-114">LDAP Query Groups</span></span>

<span data-ttu-id="e95ea-115">Im Autorisierungs-Manager können Sie LDAP-Abfragen verwenden, um die Attribute des Benutzers in Active Directory mit denen des Benutzer Objekts abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="e95ea-115">In Authorization Manager, you can use LDAP queries to match the user's attributes with those of the user's object in Active Directory.</span></span>

<span data-ttu-id="e95ea-116">Die folgende Abfrage findet z. b. alle außer Andy.</span><span class="sxs-lookup"><span data-stu-id="e95ea-116">For example, the following query finds everyone except Andy.</span></span>


```C++
(&(objectCategory=person)(objectClass=user)(!cn=andy))
```



<span data-ttu-id="e95ea-117">Die folgende Abfrage findet alle Member des Alias "jemand" unter www.fabrikam.com.</span><span class="sxs-lookup"><span data-stu-id="e95ea-117">The following query finds all members of the someone alias at www.fabrikam.com.</span></span>


```C++
(memberOf=CN=someone,OU=litwareinc,DC=Fabrikam,DC=com)
```



## <a name="basic-application-groups"></a><span data-ttu-id="e95ea-118">Grundlegende Anwendungs Gruppen</span><span class="sxs-lookup"><span data-stu-id="e95ea-118">Basic Application Groups</span></span>

<span data-ttu-id="e95ea-119">In der Autorisierungs-Manager-API wird eine Anwendungs Gruppe durch ein [**iazapplicationgroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) -Objekt dargestellt.</span><span class="sxs-lookup"><span data-stu-id="e95ea-119">In the Authorization Manager API, an application group is represented by an [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object.</span></span> <span data-ttu-id="e95ea-120">Eine einfache Anwendungs Gruppe ist eine Art von Anwendungs Gruppe.</span><span class="sxs-lookup"><span data-stu-id="e95ea-120">A basic application group is a type of application group.</span></span>

<span data-ttu-id="e95ea-121">Zum Definieren der grundlegenden Anwendungs Gruppenmitgliedschaft definieren Sie, wer ein Mitglied ist, und definieren, wer kein Mitglied ist.</span><span class="sxs-lookup"><span data-stu-id="e95ea-121">To define basic application group membership, define who is a member and define who is not a member.</span></span> <span data-ttu-id="e95ea-122">Beide Schritte werden auf die gleiche Weise ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e95ea-122">Both of these steps are carried out in the same way.</span></span> <span data-ttu-id="e95ea-123">Geben Sie 0 (null) oder mehr Windows-Benutzer und-Gruppen, zuvor definierte Basis Anwendungs Gruppen oder LDAP-Abfrage Gruppen an.</span><span class="sxs-lookup"><span data-stu-id="e95ea-123">Specify zero or more Windows users and groups, previously defined basic application groups, or LDAP query groups.</span></span> <span data-ttu-id="e95ea-124">Die Mitgliedschaft der Basis Anwendungs Gruppe wird berechnet, indem alle nicht Mitglieder aus der Gruppe entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="e95ea-124">The membership of the basic application group is calculated by removing any nonmembers from the group.</span></span> <span data-ttu-id="e95ea-125">Der Autorisierungs-Manager führt dies automatisch zur Laufzeit aus.</span><span class="sxs-lookup"><span data-stu-id="e95ea-125">Authorization Manager does this automatically at run time.</span></span>

<span data-ttu-id="e95ea-126">Die Nichtmitgliedschaft in einer grundlegenden Anwendungs Gruppe hat Vorrang vor der Mitgliedschaft.</span><span class="sxs-lookup"><span data-stu-id="e95ea-126">Nonmembership in a basic application group takes precedence over membership.</span></span>

<span data-ttu-id="e95ea-127">Zirkuläre Mitgliedschafts Definitionen sind nicht zulässig. Sie führen zu folgender Fehlermeldung: "GroupName kann nicht hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="e95ea-127">Circular membership definitions are not allowed; they result in the following error message: "Cannot add GroupName.</span></span> <span data-ttu-id="e95ea-128">Das folgende Problem ist aufgetreten: eine Schleife wurde erkannt. "</span><span class="sxs-lookup"><span data-stu-id="e95ea-128">The following problem occurred: A loop has been detected."</span></span>

## <a name="related-topics"></a><span data-ttu-id="e95ea-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e95ea-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e95ea-130">Definieren von Benutzergruppen in C++</span><span class="sxs-lookup"><span data-stu-id="e95ea-130">Defining Groups of Users in C++</span></span>](defining-groups-of-users-in-c--.md)
</dt> </dl>

 

 



