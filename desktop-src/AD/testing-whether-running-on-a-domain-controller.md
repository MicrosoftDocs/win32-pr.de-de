---
title: Testen, ob auf einem Domänencontroller ausgeführt wird
description: Im folgenden Code wird die VerifyVersionInfo-Funktion verwendet, um zu bestimmen, ob der aufrufende Prozess auf einem Windows 2000 Server-Domänencontroller ausgeführt wird.
ms.assetid: 1cef6478-5503-467c-9b82-830d17018b19
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb49577994716598bb730fcc7e86a9cce76a2835e8cfa1558b7d608b9cbc5ea2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024588"
---
# <a name="testing-whether-running-on-a-domain-controller"></a>Testen, ob auf einem Domänencontroller ausgeführt wird

Im folgenden Code wird die [**VerifyVersionInfo-Funktion**](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa) verwendet, um zu bestimmen, ob der aufrufende Prozess auf einem Windows 2000 Server-Domänencontroller ausgeführt wird. Ihr Dienstinstallationsprogramm könnte diesen Test vor der Installation eines Diensts unter dem LocalSystem-Konto verwenden. Wenn der Test angibt, dass Sie auf einem Domänencontroller ausgeführt werden, installieren Sie entweder den Dienst für die Ausführung unter einem Benutzerkonto oder zeigen eine Dialogfeldwarnung an, dass die Ausführung als LocalSystem auf einem Domänencontroller nicht möglich ist (d. h., der Dienst hätte dann uneingeschränkten Zugriff auf Active Directory Domain Services, einen äußerst leistungsstarken Sicherheitskontext, der das gesamte Netzwerk beschädigen kann).


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



 

 