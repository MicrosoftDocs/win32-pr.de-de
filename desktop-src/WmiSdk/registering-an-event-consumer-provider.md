---
description: Zum Erstellen eines WMI- \_ \_ Ereignisconsumeranbieters müssen Sie die Win32Provider-Instanz, die den Anbieter darstellt, mithilfe einer Instanz von \_ \_ eventconsumerproviderregistration registrieren.
ms.assetid: d1aa035c-f9ee-46b5-9fa5-8af77156f904
ms.tgt_platform: multiple
title: Registrieren eines Ereignisconsumeranbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df6bf47e11b1b9df072f9efbca0ba0f620e96d78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755048"
---
# <a name="registering-an-event-consumer-provider"></a>Registrieren eines Ereignisconsumeranbieters

Zum Erstellen eines WMI- [*Ereignisconsumeranbieters*](gloss-e.md) müssen Sie die [**\_ \_ Win32Provider**](--win32provider.md) -Instanz, die den Anbieter darstellt, mithilfe einer Instanz von [**\_ \_ eventconsumerproviderregistration**](--eventconsumerproviderregistration.md)registrieren. Als COM-Objekt muss sich Ihr Anbieter beim Betriebssystem und WMI registrieren. Im folgenden Verfahren wird davon ausgegangen, dass Sie den Registrierungsprozess bereits implementiert haben, wie unter [Registrieren eines Anbieters](registering-a-provider.md)beschrieben.

Im folgenden Verfahren wird beschrieben, wie ein Ereignisconsumeranbieter registriert wird.

**So registrieren Sie einen Ereignisconsumeranbieter**

1.  Erstellen Sie eine Instanz der [**\_ \_ Win32Provider**](--win32provider.md) -Klasse, die den Anbieter beschreibt.
2.  Erstellen Sie eine Instanz der [**\_ \_ eventconsumerproviderregistration**](--eventconsumerproviderregistration.md) -Klasse, die den Funktions Satz des Anbieters beschreibt.

    Die Eigenschaften, die von [**\_ \_ eventconsumerproviderregistration**](--eventconsumerproviderregistration.md) definiert werden, enthalten den Objekt Pfad zum Anbieter und die Namen der logischen Consumerklassen, die vom Ereignisconsumeranbieter unterstützt werden.

    Stellen Sie sicher, dass Sie die-Klasse mit dem **dynamischen** und dem [**Anbieter Qualifizierer**](/windows/desktop/api/Provider/nl-provider-provider) markieren. Der **dynamische** Qualifizierer signalisiert, dass WMI einen Anbieter zum Abrufen der Klassen Instanzen verwenden soll. Der **Anbieter Qualifizierer** gibt den Namen des Anbieters an, der von WMI verwendet werden soll.

Im folgenden Codebeispiel wird gezeigt, wie ein Ereignisconsumeranbieter registriert wird.

``` syntax
// Provider registration.
// ======================

instance of __Win32Provider as $P
{
    Name  = "MyEventConsumer";
    CLSID = "{4916157B-FBE7-11d1-AEC4-00C04FB68820}";

    DefaultMachineName = NULL;
    ClientLoadableCLSID = NULL;
    ImpersonationLevel = 0;

    PerUserInitialization = FALSE;
    Pure = TRUE;
    UnloadTimeout = NULL;
};


instance of __EventConsumerProviderRegistration
{
    Provider = $P;
    ConsumerClassNames = { "MyConsumer" };
};
```

 

 



