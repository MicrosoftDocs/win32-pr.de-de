---
description: Im folgenden finden Sie Hinweise und Tipps, die beim Schreiben einer Anwendung für TAPI 3 zu beachten sind.
ms.assetid: 55aae46a-af5c-4b6d-89fc-9063f078bcd6
title: Hinweise und Tipps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9202bdef97fb87b9f0736ed032b298af56917d8c
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106363065"
---
# <a name="hints-and-tips"></a><span data-ttu-id="41b87-103">Hinweise und Tipps</span><span class="sxs-lookup"><span data-stu-id="41b87-103">Hints and Tips</span></span>

<span data-ttu-id="41b87-104">Im folgenden finden Sie Hinweise und Tipps, die beim Schreiben einer Anwendung für TAPI 3 zu beachten sind:</span><span class="sxs-lookup"><span data-stu-id="41b87-104">The following are hints and tips to consider when writing an application for TAPI 3:</span></span>

1.  <span data-ttu-id="41b87-105">COM [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) erstellt indirekt Windows. Dies ist besonders wichtig für Apartment Threading.</span><span class="sxs-lookup"><span data-stu-id="41b87-105">COM [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) indirectly creates windows; this is especially important for apartment threading.</span></span> <span data-ttu-id="41b87-106">Wenn ein Thread Windows erstellt, muss er Nachrichten verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="41b87-106">If a thread creates any windows, it must process messages.</span></span> <span data-ttu-id="41b87-107">Wenn Ihre Threads **CoInitialize** aufzurufen, führen Sie ein nachrichtenpump aus, um Probleme zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="41b87-107">If your threads call **CoInitialize**, run a message pump to prevent problems.</span></span> <span data-ttu-id="41b87-108">Beispielsweise könnte com das Marshalling ordnungsgemäß verhindern, oder Methoden für COM-Schnittstellen, wie z. **b. iglobalinterfacetable** , hängen möglicherweise auf.</span><span class="sxs-lookup"><span data-stu-id="41b87-108">For example, COM might stop marshalling properly, or methods on COM interfaces, such as **IGlobalInterfaceTable** might hang.</span></span>

    <span data-ttu-id="41b87-109">In Apartment Threading müssen Sie über ein nachrichtenpump verfügen, unabhängig davon, ob Sie auf Synchronisierungs Objekte warten.</span><span class="sxs-lookup"><span data-stu-id="41b87-109">In apartment threading you must have a message pump regardless of whether you wait for synchronization objects.</span></span> <span data-ttu-id="41b87-110">Dies ist besonders wichtig, wenn Sie über eine Konsolenanwendung verfügen oder ein lokales com-/Remote Server Objekt schreiben, das Apartment Thread ist (wobei keine Konsole oder GUI vorhanden ist, das Steuerelement aber nur im System ausgeführt wird).</span><span class="sxs-lookup"><span data-stu-id="41b87-110">This is particularly important if you have a console application or you write a COM local/remote server object that is apartment threaded (where you do not have a console or a GUI, but the control just "runs" in the system).</span></span>

    > [!Caution]  
    > <span data-ttu-id="41b87-111">Beim Aufrufen der Warte-und Synchronisierungs Funktionen, z. b. " [**Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep)", " [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects)", " [**WaitForMultipleObjectsEx**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex)", " [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)", " [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex)" usw.</span><span class="sxs-lookup"><span data-stu-id="41b87-111">When calling the wait and synchronization functions, such as [**Sleep**](/windows/desktop/api/synchapi/nf-synchapi-sleep), [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects), [**WaitForMultipleObjectsEx**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex), [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject), [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex), and so on.</span></span> <span data-ttu-id="41b87-112">Verwenden Sie stattdessen [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) , und verarbeiten Sie die Nachrichten, oder verwenden Sie [**cowaitformultiplehandles**](/windows/desktop/api/combaseapi/nf-combaseapi-cowaitformultiplehandles), die automatisch erkennen, in welchem Apartment der Thread sich der Thread befindet (STA oder MTA) und entweder in einer für com modalen Schleife (if STA) oder in einem Block auf **WaitForMultipleObjects** (if MTA) warten.</span><span class="sxs-lookup"><span data-stu-id="41b87-112">Instead, use [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) and process the messages, or use [**CoWaitForMultipleHandles**](/windows/desktop/api/combaseapi/nf-combaseapi-cowaitformultiplehandles), which will automatically detect what type of apartment the thread is in (STA or MTA) and will wait either in a COM modal loop (if STA) or block on **WaitForMultipleObjects** (if MTA).</span></span> <span data-ttu-id="41b87-113">**MsgWaitForMultipleObjects** und **cowaitformultiplehandles** verarbeiten Windows-Meldungen auch gemäß den com-Regeln.</span><span class="sxs-lookup"><span data-stu-id="41b87-113">**MsgWaitForMultipleObjects** and **CoWaitForMultipleHandles** also process windows messages according to the COM rules.</span></span>

     

    <span data-ttu-id="41b87-114">Verwenden Sie anstelle von</span><span class="sxs-lookup"><span data-stu-id="41b87-114">For example, instead of:</span></span>

    `Sleep (5000);`

    <span data-ttu-id="41b87-115">Verwendung:</span><span class="sxs-lookup"><span data-stu-id="41b87-115">Use:</span></span>

    ``` syntax
     {
       DWORD dwSignalled;
       HANDLE heventDone = CreateEvent(0, FALSE, FALSE, 0);

       CoWaitForMultipleHandles (COWAIT_ALERTABLE,
                             5000,
                             1,
                             &heventDone,
                             &dwSignalled);

       CloseHandle(heventDone);
     }
    ```

2.  <span data-ttu-id="41b87-116">**Ittapieventnotification:: Event** ist die Ereignis Funktion für apps, die in einem TAPI 3-Rückruf Thread aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="41b87-116">**ITTAPIEventNotification::Event** is the apps Event function called on a TAPI 3 callback thread.</span></span>

    <span data-ttu-id="41b87-117">Führen Sie das minimal in der Ereignis Routine aus. Verwenden Sie stattdessen Ihren eigenen Thread, wenn möglich.</span><span class="sxs-lookup"><span data-stu-id="41b87-117">Do the minimum in the Event routine; instead, use your own thread where possible.</span></span>

    <span data-ttu-id="41b87-118">Beachten Sie, dass das folgende Codebeispiel bereitgestellt wird. Dies ist jedoch keine Voraussetzung.</span><span class="sxs-lookup"><span data-stu-id="41b87-118">Be aware that the following code example is provided, but is not a requirement.</span></span>

    ```syntax
    #include <windows.h>

    HRESULT
    STDMETHODCALLTYPE
    CTAPIEventNotification::Event(
        TAPI_EVENT TapiEvent,
        IDispatch *pEvent)
    {
        //
        // Addref the event so that it does not go away.
        //
        pEvent->AddRef();

        //
        // Post a message for reference.
        //
        BOOL RetVal = PostMessage(
                                  ghDlg,
                                  WM_PRIVATETAPIEVENT,
                                  (WPARAM) TapiEvent,
                                  (LPARAM) pEvent
                                  );

        // If (RetVal == 0 ) process error here.

        return S_OK;
    }     
    ```

3.  <span data-ttu-id="41b87-119">Bearbeiten Sie keine COM-Objekte nach dem Aufruf von " [**zählinitialisieren**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize)".</span><span class="sxs-lookup"><span data-stu-id="41b87-119">Do not manipulate COM objects after calling [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize).</span></span> <span data-ttu-id="41b87-120">Die Ergebnisse sind unvorhersehbar und schädlich für eine fehlerfreie Anwendung.</span><span class="sxs-lookup"><span data-stu-id="41b87-120">The results are unpredictable and detrimental to a healthy application.</span></span> <span data-ttu-id="41b87-121">Einige Beispiele hierfür sind Arbeitsthreads und C++-Dekonstruktoren, die möglicherweise ausgeführt werden, nachdem die Anwendung die **Initialisierung** aufruft.</span><span class="sxs-lookup"><span data-stu-id="41b87-121">Some examples in which this can happen are worker threads and C++ destructors that may execute after an application calls **CoUninitialize**.</span></span>

 

 
