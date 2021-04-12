---
title: Registrieren eines com-Rückrufs
description: Anstatt Änderungen am Status eines Auftrags abzufragen, können Sie sich registrieren, um eine Benachrichtigung zu erhalten, wenn sich der Status des Auftrags ändert.
ms.assetid: 29350ea4-f7a9-4a42-a531-2cf623fe247b
keywords:
- Übertragen von Auftrags Bits, Ereignis Benachrichtigung
- Registrieren für Ereignis Benachrichtigungs Bits
- Ereignis Benachrichtigungs Bits
- Ereignis Benachrichtigungs Bits, Rückrufe
- Bits von Benachrichtigungs Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdcc52c772656c2168af9c10724ee43fac25aa80
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315693"
---
# <a name="registering-a-com-callback"></a>Registrieren eines com-Rückrufs

Anstatt Änderungen am [Status eines Auftrags](polling-for-the-status-of-the-job.md) abzufragen, können Sie sich registrieren, um eine Benachrichtigung zu erhalten, wenn sich der Status des Auftrags ändert. Um Benachrichtigungen zu erhalten, müssen Sie die [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) -Schnittstelle implementieren. Die-Schnittstelle enthält die folgenden Methoden, die von Bits aufgerufen werden, abhängig von Ihrer Registrierung:

-   [**Jobübertragene**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred)
-   [**Joberror**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-joberror)
-   [**Jobmodifizierung**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobmodification)
-   [**Filetransfer**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopycallback2-filetransferred)

Ein Beispiel, in dem die [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) -Schnittstelle implementiert wird, finden Sie im Beispielcode im Thema [**ibackgroundcopycallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) -Schnittstelle.

Die [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) -Schnittstelle stellt Benachrichtigungen bereit, wenn eine Datei übertragen wird. Normalerweise verwenden Sie diese Methode, um die Datei zu validieren, damit die Datei für Peers verfügbar ist, um sie herunterzuladen. Andernfalls ist die Datei für Peers nicht verfügbar, bis Sie die Methode [**ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) aufgerufen haben. Um die Datei zu überprüfen, müssen Sie die [**IBackgroundCopyFile3:: setvalidationstate**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) -Methode aufrufen.

Es gibt zwei Methoden zum Registrieren eines com-Rückrufs: das Registrieren eines Rückruf Objekts oder das Registrieren einer Rückruf Klassen-ID. Die Verwendung eines Rückruf Objekts ist einfacher und geringerer Aufwand. die Verwendung einer Rückruf-CLSID ist zuverlässiger, aber komplizierter. Sie können entweder, beides oder keines von beiden – Bits verwendet ein Rückruf Objekt, wenn ein solches vorhanden ist und weiterhin aufgerufen werden kann. wenn dies nicht der Fall ist, wird ein neues Objekt auf der Grundlage einer bereitgestellten Klassen-ID instanziiert.

### <a name="registering-a-callback-object"></a>Registrieren eines Rückruf Objekts

Um die Implementierung mit Bits zu registrieren, müssen Sie die [**ibackgroundcopyjob:: setnotifyinterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) -Methode aufrufen. Um anzugeben, welche Methoden Bits aufruft, rufen Sie die [**ibackgroundcopyjob:: setnotifyflags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags)-Methode auf.

Die Benachrichtigungs Schnittstelle wird ungültig, wenn die Anwendung beendet wird. Bits behält die Benachrichtigungs Schnittstelle nicht bei. Folglich sollte der Initialisierungs Prozess ihrer Anwendung vorhandene Aufträge registrieren, für die Sie eine Benachrichtigung erhalten möchten. Wenn Sie Zustands-und Statusinformationen erfassen müssen, die seit der letzten Ausführung der Anwendung aufgetreten sind, rufen Sie während der Anwendungs Initialisierung Informationen zum Status und zum Fortschritt ab.

Bevor die Anwendung beendet wird, sollte Sie den Rückruf Schnittstellen Zeiger (**setnotifyinterface (null)**) löschen. Es ist effizienter, den Rückruf Zeiger zu löschen, als Bits feststellen zu können, dass er nicht mehr gültig ist.

Beachten Sie Folgendes: Wenn mehr als eine Anwendung die [**setnotifyinterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) -Methode aufruft, um die Benachrichtigungs Schnittstelle für den Auftrag festzulegen, ist die letzte Anwendung, die die **setnotifyinterface** -Methode aufruft, die, die Benachrichtigungen empfängt – die anderen Anwendungen erhalten keine Benachrichtigungen.

Im folgenden Beispiel wird gezeigt, wie Sie sich für Benachrichtigungen registrieren. Im Beispiel wird davon ausgegangen, dass der [**ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) -Schnittstellen Zeiger gültig ist. Ausführliche Informationen zur cnotifyinterface-Beispiel Klasse, die im folgenden Beispiel verwendet wird, finden Sie unter [**ibackgroundcopycallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) -Schnittstelle.


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

Um eine Rückruf-CLSID mit Bits zu registrieren, rufen Sie die [**IBackgroundCopyJob5:: SetProperty**](/windows/desktop/api/Bits5_0/nf-bits5_0-ibackgroundcopyjob5-setproperty) -Methode mit der **\_ \_ \_ Benachrichtigung \_ CLSID** PropertyId für die Bits-Auftrags Eigenschaft auf. Um anzugeben, welche Methoden Bits aufruft, rufen Sie die [**ibackgroundcopyjob:: setnotifyflags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) -Methode auf.

Sie müssen sicherstellen, dass die Benachrichtigungs-CLSID bei einem Out-of-Process-COM-Server registriert wird, bevor die CLSID bei einem BITS-Auftrag registriert wird. Das Implementieren eines [com-Servers](/windows/desktop/com/com-server-responsibilities) ist wesentlich komplizierter als das definieren und übergeben eines Rückruf Objekts, bietet jedoch einige wichtige Vorteile. Mit einem com-Server können Bits die Zuordnung zwischen einem BITS-Auftrag und dem Code Ihrer Anwendung über Systemneustarts hinweg und für große oder langlebige Aufträge hinweg aufrechterhalten. Ein com-Server ermöglicht außerdem, dass Ihre Anwendung vollständig heruntergefahren wird, während Bits die Ausführung von Übertragungen im Hintergrund fortsetzt, wodurch die Akku-, CPU-und Speicherauslastung des Systems verbessert werden kann.

Um eine Benachrichtigung bereitzustellen, die Sie für den Empfang registriert haben, versucht Bits zuerst, die entsprechende Methode eines beliebigen vorhandenen Rückruf Objekts aufzurufen, das Sie möglicherweise angefügt haben. Wenn kein vorhandenes Objekt vorhanden ist, wenn das vorhandene Objekt getrennt wurde (in der Regel aufgrund der Beendigung der Anwendung), ruft Bits mithilfe der Benachrichtigungs-CLSID ein neues Rückruf Objekt ab und verwendet dieses Objekt für alle weiteren Rückrufe, bis es getrennt wird, oder es wird durch einen neuen [**ibackgroundcopyjob:: setnotifyinterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface)-Befehl ersetzt.

Im Gegensatz zu Rückruf Objekten werden Rückruf-CLSID neben den entsprechenden Bits-Aufträgen persistent gespeichert, wenn der BITS-Dienst oder das System heruntergefahren und neu gestartet wird. Die Anwendung löscht ggf. alle zuvor festgelegten Benachrichtigungs-CLSID, bevor Sie (oder zu einem anderen Zeitpunkt) beendet wird, indem Sie eine neue Benachrichtigungs-CLSID mit der GUID \_ null übergibt. Ihre Anwendung kann jedoch vorziehen, dass die Benachrichtigungs-CLSID registriert ist, wenn Ihre Anwendung registriert ist Beachten Sie Folgendes: Wenn mehr als eine Anwendung den-Wert aufruft, der die Eigenschaft **\_ \_ \_ Benachrichtigungs- \_ CLSID für Bits-Auftrags Eigenschaften** aufruft, wird die letzte CLSID festgelegt, die Bits zum Instanziieren von Rückruf Objekten verwendet – die anderen CLSIDs werden nicht instanziiert. Ebenso gilt: Wenn eine Anwendung eine CLSID registriert und ein anderes ein Rückruf Objekt registriert, gelten die üblichen Regeln für das Rückruf Objekt, die Vorrang haben, und die CLSID wird nur dann verwendet, wenn das Rückruf Objekt gelöscht wird oder getrennt wird.

Im folgenden Beispiel wird gezeigt, wie Sie sich für CLSID-Benachrichtigungen registrieren. Im Beispiel wird davon ausgegangen, dass der [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) -Schnittstellen Zeiger gültig ist und dass Ihre Anwendung bereits als Prozess interner com-Server registriert ist, der die cnotifyinterface-Klasse implementiert. Ausführliche Informationen zur cnotifyinterface-Beispiel Klasse, die im folgenden Beispiel verwendet wird, finden Sie unter [**ibackgroundcopycallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) -Schnittstelle.


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



 

 