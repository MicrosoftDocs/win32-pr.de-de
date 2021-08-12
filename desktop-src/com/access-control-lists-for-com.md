---
title: Access Control Listen für COM
description: Access Control Listen für COM
ms.assetid: ceb37563-7e7f-4704-b671-72ed65e3e102
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e50e1641691b1a2812e861a95c5bc0f7eac8f0f8af67d41b18287c07253b8d51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118551354"
---
# <a name="access-control-lists-for-com"></a>Access Control Listen für COM

Windows Server XP Service Pack 2 (SP 2) und Windows Server 2003 Service Pack 1 (SP 1) führen Sicherheitsverbesserungen für distributed Component Object Model (DCOM) ein. Eine dieser Verbesserungen sind spezifischere Zugriffsrechte für die Verwendung in Zugriffssteuerungslisten (ACCESS Control Lists, ACLs). Die Zugriffsrechte sind:

``` syntax
COM_RIGHTS_EXECUTE 1
COM_RIGHTS_EXECUTE_LOCAL 2
COM_RIGHTS_EXECUTE_REMOTE 4
COM_RIGHTS_ACTIVATE_LOCAL 8
COM_RIGHTS_ACTIVATE_REMOTE 16
```

Um Abwärtskompatibilität zu gewährleisten, Eine ACL kann im Format vor Windows XP SP 2 und Windows Server 2003 SP 1 vorhanden sein, das nur das Zugriffsrecht COM RIGHTS EXECUTE verwendet, oder sie kann im neuen Format vorhanden sein, das in Windows XP SP 2 und \_ Windows Server 2003 SP 1 verwendet wird, das COM RIGHTS EXECUTE zusammen mit einer Kombination aus \_ COM RIGHTS EXECUTE \_ \_ \_ \_ \_ LOCAL, COM RIGHTS EXECUTE REMOTE, COM RIGHTS ACTIVATE LOCAL und \_ COM RIGHTS ACTIVATE REMOTE \_ \_ \_ \_ \_ \_ \_ \_ verwendet.

> [!Note]  
> COM RIGHTS EXECUTE muss immer vorhanden sein. Wenn dieses Recht nicht vorhanden ist, wird \_ \_ ein ungültiger Sicherheitsdeskriptor generiert.

 

Sie dürfen das alte und das neue Format nicht in einer einzelnen ACL mischen. Entweder müssen alle Zugriffssteuerungseinträge (ACCESS Control Entries, ACEs) nur das COM RIGHTS EXECUTE-Zugriffsrecht gewähren, oder alle müssen COM RIGHTS EXECUTE zusammen mit einer Kombination aus \_ \_ COM RIGHTS EXECUTE \_ \_ \_ \_ \_ LOCAL, COM RIGHTS EXECUTE REMOTE, COM RIGHTS ACTIVATE LOCAL und \_ COM RIGHTS ACTIVATE \_ REMOTE \_ \_ \_ \_ \_ \_ \_ gewähren.

Im Folgenden finden Sie ein Beispiel für eine falsch formatierte ACL:

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

Beachten Sie, dass der erste Zugriffssteuerungseintrag (ACE) nur COM RIGHTS EXECUTE (0x1) gewährt, während der zweite ACE COM RIGHTS EXECUTE, COM RIGHTS EXECUTE LOCAL und COM RIGHTS ACTIVATE LOCAL (0xb) gewährt und der dritte COM RIGHTS EXECUTE und \_ \_ COM RIGHTS ACTIVATE \_ \_ \_ \_ LOCAL \_ \_ \_ \_ \_ \_ \_ \_ \_ (0x9).

Um dies zu korrigieren, sollte der erste ACE so geändert werden, dass COM RIGHTS EXECUTE in Kombination mit einem der anderen vier Zugriffsrechte gewährt wird. Ander denn, die zweite und dritte ACEs sollten so geändert werden, dass nur COM RIGHTS EXECUTE gewährt \_ \_ \_ \_ wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DCOM-Sicherheitsverbesserungen in Windows XP Service Pack 2 und Windows Server 2003 Service Pack 1](dcom-security-enhancements-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1.md)
</dt> <dt>

[Sicherheit in COM](security-in-com.md)
</dt> </dl>

 

 




