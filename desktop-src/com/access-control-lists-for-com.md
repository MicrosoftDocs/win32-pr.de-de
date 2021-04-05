---
title: Access Control Listen für com
description: Access Control Listen für com
ms.assetid: ceb37563-7e7f-4704-b671-72ed65e3e102
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811b6cdbca36ef75bb5ee3f185b0261967d736d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709263"
---
# <a name="access-control-lists-for-com"></a><span data-ttu-id="4843f-103">Access Control Listen für com</span><span class="sxs-lookup"><span data-stu-id="4843f-103">Access Control Lists for COM</span></span>

<span data-ttu-id="4843f-104">Windows Server XP Service Pack 2 (SP 2) und Windows Server 2003 Service Pack 1 (SP 1) führen zu Sicherheitsverbesserungen für den verteilten Component Object Model (DCOM).</span><span class="sxs-lookup"><span data-stu-id="4843f-104">Windows Server XP Service Pack 2 (SP 2) and Windows Server 2003 Service Pack 1 (SP 1) introduce security enhancements for the Distributed Component Object Model (DCOM).</span></span> <span data-ttu-id="4843f-105">Eine dieser Verbesserungen sind spezifischere Zugriffsrechte für die Verwendung in Zugriffs Steuerungs Listen (Access Control Lists, ACLs).</span><span class="sxs-lookup"><span data-stu-id="4843f-105">One of these enhancements is more specific access rights for use in access control lists (ACLs).</span></span> <span data-ttu-id="4843f-106">Die Zugriffsrechte lauten:</span><span class="sxs-lookup"><span data-stu-id="4843f-106">The access rights are:</span></span>

``` syntax
COM_RIGHTS_EXECUTE 1
COM_RIGHTS_EXECUTE_LOCAL 2
COM_RIGHTS_EXECUTE_REMOTE 4
COM_RIGHTS_ACTIVATE_LOCAL 8
COM_RIGHTS_ACTIVATE_REMOTE 16
```

<span data-ttu-id="4843f-107">Um Abwärtskompatibilität zu gewährleisten, ist möglicherweise eine ACL in dem vor Windows XP SP 2 und Windows Server 2003 SP 1 verwendeten Format vorhanden. in der nur die Zugriffsrechte für com \_ \_ -Rechte ausführen verwendet werden, oder Sie können im neuen Format vorliegen, das in Windows XP SP 2 und Windows Server 2003 SP 1 verwendet wird. die com- \_ Rechte werden \_ zusammen mit einer Kombination aus com- \_ Rechten ausführen \_ \_ lokal, com- \_ Rechte \_ Execute \_ Remote, com- \_ Rechte \_ Aktivierung \_ lokal und com- \_ Rechte \_ Remote Aktivierung verwendet \_ .</span><span class="sxs-lookup"><span data-stu-id="4843f-107">To provide backward compatibility, an ACL may exist in the format used before Windows XP SP 2 and Windows Server 2003 SP 1, which uses only the access right COM\_RIGHTS\_EXECUTE, or it may exist in the new format used in Windows XP SP 2 and Windows Server 2003 SP 1, which uses COM\_RIGHTS\_EXECUTE together with a combination of COM\_RIGHTS\_EXECUTE\_LOCAL, COM\_RIGHTS\_EXECUTE\_REMOTE, COM\_RIGHTS\_ACTIVATE\_LOCAL, and COM\_RIGHTS\_ACTIVATE\_REMOTE.</span></span>

> [!Note]  
> <span data-ttu-id="4843f-108">COM- \_ Rechte \_ ausführen müssen immer vorhanden sein. das Fehlen dieses Rechts generiert eine ungültige Sicherheits Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="4843f-108">COM\_RIGHTS\_EXECUTE must always be present; the absence of this right generates an invalid security descriptor.</span></span>

 

<span data-ttu-id="4843f-109">Das alte Format und das neue Format dürfen nicht in einer einzelnen Zugriffs Steuerungs Liste (ACL) gemischt werden. entweder müssen alle Zugriffs Steuerungs Einträge (ACEs) nur die com- \_ Rechte \_ Execute Access Right gewähren, oder Sie müssen alle com- \_ Rechte \_ mit einer Kombination aus com- \_ rechten Execute \_ \_ local, com- \_ Rechte \_ Execute \_ Remote, com \_ \_ -Rechte lokal aktivieren \_ und com- \_ Rechte für \_ Remote Aktivierung gewähren \_ .</span><span class="sxs-lookup"><span data-stu-id="4843f-109">You must not mix the old format and the new format within a single ACL; either all access control entries (ACEs) must grant only the COM\_RIGHTS\_EXECUTE access right, or they all must grant COM\_RIGHTS\_EXECUTE together with a combination of COM\_RIGHTS\_EXECUTE\_LOCAL, COM\_RIGHTS\_EXECUTE\_REMOTE, COM\_RIGHTS\_ACTIVATE\_LOCAL, and COM\_RIGHTS\_ACTIVATE\_REMOTE.</span></span>

<span data-ttu-id="4843f-110">Im folgenden finden Sie ein Beispiel für eine falsch formatierte ACL:</span><span class="sxs-lookup"><span data-stu-id="4843f-110">The following is an example of an incorrectly formatted ACL:</span></span>

``` syntax
Revision 1
Sbz1 0
Control 0x8004
    SE_DACL_PRESENT
    SE_SELF_RELATIVE
Owner: S-1-5-21-1597522630-148096252-1166023319-500 (no name mapped)
Group: S-1-5-21-1597522630-148096252-1166023319-500 (no name mapped)
DACL:
    AclRevision 2
    Sbz1 0
    AclSize 128
    AceCount 4
    Sbz2 0
    Ace[0]
        AceType 0: ACCESS_ALLOWED_ACE_TYPE
        AceFlags 0
        AceSize 36
        AccessMask 0x1
        S-1-5-21-1597522630-148096252-1166023319-500 (no name mapped)
    Ace[1]
        AceType 0: ACCESS_ALLOWED_ACE_TYPE
        AceFlags 0
        AceSize 20
        AccessMask 0xb
        S-1-5-18 (Well Known Group: NT AUTHORITY\SYSTEM)
    Ace[2]
        AceType 0: ACCESS_ALLOWED_ACE_TYPE
        AceFlags 0
        AceSize 20
        AccessMask 0x9
        S-1-5-11 (Well Known Group: NT AUTHORITY\Authenticated Users)
SACL:
    (null)
```

<span data-ttu-id="4843f-111">Beachten Sie, dass der erste Zugriffs Steuerungs Eintrag (ACE) \_ nur com-Rechte \_ Execute (0x1) gewährt, während der zweite ACE com- \_ Rechte \_ ausführen, com- \_ Rechte \_ Execute \_ local und com- \_ Rechte \_ lokal aktivieren ( \_ 0xB), und der dritte die com-Rechte Execute \_ \_ und com \_ Rights \_ Aktivierung \_ local (0x9) gewährt.</span><span class="sxs-lookup"><span data-stu-id="4843f-111">Note that the first access control entry (ACE) grants COM\_RIGHTS\_EXECUTE (0x1) only, while the second ACE grants COM\_RIGHTS\_EXECUTE, COM\_RIGHTS\_EXECUTE\_LOCAL, and COM\_RIGHTS\_ACTIVATE\_LOCAL (0xb), and the third grants COM\_RIGHTS\_EXECUTE and COM\_RIGHTS\_ACTIVATE\_LOCAL (0x9).</span></span>

<span data-ttu-id="4843f-112">Um dies zu korrigieren, sollte der erste ACE geändert werden, um com- \_ Rechte \_ in Kombination mit einer der anderen vier Zugriffsrechte zu erteilen. andernfalls sollten der zweite und der dritte ACEs so geändert werden, dass nur die com- \_ Rechte Execute erteilt werden \_ .</span><span class="sxs-lookup"><span data-stu-id="4843f-112">To correct this, the first ACE should be changed to grant COM\_RIGHTS\_EXECUTE in combination with one of the other four access rights, or else the second and third ACEs should be changed to grant only COM\_RIGHTS\_EXECUTE.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4843f-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4843f-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4843f-114">DCOM-Sicherheitsverbesserungen in Windows XP Service Pack 2 und Windows Server 2003 Service Pack 1</span><span class="sxs-lookup"><span data-stu-id="4843f-114">DCOM Security Enhancements in Windows XP Service Pack 2 and Windows Server 2003 Service Pack 1</span></span>](dcom-security-enhancements-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1.md)
</dt> <dt>

[<span data-ttu-id="4843f-115">Sicherheit in com</span><span class="sxs-lookup"><span data-stu-id="4843f-115">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




