---
description: Asynchrone Aufrufe stellen schwerwiegende Sicherheitsrisiken dar, da ein Rückruf für die Senke möglicherweise nicht das Ergebnis des asynchronen Aufrufs durch die ursprüngliche Anwendung oder das Skript ist.
ms.assetid: 2b839ea9-e1e6-4123-a98a-04ebee907b3b
ms.tgt_platform: multiple
title: Festlegen der Sicherheit für einen asynchronen-Befehl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e39f78315814d3b66c97e60a6b8045d7ea9e7afe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359553"
---
# <a name="setting-security-on-an-asynchronous-call"></a><span data-ttu-id="47d9a-103">Festlegen der Sicherheit für einen asynchronen-Befehl</span><span class="sxs-lookup"><span data-stu-id="47d9a-103">Setting Security on an Asynchronous Call</span></span>

<span data-ttu-id="47d9a-104">Asynchrone Aufrufe stellen schwerwiegende Sicherheitsrisiken dar, da ein Rückruf für die [*Senke*](gloss-s.md) möglicherweise nicht das Ergebnis des asynchronen Aufrufs durch die ursprüngliche Anwendung oder das Skript ist.</span><span class="sxs-lookup"><span data-stu-id="47d9a-104">Asynchronous calls present serious security risks because a callback to the [*sink*](gloss-s.md) may not be a result of the asynchronous call by the original application or script.</span></span> <span data-ttu-id="47d9a-105">Die Sicherheit in Remote Verbindungen basiert auf der Verschlüsselung der Kommunikation zwischen dem Client und dem Anbieter auf dem Remote Computer.</span><span class="sxs-lookup"><span data-stu-id="47d9a-105">Security in remote connections is based on encryption of the communication between the client and the provider on the remote computer.</span></span> <span data-ttu-id="47d9a-106">In C++ können Sie im [**CoInitializeSecurity-CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)-Parameter die Verschlüsselung über den Authentifizierungs Ebenen-Parameter festlegen.</span><span class="sxs-lookup"><span data-stu-id="47d9a-106">In C++ you can set encryption through the authentication level parameter in the call to [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="47d9a-107">Legen Sie in der Skripterstellung *AuthenticationLevel* in der monikerverbindung oder in einem [**Swap Security**](swbemsecurity.md) -Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="47d9a-107">In scripting, set the *AuthenticationLevel* in the moniker connection or on an [**SWbemSecurity**](swbemsecurity.md) object.</span></span> <span data-ttu-id="47d9a-108">Weitere Informationen finden Sie unter [Festlegen der standardmäßigen Prozess Sicherheitsstufe mithilfe von VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="47d9a-108">For more information, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

<span data-ttu-id="47d9a-109">Das Sicherheitsrisiko für asynchrone Aufrufe besteht darin, dass WMI die Authentifizierungs Ebene für einen Rückruf verringert, bis der Rückruf erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="47d9a-109">The security risks for asynchronous calls exist because WMI lowers the authentication level on a callback until the callback succeeds.</span></span> <span data-ttu-id="47d9a-110">Bei einem ausgehenden asynchronen-Befehl kann der Client die Authentifizierungs Ebene für die Verbindung mit WMI festlegen.</span><span class="sxs-lookup"><span data-stu-id="47d9a-110">On an outgoing asynchronous call, the client can set the authentication level on the connection to WMI.</span></span> <span data-ttu-id="47d9a-111">WMI Ruft die Sicherheitseinstellungen für den Client-Befehl ab und versucht, den Rückruf mit der gleichen Authentifizierungs Ebene durchzusetzen.</span><span class="sxs-lookup"><span data-stu-id="47d9a-111">WMI retrieves the security settings on the client call and attempts to call back with the same authentication level.</span></span> <span data-ttu-id="47d9a-112">Der Rückruf wird immer auf der **\_ \_ \_ \_ Pkt- \_ Datenschutzebene der RPC-C-authn-Ebene** initiiert.</span><span class="sxs-lookup"><span data-stu-id="47d9a-112">The callback is always initiated at the **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** level.</span></span> <span data-ttu-id="47d9a-113">Wenn der Rückruf fehlschlägt, wird die Authentifizierungs Ebene von WMI auf eine Ebene gesenkt, bei der der Rückruf ggf. für die **RPC- \_ C- \_ authn-Ebene " \_ \_ None**" erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="47d9a-113">If the callback fails, WMI lowers the authentication level to a level where the callback can succeed, if necessary, to **RPC\_C\_AUTHN\_LEVEL\_NONE**.</span></span> <span data-ttu-id="47d9a-114">Im Kontext von aufrufen innerhalb des lokalen Systems, bei dem der Authentifizierungsdienst nicht Kerberos ist, wird der Rückruf immer auf **RPC- \_ C- \_ authn-Ebene " \_ \_ None**" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="47d9a-114">In the context of calls within the local system where the authentication service is not Kerberos, the callback is always returned at **RPC\_C\_AUTHN\_LEVEL\_NONE**.</span></span>

<span data-ttu-id="47d9a-115">Die minimale Authentifizierungs Ebene ist **RPC \_ C \_ authn \_ Level \_ Pkt** (**wbemauthenticationlevelpkt** für die Skripterstellung).</span><span class="sxs-lookup"><span data-stu-id="47d9a-115">The minimum authentication level is **RPC\_C\_AUTHN\_LEVEL\_PKT** (**wbemAuthenticationLevelPkt** for scripting).</span></span> <span data-ttu-id="47d9a-116">Sie können jedoch eine höhere Ebene angeben, z. **b. RPC-C- \_ \_ authn- \_ Ebene \_ Pkt \_ Privacy** (**wbemauthenticationlevelpktprivacy**).</span><span class="sxs-lookup"><span data-stu-id="47d9a-116">However, you can specify a higher level, such as **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** (**wbemAuthenticationLevelPktPrivacy**).</span></span> <span data-ttu-id="47d9a-117">Es wird empfohlen, dass Client Anwendungen oder Skripts die Authentifizierungs Ebene auf den **\_ \_ \_ \_ Standardwert der RPC C authn-Ebene** (**wbemauthenticationleveldefault**) festlegen, sodass die Authentifizierungs Ebene auf die vom Server angegebene Ebene ausgehandelt werden kann.</span><span class="sxs-lookup"><span data-stu-id="47d9a-117">It is recommended that client applications or scripts set the authentication level to **RPC\_C\_AUTHN\_LEVEL\_DEFAULT** (**wbemAuthenticationLevelDefault**) which allows the authentication level to be negotiated to the level specified by the server.</span></span>

<span data-ttu-id="47d9a-118">Der Registrierungs Wert " **HKEY \_ local \_ Machine** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **unsecappaccesscontroldefault** " steuert, ob WMI in Rückrufen eine akzeptable Authentifizierungs Ebene prüft.</span><span class="sxs-lookup"><span data-stu-id="47d9a-118">The **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**UnsecAppAccessControlDefault** registry value controls whether WMI checks for an acceptable authentication level in callbacks.</span></span> <span data-ttu-id="47d9a-119">Dies ist der einzige Mechanismus zum Schutz der senkensicherheit für asynchrone Aufrufe in Skript-oder Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="47d9a-119">This is the only mechanism for protecting sink security for asynchronous calls made in scripting or Visual Basic.</span></span> <span data-ttu-id="47d9a-120">Standardmäßig ist dieser Registrierungsschlüssel auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="47d9a-120">By default, this registry key is set to zero.</span></span> <span data-ttu-id="47d9a-121">Wenn der Registrierungsschlüssel NULL ist, überprüft WMI keine Authentifizierungs Ebenen.</span><span class="sxs-lookup"><span data-stu-id="47d9a-121">If the registry key is zero then WMI does not verify authentication levels.</span></span> <span data-ttu-id="47d9a-122">Um asynchrone Aufrufe in der Skripterstellung zu sichern, legen Sie den Registrierungsschlüssel auf 1 fest.</span><span class="sxs-lookup"><span data-stu-id="47d9a-122">To secure asynchronous calls in scripting, set the registry key to 1.</span></span> <span data-ttu-id="47d9a-123">C++-Clients können den Zugriff auf die Senke über [**iwbemunseculinipartment:: kreatesinkstub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub) steuern.</span><span class="sxs-lookup"><span data-stu-id="47d9a-123">C++ clients can call [**IWbemUnsecuredApartment::CreateSinkStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub) to control access to the sink.</span></span> <span data-ttu-id="47d9a-124">Der Wert wird standardmäßig an einem beliebigen Speicherort erstellt.</span><span class="sxs-lookup"><span data-stu-id="47d9a-124">The value is created anywhere by default.</span></span>

<span data-ttu-id="47d9a-125">Die folgenden Themen enthalten Beispiele für das Festlegen der Sicherheit für den asynchronen Sicherheitsdienst:</span><span class="sxs-lookup"><span data-stu-id="47d9a-125">The following topics provide examples of setting asynchronous call security:</span></span>

-   [<span data-ttu-id="47d9a-126">Festlegen der Sicherheit für einen asynchronen VBScript-Anrufe</span><span class="sxs-lookup"><span data-stu-id="47d9a-126">Setting Security on an Asynchronous Call in VBScript</span></span>](setting-security-on-an-asynchronous-call-in-vbscript.md)
-   <span data-ttu-id="47d9a-127">Festlegen der Sicherheit für asynchrone Aufrufe in C++</span><span class="sxs-lookup"><span data-stu-id="47d9a-127">Setting Asynchronous Call Security in C++</span></span>

## <a name="setting-asynchronous-call-security-in-c"></a><span data-ttu-id="47d9a-128">Festlegen der Sicherheit für asynchrone Aufrufe in C++</span><span class="sxs-lookup"><span data-stu-id="47d9a-128">Setting Asynchronous Call Security in C++</span></span>

<span data-ttu-id="47d9a-129">Die Methode [**iwbemunsecuanpartment:: kreatesinkstub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub) ähnelt der [**iunsecuagentpartment::**](/windows/desktop/api/Wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub) -Methode, und erstellt eine Senke in einem separaten Prozess, Unsecapp.exe, um Rückrufe zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="47d9a-129">The [**IWbemUnsecuredApartment::CreateSinkStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemunsecuredapartment-createsinkstub) method is similar to [**IUnsecuredApartment::CreateObjectStub**](/windows/desktop/api/Wbemcli/nf-wbemcli-iunsecuredapartment-createobjectstub) method and creates a sink in a separate process, Unsecapp.exe, to receive callbacks.</span></span> <span data-ttu-id="47d9a-130">Die Methode " **upatesinkstub** " verfügt jedoch über einen *dwFlag*-Parameter, der angibt, wie der separate Prozess die Zugriffs Steuerung behandelt.</span><span class="sxs-lookup"><span data-stu-id="47d9a-130">However, the **CreateSinkStub** method has a *dwFlag* parameter that specifies how the separate process handles access control.</span></span>

<span data-ttu-id="47d9a-131">Der *dwFlag* -Parameter gibt eine der folgenden Aktionen für Unsecapp.exe an:</span><span class="sxs-lookup"><span data-stu-id="47d9a-131">The *dwFlag* parameter specifies one of the following actions for Unsecapp.exe:</span></span>

-   <span data-ttu-id="47d9a-132">Verwenden Sie die Registrierungsschlüssel Einstellung, um zu bestimmen, ob der Zugriff überprüft werden soll oder nicht.</span><span class="sxs-lookup"><span data-stu-id="47d9a-132">Use the registry key setting to determine whether or not to check access.</span></span>
-   <span data-ttu-id="47d9a-133">Ignorieren Sie den Registrierungsschlüssel, und überprüfen Sie immer den Zugriff.</span><span class="sxs-lookup"><span data-stu-id="47d9a-133">Ignore the registry key and always check access.</span></span>
-   <span data-ttu-id="47d9a-134">Ignorieren Sie den Registrierungsschlüssel, und überprüfen Sie den Zugriff nie.</span><span class="sxs-lookup"><span data-stu-id="47d9a-134">Ignore the registry key and never check access.</span></span>

<span data-ttu-id="47d9a-135">Das Codebeispiel in diesem Thema erfordert, dass die folgende \# include-Anweisung ordnungsgemäß kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="47d9a-135">The code example in this topic requires the following \#include statement to correctly compile.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="47d9a-136">Im folgenden Verfahren wird beschrieben, wie ein asynchroner Befehl mit [**iwbemunsecuredapartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment)durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="47d9a-136">The following procedure describes how to perform an asynchronous call with [**IWbemUnsecuredApartment**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemunsecuredapartment).</span></span>

<span data-ttu-id="47d9a-137">**So führen Sie einen asynchronen aufrufbefehl mit iwbemunsecuredapartment aus**</span><span class="sxs-lookup"><span data-stu-id="47d9a-137">**To perform an asynchronous call with IWbemUnsecuredApartment**</span></span>

1.  <span data-ttu-id="47d9a-138">Erstellen Sie einen dedizierten Prozess mit einem Aufrufen von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="47d9a-138">Create a dedicated process with a call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="47d9a-139">Im folgenden Codebeispiel wird [**cokreatanstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) aufgerufen, um einen dedizierten Prozess zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="47d9a-139">The following code example calls [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a dedicated process.</span></span>

    ```C++
    CLSID                    CLSID_WbemUnsecuredApartment;
    IWbemUnsecuredApartment* pUnsecApp = NULL;

    CoCreateInstance(CLSID_WbemUnsecuredApartment, 
                     NULL, 
                     CLSCTX_LOCAL_SERVER, 
                     IID_IWbemUnsecuredApartment, 
                     (void**)&pUnsecApp);
    ```

    

2.  <span data-ttu-id="47d9a-140">Instanziieren Sie das sink-Objekt.</span><span class="sxs-lookup"><span data-stu-id="47d9a-140">Instantiate the sink object.</span></span>

    <span data-ttu-id="47d9a-141">Im folgenden Codebeispiel wird ein neues Sink-Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="47d9a-141">The following code example creates a new sink object.</span></span>

    ```C++
    CMySink* pSink = new CMySink;
    pSink->AddRef();
    ```

    

3.  <span data-ttu-id="47d9a-142">Erstellen Sie einen Stub für die Senke.</span><span class="sxs-lookup"><span data-stu-id="47d9a-142">Create a stub for the sink.</span></span>

    <span data-ttu-id="47d9a-143">Ein Stub ist eine Wrapper Funktion, die von der Senke erzeugt wird.</span><span class="sxs-lookup"><span data-stu-id="47d9a-143">A stub is a wrapper function produced from the sink.</span></span>

    <span data-ttu-id="47d9a-144">Im folgenden Codebeispiel wird ein Stub für die Senke erstellt.</span><span class="sxs-lookup"><span data-stu-id="47d9a-144">The following code example creates a stub for the sink.</span></span>

    ```C++
    LPCWSTR          wszReserved = NULL;           
    IWbemObjectSink* pStubSink   = NULL;
    IUnknown*        pStubUnk    = NULL; 

    pUnsecApp->CreateSinkStub(pSink,
                              WBEM_FLAG_UNSECAPP_CHECK_ACCESS,  //Authenticate callbacks regardless of registry key
                              wszReserved,
                              &pStubSink);
    ```

    

4.  <span data-ttu-id="47d9a-145">Geben Sie den Sink-Objekt Zeiger frei.</span><span class="sxs-lookup"><span data-stu-id="47d9a-145">Release the sink object pointer.</span></span>

    <span data-ttu-id="47d9a-146">Sie können den Objekt Zeiger freigeben, da der Stub jetzt den-Zeiger besitzt.</span><span class="sxs-lookup"><span data-stu-id="47d9a-146">You can release the object pointer because the stub now owns the pointer.</span></span>

    <span data-ttu-id="47d9a-147">Im folgenden Codebeispiel wird der Objekt Zeiger freigegeben.</span><span class="sxs-lookup"><span data-stu-id="47d9a-147">The following code example releases the object pointer.</span></span>

    ```C++
    pSink->Release();
    ```

    

5.  <span data-ttu-id="47d9a-148">Verwenden Sie den Stub in einem beliebigen asynchronen-Befehl.</span><span class="sxs-lookup"><span data-stu-id="47d9a-148">Use the stub in any asynchronous call.</span></span>

    <span data-ttu-id="47d9a-149">Wenn Sie mit dem-Befehl fertig sind, geben Sie den lokalen Verweis Zähler frei.</span><span class="sxs-lookup"><span data-stu-id="47d9a-149">When finished with the call, release the local reference count.</span></span>

    <span data-ttu-id="47d9a-150">Im folgenden Codebeispiel wird der Stub in einem asynchronen-Befehl verwendet.</span><span class="sxs-lookup"><span data-stu-id="47d9a-150">The following code example uses the stub in an asynchronous call.</span></span>

    ```C++
    // pServices is an IWbemServices* object
    pServices->CreateInstanceEnumAsync(strClassName, 0, NULL, pStubSink);
    ```

    

    <span data-ttu-id="47d9a-151">Manchmal müssen Sie möglicherweise einen asynchronen Aufrufvorgang abbrechen, nachdem Sie den-Befehl durchführen.</span><span class="sxs-lookup"><span data-stu-id="47d9a-151">At times you may have to cancel an asynchronous call after you make the call.</span></span> <span data-ttu-id="47d9a-152">Wenn Sie den-Befehl abbrechen müssen, brechen Sie den-Befehl mit dem gleichen Zeiger ab, der ursprünglich den-Befehl durchgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="47d9a-152">If you need to cancel the call, cancel the call with the same pointer that originally made the call.</span></span>

    <span data-ttu-id="47d9a-153">Im folgenden Codebeispiel wird beschrieben, wie ein asynchroner-Befehl abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="47d9a-153">The following code example describes how to cancel an asynchronous call.</span></span>

    ```C++
    pServices->CancelAsyncCall(pStubSink);
    ```

    

6.  <span data-ttu-id="47d9a-154">Geben Sie den lokalen Verweis Zähler frei, wenn Sie die Verwendung des asynchronen Aufrufes abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="47d9a-154">Release the local reference count when you are done using the asynchronous call.</span></span>

    <span data-ttu-id="47d9a-155">Stellen Sie sicher, dass Sie den *pstubsink* -Zeiger nur freigeben, nachdem Sie sich vergewissert haben, dass der asynchrone-Befehl nicht abgebrochen werden muss</span><span class="sxs-lookup"><span data-stu-id="47d9a-155">Make sure to release the *pStubSink* pointer only after you confirm that the asynchronous call does not must be canceled.</span></span> <span data-ttu-id="47d9a-156">Außerdem sollten Sie *pstubsink* nicht freigeben, nachdem WMI den *psink* -Senke-Zeiger freigegeben hat.</span><span class="sxs-lookup"><span data-stu-id="47d9a-156">Further, do not release *pStubSink* after WMI releases the *pSink* sink pointer.</span></span> <span data-ttu-id="47d9a-157">Durch das Freigeben von *pstubsink* nach *psink* wird eine zirkuläre Verweis Anzahl erstellt, in der die Senke und der Stub immer im Speicher bleiben.</span><span class="sxs-lookup"><span data-stu-id="47d9a-157">Releasing *pStubSink* after *pSink* creates a circular reference count in which both the sink and the stub stay in memory forever.</span></span> <span data-ttu-id="47d9a-158">Stattdessen ist ein möglicher Speicherort für die Freigabe des Zeigers der [**iwbewbjectsink:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) -Befehl, der von WMI erstellt wurde, um zu melden, dass der ursprüngliche asynchrone-Aufrufvorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="47d9a-158">Instead, a possible location to release the pointer is in the [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) call, made by WMI to report that the original asynchronous call is complete.</span></span>

7.  <span data-ttu-id="47d9a-159">Wenn Sie den Vorgang abgeschlossen haben, können Sie com mit einem [**Release von Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="47d9a-159">When finished, uninitialize COM with a call to [**Release()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).</span></span>

    <span data-ttu-id="47d9a-160">Im folgenden Codebeispiel wird gezeigt, wie [**Release ()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) auf dem *punsecapp* -Zeiger aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="47d9a-160">The following code example shows how to call [**Release()**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on the *pUnsecApp* pointer.</span></span>

    ```C++
    pUnsecApp->Release();
    ```

    

<span data-ttu-id="47d9a-161">Weitere Informationen zur [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) -Funktion und zu Parametern finden Sie in der [com](../cossdk/component-services-portal.md) -Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="47d9a-161">For more information about the [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) function and parameters, see the [COM](../cossdk/component-services-portal.md) documentation.</span></span>

 

 
