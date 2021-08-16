---
description: Zum Erstellen eines WMI-Ereignisconsumeranbieters müssen Sie die \_ \_ Win32Provider-Instanz registrieren, die Ihren Anbieter darstellt, indem Sie eine Instanz von \_ \_ EventConsumerProviderRegistration verwenden.
ms.assetid: d1aa035c-f9ee-46b5-9fa5-8af77156f904
ms.tgt_platform: multiple
title: Registrieren eines Ereignisverbraucheranbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1922970838b99e2a4a371ed7b00ae0f506a0381f0018509bfd6874074e0dd8f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992541"
---
# <a name="registering-an-event-consumer-provider"></a>Registrieren eines Ereignisverbraucheranbieters

Zum Erstellen eines [*WMI-Ereignisconsumeranbieters*](gloss-e.md) müssen Sie die [**\_ \_ Win32Provider-Instanz**](--win32provider.md) registrieren, die Ihren Anbieter darstellt, indem Sie eine Instanz von [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md)verwenden. Als COM-Objekt muss sich Ihr Anbieter beim Betriebssystem und WMI registrieren. Im folgenden Verfahren wird davon ausgegangen, dass Sie den Registrierungsprozess bereits implementiert haben, wie unter [Registrieren eines Anbieters](registering-a-provider.md)beschrieben.

Im folgenden Verfahren wird beschrieben, wie Sie einen Ereignisverbraucheranbieter registrieren.

**So registrieren Sie einen Ereignisverbraucheranbieter**

1.  Erstellen Sie eine Instanz der [**\_ \_ Win32Provider-Klasse,**](--win32provider.md) die den Anbieter beschreibt.
2.  Erstellen Sie eine Instanz der [**\_ \_ EventConsumerProviderRegistration-Klasse,**](--eventconsumerproviderregistration.md) die den Featuresatz des Anbieters beschreibt.

    Die von [**\_ \_ EventConsumerProviderRegistration definierten**](--eventconsumerproviderregistration.md) Eigenschaften enthalten den Objektpfad zum Anbieter und die Namen der logischen Consumerklassen, die der Ereignisconsumeranbieter unterstützt.

    Achten Sie darauf, die -Klasse mit den **Qualifizierern Dynamic** und [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) zu kennzeichnen. Der **dynamische** Qualifizierer signalisiert, dass WMI einen Anbieter verwenden soll, um die Klasseninstanzen abzurufen. Der **Anbieterqualifizierer** gibt den Namen des Anbieters an, den WMI verwenden soll.

Das folgende Codebeispiel zeigt, wie sie einen Ereignisverbraucheranbieter registrieren.

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

 

 



