---
description: Sie können die Prozeduren und Codebeispiele in diesem Thema verwenden, um eine vollständige WMI-Clientanwendung zu erstellen, die die COM-Initialisierung ausführt, eine Verbindung mit WMI auf dem lokalen Computer herstellt, eine Anbietermethode aufruft und dann bereinigt.
ms.assetid: ee8faa14-74ec-49a2-88d6-187627c40071
ms.tgt_platform: multiple
title: 'Beispiel: Aufrufen einer Anbietermethode'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b937ff23d7700b25f9acd9512da56a1dce87adefe8170b3651b564ec437973d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118108945"
---
# <a name="example-calling-a-provider-method"></a>Beispiel: Aufrufen einer Anbietermethode

Sie können die Prozeduren und Codebeispiele in diesem Thema verwenden, um eine vollständige WMI-Clientanwendung zu erstellen, die die COM-Initialisierung ausführt, eine Verbindung mit WMI auf dem lokalen Computer herstellt, eine Anbietermethode aufruft und dann bereinigt. Die [**Win32 \_ Process::Create-Methode**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) wird verwendet, um Notepad.exe in einem neuen Prozess zu starten.

Mit dem folgenden Verfahren wird die WMI-Anwendung ausgeführt. Die Schritte 1 bis 5 enthalten alle Schritte, die zum Einrichten und Herstellen einer Verbindung mit WMI erforderlich sind. In 6 wird die Anbietermethode aufgerufen.

**So rufen Sie eine Anbietermethode auf**

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

6.  Verwenden Sie [**den IWbemServices-Zeiger,**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) um Anforderungen an WMI zu senden. In diesem Beispiel wird [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) zum Aufrufen der [**Anbietermethode Win32 \_ Process::Create verwendet.**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process)

    Weitere Informationen zum Senden von Anforderungen an WMI finden Sie unter Manipulating Class and Instance Information (Bearbeiten von Klassen- und [Instanzinformationen)](manipulating-class-and-instance-information.md) und [Calling a Method (Aufrufen einer Methode).](calling-a-method.md)

    Wenn die Anbietermethode über In-Parameters oder out-Parameter verfügt, müssen [**IWbemClassObject-Zeigern**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) Werte der Parameter übergeben werden. Bei Parametern müssen Sie eine Instanz der Parameterdefinitionen erstellen und dann die Werte dieser neuen Instanzen festlegen. Die [**Win32 \_ Process::Create-Methode**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) erfordert einen Wert für den CommandLine-In-Parameter, um ordnungsgemäß ausgeführt zu werden. 

    Im folgenden Codebeispiel wird ein [**IWbemClassObject-Zeiger**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) erstellt, eine neue Instanz der [**Win32 \_ Process::Create-In-Parameterdefinitionen**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) erzeugt und dann der Wert des *CommandLine-In-Parameters* auf Notepad.exe.

    ```C++
    // Set up to call the Win32_Process::Create method
    BSTR MethodName = SysAllocString(L"Create");
    BSTR ClassName = SysAllocString(L"Win32_Process");

    IWbemClassObject* pClass = NULL;
    hres = pSvc->GetObject(ClassName, 0, NULL, &pClass, NULL);

    IWbemClassObject* pInParamsDefinition = NULL;
    hres = pClass->GetMethod(MethodName, 0, 
        &pInParamsDefinition, NULL);

    IWbemClassObject* pClassInstance = NULL;
    hres = pInParamsDefinition->SpawnInstance(0, &pClassInstance);

    // Create the values for the in-parameters
    VARIANT varCommand;
    varCommand.vt = VT_BSTR;
    varCommand.bstrVal = _bstr_t(L"notepad.exe");

    // Store the value for the in-parameters
    hres = pClassInstance->Put(L"CommandLine", 0,
        &varCommand, 0);
    wprintf(L"The command is: %s\n", V_BSTR(&varCommand));
    ```

    

    Das folgende Codebeispiel zeigt, wie die [**Out-Parameter der Win32 \_ Process::Create-Methode**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) an einen [**IWbemClassObject-Zeiger**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) übergeben werden. Der out-Parameterwert wird mit der [**IWbemClassObject::Get-Methode**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) ermittelt und in einer [**VARIANT-Variablen**](/windows/win32/api/oaidl/ns-oaidl-variant) gespeichert, damit er dem Benutzer angezeigt werden kann.

    ```C++
    // Execute Method
    IWbemClassObject* pOutParams = NULL;
    hres = pSvc->ExecMethod(ClassName, MethodName, 0,
        NULL, pClassInstance, &pOutParams, NULL);

    VARIANT varReturnValue;
    hres = pOutParams->Get(_bstr_t(L"ReturnValue"), 0, 
        &varReturnValue, NULL, 0);
    ```

    

Das folgende Codebeispiel zeigt, wie sie eine Anbietermethode mit WMI aufrufen.


```C++
#define _WIN32_DCOM

#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")

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
    // Set security levels for the proxy ------------------------

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

    // set up to call the Win32_Process::Create method
    BSTR MethodName = SysAllocString(L"Create");
    BSTR ClassName = SysAllocString(L"Win32_Process");

    IWbemClassObject* pClass = NULL;
    hres = pSvc->GetObject(ClassName, 0, NULL, &pClass, NULL);

    IWbemClassObject* pInParamsDefinition = NULL;
    hres = pClass->GetMethod(MethodName, 0, 
        &pInParamsDefinition, NULL);

    IWbemClassObject* pClassInstance = NULL;
    hres = pInParamsDefinition->SpawnInstance(0, &pClassInstance);

    // Create the values for the in parameters
    VARIANT varCommand;
    varCommand.vt = VT_BSTR;
    varCommand.bstrVal = _bstr_t(L"notepad.exe");

    // Store the value for the in parameters
    hres = pClassInstance->Put(L"CommandLine", 0,
        &varCommand, 0);
    wprintf(L"The command is: %s\n", V_BSTR(&varCommand));

    // Execute Method
    IWbemClassObject* pOutParams = NULL;
    hres = pSvc->ExecMethod(ClassName, MethodName, 0,
    NULL, pClassInstance, &pOutParams, NULL);

    if (FAILED(hres))
    {
        cout << "Could not execute method. Error code = 0x" 
             << hex << hres << endl;
        VariantClear(&varCommand);
        SysFreeString(ClassName);
        SysFreeString(MethodName);
        pClass->Release();
        pClassInstance->Release();
        pInParamsDefinition->Release();
        pOutParams->Release();
        pSvc->Release();
        pLoc->Release();
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // To see what the method returned,
    // use the following code.  The return value will
    // be in &varReturnValue
    VARIANT varReturnValue;
    hres = pOutParams->Get(_bstr_t(L"ReturnValue"), 0, 
        &varReturnValue, NULL, 0);


    // Clean up
    //--------------------------
    VariantClear(&varCommand);
    VariantClear(&varReturnValue);
    SysFreeString(ClassName);
    SysFreeString(MethodName);
    pClass->Release();
    pClassInstance->Release();
    pInParamsDefinition->Release();
    pOutParams->Release();
    pLoc->Release();
    pSvc->Release();
    CoUninitialize();
    return 0;
}
```



 

 
