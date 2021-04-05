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
# <a name="access-control-lists-for-com"></a>Access Control Listen für com

Windows Server XP Service Pack 2 (SP 2) und Windows Server 2003 Service Pack 1 (SP 1) führen zu Sicherheitsverbesserungen für den verteilten Component Object Model (DCOM). Eine dieser Verbesserungen sind spezifischere Zugriffsrechte für die Verwendung in Zugriffs Steuerungs Listen (Access Control Lists, ACLs). Die Zugriffsrechte lauten:

``` syntax
COM_RIGHTS_EXECUTE 1
COM_RIGHTS_EXECUTE_LOCAL 2
COM_RIGHTS_EXECUTE_REMOTE 4
COM_RIGHTS_ACTIVATE_LOCAL 8
COM_RIGHTS_ACTIVATE_REMOTE 16
```

Um Abwärtskompatibilität zu gewährleisten, ist möglicherweise eine ACL in dem vor Windows XP SP 2 und Windows Server 2003 SP 1 verwendeten Format vorhanden. in der nur die Zugriffsrechte für com \_ \_ -Rechte ausführen verwendet werden, oder Sie können im neuen Format vorliegen, das in Windows XP SP 2 und Windows Server 2003 SP 1 verwendet wird. die com- \_ Rechte werden \_ zusammen mit einer Kombination aus com- \_ Rechten ausführen \_ \_ lokal, com- \_ Rechte \_ Execute \_ Remote, com- \_ Rechte \_ Aktivierung \_ lokal und com- \_ Rechte \_ Remote Aktivierung verwendet \_ .

> [!Note]  
> COM- \_ Rechte \_ ausführen müssen immer vorhanden sein. das Fehlen dieses Rechts generiert eine ungültige Sicherheits Beschreibung.

 

Das alte Format und das neue Format dürfen nicht in einer einzelnen Zugriffs Steuerungs Liste (ACL) gemischt werden. entweder müssen alle Zugriffs Steuerungs Einträge (ACEs) nur die com- \_ Rechte \_ Execute Access Right gewähren, oder Sie müssen alle com- \_ Rechte \_ mit einer Kombination aus com- \_ rechten Execute \_ \_ local, com- \_ Rechte \_ Execute \_ Remote, com \_ \_ -Rechte lokal aktivieren \_ und com- \_ Rechte für \_ Remote Aktivierung gewähren \_ .

Im folgenden finden Sie ein Beispiel für eine falsch formatierte ACL:

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

Beachten Sie, dass der erste Zugriffs Steuerungs Eintrag (ACE) \_ nur com-Rechte \_ Execute (0x1) gewährt, während der zweite ACE com- \_ Rechte \_ ausführen, com- \_ Rechte \_ Execute \_ local und com- \_ Rechte \_ lokal aktivieren ( \_ 0xB), und der dritte die com-Rechte Execute \_ \_ und com \_ Rights \_ Aktivierung \_ local (0x9) gewährt.

Um dies zu korrigieren, sollte der erste ACE geändert werden, um com- \_ Rechte \_ in Kombination mit einer der anderen vier Zugriffsrechte zu erteilen. andernfalls sollten der zweite und der dritte ACEs so geändert werden, dass nur die com- \_ Rechte Execute erteilt werden \_ .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DCOM-Sicherheitsverbesserungen in Windows XP Service Pack 2 und Windows Server 2003 Service Pack 1](dcom-security-enhancements-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1.md)
</dt> <dt>

[Sicherheit in com](security-in-com.md)
</dt> </dl>

 

 




