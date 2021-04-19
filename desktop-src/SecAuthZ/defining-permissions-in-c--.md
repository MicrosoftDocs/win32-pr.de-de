---
description: Anweisungen zum Verwenden der Autorisierungs-Manager-API zum Definieren von Berechtigungen in C++ durch Erstellen eines Autorisierungs Richtlinien Speicher.
ms.assetid: 8a3bf625-7973-4905-a63c-e42e6682b7c2
title: Definieren von Berechtigungen in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc398d811f44b69dbde8d30f135fd4f30a552bbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366518"
---
# <a name="defining-permissions-in-c"></a><span data-ttu-id="16828-103">Definieren von Berechtigungen in C++</span><span class="sxs-lookup"><span data-stu-id="16828-103">Defining Permissions in C++</span></span>

<span data-ttu-id="16828-104">Im Autorisierungs-Manager definieren Sie, welche Benutzer Zugriff auf welche Anwendungs Ressourcen haben, indem Sie einen Autorisierungs Richtlinien Speicher erstellen.</span><span class="sxs-lookup"><span data-stu-id="16828-104">In Authorization Manager, you define which users have access to which application resources by creating an authorization policy store.</span></span>

<span data-ttu-id="16828-105">Informationen zum Definieren von Berechtigungen mit Zugriffs Steuerungs Listen finden Sie unter [Definieren von Berechtigungen mit ACLs in C++](defining-permissions-with-acls-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="16828-105">For information about defining permissions with ACLs, see [Defining Permissions with ACLs in C++](defining-permissions-with-acls-in-c--.md).</span></span>

<span data-ttu-id="16828-106">**So definieren Sie Zugriffsberechtigungen**</span><span class="sxs-lookup"><span data-stu-id="16828-106">**To define access permissions**</span></span>

1.  <span data-ttu-id="16828-107">Erstellen Sie den Speicher, in dem die Autorisierungs Richtlinie definiert ist:</span><span class="sxs-lookup"><span data-stu-id="16828-107">Create the store where the authorization policy is defined:</span></span><dl>

[<span data-ttu-id="16828-108">Erstellen eines Autorisierungs Richtlinien-Speicher Objekts in C++</span><span class="sxs-lookup"><span data-stu-id="16828-108">Creating an Authorization Policy Store Object in C++</span></span>](creating-an-authorization-policy-store-object-in-c--.md)  
    </dl>
2.  <span data-ttu-id="16828-109">Erstellen Sie im Autorisierungs Richtlinien Speicher einen Abschnitt für eine bestimmte Anwendung:</span><span class="sxs-lookup"><span data-stu-id="16828-109">Create a section in the authorization policy store for a specific application:</span></span><dl>

[<span data-ttu-id="16828-110">Erstellen eines Anwendungs Objekts in C++</span><span class="sxs-lookup"><span data-stu-id="16828-110">Creating an Application Object in C++</span></span>](creating-an-application-object-in-c--.md)  
    </dl>
3.  <span data-ttu-id="16828-111">Definieren von Vorgängen, die die Anwendung implementiert, um auf Ressourcen zuzugreifen und diese zu ändern</span><span class="sxs-lookup"><span data-stu-id="16828-111">Define operations that the application implements to access and modify resources:</span></span><dl>

[<span data-ttu-id="16828-112">Definieren von Vorgängen in C++</span><span class="sxs-lookup"><span data-stu-id="16828-112">Defining Operations in C++</span></span>](defining-operations-in-c--.md)  
    </dl>
4.  <span data-ttu-id="16828-113">Gruppieren von Vorgängen in Aufgaben auf hoher Ebene, die von Benutzern ausgeführt werden sollen:</span><span class="sxs-lookup"><span data-stu-id="16828-113">Group operations into high-level tasks that users want to perform:</span></span><dl>

[<span data-ttu-id="16828-114">Gruppieren von Vorgängen in Aufgaben in C++</span><span class="sxs-lookup"><span data-stu-id="16828-114">Grouping Operations into Tasks in C++</span></span>](grouping-operations-into-tasks-in-c--.md)  
    </dl>
5.  <span data-ttu-id="16828-115">Definieren von Rollen, die aus Gruppen von Aufgaben bestehen:</span><span class="sxs-lookup"><span data-stu-id="16828-115">Define roles that consist of groups of tasks:</span></span><dl>

[<span data-ttu-id="16828-116">Gruppieren von Aufgaben in Rollen in C++</span><span class="sxs-lookup"><span data-stu-id="16828-116">Grouping Tasks into Roles in C++</span></span>](grouping-tasks-into-roles-in-c--.md)  
    </dl><span data-ttu-id="16828-117">Ein Benutzer, der einer Rolle zugewiesen ist, verfügt über die Berechtigung zum Ausführen beliebiger Aufgaben, die dieser Rolle zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="16828-117">A user that is assigned to a role has permission to perform any task assigned to that role.</span></span>
6.  <span data-ttu-id="16828-118">Erstellen Sie Skripts, um den Zugriff auf Aufgaben zur Laufzeit zu qualifizieren:</span><span class="sxs-lookup"><span data-stu-id="16828-118">Create scripts to qualify access to tasks at run time:</span></span><dl>

[<span data-ttu-id="16828-119">Qualifizieren des Zugriffs mit Geschäftslogik in C++</span><span class="sxs-lookup"><span data-stu-id="16828-119">Qualifying Access with Business Logic in C++</span></span>](qualifying-access-with-business-logic-in-c--.md)  
    </dl><span data-ttu-id="16828-120">Dieser Schritt ist optional.</span><span class="sxs-lookup"><span data-stu-id="16828-120">This step is optional.</span></span>
7.  <span data-ttu-id="16828-121">Definieren von Benutzergruppen:</span><span class="sxs-lookup"><span data-stu-id="16828-121">Define groups of users:</span></span><dl>

[<span data-ttu-id="16828-122">Definieren von Benutzergruppen in C++</span><span class="sxs-lookup"><span data-stu-id="16828-122">Defining Groups of Users in C++</span></span>](defining-groups-of-users-in-c--.md)  
    </dl><span data-ttu-id="16828-123">Diese Gruppen können dann Rollen zugewiesen werden, um zu bestimmen, welche Aufgaben Sie ausführen können.</span><span class="sxs-lookup"><span data-stu-id="16828-123">These groups can then be assigned to roles to determine which tasks they can perform.</span></span>
8.  <span data-ttu-id="16828-124">Benutzer zu Benutzergruppen hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="16828-124">Add users to user groups:</span></span><dl>

[<span data-ttu-id="16828-125">Hinzufügen von Benutzern zu einer Anwendungs Gruppe in C++</span><span class="sxs-lookup"><span data-stu-id="16828-125">Adding Users to an Application Group in C++</span></span>](adding-users-to-an-application-group-in-c--.md)  
    </dl>

 

 



