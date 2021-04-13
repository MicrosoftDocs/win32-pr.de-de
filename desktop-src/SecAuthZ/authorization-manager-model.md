---
description: Der Autorisierungs-Manager stellt ein flexibles Framework für das Integrieren einer rollenbasierten Zugriffssteuerung in Anwendungen bereit. Er ermöglicht Administratoren, die diese Anwendungen verwenden, das Bereitstellen von Zugriffsrechten über zugewiesene Benutzerrollen, die sich auf unterschiedliche Tätigkeiten beziehen.
ms.assetid: c6d37b2e-b149-43e2-8155-cb2f669e421c
title: Authorization Manager-Modell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3455c9577f24b260bd02f947d0af99ec85570bd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350609"
---
# <a name="authorization-manager-model"></a><span data-ttu-id="26c1e-104">Authorization Manager-Modell</span><span class="sxs-lookup"><span data-stu-id="26c1e-104">Authorization Manager Model</span></span>

<span data-ttu-id="26c1e-105">Der Autorisierungs-Manager stellt ein flexibles Framework für das Integrieren einer rollenbasierten Zugriffssteuerung in Anwendungen bereit.</span><span class="sxs-lookup"><span data-stu-id="26c1e-105">Authorization Manager provides a flexible framework for integrating role-based access control into applications.</span></span> <span data-ttu-id="26c1e-106">Er ermöglicht Administratoren, die diese Anwendungen verwenden, das Bereitstellen von Zugriffsrechten über zugewiesene Benutzerrollen, die sich auf unterschiedliche Tätigkeiten beziehen.</span><span class="sxs-lookup"><span data-stu-id="26c1e-106">It enables administrators who use those applications to provide access through assigned user roles that relate to job functions.</span></span>

<span data-ttu-id="26c1e-107">Autorisierungs-Manager-Anwendungen speichern Autorisierungsrichtlinien in Form von Autorisierungsspeichern, die in Active Directory- oder XML-Dateien gespeichert sind und Autorisierungsrichtlinien zur Laufzeit anwenden.</span><span class="sxs-lookup"><span data-stu-id="26c1e-107">Authorization Manager applications store authorization policy in the form of authorization stores that are stored in Active Directory or XML files and apply authorization policy at run time.</span></span>

<span data-ttu-id="26c1e-108">Anwendungen aufrufen dann eine Lauf Zeit Zugriffs Überprüfung-Methode, die den Zugriff auf die Richtlinien Informationen im Autorisierungs Speicher überprüft.</span><span class="sxs-lookup"><span data-stu-id="26c1e-108">Applications then call a run-time access check method that checks access against the policy information in the authorization store.</span></span>

<span data-ttu-id="26c1e-109">Die Autorisierungs Richtlinie umfasst die folgenden Teile:</span><span class="sxs-lookup"><span data-stu-id="26c1e-109">Authorization policy includes the following parts:</span></span>

-   [<span data-ttu-id="26c1e-110">Richtlinien Speicher, Anwendungen und Bereiche</span><span class="sxs-lookup"><span data-stu-id="26c1e-110">Policy Stores, Applications, and Scopes</span></span>](policy-stores--applications--and-scopes.md)
-   [<span data-ttu-id="26c1e-111">Benutzer und Gruppen</span><span class="sxs-lookup"><span data-stu-id="26c1e-111">Users and Groups</span></span>](users-and-groups.md)
-   [<span data-ttu-id="26c1e-112">Vorgänge und Aufgaben</span><span class="sxs-lookup"><span data-stu-id="26c1e-112">Operations and Tasks</span></span>](operations-and-tasks.md)
-   [<span data-ttu-id="26c1e-113">Rollen</span><span class="sxs-lookup"><span data-stu-id="26c1e-113">Roles</span></span>](roles.md)
-   [<span data-ttu-id="26c1e-114">Geschäftsregeln</span><span class="sxs-lookup"><span data-stu-id="26c1e-114">Business Rules</span></span>](business-rules.md)
-   [<span data-ttu-id="26c1e-115">Sammlungen</span><span class="sxs-lookup"><span data-stu-id="26c1e-115">Collections</span></span>](collections.md)

 

 



