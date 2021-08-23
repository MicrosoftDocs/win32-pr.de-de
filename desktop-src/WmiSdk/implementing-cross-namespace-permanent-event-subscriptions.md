---
description: Es wird empfohlen, alle permanenten Abonnements in den Stammabonnementnamespace \\ \\ zu kompilieren.
ms.assetid: 6d4ccc86-f29f-4ca5-bea5-c77ee07d7789
ms.tgt_platform: multiple
title: Implementieren namespaceübergreifender permanenter Ereignisabonnements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b175f89a4a686aa47818daf3479d521306f6190fb245222c4c21c17ca6470dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757950"
---
# <a name="implementing-cross-namespace-permanent-event-subscriptions"></a>Implementieren namespaceübergreifender permanenter Ereignisabonnements

Es wird empfohlen, alle permanenten Abonnements in den Stammabonnementnamespace \\ \\ zu kompilieren. Dies verhindert, dass der permanente Consumer in jeden verwendeten Namespace kompiliert werden muss. Dies bedeutet, dass es nur einen Namespace gibt, um nach permanenten Abonnements zu suchen. Verwenden Sie **die EventNamespace-Eigenschaft** von [**\_ \_ EventFilter,**](--eventfilter.md) um ein namespaceübergreifendes Abonnement zu implementieren.

Bei Verwendung von [**CommandLineEventConsumer**](commandlineeventconsumer.md)ist es wichtig, die ausführbare Datei zu schützen, die Sie starten. Wenn sich die ausführbare Datei nicht an einem sicheren Speicherort befindet oder mit einer starken Zugriffssteuerungsliste (ACL) geschützt ist, kann jeder Ihre ausführbare Datei durch eine eigene ersetzen. Weitere Informationen zu ACLs finden Sie unter Creating a Security Descriptor for a New Object in C++ (Erstellen eines [Sicherheitsdeskriptors für ein neues Objekt in C++).](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--)

Das folgende Managed Object Format (MOF)-Codebeispiel zeigt ein namespaceübergreifendes Abonnement.

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

 

 
