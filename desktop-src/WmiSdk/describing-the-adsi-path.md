---
description: Das Lightweight Directory Access Protocol (LDAP) erfordert, dass Sie einige Zeichen mit einem umgekehrten Schrägstrich ( \) Zeichen, wenn Sie Sie in einem LDAP Active Directory Service Interfaces (ADSI)-Pfad verwenden, mit Escapezeichen versehen.
ms.assetid: bc04359c-4eda-4574-a9c2-f005a1d92dea
ms.tgt_platform: multiple
title: Beschreiben des ADSI-Pfads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51a6f3f28ffa5faa80dbd9f3d7906bba542e47e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528610"
---
# <a name="describing-the-adsi-path"></a>Beschreiben des ADSI-Pfads

Das Lightweight Directory Access Protocol (LDAP) erfordert, dass Sie einige Zeichen mit einem umgekehrten Schrägstrich ( \) Zeichen, wenn Sie Sie in einem LDAP Active Directory Service Interfaces (ADSI)-Pfad verwenden, mit Escapezeichen versehen.

, = +<>\# ; \\ "

Das Escapezeichen ist nur für den **adsipath** -Eigenschafts Wert erforderlich.

Im folgenden Beispiel wird gezeigt, wie die **adsipath** -Eigenschaft definiert wird. Beachten Sie, dass das \# Zeichen im **CN** -Eigenschafts Wert ABC mit Escapezeichen versehen \# wird.


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
> Weitere Informationen zur Unterstützung und Installation dieser Komponente auf einem bestimmten Betriebssystem finden Sie unter [Betriebssystem Verfügbarkeit von WMI-Komponenten](operating-system-availability-of-wmi-components.md).

 

 

 



