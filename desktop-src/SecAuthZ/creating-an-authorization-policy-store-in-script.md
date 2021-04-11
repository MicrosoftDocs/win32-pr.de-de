---
description: Anweisungen zum Verwenden der Autorisierungs-Manager-API zum Erstellen eines Autorisierungs Richtlinien Speicher im Skript.
ms.assetid: bd9a995a-4195-4da4-a194-472448a0cb08
title: Erstellen eines Autorisierungs Richtlinien Speicher im Skript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c0cb35e8e998f95e99193d1dc5e8a74838b7efc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130656"
---
# <a name="creating-an-authorization-policy-store-in-script"></a><span data-ttu-id="2c94d-103">Erstellen eines Autorisierungs Richtlinien Speicher im Skript</span><span class="sxs-lookup"><span data-stu-id="2c94d-103">Creating an Authorization Policy Store in Script</span></span>

<span data-ttu-id="2c94d-104">Erstellen Sie eine Autorisierungs Richtlinie vor oder während der Installation einer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="2c94d-104">Create an authorization policy before or during the installation of an application.</span></span>

<span data-ttu-id="2c94d-105">Wenn Sie die Autorisierungs-Manager-API verwenden, um eine Autorisierungs Richtlinie zu erstellen, befolgen Sie die Anweisungen in den folgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="2c94d-105">When you use the Authorization Manager API to create an authorization policy, follow the instructions provided in the following topics.</span></span>



| <span data-ttu-id="2c94d-106">Thema</span><span class="sxs-lookup"><span data-stu-id="2c94d-106">Topic</span></span>                                                                                                                  | <span data-ttu-id="2c94d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2c94d-107">Description</span></span>                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c94d-108">Erstellen eines Autorisierungs Richtlinien-Speicher Objekts im Skript</span><span class="sxs-lookup"><span data-stu-id="2c94d-108">Creating an Authorization Policy Store Object in Script</span></span>](creating-an-authorization-policy-store-object-in-script.md) | <span data-ttu-id="2c94d-109">Ein Autorisierungs Richtlinien Speicher enthält Informationen über die Sicherheitsrichtlinie einer Anwendung oder Gruppe von Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="2c94d-109">An authorization policy store contains information about the security policy of an application or group of applications.</span></span>                                                                                                                                       |
| [<span data-ttu-id="2c94d-110">Erstellen eines Anwendungs Objekts im Skript</span><span class="sxs-lookup"><span data-stu-id="2c94d-110">Creating an Application Object in Script</span></span>](creating-an-application-object-in-script.md)                               | <span data-ttu-id="2c94d-111">Für jede Anwendung, die einen Autorisierungs Richtlinien Speicher verwendet, müssen Sie ein [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) -Objekt erstellen und in einem Richtlinien Speicher speichern.</span><span class="sxs-lookup"><span data-stu-id="2c94d-111">For each application that uses an authorization policy store, you must create an [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) object and save it to a policy store.</span></span>                                                                                                |
| [<span data-ttu-id="2c94d-112">Definieren von Vorgängen in Skripts</span><span class="sxs-lookup"><span data-stu-id="2c94d-112">Defining Operations in Script</span></span>](defining-operations-in-script.md)                                                     | <span data-ttu-id="2c94d-113">Bei einem Vorgang handelt es sich um eine Funktion oder Methode einer Anwendung auf niedriger Ebene.</span><span class="sxs-lookup"><span data-stu-id="2c94d-113">An operation is a low-level function or method of an application.</span></span>                                                                                                                                                                                              |
| [<span data-ttu-id="2c94d-114">Gruppieren von Vorgängen in Aufgaben in Skripts</span><span class="sxs-lookup"><span data-stu-id="2c94d-114">Grouping Operations into Tasks in Script</span></span>](grouping-operations-into-tasks-in-script.md)                               | <span data-ttu-id="2c94d-115">Eine Aufgabe ist eine allgemeine Aktion, die Benutzer einer Anwendung ausführen müssen.</span><span class="sxs-lookup"><span data-stu-id="2c94d-115">A task is a high-level action that users of an application need to complete.</span></span> <span data-ttu-id="2c94d-116">Aufgaben bestehen aus Vorgängen, bei denen es sich um Low-Level-Funktionen und-Methoden der Anwendung handelt.</span><span class="sxs-lookup"><span data-stu-id="2c94d-116">Tasks are made up of operations, which are low-level functions and methods of the application.</span></span>                                                                                    |
| [<span data-ttu-id="2c94d-117">Gruppieren von Aufgaben in Rollen in Skripts</span><span class="sxs-lookup"><span data-stu-id="2c94d-117">Grouping Tasks into Roles in Script</span></span>](grouping-tasks-into-roles-in-script.md)                                         | <span data-ttu-id="2c94d-118">Eine Rolle stellt eine Kategorie von Benutzern und die Aufgaben dar, die diese Benutzer für die Ausführung autorisiert haben.</span><span class="sxs-lookup"><span data-stu-id="2c94d-118">A role represents a category of users and the tasks those users are authorized to perform.</span></span>                                                                                                                                                                     |
| [<span data-ttu-id="2c94d-119">Definieren von Benutzergruppen in Skripts</span><span class="sxs-lookup"><span data-stu-id="2c94d-119">Defining Groups of Users in Script</span></span>](defining-groups-of-users-in-script.md)                                           | <span data-ttu-id="2c94d-120">Ein [**iazapplicationgroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) -Objekt stellt eine Gruppe von Benutzern dar.</span><span class="sxs-lookup"><span data-stu-id="2c94d-120">An [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object represents a group of users.</span></span> <span data-ttu-id="2c94d-121">Rollen können dieser Gruppe von Benutzern gemeinsam zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="2c94d-121">Roles can then be assigned to this group of users collectively.</span></span> <span data-ttu-id="2c94d-122">Ein **iazapplicationgroup** -Objekt kann auch andere **iazapplicationgroup** -Objekte als Member enthalten.</span><span class="sxs-lookup"><span data-stu-id="2c94d-122">An **IAzApplicationGroup** object can also include other **IAzApplicationGroup** objects as members.</span></span> |
| [<span data-ttu-id="2c94d-123">Hinzufügen von Benutzern zu einer Anwendungs Gruppe im Skript</span><span class="sxs-lookup"><span data-stu-id="2c94d-123">Adding Users to an Application Group in Script</span></span>](adding-users-to-an-application-group-in-script.md)                   | <span data-ttu-id="2c94d-124">Eine Anwendungs Gruppe ist eine Gruppe von Benutzern und Benutzergruppen.</span><span class="sxs-lookup"><span data-stu-id="2c94d-124">An application group is a group of users and user groups.</span></span> <span data-ttu-id="2c94d-125">Eine Anwendungs Gruppe kann andere Anwendungs Gruppen enthalten, sodass Gruppen von Benutzern gruppiert werden können.</span><span class="sxs-lookup"><span data-stu-id="2c94d-125">An application group can contain other application groups, so groups of users can be nested.</span></span> <span data-ttu-id="2c94d-126">Eine Anwendungs Gruppe wird durch ein [**iazapplicationgroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) -Objekt dargestellt.</span><span class="sxs-lookup"><span data-stu-id="2c94d-126">An application group is represented by an [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object.</span></span>    |



 

 

 



