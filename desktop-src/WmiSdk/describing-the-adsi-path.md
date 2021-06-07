---
description: Das Lightweight Directory Access Protocol (LDAP) erfordert, dass Sie einige Zeichen mit einem umgekehrten Schrägstrich \) (Zeichen) escapen, wenn Sie sie in einem ADSI-Pfad (LDAP Active Directory Service Interfaces) verwenden.
ms.assetid: bc04359c-4eda-4574-a9c2-f005a1d92dea
ms.tgt_platform: multiple
title: Beschreiben des ADSI-Pfads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e0ba1dafac273ab3564549a5caca44180161643
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387109"
---
# <a name="describing-the-adsi-path"></a>Beschreiben des ADSI-Pfads

Das Lightweight Directory Access Protocol (LDAP) erfordert, dass Sie einige Zeichen mit einem umgekehrten Schrägstrich \\ () escapen, wenn Sie sie in einem ADSI-Pfad (LDAP Active Directory Service Interfaces) verwenden.

,=+<>\# ; \\ "

Das Escapezeichen ist nur für den **ADSIPath-Eigenschaftswert** erforderlich.

Das folgende Beispiel zeigt, wie die **ADSIPath-Eigenschaft** definiert wird. Beachten Sie, dass das \# Zeichen im **CN-Eigenschaftswert** von abc \# mit Escapezeichen umbrochen wird.


```C++
// #include <windows.h> for this code to compile

BSTR strObjPath = 
    SysAllocString(L"ds_user.ADSIPath=\"LDAP://CN=abc\#,"
                   L"CN=Users,DC=dsprovider,DC=nttest,"
                   L"DC=microsoft,DC=com\"");

// Use strObjectPath here.

SysFreeString(strObjPath); // Free memory resources.
```



> [!Note]  
> Weitere Informationen zur Unterstützung und Installation dieser Komponente unter einem bestimmten Betriebssystem finden Sie unter [Betriebssystemverfügbarkeit von WMI-Komponenten.](operating-system-availability-of-wmi-components.md)

 

 

 



