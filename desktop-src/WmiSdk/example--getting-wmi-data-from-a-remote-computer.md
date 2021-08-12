---
description: Sie können die Prozedur- und Codebeispiele in diesem Thema verwenden, um eine vollständige WMI-Clientanwendung zu erstellen, die die COM-Initialisierung ausführt, eine Verbindung mit WMI auf einem Remotecomputer herstellt, Daten semisynchron erhält und dann bereinigt.
ms.assetid: 30e65b9e-9372-46d1-843a-bda0d6ec1c69
ms.tgt_platform: multiple
title: 'Beispiel: Abrufen von WMI-Daten von einem Remotecomputer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 722247d9b58c9fc27c5fac63a97f86d0c155faa92e41fc68506c5d280d0b040a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118556623"
---
# <a name="example-getting-wmi-data-from-a-remote-computer"></a>Beispiel: Abrufen von WMI-Daten von einem Remotecomputer

Sie können die Prozedur- und Codebeispiele in diesem Thema verwenden, um eine vollständige WMI-Clientanwendung zu erstellen, die die COM-Initialisierung ausführt, eine Verbindung mit WMI auf einem Remotecomputer herstellt, Daten semisynchron erhält und dann bereinigt. Weitere Informationen zum Abrufen von Daten vom lokalen Computer finden Sie unter [Beispiel: Abrufen von WMI-Daten vom lokalen Computer.](example--getting-wmi-data-from-the-local-computer.md) Weitere Informationen zum asynchronen Abrufen der Daten finden Sie unter [Beispiel: Asynchrones Abrufen von WMI-Daten vom lokalen Computer.](example--getting-wmi-data-from-the-local-computer-asynchronously.md)

> [!Note]  
> Wenn Sie versuchen, eine Verbindung mit einem Remotecomputer herzustellen, lesen Sie die Informationen unter Herstellen einer[Verbindung mit WMI Remotely](connecting-to-wmi-remotely-starting-with-vista.md).

 

Das folgende Verfahren zeigt, wie die WMI-Anwendung ausgeführt wird. Die Schritte 1 bis 5 enthalten alle Schritte, die zum Einrichten und Herstellen einer Verbindung mit WMI erforderlich sind. In den Schritten 6 und 7 werden Daten abgefragt und empfangen.

**So erhalten Sie WMI-Daten von einem Remotecomputer**

1.  Initialisieren Sie COM-Parameter mit einem Aufruf von [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).

    Weitere Informationen finden Sie unter [Initialisieren von COM für eine WMI-Anwendung.](initializing-com-for-a-wmi-application.md)

2.  Initialisieren Sie die COM-Prozesssicherheit, indem [**Sie CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)aufrufen.

    Weitere Informationen finden Sie unter [Festlegen der Standardprozesssicherheitsstufe mit C++](setting-the-default-process-security-level-using-c-.md).

3.  Rufen Sie den anfänglichen Locator für WMI ab, indem [**Sie CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)aufrufen.

    Weitere Informationen finden Sie unter [Erstellen einer Verbindung mit einem WMI-Namespace.](creating-a-connection-to-a-wmi-namespace.md)

4.  Rufen Sie einen Zeiger auf [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) für den \\ \\ \\ Cimv2-Stammnamespace auf einem Remotecomputer ab, indem [**Sie IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)aufrufen. Wenn Sie eine Verbindung mit einem Remotecomputer herstellen, müssen Sie den Computernamen, die Domäne, den Benutzernamen und das Kennwort des Remotecomputers kennen, mit dem Sie eine Verbindung herstellen. Diese Attribute werden alle an die **IWbemLocator::ConnectServer-Methode** übergeben. Stellen Sie außerdem sicher, dass der Benutzername auf dem Computer, der versucht, eine Verbindung mit dem Remotecomputer herzustellen, über die richtigen Zugriffsberechtigungen auf dem Remotecomputer verfügt. Weitere Informationen finden Sie unter [Herstellen einer Verbindung über Windows Firewall.](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista) Informationen zum Herstellen einer Verbindung mit dem lokalen Computer finden Sie unter [Beispiel: Abrufen von WMI-Daten vom lokalen Computer](example--getting-wmi-data-from-the-local-computer.md) und [Erstellen einer Verbindung mit einem WMI-Namespace.](creating-a-connection-to-a-wmi-namespace.md)

    Bei der Verarbeitung von Benutzernamen und Kennwörtern wird empfohlen, dass der Benutzer zur Eingabe der Informationen aufgefordert wird, die Informationen verwendet und die Informationen dann löscht, damit die Wahrscheinlichkeit geringer ist, dass die Informationen von einem nicht autorisierten Benutzer abgefangen werden. Schritt 4 im folgenden Beispielcode verwendet [**CredUIPromptForCredentials,**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) um den Benutzernamen und das Kennwort abzurufen, und verwendet dann [**SecureZeroMemory,**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) um die Informationen zu entfernen, nachdem sie in [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)verwendet wurden. Weitere Informationen finden Sie unter [Handling Passwords (Behandeln von Kennwörtern)](/windows/desktop/SecBP/handling-passwords) und [Asking the User for Credentials (Fragen des Benutzers nach Anmeldeinformationen)](/windows/desktop/SecBP/asking-the-user-for-credentials) auf MSDN.

5.  Erstellen Sie eine [COAUTHIDENTITY-Struktur,](/windows/win32/api/wtypesbase/ns-wtypesbase-coauthidentity) um Anmeldeinformationen zum Festlegen der Proxysicherheit bereitzustellen.
6.  Legen Sie [**die IWbemServices-Proxysicherheit**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) fest, damit der WMI-Dienst die Identität des Clients annehmen kann, indem [**Er coSetProxyBlanket aufruft.**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)

    Weitere Informationen finden Sie unter [Festlegen der Sicherheitsstufen für eine WMI-Verbindung.](setting-the-security-levels-on-a-wmi-connection.md)

7.  Verwenden Sie den [**IWbemServices-Zeiger,**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) um WMI-Anforderungen zu stellen. Eine Abfrage wird ausgeführt, um den Namen des Betriebssystems und die Menge des freien physischen Arbeitsspeichers durch Aufrufen von [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)abzurufen.

    Die folgende WQL-Abfrage ist eines der Methodenargumente.

    `SELECT * FROM Win32_OperatingSystem`

    Das Ergebnis dieser Abfrage wird in einem [**IEnumWbemClassObject-Zeiger**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) gespeichert. Dadurch können die Datenobjekte aus der Abfrage halbsynchron mit der **IEnumWbemClassObject-Schnittstelle** abgerufen werden. Weitere Informationen finden Sie unter [Aufzählen von WMI.](enumerating-wmi.md) Informationen zum asynchronen Abrufen der Daten finden Sie unter [Beispiel: Asynchrones Abrufen von WMI-Daten vom lokalen Computer.](example--getting-wmi-data-from-the-local-computer-asynchronously.md)

    Weitere Informationen zum Senden von WMI-Anforderungen finden Sie unter Bearbeiten von [Klassen- und Instanzinformationen,](manipulating-class-and-instance-information.md) [Abfragen von WMI](querying-wmi.md)und [Aufrufen einer Methode.](calling-a-method.md)

8.  Legen Sie [**die IEnumWbemClassObject-Enumeratorproxysicherheit**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) fest. Stellen Sie sicher, dass Sie die Anmeldeinformationen aus dem Arbeitsspeicher löschen, nachdem Sie sie verwendet haben.

    Weitere Informationen finden Sie unter [Festlegen der Sicherheit für IWbemServices und andere Proxys.](setting-the-security-on-iwbemservices-and-other-proxies.md)

9.  Abrufen und Anzeigen der Daten aus der WQL-Abfrage. Der [**IEnumWbemClassObject-Zeiger**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) ist mit den Datenobjekten verknüpft, die von der Abfrage zurückgegeben wurden, und die Datenobjekte können mit der [**IEnumWbemClassObject::Next-Methode**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) abgerufen werden. Diese Methode verknüpft die Datenobjekte mit einem [**IWbemClassObject-Zeiger,**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) der an die -Methode übergeben wird. Verwenden Sie die [**IWbemClassObject::Get-Methode,**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) um die gewünschten Informationen aus den Datenobjekten abzurufen.

    Das folgende Codebeispiel wird verwendet, um die `Name` -Eigenschaft aus dem Datenobjekt abzurufen, das den Namen des Betriebssystems bereitstellt.

    ```C++
    VARIANT vtProp;

    // Get the value of the Name property
    hr = pclsObj->Get(L"Name", 0, &vtProp, 0, 0);
    wcout << " OS Name : " << vtProp.bstrVal << endl;
    ```

    

    Sobald der Wert der `Name` Eigenschaft in der [**VARIANT-Variablen**](/windows/win32/api/oaidl/ns-oaidl-variant) gespeichert `vtProp` ist, kann er dem Benutzer angezeigt werden.

    Das folgende Codebeispiel zeigt, wie die [**VARIANT-Variable**](/windows/win32/api/oaidl/ns-oaidl-variant) erneut verwendet werden kann, um den Wert der Menge des freien physischen Arbeitsspeichers zu speichern und anzuzeigen.

    ```C++
    hr = pclsObj->Get(L"FreePhysicalMemory",
        0, &vtProp, 0, 0);
    wcout << " Free physical memory (in kilobytes): "
        << vtProp.uintVal << endl;
    ```

    

    Weitere Informationen finden Sie unter [Aufzählen von WMI.](enumerating-wmi.md)

Das folgende Codebeispiel zeigt, wie WMI-Daten semisynchron von einem Remotecomputer abrufen.


```C++
#define _WIN32_DCOM
#define UNICODE
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
#pragma comment(lib, "credui.lib")
#pragma comment(lib, "comsuppw.lib")
#include <wincred.h>
#include <strsafe.h>

int __cdecl main(int argc, char **argv)
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
        RPC_C_IMP_LEVEL_IDENTIFY,    // Default Impersonation  
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

    // Get the user name and password for the remote computer
    CREDUI_INFO cui;
    bool useToken = false;
    bool useNTLM = true;
    wchar_t pszName[CREDUI_MAX_USERNAME_LENGTH+1] = {0};
    wchar_t pszPwd[CREDUI_MAX_PASSWORD_LENGTH+1] = {0};
    wchar_t pszDomain[CREDUI_MAX_USERNAME_LENGTH+1];
    wchar_t pszUserName[CREDUI_MAX_USERNAME_LENGTH+1];
    wchar_t pszAuthority[CREDUI_MAX_USERNAME_LENGTH+1];
    BOOL fSave;
    DWORD dwErr;

    memset(&cui,0,sizeof(CREDUI_INFO));
    cui.cbSize = sizeof(CREDUI_INFO);
    cui.hwndParent = NULL;
    // Ensure that MessageText and CaptionText identify
    // what credentials to use and which application requires them.
    cui.pszMessageText = TEXT("Press cancel to use process token");
    cui.pszCaptionText = TEXT("Enter Account Information");
    cui.hbmBanner = NULL;
    fSave = FALSE;

    dwErr = CredUIPromptForCredentials( 
        &cui,                             // CREDUI_INFO structure
        TEXT(""),                         // Target for credentials
        NULL,                             // Reserved
        0,                                // Reason
        pszName,                          // User name
        CREDUI_MAX_USERNAME_LENGTH+1,     // Max number for user name
        pszPwd,                           // Password
        CREDUI_MAX_PASSWORD_LENGTH+1,     // Max number for password
        &fSave,                           // State of save check box
        CREDUI_FLAGS_GENERIC_CREDENTIALS |// flags
        CREDUI_FLAGS_ALWAYS_SHOW_UI |
        CREDUI_FLAGS_DO_NOT_PERSIST);  

    if(dwErr == ERROR_CANCELLED)
    {
        useToken = true;
    }
    else if (dwErr)
    {
        cout << "Did not get credentials " << dwErr << endl;
        pLoc->Release();     
        CoUninitialize();
        return 1;      
    }

    // change the computerName strings below to the full computer name
    // of the remote computer
    if(!useNTLM)
    {
        StringCchPrintf(pszAuthority, CREDUI_MAX_USERNAME_LENGTH+1, L"kERBEROS:%s", L"COMPUTERNAME");
    }

    // Connect to the remote root\cimv2 namespace
    // and obtain pointer pSvc to make IWbemServices calls.
    //---------------------------------------------------------
   
    hres = pLoc->ConnectServer(
        _bstr_t(L"\\\\COMPUTERNAME\\root\\cimv2"),
        _bstr_t(useToken?NULL:pszName),    // User name
        _bstr_t(useToken?NULL:pszPwd),     // User password
        NULL,                              // Locale             
        NULL,                              // Security flags
        _bstr_t(useNTLM?NULL:pszAuthority),// Authority        
        NULL,                              // Context object 
        &pSvc                              // IWbemServices proxy
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


    // step 5: --------------------------------------------------
    // Create COAUTHIDENTITY that can be used for setting security on proxy

    COAUTHIDENTITY *userAcct =  NULL ;
    COAUTHIDENTITY authIdent;

    if( !useToken )
    {
        memset(&authIdent, 0, sizeof(COAUTHIDENTITY));
        authIdent.PasswordLength = wcslen (pszPwd);
        authIdent.Password = (USHORT*)pszPwd;

        LPWSTR slash = wcschr (pszName, L'\\');
        if( slash == NULL )
        {
            cout << "Could not create Auth identity. No domain specified\n" ;
            pSvc->Release();
            pLoc->Release();     
            CoUninitialize();
            return 1;               // Program has failed.
        }

        StringCchCopy(pszUserName, CREDUI_MAX_USERNAME_LENGTH+1, slash+1);
        authIdent.User = (USHORT*)pszUserName;
        authIdent.UserLength = wcslen(pszUserName);

        StringCchCopyN(pszDomain, CREDUI_MAX_USERNAME_LENGTH+1, pszName, slash - pszName);
        authIdent.Domain = (USHORT*)pszDomain;
        authIdent.DomainLength = slash - pszName;
        authIdent.Flags = SEC_WINNT_AUTH_IDENTITY_UNICODE;

        userAcct = &authIdent;

    }

    // Step 6: --------------------------------------------------
    // Set security levels on a WMI connection ------------------

    hres = CoSetProxyBlanket(
       pSvc,                           // Indicates the proxy to set
       RPC_C_AUTHN_DEFAULT,            // RPC_C_AUTHN_xxx
       RPC_C_AUTHZ_DEFAULT,            // RPC_C_AUTHZ_xxx
       COLE_DEFAULT_PRINCIPAL,         // Server principal name 
       RPC_C_AUTHN_LEVEL_PKT_PRIVACY,  // RPC_C_AUTHN_LEVEL_xxx 
       RPC_C_IMP_LEVEL_IMPERSONATE,    // RPC_C_IMP_LEVEL_xxx
       userAcct,                       // client identity
       EOAC_NONE                       // proxy capabilities 
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

    // Step 7: --------------------------------------------------
    // Use the IWbemServices pointer to make requests of WMI ----

    // For example, get the name of the operating system
    IEnumWbemClassObject* pEnumerator = NULL;
    hres = pSvc->ExecQuery(
        bstr_t("WQL"), 
        bstr_t("Select * from Win32_OperatingSystem"),
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

    // Step 8: -------------------------------------------------
    // Secure the enumerator proxy
    hres = CoSetProxyBlanket(
        pEnumerator,                    // Indicates the proxy to set
        RPC_C_AUTHN_DEFAULT,            // RPC_C_AUTHN_xxx
        RPC_C_AUTHZ_DEFAULT,            // RPC_C_AUTHZ_xxx
        COLE_DEFAULT_PRINCIPAL,         // Server principal name 
        RPC_C_AUTHN_LEVEL_PKT_PRIVACY,  // RPC_C_AUTHN_LEVEL_xxx 
        RPC_C_IMP_LEVEL_IMPERSONATE,    // RPC_C_IMP_LEVEL_xxx
        userAcct,                       // client identity
        EOAC_NONE                       // proxy capabilities 
        );

    if (FAILED(hres))
    {
        cout << "Could not set proxy blanket on enumerator. Error code = 0x" 
             << hex << hres << endl;
        pEnumerator->Release();
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // When you have finished using the credentials,
    // erase them from memory.
    SecureZeroMemory(pszName, sizeof(pszName));
    SecureZeroMemory(pszPwd, sizeof(pszPwd));
    SecureZeroMemory(pszUserName, sizeof(pszUserName));
    SecureZeroMemory(pszDomain, sizeof(pszDomain));


    // Step 9: -------------------------------------------------
    // Get the data from the query in step 7 -------------------
 
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

        // Get the value of the FreePhysicalMemory property
        hr = pclsObj->Get(L"FreePhysicalMemory",
            0, &vtProp, 0, 0);
        wcout << " Free physical memory (in kilobytes): "
            << vtProp.uintVal << endl;
        VariantClear(&vtProp);

        pclsObj->Release();
        pclsObj = NULL;
    }

    // Cleanup
    // ========
    
    pSvc->Release();
    pLoc->Release();
    pEnumerator->Release();
    if( pclsObj )
    {
        pclsObj->Release();
    }
    
    CoUninitialize();

    return 0;   // Program successfully completed.
    
}
```



 

 
