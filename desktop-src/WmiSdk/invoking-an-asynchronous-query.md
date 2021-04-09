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
# <a name="invoking-an-asynchronous-query"></a><span data-ttu-id="9e409-103">Aufrufen einer asynchronen Abfrage</span><span class="sxs-lookup"><span data-stu-id="9e409-103">Invoking an Asynchronous Query</span></span>

<span data-ttu-id="9e409-104">Eine asynchrone Abfrage, die etwas komplexer zu schreiben ist, ist die bevorzugte Art von Abfrage, wenn die System-oder Netzwerkleistung durch Abfragen einer großen Gruppe von Daten beeinträchtigt wird.</span><span class="sxs-lookup"><span data-stu-id="9e409-104">An asynchronous query, while somewhat more complex to write, is the preferred type of query when system or network performance will be affected by querying a large group of data.</span></span> <span data-ttu-id="9e409-105">In Skripts sind das Erstellen eines [**Austausch**](swbemsink.md) baren Objekts und der Unterroutinen zum Behandeln der Ereignisse, die die Senke empfangen könnte, die einzigen zusätzlichen Tasks, die über die grundlegende Abfrage hinausgehen.</span><span class="sxs-lookup"><span data-stu-id="9e409-105">In script, creating an [**SWbemSink**](swbemsink.md) object and subroutines to handle the events that the sink could receive are the only additional tasks beyond the basic query.</span></span>

> [!Note]  
> <span data-ttu-id="9e409-106">Da der Rückruf für die Senke möglicherweise nicht auf derselben Authentifizierungs Ebene wie der Client zurückgegeben wird, wird empfohlen, semisynchrone anstelle der asynchronen Kommunikation zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="9e409-106">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="9e409-107">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="9e409-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="9e409-108">Das folgende abgekürzte Skript fragt alle Datendateien auf dem lokalen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="9e409-108">The following abbreviated script queries for all of the data files on the local machine.</span></span> <span data-ttu-id="9e409-109">Diese Abfrage kann übermäßig viel Zeit in Anspruch nehmen, wenn Sie für alle Computer in einem Netzwerk ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9e409-109">This query could take an excessive amount of time if it were executed for all of the machines on a network.</span></span> <span data-ttu-id="9e409-110">Ein " [**slibemsink**](swbemsink.md) "-Objekt ist eingerichtet, und das einzige Ereignis, das behandelt wird, ist das onabgeschlossene-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="9e409-110">An [**SWbemSink**](swbemsink.md) object is set up and the only event that is handled is the OnCompleted event.</span></span>


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



<span data-ttu-id="9e409-111">Ausführliche Informationen zum Erstellen von asynchronen Methoden aufrufen in Skripts finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="9e409-111">For detailed information about constructing asynchronous method calls in script, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="9e409-112">In C++-Anwendungen erzeugt eine asynchrone Abfrage einen separaten Prozess zum Empfangen von Abfrage Daten.</span><span class="sxs-lookup"><span data-stu-id="9e409-112">In C++ applications, an asynchronous query spawns a separate process to receive query data.</span></span> <span data-ttu-id="9e409-113">Eine asynchrone Abfrage ist komplexer als eine synchrone Abfrage, da Sie eine Multithread-Anwendung codieren müssen.</span><span class="sxs-lookup"><span data-stu-id="9e409-113">An asynchronous query is more complex than a synchronous query, as you must code a multithreaded application.</span></span> <span data-ttu-id="9e409-114">Bei einer asynchronen Abfrage wird jedoch nicht der Hauptthread der Anwendung monopolisiert.</span><span class="sxs-lookup"><span data-stu-id="9e409-114">However, an asynchronous query does not monopolize the main thread of your application.</span></span>

<span data-ttu-id="9e409-115">Im folgenden Verfahren wird beschrieben, wie eine asynchrone Abfrage in C++ durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9e409-115">The following procedure describes how to perform an asynchronous query in C++.</span></span>

<span data-ttu-id="9e409-116">**So führen Sie eine asynchrone Abfrage in C++ aus**</span><span class="sxs-lookup"><span data-stu-id="9e409-116">**To perform an asynchronous query in C++**</span></span>

1.  <span data-ttu-id="9e409-117">Implementieren Sie ein **iwbemsink** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="9e409-117">Implement an **IWbemSink** object.</span></span>

    <span data-ttu-id="9e409-118">Ein **iwbemsink** -Objekt empfängt Informationen zu einem asynchronen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="9e409-118">An **IWbemSink** object receives information about an asynchronous operation.</span></span>

2.  <span data-ttu-id="9e409-119">Beschreiben Sie Ihre Abfrage in einem [**callbemservices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)-Befehl.</span><span class="sxs-lookup"><span data-stu-id="9e409-119">Describe your query in a call to [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync).</span></span>

    <span data-ttu-id="9e409-120">WMI verschiebt den Prozess, der den CIM abfragt, sofort in einen anderen Thread und gibt den Thread frei, der die Abfrage für eine andere Aufgabe ausgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="9e409-120">WMI immediately moves the process that queries the CIM to another thread and frees up the thread that executed the query for another task.</span></span>

3.  <span data-ttu-id="9e409-121">Warten Sie, bis WMI die [**iwbemubjectsink::**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) Expression-Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="9e409-121">Wait for WMI to call the [**IWbemObjectSink::Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) method.</span></span>

    <span data-ttu-id="9e409-122">Wenn der Vorgang abgeschlossen ist, [**zeigen**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) WMI-Aufrufe an, dass die Abfrage abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="9e409-122">When finished, WMI calls [**Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) to signal your application that the query is complete.</span></span> <span data-ttu-id="9e409-123">WMI gibt auch Ergebnisse der Abfrage an die Senke als Zeiger auf einen [**ienumwbemclassobject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) -Schnittstellen Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="9e409-123">WMI also returns results of the query to the sink as a pointer to an [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) interface pointer.</span></span> <span data-ttu-id="9e409-124">Verwenden Sie wie bei einer synchronen Abfrage den-Zeiger, um auf die Objekte zuzugreifen, die das Ergebnis der Abfrage bilden.</span><span class="sxs-lookup"><span data-stu-id="9e409-124">As with a synchronous query, use the pointer to access the objects that make up the result of your query.</span></span>

<span data-ttu-id="9e409-125">Das folgende Codebeispiel wird nicht ohne Fehler kompiliert, weil die Klasse "querysink" nicht definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="9e409-125">The following code example does not compile without an error because the class QuerySink has not been defined.</span></span> <span data-ttu-id="9e409-126">Die Definition der querysink-Klasse finden Sie unter [**iwbemubjectsink**](iwbemobjectsink.md).</span><span class="sxs-lookup"><span data-stu-id="9e409-126">For the definition of the QuerySink class, see [**IWbemObjectSink**](iwbemobjectsink.md).</span></span> <span data-ttu-id="9e409-127">Für das Codebeispiel sind auch die folgenden Referenz-und \# include-Anweisungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9e409-127">The code example also requires the following reference and \#include statements.</span></span>


```C++
#include <iostream>
using namespace std;
#include <wbemidl.h>
```



<span data-ttu-id="9e409-128">Im folgenden Codebeispiel wird gezeigt, wie Sie einen asynchronen-Befehl zum Ausgeben einer Abfrage ausführen.</span><span class="sxs-lookup"><span data-stu-id="9e409-128">The following code example shows how to make an asynchronous call to issue a query.</span></span>


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



<span data-ttu-id="9e409-129">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="9e409-129">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

 



