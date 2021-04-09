---
title: Testen, ob auf einem Domänen Controller ausgeführt wird
description: Der folgende Code verwendet die verifyversioninfo-Funktion, um zu bestimmen, ob der Aufrufprozess auf einem Windows 2000-Server-Domänen Controller ausgeführt wird.
ms.assetid: 1cef6478-5503-467c-9b82-830d17018b19
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8aeb73af18be9f0c787c2ee30b150689d760aec
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101411"
---
# <a name="testing-whether-running-on-a-domain-controller"></a>Testen, ob auf einem Domänen Controller ausgeführt wird

Der folgende Code verwendet die [**verifyversioninfo**](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa) -Funktion, um zu bestimmen, ob der Aufrufprozess auf einem Windows 2000-Server-Domänen Controller ausgeführt wird. Das Dienst Installationsprogramm kann diesen Test verwenden, bevor ein Dienst unter dem Konto "LocalSystem" installiert wird. Wenn der Test anzeigt, dass Sie auf einem Domänen Controller ausgeführt werden, installieren Sie entweder den Dienst, der unter einem Benutzerkonto ausgeführt wird, oder ein Dialogfeld, in dem die Gefahren bei der Ausführung von als LocalSystem auf einem Domänen Controller angezeigt werden (der Dienst würde dann uneingeschränkten Zugriff auf Active Directory Domain Services haben, einen überaus leistungsfähigen Sicherheitskontext, der das potenzielle Netzwerk beschädigen kann).


```C++
BOOL Is_Win2000_DomainController () 
{
   OSVERSIONINFOEX osvi;
   DWORDLONG dwlConditionMask = 0;
 
   // Initialize the OSVERSIONINFOEX structure.
   ZeroMemory(&osvi, sizeof(OSVERSIONINFOEX));
   osvi.dwOSVersionInfoSize = sizeof(OSVERSIONINFOEX);
   osvi.dwMajorVersion = 5;
   osvi.wProductType = VER_NT_DOMAIN_CONTROLLER;
 
   // Initialize the condition mask.
   VER_SET_CONDITION( dwlConditionMask, VER_MAJORVERSION, 
      VER_GREATER_EQUAL );
   VER_SET_CONDITION( dwlConditionMask, VER_PRODUCT_TYPE, 
      VER_EQUAL );
 
   // Perform the test.
   return VerifyVersionInfo(
      &osvi, 
      VER_MAJORVERSION | VER_PRODUCT_TYPE,
      dwlConditionMask);
}
```



 

 