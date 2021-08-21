---
description: Sie können die Prozeduren und Codebeispiele in diesem Thema verwenden, um eine vollständige WMI-Clientanwendung zu erstellen, die eine COM-Initialisierung ausführt, eine Verbindung mit WMI auf dem lokalen Computer herstellt, Daten halbsynchron abruft und dann bereinigt.
ms.assetid: 35dc97aa-dcef-48c1-af8b-ce43e3cf1d3e
ms.tgt_platform: multiple
title: 'Beispiel: Abrufen von WMI-Daten vom lokalen Computer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71036d95996926ce9e5a0200587a15abb8dc992c82999aa65c54be50d0e1691b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050908"
---
# <a name="example-getting-wmi-data-from-the-local-computer"></a>Beispiel: Abrufen von WMI-Daten vom lokalen Computer

Sie können die Prozeduren und Codebeispiele in diesem Thema verwenden, um eine vollständige WMI-Clientanwendung zu erstellen, die eine COM-Initialisierung ausführt, eine Verbindung mit WMI auf dem lokalen Computer herstellt, Daten halbsynchron abruft und dann bereinigt. Dieses Beispiel ruft den Namen des Betriebssystems auf dem lokalen Computer ab und zeigt ihn an. Informationen zum Abrufen von Daten von einem Remotecomputer finden Sie unter [Beispiel: Abrufen von WMI-Daten von einem Remotecomputer.](example--getting-wmi-data-from-a-remote-computer.md) Informationen zum asynchronen Abrufen der Daten finden Sie unter Beispiel: Asynchrones Abrufen [von WMI-Daten vom lokalen Computer.](example--getting-wmi-data-from-the-local-computer-asynchronously.md)

Mit dem folgenden Verfahren wird die WMI-Anwendung ausgeführt. Die Schritte 1 bis 5 enthalten alle schritte, die zum Einrichten und Herstellen einer Verbindung mit WMI erforderlich sind, und die Schritte 6 und 7 enthalten die Daten, die abgefragt und empfangen werden.

1.  Initialisieren Sie COM-Parameter mit einem Aufruf von [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).

    Weitere Informationen finden Sie unter [Initialisieren von COM für eine WMI-Anwendung.](initializing-com-for-a-wmi-application.md)

2.  Initialisieren Sie die COM-Prozesssicherheit, indem [**Sie CoInitializeSecurity aufrufen.**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)

    Weitere Informationen finden Sie unter [Festlegen der Standardprozesssicherheitsebene mithilfe von C++.](setting-the-default-process-security-level-using-c-.md)

3.  Rufen Sie den ersten Locator für WMI ab, indem Sie [**CoCreateInstance aufrufen.**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)

    Weitere Informationen finden Sie unter [Erstellen einer Verbindung mit einem WMI-Namespace.](creating-a-connection-to-a-wmi-namespace.md)

4.  Rufen Sie einen Zeiger auf [**IWbemServices für**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) den cimv2-Stammnamespace auf dem lokalen Computer ab, indem Sie \\ [**IWbemLocator::ConnectServer aufrufen.**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) Informationen zum Herstellen einer Verbindung mit einem Remotecomputer finden Sie unter [Beispiel: Abrufen von WMI-Daten von einem Remotecomputer.](example--getting-wmi-data-from-a-remote-computer.md)

    Weitere Informationen finden Sie unter [Erstellen einer Verbindung mit einem WMI-Namespace.](creating-a-connection-to-a-wmi-namespace.md)

5.  Legen [**Sie die IWbemServices-Proxysicherheit**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) fest, damit der WMI-Dienst die Identität des Clients durch Aufrufen von [**CoSetProxyBlanket angenommen werden kann.**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)

    Weitere Informationen finden Sie unter [Festlegen der Sicherheitsebenen für eine WMI-Verbindung.](setting-the-security-levels-on-a-wmi-connection.md)

6.  Verwenden Sie [**den IWbemServices-Zeiger,**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) um Anforderungen an WMI zu senden. In diesem Beispiel wird eine Abfrage für den Namen des Betriebssystems durch Aufrufen von [**IWbemServices::ExecQuery ausgeführt.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)

    Die folgende WQL-Abfrage ist eines der Methodenargumente.

    `SELECT * FROM Win32_OperatingSystem`

    Das Ergebnis dieser Abfrage wird in einem [**IEnumWbemClassObject-Zeiger**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) gespeichert. Dadurch können die Datenobjekte aus der Abfrage halbsynchron mit der **IEnumWbemClassObject-Schnittstelle abgerufen** werden. Weitere Informationen finden Sie unter [Aufzählen von WMI.](enumerating-wmi.md) Informationen zum asynchronen Abrufen der Daten finden Sie unter Beispiel: Asynchrones Abrufen [von WMI-Daten vom lokalen Computer.](example--getting-wmi-data-from-the-local-computer-asynchronously.md)

    Weitere Informationen zum Senden von Anforderungen an WMI finden Sie unter [Bearbeiten](manipulating-class-and-instance-information.md)von Klassen- und Instanzinformationen, [Abfragen von WMI](querying-wmi.md)und Aufrufen einer [Methode.](calling-a-method.md)

7.  Hier können Sie die Daten aus der WQL-Abfrage erhalten und anzeigen. Der [**IEnumWbemClassObject-Zeiger**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) ist mit den Von der Abfrage zurückgegebenen Datenobjekten verknüpft, und die Datenobjekte können mit der [**IEnumWbemClassObject::Next-Methode abgerufen**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) werden. Diese Methode verknüpft die Datenobjekte mit einem [**IWbemClassObject-Zeiger,**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) der an die -Methode übergeben wird. Verwenden Sie [**die IWbemClassObject::Get-Methode,**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) um die gewünschten Informationen aus den Datenobjekten zu erhalten.

    Das folgende Codebeispiel wird verwendet, um die Name-Eigenschaft aus dem -Datenobjekt zu erhalten, das den Namen des Betriebssystems enthält.

    ```C++
    VARIANT vtProp;

    // Get the value of the Name property
    hr = pclsObj->Get(L"Name", 0, &vtProp, 0, 0);
    ```

    

    Nachdem der Wert der Name-Eigenschaft in der [**VARIANT-Variablen**](/windows/win32/api/oaidl/ns-oaidl-variant) vtProp gespeichert wurde, kann er dem Benutzer angezeigt werden.

    Weitere Informationen finden Sie unter [Aufzählen von WMI.](enumerating-wmi.md)

Im folgenden Codebeispiel werden WMI-Daten halbsynchron von einem lokalen Computer abgerufen.


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
        -1,                          // COM authentication
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
 
    // Connect to the root\cimv2 namespace with
    // the current user and obtain pointer pSvc
    // to make IWbemServices calls.
    hres = pLoc->ConnectServer(
         _bstr_t(L"ROOT\\CIMV2"), // Object path of WMI namespace
         NULL,                    // User name. NULL = current user
         NULL,                    // User password. NULL = current
         0,                       // Locale. NULL indicates current
         NULL,                    // Security flags.
         0,                       // Authority (for example, Kerberos)
         0,                       // Context object 
         &pSvc                    // pointer to IWbemServices proxy
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

    // Step 6: --------------------------------------------------
    // Use the IWbemServices pointer to make requests of WMI ----

    // For example, get the name of the operating system
    IEnumWbemClassObject* pEnumerator = NULL;
    hres = pSvc->ExecQuery(
        bstr_t("WQL"), 
        bstr_t("SELECT * FROM Win32_OperatingSystem"),
        WBEM_FLAG_FORWARD_ONLY | WBEM_FLAG_RETURN_IMMEDIATELY, 
        NULL,
        &pEnumerator);
    
    if (FAILED(hres))
    {
        cout << "Query for operating system name failed."
            << " Error code = 0x" 
            << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // Step 7: -------------------------------------------------
    // Get the data from the query in step 6 -------------------
 
    IWbemClassObject *pclsObj = NULL;
    ULONG uReturn = 0;
   
    while (pEnumerator)
    {
        HRESULT hr = pEnumerator->Next(WBEM_INFINITE, 1, 
            &pclsObj, &uReturn);

        if(0 == uReturn)
        {
            break;
        }

        VARIANT vtProp;

        // Get the value of the Name property
        hr = pclsObj->Get(L"Name", 0, &vtProp, 0, 0);
        wcout << " OS Name : " << vtProp.bstrVal << endl;
        VariantClear(&vtProp);

        pclsObj->Release();
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



 

 
