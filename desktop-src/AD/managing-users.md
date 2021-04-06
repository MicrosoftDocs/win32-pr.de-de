---
title: Verwalten von Benutzern
description: Benutzerkonten werden als Objekte in Active Directory Domain Services erstellt und gespeichert.
ms.assetid: 57c83e4d-2d9f-4f22-97e2-27e2d277f014
ms.tgt_platform: multiple
keywords:
- Active Directory, verwenden und Verwalten von Benutzern
- Benutzer-AD
- Benutzer AD, Verwalten von Benutzern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d1105132c6836e108a416331b2f4a6ad666c03d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855412"
---
# <a name="managing-users"></a><span data-ttu-id="27575-106">Verwalten von Benutzern</span><span class="sxs-lookup"><span data-stu-id="27575-106">Managing Users</span></span>

<span data-ttu-id="27575-107">Benutzerkonten werden als Objekte in Active Directory Domain Services erstellt und gespeichert.</span><span class="sxs-lookup"><span data-stu-id="27575-107">User accounts are created and stored as objects in Active Directory Domain Services.</span></span> <span data-ttu-id="27575-108">Diese Benutzer Objekte stellen Benutzer und Computer dar.</span><span class="sxs-lookup"><span data-stu-id="27575-108">These user objects represent users and computers.</span></span> <span data-ttu-id="27575-109">In diesem Abschnitt wird definiert, was Benutzer sind und wie Sie verwendet werden, und es wird erläutert, wie Benutzer in Active Directory Domain Services Programm gesteuert verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="27575-109">This section defines what users are and how they are used, and explains how to programmatically manage users in Active Directory Domain Services.</span></span> <span data-ttu-id="27575-110">In diesem Abschnitt werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="27575-110">This section discusses the following topics:</span></span>

-   [<span data-ttu-id="27575-111">Benutzer in Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="27575-111">Users in Active Directory Domain Services</span></span>](users-in-active-directory-domain-services.md)
-   [<span data-ttu-id="27575-112">Sicherheitsprinzipale</span><span class="sxs-lookup"><span data-stu-id="27575-112">Security Principals</span></span>](security-principals.md)
-   [<span data-ttu-id="27575-113">Was ist ein Benutzer?</span><span class="sxs-lookup"><span data-stu-id="27575-113">What is a User?</span></span>](what-is-a-user.md)
-   [<span data-ttu-id="27575-114">Beispiel Code für die Bindung an den Benutzer Container</span><span class="sxs-lookup"><span data-stu-id="27575-114">Example Code for Binding to the Users Container</span></span>](example-code-for-binding-to-the-users-container.md)
-   [<span data-ttu-id="27575-115">Benutzerobjekt Attribute</span><span class="sxs-lookup"><span data-stu-id="27575-115">User Object Attributes</span></span>](user-object-attributes.md)
-   [<span data-ttu-id="27575-116">Erstellen eines Benutzers</span><span class="sxs-lookup"><span data-stu-id="27575-116">Creating a User</span></span>](creating-a-user.md)
-   <span data-ttu-id="27575-117">Löschen eines Benutzers.</span><span class="sxs-lookup"><span data-stu-id="27575-117">Deleting a user.</span></span> <span data-ttu-id="27575-118">Ein Benutzer wird im gleichen wie ein beliebiges anderes Objekt in Active Directory Domain Services gelöscht.</span><span class="sxs-lookup"><span data-stu-id="27575-118">A user is deleted in the same was as any other object in Active Directory Domain Services.</span></span> <span data-ttu-id="27575-119">Weitere Informationen zum Löschen von Objekten finden Sie unter [Erstellen und Löschen von Objekten in Active Directory Domain Services](creating-and-deleting-objects-in-active-directory-domain-services.md).</span><span class="sxs-lookup"><span data-stu-id="27575-119">For more information about deleting objects, see [Creating and Deleting Objects in Active Directory Domain Services](creating-and-deleting-objects-in-active-directory-domain-services.md).</span></span>
-   [<span data-ttu-id="27575-120">Auflisten von Benutzern</span><span class="sxs-lookup"><span data-stu-id="27575-120">Enumerating Users</span></span>](enumerating-users.md)
-   [<span data-ttu-id="27575-121">Abfragen von Benutzern</span><span class="sxs-lookup"><span data-stu-id="27575-121">Querying for Users</span></span>](querying-for-users.md)
-   <span data-ttu-id="27575-122">Benutzer werden verschoben.</span><span class="sxs-lookup"><span data-stu-id="27575-122">Moving users.</span></span> <span data-ttu-id="27575-123">Ein Benutzer wird im gleichen wie ein beliebiges anderes Active Directory Objekt verschoben.</span><span class="sxs-lookup"><span data-stu-id="27575-123">A user is moved in the same was as any other Active Directory object.</span></span> <span data-ttu-id="27575-124">Weitere Informationen zum Verschieben von Active Directory Objekten finden Sie unter [Verschieben von Objekten](moving-objects.md).</span><span class="sxs-lookup"><span data-stu-id="27575-124">For more information about moving Active Directory objects, see [Moving Objects](moving-objects.md).</span></span>
-   [<span data-ttu-id="27575-125">Verwalten von Benutzern auf Mitglieds Servern und Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="27575-125">Managing Users on Member Servers and Windows 2000 Professional</span></span>](managing-users-on-member-servers-and-windows-2000-professional.md)

 

 




