---
description: Mithilfe der Prozeduren und Codebeispiele in diesem Thema können Sie eine vollständige WMI-Client Anwendung erstellen, die COM-Initialisierung ausführt, eine Verbindung mit WMI auf dem lokalen Computer herstellt, Daten liest und bereinigt.
ms.assetid: d80bcf9f-e57c-499f-b7b8-cf25678c5a82
ms.tgt_platform: multiple
title: 'Beispiel: Erstellen einer WMI-Anwendung'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e76836090d09ecee413da34d9a15381b9d0a891
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368238"
---
# <a name="example-creating-a-wmi-application"></a><span data-ttu-id="e8e13-103">Beispiel: Erstellen einer WMI-Anwendung</span><span class="sxs-lookup"><span data-stu-id="e8e13-103">Example: Creating a WMI Application</span></span>

<span data-ttu-id="e8e13-104">Mithilfe der Prozeduren und Codebeispiele in diesem Thema können Sie eine vollständige WMI-Client Anwendung erstellen, die COM-Initialisierung ausführt, eine Verbindung mit WMI auf dem lokalen Computer herstellt, Daten liest und bereinigt.</span><span class="sxs-lookup"><span data-stu-id="e8e13-104">You can use the procedure and code examples in this topic to create a complete WMI client application that performs COM initialization, connects to WMI on the local computer, reads some data, and cleans up.</span></span> <span data-ttu-id="e8e13-105">[Beim Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md) wird beschrieben, wie Sie Daten von Remote Computern abrufen.</span><span class="sxs-lookup"><span data-stu-id="e8e13-105">[Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md) describes how to obtain data from remote computers.</span></span>

<span data-ttu-id="e8e13-106">Das folgende Verfahren enthält alle Schritte, die für alle C++-WMI-Anwendungen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="e8e13-106">This following procedure includes all of the steps that are required by all C++ WMI applications.</span></span>

1.  <span data-ttu-id="e8e13-107">Initialisieren von com-Parametern mit einem [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex)-Rückruf.</span><span class="sxs-lookup"><span data-stu-id="e8e13-107">Initialize COM parameters with a call to [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

    <span data-ttu-id="e8e13-108">Weitere Informationen finden Sie unter [Initialisieren von com für eine WMI-Anwendung](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="e8e13-108">For more information, see [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

2.  <span data-ttu-id="e8e13-109">Initialisieren Sie die com-Prozesssicherheit durch Aufrufen von [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="e8e13-109">Initialize COM process security by calling [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

    <span data-ttu-id="e8e13-110">Weitere Informationen finden Sie unter [Festlegen der standardmäßigen Prozess Sicherheitsstufe mithilfe von C++](setting-the-default-process-security-level-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="e8e13-110">For more information, see [Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md).</span></span>

3.  <span data-ttu-id="e8e13-111">Abrufen eines Zeigers auf [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) für einen Namespace auf einem angegebenen Host Computer – der lokale Computer im einfachen Fall – durch Aufrufen von [**IWBEMLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span><span class="sxs-lookup"><span data-stu-id="e8e13-111">Obtain a pointer to [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) for a namespace on a specified host computer—the local computer in the simple case—by calling [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span>

    <span data-ttu-id="e8e13-112">Verwenden Sie zum Herstellen einer Verbindung mit einem Remote Computer, z. b. Computer \_ a, den folgenden Objekt Pfad Parameter:</span><span class="sxs-lookup"><span data-stu-id="e8e13-112">To connect to a remote computer, for example Computer\_A, use the following object path parameter:</span></span>

    ```C++
    _bstr_t(L"\\COMPUTER_A\ROOT\\CIMV2")
    ```

    

    <span data-ttu-id="e8e13-113">Weitere Informationen finden Sie unter [Erstellen einer Verbindung mit einem WMI-Namespace](creating-a-connection-to-a-wmi-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="e8e13-113">For more information, see [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

4.  <span data-ttu-id="e8e13-114">Legen Sie die [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Proxy Sicherheit fest, damit der WMI-Dienst die Identität des Clients durch Aufrufen von [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="e8e13-114">Set the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy security so WMI service can impersonate the client by calling [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

    <span data-ttu-id="e8e13-115">Weitere Informationen finden Sie unter [Festlegen der Sicherheitsstufen für eine WMI-Verbindung](setting-the-security-levels-on-a-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="e8e13-115">For more information, see [Setting the Security Levels on a WMI Connection](setting-the-security-levels-on-a-wmi-connection.md).</span></span>

5.  <span data-ttu-id="e8e13-116">Verwenden Sie den [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Zeiger, um WMI-Anforderungen zu stellen.</span><span class="sxs-lookup"><span data-stu-id="e8e13-116">Use the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer to make requests of WMI.</span></span> <span data-ttu-id="e8e13-117">Beispielsweise Abfragen für alle [**Win32- \_ Dienst**](/windows/desktop/CIMWin32Prov/win32-service) Instanzen, um zu bestimmen, welche Dienste beendet werden.</span><span class="sxs-lookup"><span data-stu-id="e8e13-117">For example, querying for all the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) instances to determine which services are stopped.</span></span>

    <span data-ttu-id="e8e13-118">Weitere Informationen finden Sie unter Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md), [Abfragen von WMI](querying-wmi.md)und [empfangen eines WMI-Ereignisses](receiving-a-wmi-event.md).</span><span class="sxs-lookup"><span data-stu-id="e8e13-118">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md), [Querying WMI](querying-wmi.md), and [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

6.  <span data-ttu-id="e8e13-119">Bereinigen Sie Objekte und com.</span><span class="sxs-lookup"><span data-stu-id="e8e13-119">Clean up objects and COM.</span></span>

    <span data-ttu-id="e8e13-120">Weitere Informationen finden Sie unter [Bereinigen und Herunterfahren einer WMI-Anwendung](cleaning-up-and-shutting-down-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="e8e13-120">For more information, see [Cleaning up and Shutting Down a WMI Application](cleaning-up-and-shutting-down-a-wmi-application.md).</span></span>

<span data-ttu-id="e8e13-121">Der folgende Beispielcode ist eine komplette WMI-Client Anwendung.</span><span class="sxs-lookup"><span data-stu-id="e8e13-121">The following example code is a complete WMI client application.</span></span>


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



 

 
