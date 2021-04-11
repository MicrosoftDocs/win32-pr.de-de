---
description: Anweisungen zum Verwenden der Autorisierungs-Manager-API zum Definieren von Berechtigungen in Skripts durch Erstellen eines Autorisierungs Richtlinien Speicher.
ms.assetid: 114426e8-03a7-41e2-96c9-e2da91aa7d84
title: Definieren von Berechtigungen in Skripts
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e16f377ffa669da0b686ac28783e9a370efec94d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960328"
---
# <a name="defining-permissions-in-script"></a><span data-ttu-id="ca38f-103">Definieren von Berechtigungen in Skripts</span><span class="sxs-lookup"><span data-stu-id="ca38f-103">Defining Permissions in Script</span></span>

<span data-ttu-id="ca38f-104">Im Autorisierungs-Manager definieren Sie, welche Benutzer Zugriff auf welche Anwendungs Ressourcen haben, indem Sie einen Autorisierungs Richtlinien Speicher erstellen.</span><span class="sxs-lookup"><span data-stu-id="ca38f-104">In Authorization Manager, you define which users have access to which application resources by creating an authorization policy store.</span></span>

<span data-ttu-id="ca38f-105">**So definieren Sie Zugriffsberechtigungen**</span><span class="sxs-lookup"><span data-stu-id="ca38f-105">**To define access permissions**</span></span>

1.  <span data-ttu-id="ca38f-106">Erstellen Sie den Speicher, in dem die Autorisierungs Richtlinie definiert ist:</span><span class="sxs-lookup"><span data-stu-id="ca38f-106">Create the store where the authorization policy is defined:</span></span><dl>

[<span data-ttu-id="ca38f-107">Erstellen eines Autorisierungs Richtlinien Speicher im Skript</span><span class="sxs-lookup"><span data-stu-id="ca38f-107">Creating an Authorization Policy Store in Script</span></span>](creating-an-authorization-policy-store-object-in-script.md)  
    </dl>
2.  <span data-ttu-id="ca38f-108">Erstellen Sie im Autorisierungs Richtlinien Speicher einen Abschnitt für eine bestimmte Anwendung:</span><span class="sxs-lookup"><span data-stu-id="ca38f-108">Create a section in the authorization policy store for a specific application:</span></span><dl>

[<span data-ttu-id="ca38f-109">Erstellen eines Anwendungs Objekts im Skript</span><span class="sxs-lookup"><span data-stu-id="ca38f-109">Creating an Application Object in Script</span></span>](creating-an-application-object-in-script.md)  
    </dl>
3.  <span data-ttu-id="ca38f-110">Definieren von Vorgängen, die die Anwendung implementiert, um auf Ressourcen zuzugreifen und diese zu ändern</span><span class="sxs-lookup"><span data-stu-id="ca38f-110">Define operations that the application implements to access and modify resources:</span></span><dl>

[<span data-ttu-id="ca38f-111">Definieren von Vorgängen in Skripts</span><span class="sxs-lookup"><span data-stu-id="ca38f-111">Defining Operations in Script</span></span>](defining-operations-in-script.md)  
    </dl>
4.  <span data-ttu-id="ca38f-112">Gruppieren von Vorgängen in Aufgaben auf hoher Ebene, die von Benutzern ausgeführt werden sollen:</span><span class="sxs-lookup"><span data-stu-id="ca38f-112">Group operations into high-level tasks that users want to perform:</span></span><dl>

[<span data-ttu-id="ca38f-113">Gruppieren von Vorgängen in Aufgaben in Skripts</span><span class="sxs-lookup"><span data-stu-id="ca38f-113">Grouping Operations into Tasks in Script</span></span>](grouping-operations-into-tasks-in-script.md)  
    </dl>
5.  <span data-ttu-id="ca38f-114">Definieren von Rollen, die aus Gruppen von Aufgaben bestehen:</span><span class="sxs-lookup"><span data-stu-id="ca38f-114">Define roles that consist of groups of tasks:</span></span><dl>

[<span data-ttu-id="ca38f-115">Gruppieren von Aufgaben in Rollen in Skripts</span><span class="sxs-lookup"><span data-stu-id="ca38f-115">Grouping Tasks into Roles in Script</span></span>](grouping-tasks-into-roles-in-script.md)  
    </dl><span data-ttu-id="ca38f-116">Ein Benutzer, der einer Rolle zugewiesen ist, verfügt über die Berechtigung zum Ausführen beliebiger Aufgaben, die dieser Rolle zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="ca38f-116">A user that is assigned to a role has permission to perform any task assigned to that role.</span></span>
6.  <span data-ttu-id="ca38f-117">Erstellen Sie Skripts, um den Zugriff auf Aufgaben zur Laufzeit zu qualifizieren:</span><span class="sxs-lookup"><span data-stu-id="ca38f-117">Create scripts to qualify access to tasks at run time:</span></span><dl>

[<span data-ttu-id="ca38f-118">Qualifizieren des Zugriffs mit Geschäftslogik in Skripts</span><span class="sxs-lookup"><span data-stu-id="ca38f-118">Qualifying Access with Business Logic in Script</span></span>](qualifying-access-with-business-logic-in-script.md)  
    </dl><span data-ttu-id="ca38f-119">Dieser Schritt ist optional.</span><span class="sxs-lookup"><span data-stu-id="ca38f-119">This step is optional.</span></span>
7.  <span data-ttu-id="ca38f-120">Definieren von Benutzergruppen:</span><span class="sxs-lookup"><span data-stu-id="ca38f-120">Define groups of users:</span></span><dl>

[<span data-ttu-id="ca38f-121">Definieren von Benutzergruppen in Skripts</span><span class="sxs-lookup"><span data-stu-id="ca38f-121">Defining Groups of Users in Script</span></span>](defining-groups-of-users-in-script.md)  
    </dl><span data-ttu-id="ca38f-122">Diese Gruppen können dann Rollen zugewiesen werden, um zu bestimmen, welche Aufgaben Sie ausführen können.</span><span class="sxs-lookup"><span data-stu-id="ca38f-122">These groups can then be assigned to roles to determine which tasks they can perform.</span></span>
8.  <span data-ttu-id="ca38f-123">Benutzer zu Benutzergruppen hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="ca38f-123">Add users to user groups:</span></span><dl>

[<span data-ttu-id="ca38f-124">Hinzufügen von Benutzern zu einer Anwendungs Gruppe im Skript</span><span class="sxs-lookup"><span data-stu-id="ca38f-124">Adding Users to an Application Group in Script</span></span>](adding-users-to-an-application-group-in-script.md)  
    </dl>

 

 



