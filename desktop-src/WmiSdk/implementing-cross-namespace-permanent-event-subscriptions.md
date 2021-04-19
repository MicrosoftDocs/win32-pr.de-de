---
description: Es wird empfohlen, dass alle permanenten Abonnements in den Namespace des Stamm Abonnements kompiliert werden \\ \\ .
ms.assetid: 6d4ccc86-f29f-4ca5-bea5-c77ee07d7789
ms.tgt_platform: multiple
title: Implementieren von Abonnements für permanente Namespace-Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52771e40d4dfb036354c3b37b562b32edd3034ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363247"
---
# <a name="implementing-cross-namespace-permanent-event-subscriptions"></a><span data-ttu-id="92bc2-103">Implementieren von Abonnements für permanente Namespace-Ereignisse</span><span class="sxs-lookup"><span data-stu-id="92bc2-103">Implementing Cross-Namespace Permanent Event Subscriptions</span></span>

<span data-ttu-id="92bc2-104">Es wird empfohlen, dass alle permanenten Abonnements in den Namespace des Stamm Abonnements kompiliert werden \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="92bc2-104">It is recommended that all permanent subscriptions be compiled into the \\root\\subscription namespace.</span></span> <span data-ttu-id="92bc2-105">Dadurch wird verhindert, dass der permanente Consumer in jeden verwendeten Namespace kompiliert werden muss. Dies bedeutet, dass nur ein Namespace vorhanden ist, um nach permanenten Abonnements zu suchen.</span><span class="sxs-lookup"><span data-stu-id="92bc2-105">This prevents the need to compile the permanent consumer into each namespace being used, which means that there is only one namespace to look for permanent subscriptions.</span></span> <span data-ttu-id="92bc2-106">Verwenden Sie die **eventnamespace** -Eigenschaft von [**\_ \_ EventFilter**](--eventfilter.md) zum Implementieren eines Cross-Namespace-Abonnements.</span><span class="sxs-lookup"><span data-stu-id="92bc2-106">Use the **EventNamespace** property of [**\_\_EventFilter**](--eventfilter.md) to implement a cross-namespace subscription.</span></span>

<span data-ttu-id="92bc2-107">Wenn Sie [**commandlineeventconsumer**](commandlineeventconsumer.md)verwenden, ist es wichtig, die ausführbare Datei zu sichern, die Sie starten.</span><span class="sxs-lookup"><span data-stu-id="92bc2-107">When using the [**CommandLineEventConsumer**](commandlineeventconsumer.md), it is important to secure the executable you are launching.</span></span> <span data-ttu-id="92bc2-108">Wenn sich die ausführbare Datei nicht an einem sicheren Speicherort befindet oder durch eine sichere Zugriffs Steuerungs Liste (ACL) geschützt ist, kann jeder Benutzer die ausführbare Datei durch einen eigenen ersetzen.</span><span class="sxs-lookup"><span data-stu-id="92bc2-108">If the executable is not in a secure location, or secured with a strong access control list (ACL), anyone can replace your executable with one of their own.</span></span> <span data-ttu-id="92bc2-109">Weitere Informationen zu ACLs finden Sie unter [Erstellen einer Sicherheits Beschreibung für ein neues Objekt in C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="92bc2-109">For more information about ACLs, see [Creating a Security Descriptor for a New Object in C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

<span data-ttu-id="92bc2-110">Im folgenden Managed Object Format (MOF)-Codebeispiel wird ein Cross-Namespace-Abonnement veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="92bc2-110">The following Managed Object Format (MOF) code example shows a cross-namespace subscription.</span></span>

``` syntax
#pragma namespace("\\root\\subscription")

instance of __EventFilter as $FLT
{
  Name = "Filter";
  Query = "SELECT * FROM __InstanceModificationEvent "
          "WHERE TargetInstance ISA \"Win32_LocalTime\" "
          "AND TargetInstance.Hour = 8 "
          "AND TargetInstance.Minute = 0 "
          "AND TargetInstance.Second = 0 "
          "AND TargetInstance.DayOfWeek = 6";
  QueryLanguage = "WQL";
  EventNamespace = "root\\cimv2";
};

instance of CommandLineEventConsumer as $CONS
{
  ExecutablePath = "cmd.exe";
  ShowWindowCommand = 7;
  RunInteractively = true;
};

instance of __FilterToConsumerBinding
{
  Consumer = $CONS;
  Filter = $FLT;
};
```

 

 
