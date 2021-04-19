---
description: Ein Instanzanbieter stellt Instanzen von einer oder mehreren angegebenen Klassen bereit.
ms.assetid: d53c3399-cba8-4b5d-8da0-b5a23f94c0ae
ms.tgt_platform: multiple
title: Schreiben eines Instanzanbieters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bddfaa867624bd84cc975d32a8e7b747064d1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358536"
---
# <a name="writing-an-instance-provider"></a>Schreiben eines Instanzanbieters

Ein Instanzanbieter stellt Instanzen von einer oder mehreren angegebenen Klassen bereit. Ein Instanzanbieter kann z. b. Informationen zu einer CPU oder einer anderen Art von Hardware bereitstellen. Da sich die von einem Instanzanbieter verwalteten Objekte regelmäßig ändern, werden alle Instanzanbieter als Pull-Anbieter betrachtet. Das heißt, ein Anbieter, der Informationen zu einem verwalteten Objekt dynamisch abruft, wenn WMI eine Anforderung an die Informationen sendet. Der Name stammt aus der Idee, dass WMI die Informationen vom Anbieter im Auftrag einer Client Anforderung abruft. Mithilfe von pulltechnologien kann ein Instanzanbieter Abruf-, Enumerations-, Änderungs-, Lösch-und Abfrage Verarbeitung einer bestimmten-Instanz unterstützen.

Hochleistungs Anbieter können die Effizienz eines Instanzanbieters erhöhen oder Programm gesteuert auf die Daten zugreifen, die im System Monitor angezeigt werden. Weitere Informationen finden Sie unter [Erstellen eines Instanzanbieters in einen High-Performance-Anbieter](making-an-instance-provider-into-a-high-performance-provider.md).

Im folgenden Verfahren wird beschrieben, wie ein Instanzanbieter geschrieben wird.

**So schreiben Sie einen Instanzanbieter**

1.  [Registrieren Sie Ihren Anbieter bei WMI](registering-an-instance-provider.md).

    Instanzanbieter registrieren sich bei WMI, indem Sie eine [**\_ \_ Win32Provider**](--win32provider.md) -Instanz und eine [**\_ \_ instanceproviderregistration**](--instanceproviderregistration.md) -Klasse erstellen.

2.  [Initialisieren Sie den Anbieter](initializing-a-provider.md).

    WMI verwendet [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) , um einen Anbieter zu laden und zu initialisieren. Dies ist eine Aufgabe, die allen Anbietern gemeinsam ist.

    > [!Note]  
    > Instanzanbietern wird dringend empfohlen, das Multithreading-Modell "beide" zu verwenden.

     

3.  [Implementieren Sie die IWbemServices-Schnittstelle für Ihren Anbieter](implementing-the-primary-interface-for-an-instance-provider.md).

    Die [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Schnittstelle ist die primäre Schnittstelle für einen Instanzanbieter.

4.  Fügen Sie zusätzlichen Code hinzu, der für Ihren Anbieter erforderlich ist.

    Wenn Sie Ihren Anbieter entwerfen, müssen Sie wahrscheinlich WMI-Schnittstellen abrufen. Weitere Informationen finden Sie unter [Aufrufen von WMI-aufrufen](making-calls-to-wmi.md).

    Beim Abrufen von Informationen für einen Client müssen Sie möglicherweise auf die Sicherheitsebenen für diesen Client zugreifen. Weitere Informationen finden Sie unter Annehmen der Identität [eines Clients](impersonating-a-client.md).

5.  Implementieren Sie ggf. [die Hochleistungs Schnittstelle](improving-the-efficiency-of-an-instance-provider.md).

    Die Hochleistungs Schnittstelle erhöht die Geschwindigkeit, mit der der Anbieter auf WMI-Anforderungen reagieren kann.

6.  Implementieren Sie ggf. die [Unterstützung für Teil Instanzupdates](supporting-partial-instance-operations.md).

    Wie der Name schon sagt, ist eine partielle Instanzaktualisierung eine Technik, mit der nur ein Teil einer Instanz aktualisiert wird. Weitere Informationen zum Aufrufen einer partiellen Instanz von einem Client finden Sie unter [Aktualisieren eines Teils einer Instanz](updating-part-of-an-instance.md) und Abrufen eines Teils einer [WMI-Instanz](retrieving-part-of-an-instance.md).

7.  Ersetzen Sie den bereits vorhandenen Anbieter durch den neuen Code.

    Sie müssen diesen Schritt nicht ausführen, wenn Sie nicht über einen vorhandenen Anbieter verfügen, der kopiert werden soll. Weitere Informationen finden Sie unter [Aktualisieren eines Anbieters](updating-a-provider.md).

 

 



