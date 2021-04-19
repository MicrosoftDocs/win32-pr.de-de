---
description: Ein physischer Consumer ist ein COM-Objekt, das die iwbemunboundobjectsink-Schnittstelle implementiert.
ms.assetid: 497457dc-61ca-4527-89fd-2af0383de5e9
ms.tgt_platform: multiple
title: Implementieren eines physischen Consumers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af0a9530ed7a98ce19b3b39f2f5a1fe52f3b0631
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350356"
---
# <a name="implementing-a-physical-consumer"></a>Implementieren eines physischen Consumers

Ein physischer Consumer ist ein COM-Objekt, das die [**iwbemunboundobjectsink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) -Schnittstelle implementiert. WMI lädt den physischen Consumer und übergibt Ereignisse als Antwort auf ein oder mehrere Ereignisse, wie vom zugeordneten logischen Consumer definiert, durch **iwbemunboundobjectsink** . Permanente Verbraucher haben besondere Sicherheitsanforderungen. Weitere Informationen finden Sie unter [Sichern von WMI-Ereignissen](securing-wmi-events.md).

Im folgenden Verfahren wird beschrieben, wie ein physischer Consumer für einen permanenten Ereignisconsumer implementiert wird.

**So implementieren Sie einen physischen Consumer für einen permanenten Ereignisconsumer**

1.  Erstellen Sie ein COM-Objekt.

    Sie müssen einen physischen Consumer als lokalen Server oder Remote Server mit dem com-Protokoll implementieren.

2.  Bestimmen Sie, ob eine synchrone oder asynchrone Ereignis Benachrichtigung unterstützt werden soll.

    Bei der asynchronen Ereignis Benachrichtigung ist der sendende Thread nicht mit dem empfangenden Thread verknüpft. Daher wird weder WMI noch der Ereignis Anbieter blockiert, während WMI eine Benachrichtigung an jeden Consumer übergibt, der für den Empfang des Ereignisses registriert ist. Der Nachteil der asynchronen Übermittlung besteht darin, dass ein Kontextwechsel zwischen dem Zeitpunkt, zu dem der Anbieter das Ereignis erzeugt, und dem Zeitpunkt auftritt, zu dem der Consumer das Ereignis empfängt. Weitere Informationen zum asynchronen Arbeiten finden Sie im Thema zu den [com-Grundlagen](../com/guide.md) im com-Abschnitt des Microsoft Windows Software Development Kit (SDK). Weitere Informationen zu Kontext wechseln finden Sie im Abschnitt " [Kontext](../procthread/context-switches.md) Wechsel" im Abschnitt DLLs, Prozesse und Threads des Windows SDK.

    > [!Note]  
    > Da der Rückruf für die Senke möglicherweise nicht auf derselben Authentifizierungs Ebene wie der Client zurückgegeben wird, wird empfohlen, semisynchrone anstelle der asynchronen Kommunikation zu verwenden. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

     

    Bei der synchronen Benachrichtigung übermittelt WMI die Benachrichtigung in demselben Thread, den der Ereignis Anbieter verwendet hat, um das Ereignis an WMI zu übermitteln. Wenn in diesem Fall ein Ereignis Anbieter eine Benachrichtigung sendet, wird der Ereignis Anbieter von WMI blockiert, bis die Benachrichtigung von WMI übermittelt wird. Nur wenn Ihr Consumer extrem schnell ist und ein Ereignis in 100 Mikrosekunden oder weniger verarbeiten kann, sollten Sie die Unterstützung synchroner Benachrichtigungen in Erwägung gezogen. Synchrone Consumer, die zu lange dauern, um Ereignisse zu verarbeiten, können die Übermittlung von Ereignissen für alle anderen Consumer erheblich verlangsamen. Außerdem kann der Anbieter versehentlich blockiert werden. Weitere Informationen finden Sie unter [Binden eines Ereignis Filters mit einem logischen Consumer](binding-an-event-filter-with-a-logical-consumer.md).

3.  Implementieren Sie die [**iwbemunboundobjectsink:: jecetoconsumer**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemunboundobjectsink-indicatetoconsumer) -Funktion.

    WMI verwendet die [**Funktion "**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemunboundobjectsink-indicatetoconsumer) -Funktion", um die erforderlichen Zeiger und Ereignisse für die synchrone und asynchrone Kommunikation an den physischen Consumer zu übergeben. Ihre Implementierung von " **indikatetoconsumer** " muss den gesamten erforderlichen Code enthalten, um auf ein Ereignis zu reagieren.

    Anders als bei einem temporären Ereignisconsumer müssen Sie die [**IWBEMLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) -Schnittstelle nicht zum Kontaktieren von WMI anrufen. Stattdessen wird von WMI über den Ereignisconsumeranbieter ein Zeiger auf den Consumer angezeigt. Weitere Informationen finden Sie unter [Schreiben eines Ereignisconsumeranbieters](writing-an-event-consumer-provider.md).

    Wenn Sie jedoch WMI zurückkehren möchten, verwenden Sie die [**IWBEMLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) -Schnittstelle und die [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Schnittstelle. Die herkömmliche Methode zum Herstellen einer Verbindung mit WMI ist die Initialisierung des COM-Objekts. Weitere Informationen finden Sie unter [Erstellen einer WMI-Anwendung oder eines Skripts](creating-a-wmi-application-or-script.md).

    Wenn Sie den physischen Consumer als in-Process-COM-Server implementieren und getrennt vom Initialisierungs Prozess eine Verbindung mit WMI herstellen, müssen Sie für den Zugriff auf die [**IWBEMLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) -Schnittstelle im [**cokreateinstance-Code**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)die **\_ clbemlocator** -Schnittstelle verwenden.

    Im folgenden Beispiel wird gezeigt, wie der **CLSID \_ wbemadministrativelocator** -Klassen Bezeichner verwendet wird, um auf die [**IWBEMLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) -Schnittstelle zuzugreifen.

    ```C++
    IWbemLocator *pLoc = 0;

    DWORD dwRes = CoCreateInstance(CLSID_WbemAdministrativeLocator, 0, 
        CLSCTX_INPROC_SERVER, IID_IWbemLocator, (LPVOID *) &pLoc);
    ```

    

    Die [**IWBEMLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) -Schnittstelle erhält den anfänglichen Namespace Zeiger auf WMI auf einem bestimmten Host Computer. Wenn der **CLSID- \_ wbemadministrativelocator** -Bezeichner nicht im [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Befehl verwendet wird, führt dies zu einem Fehler vom Typ "Zugriff verweigert".

    Unter normalen Umständen werden von WMI asynchrone Ereignisse nacheinander an den Client übermittelt. Wenn ein Client jedoch nicht so schnell, wie die Ereignisse eintreffen, asynchrone Ereignis Benachrichtigungen empfangen kann, startet WMI automatisch eine Batch Verarbeitung von Ereignissen in einem einzelnen-Befehl. Die automatische Batch Verarbeitung hilft, wenn die Roundtrip-Zeiten ein Problem darstellen, wie es häufig bei Szenarios mit hohem Durchsatz der Fall ist. Die Batch Verarbeitung verbessert jedoch nicht die Systemleistung, wenn der Client oder die Netzwerkbandbreite fehlerhaft ist.

 

 
