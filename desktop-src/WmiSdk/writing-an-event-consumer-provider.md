---
description: Ein Ereignisconsumeranbieter ist eine Komponente der permanenten consumerarchitektur, die bestimmt, welcher permanente Ereignisconsumer ein bestimmtes Ereignis behandelt.
ms.assetid: c5a0d0ec-99af-4815-9ad2-e59db70e04ce
ms.tgt_platform: multiple
title: Schreiben eines Ereignisconsumeranbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c7aeeb9b44b37d887df49cf5049d5a9e59ad72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347435"
---
# <a name="writing-an-event-consumer-provider"></a>Schreiben eines Ereignisconsumeranbieters

Ein Ereignisconsumeranbieter ist eine Komponente der permanenten consumerarchitektur, die bestimmt, welcher permanente Ereignisconsumer ein bestimmtes Ereignis behandelt. Sie sollten einen Ereignisconsumeranbieter zusammen mit ihren permanenten Ereignisconsumer erstellen, um Ereignisse ordnungsgemäß aus WMI zu leiten.

Ein Ereignisconsumeranbieter verknüpft einen Ereignis Anbieter mit einer Liste von Consumerklassen. Instanzen dieser Consumerklassen empfangen dann Ereignisse von diesem Anbieter. WMI identifiziert den Consumeranbieter, an den die Ereignisse übermittelt werden, basierend auf der [**\_ \_ eventconsumerproviderregistration**](--eventconsumerproviderregistration.md) -Instanz, die die [**\_ \_ Win32Provider**](--win32provider.md) -Instanz des consumeranbieters einer logischen Consumerklasse zuordnet. Benutzer erstellen Instanzen der Consumer-Klasse als Teil eines permanenten Abonnements. Wenn der Ereignis Anbieter nicht ausgeführt wird, wenn ein Ereignis auftritt, startet WMI den Anbieter, wenn er Ereignisse übermitteln muss.

Im folgenden Verfahren wird beschrieben, wie ein Ereignisconsumeranbieter implementiert wird.

**So implementieren Sie einen Ereignisconsumeranbieter**

1.  Entwerfen Sie Consumerklassen in Managed Object Format (MOF), und registrieren Sie Sie bei WMI. Weitere Informationen finden Sie unter [Entwerfen von Managed Object Format-Klassen (MOF)](designing-managed-object-format--mof--classes.md).

    Klassen Anbieter registrieren sich bei WMI durch Erstellen einer [**\_ \_ Win32Provider**](--win32provider.md) -Instanz und einer [**\_ \_ eventconsumerproviderregistration**](--eventconsumerproviderregistration.md) -Klasse. Weitere Informationen finden Sie unter [Registrieren eines Ereignisconsumeranbieters](registering-an-event-consumer-provider.md).

2.  Implementieren Sie die [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) -Schnittstelle für Ihren Anbieter.

    WMI verwendet [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) , um einen Anbieter zu laden und zu initialisieren. Weitere Informationen finden Sie unter [Initialisieren eines Anbieters](initializing-a-provider.md).

    > [!Note]  
    > Ereignisconsumeranbietern wird dringend empfohlen, das Multithreading Modell "both" zu verwenden.

     

3.  Implementieren Sie die [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) -Schnittstelle für Ihren Anbieter.

    Die [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) -Schnittstelle ist die primäre Schnittstelle für einen Ereignisconsumeranbieter.

4.  Stellen Sie einen oder mehrere physische Consumer bereit, um die Ereignis Nachrichten von WMI zu empfangen.

    Ein physischer Consumer ist ein COM-Objekt, das einen permanenten Ereignisconsumer darstellt. Alle physischen Consumer müssen die [**iwbemunboundobjectsink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) -Schnittstelle implementieren. Weitere Informationen finden Sie unter [Implementieren eines physischen](implementing-a-physical-consumer.md)Consumers.

 

 



