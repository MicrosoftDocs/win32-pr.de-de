---
description: Der Beendigungs&\# 32; Die WMI-Klassenmethode beendet einen Prozess und alle zugehörigen Threads.
ms.assetid: 6c6b27d4-cf9b-42d7-9136-42641ea56ee8
ms.tgt_platform: multiple
title: Beendigungs Methode der Win32_Process-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.Terminate
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 00300ca9656c3b732b9c294aeba9a6c626ac6e2e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958263"
---
# <a name="terminate-method-of-the-win32_process-class"></a>Beendigungs Methode der Win32- \_ Prozess Klasse

Die Methode zum **Beenden** der [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) beendet einen Prozess und alle zugehörigen Threads.

In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet. Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntax


```mof
uint32 Terminate(
  [in] uint32 Reason
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Grund* \[ in\]
</dt> <dd>

Der Exitcode für den Prozess und für alle Threads, die als Ergebnis dieses Aufrufes beendet wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Wert 0 (null) zurück, wenn der Prozess erfolgreich beendet wurde, und jede andere Zahl gibt einen Fehler an. Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Erfolgreicher Abschluss** (0)
</dt> <dt>

**Zugriff verweigert** (2)
</dt> <dt>

**Unzureichende Berechtigungen** (3)
</dt> <dt>

**Unbekannter Fehler** (8)
</dt> <dt>

Der **Pfad wurde nicht gefunden** (9).
</dt> <dt>

**Ungültiger Parameter** (21)
</dt> <dt>

**Sonstige** (22 4294967295)
</dt> </dl>

## <a name="remarks"></a>Bemerkungen

**Übersicht**

Computer Probleme sind häufig auf einen Prozess zurückzuführen, der nicht mehr erwartungsgemäß funktioniert. Beispielsweise kann es vorkommen, dass der Prozess Speicher Verluste verursacht oder nicht mehr auf Benutzereingaben reagiert. Wenn Probleme wie diese auftreten, muss der Prozess beendet werden. Obwohl dies möglicherweise wie eine einfache genug Aufgabe aussieht, kann das Beenden eines Prozesses durch verschiedene Faktoren erschwert werden:

-   Der Prozess ist möglicherweise nicht mehr auf Menüs oder Tastaturbefehle zum Schließen der Anwendung reagiert. Dadurch kann der typische Benutzer die Anwendung nicht verwerfen und den Prozess beenden.
-   Der Prozess ist möglicherweise verwaist. Beispielsweise kann ein Skript eine Instanz von Word erstellen und dann beenden, ohne diese Instanz zu zerstören. Tatsächlich wird Word weiterhin auf dem Computer ausgeführt, auch wenn keine Benutzeroberfläche sichtbar ist. Da keine Benutzeroberfläche vorhanden ist, stehen keine Menü-oder Tastaturbefehle zum Beenden des Prozesses zur Verfügung.
-   Möglicherweise wissen Sie nicht, welcher Prozess beendet werden muss. Beispielsweise kann es sein, dass Sie alle Programme beenden möchten, die eine bestimmte Arbeitsspeicher Menge überschreiten.
-   Da Sie mit dem Task-Manager nur die Prozesse beenden können, die Sie erstellt haben, können Sie einen Prozess möglicherweise nicht beenden, auch wenn Sie ein Administrator auf dem Computer sind.

Mithilfe von Skripts können Sie all diese potenziellen Hindernisse überwinden und so eine beträchtliche administrative Kontrolle über Ihre Computer gewährleisten. Wenn Sie z. b. vermuten, dass Benutzer Spiele spielen, die in Ihrer Organisation unzulässig waren, können Sie problemlos ein Skript schreiben, um eine Verbindung zu den einzelnen Computern herzustellen, festzustellen, ob das Spiel ausgeführt wird, und den Prozess sofort beenden.

**Verwenden der Beendigungs Methode**

Sie können einen Prozess beenden, indem Sie Folgendes ausführen:

-   Beenden eines Prozesses, der derzeit ausgeführt wird. Beispielsweise müssen Sie möglicherweise ein Diagnoseprogramm beenden, das auf einem Remote Computer ausgeführt wird. Wenn es keine Möglichkeit gibt, die Anwendung Remote zu steuern, können Sie einfach den Prozess für diese Anwendung beenden.
-   Verhindern, dass ein Prozess an erster Stelle ausgeführt wird. Durch die kontinuierliche Überwachung der Prozesserstellung auf einem Computer können Sie jeden Prozess ermitteln und sofort beenden, sobald er gestartet wird. Dies bietet eine Methode, um sicherzustellen, dass bestimmte Anwendungen (z. b. Programme, die große Mediendateien über das Internet herunterladen) niemals auf bestimmten Computern ausgeführt werden.

> [!Note]  
> Gruppenrichtlinie können auch verwendet werden, um die Programme einzuschränken, die auf einem Computer ausgeführt werden. Gruppenrichtlinie können jedoch nur die Programme beschränken, die entweder über das Startmenü oder Windows-Explorer ausgeführt werden. Es hat keine Auswirkung auf Programme, die mit anderen Methoden gestartet wurden, z. b. über die Befehlszeile. Im Gegensatz dazu kann WMI verhindern, dass ein Prozess ausgeführt wird, unabhängig davon, wie der Prozess gestartet wurde.

 

**Beenden eines Prozesses, den Sie nicht besitzen**

Um einen Prozess zu beenden, den Sie nicht besitzen, aktivieren **Sie die Berechtigung** "" für "". In VBScript können Sie dieses Privileg mit den folgenden Codezeilen aktivieren:


```VB
Set objLoc = createobject("wbemscripting.swbemlocator")
objLoc.Security_.privileges.addasstring "sedebugprivilege", true
```



Weitere Informationen zum Aktivieren dieser Berechtigung in C++ finden Sie unter [aktivieren und Deaktivieren von Berechtigungen in C++](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--).

## <a name="examples"></a>Beispiele

Mit dem PowerShell-Codebeispiel für das [Beenden des laufenden Vorgangs auf mehreren Servern](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) wird ein Prozess beendet, der auf einem oder mehreren Computern ausgeführt wird.

Im folgenden VBScript-Beispiel wird der Prozess beendet, in dem die Anwendungs Diagnose.exe derzeit ausgeführt wird.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcessList = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'Diagnose.exe'")
For Each objProcess in colProcessList
 objProcess.Terminate()
Next
```



Im folgenden VBScript-Beispiel wird ein temporärer Ereignisconsumer verwendet, um einen Prozess zu beenden, sobald er gestartet wird.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colMonitoredProcesses = objWMIService.ExecNotificationQuery("SELECT * FROM __InstanceCreationEvent " _
 & " WITHIN 1 WHERE TargetInstance ISA 'Win32_Process'")
i = 0
Do While i = 0
 Set objLatestProcess = colMonitoredProcesses.NextEvent
 If objLatestProcess.TargetInstance.Name = "Download.exe" Then
 objLatestProcess.TargetInstance.Terminate()
 End If
Loop
```



Im folgenden VBScript-Codebeispiel wird eine Verbindung mit einem Remote Computer hergestellt, und der Notepad.exe auf diesem Computer wird beendet.


```VB
strComputer = "FullComputerName" 
strDomain = "DOMAIN" 
strUser = InputBox("Enter user name") 
strPassword = InputBox("Enter password") 
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator") 
Set objWMIService = objSWbemLocator.ConnectServer(strComputer, _ 
    "root\CIMV2", _ 
    strUser, _ 
    strPassword, _ 
    "MS_409", _ 
    "ntlmdomain:" + strDomain) 
Set colProcessList = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'notepad.exe'")
For Each objProcess in colProcessList
    objProcess.Terminate()
Next
```



Der folgende C++-Code beendet den Notepad.exe Prozess auf dem lokalen Computer. Geben Sie ein-oder-Prozess handle (Prozess-ID) im Code an, um den Prozess zu beenden. Dieser Wert befindet sich in der Handle-Eigenschaft in der [**Win32- \_ Prozess**](win32-process.md) Klasse (die Schlüsseleigenschaft für die-Klasse). Wenn Sie einen Wert für die Handle-Eigenschaft angeben, geben Sie einen Pfad zur Instanz der-Klasse an, die Sie beenden möchten. Weitere Informationen zum Herstellen einer Verbindung mit einem Remote Computer finden Sie unter [Beispiel: erhalten von WMI-Daten von einem Remote Computer aus](/windows/desktop/WmiSdk/example--getting-wmi-data-from-a-remote-computer).


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
    // Note: If you are using Windows 2000, specify -
    // the default authentication credentials for a user by using
    // a SOLE_AUTHENTICATION_LIST structure in the pAuthList ----
    // parameter of CoInitializeSecurity ------------------------

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
        pSvc->Release();     
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

    // Set up to call the Win32_Process::Create method
    BSTR ClassName = SysAllocString(L"Win32_Process");

    /* YOU NEED TO CHANGE THE NUMBER VALUE OF THE HANDLE 
       (PROCESS ID) TO THE CORRECT VALUE OF THE PROCESS YOU 
       ARE TRYING TO TERMINATE (this provides a path to
       the class instance you are tying to terminate). */
    BSTR ClassNameInstance = SysAllocString(
        L"Win32_Process.Handle=\"3168\"");

    _bstr_t MethodName = (L"Terminate");
    BSTR ParameterName = SysAllocString(L"Reason");

    IWbemClassObject* pClass = NULL;
    hres = pSvc->GetObject(ClassName, 0, NULL, &pClass, NULL);

    IWbemClassObject* pInParamsDefinition = NULL;
    IWbemClassObject* pOutMethod = NULL;
    hres = pClass->GetMethod(MethodName, 0, 
        &pInParamsDefinition, &pOutMethod);

    if (FAILED(hres))
    {
        cout << "Could not get the method. Error code = 0x" 
             << hex << hres << endl;
    }

    IWbemClassObject* pClassInstance = NULL;
    hres = pInParamsDefinition->SpawnInstance(0, &pClassInstance);

    // Create the values for the in parameters
    VARIANT pcVal;
    VariantInit(&pcVal);
    V_VT(&pcVal) = VT_I4;

    // Store the value for the in parameters
    hres = pClassInstance->Put(L"Reason", 0,
        &pcVal, 0);

    // Execute Method
    hres = pSvc->ExecMethod(ClassNameInstance, MethodName, 0,
    NULL, pClassInstance, NULL, NULL);

    if (FAILED(hres))
    {
        cout << "Could not execute method. Error code = 0x" 
             << hex << hres << endl;
        VariantClear(&pcVal);
        SysFreeString(ClassName);
        SysFreeString(MethodName);
        pClass->Release();
        pInParamsDefinition->Release();
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 1;           // Program has failed.
    }


    // Clean up
    //--------------------------
    VariantClear(&pcVal);
    SysFreeString(ClassName);
    SysFreeString(MethodName);
    pClass->Release();
    pInParamsDefinition->Release();
    pLoc->Release();
    pSvc->Release();
    CoUninitialize();
    return 0;
}
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

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32- \_ Prozess**](win32-process.md)
</dt> <dt>

[WMI-Tasks: Leistungsüberwachung](/windows/desktop/WmiSdk/wmi-tasks--performance-monitoring)
</dt> <dt>

[WMI-Tasks: Prozesse](/windows/desktop/WmiSdk/wmi-tasks--processes)
</dt> </dl>

 

