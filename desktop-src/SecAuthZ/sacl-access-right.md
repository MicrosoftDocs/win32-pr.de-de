---
description: Mit dem Zugriffs \_ System- \_ Sicherheits Zugriffsrecht wird gesteuert, ob die SACL in der Sicherheits Beschreibung des Objekts abgerufen oder festgelegt werden kann. Das System gewährt dieses Zugriffsrecht, wenn die \_ Berechtigung SE Security \_ Name im Zugriffs Token des anfordernden Threads aktiviert ist.
ms.assetid: 88198243-dae5-49ac-9d54-bfae7a3a0b1a
title: SACL-Zugriffsrecht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2366f30748a93294d4f30122102d656fb2590d34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347816"
---
# <a name="sacl-access-right"></a>SACL-Zugriffsrecht

Mit dem Zugriffs \_ System \_ -Sicherheits Zugriffsrecht wird gesteuert, wie die SACL in der [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly)eines Objekts abgerufen oder festgelegt werden kann. Das System gewährt diesen Zugriffsrecht nur, wenn die \_ Berechtigung SE Security \_ Name im [*Zugriffs Token*](/windows/desktop/SecGloss/a-gly) des anfordernden Threads aktiviert ist.

**So greifen Sie auf die SACL eines Objekts zu**

1.  Zum Aktivieren [**der**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) \_ Berechtigung "Sicherheits Name löschen" \_ .
2.  Fordern Sie das Zugriffs \_ System- \_ Sicherheits Zugriffsrecht an, wenn Sie ein Handle für das Objekt öffnen.
3.  Die SACL des Objekts wird mit einer Funktion wie [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) oder [**setsecurityinfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo)abgerufen oder festgelegt.
4.  Zum [**Deaktivieren**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) der \_ Berechtigung "Sicherheits Name löschen" \_

Aktivieren Sie zum Zugreifen auf eine SACL mithilfe der Funktionen " [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) " oder " [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) " die Berechtigung "SE \_ Security \_ Name". Die Funktion fordert intern das Zugriffsrecht an.

Das \_ \_ Sicherheits Zugriffsrecht des Zugriffs Systems ist in einer DACL ungültig, da DACLs den Zugriff auf eine SACL nicht steuern. Sie können jedoch das Zugriffs System- \_ \_ Sicherheits Zugriffsrecht in einer SACL verwenden, um die Zugriffsrechte zu überwachen.

 

 
