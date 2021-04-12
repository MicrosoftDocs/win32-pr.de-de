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
# <a name="describing-the-adsi-path"></a><span data-ttu-id="4dcdd-103">Beschreiben des ADSI-Pfads</span><span class="sxs-lookup"><span data-stu-id="4dcdd-103">Describing the ADSI Path</span></span>

<span data-ttu-id="4dcdd-104">Das Lightweight Directory Access Protocol (LDAP) erfordert, dass Sie einige Zeichen mit einem umgekehrten Schrägstrich ( \) Zeichen, wenn Sie Sie in einem LDAP Active Directory Service Interfaces (ADSI)-Pfad verwenden, mit Escapezeichen versehen.</span><span class="sxs-lookup"><span data-stu-id="4dcdd-104">The Lightweight Directory Access Protocol (LDAP) requires that you escape some characters with a backslash (\) character when you use them in an LDAP Active Directory Service Interfaces (ADSI) path.</span></span>

<span data-ttu-id="4dcdd-105">, = +<>\# ; \\ "</span><span class="sxs-lookup"><span data-stu-id="4dcdd-105">,=+<>\#;\\"</span></span>

<span data-ttu-id="4dcdd-106">Das Escapezeichen ist nur für den **adsipath** -Eigenschafts Wert erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4dcdd-106">The escape character is only required for the **ADSIPath** property value.</span></span>

<span data-ttu-id="4dcdd-107">Im folgenden Beispiel wird gezeigt, wie die **adsipath** -Eigenschaft definiert wird.</span><span class="sxs-lookup"><span data-stu-id="4dcdd-107">The following example shows how to define the **ADSIPath** property.</span></span> <span data-ttu-id="4dcdd-108">Beachten Sie, dass das \# Zeichen im **CN** -Eigenschafts Wert ABC mit Escapezeichen versehen \# wird.</span><span class="sxs-lookup"><span data-stu-id="4dcdd-108">Note that the \# character in the **CN** property value of abc\# is escaped.</span></span>


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
> <span data-ttu-id="4dcdd-109">Weitere Informationen zur Unterstützung und Installation dieser Komponente auf einem bestimmten Betriebssystem finden Sie unter [Betriebssystem Verfügbarkeit von WMI-Komponenten](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="4dcdd-109">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

 

 



