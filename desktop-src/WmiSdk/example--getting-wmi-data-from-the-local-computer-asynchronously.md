---
description: Sie können die Prozeduren und Codebeispiele in diesem Thema verwenden, um eine vollständige WMI-Clientanwendung zu erstellen, die die COM-Initialisierung ausführt, eine Verbindung mit WMI auf dem lokalen Computer herstellt, Daten asynchron abruft und dann bereinigt.
ms.assetid: 1e11ca27-e67d-486c-8fc5-a10382edfff3
ms.tgt_platform: multiple
title: 'Beispiel: Asynchrones Abrufen von WMI-Daten vom lokalen Computer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67eb71247816319553389c451dd2e7ad268c49ee7aadeaddc118a3f08448171b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118319428"
---
# <a name="example-getting-wmi-data-from-the-local-computer-asynchronously"></a>Beispiel: Asynchrones Abrufen von WMI-Daten vom lokalen Computer

Sie können die Prozeduren und Codebeispiele in diesem Thema verwenden, um eine vollständige WMI-Clientanwendung zu erstellen, die die COM-Initialisierung ausführt, eine Verbindung mit WMI auf dem lokalen Computer herstellt, Daten asynchron abruft und dann bereinigt. Dieses Beispiel ruft den Namen des Betriebssystems auf dem lokalen Computer ab und zeigt ihn an.

Mit dem folgenden Verfahren wird die WMI-Anwendung ausgeführt. Die Schritte 1 bis 5 enthalten alle erforderlichen Schritte zum Einrichten und Herstellen einer Verbindung mit WMI. Die Schritte 6 und 7 enthalten die Schritte 6 und 7, in denen der Betriebssystemname asynchron abgerufen wird.

**So erhalten Sie AsynchronE WMI-Daten vom lokalen Computer**

1.  Initialisieren Sie COM-Parameter mit einem Aufruf von [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).

    Weitere Informationen finden Sie unter [Initialisieren von COM für eine WMI-Anwendung.](initializing-com-for-a-wmi-application.md)

2.  Initialisieren Sie die COM-Prozesssicherheit, indem [**Sie CoInitializeSecurity aufrufen.**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)

    Weitere Informationen finden Sie unter [Festlegen der Standardprozesssicherheitsebene mithilfe von C++.](setting-the-default-process-security-level-using-c-.md)

3.  Rufen Sie den ersten Locator für WMI ab, indem Sie [**CoCreateInstance aufrufen.**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)

    Weitere Informationen finden Sie unter [Erstellen einer Verbindung mit einem WMI-Namespace.](creating-a-connection-to-a-wmi-namespace.md)

4.  Rufen Sie einen Zeiger auf [**IWbemServices für**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) den cimv2-Stammnamespace auf dem lokalen Computer ab, indem Sie \\ [**IWbemLocator::ConnectServer aufrufen.**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) Weitere Informationen zum Herstellen einer Verbindung mit einem Remotecomputer finden Sie unter Beispiel: Abrufen von [WMI-Daten von einem Remotecomputer.](example--getting-wmi-data-from-a-remote-computer.md)

    Weitere Informationen finden Sie unter [Erstellen einer Verbindung mit einem WMI-Namespace.](creating-a-connection-to-a-wmi-namespace.md)

5.  Legen [**Sie die IWbemServices-Proxysicherheit**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) fest, damit der WMI-Dienst die Identität des Clients durch Aufrufen von [**CoSetProxyBlanket angenommen werden kann.**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)

    Weitere Informationen finden Sie unter [Festlegen der Sicherheitsebenen für eine WMI-Verbindung.](setting-the-security-levels-on-a-wmi-connection.md)

6.  Verwenden Sie [**den IWbemServices-Zeiger,**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) um Anforderungen an WMI zu senden. In diesem Beispiel wird die [**IWbemServices::ExecQueryAsync-Methode**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) verwendet, um die Daten asynchron zu empfangen. Wenn Sie Daten asynchron empfangen, müssen Sie eine Implementierung von [**IWbemObjectSink bereitstellen.**](iwbemobjectsink.md) In diesem Beispiel wird die Implementierung in der QuerySink-Klasse angegeben. Der Implementierungscode und der Headerdateicode für diese Klasse werden im Anschluss an das Hauptbeispiel bereitgestellt. Die **IWbemServices::ExecQueryAsync-Methode** ruft die QuerySink::Indicate-Methode auf, wenn die Daten empfangen werden.

    Weitere Informationen zum Erstellen einer WMI-Anforderung finden Sie unter Manipulating Class and Instance Information (Bearbeiten von Klassen- und [Instanzinformationen)](manipulating-class-and-instance-information.md) und [Calling a Method (Aufrufen einer Methode).](calling-a-method.md)

7.  Warten Sie, bis die Daten asynchron abgerufen werden. Verwenden Sie [**die IWbemServices::CancelAsyncCall-Methode,**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) um den asynchronen Aufruf manuell zu beenden.

Das folgende Codebeispiel ruft WMI-Daten asynchron vom lokalen Computer ab.


```C++
#include "querysink.h"


int main(int argc, char **argv)
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

    hres =  CoInitializeSecurity(NULL, 
                                 -1,                          // COM authentication
                                 NULL,                        // Authentication services
                                 NULL,                        // Reserved
                                 RPC_C_AUTHN_LEVEL_DEFAULT,   // Default authentication 
                                 RPC_C_IMP_LEVEL_IMPERSONATE, // Default Impersonation  
                                 NULL,                        // Authentication info
                                 EOAC_NONE,                   // Additional capabilities 
                                 NULL);                       // Reserved

                      
    if (FAILED(hres))
    {
        cout << "Failed to initialize security. Error code = 0x" 
            << hex << hres << endl;
        CoUninitialize();
        return 1;                    // Program has failed.
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
        cout << "Failed to create IWbemLocator object."
            << " Err code = 0x"
            << hex << hres << endl;
        CoUninitialize();
        return 1;                 // Program has failed.
    }

    // Step 4: -----------------------------------------------------
    // Connect to WMI through the IWbemLocator::ConnectServer method

    IWbemServices *pSvc = NULL;
 
    // Connect to the local root\cimv2 namespace
    // and obtain pointer pSvc to make IWbemServices calls.
    hres = pLoc->ConnectServer(_bstr_t(L"ROOT\\CIMV2"), 
                               NULL,
                               NULL,
                               0,
                               NULL,
                               0,
                               0, 
                               &pSvc);
    
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

    hres = CoSetProxyBlanket(pSvc,                        // Indicates the proxy to set
                             RPC_C_AUTHN_WINNT,           // RPC_C_AUTHN_xxx
                             RPC_C_AUTHZ_NONE,            // RPC_C_AUTHZ_xxx
                             NULL,                        // Server principal name 
                             RPC_C_AUTHN_LEVEL_CALL,      // RPC_C_AUTHN_LEVEL_xxx 
                             RPC_C_IMP_LEVEL_IMPERSONATE, // RPC_C_IMP_LEVEL_xxx
                             NULL,                        // client identity
                             EOAC_NONE);                  // proxy capabilities 

    if (FAILED(hres))
    {
        cout << "Could not set proxy blanket. Error code = 0x" 
            << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // Step 6: --------------------------------------------------
    // Use the IWbemServices pointer to make requests of WMI ----

    // For example, get the name of the operating system.
    // The IWbemService::ExecQueryAsync method will call
    // the QuerySink::Indicate method when it receives a result
    // and the QuerySink::Indicate method will display the OS name
    QuerySink* pResponseSink = new QuerySink();
    pResponseSink->AddRef();
    hres = pSvc->ExecQueryAsync(bstr_t("WQL"), 
                                bstr_t("SELECT * FROM Win32_OperatingSystem"),
                                WBEM_FLAG_BIDIRECTIONAL, 
                                NULL,
                                pResponseSink);
    
    if (FAILED(hres))
    {
        cout << "Query for operating system name failed."
            << " Error code = 0x" 
            << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();
        pResponseSink->Release();
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // Step 7: -------------------------------------------------
    // Wait to get the data from the query in step 6 -----------
    Sleep(500);
    pSvc->CancelAsyncCall(pResponseSink);

    // Cleanup
    // ========
    pSvc->Release();
    pLoc->Release();
    CoUninitialize();

    return 0;   // Program successfully completed.
 
}
```



Die folgende Headerdatei wird für die QuerySink-Klasse verwendet. Die QuerySink-Klasse wird im vorherigen Codebeispiel verwendet.


```C++
// QuerySink.h
#ifndef QUERYSINK_H
#define QUERYSINK_H

#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")

class QuerySink : public IWbemObjectSink
{
    LONG m_lRef;
    bool bDone;
 CRITICAL_SECTION threadLock; // for thread safety

public:
    QuerySink() { m_lRef = 0; bDone = false; 
     InitializeCriticalSection(&threadLock); }
    ~QuerySink() { bDone = true;
        DeleteCriticalSection(&threadLock); }

    virtual ULONG STDMETHODCALLTYPE AddRef();
    virtual ULONG STDMETHODCALLTYPE Release();        
    virtual HRESULT STDMETHODCALLTYPE QueryInterface(REFIID riid,
        void** ppv);

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

 bool IsDone();
};

#endif    // end of QuerySink.h
```



Das folgende Codebeispiel ist eine Implementierung der QuerySink-Klasse.


```C++
// QuerySink.cpp
#include "querysink.h"

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


HRESULT QuerySink::Indicate(long lObjectCount,
    IWbemClassObject **apObjArray)
{
 HRESULT hres = S_OK;

    for (int i = 0; i < lObjectCount; i++)
    {
        VARIANT varName;
        hres = apObjArray[i]->Get(_bstr_t(L"Name"),
            0, &varName, 0, 0);

        if (FAILED(hres))
        {
            cout << "Failed to get the data from the query"
                << " Error code = 0x"
                << hex << hres << endl;
            return WBEM_E_FAILED;       // Program has failed.
        }

        printf("Name: %ls\n", V_BSTR(&varName));
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
 if(lFlags == WBEM_STATUS_COMPLETE)
 {
  printf("Call complete.\n");

  EnterCriticalSection(&threadLock);
  bDone = true;
  LeaveCriticalSection(&threadLock);
 }
 else if(lFlags == WBEM_STATUS_PROGRESS)
 {
  printf("Call in progress.\n");
 }
    
    return WBEM_S_NO_ERROR;
}


bool QuerySink::IsDone()
{
    bool done = true;

 EnterCriticalSection(&threadLock);
 done = bDone;
 LeaveCriticalSection(&threadLock);

    return done;
}    // end of QuerySink.cpp
```



 

 
