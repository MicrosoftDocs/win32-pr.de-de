---
description: WMI-Anwendungen, die in C++ geschrieben wurden, können asynchrone Aufrufe durchführen, indem Sie viele der Methoden der COM-Schnittstelle IWbemServices verwenden.
ms.assetid: 5179969f-bc7d-4408-84ef-7b003950a59f
ms.tgt_platform: multiple
title: Erstellen eines asynchronen Aufrufes mit C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f093aef4b1a1b4dbede53333e77d737f8efd69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351567"
---
# <a name="making-an-asynchronous-call-with-c"></a>Erstellen eines asynchronen Aufrufes mit C++

WMI-Anwendungen, die in C++ geschrieben wurden, können asynchrone Aufrufe durchführen, indem Sie viele der Methoden der COM-Schnittstelle [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) verwenden. Die empfohlene Vorgehensweise zum Aufrufen einer [*WMI-Methode*](gloss-w.md) oder einer [*Anbieter Methode*](gloss-p.md) ist jedoch die Verwendung von semisynchronen aufrufen, da semisynchrone Aufrufe sicherer als asynchrone Aufrufe sind. Weitere Informationen finden Sie unter [Erstellen eines semisynchronen Aufrufes mit C++](making-a-semisynchronous-call-with-c--.md) und [Festlegen der Sicherheit für einen asynchronen](setting-security-on-an-asynchronous-call.md)-Befehl.

Im folgenden Verfahren wird beschrieben, wie Sie einen asynchronen-Befehl durchführen, indem Sie die-Senke in Ihrem Prozess verwenden.

**So führen Sie einen asynchronen aufrufbefehl mithilfe von C++ aus**

1.  Implementieren Sie die [**iwbebobjectsink**](iwbemobjectsink.md) -Schnittstelle.

    Alle Anwendungen, die asynchrone Aufrufe ausführen, müssen [**iwbemjebjectsink**](iwbemobjectsink.md)implementieren. Temporäre Ereignisconsumer implementieren ebenfalls " **iwbemubjectsink** ", um Benachrichtigungen über Ereignisse zu empfangen.

2.  Melden Sie sich beim Ziel-WMI-Namespace an.

    Anwendungen müssen während der Initialisierungsphase immer die com-Funktion [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) aufruft. Wenn dies nicht der Fall ist, bevor ein asynchroner Rückruf durchzuführen ist, gibt WMI die Anwendungs Senke frei, ohne dass der asynchrone-Befehl abgeschlossen ist. Weitere Informationen finden Sie unter [Initialisieren von com für eine WMI-Anwendung](initializing-com-for-a-wmi-application.md).

3.  Legen Sie die Sicherheit für die Senke fest.

    Asynchrone Aufrufe erstellen eine Vielzahl von Sicherheitsproblemen, die möglicherweise behoben werden müssen, z. b., um den WMI-Zugriff auf Ihre Anwendung zuzulassen. Weitere Informationen finden Sie unter [Festlegen der Sicherheit für einen asynchronen](setting-security-on-an-asynchronous-call.md)-Befehl.

4.  Führen Sie den asynchronen aufrufsbefehl aus.

    Die-Methode gibt sofort mit dem Code für die **\_ \_ \_ Fehlermeldung "kein Fehler** " zurück. Die Anwendung kann mit anderen Aufgaben fortfahren, während darauf gewartet wird, dass der Vorgang beendet wird. WMI meldet an die Anwendung zurück, indem Methoden in der [**iwbemubjectsink**](iwbemobjectsink.md) -Implementierung der Anwendung aufgerufen werden.

5.  Überprüfen Sie ggf. die Implementierung regelmäßig auf Updates.

    Anwendungen können eine Benachrichtigung über den zwischen Status erhalten, indem Sie den *lFlags* -Parameter im asynchronen WBEM-aufrufsflag- **\_ \_ Sende \_ Status** festlegen. WMI meldet den Status Ihres Aufrufes, indem er den *lFlags* -Parameter von [**iwbemubjectsink**](iwbemobjectsink.md) auf den **Status des WBEM- \_ Status \_** festlegt.

6.  Falls erforderlich, können Sie den Aufruf abbrechen, bevor die Verarbeitung von WMI abgeschlossen ist, indem Sie die [**IWbemServices:: cancelcallasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) -Methode aufrufen.

    Die [**cancelasynccall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) -Methode bricht die asynchrone Verarbeitung ab, indem Sie den Zeiger auf die [**IWbemObjectSink**](iwbemobjectsink.md) -Schnittstelle unmittelbar freigibt und sicherstellt, dass der Zeiger freigegeben wird, bevor **cancelasynccall** zurückgegeben wird.

    Wenn Sie ein Wrapper Objekt verwenden, das die **iunsichere** -Schnittstelle zum Hosten von [**iwbewbjectsink**](iwbemobjectsink.md)implementiert, finden Sie möglicherweise einige zusätzliche Komplikationen. Da die Anwendung denselben Zeiger an [**cancelasynccall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) übergeben muss, der in den ursprünglichen asynchronen-Befehl übergeben wurde, muss die Anwendung bis zum-Wrapper Objekt speichern, bis klar wird, dass kein Abbruch erforderlich ist. Weitere Informationen finden Sie unter [Festlegen der Sicherheit für einen asynchronen](setting-security-on-an-asynchronous-call.md)-Befehl.

7.  Wenn Sie fertig sind, bereinigen Sie die Zeiger, und fahren Sie die Anwendung herunter.

    WMI stellt den abschließenden Status-aufrufen über die [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) -Methode bereit.

    > [!Note]  
    > Nachdem die endgültige Statusaktualisierung gesendet wurde, wird die Objekt Senke von WMI freigegeben, indem die **releasemethode** für die Klasse aufgerufen wird, die die [**iwbewbjectsink**](iwbemobjectsink.md) -Schnittstelle implementiert. Im vorherigen Beispiel ist dies die **querysink:: Release** -Methode. Wenn Sie die Kontrolle über die Lebensdauer des Sink-Objekts haben möchten, können Sie die Senke mit einem anfänglichen Verweis Zähler von einem (1) implementieren.

     

    Wenn eine Client Anwendung die gleiche Senke-Schnittstelle in zwei unterschiedlichen asynchronen Aufrufen übergibt, garantiert WMI nicht die Reihenfolge des Rückrufs. Eine Client Anwendung, die überlappende asynchrone Aufrufe durchläuft, sollte entweder unterschiedliche Sink-Objekte übergeben oder die Aufrufe serialisieren.

Im folgenden Beispiel sind die folgenden Referenz-und \# include-Anweisungen erforderlich.


```C++
#include <iostream>
using namespace std;
#pragma comment(lib, "wbemuuid.lib")
#include <wbemidl.h>
```



Im folgenden Beispiel wird beschrieben, wie eine asynchrone Abfrage mithilfe der [**ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) -Methode erstellt wird, aber keine Sicherheitseinstellungen erstellt oder das [**iwbemubjectsink**](iwbemobjectsink.md) -Objekt freigegeben wird. Weitere Informationen finden Sie unter [Festlegen der Sicherheit für einen asynchronen](setting-security-on-an-asynchronous-call.md)-Befehl.


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
> Der obige Code wird nicht ohne Fehler kompiliert, weil die **querysink** -Klasse nicht definiert wurde. Weitere Informationen zu **querysink** finden Sie unter [**iwbemubjectsink**](iwbemobjectsink.md).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufrufen einer Methode](calling-a-method.md)
</dt> </dl>

 

 
