---
description: Sie können die Prozeduren und Codebeispiele in diesem Thema verwenden, um eine vollständige WMI-Clientanwendung zu erstellen, die die COM-Initialisierung ausführt, eine Verbindung mit WMI auf dem lokalen Computer herstellt, einige Daten liest und bereinigt.
ms.assetid: d80bcf9f-e57c-499f-b7b8-cf25678c5a82
ms.tgt_platform: multiple
title: 'Beispiel: Erstellen einer WMI-Anwendung'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49e7633c666beb900da4cdbe41909880d9766c903be0fc8b6aa1d4e45be8d90f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118319309"
---
# <a name="example-creating-a-wmi-application"></a>Beispiel: Erstellen einer WMI-Anwendung

Sie können die Prozeduren und Codebeispiele in diesem Thema verwenden, um eine vollständige WMI-Clientanwendung zu erstellen, die die COM-Initialisierung ausführt, eine Verbindung mit WMI auf dem lokalen Computer herstellt, einige Daten liest und bereinigt. [Unter Herstellen einer Verbindung mit WMI auf einem Remotecomputer wird](connecting-to-wmi-on-a-remote-computer.md) beschrieben, wie Sie Daten von Remotecomputern abrufen.

Das folgende Verfahren umfasst alle Schritte, die für alle C++-WMI-Anwendungen erforderlich sind.

1.  Initialisieren Sie COM-Parameter mit einem Aufruf von [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).

    Weitere Informationen finden Sie unter [Initialisieren von COM für eine WMI-Anwendung.](initializing-com-for-a-wmi-application.md)

2.  Initialisieren Sie die COM-Prozesssicherheit, indem [**Sie CoInitializeSecurity aufrufen.**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)

    Weitere Informationen finden Sie unter [Festlegen der Standardprozesssicherheitsebene mithilfe von C++.](setting-the-default-process-security-level-using-c-.md)

3.  Rufen Sie durch Aufrufen von [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)einen Zeiger auf [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) für einen Namespace auf einem angegebenen Hostcomputer ab – im einfachen Fall auf den lokalen Computer.

    Verwenden Sie den folgenden Objektpfadparameter, um eine Verbindung mit einem Remotecomputer herzustellen, z. B. Computer \_ A:

    ```C++
    _bstr_t(L"\\COMPUTER_A\ROOT\\CIMV2")
    ```

    

    Weitere Informationen finden Sie unter [Erstellen einer Verbindung mit einem WMI-Namespace.](creating-a-connection-to-a-wmi-namespace.md)

4.  Legen Sie [**die IWbemServices-Proxysicherheit**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) fest, damit der WMI-Dienst die Identität des Clients durch Aufrufen von [**CoSetProxyBlanket angenommen werden kann.**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)

    Weitere Informationen finden Sie unter [Festlegen der Sicherheitsebenen für eine WMI-Verbindung.](setting-the-security-levels-on-a-wmi-connection.md)

5.  Verwenden Sie [**den IWbemServices-Zeiger,**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) um Anforderungen an WMI zu senden. Beispiel: Abfragen aller [**Win32-Dienstinstanzen, \_**](/windows/desktop/CIMWin32Prov/win32-service) um zu bestimmen, welche Dienste beendet werden.

    Weitere Informationen finden Sie unter [Bearbeiten von Klassen- und Instanzinformationen,](manipulating-class-and-instance-information.md)Abfragen von [WMI](querying-wmi.md)und [Empfangen eines WMI-Ereignisses.](receiving-a-wmi-event.md)

6.  Bereinigt Objekte und COM.

    Weitere Informationen finden Sie unter [Bereinigen und Herunterfahren einer WMI-Anwendung.](cleaning-up-and-shutting-down-a-wmi-application.md)

Der folgende Beispielcode ist eine vollständige WMI-Clientanwendung.


```C++

#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")

int main(int argc, char **argv)
{
    HRESULT hres;

    // Initialize COM.
    hres =  CoInitializeEx(0, COINIT_MULTITHREADED); 
    if (FAILED(hres))
    {
        cout << "Failed to initialize COM library. " 
            << "Error code = 0x" 
            << hex << hres << endl;
        return 1;              // Program has failed.
    }

    // Initialize 
    hres =  CoInitializeSecurity(
        NULL,     
        -1,      // COM negotiates service                  
        NULL,    // Authentication services
        NULL,    // Reserved
        RPC_C_AUTHN_LEVEL_DEFAULT,    // authentication
        RPC_C_IMP_LEVEL_IMPERSONATE,  // Impersonation
        NULL,             // Authentication info 
        EOAC_NONE,        // Additional capabilities
        NULL              // Reserved
        );

                      
    if (FAILED(hres))
    {
        cout << "Failed to initialize security. " 
            << "Error code = 0x" 
            << hex << hres << endl;
        CoUninitialize();
        return 1;          // Program has failed.
    }

    // Obtain the initial locator to Windows Management
    // on a particular host computer.
    IWbemLocator *pLoc = 0;

    hres = CoCreateInstance(
        CLSID_WbemLocator,             
        0, 
        CLSCTX_INPROC_SERVER, 
        IID_IWbemLocator, (LPVOID *) &pLoc);
 
    if (FAILED(hres))
    {
        cout << "Failed to create IWbemLocator object. "
            << "Error code = 0x"
            << hex << hres << endl;
        CoUninitialize();
        return 1;       // Program has failed.
    }

    IWbemServices *pSvc = 0;

    // Connect to the root\cimv2 namespace with the
    // current user and obtain pointer pSvc
    // to make IWbemServices calls.

    hres = pLoc->ConnectServer(
        
        _bstr_t(L"ROOT\\CIMV2"), // WMI namespace
        NULL,                    // User name
        NULL,                    // User password
        0,                       // Locale
        NULL,                    // Security flags                 
        0,                       // Authority       
        0,                       // Context object
        &pSvc                    // IWbemServices proxy
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

    // Set the IWbemServices proxy so that impersonation
    // of the user (client) occurs.
    hres = CoSetProxyBlanket(
       
       pSvc,                         // the proxy to set
       RPC_C_AUTHN_WINNT,            // authentication service
       RPC_C_AUTHZ_NONE,             // authorization service
       NULL,                         // Server principal name
       RPC_C_AUTHN_LEVEL_CALL,       // authentication level
       RPC_C_IMP_LEVEL_IMPERSONATE,  // impersonation level
       NULL,                         // client identity 
       EOAC_NONE                     // proxy capabilities     
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


    // Use the IWbemServices pointer to make requests of WMI. 
    // Make requests here:

    // For example, query for all the running processes
    IEnumWbemClassObject* pEnumerator = NULL;
    hres = pSvc->ExecQuery(
        bstr_t("WQL"), 
        bstr_t("SELECT * FROM Win32_Process"),
        WBEM_FLAG_FORWARD_ONLY | WBEM_FLAG_RETURN_IMMEDIATELY, 
        NULL,
        &pEnumerator);
    
    if (FAILED(hres))
    {
        cout << "Query for processes failed. "
             << "Error code = 0x" 
             << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 1;               // Program has failed.
    }
    else
    { 
        IWbemClassObject *pclsObj;
        ULONG uReturn = 0;
   
        while (pEnumerator)
        {
            hres = pEnumerator->Next(WBEM_INFINITE, 1, 
                &pclsObj, &uReturn);

            if(0 == uReturn)
            {
                break;
            }

            VARIANT vtProp;

            // Get the value of the Name property
            hres = pclsObj->Get(L"Name", 0, &vtProp, 0, 0);
            wcout << "Process Name : " << vtProp.bstrVal << endl;
            VariantClear(&vtProp);
            
            pclsObj->Release();
            pclsObj = NULL;
        }
         
    }
 
    // Cleanup
    // ========
    
    pSvc->Release();
    pLoc->Release();
    pEnumerator->Release();  
    
    CoUninitialize();

    return 0;   // Program successfully completed.
}
```



 

 
