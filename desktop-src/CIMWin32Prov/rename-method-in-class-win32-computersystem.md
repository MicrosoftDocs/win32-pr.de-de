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
# <a name="rename-method-of-the-win32_computersystem-class"></a><span data-ttu-id="895f5-103">Rename-Methode der Win32 \_ Computersystem-Klasse</span><span class="sxs-lookup"><span data-stu-id="895f5-103">Rename method of the Win32\_ComputerSystem class</span></span>

<span data-ttu-id="895f5-104">Die **Rename** -Methode benennt einen Computer um.</span><span class="sxs-lookup"><span data-stu-id="895f5-104">The **Rename** method renames a computer.</span></span>

<span data-ttu-id="895f5-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="895f5-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="895f5-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="895f5-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="895f5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="895f5-107">Syntax</span></span>


```mof
uint32 Rename(
  [in] string Name,
  [in] string Password,
  [in] string UserName
);
```



## <a name="parameters"></a><span data-ttu-id="895f5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="895f5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="895f5-109">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="895f5-109">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="895f5-110">Neuer Computername.</span><span class="sxs-lookup"><span data-stu-id="895f5-110">New computer name.</span></span> <span data-ttu-id="895f5-111">Der Wert dieses Parameters darf keine Steuerzeichen, führende oder nachfolgende Leerzeichen oder eines der folgenden Zeichen enthalten:/ \\ \\ \[ \] .</span><span class="sxs-lookup"><span data-stu-id="895f5-111">The value of this parameter cannot include control characters, leading or trailing spaces, or any of the following characters: / \\\\ \[ \].</span></span>

</dd> <dt>

<span data-ttu-id="895f5-112">*Kennwort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="895f5-112">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="895f5-113">Kennwort, das beim Herstellen einer Verbindung mit dem Domänen Controller verwendet werden soll, wenn der Parameter *username* einen Kontonamen angibt</span><span class="sxs-lookup"><span data-stu-id="895f5-113">Password to use when connecting to the domain controller if the *UserName* parameter specifies an account name.</span></span> <span data-ttu-id="895f5-114">Andernfalls muss dieser Parameter **null** sein.</span><span class="sxs-lookup"><span data-stu-id="895f5-114">Otherwise, this parameter must be **NULL**.</span></span> <span data-ttu-id="895f5-115">Weitere Informationen zu *Kennwort* -und *username* -Parametern finden Sie im Abschnitt "Hinweise" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="895f5-115">See the Remarks section of this topic for more information about *Password* and *UserName* parameters.</span></span>

</dd> <dt>

<span data-ttu-id="895f5-116">*Benutzername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="895f5-116">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="895f5-117">Zeichenfolge, die den Kontonamen angibt, der beim Herstellen einer Verbindung mit dem Domänen Controller verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="895f5-117">String that specifies the account name to use when connecting to the domain controller.</span></span> <span data-ttu-id="895f5-118">Die Zeichenfolge muss auf **null** enden und einen Domänen-NetBIOS-Namen und ein Benutzerkonto angeben, z. b. "Domänen Name \\ username" oder " someone@domainname.com ", ein Benutzer Prinzipal Name (User Principal Name, UPN).</span><span class="sxs-lookup"><span data-stu-id="895f5-118">The string must be **null**-terminated, and must specify a domain NetBIOS name and user account for example, "DOMAINNAME\\username" or "someone@domainname.com", which is a user principal name (UPN).</span></span> <span data-ttu-id="895f5-119">Wenn der **username** -Parameter **null** ist, verwendet WMI den Kontext des Aufrufers.</span><span class="sxs-lookup"><span data-stu-id="895f5-119">If the **UserName** parameter is **NULL**, WMI uses the context of the caller.</span></span> <span data-ttu-id="895f5-120">Weitere Informationen zu *Kennwort* -und *username* -Parametern finden Sie im Abschnitt "Hinweise" in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="895f5-120">See the Remarks section of this topic for more information about *Password* and *UserName* parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="895f5-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="895f5-121">Return value</span></span>

<span data-ttu-id="895f5-122">Gibt bei Erfolg 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="895f5-122">Returns a 0 (zero) if successful.</span></span> <span data-ttu-id="895f5-123">Ein Rückgabewert ungleich NULL weist auf einen Fehler hin.</span><span class="sxs-lookup"><span data-stu-id="895f5-123">A nonzero return value indicates an error.</span></span> <span data-ttu-id="895f5-124">Wenn der Vorgang erfolgreich ist, ist ein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="895f5-124">If successful, a reboot is required.</span></span> <span data-ttu-id="895f5-125">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="895f5-125">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="895f5-126">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="895f5-126">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="895f5-127">**Erfolg** (0)</span><span class="sxs-lookup"><span data-stu-id="895f5-127">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="895f5-128">**Sonstige** (1 4294967295)</span><span class="sxs-lookup"><span data-stu-id="895f5-128">**Other** (1 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="895f5-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="895f5-129">Remarks</span></span>

<span data-ttu-id="895f5-130">Sie können die **Umbenennungs** Methode zum Umbenennen eines Computers verwenden, wenn Sie ein Mitglied der lokalen Administrator Gruppe sind.</span><span class="sxs-lookup"><span data-stu-id="895f5-130">You can use the **Rename** method to rename a computer if you are a member of the local administrator group.</span></span> <span data-ttu-id="895f5-131">Die Methode kann jedoch nicht Remote für Domänen Computer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="895f5-131">However, you cannot use the method remotely for domain computers.</span></span>

<span data-ttu-id="895f5-132">Wenn die Parameter " *Password* " und " *username* " angegeben werden, muss für die Verbindung mit WMI die Authentifizierungs Ebene " **\_ \_ \_ \_ Pkt- \_ Datenschutz für RPC-C-authn-Ebene** (**wbemauthenticationlevelpktprivacy** for Script and Visual Basic (VB))" verwendet werden</span><span class="sxs-lookup"><span data-stu-id="895f5-132">If the *Password* and *UserName* parameters are specified, the connection to WMI must use the **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** (**wbemAuthenticationLevelPktPrivacy** for script and Visual Basic (VB)) authentication level.</span></span>

<span data-ttu-id="895f5-133">Zum Herstellen einer Verbindung mit einem Remote Computer und zum Angeben von Anmelde Informationen verwenden Sie die Serverlocatorpunkt-Objekt Verbindung, die den Wert IWbemLocator für C++ und den Austausch von "Swap" und "vb" hat.</span><span class="sxs-lookup"><span data-stu-id="895f5-133">To connect to a remote computer and specify credentials, use the locator object connection, which is IWbemLocator for C++, and SWbemLocator for script and VB.</span></span> <span data-ttu-id="895f5-134">Verwenden Sie die monikerverbindung nicht.</span><span class="sxs-lookup"><span data-stu-id="895f5-134">Do not use the moniker connection.</span></span>

<span data-ttu-id="895f5-135">Zum Herstellen einer Verbindung mit einem lokalen Computer ist es nicht möglich, ein Kennwort oder eine Authentifizierungs Stelle anzugeben, z. b. Kerberos.</span><span class="sxs-lookup"><span data-stu-id="895f5-135">To connect to a local computer, you cannot specify a password or an authentication authority, such as Kerberos.</span></span> <span data-ttu-id="895f5-136">Sie können nur das Kennwort und die Autorität in Verbindungen mit Remote Computern angeben.</span><span class="sxs-lookup"><span data-stu-id="895f5-136">You can only specify the password and authority in connections to remote computers.</span></span>

<span data-ttu-id="895f5-137">Wenn die Authentifizierungs Stufe zu niedrig ist, wenn ein *Kennwort* und ein *Benutzername* angegeben werden, gibt WMI den **erforderlichen WBEM \_ E- \_ \_ Verbindungs \_** Fehler für C/C++ und **wbemErrEncryptedConnectionRequired** für Skript und VB zurück.</span><span class="sxs-lookup"><span data-stu-id="895f5-137">If the authentication level is too low when a *Password* and *UserName* are specified, then WMI returns the **WBEM\_E\_ENCRYPTED\_CONNECTION\_REQUIRED** error for C/C++, and **wbemErrEncryptedConnectionRequired** for script and VB.</span></span>

<span data-ttu-id="895f5-138">Weitere Informationen finden Sie unter [**austauschen von " \_ ConnectServer",**](/windows/desktop/WmiSdk/swbemlocator-connectserver)"[**IWBEMLocator:: ConnectServer**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemlocator-connectserver)" und [Erstellen einer Monikerzeichenfolge](/windows/desktop/WmiSdk/constructing-a-moniker-string).</span><span class="sxs-lookup"><span data-stu-id="895f5-138">For more information, see [**SWbemLocator\_ConnectServer,**](/windows/desktop/WmiSdk/swbemlocator-connectserver)[**IWbemLocator::ConnectServer**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemlocator-connectserver), and [Constructing a Moniker String](/windows/desktop/WmiSdk/constructing-a-moniker-string).</span></span>

## <a name="examples"></a><span data-ttu-id="895f5-139">Beispiele</span><span class="sxs-lookup"><span data-stu-id="895f5-139">Examples</span></span>

<span data-ttu-id="895f5-140">Das folgende Skript zeigt, wie Sie einen lokalen Computer umbenennen.</span><span class="sxs-lookup"><span data-stu-id="895f5-140">The following script shows you how to rename a local computer.</span></span>


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



<span data-ttu-id="895f5-141">Im folgenden C++-Codebeispiel wird ein Computersystem umbenannt.</span><span class="sxs-lookup"><span data-stu-id="895f5-141">The following C++ code sample renames a computer system.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="895f5-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="895f5-142">Requirements</span></span>



| <span data-ttu-id="895f5-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="895f5-143">Requirement</span></span> | <span data-ttu-id="895f5-144">Wert</span><span class="sxs-lookup"><span data-stu-id="895f5-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="895f5-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="895f5-145">Minimum supported client</span></span><br/> | <span data-ttu-id="895f5-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="895f5-146">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="895f5-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="895f5-147">Minimum supported server</span></span><br/> | <span data-ttu-id="895f5-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="895f5-148">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="895f5-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="895f5-149">Namespace</span></span><br/>                | <span data-ttu-id="895f5-150">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="895f5-150">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="895f5-151">MOF</span><span class="sxs-lookup"><span data-stu-id="895f5-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="895f5-152"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="895f5-152"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="895f5-153">DLL</span><span class="sxs-lookup"><span data-stu-id="895f5-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="895f5-154"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="895f5-154"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="895f5-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="895f5-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="895f5-156">**Win32- \_ Computersystem**</span><span class="sxs-lookup"><span data-stu-id="895f5-156">**Win32\_ComputerSystem**</span></span>](win32-computersystem.md)
</dt> <dt>

[<span data-ttu-id="895f5-157">WMI-Tasks: Konten und Domänen</span><span class="sxs-lookup"><span data-stu-id="895f5-157">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> </dl>

 

