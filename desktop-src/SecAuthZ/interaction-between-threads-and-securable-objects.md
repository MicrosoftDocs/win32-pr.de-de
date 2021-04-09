---
description: Bei einer Zugriffs Überprüfung vergleicht das System die Sicherheitsinformationen im Thread Zugriffs Token mit den Sicherheitsinformationen in der Sicherheits Beschreibung des Objekts.
ms.assetid: 40871179-d383-43d0-810d-0805c88dbbd6
title: Interaktion zwischen Threads und Sicherungs fähigen Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f3e2b18f707ece4d651eeca1c6897bb67aad334
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867808"
---
# <a name="interaction-between-threads-and-securable-objects"></a><span data-ttu-id="76552-103">Interaktion zwischen Threads und Sicherungs fähigen Objekten</span><span class="sxs-lookup"><span data-stu-id="76552-103">Interaction Between Threads and Securable Objects</span></span>

<span data-ttu-id="76552-104">Wenn ein Thread versucht, ein Sicherungs [fähiges Objekt](securable-objects.md)zu verwenden, führt das System eine Zugriffs Überprüfung durch, bevor der Thread fortgesetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="76552-104">When a thread attempts to use a [securable object](securable-objects.md), the system performs an access check before allowing the thread to proceed.</span></span> <span data-ttu-id="76552-105">Bei einer Zugriffs Überprüfung vergleicht das System die Sicherheitsinformationen im [*Zugriffs Token*](/windows/desktop/SecGloss/a-gly) des Threads mit den Sicherheitsinformationen in der [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly)des Objekts.</span><span class="sxs-lookup"><span data-stu-id="76552-105">In an access check, the system compares the security information in the thread's [*access token*](/windows/desktop/SecGloss/a-gly) against the security information in the object's [*security descriptor*](/windows/desktop/SecGloss/s-gly).</span></span>

-   <span data-ttu-id="76552-106">Das Zugriffs Token enthält [*Sicherheits*](/windows/desktop/SecGloss/s-gly) -IDs (Security Identifier, SIDs), die den dem Thread zugeordneten Benutzer identifizieren.</span><span class="sxs-lookup"><span data-stu-id="76552-106">The access token contains [*security identifiers*](/windows/desktop/SecGloss/s-gly) (SIDs) that identify the user associated with the thread.</span></span>
-   <span data-ttu-id="76552-107">Die Sicherheits Beschreibung identifiziert den Besitzer des Objekts und enthält eine freigegebene [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL).</span><span class="sxs-lookup"><span data-stu-id="76552-107">The security descriptor identifies the object's owner and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL).</span></span> <span data-ttu-id="76552-108">Die DACL enthält [*Zugriffs Steuerungs Einträge (Access Control Entries*](/windows/desktop/SecGloss/a-gly) , ACEs), von denen jede die Zugriffsrechte angibt, die einem bestimmten Benutzer oder einer Gruppe gewährt oder verweigert werden.</span><span class="sxs-lookup"><span data-stu-id="76552-108">The DACL contains [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs), each of which specify the access rights allowed or denied to a specific user or group.</span></span>

<span data-ttu-id="76552-109">Das System überprüft die DACL des Objekts und sucht nach ACEs, die für die Benutzer-und Gruppen-SIDs aus dem Zugriffs Token des Threads gelten.</span><span class="sxs-lookup"><span data-stu-id="76552-109">The system checks the object's DACL, looking for ACEs that apply to the user and group SIDs from the thread's access token.</span></span> <span data-ttu-id="76552-110">Das System prüft jeden ACE, bis der Zugriff gewährt oder verweigert wird oder wenn keine weiteren ACEs zum Überprüfen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="76552-110">The system checks each ACE until access is either granted or denied or until there are no more ACEs to check.</span></span> <span data-ttu-id="76552-111">Eine [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/a-gly) (ACL) kann mehrere ACEs enthalten, die für die SIDs des Tokens gelten.</span><span class="sxs-lookup"><span data-stu-id="76552-111">Conceivably, an [*access control list*](/windows/desktop/SecGloss/a-gly) (ACL) could have several ACEs that apply to the token's SIDs.</span></span> <span data-ttu-id="76552-112">Wenn dies der Fall ist, häufen sich die von den einzelnen ACE gewährten Zugriffsrechte an.</span><span class="sxs-lookup"><span data-stu-id="76552-112">And, if this occurs, the access rights granted by each ACE accumulate.</span></span> <span data-ttu-id="76552-113">Wenn ein ACE z. b. Lesezugriff auf eine Gruppe gewährt und ein anderer ACE Schreibzugriff für einen Benutzer gewährt, der Mitglied der Gruppe ist, kann der Benutzer sowohl Lese-als auch Schreibzugriff auf das Objekt haben.</span><span class="sxs-lookup"><span data-stu-id="76552-113">For example, if one ACE grants read access to a group and another ACE grants write access to a user who is a member of the group, the user can have both read and write access to the object.</span></span>

<span data-ttu-id="76552-114">In der folgenden Abbildung wird die Beziehung zwischen diesen Sicherheitsinformationen angezeigt:</span><span class="sxs-lookup"><span data-stu-id="76552-114">The following illustration shows the relationship between these blocks of security information:</span></span>

![Beziehungen zwischen Prozessen, ACEs und DACLs](images/cssec-02.png)

 

 
