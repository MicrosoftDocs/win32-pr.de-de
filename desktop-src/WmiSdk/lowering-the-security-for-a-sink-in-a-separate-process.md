---
description: Windows-Verwaltungsinstrumentation (WMI) kann die Senke erstellen, um asynchrone Rückrufe für eine Client Anwendung in einem separaten Prozess zu empfangen.
ms.assetid: 3d3111ac-7d83-48d6-94e4-36cb46a506fa
ms.tgt_platform: multiple
title: Verringern der Sicherheit für eine Senke in einem separaten Prozess
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63aec8bcb451d254961acae8278cb45cb4454f37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358585"
---
# <a name="lowering-the-security-for-a-sink-in-a-separate-process"></a><span data-ttu-id="c62fe-103">Verringern der Sicherheit für eine Senke in einem separaten Prozess</span><span class="sxs-lookup"><span data-stu-id="c62fe-103">Lowering the Security for a Sink in a Separate Process</span></span>

<span data-ttu-id="c62fe-104">Windows-Verwaltungsinstrumentation (WMI) kann die Senke erstellen, um asynchrone Rückrufe für eine Client Anwendung in einem separaten Prozess zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="c62fe-104">Windows Management Instrumentation (WMI) can create the sink to receive asynchronous callbacks for a client application in a separate process.</span></span> <span data-ttu-id="c62fe-105">Der separate Prozess ist Unsecapp.exe.</span><span class="sxs-lookup"><span data-stu-id="c62fe-105">The separate process is Unsecapp.exe.</span></span> <span data-ttu-id="c62fe-106">Verwenden Sie die [**iwbemunsecuder**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="c62fe-106">Use the [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment) interface.</span></span> <span data-ttu-id="c62fe-107">Mit **iwbemunsecuredapartment** können Sie steuern, ob Unsecapp.exe Rückrufe für die Senke authentifiziert.</span><span class="sxs-lookup"><span data-stu-id="c62fe-107">**IWbemUnsecuredApartment** allows you to control whether Unsecapp.exe authenticates callbacks to the sink.</span></span> <span data-ttu-id="c62fe-108">Weitere Informationen finden Sie unter [Festlegen der Sicherheit für einen asynchronen](setting-security-on-an-asynchronous-call.md)-Befehl.</span><span class="sxs-lookup"><span data-stu-id="c62fe-108">For more information, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="c62fe-109">Anschließend können Sie die Sicherheit für diesen Prozess verringern, und WMI kann ohne Einschränkung auf die Senke zugreifen.</span><span class="sxs-lookup"><span data-stu-id="c62fe-109">You can then lower the security on that process and WMI can access the sink without restriction.</span></span> <span data-ttu-id="c62fe-110">Zur Unterstützung dieser Technik stellt WMI den Unsecapp.exe Prozess bereit, der als separater Prozess fungiert.</span><span class="sxs-lookup"><span data-stu-id="c62fe-110">To assist with this technique WMI provides the Unsecapp.exe process to function as the separate process.</span></span> <span data-ttu-id="c62fe-111">Sie können Unsecapp.exe hosten, indem Sie die [**iunsecuredapartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment) -Schnittstelle abrufen.</span><span class="sxs-lookup"><span data-stu-id="c62fe-111">You can host Unsecapp.exe with a call to the [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment) interface.</span></span>

<span data-ttu-id="c62fe-112">Die [**iunsecumenpartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment) -Schnittstelle ermöglicht es einer Client Anwendung, einen separaten dedizierten Prozess zu erstellen, der Unsecapp.exe zum Hosting einer [**iwbebobjectsink**](iwbemobjectsink.md) -Implementierung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c62fe-112">The [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment) interface allows a client application to create a separate dedicated process running Unsecapp.exe for hosting a [**IWbemObjectSink**](iwbemobjectsink.md) implementation.</span></span> <span data-ttu-id="c62fe-113">Der dedizierte Prozess kann [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) aufrufen, um den WMI-Zugriff auf den dedizierten Prozess zu gewähren, ohne die Sicherheit des Haupt Prozesses zu beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="c62fe-113">The dedicated process can call [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) to grant WMI access to the dedicated process without compromising the security of the main process.</span></span> <span data-ttu-id="c62fe-114">Nach der Initialisierung fungiert der dedizierte Prozess als Vermittler zwischen dem Hauptprozess und WMI.</span><span class="sxs-lookup"><span data-stu-id="c62fe-114">After initialization, the dedicated process acts as an intermediary between the main process and WMI.</span></span>

<span data-ttu-id="c62fe-115">Im folgenden Verfahren wird beschrieben, wie ein asynchroner-Befehl mit [**iunsecuredapartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment)durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c62fe-115">The following procedure describes how to perform an asynchronous call with [**IUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iunsecuredapartment).</span></span>

<span data-ttu-id="c62fe-116">**So führen Sie einen asynchronen aufrufsbefehl mit iunsecuredapartment aus**</span><span class="sxs-lookup"><span data-stu-id="c62fe-116">**To perform an asynchronous call with IUnsecuredApartment**</span></span>

1.  <span data-ttu-id="c62fe-117">Erstellen Sie einen dedizierten Prozess mit einem Aufrufen von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="c62fe-117">Create a dedicated process with a call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="c62fe-118">Im folgenden Codebeispiel wird [**cokreatanstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) aufgerufen, um einen dedizierten Prozess zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c62fe-118">The following code example calls [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a dedicated process.</span></span>

    ```C++
    IUnsecuredApartment* pUnsecApp = NULL;

    CoCreateInstance(CLSID_UnsecuredApartment, NULL, 
      CLSCTX_LOCAL_SERVER, IID_IUnsecuredApartment, 
      (void**)&pUnsecApp);
    ```

    

2.  <span data-ttu-id="c62fe-119">Instanziieren Sie das sink-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c62fe-119">Instantiate the sink object.</span></span>

    <span data-ttu-id="c62fe-120">Im folgenden Codebeispiel wird ein neues Sink-Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="c62fe-120">The following code example creates a new sink object.</span></span>

    ```C++
    CMySink* pSink = new CMySink;
    pSink->AddRef();
    ```

    

3.  <span data-ttu-id="c62fe-121">Erstellen Sie einen Stub für die Senke.</span><span class="sxs-lookup"><span data-stu-id="c62fe-121">Create a stub for the sink.</span></span>

    <span data-ttu-id="c62fe-122">Ein Stub ist eine Wrapper Funktion, die von der Senke erzeugt wird.</span><span class="sxs-lookup"><span data-stu-id="c62fe-122">A stub is a wrapper function produced from the sink.</span></span>

    <span data-ttu-id="c62fe-123">Im folgenden Codebeispiel wird " [**itateobjectstub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub) " aufgerufen, um einen Stub für die Senke zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c62fe-123">The following code example calls [**CreateObjectStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub) to create a stub for the sink.</span></span>

    ```C++
    IUnknown* pStubUnk = NULL; 
    pUnsecApp->CreateObjectStub(pSink, &pStubUnk);
    ```

    

4.  <span data-ttu-id="c62fe-124">Aufrufen von [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für den Wrapper und Anfordern eines Zeigers auf die [**iwbemubjectsink**](iwbemobjectsink.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="c62fe-124">Call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) for the wrapper, and request a pointer to the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span>

    <span data-ttu-id="c62fe-125">Im folgenden Codebeispiel wird [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) aufgerufen und ein Zeiger auf die [**iwbemubjectsink**](iwbemobjectsink.md) -Schnittstelle angefordert.</span><span class="sxs-lookup"><span data-stu-id="c62fe-125">The following code example calls [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) and requests a pointer to the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span>

    ```C++
    IWbemObjectSink* pStubSink = NULL;
    pStubUnk->QueryInterface(IID_IWbemObjectSink, (void **)&pStubSink); pStubUnk->Release();
    ```

    

5.  <span data-ttu-id="c62fe-126">Geben Sie den Sink-Objekt Zeiger frei.</span><span class="sxs-lookup"><span data-stu-id="c62fe-126">Release the sink object pointer.</span></span>

    <span data-ttu-id="c62fe-127">Sie können den Objekt Zeiger freigeben, da der Stub jetzt den-Zeiger besitzt.</span><span class="sxs-lookup"><span data-stu-id="c62fe-127">You can release the object pointer because the stub now owns the pointer.</span></span>

    <span data-ttu-id="c62fe-128">Im folgenden Codebeispiel wird der Senke-Objekt Zeiger freigegeben.</span><span class="sxs-lookup"><span data-stu-id="c62fe-128">The following code example releases the sink object pointer.</span></span>

    ```C++
    pSink->Release();
    ```

    

6.  <span data-ttu-id="c62fe-129">Verwenden Sie den Stub in einem beliebigen asynchronen-Befehl.</span><span class="sxs-lookup"><span data-stu-id="c62fe-129">Use the stub in any asynchronous call.</span></span>

    <span data-ttu-id="c62fe-130">Wenn Sie mit dem-Befehl fertig sind, geben Sie den lokalen Verweis Zähler frei.</span><span class="sxs-lookup"><span data-stu-id="c62fe-130">When finished with the call, release the local reference count.</span></span>

    <span data-ttu-id="c62fe-131">Im folgenden Codebeispiel wird der Stub in einem asynchronen-Befehl verwendet.</span><span class="sxs-lookup"><span data-stu-id="c62fe-131">The following code example uses the stub in an asynchronous call.</span></span>

    ```C++
    // pServices is an IWbemServices* object
    pServices->CreateInstanceEnumAsync(strClassName, 0, NULL, pStubSink);
    ```

    

    <span data-ttu-id="c62fe-132">Manchmal müssen Sie möglicherweise einen asynchronen Aufrufvorgang abbrechen, nachdem Sie den-Befehl durchführen.</span><span class="sxs-lookup"><span data-stu-id="c62fe-132">At times you may have to cancel an asynchronous call after you make the call.</span></span> <span data-ttu-id="c62fe-133">Wenn Sie den-Befehl abbrechen müssen, brechen Sie den-Befehl mit dem gleichen Zeiger ab, der ursprünglich den-Befehl durchgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="c62fe-133">If you need to cancel the call, cancel the call with the same pointer that originally made the call.</span></span>

    <span data-ttu-id="c62fe-134">Im folgenden Codebeispiel wird gezeigt, wie ein asynchroner-Befehl abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="c62fe-134">The following code example shows how to cancel an asynchronous call.</span></span>

    ```C++
    pServices->CancelAsyncCall(pStubSink);
    ```

    

7.  <span data-ttu-id="c62fe-135">Geben Sie den lokalen Verweis Zähler frei, wenn Sie die Verwendung des asynchronen Aufrufes abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="c62fe-135">Release the local reference count when you are done using the asynchronous call.</span></span>

    <span data-ttu-id="c62fe-136">Stellen Sie sicher, dass Sie den *pstubsink* -Zeiger erst freigeben, nachdem Sie sich vergewissert haben, dass der asynchrone-Befehl nicht abgebrochen werden muss.</span><span class="sxs-lookup"><span data-stu-id="c62fe-136">Make sure to release the *pStubSink* pointer only after you confirm that the asynchronous call does not need to be canceled.</span></span> <span data-ttu-id="c62fe-137">Außerdem sollten Sie *pstubsink* nicht freigeben, nachdem WMI den *psink* -Senke-Zeiger freigegeben hat.</span><span class="sxs-lookup"><span data-stu-id="c62fe-137">Further, do not release *pStubSink* after WMI releases the *pSink* sink pointer.</span></span> <span data-ttu-id="c62fe-138">Durch das Freigeben von *pstubsink* nach *psink* wird eine zirkuläre Verweis Anzahl erstellt, in der die Senke und der Stub immer im Speicher bleiben.</span><span class="sxs-lookup"><span data-stu-id="c62fe-138">Releasing *pStubSink* after *pSink* creates a circular reference count in which both the sink and the stub stay in memory forever.</span></span> <span data-ttu-id="c62fe-139">Stattdessen ist ein möglicher Speicherort für die Freigabe des Zeigers der [**iwbewbjectsink:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) -Befehl, der von WMI erstellt wurde, um zu melden, dass der ursprüngliche asynchrone-Aufrufvorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="c62fe-139">Instead, a possible location to release the pointer is in the [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) call, made by WMI to report that the original asynchronous call is complete.</span></span>

8.  <span data-ttu-id="c62fe-140">Wenn Sie den Vorgang abgeschlossen haben, können Sie com mit einem [**Release von Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="c62fe-140">When finished, uninitialize COM with a call to [**Release()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span>

    <span data-ttu-id="c62fe-141">Im folgenden Codebeispiel wird gezeigt, wie [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) auf dem *punsecapp* -Zeiger aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c62fe-141">The following code example shows how to call [**Release()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on the *pUnsecApp* pointer.</span></span>

    ```C++
    pUnsecApp->Release();
    ```

    

    <span data-ttu-id="c62fe-142">Die Codebeispiele in diesem Thema erfordern den folgenden Verweis und die \# include-Anweisung zur ordnungsgemäßen Kompilierung.</span><span class="sxs-lookup"><span data-stu-id="c62fe-142">The code examples in this topic require the following reference and \#include statement to correctly compile.</span></span>

    ```C++
    #include <wbemidl.h>
    #pragma comment(lib, "wbemuuid.lib")
    ```

    

<span data-ttu-id="c62fe-143">Weitere Informationen zur [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) -Funktion und zu Parametern finden Sie in der [com](../cossdk/component-services-portal.md) -Dokumentation im Platform Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="c62fe-143">For more information about the [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) function and parameters, see the [COM](../cossdk/component-services-portal.md) documentation in the Platform Software Development Kit (SDK).</span></span>

 

 
