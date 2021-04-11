---
description: Eine Anmelde Sitzung ist eine computesitzung, die beginnt, wenn eine Benutzerauthentifizierung erfolgreich ist, und endet, wenn sich der Benutzer beim System anmeldet.
ms.assetid: 14f0f9e7-90ba-47d7-a8d5-06f9d2f1a7a1
title: LSA-Anmelde Sitzungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f32a4912218b68c25c5c23334f7b34ef875fa318
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217329"
---
# <a name="lsa-logon-sessions"></a><span data-ttu-id="543a8-103">LSA-Anmelde Sitzungen</span><span class="sxs-lookup"><span data-stu-id="543a8-103">LSA Logon Sessions</span></span>

<span data-ttu-id="543a8-104">Eine [*Anmelde Sitzung*](../secgloss/l-gly.md) ist eine computesitzung, die beginnt, wenn eine Benutzerauthentifizierung erfolgreich ist, und endet, wenn sich der Benutzer beim System anmeldet.</span><span class="sxs-lookup"><span data-stu-id="543a8-104">A [*logon session*](../secgloss/l-gly.md) is a computing session that begins when a user authentication is successful and ends when the user logs off of the system.</span></span>

<span data-ttu-id="543a8-105">Wenn ein Benutzer erfolgreich authentifiziert wurde, erstellt das Authentifizierungs Paket eine Anmelde Sitzung und gibt Informationen an die [*Lokale Sicherheits Autorität (Local Security Authority*](../secgloss/l-gly.md) , LSA) zurück, [*die zum Erstellen eines Tokens*](../secgloss/t-gly.md) für den neuen Benutzer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="543a8-105">When a user is successfully authenticated, the authentication package creates a logon session and returns information to the [*Local Security Authority*](../secgloss/l-gly.md) (LSA) that is used to create a [*token*](../secgloss/t-gly.md) for the new user.</span></span> <span data-ttu-id="543a8-106">Dieses Token enthält unter anderem einen [*lokal eindeutigen Bezeichner*](../secgloss/l-gly.md) (LUID) für die Anmelde Sitzung, die als Anmelde- [*ID*](../secgloss/l-gly.md)bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="543a8-106">This token includes, among other things, a [*locally unique identifier*](../secgloss/l-gly.md) (LUID) for the logon session, called the [*logon Id*](../secgloss/l-gly.md).</span></span>

<span data-ttu-id="543a8-107">Wenn ein Token erstellt wird, wird der [*Verweis Zähler*](../secgloss/r-gly.md) für die Anmelde Sitzung inkrementiert.</span><span class="sxs-lookup"><span data-stu-id="543a8-107">When a token is created, the [*reference count*](../secgloss/r-gly.md) for the logon session is incremented.</span></span> <span data-ttu-id="543a8-108">Der Verweis Zähler wird auch immer dann erhöht, wenn Kopien des Tokens für die Prozesserstellung, den Identitätswechsel oder andere Verwendungszwecke erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="543a8-108">The reference count is also incremented whenever copies of the token are created for process creation, impersonation, or other uses.</span></span> <span data-ttu-id="543a8-109">Wenn tokenverwendungen abgeschlossen sind und Kopien des Tokens gelöscht werden, wird der Verweis Zähler für die Anmelde Sitzung dekrementiert.</span><span class="sxs-lookup"><span data-stu-id="543a8-109">As token uses are completed and copies of the token are deleted, the reference count for the logon session is decremented.</span></span> <span data-ttu-id="543a8-110">Wenn der Verweis Zähler Null erreicht, wird die Anmelde Sitzung gelöscht.</span><span class="sxs-lookup"><span data-stu-id="543a8-110">When the reference count reaches zero, the logon session is deleted.</span></span>

> [!Note]  
> <span data-ttu-id="543a8-111">Wenn die Authentifizierung nicht erfolgreich ist, sollte das [*Authentifizierungs Paket*](../secgloss/a-gly.md) keine Anmelde Sitzung erstellen.</span><span class="sxs-lookup"><span data-stu-id="543a8-111">If authentication is not successful, the [*authentication package*](../secgloss/a-gly.md) should not create a logon session.</span></span> <span data-ttu-id="543a8-112">Wenn das Authentifizierungs Paket eine Anmelde Sitzung erstellen muss, bevor die Gültigkeit des Benutzers bestimmt wird, und wenn die Authentifizierung fehlschlägt, muss das Authentifizierungs Paket die Sitzung löschen.</span><span class="sxs-lookup"><span data-stu-id="543a8-112">If the authentication package must create a logon session before making a final determination about the validity of the user, and if authentication fails, the authentication package must delete the session.</span></span>

 

 

 
