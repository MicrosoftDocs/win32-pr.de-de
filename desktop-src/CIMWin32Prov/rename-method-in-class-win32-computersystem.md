---
description: Benennt einen Computer um.
ms.assetid: 9d338ebe-caf0-42c4-995f-fd750e5664df
ms.tgt_platform: multiple
title: Rename-Methode der Win32_ComputerSystem-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2ca60021c921e47de3c7afd5b8ee0bb2ea5e6d12
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041339"
---
# <a name="rename-method-of-the-win32_computersystem-class"></a>Rename-Methode der Win32 \_ Computersystem-Klasse

Die **Rename** -Methode benennt einen Computer um.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 Rename(
  [in] string Name,
  [in] string Password,
  [in] string UserName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Name* \[ in\]
</dt> <dd>

Neuer Computername. Der Wert dieses Parameters darf keine Steuerzeichen, führende oder nachfolgende Leerzeichen oder eines der folgenden Zeichen enthalten:/ \\ \\ \[ \] .

</dd> <dt>

*Kennwort* \[ in\]
</dt> <dd>

Kennwort, das beim Herstellen einer Verbindung mit dem Domänen Controller verwendet werden soll, wenn der Parameter *username* einen Kontonamen angibt Andernfalls muss dieser Parameter **null** sein. Weitere Informationen zu *Kennwort* -und *username* -Parametern finden Sie im Abschnitt "Hinweise" in diesem Thema.

</dd> <dt>

*Benutzername* \[ in\]
</dt> <dd>

Zeichenfolge, die den Kontonamen angibt, der beim Herstellen einer Verbindung mit dem Domänen Controller verwendet wird. Die Zeichenfolge muss auf **null** enden und einen Domänen-NetBIOS-Namen und ein Benutzerkonto angeben, z. b. "Domänen Name \\ username" oder " someone@domainname.com ", ein Benutzer Prinzipal Name (User Principal Name, UPN). Wenn der **username** -Parameter **null** ist, verwendet WMI den Kontext des Aufrufers. Weitere Informationen zu *Kennwort* -und *username* -Parametern finden Sie im Abschnitt "Hinweise" in diesem Thema.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 (null) zurück. Ein Rückgabewert ungleich NULL weist auf einen Fehler hin. Wenn der Vorgang erfolgreich ist, ist ein Neustart erforderlich. Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Erfolg** (0)
</dt> <dt>

**Sonstige** (1 4294967295)
</dt> </dl>

## <a name="remarks"></a>Bemerkungen

Sie können die **Umbenennungs** Methode zum Umbenennen eines Computers verwenden, wenn Sie ein Mitglied der lokalen Administrator Gruppe sind. Die Methode kann jedoch nicht Remote für Domänen Computer verwendet werden.

Wenn die Parameter " *Password* " und " *username* " angegeben werden, muss für die Verbindung mit WMI die Authentifizierungs Ebene " **\_ \_ \_ \_ Pkt- \_ Datenschutz für RPC-C-authn-Ebene** (**wbemauthenticationlevelpktprivacy** for Script and Visual Basic (VB))" verwendet werden

Zum Herstellen einer Verbindung mit einem Remote Computer und zum Angeben von Anmelde Informationen verwenden Sie die Serverlocatorpunkt-Objekt Verbindung, die den Wert IWbemLocator für C++ und den Austausch von "Swap" und "vb" hat. Verwenden Sie die monikerverbindung nicht.

Zum Herstellen einer Verbindung mit einem lokalen Computer ist es nicht möglich, ein Kennwort oder eine Authentifizierungs Stelle anzugeben, z. b. Kerberos. Sie können nur das Kennwort und die Autorität in Verbindungen mit Remote Computern angeben.

Wenn die Authentifizierungs Stufe zu niedrig ist, wenn ein *Kennwort* und ein *Benutzername* angegeben werden, gibt WMI den **erforderlichen WBEM \_ E- \_ \_ Verbindungs \_** Fehler für C/C++ und **wbemErrEncryptedConnectionRequired** für Skript und VB zurück.

Weitere Informationen finden Sie unter [**austauschen von " \_ ConnectServer",**](/windows/desktop/WmiSdk/swbemlocator-connectserver)"[**IWBEMLocator:: ConnectServer**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemlocator-connectserver)" und [Erstellen einer Monikerzeichenfolge](/windows/desktop/WmiSdk/constructing-a-moniker-string).

## <a name="examples"></a>Beispiele

Das folgende Skript zeigt, wie Sie einen lokalen Computer umbenennen.


```VB
Name = "name"
Password = "password"
Username = "username"

Set objWMIService = GetObject("Winmgmts:root\cimv2")

' Call always gets only one Win32_ComputerSystem object.
For Each objComputer in _
    objWMIService.InstancesOf("Win32_ComputerSystem")

        Return = objComputer.rename(Name,Password,Username)
        If Return <> 0 Then
           WScript.Echo "Rename failed. Error = " & Err.Number
        Else
           WScript.Echo "Rename succeeded." & _
               " Reboot for new name to go into effect"
        End If

Next
```



Im folgenden C++-Codebeispiel wird ein Computersystem umbenannt.


```C++
int set_computer_name(const string &newname/*, const string &username, const string &password*/)
{
 HRESULT hres;


// Step 1: --------------------------------------------------
 // Initialize COM. ------------------------------------------


hres = CoInitializeEx(0, COINIT_MULTITHREADED); 
 if (FAILED(hres))
 {
 cout << "Failed to initialize COM library. Error code = 0x" 
 << hex << hres << endl;
 return 1; // Program has failed.
 }


// Step 2: --------------------------------------------------
 // Set general COM security levels --------------------------
 // Note: If you are using Windows 2000, you need to specify -
 // the default authentication credentials for a user by using
 // a SOLE_AUTHENTICATION_LIST structure in the pAuthList ----
 // parameter of CoInitializeSecurity ------------------------


hres = CoInitializeSecurity(
 NULL, 
 -1, // COM authentication
 NULL, // Authentication services
 NULL, // Reserved
 RPC_C_AUTHN_LEVEL_DEFAULT, // Default authentication 
 RPC_C_IMP_LEVEL_IMPERSONATE, // Default Impersonation 
 NULL, // Authentication info
 EOAC_NONE, // Additional capabilities 
 NULL // Reserved
 );




 if (FAILED(hres))
 {
 cout << "Failed to initialize security. Error code = 0x" 
 << hex << hres << endl;
 CoUninitialize();
 return 1; // Program has failed.
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
 return 1; // Program has failed.
 }


// Step 4: -----------------------------------------------------
 // Connect to WMI through the IWbemLocator::ConnectServer method


IWbemServices *pSvc = NULL;

 // Connect to the root\cimv2 namespace with
 // the current user and obtain pointer pSvc
 // to make IWbemServices calls.
 hres = pLoc->ConnectServer(
 _bstr_t(L"ROOT\\CIMV2"), // Object path of WMI namespace
 NULL, // User name. NULL = current user
 NULL, // User password. NULL = current
 0, // Locale. NULL indicates current
 NULL, // Security flags.
 0, // Authority (e.g. Kerberos)
 0, // Context object 
 &pSvc // pointer to IWbemServices proxy
 );

 if (FAILED(hres))
 {
 cout << "Could not connect. Error code = 0x" 
 << hex << hres << endl;
 pLoc->Release(); 
 CoUninitialize();
 return 1; // Program has failed.
 }


/*cout << "Connected to ROOT\\CIMV2 WMI namespace" << endl;*/




 // Step 5: --------------------------------------------------
 // Set security levels on the proxy -------------------------


hres = CoSetProxyBlanket(
 pSvc, // Indicates the proxy to set
 RPC_C_AUTHN_WINNT, // RPC_C_AUTHN_xxx
 RPC_C_AUTHZ_NONE, // RPC_C_AUTHZ_xxx
 NULL, // Server principal name 
 RPC_C_AUTHN_LEVEL_CALL, // RPC_C_AUTHN_LEVEL_xxx 
 RPC_C_IMP_LEVEL_IMPERSONATE, // RPC_C_IMP_LEVEL_xxx
 NULL, // client identity
 EOAC_NONE // proxy capabilities 
 );


if (FAILED(hres))
 {
 cout << "Could not set proxy blanket. Error code = 0x" 
 << hex << hres << endl;
 pSvc->Release();
 pLoc->Release(); 
 CoUninitialize();
 return 1; // Program has failed.
 }


// Step 6: --------------------------------------------------
 // Use the IWbemServices pointer to make requests of WMI ----


// For example, get the name of the operating system
 IEnumWbemClassObject* pEnumerator = NULL;
 hres = pSvc->ExecQuery(
 bstr_t("WQL"), 
 bstr_t("SELECT * FROM Win32_ComputerSystem"),
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
 return 1; // Program has failed.
 }


// Step 7: -------------------------------------------------
 // Get the data from the query in step 6 -------------------

 IWbemClassObject *pclsObj;
 ULONG uReturn = 0;

 while (pEnumerator)
 {
 HRESULT hr = pEnumerator->Next(WBEM_INFINITE, 1, 
 &pclsObj, &uReturn);


if(0 == uReturn)
 {
 break;
 }


// set up to call the Win32_ComputerSystem::Rename method
 BSTR MethodName = SysAllocString(L"Rename");
 BSTR ClassName = SysAllocString(L"Win32_ComputerSystem");


IWbemClassObject* pClass = NULL;
 hres = pSvc->GetObject(ClassName, 0, NULL, &pClass, NULL);


IWbemClassObject* pInParamsDefinition = NULL;
 hres = pClass->GetMethod(MethodName, 0, 
 &pInParamsDefinition, NULL);


IWbemClassObject* pClassInstance = NULL;
 hres = pInParamsDefinition->SpawnInstance(0, &pClassInstance);


// Create the values for the in parameters
 wstring val;
 BSTR NewName;
 val.assign(newname.begin(), newname.end());
 NewName = SysAllocString(val.c_str());


VARIANT varName;
 varName.vt = VT_BSTR;
 varName.bstrVal = NewName;


// Store the value for the in parameters
 hres = pClassInstance->Put(L"Name", 0,
 &varName, 0);
 wprintf(L"Set computer name to %s\n", V_BSTR(&varName));


VARIANT var;
 CIMTYPE pType;
 LONG pFlavor;
 pclsObj->Get(L"__PATH",0,&var,&pType,&pFlavor);


// Execute Method
 IWbemClassObject* pOutParams = NULL;
 hres = pSvc->ExecMethod(var.bstrVal, MethodName, 0,
 NULL, pClassInstance, &pOutParams, NULL);


if (FAILED(hres))
 {
 cout << "Could not execute method. Error code = 0x" 
 << hex << hres << endl;
 VariantClear(&varName);
 SysFreeString(ClassName);
 SysFreeString(MethodName);
 SysFreeString(NewName);
 pClass->Release();
 pInParamsDefinition->Release();
 pOutParams->Release();
 return 1; // Program has failed.
 }


// To see what the method returned,
 // use the following code. The return value will
 // be in &varReturnValue
 VARIANT varReturnValue;
 hres = pOutParams->Get(_bstr_t(L"ReturnValue"), 0, 
 &varReturnValue, NULL, 0);




 // Clean up
 //--------------------------
 VariantClear(&varName);
 VariantClear(&varReturnValue);
 SysFreeString(ClassName);
 SysFreeString(MethodName);
 SysFreeString(NewName);
 pClass->Release();
 pInParamsDefinition->Release();
 pOutParams->Release();
 return 0;


}


// Cleanup
 // ========

 pSvc->Release();
 pLoc->Release();
 pEnumerator->Release();
 pclsObj->Release();
 CoUninitialize();


return 0; // Program successfully completed.
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ Computersystem**](win32-computersystem.md)
</dt> <dt>

[WMI-Tasks: Konten und Domänen](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> </dl>

 

