---
description: Das \_ Zugriffsrecht ACCESS SYSTEM SECURITY steuert die \_ Möglichkeit, die SACL in einem Objektsicherheitsdeskriptor abzurufen oder festzulegen. Das System gewährt dieses Zugriffsrecht, wenn die berechtigung \_ SE SECURITY NAME im \_ Zugriffstoken des anfordernden Threads aktiviert ist.
ms.assetid: 88198243-dae5-49ac-9d54-bfae7a3a0b1a
title: SACL-Zugriffsrecht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88256664db25c6e906f3b4ca0459217a29d0cc7c0e2dd544c1cf198bc24fff5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780515"
---
# <a name="sacl-access-right"></a>SACL-Zugriffsrecht

Das \_ Zugriffsrecht ACCESS SYSTEM SECURITY steuert die \_ Möglichkeit, die SACL im [*Sicherheitsdeskriptor*](/windows/desktop/SecGloss/s-gly)eines Objekts abzurufen oder festzulegen. Das System gewährt dieses Zugriffsrecht nur, wenn die berechtigung SE \_ SECURITY \_ NAME im [*Zugriffstoken*](/windows/desktop/SecGloss/a-gly) des anfordernden Threads aktiviert ist.

**So greifen Sie auf die SACL eines Objekts zu**

1.  Rufen Sie die [**Funktion AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) auf, um die SE \_ SECURITY \_ NAME-Berechtigung zu aktivieren.
2.  Fordern Sie das Zugriffsrecht ACCESS \_ SYSTEM \_ SECURITY an, wenn Sie ein Handle für das Objekt öffnen.
3.  Dient zum Abrufen oder Festlegen der SACL des Objekts mithilfe einer Funktion wie [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) oder [**SetSecurityInfo.**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)
4.  Rufen [**Sie AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) auf, um die SE \_ SECURITY \_ NAME-Berechtigung zu deaktivieren.

Um mithilfe der Funktionen [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) oder [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) auf eine SACL zuzugreifen, aktivieren Sie die berechtigung SE \_ SECURITY \_ NAME. Die Funktion fordert intern das Zugriffsrecht an.

Das \_ Zugriffsrecht ACCESS SYSTEM SECURITY ist in einer \_ DACL ungültig, da DACLs den Zugriff auf eine SACL nicht steuern. Sie können jedoch das Zugriffsrecht ACCESS \_ SYSTEM SECURITY in einer \_ SACL verwenden, um Versuche zu überwachen, das Zugriffsrecht zu verwenden.

 

 
