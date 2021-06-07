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
# <a name="describing-the-adsi-path"></a><span data-ttu-id="c5719-103">Beschreiben des ADSI-Pfads</span><span class="sxs-lookup"><span data-stu-id="c5719-103">Describing the ADSI Path</span></span>

<span data-ttu-id="c5719-104">Das Lightweight Directory Access Protocol (LDAP) erfordert, dass Sie einige Zeichen mit einem umgekehrten Schrägstrich \\ () escapen, wenn Sie sie in einem ADSI-Pfad (LDAP Active Directory Service Interfaces) verwenden.</span><span class="sxs-lookup"><span data-stu-id="c5719-104">The Lightweight Directory Access Protocol (LDAP) requires that you escape some characters with a backslash (\\) character when you use them in an LDAP Active Directory Service Interfaces (ADSI) path.</span></span>

<span data-ttu-id="c5719-105">,=+<>\# ; \\ "</span><span class="sxs-lookup"><span data-stu-id="c5719-105">,=+<>\#;\\"</span></span>

<span data-ttu-id="c5719-106">Das Escapezeichen ist nur für den **ADSIPath-Eigenschaftswert** erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c5719-106">The escape character is only required for the **ADSIPath** property value.</span></span>

<span data-ttu-id="c5719-107">Das folgende Beispiel zeigt, wie die **ADSIPath-Eigenschaft** definiert wird.</span><span class="sxs-lookup"><span data-stu-id="c5719-107">The following example shows how to define the **ADSIPath** property.</span></span> <span data-ttu-id="c5719-108">Beachten Sie, dass das \# Zeichen im **CN-Eigenschaftswert** von abc \# mit Escapezeichen umbrochen wird.</span><span class="sxs-lookup"><span data-stu-id="c5719-108">Note that the \# character in the **CN** property value of abc\# is escaped.</span></span>


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
> <span data-ttu-id="c5719-109">Weitere Informationen zur Unterstützung und Installation dieser Komponente unter einem bestimmten Betriebssystem finden Sie unter [Betriebssystemverfügbarkeit von WMI-Komponenten.](operating-system-availability-of-wmi-components.md)</span><span class="sxs-lookup"><span data-stu-id="c5719-109">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

 

 



