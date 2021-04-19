---
description: Ein Objektbesitzer hat implizit Schreib \_ Zugriff auf das Objekt. Dies bedeutet, dass der Besitzer die Objekte der freigegebenen Zugriffs Steuerungs Liste (DACL) ändern und somit den Zugriff auf das Objekt steuern kann.
ms.assetid: 16144f38-3416-4594-b5e4-ca84fcbdddc9
title: Besitzer eines neuen Objekts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32f16124d84e17a075c78c676465ad753fcc12db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364064"
---
# <a name="owner-of-a-new-object"></a><span data-ttu-id="686c4-104">Besitzer eines neuen Objekts</span><span class="sxs-lookup"><span data-stu-id="686c4-104">Owner of a New Object</span></span>

<span data-ttu-id="686c4-105">Der Besitzer eines Objekts hat implizit Schreib \_ Zugriff auf das Objekt.</span><span class="sxs-lookup"><span data-stu-id="686c4-105">An object's owner implicitly has WRITE\_DAC access to the object.</span></span> <span data-ttu-id="686c4-106">Dies bedeutet, dass der Besitzer die [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) des Objekts ändern kann und somit den Zugriff auf das Objekt steuern kann.</span><span class="sxs-lookup"><span data-stu-id="686c4-106">This means that the owner can modify the object's [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL), and thus, can control access to the object.</span></span>

<span data-ttu-id="686c4-107">Der Besitzer eines neuen Objekts ist die Standard- [*Sicherheits*](/windows/desktop/SecGloss/s-gly) -ID (SID) des Besitzers aus dem [*primären*](/windows/desktop/SecGloss/p-gly) Token oder dem Identitätswechsel [*Token*](/windows/desktop/SecGloss/i-gly) des Erstellungs [*Prozesses*](/windows/desktop/SecGloss/p-gly).</span><span class="sxs-lookup"><span data-stu-id="686c4-107">The owner of a new object is the default owner [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) from the [*primary*](/windows/desktop/SecGloss/p-gly) or [*impersonation token*](/windows/desktop/SecGloss/i-gly) of the creating [*process*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="686c4-108">Um den Standard Besitzer in einem [*Zugriffs Token*](/windows/desktop/SecGloss/a-gly)abzurufen oder festzulegen, müssen Sie die [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) -oder [**settokeninformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-settokeninformation) -Funktion mit der tokenbesitzerstruktur aufrufen. [**\_**](/windows/desktop/api/Winnt/ns-winnt-token_owner)</span><span class="sxs-lookup"><span data-stu-id="686c4-108">To get or set the default owner in an [*access token*](/windows/desktop/SecGloss/a-gly), call the [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) or [**SetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-settokeninformation) function with the [**TOKEN\_OWNER**](/windows/desktop/api/Winnt/ns-winnt-token_owner) structure.</span></span> <span data-ttu-id="686c4-109">Das System lässt nicht zu, dass der Standard Besitzer eines Tokens auf eine ungültige sid festgelegt wird, z. b. die SID des Kontos eines anderen Benutzers.</span><span class="sxs-lookup"><span data-stu-id="686c4-109">The system does not allow you to set a token's default owner to a SID that is not valid, such as the SID of another user's account.</span></span>

<span data-ttu-id="686c4-110">Ein Prozess, bei dem die SE \_ Take \_ Ownership-Berechtigung aktiviert ist, kann sich selbst als Besitzer eines Objekts festlegen.</span><span class="sxs-lookup"><span data-stu-id="686c4-110">A process with the SE\_TAKE\_OWNERSHIP privilege enabled can set itself as the owner of an object.</span></span> <span data-ttu-id="686c4-111">Ein Prozess, bei dem die Berechtigung "SE \_ Restore \_ Name" aktiviert ist, oder mit dem Schreib \_ Besitzer Zugriff auf das Objekt kann eine beliebige gültige Benutzer-oder Gruppen-SID als Besitzer eines Objekts festlegen.</span><span class="sxs-lookup"><span data-stu-id="686c4-111">A process with the SE\_RESTORE\_NAME privilege enabled or with WRITE\_OWNER access to the object can set any valid user or group SID as the owner of an object.</span></span>

 

 
