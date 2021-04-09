---
description: Eine asynchrone Abfrage, die etwas komplexer zu schreiben ist, ist die bevorzugte Art von Abfrage, wenn die System-oder Netzwerkleistung durch Abfragen einer großen Gruppe von Daten beeinträchtigt wird.
ms.assetid: b382610a-dac9-4d31-b756-aa84d16f0234
ms.tgt_platform: multiple
title: Aufrufen einer asynchronen Abfrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a0e297c6a1955d0006d888fc95f5e827f5cb75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868747"
---
# <a name="invoking-an-asynchronous-query"></a>Aufrufen einer asynchronen Abfrage

Eine asynchrone Abfrage, die etwas komplexer zu schreiben ist, ist die bevorzugte Art von Abfrage, wenn die System-oder Netzwerkleistung durch Abfragen einer großen Gruppe von Daten beeinträchtigt wird. In Skripts sind das Erstellen eines [**Austausch**](swbemsink.md) baren Objekts und der Unterroutinen zum Behandeln der Ereignisse, die die Senke empfangen könnte, die einzigen zusätzlichen Tasks, die über die grundlegende Abfrage hinausgehen.

> [!Note]  
> Da der Rückruf für die Senke möglicherweise nicht auf derselben Authentifizierungs Ebene wie der Client zurückgegeben wird, wird empfohlen, semisynchrone anstelle der asynchronen Kommunikation zu verwenden. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

 

Das folgende abgekürzte Skript fragt alle Datendateien auf dem lokalen Computer ab. Diese Abfrage kann übermäßig viel Zeit in Anspruch nehmen, wenn Sie für alle Computer in einem Netzwerk ausgeführt wird. Ein " [**slibemsink**](swbemsink.md) "-Objekt ist eingerichtet, und das einzige Ereignis, das behandelt wird, ist das onabgeschlossene-Ereignis.


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



Ausführliche Informationen zum Erstellen von asynchronen Methoden aufrufen in Skripts finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

In C++-Anwendungen erzeugt eine asynchrone Abfrage einen separaten Prozess zum Empfangen von Abfrage Daten. Eine asynchrone Abfrage ist komplexer als eine synchrone Abfrage, da Sie eine Multithread-Anwendung codieren müssen. Bei einer asynchronen Abfrage wird jedoch nicht der Hauptthread der Anwendung monopolisiert.

Im folgenden Verfahren wird beschrieben, wie eine asynchrone Abfrage in C++ durchgeführt wird.

**So führen Sie eine asynchrone Abfrage in C++ aus**

1.  Implementieren Sie ein **iwbemsink** -Objekt.

    Ein **iwbemsink** -Objekt empfängt Informationen zu einem asynchronen Vorgang.

2.  Beschreiben Sie Ihre Abfrage in einem [**callbemservices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)-Befehl.

    WMI verschiebt den Prozess, der den CIM abfragt, sofort in einen anderen Thread und gibt den Thread frei, der die Abfrage für eine andere Aufgabe ausgeführt hat.

3.  Warten Sie, bis WMI die [**iwbemubjectsink::**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) Expression-Methode aufruft.

    Wenn der Vorgang abgeschlossen ist, [**zeigen**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) WMI-Aufrufe an, dass die Abfrage abgeschlossen ist. WMI gibt auch Ergebnisse der Abfrage an die Senke als Zeiger auf einen [**ienumwbemclassobject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) -Schnittstellen Zeiger zurück. Verwenden Sie wie bei einer synchronen Abfrage den-Zeiger, um auf die Objekte zuzugreifen, die das Ergebnis der Abfrage bilden.

Das folgende Codebeispiel wird nicht ohne Fehler kompiliert, weil die Klasse "querysink" nicht definiert wurde. Die Definition der querysink-Klasse finden Sie unter [**iwbemubjectsink**](iwbemobjectsink.md). Für das Codebeispiel sind auch die folgenden Referenz-und \# include-Anweisungen erforderlich.


```C++
#include <iostream>
using namespace std;
#include <wbemidl.h>
```



Im folgenden Codebeispiel wird gezeigt, wie Sie einen asynchronen-Befehl zum Ausgeben einer Abfrage ausführen.


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



Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

 

 



