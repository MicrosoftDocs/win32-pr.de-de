---
description: Ein Ereignisverbraucheranbieter ist eine Komponente der permanenten Consumerarchitektur, die bestimmt, welcher Permanentereignis-Consumer ein bestimmtes Ereignis behandelt.
ms.assetid: c5a0d0ec-99af-4815-9ad2-e59db70e04ce
ms.tgt_platform: multiple
title: Schreiben eines Ereignisverbraucheranbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 312e0c2ecbf02d8bb0a8f491339d191aadde41a66cd3e3228c3187d5dcf689e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118553097"
---
# <a name="writing-an-event-consumer-provider"></a>Schreiben eines Ereignisverbraucheranbieters

Ein Ereignisverbraucheranbieter ist eine Komponente der permanenten Consumerarchitektur, die bestimmt, welcher Permanentereignis-Consumer ein bestimmtes Ereignis behandelt. Sie sollten einen Ereignisverbraucheranbieter zusammen mit Ihren permanenten Ereignisverbrauchern erstellen, um Ereignisse ordnungsgemäß von WMI weiter zu routen.

Ein Ereignisverbraucheranbieter verknüpft einen Ereignisanbieter mit einer Liste von Consumerklassen. Instanzen dieser Consumerklassen empfangen dann Ereignisse von diesem Anbieter. WMI identifiziert basierend auf der [**\_ \_ EventConsumerProviderRegistration-Instanz,**](--eventconsumerproviderregistration.md) die die [**\_ \_ Win32Provider-Instanz**](--win32provider.md) des Consumeranbieters einer logischen Consumerklasse zu ordnet, an welchen Consumeranbieter die Ereignisse übermittelt werden. Benutzer erstellen Instanzen der Consumerklasse als Teil eines permanenten Abonnements. Wenn der Ereignisanbieter nicht ausgeführt wird, wenn ein Ereignis auftritt, startet WMI den Anbieter, wenn Ereignisse übermittelt werden müssen.

Im folgenden Verfahren wird beschrieben, wie ein Ereignisverbraucheranbieter implementiert wird.

**So implementieren Sie einen Ereignisverbraucheranbieter**

1.  Entwerfen Sie Consumerklassen in Managed Object Format (MOF), und registrieren Sie sie bei WMI. Weitere Informationen finden Sie unter [Entwerfen Managed Object Format -Klassen (MOF).](designing-managed-object-format--mof--classes.md)

    Klassenanbieter registrieren sich bei WMI, indem sie eine [**\_ \_ Win32Provider-Instanz**](--win32provider.md) und eine [**\_ \_ EventConsumerProviderRegistration-Klasse**](--eventconsumerproviderregistration.md) erstellen. Weitere Informationen finden Sie unter [Registrieren eines Ereignisverbraucheranbieters.](registering-an-event-consumer-provider.md)

2.  Implementieren Sie [**die IWbemProviderInit-Schnittstelle**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) für Ihren Anbieter.

    WMI verwendet [**IWbemProviderInit zum**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) Laden und Initialisieren eines Anbieters. Weitere Informationen finden Sie unter [Initialisieren eines Anbieters.](initializing-a-provider.md)

    > [!Note]  
    > Ereignisverbraucheranbietern wird dringend empfohlen, das Multithreadingmodell "Both" zu verwenden.

     

3.  Implementieren Sie [**die IWbemEventConsumerProvider-Schnittstelle**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) für Ihren Anbieter.

    Die [**IWbemEventConsumerProvider-Schnittstelle**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) ist die primäre Schnittstelle für einen Ereignisconsumeranbieter.

4.  Geben Sie mindestens einen physischen Consumers an, um die Ereignismeldungen von WMI zu empfangen.

    Ein physischer Consumer ist ein COM-Objekt, das einen permanenten Ereignis consumer darstellt. Alle physischen Benutzer müssen die [**IWbemUnboundObjectSink-Schnittstelle**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) implementieren. Weitere Informationen finden Sie unter [Implementieren eines physischen Consumers.](implementing-a-physical-consumer.md)

 

 



