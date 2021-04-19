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
# <a name="implementing-cross-namespace-permanent-event-subscriptions"></a>Implementieren von Abonnements für permanente Namespace-Ereignisse

Es wird empfohlen, dass alle permanenten Abonnements in den Namespace des Stamm Abonnements kompiliert werden \\ \\ . Dadurch wird verhindert, dass der permanente Consumer in jeden verwendeten Namespace kompiliert werden muss. Dies bedeutet, dass nur ein Namespace vorhanden ist, um nach permanenten Abonnements zu suchen. Verwenden Sie die **eventnamespace** -Eigenschaft von [**\_ \_ EventFilter**](--eventfilter.md) zum Implementieren eines Cross-Namespace-Abonnements.

Wenn Sie [**commandlineeventconsumer**](commandlineeventconsumer.md)verwenden, ist es wichtig, die ausführbare Datei zu sichern, die Sie starten. Wenn sich die ausführbare Datei nicht an einem sicheren Speicherort befindet oder durch eine sichere Zugriffs Steuerungs Liste (ACL) geschützt ist, kann jeder Benutzer die ausführbare Datei durch einen eigenen ersetzen. Weitere Informationen zu ACLs finden Sie unter [Erstellen einer Sicherheits Beschreibung für ein neues Objekt in C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).

Im folgenden Managed Object Format (MOF)-Codebeispiel wird ein Cross-Namespace-Abonnement veranschaulicht.

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

 

 
