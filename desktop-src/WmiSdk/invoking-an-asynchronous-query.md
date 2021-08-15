---
description: Eine asynchrone Abfrage ist zwar etwas komplexer zu schreiben, ist jedoch der bevorzugte Abfragetyp, wenn die System- oder Netzwerkleistung durch Abfragen einer großen Datengruppe beeinträchtigt wird.
ms.assetid: b382610a-dac9-4d31-b756-aa84d16f0234
ms.tgt_platform: multiple
title: Aufrufen einer asynchronen Abfrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52ae188e3826562b1de68357db34dca6cea60a40e4be07c16946b13ed3eb3007
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993070"
---
# <a name="invoking-an-asynchronous-query"></a>Aufrufen einer asynchronen Abfrage

Eine asynchrone Abfrage ist zwar etwas komplexer zu schreiben, ist jedoch der bevorzugte Abfragetyp, wenn die System- oder Netzwerkleistung durch Abfragen einer großen Datengruppe beeinträchtigt wird. Im Skript sind das Erstellen eines [**SWbemSink-Objekts**](swbemsink.md) und von Unterroutinen zur Verarbeitung der Ereignisse, die die Senke empfangen könnte, die einzigen zusätzlichen Aufgaben, die über die grundlegende Abfrage hinausgehen.

> [!Note]  
> Da der Rückruf an die Senke möglicherweise nicht auf derselben Authentifizierungsebene zurückgegeben wird, wie der Client erfordert, wird empfohlen, anstelle der asynchronen Kommunikation semisynchrone zu verwenden. Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

 

Das folgende abgekürzte Skript fragt alle Datendateien auf dem lokalen Computer ab. Diese Abfrage kann übermäßig lange dauern, wenn sie für alle Computer in einem Netzwerk ausgeführt wird. Ein [**SWbemSink-Objekt**](swbemsink.md) wird eingerichtet, und das einzige Ereignis, das behandelt wird, ist das OnCompleted-Ereignis.


```VB
Sub SINK_OnCompleted(iHResult, objErrorObject, objAsyncContext)
    WScript.Echo "Asynchronous operation is done."
End Sub

Set service = GetObject("winmgmts:")
Set sink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
service.ExecQueryAsync sink, "SELECT * FROM Win32_DataFile"
WScript.Echo "Waiting for instances."
sink.Cancel()
set sink= Nothing
```



Ausführliche Informationen zum Erstellen von asynchronen Methodenaufrufen im Skript finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

In C++-Anwendungen erstellt eine asynchrone Abfrage einen separaten Prozess zum Empfangen von Abfragedaten. Eine asynchrone Abfrage ist komplexer als eine synchrone Abfrage, da Sie eine Multithreadanwendung codiert werden müssen. Eine asynchrone Abfrage führt jedoch nicht zu einer Vergrößerung des Hauptthreads Ihrer Anwendung.

Im folgenden Verfahren wird beschrieben, wie Eine asynchrone Abfrage in C++ ausgeführt wird.

**So führen Sie eine asynchrone Abfrage in C++ aus**

1.  Implementieren Sie **ein IWbemSink-Objekt.**

    Ein **IWbemSink-Objekt** empfängt Informationen zu einem asynchronen Vorgang.

2.  Beschreiben Sie Ihre Abfrage in einem Aufruf von [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync).

    WMI verschiebt den Prozess, der cim abfragt, sofort in einen anderen Thread und gibt den Thread frei, der die Abfrage für eine andere Aufgabe ausgeführt hat.

3.  Warten Sie, bis WMI die [**IWbemObjectSink::Indicate-Methode**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) aufruft.

    Wenn Sie fertig sind, ruft WMI [**Indicate auf,**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) um Ihrer Anwendung zu signalisieren, dass die Abfrage abgeschlossen ist. WMI gibt auch Ergebnisse der Abfrage als Zeiger auf einen [**IEnumWbemClassObject-Schnittstellenzeiger**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) an die Senke zurück. Verwenden Sie wie bei einer synchronen Abfrage den -Zeiger, um auf die Objekte zu zugreifen, aus denen das Ergebnis der Abfrage resultiert.

Das folgende Codebeispiel wird nicht ohne Fehler kompiliert, da die QuerySink-Klasse nicht definiert wurde. Die Definition der QuerySink-Klasse finden Sie unter [**IWbemObjectSink**](iwbemobjectsink.md). Das Codebeispiel erfordert auch den folgenden Verweis und \# include-Anweisungen.


```C++
#include <iostream>
using namespace std;
#include <wbemidl.h>
```



Im folgenden Codebeispiel wird veranschaulicht, wie sie einen asynchronen Aufruf zum Ausführen einer Abfrage ausführen.


```C++
void ExecQuery(IWbemServices *pSvc)
{
    // Create a new sink object.
    QuerySink *pSink = new QuerySink;

    // Initialize the query and query language.
    BSTR strQuery = SysAllocString(L"SELECT * FROM ClassName");
    BSTR strQueryLang = SysAllocString(L"WQL");
    
    // Issue the query.
    HRESULT hRes = pSvc->ExecQueryAsync(strQueryLang, strQuery, 0,
        NULL, pSink);

    // Clean up.
    SysFreeString(strQuery);
    SysFreeString(strQueryLang);
    
    if (hRes)
    {
        printf("ExecQueryAsync failed with = 0x%X\n", hRes);
        return;
    }
    
    printf("Completed.\n");
}
```



Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

 

 



