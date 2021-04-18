---
description: Die iwbeporbjectsink-Schnittstelle erstellt eine Sink-Schnittstelle, die alle Arten von Benachrichtigungen innerhalb des WMI-Programmiermodells empfangen kann.
ms.assetid: 987aea1d-912a-4691-987f-181c1ef1a8a9
ms.tgt_platform: multiple
title: Iwbemubjectsink-Schnittstelle (wbemcli. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemObjectSink
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: 980865605eadfd5e4cb61a511317dec7838b8e47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368237"
---
# <a name="iwbemobjectsink-interface"></a><span data-ttu-id="99ee2-103">Iwbemubjectsink-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="99ee2-103">IWbemObjectSink interface</span></span>

<span data-ttu-id="99ee2-104">Die **iwbeporbjectsink** -Schnittstelle erstellt eine Sink-Schnittstelle, die alle Arten von Benachrichtigungen innerhalb des WMI-Programmiermodells empfangen kann.</span><span class="sxs-lookup"><span data-stu-id="99ee2-104">The **IWbemObjectSink** interface creates a sink interface that can receive all types of notifications within the WMI programming model.</span></span> <span data-ttu-id="99ee2-105">Clients müssen diese Schnittstelle implementieren, um sowohl die Ergebnisse der [asynchronen Methoden](making-an-asynchronous-call-with-c--.md) von [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)als auch bestimmte Arten von Ereignis Benachrichtigungen zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="99ee2-105">Clients must implement this interface to receive both the results of the [asynchronous methods](making-an-asynchronous-call-with-c--.md) of [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), and specific types of event notifications.</span></span> <span data-ttu-id="99ee2-106">Anbieter verwenden, implementieren diese Schnittstelle jedoch nicht, um der WMI Ereignisse und Objekte bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="99ee2-106">Providers use, but do not implement this interface to provide events and objects to WMI.</span></span>

<span data-ttu-id="99ee2-107">In der Regel wird von Anbietern eine von WMI bereitgestellte Implementierung aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="99ee2-107">Typically, providers call an implementation provided to them by WMI.</span></span> <span data-ttu-id="99ee2-108">In diesen Fällen [**geben**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) Sie an, um-Objekte für den WMI-Dienst bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="99ee2-108">In these cases, call [**Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) to provide objects to the WMI service.</span></span> <span data-ttu-id="99ee2-109">Anschließend wird [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) aufgerufen, um das Ende der Benachrichtigungs Sequenz anzugeben.</span><span class="sxs-lookup"><span data-stu-id="99ee2-109">After that, call [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) to indicate the end of the notification sequence.</span></span> <span data-ttu-id="99ee2-110">Sie können auch **SetStatus** aufrufen, um Fehler anzugeben, wenn die Senke keine Objekte enthält.</span><span class="sxs-lookup"><span data-stu-id="99ee2-110">You can also call **SetStatus** to indicate errors when the sink does not have any objects.</span></span>

<span data-ttu-id="99ee2-111">Beim Programmieren von asynchronen WMI-Clients stellt der Benutzer die-Implementierung bereit.</span><span class="sxs-lookup"><span data-stu-id="99ee2-111">When programming asynchronous clients of WMI, the user provides the implementation.</span></span> <span data-ttu-id="99ee2-112">WMI Ruft die Methoden zum Übermitteln von Objekten auf und legt den Status des Ergebnisses fest.</span><span class="sxs-lookup"><span data-stu-id="99ee2-112">WMI calls the methods to deliver objects and set the status of the result.</span></span>

> [!Note]  
> <span data-ttu-id="99ee2-113">Wenn eine Client Anwendung die gleiche Senke-Schnittstelle in zwei unterschiedlichen asynchronen Aufrufen übergibt, garantiert WMI nicht die Reihenfolge des Rückrufs.</span><span class="sxs-lookup"><span data-stu-id="99ee2-113">If a client application passes the same sink interface in two different overlapping asynchronous calls, WMI does not guarantee the order of the callback.</span></span> <span data-ttu-id="99ee2-114">Client Anwendungen, die überlappende asynchrone Aufrufe durchführen, sollten entweder unterschiedliche Sink-Objekte übergeben oder Ihre Aufrufe serialisieren.</span><span class="sxs-lookup"><span data-stu-id="99ee2-114">Client applications that make overlapping asynchronous calls should either pass different sink objects, or serialize their calls.</span></span>

 

> [!Note]  
> <span data-ttu-id="99ee2-115">Da der Rückruf für die Senke möglicherweise nicht auf derselben Authentifizierungs Ebene wie der Client zurückgegeben wird, empfiehlt es sich, anstelle der asynchronen Kommunikation semisynchrone anstelle der asynchronen Kommunikation zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="99ee2-115">Because the call-back to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="99ee2-116">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="99ee2-116">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

## <a name="members"></a><span data-ttu-id="99ee2-117">Member</span><span class="sxs-lookup"><span data-stu-id="99ee2-117">Members</span></span>

<span data-ttu-id="99ee2-118">Die **iwbeporbjectsink** -Schnittstelle verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="99ee2-118">The **IWbemObjectSink** interface has these types of members:</span></span>

-   [<span data-ttu-id="99ee2-119">Methoden</span><span class="sxs-lookup"><span data-stu-id="99ee2-119">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="99ee2-120">Methoden</span><span class="sxs-lookup"><span data-stu-id="99ee2-120">Methods</span></span>

<span data-ttu-id="99ee2-121">Die **iwbemubjectsink** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="99ee2-121">The **IWbemObjectSink** interface has these methods.</span></span>



| <span data-ttu-id="99ee2-122">Methode</span><span class="sxs-lookup"><span data-stu-id="99ee2-122">Method</span></span>                                         | <span data-ttu-id="99ee2-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="99ee2-123">Description</span></span>                                                                                                             |
|:-----------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="99ee2-124">**Aufgezeigt**</span><span class="sxs-lookup"><span data-stu-id="99ee2-124">**Indicate**</span></span>](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate)   | <span data-ttu-id="99ee2-125">Empfängt Benachrichtigungsobjekte.</span><span class="sxs-lookup"><span data-stu-id="99ee2-125">Receives notification objects.</span></span><br/>                                                                               |
| [<span data-ttu-id="99ee2-126">**SetStatus**</span><span class="sxs-lookup"><span data-stu-id="99ee2-126">**SetStatus**</span></span>](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) | <span data-ttu-id="99ee2-127">Wird von Quellen aufgerufen, um das Ende einer Benachrichtigungs Sequenz anzugeben, oder, um andere Statuscodes an die Senke zu senden.</span><span class="sxs-lookup"><span data-stu-id="99ee2-127">Called by sources to indicate the end of a notification sequence, or to send other status codes to the sink.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="99ee2-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="99ee2-128">Remarks</span></span>

<span data-ttu-id="99ee2-129">Wenn Sie eine Ereignis-Abonnement-Senke (**iwbewbjectsink** oder [**iwbemeventsink**](iwbemeventsink.md)) implementieren, sollten Sie in der Methode " [**angeben**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) " oder " [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) " für das senkentabbild keine WMI aufrufen.</span><span class="sxs-lookup"><span data-stu-id="99ee2-129">When implementing an event subscription sink (**IWbemObjectSink** or [**IWbemEventSink**](iwbemeventsink.md)), do not call into WMI from within the [**Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) or [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) methods on the sink object.</span></span> <span data-ttu-id="99ee2-130">Beispiels [**Weise kann das Aufrufen von**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) [**IWbemServices:: cancelasynccall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) zum Abbrechen der Senke aus einer Implementierung von den WMI-Zustand beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="99ee2-130">For example, calling [**IWbemServices::CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) to cancel the sink from within an implementation of [**Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) can interfere with the WMI state.</span></span> <span data-ttu-id="99ee2-131">Um ein Ereignis Abonnement abzubrechen, legen Sie ein Flag fest, und rufen Sie **IWbemServices:: cancelasynccall** von einem anderen Thread oder Objekt auf.</span><span class="sxs-lookup"><span data-stu-id="99ee2-131">To cancel an event subscription, set a flag and call **IWbemServices::CancelAsyncCall** from another thread or object.</span></span> <span data-ttu-id="99ee2-132">Bei Implementierungen, die sich nicht auf eine Ereignis Senke beziehen, wie z. b. Object-, enum-und Abfrage-Abruf Werte, können Sie einen Rückruf in WMI durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="99ee2-132">For implementations that are not related to an event sink, such as object, enum, and query retrievals, you can call back into WMI.</span></span>

<span data-ttu-id="99ee2-133">Sink-Implementierungen sollten die Ereignis Benachrichtigung innerhalb von 100 MS verarbeiten, weil der WMI-Thread, der die Ereignis Benachrichtigung übermittelt, erst dann andere Aufgaben ausführen kann, wenn die Verarbeitung des Sink-Objekts abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="99ee2-133">Sink implementations should process the event notification within 100 MSEC because the WMI thread that delivers the event notification cannot do other work until the sink object has completed processing.</span></span> <span data-ttu-id="99ee2-134">Wenn für die Benachrichtigung eine große Menge an Verarbeitung erforderlich ist, kann die Senke eine interne Warteschlange für einen anderen Thread verwenden, um die Verarbeitung zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="99ee2-134">If the notification requires a large amount of processing, the sink can use an internal queue for another thread to handle the processing.</span></span>

## <a name="examples"></a><span data-ttu-id="99ee2-135">Beispiele</span><span class="sxs-lookup"><span data-stu-id="99ee2-135">Examples</span></span>

<span data-ttu-id="99ee2-136">Das folgende Codebeispiel ist eine einfache Implementierung einer Objekt Senke.</span><span class="sxs-lookup"><span data-stu-id="99ee2-136">The following code example is a simple implementation of an object sink.</span></span> <span data-ttu-id="99ee2-137">Dieses Beispiel kann mit [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) oder [**IWbemServices:: | ateinstanceenumasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) verwendet werden, um die zurückgegebenen Instanzen zu empfangen:</span><span class="sxs-lookup"><span data-stu-id="99ee2-137">This sample can be used with [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) or [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) to receive the returned instances:</span></span>


```C++
#include <iostream>
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")

class QuerySink : public IWbemObjectSink
{
    LONG m_lRef;
    bool bDone; 

public:
    QuerySink() { m_lRef = 0; }
   ~QuerySink() { bDone = TRUE; }

    virtual ULONG STDMETHODCALLTYPE AddRef();
    virtual ULONG STDMETHODCALLTYPE Release();        
    virtual HRESULT STDMETHODCALLTYPE 
        QueryInterface(REFIID riid, void** ppv);

    virtual HRESULT STDMETHODCALLTYPE Indicate( 
            /* [in] */
            LONG lObjectCount,
            /* [size_is][in] */
            IWbemClassObject __RPC_FAR *__RPC_FAR *apObjArray
            );
        
    virtual HRESULT STDMETHODCALLTYPE SetStatus( 
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
            );
};


ULONG QuerySink::AddRef()
{
    return InterlockedIncrement(&m_lRef);
}

ULONG QuerySink::Release()
{
    LONG lRef = InterlockedDecrement(&m_lRef);
    if(lRef == 0)
        delete this;
    return lRef;
}

HRESULT QuerySink::QueryInterface(REFIID riid, void** ppv)
{
    if (riid == IID_IUnknown || riid == IID_IWbemObjectSink)
    {
        *ppv = (IWbemObjectSink *) this;
        AddRef();
        return WBEM_S_NO_ERROR;
    }
    else return E_NOINTERFACE;
}


HRESULT QuerySink::Indicate(long lObjCount, IWbemClassObject **pArray)
{
    for (long i = 0; i < lObjCount; i++)
    {
        IWbemClassObject *pObj = pArray[i];

        // ... use the object.

        // AddRef() is only required if the object will be held after
        // the return to the caller.
    }

    return WBEM_S_NO_ERROR;
}

HRESULT QuerySink::SetStatus(
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
        )
{
    printf("QuerySink::SetStatus hResult = 0x%X\n", hResult);
    return WBEM_S_NO_ERROR;
}
```



## <a name="requirements"></a><span data-ttu-id="99ee2-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="99ee2-138">Requirements</span></span>



| <span data-ttu-id="99ee2-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="99ee2-139">Requirement</span></span> | <span data-ttu-id="99ee2-140">Wert</span><span class="sxs-lookup"><span data-stu-id="99ee2-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99ee2-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="99ee2-141">Minimum supported client</span></span><br/> | <span data-ttu-id="99ee2-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="99ee2-142">Windows Vista</span></span><br/>                                                                                 |
| <span data-ttu-id="99ee2-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="99ee2-143">Minimum supported server</span></span><br/> | <span data-ttu-id="99ee2-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="99ee2-144">Windows Server 2008</span></span><br/>                                                                           |
| <span data-ttu-id="99ee2-145">Header</span><span class="sxs-lookup"><span data-stu-id="99ee2-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="99ee2-146"><dt>Wbemcli. h (Include wbemittell. h)</dt></span><span class="sxs-lookup"><span data-stu-id="99ee2-146"><dt>Wbemcli.h (include Wbemidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="99ee2-147">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="99ee2-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="99ee2-148"><dt>Wbemuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="99ee2-148"><dt>Wbemuuid.lib</dt></span></span> </dl>                  |
| <span data-ttu-id="99ee2-149">DLL</span><span class="sxs-lookup"><span data-stu-id="99ee2-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99ee2-150"><dt>Fastprox.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99ee2-150"><dt>Fastprox.dll</dt></span></span> </dl>                  |



## <a name="see-also"></a><span data-ttu-id="99ee2-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99ee2-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99ee2-152">COM-API für WMI</span><span class="sxs-lookup"><span data-stu-id="99ee2-152">COM API for WMI</span></span>](com-api-for-wmi.md)
</dt> <dt>

[<span data-ttu-id="99ee2-153">Erstellen eines asynchronen Aufrufes mit C++</span><span class="sxs-lookup"><span data-stu-id="99ee2-153">Making an Asynchronous Call with C++</span></span>](making-an-asynchronous-call-with-c--.md)
</dt> <dt>

[<span data-ttu-id="99ee2-154">Festlegen der Sicherheit für einen asynchronen-Befehl</span><span class="sxs-lookup"><span data-stu-id="99ee2-154">Setting Security on an Asynchronous Call</span></span>](setting-security-on-an-asynchronous-call.md)
</dt> <dt>

[<span data-ttu-id="99ee2-155">Empfangen von Ereignissen für die Dauer der Anwendung</span><span class="sxs-lookup"><span data-stu-id="99ee2-155">Receiving Events for the Duration of your Application</span></span>](receiving-events-for-the-duration-of-your-application.md)
</dt> </dl>

 

 




