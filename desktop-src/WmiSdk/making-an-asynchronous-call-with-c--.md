---
description: In C++ geschriebene WMI-Anwendungen können asynchrone Aufrufe mithilfe vieler Methoden der IWbemServices-COM-Schnittstelle vornehmen.
ms.assetid: 5179969f-bc7d-4408-84ef-7b003950a59f
ms.tgt_platform: multiple
title: Erstellen eines asynchronen Aufrufs mit C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcd988382399f3fc377476c486b363cf51db6c4d9ef559c787236e41bb74117a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131192"
---
# <a name="making-an-asynchronous-call-with-c"></a>Erstellen eines asynchronen Aufrufs mit C++

In C++ geschriebene WMI-Anwendungen können asynchrone Aufrufe mithilfe vieler Methoden der [**IWbemServices-COM-Schnittstelle**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) vornehmen. Das empfohlene Verfahren zum Aufrufen einer [*WMI-*](gloss-w.md) oder [*Anbietermethode*](gloss-p.md) ist jedoch die Verwendung von semisynchronen Aufrufen, da semisynchrone Aufrufe sicherer sind als asynchrone Aufrufe. Weitere Informationen finden Sie unter [Erstellen eines semisynchronen Aufrufs mit C++](making-a-semisynchronous-call-with-c--.md) und [Festlegen der Sicherheit für einen asynchronen Aufruf.](setting-security-on-an-asynchronous-call.md)

Im folgenden Verfahren wird beschrieben, wie Sie mithilfe der Senke in Ihrem Prozess einen asynchronen Aufruf ausführen.

**So erstellen Sie einen asynchronen Aufruf mit C++**

1.  Implementieren Sie die [**IWbemObjectSink-Schnittstelle.**](iwbemobjectsink.md)

    Alle Anwendungen, die asynchrone Aufrufe ausführen, müssen [**IWbemObjectSink**](iwbemobjectsink.md)implementieren. Temporäre Ereignisverbraucher implementieren auch **IWbemObjectSink,** um Benachrichtigungen über Ereignisse zu empfangen.

2.  Melden Sie sich beim WMI-Zielnamespace an.

    Anwendungen müssen während der Initialisierungsphase immer die COM-Funktion [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) aufrufen. Wenn sie dies nicht tun, bevor sie einen asynchronen Aufruf durchführen, gibt WMI die Anwendungssenke frei, ohne den asynchronen Aufruf abzuschließen. Weitere Informationen finden Sie unter [Initialisieren von COM für eine WMI-Anwendung.](initializing-com-for-a-wmi-application.md)

3.  Legen Sie die Sicherheit für Ihre Senke fest.

    Asynchrone Aufrufe erzeugen eine Vielzahl von Sicherheitsproblemen, mit denen Sie möglicherweise umgehen müssen, z. B. das Zulassen des WMI-Zugriffs auf Ihre Anwendung. Weitere Informationen finden Sie unter [Festlegen der Sicherheit für einen asynchronen Aufruf.](setting-security-on-an-asynchronous-call.md)

4.  Nehmen Sie den asynchronen Aufruf vor.

    Die -Methode gibt sofort mit dem **Erfolgscode WBEM \_ S NO \_ \_ ERROR** zurück. Die Anwendung kann mit anderen Aufgaben fortfahren, während auf den Abschluss des Vorgangs gewartet wird. WMI meldet die Anwendung zurück, indem Methoden in der [**IWbemObjectSink-Implementierung**](iwbemobjectsink.md) Ihrer Anwendung aufgerufen werden.

5.  Überprüfen Sie bei Bedarf Ihre Implementierung in regelmäßigen Abständen auf Updates.

    Anwendungen können eine Benachrichtigung über den Zwischenstatus erhalten, indem sie den *lFlags-Parameter* im asynchronen Aufruf von **WBEM \_ FLAG SEND \_ \_ STATUS** festlegen. WMI meldet den Status Ihres Aufrufs, indem der *lFlags-Parameter* von [**IWbemObjectSink**](iwbemobjectsink.md) auf **WBEM STATUS PROGRESS festgelegt \_ \_ wird.**

6.  Bei Bedarf können Sie den Aufruf abbrechen, bevor WMI die Verarbeitung beendet, indem Sie die [**IWbemServices::CancelCallAsync-Methode**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) aufrufen.

    Die [**CancelAsyncCall-Methode**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) bricht die asynchrone Verarbeitung ab, indem der Zeiger sofort auf die [**IWbemObjectSink-Schnittstelle**](iwbemobjectsink.md) freigegeben wird, und garantiert, dass der Zeiger freigegeben wird, bevor **CancelAsyncCall** zurückgegeben wird.

    Wenn Sie ein Wrapperobjekt verwenden, das die **IUnsecured-Schnittstelle** zum Hosten von [**IWbemObjectSink**](iwbemobjectsink.md)implementiert, treten möglicherweise zusätzliche Schwierigkeiten auf. Da die Anwendung den gleichen Zeiger an [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) übergeben muss, der im ursprünglichen asynchronen Aufruf übergeben wurde, muss die Anwendung an das Wrapperobjekt halten, bis klar wird, dass kein Abbruch erforderlich ist. Weitere Informationen finden Sie unter [Festlegen der Sicherheit für einen asynchronen Aufruf.](setting-security-on-an-asynchronous-call.md)

7.  Wenn Sie fertig sind, bereinigen Sie Zeiger, und fahren Sie die Anwendung herunter.

    WMI stellt den endgültigen Statusaufruf über die [**SetStatus-Methode**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) bereit.

    > [!Note]  
    > Nach dem Senden des endgültigen Statusupdates gibt WMI die Objektsenke frei, indem die **Release-Methode** für die Klasse aufgerufen wird, die die [**IWbemObjectSink-Schnittstelle**](iwbemobjectsink.md) implementiert. Im vorherigen Beispiel ist dies die **QuerySink::Release-Methode.** Wenn Sie die Lebensdauer des Senkenobjekts steuern möchten, können Sie die Senke mit einem anfänglichen Verweiszähler (1) implementieren.

     

    Wenn eine Clientanwendung dieselbe Senkenschnittstelle in zwei verschiedenen überlappenden asynchronen Aufrufen übergibt, garantiert WMI nicht die Reihenfolge des Rückrufs. Eine Clientanwendung, die überlappende asynchrone Aufrufe vornimmt, sollte entweder verschiedene Senkenobjekte übergeben oder die Aufrufe serialisieren.

Das folgende Beispiel erfordert den folgenden Verweis und \# include-Anweisungen.


```C++
#include <iostream>
using namespace std;
#pragma comment(lib, "wbemuuid.lib")
#include <wbemidl.h>
```



Im folgenden Beispiel wird beschrieben, wie eine asynchrone Abfrage mit der [**ExecQueryAsync-Methode**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) erstellt wird, aber keine Sicherheitseinstellungen erstellt oder das [**IWbemObjectSink-Objekt**](iwbemobjectsink.md) veröffentlicht wird. Weitere Informationen finden Sie unter [Festlegen der Sicherheit für einen asynchronen Aufruf.](setting-security-on-an-asynchronous-call.md)


```C++
// Set input parameters to ExecQueryAsync.
BSTR QueryLang = SysAllocString(L"WQL");
BSTR Query = SysAllocString(L"SELECT * FROM MyClass");

// Create IWbemObjectSink object and set pointer.
QuerySink *pSink = new QuerySink;

IWbemServices* pSvc = 0;

// Call ExecQueryAsync.
HRESULT hRes = pSvc->ExecQueryAsync(QueryLang, 
                                    Query, 
                                    0, 
                                    NULL, 
                                    pSink);

// Check for errors.
if (hRes)
{
    printf("ExecQueryAsync failed with = 0x%X\n", hRes);
    SysFreeString(QueryLang);
    SysFreeString(Query);
    delete pSink;    
    return ERROR;
}
```



> [!Note]  
> Der obige Code wird nicht ohne Fehler kompiliert, da die **QuerySink-Klasse** nicht definiert wurde. Weitere Informationen zu **QuerySink** finden Sie unter [**IWbemObjectSink**](iwbemobjectsink.md).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufrufen einer Methode](calling-a-method.md)
</dt> </dl>

 

 
