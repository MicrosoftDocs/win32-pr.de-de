---
title: Verwendung von Sicherheitsgruppen in Access Control
description: Die Sicherheits-ID (SID) ist der Objekt Bezeichner des Benutzers oder der Sicherheitsgruppe, wenn der Benutzer oder die Gruppe zu Sicherheitszwecken verwendet wird.
ms.assetid: 3236c51f-21c1-4c07-9b76-2668ae72a42f
ms.tgt_platform: multiple
keywords:
- Verwendung von Sicherheitsgruppen in Access Control
- Zugriffs Steuerung, Sicherheitsgruppen, die in verwendet werden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf7096e32c64fe420ca6625378725ce8e4864beb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337753"
---
# <a name="how-security-groups-are-used-in-access-control"></a><span data-ttu-id="8a911-105">Verwendung von Sicherheitsgruppen in Access Control</span><span class="sxs-lookup"><span data-stu-id="8a911-105">How Security Groups are Used in Access Control</span></span>

<span data-ttu-id="8a911-106">Die Sicherheits-ID (SID) ist der Objekt Bezeichner des Benutzers oder der Sicherheitsgruppe, wenn der Benutzer oder die Gruppe zu Sicherheitszwecken verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8a911-106">The security identifier (SID) is the object identifier of the user or security group when the user or group is used for security purposes.</span></span> <span data-ttu-id="8a911-107">Der Name des Benutzers oder der Gruppe wird nicht als eindeutiger Bezeichner innerhalb des Systems verwendet.</span><span class="sxs-lookup"><span data-stu-id="8a911-107">The name of the user or group is not used as the unique identifier within the system.</span></span> <span data-ttu-id="8a911-108">Die SID wird im **objectSID** -Attribut von Benutzer Objekten und Sicherheitsgruppen Objekten gespeichert.</span><span class="sxs-lookup"><span data-stu-id="8a911-108">The SID is stored in the **objectSid** attribute of user objects and security group objects.</span></span> <span data-ttu-id="8a911-109">Der Active Directory Server generiert die **objectSID** , wenn der Benutzer oder die Gruppe erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="8a911-109">The Active Directory server generates the **objectSid** when the user or group is created.</span></span> <span data-ttu-id="8a911-110">Das System stellt sicher, dass die SIDs innerhalb einer Gesamtstruktur eindeutig sind.</span><span class="sxs-lookup"><span data-stu-id="8a911-110">The system ensures that the SIDs are unique across a forest.</span></span> <span data-ttu-id="8a911-111">Beachten Sie, dass es sich bei **objectGUID** um den eindeutigen Bezeichner eines Benutzers, einer Gruppe oder eines beliebigen anderen Verzeichnis Objekts handelt.</span><span class="sxs-lookup"><span data-stu-id="8a911-111">Be aware that the **objectGuid** is the unique identifier of a user, group, or any other directory object.</span></span> <span data-ttu-id="8a911-112">Die SID ändert sich, wenn ein Benutzer oder eine Gruppe in eine andere Domäne verschoben wird. die **objectGUID** bleibt unverändert.</span><span class="sxs-lookup"><span data-stu-id="8a911-112">The SID changes if a user or group is moved to another domain; the **objectGuid** remains the same.</span></span>

<span data-ttu-id="8a911-113">Wenn einem Benutzer oder einer Gruppe die Berechtigung für den Zugriff auf eine Ressource, z. b. ein Drucker oder eine Dateifreigabe, erteilt wird, wird die SID des Benutzers oder der Gruppe zum Zugriffs Steuerungs Eintrag (Access Control Entry, ACE) hinzugefügt, der die gewährte Berechtigung in der freigegebenen Zugriffs Steuerungs Liste (DACL) der Ressource definiert.</span><span class="sxs-lookup"><span data-stu-id="8a911-113">When a user or group is given permission to access a resource, such as a printer or a file share, the SID of the user or group is added to the access control entry (ACE) defining the granted permission in the resource's discretionary access control list (DACL).</span></span> <span data-ttu-id="8a911-114">In Active Directory Domain Services verfügt jedes Objekt über ein **ntSecurityDescriptor** -Attribut, das eine DACL speichert, die den Zugriff auf das jeweilige Objekt oder die Attribute für dieses Objekt definiert.</span><span class="sxs-lookup"><span data-stu-id="8a911-114">In Active Directory Domain Services, each object has an **nTSecurityDescriptor** attribute that stores a DACL defining the access to that particular object or attributes on that object.</span></span> <span data-ttu-id="8a911-115">Weitere Informationen zum Festlegen der Zugriffs Steuerung für Objekte in Active Directory Domain Services finden [Sie Untersteuern des Zugriffs auf Objekte in Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md).</span><span class="sxs-lookup"><span data-stu-id="8a911-115">For more information about setting access control on objects in Active Directory Domain Services, see [Controlling Access to Objects in Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md).</span></span>

<span data-ttu-id="8a911-116">Wenn sich ein Benutzer bei einer Windows 2000-Domäne anmeldet, generiert das Betriebssystem ein Zugriffs Token.</span><span class="sxs-lookup"><span data-stu-id="8a911-116">When a user logs on to a Windows 2000 domain, the operating system generates an access token.</span></span> <span data-ttu-id="8a911-117">Dieses Zugriffs Token wird verwendet, um zu bestimmen, auf welche Ressourcen der Benutzer zugreifen darf.</span><span class="sxs-lookup"><span data-stu-id="8a911-117">This access token is used to determine which resources the user may access.</span></span> <span data-ttu-id="8a911-118">Das Benutzer Zugriffs Token enthält die folgenden Daten:</span><span class="sxs-lookup"><span data-stu-id="8a911-118">The user access token includes the following data:</span></span>

-   <span data-ttu-id="8a911-119">Benutzer-SID.</span><span class="sxs-lookup"><span data-stu-id="8a911-119">User SID.</span></span>
-   <span data-ttu-id="8a911-120">SIDs aller globalen und universellen Sicherheitsgruppen, in denen der Benutzer Mitglied ist.</span><span class="sxs-lookup"><span data-stu-id="8a911-120">SIDs of all global and universal security groups that the user is a member of.</span></span>
-   <span data-ttu-id="8a911-121">SIDs aller nellen globalen und universellen Sicherheitsgruppen.</span><span class="sxs-lookup"><span data-stu-id="8a911-121">SIDs of all nested global and universal security groups.</span></span>

<span data-ttu-id="8a911-122">Jeder Prozess, der für diesen Benutzer ausgeführt wird, verfügt über eine Kopie dieses Zugriffs Tokens.</span><span class="sxs-lookup"><span data-stu-id="8a911-122">Every process executed on behalf of this user has a copy of this access token.</span></span>

<span data-ttu-id="8a911-123">Wenn der Benutzer versucht, auf Ressourcen auf einem Computer zuzugreifen, nimmt der Dienst, über den der Benutzer auf die Ressource zugreift, die Identität des Benutzers an, indem ein neues Zugriffs Token basierend auf dem Zugriffs Token erstellt wird, das zum Zeitpunkt der Benutzeranmeldung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="8a911-123">When the user attempts to access resources on a computer, the service through which the user accesses the resource will impersonate the user by creating a new access token based on the access token created at user logon time.</span></span> <span data-ttu-id="8a911-124">Dieses neue Zugriffs Token enthält auch die folgenden SIDs:</span><span class="sxs-lookup"><span data-stu-id="8a911-124">This new access token will also contain the following SIDs:</span></span>

-   <span data-ttu-id="8a911-125">SIDs für alle lokalen Domänen Gruppen in der Zieldomäne, in der der Benutzer Mitglied ist.</span><span class="sxs-lookup"><span data-stu-id="8a911-125">SIDs for all domain local groups in the target domain that the user is a member of.</span></span>
-   <span data-ttu-id="8a911-126">SIDs für alle lokalen Computer Gruppen auf dem Zielcomputer, in denen der Benutzer Mitglied ist.</span><span class="sxs-lookup"><span data-stu-id="8a911-126">SIDs for all machine local groups on the target computer that the user is a member of.</span></span>

<span data-ttu-id="8a911-127">Der Dienst verwendet dieses neue Zugriffs Token, um den Zugriff auf die Ressource auszuwerten.</span><span class="sxs-lookup"><span data-stu-id="8a911-127">The service uses this new access token to evaluate access to the resource.</span></span> <span data-ttu-id="8a911-128">Wenn eine SID im Zugriffs Token in einem ACEs in der DACL angezeigt wird, erteilt der Dienst dem Benutzer die Berechtigungen, die in diesen ACEs angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="8a911-128">If a SID in the access token appears in any ACEs in the DACL, the service gives the user the permissions specified in those ACEs.</span></span>

 

 




