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
# <a name="making-an-asynchronous-call-with-c"></a><span data-ttu-id="2d9a7-103">Erstellen eines asynchronen Aufrufes mit C++</span><span class="sxs-lookup"><span data-stu-id="2d9a7-103">Making an Asynchronous Call with C++</span></span>

<span data-ttu-id="2d9a7-104">WMI-Anwendungen, die in C++ geschrieben wurden, können asynchrone Aufrufe durchführen, indem Sie viele der Methoden der COM-Schnittstelle [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) verwenden.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-104">WMI applications written in C++ can make asynchronous calls by using many of the methods of the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) COM interface.</span></span> <span data-ttu-id="2d9a7-105">Die empfohlene Vorgehensweise zum Aufrufen einer [*WMI-Methode*](gloss-w.md) oder einer [*Anbieter Methode*](gloss-p.md) ist jedoch die Verwendung von semisynchronen aufrufen, da semisynchrone Aufrufe sicherer als asynchrone Aufrufe sind.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-105">However, the recommended procedure for calling a [*WMI method*](gloss-w.md) or a [*provider method*](gloss-p.md) is by using semisynchronous calls because semisynchronous calls are more secure than asynchronous calls.</span></span> <span data-ttu-id="2d9a7-106">Weitere Informationen finden Sie unter [Erstellen eines semisynchronen Aufrufes mit C++](making-a-semisynchronous-call-with-c--.md) und [Festlegen der Sicherheit für einen asynchronen](setting-security-on-an-asynchronous-call.md)-Befehl.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-106">For more information, see [Making a Semisynchronous Call with C++](making-a-semisynchronous-call-with-c--.md) and [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="2d9a7-107">Im folgenden Verfahren wird beschrieben, wie Sie einen asynchronen-Befehl durchführen, indem Sie die-Senke in Ihrem Prozess verwenden.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-107">The following procedure describes how to make an asynchronous call by using the sink in your process.</span></span>

<span data-ttu-id="2d9a7-108">**So führen Sie einen asynchronen aufrufbefehl mithilfe von C++ aus**</span><span class="sxs-lookup"><span data-stu-id="2d9a7-108">**To make an asynchronous call using C++**</span></span>

1.  <span data-ttu-id="2d9a7-109">Implementieren Sie die [**iwbebobjectsink**](iwbemobjectsink.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-109">Implement the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span>

    <span data-ttu-id="2d9a7-110">Alle Anwendungen, die asynchrone Aufrufe ausführen, müssen [**iwbemjebjectsink**](iwbemobjectsink.md)implementieren.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-110">All applications that make asynchronous calls must implement [**IWbemObjectSink**](iwbemobjectsink.md).</span></span> <span data-ttu-id="2d9a7-111">Temporäre Ereignisconsumer implementieren ebenfalls " **iwbemubjectsink** ", um Benachrichtigungen über Ereignisse zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-111">Temporary event consumers also implement **IWbemObjectSink** to receive notification of events.</span></span>

2.  <span data-ttu-id="2d9a7-112">Melden Sie sich beim Ziel-WMI-Namespace an.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-112">Log on to the target WMI namespace.</span></span>

    <span data-ttu-id="2d9a7-113">Anwendungen müssen während der Initialisierungsphase immer die com-Funktion [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) aufruft.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-113">Applications always have to call the COM function [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) during the initialization phase.</span></span> <span data-ttu-id="2d9a7-114">Wenn dies nicht der Fall ist, bevor ein asynchroner Rückruf durchzuführen ist, gibt WMI die Anwendungs Senke frei, ohne dass der asynchrone-Befehl abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-114">If they do not do so before making an asynchronous call, WMI releases the application sink without completing the asynchronous call.</span></span> <span data-ttu-id="2d9a7-115">Weitere Informationen finden Sie unter [Initialisieren von com für eine WMI-Anwendung](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="2d9a7-115">For more information, see [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

3.  <span data-ttu-id="2d9a7-116">Legen Sie die Sicherheit für die Senke fest.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-116">Set the security for your sink.</span></span>

    <span data-ttu-id="2d9a7-117">Asynchrone Aufrufe erstellen eine Vielzahl von Sicherheitsproblemen, die möglicherweise behoben werden müssen, z. b., um den WMI-Zugriff auf Ihre Anwendung zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-117">Asynchronous calls create a variety of security issues that you may have to deal with, for example, allowing WMI access to your application.</span></span> <span data-ttu-id="2d9a7-118">Weitere Informationen finden Sie unter [Festlegen der Sicherheit für einen asynchronen](setting-security-on-an-asynchronous-call.md)-Befehl.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-118">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

4.  <span data-ttu-id="2d9a7-119">Führen Sie den asynchronen aufrufsbefehl aus.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-119">Make the asynchronous call.</span></span>

    <span data-ttu-id="2d9a7-120">Die-Methode gibt sofort mit dem Code für die **\_ \_ \_ Fehlermeldung "kein Fehler** " zurück.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-120">The method returns immediately with the **WBEM\_S\_NO\_ERROR** success code.</span></span> <span data-ttu-id="2d9a7-121">Die Anwendung kann mit anderen Aufgaben fortfahren, während darauf gewartet wird, dass der Vorgang beendet wird.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-121">The application can proceed with other tasks while waiting for the operation to complete.</span></span> <span data-ttu-id="2d9a7-122">WMI meldet an die Anwendung zurück, indem Methoden in der [**iwbemubjectsink**](iwbemobjectsink.md) -Implementierung der Anwendung aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-122">WMI reports back to the application by calling methods in the [**IWbemObjectSink**](iwbemobjectsink.md) implementation of your application.</span></span>

5.  <span data-ttu-id="2d9a7-123">Überprüfen Sie ggf. die Implementierung regelmäßig auf Updates.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-123">If necessary, check your implementation periodically for updates.</span></span>

    <span data-ttu-id="2d9a7-124">Anwendungen können eine Benachrichtigung über den zwischen Status erhalten, indem Sie den *lFlags* -Parameter im asynchronen WBEM-aufrufsflag- **\_ \_ Sende \_ Status** festlegen.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-124">Applications can receive notification of intermediate status by setting the *lFlags* parameter in the asynchronous call to **WBEM\_FLAG\_SEND\_STATUS**.</span></span> <span data-ttu-id="2d9a7-125">WMI meldet den Status Ihres Aufrufes, indem er den *lFlags* -Parameter von [**iwbemubjectsink**](iwbemobjectsink.md) auf den **Status des WBEM- \_ Status \_** festlegt.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-125">WMI reports the status of your call by setting the *lFlags* parameter of [**IWbemObjectSink**](iwbemobjectsink.md) to **WBEM\_STATUS\_PROGRESS**.</span></span>

6.  <span data-ttu-id="2d9a7-126">Falls erforderlich, können Sie den Aufruf abbrechen, bevor die Verarbeitung von WMI abgeschlossen ist, indem Sie die [**IWbemServices:: cancelcallasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-126">If necessary, you can cancel the call before WMI finishes processing by calling the [**IWbemServices::CancelCallAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) method.</span></span>

    <span data-ttu-id="2d9a7-127">Die [**cancelasynccall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) -Methode bricht die asynchrone Verarbeitung ab, indem Sie den Zeiger auf die [**IWbemObjectSink**](iwbemobjectsink.md) -Schnittstelle unmittelbar freigibt und sicherstellt, dass der Zeiger freigegeben wird, bevor **cancelasynccall** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-127">The [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) method cancels asynchronous processing by immediately releasing the pointer to the [**IWbemObjectSink**](iwbemobjectsink.md) interface and guarantees that the pointer is released before **CancelAsyncCall** returns.</span></span>

    <span data-ttu-id="2d9a7-128">Wenn Sie ein Wrapper Objekt verwenden, das die **iunsichere** -Schnittstelle zum Hosten von [**iwbewbjectsink**](iwbemobjectsink.md)implementiert, finden Sie möglicherweise einige zusätzliche Komplikationen.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-128">If you are using a wrapper object implementing the **IUnsecured** interface to host [**IWbemObjectSink**](iwbemobjectsink.md), you may find some additional complications.</span></span> <span data-ttu-id="2d9a7-129">Da die Anwendung denselben Zeiger an [**cancelasynccall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) übergeben muss, der in den ursprünglichen asynchronen-Befehl übergeben wurde, muss die Anwendung bis zum-Wrapper Objekt speichern, bis klar wird, dass kein Abbruch erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-129">Because the application must pass the same pointer to [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) that was passed in the original asynchronous call, the application must hold on to the wrapper object until it becomes clear that cancellation is not required.</span></span> <span data-ttu-id="2d9a7-130">Weitere Informationen finden Sie unter [Festlegen der Sicherheit für einen asynchronen](setting-security-on-an-asynchronous-call.md)-Befehl.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-130">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

7.  <span data-ttu-id="2d9a7-131">Wenn Sie fertig sind, bereinigen Sie die Zeiger, und fahren Sie die Anwendung herunter.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-131">When finished, clean up pointers and shut down the application.</span></span>

    <span data-ttu-id="2d9a7-132">WMI stellt den abschließenden Status-aufrufen über die [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) -Methode bereit.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-132">WMI provides the final status call through the [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) method.</span></span>

    > [!Note]  
    > <span data-ttu-id="2d9a7-133">Nachdem die endgültige Statusaktualisierung gesendet wurde, wird die Objekt Senke von WMI freigegeben, indem die **releasemethode** für die Klasse aufgerufen wird, die die [**iwbewbjectsink**](iwbemobjectsink.md) -Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-133">After sending the final status update, WMI releases the object sink by calling the **Release** method for the class that implements the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span> <span data-ttu-id="2d9a7-134">Im vorherigen Beispiel ist dies die **querysink:: Release** -Methode.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-134">In the previous example, this is the **QuerySink::Release** method.</span></span> <span data-ttu-id="2d9a7-135">Wenn Sie die Kontrolle über die Lebensdauer des Sink-Objekts haben möchten, können Sie die Senke mit einem anfänglichen Verweis Zähler von einem (1) implementieren.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-135">If you want to have control over the lifetime of the sink object, you can implement the sink with an initial reference count of one (1).</span></span>

     

    <span data-ttu-id="2d9a7-136">Wenn eine Client Anwendung die gleiche Senke-Schnittstelle in zwei unterschiedlichen asynchronen Aufrufen übergibt, garantiert WMI nicht die Reihenfolge des Rückrufs.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-136">If a client application passes the same sink interface in two different overlapping asynchronous calls, WMI does not guarantee the order of the callback.</span></span> <span data-ttu-id="2d9a7-137">Eine Client Anwendung, die überlappende asynchrone Aufrufe durchläuft, sollte entweder unterschiedliche Sink-Objekte übergeben oder die Aufrufe serialisieren.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-137">A client application making overlapping asynchronous calls should either pass different sink objects or serialize the calls.</span></span>

<span data-ttu-id="2d9a7-138">Im folgenden Beispiel sind die folgenden Referenz-und \# include-Anweisungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-138">The following example requires the following reference and \#include statements.</span></span>


```C++
#include <iostream>
using namespace std;
#pragma comment(lib, "wbemuuid.lib")
#include <wbemidl.h>
```



<span data-ttu-id="2d9a7-139">Im folgenden Beispiel wird beschrieben, wie eine asynchrone Abfrage mithilfe der [**ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) -Methode erstellt wird, aber keine Sicherheitseinstellungen erstellt oder das [**iwbemubjectsink**](iwbemobjectsink.md) -Objekt freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-139">The following example describes how to make an asynchronous query using the [**ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method, but does not create security settings or release the [**IWbemObjectSink**](iwbemobjectsink.md) object.</span></span> <span data-ttu-id="2d9a7-140">Weitere Informationen finden Sie unter [Festlegen der Sicherheit für einen asynchronen](setting-security-on-an-asynchronous-call.md)-Befehl.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-140">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>


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
> <span data-ttu-id="2d9a7-141">Der obige Code wird nicht ohne Fehler kompiliert, weil die **querysink** -Klasse nicht definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-141">The code above does not compile without error because the **QuerySink** class has not been defined.</span></span> <span data-ttu-id="2d9a7-142">Weitere Informationen zu **querysink** finden Sie unter [**iwbemubjectsink**](iwbemobjectsink.md).</span><span class="sxs-lookup"><span data-stu-id="2d9a7-142">For more information about **QuerySink**, see [**IWbemObjectSink**](iwbemobjectsink.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="2d9a7-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2d9a7-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d9a7-144">Aufrufen einer Methode</span><span class="sxs-lookup"><span data-stu-id="2d9a7-144">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 
