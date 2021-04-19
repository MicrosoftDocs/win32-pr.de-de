---
description: Ein Ereignis Anbieter ist ein COM-Objekt, das WMI Benachrichtigungen zu systeminternen und extrinsischen Ereignissen liefert.
ms.assetid: 075bdc65-4ea3-4f91-9823-1d2d0dc13423
ms.tgt_platform: multiple
title: Schreiben eines Ereignis Anbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb118d89f214e9fc651c1c9d93abfcfe43f49fc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360008"
---
# <a name="writing-an-event-provider"></a>Schreiben eines Ereignis Anbieters

Ein Ereignis Anbieter ist ein COM-Objekt, das WMI Benachrichtigungen zu systeminternen und extrinsischen Ereignissen liefert. Ein System internes Ereignis meldet eine interne Datenänderung an WMI, während ein System externe-Ereignis ein benutzerdefiniertes Ereignis meldet, das nicht von einem systeminternen Ereignis beschrieben wird. Beispielsweise würde ein Ereignis als Reaktion auf Änderungen, Erstellung oder Löschung der [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Klasse als System internes Ereignis klassifiziert werden. Ein Ereignis, das auf der Grundlage einer anderen als der Änderung, Erstellung oder Löschung eines vorhandenen WMI-Objekts generiert wird, ist ein extrinsisches Ereignis. Unabhängig von der unterstützten Klasse können Sie alle Ereignis Anbieter auf die gleiche Weise implementieren.

Im folgenden Verfahren wird beschrieben, wie ein Ereignis Anbieter implementiert wird.

**So implementieren Sie einen Ereignis Anbieter**

1.  Entwerfen und registrieren Sie den Klassen Anbieter bei WMI.

    Klassen Anbieter registrieren sich bei WMI durch Erstellen einer [**\_ \_ Win32Provider**](--win32provider.md) -Instanz und einer [**\_ \_ eventproviderregistration**](--eventproviderregistration.md) -Klasse. Weitere Informationen finden Sie unter [Registrieren eines Ereignis Anbieters](registering-an-event-provider.md).

2.  Implementieren Sie die [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) -Schnittstelle für Ihren Anbieter.

    Die [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) -Schnittstelle ist eine gemeinsame Schnittstelle, mit der WMI alle Anbieter lädt und initialisiert. Weitere Informationen finden Sie unter [Initialisieren eines Anbieters](initializing-a-provider.md).

3.  Implementieren Sie den [**iwbemeventprovider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) als primäre Schnittstelle für Ihren Anbieter.

    Die [**iwbemeventprovider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) -Schnittstelle verwendet die **providerevents** -Methode, um Ereignisse für WMI bereitzustellen. Weitere Informationen finden Sie unter [Implementieren der primären Schnittstelle für einen Ereignis Anbieter](implementing-the-primary-interface-for-an-event-provider.md).

    > [!Note]  
    > Ereignis Anbieter müssen das Multithreading Modell "both" verwenden.

     

4.  Optional können Sie auch die [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink) -Schnittstelle implementieren, um die Leistung des Ereignis Anbieters zu erhöhen.

    Die [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink) -Schnittstelle ermöglicht dem Anbieter die Optimierung von Abfragen vor dem Senden einer Antwort an WMI. Dies ist besonders nützlich für einen Anbieter, der Ereignisse mehrerer Typen bereitstellt und so viele interne Optimierungen wie möglich ausführen muss. Weitere Informationen finden Sie unter [Optimieren eines Ereignis Anbieters](optimizing-an-event-provider.md).

5.  Implementieren Sie die [**IWbemEventProviderSecurity**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovidersecurity) -Schnittstelle, um Consumer auf bestimmte Sicherheits-IDs (SIDs) zu beschränken, oder implementieren Sie [**iwbemeventsink:: setsink Security**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) , um die Senke selbst zu sichern. Der Anbieter kann auch die **\_ sicherheitsbeschreibungenschaft** in der-Ereignisklasse festlegen, um einzelne Ereignisse im MOF-Code zu sichern. Weitere Informationen finden Sie unter [Sichern von WMI-Ereignissen](securing-wmi-events.md).
6.  Fügen Sie zusätzlichen Code hinzu, der für Ihren Anbieter erforderlich ist.

    Wenn Sie Ihren Anbieter entwerfen, müssen Sie wahrscheinlich WMI-Schnittstellen abrufen. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

    Beim Abrufen von Informationen für einen Client müssen Sie möglicherweise auf die Sicherheitsebenen für diesen Client zugreifen. Weitere Informationen finden Sie unter Annehmen der Identität [eines Clients](impersonating-a-client.md).

7.  Ersetzen Sie den bereits vorhandenen Anbieter durch den neuen Code.

    Sie müssen diesen Schritt nicht ausführen, wenn Sie nicht über einen vorhandenen Anbieter verfügen, der kopiert werden soll. Weitere Informationen finden Sie unter [Aktualisieren eines Anbieters](updating-a-provider.md).

Eine Client Anwendung kann ein Ereignis anfordern, indem Sie sich selbst bei WMI als Ereignisconsumer registriert. Weitere Informationen finden Sie unter [empfangen eines WMI-Ereignisses](receiving-a-wmi-event.md).

 

 
