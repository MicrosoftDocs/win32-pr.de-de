---
description: 'Semisynchrone Aufrufe sind die empfohlenen Methoden zum Aufrufen von WMI-Methoden, wie z. b. IWbemServices:: ExecMethod und Provider-Methoden, wie z. b. die CHKDSK-Methode der Win32 \_ LogicalDisk-Klasse.'
ms.assetid: 3d5ddd77-19f7-42d0-b8ca-a0a11f6b3f0f
ms.tgt_platform: multiple
title: Erstellen eines semisynchronen Aufrufes mit C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c4546a7220d191b822e9f0f30a767e89e4dc26a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529615"
---
# <a name="making-a-semisynchronous-call-with-c"></a><span data-ttu-id="11e69-103">Erstellen eines semisynchronen Aufrufes mit C++</span><span class="sxs-lookup"><span data-stu-id="11e69-103">Making a Semisynchronous Call with C++</span></span>

<span data-ttu-id="11e69-104">Semisynchrone Aufrufe sind die empfohlenen Methoden zum Aufrufen von WMI-Methoden, wie z. b. [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) und Provider-Methoden, wie z. b. die [**chkdsk-Methode der Win32 \_ LogicalDisk-Klasse**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk).</span><span class="sxs-lookup"><span data-stu-id="11e69-104">Semisynchronous calls are the recommended means to call WMI methods, such as [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) and provider methods, such as the [**Chkdsk Method of the Win32\_LogicalDisk Class**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk).</span></span>

<span data-ttu-id="11e69-105">Ein Nachteil der synchronen Verarbeitung ist, dass der aufruferthread blockiert wird, bis der Aufruf abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="11e69-105">One disadvantage of synchronous processing is that the caller thread is blocked until the call completes.</span></span> <span data-ttu-id="11e69-106">Die Blockierung hin kann zu einer Verzögerung bei der Verarbeitungszeit führen.</span><span class="sxs-lookup"><span data-stu-id="11e69-106">The blockage can cause a delay in processing time.</span></span> <span data-ttu-id="11e69-107">Im Gegensatz dazu muss ein asynchroner-Befehl in einem Skript " [**Swap-Sink**](swbemsink.md) " implementieren.</span><span class="sxs-lookup"><span data-stu-id="11e69-107">In contrast, an asynchronous call must implement [**SWbemSink**](swbemsink.md) in script.</span></span> <span data-ttu-id="11e69-108">In C++ muss der asynchrone Code die [**iwbebobjectsink**](iwbemobjectsink.md) -Schnittstelle implementieren, mehrere Threads verwenden und den Informationsfluss zurück an den Aufrufer steuern.</span><span class="sxs-lookup"><span data-stu-id="11e69-108">In C++, asynchronous code must implement the [**IWbemObjectSink**](iwbemobjectsink.md) interface, use multiple threads, and control the flow of information back to the caller.</span></span> <span data-ttu-id="11e69-109">Große Resultsets aus Abfragen können z. b. sehr viel Zeit in Anspruch nehmen und erzwingen, dass der Aufrufer beträchtliche Systemressourcen für die Übermittlung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="11e69-109">Large result sets from queries, for example, can take a considerable amount of time to deliver and forces the caller to spend significant system resources to handle the delivery.</span></span>

<span data-ttu-id="11e69-110">Durch die semisynchrone Verarbeitung werden sowohl die Probleme beim Blockieren von Threads als auch bei der Übertragung durch Abfragen eines speziellen Status Objekts, das die [**iwbemcallresult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) -Schnittstelle implementiert</span><span class="sxs-lookup"><span data-stu-id="11e69-110">Semisynchronous processing solves both the thread blockage and uncontrolled delivery problems by polling a special status object that implements the [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) interface.</span></span> <span data-ttu-id="11e69-111">Mithilfe von **iwbemcallresult** können Sie die Geschwindigkeit und Effizienz von Abfragen, Enumerationen und Ereignis Benachrichtigungen verbessern.</span><span class="sxs-lookup"><span data-stu-id="11e69-111">Through **IWbemCallResult**, you can improve the speed and efficiency of queries, enumerations, and event notifications.</span></span>

<span data-ttu-id="11e69-112">Im folgenden Verfahren wird beschrieben, wie Sie einen semisynchronen-Befehl mit der [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Schnittstelle erstellen.</span><span class="sxs-lookup"><span data-stu-id="11e69-112">The following procedure describes how to make a semisynchronous call with the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface.</span></span>

<span data-ttu-id="11e69-113">**So führen Sie mit der IWbemServices-Schnittstelle einen semisynchronen Befehl aus**</span><span class="sxs-lookup"><span data-stu-id="11e69-113">**To make a semisynchronous call with the IWbemServices interface**</span></span>

1.  <span data-ttu-id="11e69-114">Führen Sie den-Befehl wie gewohnt aus, aber mit dem WBEM-Flag wird sofort das Flag im *IFlags* -Parameter **\_ \_ zurück \_ gegeben** .</span><span class="sxs-lookup"><span data-stu-id="11e69-114">Make your call as normal, but with the **WBEM\_FLAG\_RETURN\_IMMEDIATELY** flag set in the *IFlags* parameter.</span></span>

    <span data-ttu-id="11e69-115">Sie können das **WBEM \_ - \_ Flag \_ direkt** mit anderen Flags kombinieren, die für die jeweilige Methode gültig sind.</span><span class="sxs-lookup"><span data-stu-id="11e69-115">You can combine **WBEM\_FLAG\_RETURN\_IMMEDIATELY** with other flags that are valid for the specific method.</span></span> <span data-ttu-id="11e69-116">Verwenden Sie z. b. für alle Aufrufe, die Enumeratoren zurückgeben, das **WBEM-Flag für den \_ \_ Vorwärts \_ -Flag** .</span><span class="sxs-lookup"><span data-stu-id="11e69-116">For example, use the **WBEM\_FLAG\_FORWARD\_ONLY** flag for all calls that return enumerators.</span></span> <span data-ttu-id="11e69-117">Das Festlegen dieser Flags in Kombination spart Zeit und Speicherplatz und verbessert die Reaktionsfähigkeit.</span><span class="sxs-lookup"><span data-stu-id="11e69-117">Setting these flags in combination saves time and space, and improves responsiveness.</span></span>

2.  <span data-ttu-id="11e69-118">Abrufen der Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="11e69-118">Poll for your results.</span></span>

    <span data-ttu-id="11e69-119">Wenn Sie eine Methode aufrufen, die einen Enumerator zurückgibt, wie z. b. [**IWbemServices:: kreateclassenum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum) oder [**IWbemServices:: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery), können Sie die Enumeratoren mit der [**ienumwbemclassobject:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) -Methode oder der [**ienumwbemclassobject:: nextasync**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync) -Methode Abfragen.</span><span class="sxs-lookup"><span data-stu-id="11e69-119">If you call a method that returns an enumerator, such as [**IWbemServices::CreateClassEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum) or [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery), you can poll the enumerators with the [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) or [**IEnumWbemClassObject::NextAsync**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync) methods.</span></span> <span data-ttu-id="11e69-120">Der **ienumwbemclassobject:: nextasync** -Aufrufwert ist nicht blockierend und wird sofort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="11e69-120">The **IEnumWbemClassObject::NextAsync** call is nonblocking and returns immediately.</span></span> <span data-ttu-id="11e69-121">Im Hintergrund beginnt WMI mit dem übermitteln der angeforderten Anzahl von Objekten durch Aufrufen von [**iwbemubjectsink:: angeben**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate).</span><span class="sxs-lookup"><span data-stu-id="11e69-121">In the background, WMI begins to deliver the requested number of objects by calling [**IWbemObjectSink::Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate).</span></span> <span data-ttu-id="11e69-122">WMI hält dann an und wartet auf einen anderen **nextasync** -Aufruf.</span><span class="sxs-lookup"><span data-stu-id="11e69-122">WMI then stops and waits for another **NextAsync** call.</span></span>

    <span data-ttu-id="11e69-123">Wenn Sie eine Methode aufrufen, die keinen Enumerator zurückgibt (z. b. [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)), müssen Sie den Parameter *ppcallresult* auf einen gültigen Zeiger festlegen.</span><span class="sxs-lookup"><span data-stu-id="11e69-123">If you call a method that does not return an enumerator, such as [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), you must set the *ppCallResult* parameter to a valid pointer.</span></span> <span data-ttu-id="11e69-124">Verwenden Sie [**iwbemcallresult:: getcallstatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) für den zurückgegebenen Zeiger, um **WBEM \_ S \_ No \_ Error** abzurufen.</span><span class="sxs-lookup"><span data-stu-id="11e69-124">Use the [**IWbemCallResult::GetCallStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) on the returned pointer to retrieve **WBEM\_S\_NO\_ERROR**.</span></span>

3.  <span data-ttu-id="11e69-125">Beenden Sie den-Befehl.</span><span class="sxs-lookup"><span data-stu-id="11e69-125">Finish your call.</span></span>

    <span data-ttu-id="11e69-126">Für einen Aufruf, der einen Enumerator zurückgibt, ruft WMI [**iwbewbjectsink:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) auf, um den Abschluss des Vorgangs zu melden.</span><span class="sxs-lookup"><span data-stu-id="11e69-126">For a call that returns an enumerator, WMI calls [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) to report the completion of the operation.</span></span> <span data-ttu-id="11e69-127">Wenn Sie das gesamte Ergebnis nicht benötigen, geben Sie den Enumerator durch Aufrufen der [**ienumwbemclassobject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)::[**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode frei.</span><span class="sxs-lookup"><span data-stu-id="11e69-127">If you do not need the entire result, release the enumerator by calling the [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)::[**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method.</span></span> <span data-ttu-id="11e69-128">Das Aufrufen von **Release** führt dazu, dass WMI die Übermittlung aller verbleibenden Objekte abbricht.</span><span class="sxs-lookup"><span data-stu-id="11e69-128">Calling **Release** results in WMI canceling the delivery of all objects that remain.</span></span>

    <span data-ttu-id="11e69-129">Rufen Sie für einen Aufruf, der keinen Enumerator verwendet, das [**getcallstatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) -Objekt über den *plstatus* -Parameter der Methode ab.</span><span class="sxs-lookup"><span data-stu-id="11e69-129">For a call that does not use an enumerator, retrieve the [**GetCallStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) object through the *plStatus* parameter of your method.</span></span>

<span data-ttu-id="11e69-130">Das C++-Codebeispiel in diesem Thema erfordert, dass die folgenden \# include-Anweisungen ordnungsgemäß kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="11e69-130">The C++ code example in this topic requires the following \#include statements to compile correctly.</span></span>


```C++
#include <comdef.h>
#include <wbemidl.h>
```



<span data-ttu-id="11e69-131">Im folgenden Codebeispiel wird gezeigt, wie Sie einen semisynchronen aufzurufenden [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)-Befehl erstellen.</span><span class="sxs-lookup"><span data-stu-id="11e69-131">The following code example shows how to make a semisynchronous call to [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span></span>


```C++
void GetObjSemiSync(IWbemServices *pSvc)
{

    IWbemCallResult *pCallRes = 0;
    IWbemClassObject *pObj = 0;
    
    HRESULT hRes = pSvc->GetObject(_bstr_t(L"MyClass=\"AAA\""), 0,
        0, 0, &pCallRes
        );
        
    if (hRes || pCallRes == 0)
        return;
        
    while (true)
    {
        LONG lStatus = 0;
        HRESULT hRes = pCallRes->GetCallStatus(5000, &lStatus);
        if ( hRes == WBEM_S_NO_ERROR || hRes != WBEM_S_TIMEDOUT )
            break;

        // Do another task
    }

    hRes = pCallRes->GetResultObject(5000, &pObj);
    if (hRes)
    {
        pCallRes->Release();
        return;
    }

    pCallRes->Release();

    // Use the object.

    // ...

    // Release it.
    // ===========
        
    pObj->Release();    // Release objects not owned.            
  
}
```



## <a name="related-topics"></a><span data-ttu-id="11e69-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="11e69-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11e69-133">Aufrufen einer Methode</span><span class="sxs-lookup"><span data-stu-id="11e69-133">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 
