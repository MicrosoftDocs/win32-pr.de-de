---
title: Registrieren eines COM-Rückrufs
description: Anstatt Änderungen im Status eines Auftrags abzufragen, können Sie sich registrieren, um eine Benachrichtigung zu erhalten, wenn sich der Status des Auftrags ändert.
ms.assetid: 29350ea4-f7a9-4a42-a531-2cf623fe247b
keywords:
- BITS des Übertragungsauftrags, Ereignisbenachrichtigung
- Registrieren für Ereignisbenachrichtigungs-BITS
- Bits für Ereignisbenachrichtigungen
- Ereignisbenachrichtigung BITS , Rückrufe
- Benachrichtigungsereignisse BITS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 753feb481a578c30322d18def07418c2dcb611d601fcb438b0e85e843697790b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118680004"
---
# <a name="registering-a-com-callback"></a>Registrieren eines COM-Rückrufs

Anstatt Änderungen im Status eines Auftrags [abzufragen,](polling-for-the-status-of-the-job.md) können Sie sich registrieren, um eine Benachrichtigung zu erhalten, wenn sich der Status des Auftrags ändert. Um Benachrichtigungen zu erhalten, müssen Sie die [**IBackgroundCopyCallback2-Schnittstelle**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) implementieren. Die -Schnittstelle enthält die folgenden Methoden, die BITS abhängig von Ihrer Registrierung aufruft:

-   [**JobTransferred**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred)
-   [**JobError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-joberror)
-   [**JobModification**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobmodification)
-   [**FileTransferred**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopycallback2-filetransferred)

Ein Beispiel, das die [**IBackgroundCopyCallback2-Schnittstelle**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) implementiert, finden Sie im Beispielcode im Thema [**IBackgroundCopyCallback interface (IBackgroundCopyCallback-Schnittstelle).**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback)

Die [**IBackgroundCopyCallback2-Schnittstelle**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) stellt eine Benachrichtigung bereit, wenn eine Datei übertragen wird. In der Regel verwenden Sie diese Methode, um die Datei zu überprüfen, sodass die Datei für Peers zum Herunterladen verfügbar ist. Andernfalls ist die Datei erst für Peers verfügbar, wenn Sie die [**IBackgroundCopyJob::Complete-Methode**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) aufrufen. Rufen Sie zum Überprüfen der Datei die [**IBackgroundCopyFile3::SetValidationState-Methode auf.**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate)

Es gibt zwei Methoden zum Registrieren eines COM-Rückrufs: das Registrieren eines Rückrufobjekts oder das Registrieren einer Rückrufklassen-ID. Die Verwendung eines Rückrufobjekts ist einfacher und geringerer Aufwand. Die Verwendung einer Rückruf-CLSID ist zuverlässiger, aber komplizierter. Sie können entweder beides oder keines registrieren– BITS verwendet ein Rückrufobjekt, sofern vorhanden, und kann trotzdem aufgerufen werden. Andernfalls wird ein Fallback auf die Instanziierung eines neuen Objekts basierend auf einer bereitgestellten Klassen-ID verwendet.

### <a name="registering-a-callback-object"></a>Registrieren eines Rückrufobjekts

Um Ihre Implementierung bei BITS zu registrieren, rufen Sie die [**IBackgroundCopyJob::SetNotifyInterface-Methode**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) auf. Um anzugeben, welche Methoden BITS aufruft, rufen Sie die [**IBackgroundCopyJob::SetNotifyFlags-Methode**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags)auf.

Die Benachrichtigungsschnittstelle wird ungültig, wenn Ihre Anwendung beendet wird. BITS hält die Benachrichtigungsschnittstelle nicht bei. Daher sollte der Initialisierungsprozess Ihrer Anwendung vorhandene Aufträge registrieren, für die Sie eine Benachrichtigung erhalten möchten. Wenn Sie Status- und Statusinformationen erfassen müssen, die seit der letzten Ausführung der Anwendung aufgetreten sind, suchen Sie während der Anwendungsinitialisierung nach Status- und Statusinformationen.

Vor dem Beenden sollte Ihre Anwendung den Rückrufschnittstellenzeiger löschen (**SetNotifyInterface(NULL)**). Es ist effizienter, den Rückrufzeiger zu löschen, als bits erkennen zu lassen, dass er nicht mehr gültig ist.

Beachten Sie Folgendes: Wenn mehr als eine Anwendung die [**SetNotifyInterface-Methode**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) aufruft, um die Benachrichtigungsschnittstelle für den Auftrag festzulegen, ist die letzte Anwendung, die die **SetNotifyInterface-Methode** aufruft, diejenige, die Benachrichtigungen empfängt– die anderen Anwendungen empfangen keine Benachrichtigungen.

Das folgende Beispiel zeigt, wie Sie sich für Benachrichtigungen registrieren. Im Beispiel wird davon ausgegangen, dass der [**IBackgroundCopyJob-Schnittstellenzeiger**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) gültig ist. Ausführliche Informationen zur CNotifyInterface-Beispielklasse, die im folgenden Beispiel verwendet wird, finden Sie in der [**IBackgroundCopyCallback-Schnittstelle.**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback)


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
CNotifyInterface *pNotify = new CNotifyInterface();

if (pNotify)
{
    hr = pJob->SetNotifyInterface(pNotify);
    if (SUCCEEDED(hr))
    {
        hr = pJob->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED | 
                                  BG_NOTIFY_JOB_ERROR );
    }
    pNotify->Release();
    pNotify = NULL;

    if (FAILED(hr))
    {
        //Handle error - unable to register callbacks.
    }
}
```



### <a name="registering-a-callback-clsid"></a>Registrieren einer Rückruf-CLSID

Um eine Rückruf-CLSID bei BITS zu registrieren, rufen Sie die [**IBackgroundCopyJob5::SetProperty-Methode**](/windows/desktop/api/Bits5_0/nf-bits5_0-ibackgroundcopyjob5-setproperty) mit der **BITS \_ JOB PROPERTY \_ NOTIFICATION \_ \_ CLSID** PropertyId auf. Um anzugeben, welche Methoden BITS aufruft, rufen Sie die [**IBackgroundCopyJob::SetNotifyFlags-Methode**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) auf.

Sie müssen sicherstellen, dass die Benachrichtigungs-CLSID bei einem out-of-process-COM-Server registriert ist, bevor Sie die CLSID bei einem BITS-Auftrag registrieren. Die Implementierung eines [COM-Servers](/windows/desktop/com/com-server-responsibilities) ist deutlich komplizierter als das Definieren und Übergeben eines Rückrufobjekts, bietet aber mehrere wichtige Vorteile. Ein COM-Server ermöglicht BITS, die Zuordnung zwischen einem BITS-Auftrag und dem Code Ihrer Anwendung über Systemneustarts hinweg und für große oder langlebige Aufträge beizubehalten. Ein COM-Server ermöglicht Es Ihrer Anwendung auch, vollständig herunterzufahren, während BITS weiterhin Übertragungen im Hintergrund ausführt, was die Akku-, CPU- und Arbeitsspeicherauslastung des Systems verbessern kann.

Um eine Benachrichtigung bereitzustellen, die Sie für den Empfang registriert haben, versucht BITS zunächst, die entsprechende Methode eines vorhandenen Rückrufobjekts aufzurufen, das Sie möglicherweise angefügt haben. Wenn kein vorhandenes Objekt vorhanden ist oder das vorhandene Objekt getrennt wurde (in der Regel aufgrund des Beendens der Anwendung), ruft BITS CoCreateInstance mithilfe der Benachrichtigungs-CLSID auf, um ein neues Rückrufobjekt zu instanziieren, und verwendet dieses Objekt für alle weiteren Rückrufe, bis es getrennt wird oder durch einen neuen Aufruf von [**IBackgroundCopyJob::SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface)ersetzt wird.

Im Gegensatz zu Rückrufobjekten wird die Rückruf-CLSID zusammen mit ihren entsprechenden BITS-Auftrag(en) beibehalten, wenn der BITS-Dienst oder das System heruntergefahren und neu gestartet werden. Ihre Anwendung löscht möglicherweise jede zuvor festgelegte Benachrichtigungs-CLSID vor dem Beenden (oder zu einem anderen Zeitpunkt), indem sie eine neue Benachrichtigungs-CLSID von GUID \_ NULL übergibt. Ihre Anwendung bevorzugt jedoch die Benachrichtigungs-CLSID registriert, wenn ihre Anwendung registriert ist, damit COM sie als Reaktion auf CoCreateInstance-Anforderungen für Ihre CLSID startet. Beachten Sie Folgendes: Wenn mehr als eine Anwendung die **BITS \_ JOB PROPERTY NOTIFICATION \_ \_ \_ CLSID-Eigenschaft** aufruft, ist die letzte festzulegende CLSID die CLSID, die BITS zum Instanziieren von Rückrufobjekten verwendet– die anderen CLSIDs werden nicht instanziiert. Wenn eine Anwendung eine CLSID registriert und eine andere ein Rückrufobjekt registriert, gelten die üblichen Regeln für das Rückrufobjekt, das Vorrang hat, und die CLSID wird nur verwendet, wenn das Rückrufobjekt gelöscht oder getrennt wird.

Das folgende Beispiel zeigt, wie Sie sich für CLSID-Benachrichtigungen registrieren. Im Beispiel wird davon ausgegangen, dass der [**IBackgroundCopyJob5-Schnittstellenzeiger**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) gültig ist und dass Ihre Anwendung bereits als out-of-process-COM-Server registriert wurde, der die CNotifyInterface-Klasse implementiert. Ausführliche Informationen zur CNotifyInterface-Beispielklasse, die im folgenden Beispiel verwendet wird, finden Sie in der [**IBackgroundCopyCallback-Schnittstelle.**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback)


```C++
HRESULT hr; 
IBackgroundCopyJob5* job; 
BITS_JOB_PROPERTY_VALUE propertyValue; 
propertyValue.ClsID = __uuidof(CNotifyInterface); 

hr = job->SetProperty(BITS_JOB_PROPERTY_NOTIFICATION_CLSID, propertyValue); 
if (SUCCEEDED(hr)) 
{ 
    hr = job->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED |  
                             BG_NOTIFY_JOB_ERROR); 
} 

if (FAILED(hr)) 
{ 
    // Handle error - unable to register callbacks. 
} 
```



 

 