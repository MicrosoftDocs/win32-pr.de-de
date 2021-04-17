---
description: Sie können das Verfahren und das Codebeispiel in diesem Thema verwenden, um eine WMI-Client Anwendung abzuschließen, die COM-Initialisierung ausführt, eine Verbindung mit WMI auf dem lokalen Computer herstellt, eine Ereignis Benachrichtigung empfängt und dann bereinigt.
ms.assetid: 4d581965-e22a-4205-908c-661eeeec88cf
ms.tgt_platform: multiple
title: 'Beispiel: empfangen von Ereignis Benachrichtigungen über WMI'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd6380d306783f8b547d0d93df0275fd36e17e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485547"
---
# <a name="example-receiving-event-notifications-through-wmi"></a>Beispiel: empfangen von Ereignis Benachrichtigungen über WMI

Sie können das Verfahren und das Codebeispiel in diesem Thema verwenden, um eine WMI-Client Anwendung abzuschließen, die COM-Initialisierung ausführt, eine Verbindung mit WMI auf dem lokalen Computer herstellt, eine Ereignis Benachrichtigung empfängt und dann bereinigt. Im Beispiel wird der Benutzer über ein Ereignis benachrichtigt, wenn ein neuer Prozess erstellt wird. Die Ereignisse werden asynchron empfangen.

Das folgende Verfahren wird verwendet, um die WMI-Anwendung auszuführen. Die Schritte 1 bis 5 enthalten alle Schritte, die für die Einrichtung und Verbindung mit WMI erforderlich sind, und in Schritt 6 werden die Ereignis Benachrichtigungen empfangen.

**So empfangen Sie eine Ereignis Benachrichtigung über WMI**

1.  Initialisieren von com-Parametern mit einem [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex)-Rückruf.

    Weitere Informationen finden Sie unter [Initialisieren von com für eine WMI-Anwendung](initializing-com-for-a-wmi-application.md).

2.  Initialisieren Sie die com-Prozesssicherheit durch Aufrufen von [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).

    Weitere Informationen finden Sie unter [Festlegen der standardmäßigen Prozess Sicherheitsstufe mithilfe von C++](setting-the-default-process-security-level-using-c-.md).

3.  Rufen Sie den anfänglichen Serverlocatorpunkt in WMI durch Aufrufen von [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)ab.

    Weitere Informationen finden Sie unter [Erstellen einer Verbindung mit einem WMI-Namespace](creating-a-connection-to-a-wmi-namespace.md).

4.  Rufen Sie mithilfe [](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) \\ von [**IWBEMLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)einen Zeiger auf IWbemServices für den Stamm-CIMV2-Namespace auf dem lokalen Computer ab. Informationen zum Herstellen einer Verbindung mit einem Remote Computer finden Sie unter [Beispiel: erhalten von WMI-Daten von einem Remote Computer aus](example--getting-wmi-data-from-a-remote-computer.md).

    Weitere Informationen finden Sie unter [Erstellen einer Verbindung mit einem WMI-Namespace](creating-a-connection-to-a-wmi-namespace.md).

5.  Legen Sie die [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Proxy Sicherheit fest, damit der WMI-Dienst die Identität des Clients durch Aufrufen von [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)annehmen kann.

    Weitere Informationen finden Sie unter [Festlegen der Sicherheitsstufen für eine WMI-Verbindung](setting-the-security-levels-on-a-wmi-connection.md).

6.  Verwenden Sie den [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Zeiger, um WMI-Anforderungen zu stellen. In diesem Beispiel wird die [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) -Methode verwendet, um asynchrone Ereignisse zu empfangen. Wenn Sie asynchrone Ereignisse empfangen, müssen Sie die Implementierung von [**iwbemjebjectsink**](iwbemobjectsink.md)bereitstellen. In diesem Beispiel wird die Implementierung in der EventSink-Klasse bereitstellt. Der Implementierungs Code und der Header Datei Code für diese Klasse werden unterhalb des Haupt Beispiels bereitgestellt. Die **IWbemServices:: ExecNotificationQueryAsync** -Methode ruft die **EventSink::** Display-Methode immer dann auf, wenn ein Ereignis empfangen wird. In diesem Beispiel wird die **EventSink::** Print-Methode immer dann aufgerufen, wenn ein Prozess erstellt wird. Um dieses Beispiel zu testen, führen Sie den Code aus und starten einen Prozess, z. b. Notepad.exe. Dadurch wird eine Ereignis Benachrichtigung ausgelöst.

    Weitere Informationen zum Erstellen von WMI-Anforderungen finden Sie unter Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md) und [Aufrufen einer Methode](calling-a-method.md).

Der folgende Beispielcode empfängt Ereignis Benachrichtigungen über WMI.


```C++
#include "eventsink.h"

int main(int iArgCnt, char ** argv)
{
    HRESULT hres;

    // Step 1: --------------------------------------------------
    // Initialize COM. ------------------------------------------

    hres =  CoInitializeEx(0, COINIT_MULTITHREADED); 
    if (FAILED(hres))
    {
        cout << "Failed to initialize COM library. Error code = 0x" 
             << hex << hres << endl;
        return 1;                  // Program has failed.
    }

    // Step 2: --------------------------------------------------
    // Set general COM security levels --------------------------

    hres =  CoInitializeSecurity(
        NULL, 
        -1,                          // COM negotiates service
        NULL,                        // Authentication services
        NULL,                        // Reserved
        RPC_C_AUTHN_LEVEL_DEFAULT,   // Default authentication 
        RPC_C_IMP_LEVEL_IMPERSONATE, // Default Impersonation  
        NULL,                        // Authentication info
        EOAC_NONE,                   // Additional capabilities 
        NULL                         // Reserved
        );

                      
    if (FAILED(hres))
    {
        cout << "Failed to initialize security. Error code = 0x" 
             << hex << hres << endl;
        CoUninitialize();
        return 1;                      // Program has failed.
    }
    
    // Step 3: ---------------------------------------------------
    // Obtain the initial locator to WMI -------------------------

    IWbemLocator *pLoc = NULL;

    hres = CoCreateInstance(
        CLSID_WbemLocator,             
        0, 
        CLSCTX_INPROC_SERVER, 
        IID_IWbemLocator, (LPVOID *) &pLoc);
 
    if (FAILED(hres))
    {
        cout << "Failed to create IWbemLocator object. "
             << "Err code = 0x"
             << hex << hres << endl;
        CoUninitialize();
        return 1;                 // Program has failed.
    }

    // Step 4: ---------------------------------------------------
    // Connect to WMI through the IWbemLocator::ConnectServer method

    IWbemServices *pSvc = NULL;
 
    // Connect to the local root\cimv2 namespace
    // and obtain pointer pSvc to make IWbemServices calls.
    hres = pLoc->ConnectServer(
        _bstr_t(L"ROOT\\CIMV2"), 
        NULL,
        NULL, 
        0, 
        NULL, 
        0, 
        0, 
        &pSvc
    );
     
    if (FAILED(hres))
    {
        cout << "Could not connect. Error code = 0x" 
             << hex << hres << endl;
        pLoc->Release();     
        CoUninitialize();
        return 1;                // Program has failed.
    }

    cout << "Connected to ROOT\\CIMV2 WMI namespace" << endl;


    // Step 5: --------------------------------------------------
    // Set security levels on the proxy -------------------------

    hres = CoSetProxyBlanket(
        pSvc,                        // Indicates the proxy to set
        RPC_C_AUTHN_WINNT,           // RPC_C_AUTHN_xxx 
        RPC_C_AUTHZ_NONE,            // RPC_C_AUTHZ_xxx 
        NULL,                        // Server principal name 
        RPC_C_AUTHN_LEVEL_CALL,      // RPC_C_AUTHN_LEVEL_xxx 
        RPC_C_IMP_LEVEL_IMPERSONATE, // RPC_C_IMP_LEVEL_xxx
        NULL,                        // client identity
        EOAC_NONE                    // proxy capabilities 
    );

    if (FAILED(hres))
    {
        cout << "Could not set proxy blanket. Error code = 0x" 
             << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // Step 6: -------------------------------------------------
    // Receive event notifications -----------------------------

    // Use an unsecured apartment for security
    IUnsecuredApartment* pUnsecApp = NULL;

    hres = CoCreateInstance(CLSID_UnsecuredApartment, NULL, 
        CLSCTX_LOCAL_SERVER, IID_IUnsecuredApartment, 
        (void**)&pUnsecApp);
 
    EventSink* pSink = new EventSink;
    pSink->AddRef();

    IUnknown* pStubUnk = NULL; 
    pUnsecApp->CreateObjectStub(pSink, &pStubUnk);

    IWbemObjectSink* pStubSink = NULL;
    pStubUnk->QueryInterface(IID_IWbemObjectSink,
        (void **) &pStubSink);

    // The ExecNotificationQueryAsync method will call
    // The EventQuery::Indicate method when an event occurs
    hres = pSvc->ExecNotificationQueryAsync(
        _bstr_t("WQL"), 
        _bstr_t("SELECT * " 
            "FROM __InstanceCreationEvent WITHIN 1 "
            "WHERE TargetInstance ISA 'Win32_Process'"), 
        WBEM_FLAG_SEND_STATUS, 
        NULL, 
        pStubSink);

    // Check for errors.
    if (FAILED(hres))
    {
        printf("ExecNotificationQueryAsync failed "
            "with = 0x%X\n", hres);
        pSvc->Release();
        pLoc->Release();
        pUnsecApp->Release();
        pStubUnk->Release();
        pSink->Release();
        pStubSink->Release();
        CoUninitialize();    
        return 1;
    }

    // Wait for the event
    Sleep(10000);
         
    hres = pSvc->CancelAsyncCall(pStubSink);

    // Cleanup
    // ========

    pSvc->Release();
    pLoc->Release();
    pUnsecApp->Release();
    pStubUnk->Release();
    pSink->Release();
    pStubSink->Release();
    CoUninitialize();

    return 0;   // Program successfully completed.
 
}
```



Die folgende Header Datei wird für die EventSink-Klasse verwendet. Die EventSink-Klasse wird im vorherigen Codebeispiel verwendet.


```C++
// EventSink.h
#ifndef EVENTSINK_H
#define EVENTSINK_H

#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")

class EventSink : public IWbemObjectSink
{
    LONG m_lRef;
    bool bDone;

public:
    EventSink() { m_lRef = 0; }
   ~EventSink() { bDone = true; }

    virtual ULONG STDMETHODCALLTYPE AddRef();
    virtual ULONG STDMETHODCALLTYPE Release();        
    virtual HRESULT 
        STDMETHODCALLTYPE QueryInterface(REFIID riid, void** ppv);

    virtual HRESULT STDMETHODCALLTYPE Indicate( 
            LONG lObjectCount,
            IWbemClassObject __RPC_FAR *__RPC_FAR *apObjArray
            );
        
    virtual HRESULT STDMETHODCALLTYPE SetStatus( 
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
            );
};

#endif    // end of EventSink.h
```



Der folgende Beispielcode ist eine Implementierung der EventSink-Klasse.


```C++
// EventSink.cpp
#include "eventsink.h"

ULONG EventSink::AddRef()
{
    return InterlockedIncrement(&m_lRef);
}

ULONG EventSink::Release()
{
    LONG lRef = InterlockedDecrement(&m_lRef);
    if(lRef == 0)
        delete this;
    return lRef;
}

HRESULT EventSink::QueryInterface(REFIID riid, void** ppv)
{
    if (riid == IID_IUnknown || riid == IID_IWbemObjectSink)
    {
        *ppv = (IWbemObjectSink *) this;
        AddRef();
        return WBEM_S_NO_ERROR;
    }
    else return E_NOINTERFACE;
}


HRESULT EventSink::Indicate(long lObjectCount,
    IWbemClassObject **apObjArray)
{
 HRESULT hres = S_OK;

    for (int i = 0; i < lObjectCount; i++)
    {
        printf("Event occurred\n");
    }

    return WBEM_S_NO_ERROR;
}

HRESULT EventSink::SetStatus(
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
        )
{
    if(lFlags == WBEM_STATUS_COMPLETE)
    {
        printf("Call complete. hResult = 0x%X\n", hResult);
    }
    else if(lFlags == WBEM_STATUS_PROGRESS)
    {
        printf("Call in progress.\n");
    }

    return WBEM_S_NO_ERROR;
}    // end of EventSink.cpp
```



 

 
