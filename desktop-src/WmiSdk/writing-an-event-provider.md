---
description: Ein Ereignisanbieter ist ein COM-Objekt, das WMI mit Benachrichtigungen zu systeminternen und extrinsischen Ereignissen liefert.
ms.assetid: 075bdc65-4ea3-4f91-9823-1d2d0dc13423
ms.tgt_platform: multiple
title: Schreiben eines Ereignisanbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c04abf060ef5316790b04682430abd92d0a6bea31175f0e192fc7f73d047633d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757210"
---
# <a name="writing-an-event-provider"></a>Schreiben eines Ereignisanbieters

Ein Ereignisanbieter ist ein COM-Objekt, das WMI mit Benachrichtigungen zu systeminternen und extrinsischen Ereignissen liefert. Ein systeminternes Ereignis meldet eine interne Datenänderung an WMI, während ein extrinsisches Ereignis ein benutzerdefiniertes Ereignis meldet, das nicht von einem systeminternen Ereignis beschrieben wird. Beispielsweise würde ein Ereignis als Reaktion auf Änderungen, Erstellung oder Löschung der [**Win32 \_ LogicalDisk-Klasse**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) als systeminternes Ereignis klassifiziert. Ein Ereignis, das auf der Grundlage eines anderen Ereignisses als der Änderung, Erstellung oder Löschung eines vorhandenen WMI-Objekts generiert wird, ist ein extrinsisches Ereignis. Unabhängig von der unterstützten Klasse können Sie alle Ereignisanbieter auf die gleiche Weise implementieren.

Im folgenden Verfahren wird beschrieben, wie sie einen Ereignisanbieter implementieren.

**So implementieren Sie einen Ereignisanbieter**

1.  Entwerfen und registrieren Sie Ihren Klassenanbieter bei WMI.

    Klassenanbieter registrieren sich bei WMI, indem sie eine [**\_ \_ Win32Provider-Instanz**](--win32provider.md) und eine [**\_ \_ EventProviderRegistration-Klasse**](--eventproviderregistration.md) erstellen. Weitere Informationen finden Sie unter [Registrieren eines Ereignisanbieters.](registering-an-event-provider.md)

2.  Implementieren Sie [**die IWbemProviderInit-Schnittstelle**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) für Ihren Anbieter.

    Die [**IWbemProviderInit-Schnittstelle**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) ist eine gemeinsame Schnittstelle, die WMI zum Laden und Initialisieren aller Anbieter verwendet. Weitere Informationen finden Sie unter [Initialisieren eines Anbieters.](initializing-a-provider.md)

3.  Implementieren Sie [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) als primäre Schnittstelle für Ihren Anbieter.

    Die [**IWbemEventProvider-Schnittstelle**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) verwendet die **ProviderEvents-Methode,** um Ereignisse an WMI zu senden. Weitere Informationen finden Sie unter [Implementieren der primären Schnittstelle für einen Ereignisanbieter.](implementing-the-primary-interface-for-an-event-provider.md)

    > [!Note]  
    > Ereignisanbieter müssen das Multithreadingmodell "Both" verwenden.

     

4.  Optional können Sie auch die [**IWbemEventProviderQuerySink-Schnittstelle**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink) implementieren, um die Leistung Ihres Ereignisanbieters zu erhöhen.

    Die [**IWbemEventProviderQuerySink-Schnittstelle**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink) ermöglicht es dem Anbieter, Abfragen vor dem Senden einer Antwort an WMI zu optimieren, und ist besonders nützlich für einen Anbieter, der Ereignisse mehrerer Typen liefert und so viele interne Optimierungen wie möglich ausführen muss. Weitere Informationen finden Sie unter [Optimieren eines Ereignisanbieters.](optimizing-an-event-provider.md)

5.  Implementieren Sie die [**IWbemEventProviderSecurity-Schnittstelle,**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovidersecurity) um Die Benutzer auf bestimmte Sicherheits-IDs (SIDs) zu beschränken, oder implementieren Sie [**IWbemEventSink::SetSinkSecurity,**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) um die Senke selbst zu schützen. Der Anbieter kann auch die **SECURITY \_ DESCRIPTOR-Eigenschaft** in der Ereignisklasse festlegen, um einzelne Ereignisse im MOF-Code zu schützen. Weitere Informationen finden Sie unter [Sichern von WMI-Ereignissen.](securing-wmi-events.md)
6.  Fügen Sie zusätzlichen Code hinzu, der für Ihren Anbieter erforderlich ist.

    Beim Entwerfen Ihres Anbieters müssen Sie wahrscheinlich WMI-Schnittstellen aufrufen. Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

    Beim Abrufen von Informationen für einen Client müssen Sie möglicherweise auf die Sicherheitsebenen für diesen Client zugreifen. Weitere Informationen finden Sie unter [Impersonating a Client](impersonating-a-client.md).

7.  Ersetzen Sie den bereits vorhandene Anbieter durch Ihren neuen Code.

    Sie müssen diesen Schritt nicht ausführen, wenn Sie nicht über einen bereits vorhandene Anbieter zum Kopieren verfügen. Weitere Informationen finden Sie unter [Aktualisieren eines Anbieters.](updating-a-provider.md)

Eine Clientanwendung kann ein Ereignis anfordern, indem sie sich selbst bei WMI als Ereignisverbraucher registriert. Weitere Informationen finden Sie unter [Empfangen eines WMI-Ereignisses.](receiving-a-wmi-event.md)

 

 
