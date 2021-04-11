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
# <a name="terminate-method-of-the-win32_process-class"></a><span data-ttu-id="391cf-103">Beendigungs Methode der Win32- \_ Prozess Klasse</span><span class="sxs-lookup"><span data-stu-id="391cf-103">Terminate method of the Win32\_Process class</span></span>

<span data-ttu-id="391cf-104">Die Methode zum **Beenden** der [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) beendet einen Prozess und alle zugehörigen Threads.</span><span class="sxs-lookup"><span data-stu-id="391cf-104">The **Terminate** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method terminates a process and all of its threads.</span></span>

<span data-ttu-id="391cf-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="391cf-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="391cf-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="391cf-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="391cf-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="391cf-107">Syntax</span></span>


```mof
uint32 Terminate(
  [in] uint32 Reason
);
```



## <a name="parameters"></a><span data-ttu-id="391cf-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="391cf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="391cf-109">*Grund* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="391cf-109">*Reason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="391cf-110">Der Exitcode für den Prozess und für alle Threads, die als Ergebnis dieses Aufrufes beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="391cf-110">Exit code for the process and for all of the threads terminated as a result of this call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="391cf-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="391cf-111">Return value</span></span>

<span data-ttu-id="391cf-112">Gibt den Wert 0 (null) zurück, wenn der Prozess erfolgreich beendet wurde, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="391cf-112">Returns a value of 0 (zero) if the process was successfully terminated, and any other number to indicate an error.</span></span> <span data-ttu-id="391cf-113">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="391cf-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="391cf-114">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="391cf-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="391cf-115">**Erfolgreicher Abschluss** (0)</span><span class="sxs-lookup"><span data-stu-id="391cf-115">**Successful completion** (0)</span></span>
</dt> <dt>

<span data-ttu-id="391cf-116">**Zugriff verweigert** (2)</span><span class="sxs-lookup"><span data-stu-id="391cf-116">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="391cf-117">**Unzureichende Berechtigungen** (3)</span><span class="sxs-lookup"><span data-stu-id="391cf-117">**Insufficient privilege** (3)</span></span>
</dt> <dt>

<span data-ttu-id="391cf-118">**Unbekannter Fehler** (8)</span><span class="sxs-lookup"><span data-stu-id="391cf-118">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="391cf-119">Der **Pfad wurde nicht gefunden** (9).</span><span class="sxs-lookup"><span data-stu-id="391cf-119">**Path not found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="391cf-120">**Ungültiger Parameter** (21)</span><span class="sxs-lookup"><span data-stu-id="391cf-120">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="391cf-121">**Sonstige** (22 4294967295)</span><span class="sxs-lookup"><span data-stu-id="391cf-121">**Other** (22 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="391cf-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="391cf-122">Remarks</span></span>

<span data-ttu-id="391cf-123">**Übersicht**</span><span class="sxs-lookup"><span data-stu-id="391cf-123">**Overview**</span></span>

<span data-ttu-id="391cf-124">Computer Probleme sind häufig auf einen Prozess zurückzuführen, der nicht mehr erwartungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="391cf-124">Computer problems are often due to a process that is no longer working as expected.</span></span> <span data-ttu-id="391cf-125">Beispielsweise kann es vorkommen, dass der Prozess Speicher Verluste verursacht oder nicht mehr auf Benutzereingaben reagiert.</span><span class="sxs-lookup"><span data-stu-id="391cf-125">For example, the process might be leaking memory, or it might have stopped responding to user input.</span></span> <span data-ttu-id="391cf-126">Wenn Probleme wie diese auftreten, muss der Prozess beendet werden.</span><span class="sxs-lookup"><span data-stu-id="391cf-126">When problems such as these occur, the process must be terminated.</span></span> <span data-ttu-id="391cf-127">Obwohl dies möglicherweise wie eine einfache genug Aufgabe aussieht, kann das Beenden eines Prozesses durch verschiedene Faktoren erschwert werden:</span><span class="sxs-lookup"><span data-stu-id="391cf-127">Although this might seem like a simple enough task, terminating a process can be complicated by several factors:</span></span>

-   <span data-ttu-id="391cf-128">Der Prozess ist möglicherweise nicht mehr auf Menüs oder Tastaturbefehle zum Schließen der Anwendung reagiert.</span><span class="sxs-lookup"><span data-stu-id="391cf-128">The process might be hung and therefore no longer responds to menu or keyboard commands for closing the application.</span></span> <span data-ttu-id="391cf-129">Dadurch kann der typische Benutzer die Anwendung nicht verwerfen und den Prozess beenden.</span><span class="sxs-lookup"><span data-stu-id="391cf-129">This makes it all but impossible for the typical user to dismiss the application and terminate the process.</span></span>
-   <span data-ttu-id="391cf-130">Der Prozess ist möglicherweise verwaist.</span><span class="sxs-lookup"><span data-stu-id="391cf-130">The process might be orphaned.</span></span> <span data-ttu-id="391cf-131">Beispielsweise kann ein Skript eine Instanz von Word erstellen und dann beenden, ohne diese Instanz zu zerstören.</span><span class="sxs-lookup"><span data-stu-id="391cf-131">For example, a script might create an instance of Word and then exit without destroying that instance.</span></span> <span data-ttu-id="391cf-132">Tatsächlich wird Word weiterhin auf dem Computer ausgeführt, auch wenn keine Benutzeroberfläche sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="391cf-132">In effect, Word remains running on the computer, even though no user interface is visible.</span></span> <span data-ttu-id="391cf-133">Da keine Benutzeroberfläche vorhanden ist, stehen keine Menü-oder Tastaturbefehle zum Beenden des Prozesses zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="391cf-133">Because there is no user interface, there are no menu or keyboard commands available to terminate the process.</span></span>
-   <span data-ttu-id="391cf-134">Möglicherweise wissen Sie nicht, welcher Prozess beendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="391cf-134">You might not know which process needs to be terminated.</span></span> <span data-ttu-id="391cf-135">Beispielsweise kann es sein, dass Sie alle Programme beenden möchten, die eine bestimmte Arbeitsspeicher Menge überschreiten.</span><span class="sxs-lookup"><span data-stu-id="391cf-135">For example, you might want to terminate all programs that are exceeding a specified amount of memory.</span></span>
-   <span data-ttu-id="391cf-136">Da Sie mit dem Task-Manager nur die Prozesse beenden können, die Sie erstellt haben, können Sie einen Prozess möglicherweise nicht beenden, auch wenn Sie ein Administrator auf dem Computer sind.</span><span class="sxs-lookup"><span data-stu-id="391cf-136">Because Task Manager allows you to terminate only those processes that you created, you might not be able to terminate a process, even if you are an administrator on the computer.</span></span>

<span data-ttu-id="391cf-137">Mithilfe von Skripts können Sie all diese potenziellen Hindernisse überwinden und so eine beträchtliche administrative Kontrolle über Ihre Computer gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="391cf-137">Scripts enable you to overcome all of these potential obstacles, providing you with considerable administrative control over your computers.</span></span> <span data-ttu-id="391cf-138">Wenn Sie z. b. vermuten, dass Benutzer Spiele spielen, die in Ihrer Organisation unzulässig waren, können Sie problemlos ein Skript schreiben, um eine Verbindung zu den einzelnen Computern herzustellen, festzustellen, ob das Spiel ausgeführt wird, und den Prozess sofort beenden.</span><span class="sxs-lookup"><span data-stu-id="391cf-138">For example, if you suspect users are playing games that have been prohibited in your organization, you can easily write a script to connect to each computer, identify whether the game is running, and immediately terminate the process.</span></span>

<span data-ttu-id="391cf-139">**Verwenden der Beendigungs Methode**</span><span class="sxs-lookup"><span data-stu-id="391cf-139">**Using the Terminate Method**</span></span>

<span data-ttu-id="391cf-140">Sie können einen Prozess beenden, indem Sie Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="391cf-140">You can terminate a process by:</span></span>

-   <span data-ttu-id="391cf-141">Beenden eines Prozesses, der derzeit ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="391cf-141">Terminating a process that is currently running.</span></span> <span data-ttu-id="391cf-142">Beispielsweise müssen Sie möglicherweise ein Diagnoseprogramm beenden, das auf einem Remote Computer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="391cf-142">For example, you might need to terminate a diagnostic program running on a remote computer.</span></span> <span data-ttu-id="391cf-143">Wenn es keine Möglichkeit gibt, die Anwendung Remote zu steuern, können Sie einfach den Prozess für diese Anwendung beenden.</span><span class="sxs-lookup"><span data-stu-id="391cf-143">If there is no way to control the application remotely, you can simply terminate the process for that application.</span></span>
-   <span data-ttu-id="391cf-144">Verhindern, dass ein Prozess an erster Stelle ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="391cf-144">Preventing a process from running in the first place.</span></span> <span data-ttu-id="391cf-145">Durch die kontinuierliche Überwachung der Prozesserstellung auf einem Computer können Sie jeden Prozess ermitteln und sofort beenden, sobald er gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="391cf-145">By continuously monitoring process creation on a computer, you can identify and instantly terminate any process as soon as it starts.</span></span> <span data-ttu-id="391cf-146">Dies bietet eine Methode, um sicherzustellen, dass bestimmte Anwendungen (z. b. Programme, die große Mediendateien über das Internet herunterladen) niemals auf bestimmten Computern ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="391cf-146">This provides one method of ensuring that certain applications (such as programs that download large media files over the Internet) are never run on certain computers.</span></span>

> [!Note]  
> <span data-ttu-id="391cf-147">Gruppenrichtlinie können auch verwendet werden, um die Programme einzuschränken, die auf einem Computer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="391cf-147">Group Policy can also be used to restrict the programs that run on a computer.</span></span> <span data-ttu-id="391cf-148">Gruppenrichtlinie können jedoch nur die Programme beschränken, die entweder über das Startmenü oder Windows-Explorer ausgeführt werden. Es hat keine Auswirkung auf Programme, die mit anderen Methoden gestartet wurden, z. b. über die Befehlszeile.</span><span class="sxs-lookup"><span data-stu-id="391cf-148">However, Group Policy can restrict only the programs run using either the Start menu or Windows Explorer; it has no effect on programs started using other means, such as the command line.</span></span> <span data-ttu-id="391cf-149">Im Gegensatz dazu kann WMI verhindern, dass ein Prozess ausgeführt wird, unabhängig davon, wie der Prozess gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="391cf-149">By contrast, WMI can prevent a process from running regardless of how the process was started.</span></span>

 

<span data-ttu-id="391cf-150">**Beenden eines Prozesses, den Sie nicht besitzen**</span><span class="sxs-lookup"><span data-stu-id="391cf-150">**Terminating a Process You Do Not Own**</span></span>

<span data-ttu-id="391cf-151">Um einen Prozess zu beenden, den Sie nicht besitzen, aktivieren **Sie die Berechtigung** "" für "".</span><span class="sxs-lookup"><span data-stu-id="391cf-151">To terminate a process that you do not own, enable the **SeDebugPrivilege** privilege.</span></span> <span data-ttu-id="391cf-152">In VBScript können Sie dieses Privileg mit den folgenden Codezeilen aktivieren:</span><span class="sxs-lookup"><span data-stu-id="391cf-152">In VBScript, you can enable this privilege with the following lines of code:</span></span>


```VB
Set objLoc = createobject("wbemscripting.swbemlocator")
objLoc.Security_.privileges.addasstring "sedebugprivilege", true
```



<span data-ttu-id="391cf-153">Weitere Informationen zum Aktivieren dieser Berechtigung in C++ finden Sie unter [aktivieren und Deaktivieren von Berechtigungen in C++](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--).</span><span class="sxs-lookup"><span data-stu-id="391cf-153">For more information about enabling this privilege in C++, see [Enabling and Disabling Privileges in C++](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--).</span></span>

## <a name="examples"></a><span data-ttu-id="391cf-154">Beispiele</span><span class="sxs-lookup"><span data-stu-id="391cf-154">Examples</span></span>

<span data-ttu-id="391cf-155">Mit dem PowerShell-Codebeispiel für das [Beenden des laufenden Vorgangs auf mehreren Servern](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) wird ein Prozess beendet, der auf einem oder mehreren Computern ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="391cf-155">The [Terminate running process on multiple servers](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) PowerShell code sample on TechNet Gallery terminates a process running on a single or multiple computers.</span></span>

<span data-ttu-id="391cf-156">Im folgenden VBScript-Beispiel wird der Prozess beendet, in dem die Anwendungs Diagnose.exe derzeit ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="391cf-156">The following VBScript sample terminates the process in which the application Diagnose.exe is currently running.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcessList = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'Diagnose.exe'")
For Each objProcess in colProcessList
 objProcess.Terminate()
Next
```



<span data-ttu-id="391cf-157">Im folgenden VBScript-Beispiel wird ein temporärer Ereignisconsumer verwendet, um einen Prozess zu beenden, sobald er gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="391cf-157">The following VBScript sample uses a temporary event consumer to terminate a process as soon as it starts.</span></span>


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



<span data-ttu-id="391cf-158">Im folgenden VBScript-Codebeispiel wird eine Verbindung mit einem Remote Computer hergestellt, und der Notepad.exe auf diesem Computer wird beendet.</span><span class="sxs-lookup"><span data-stu-id="391cf-158">The following VBScript code example connects to a remote computer and terminates Notepad.exe on that computer.</span></span>


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



<span data-ttu-id="391cf-159">Der folgende C++-Code beendet den Notepad.exe Prozess auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="391cf-159">The following C++ code terminates the Notepad.exe process on the local computer.</span></span> <span data-ttu-id="391cf-160">Geben Sie ein-oder-Prozess handle (Prozess-ID) im Code an, um den Prozess zu beenden.</span><span class="sxs-lookup"><span data-stu-id="391cf-160">Specify a or process handle (process id) in the code to terminate the process.</span></span> <span data-ttu-id="391cf-161">Dieser Wert befindet sich in der Handle-Eigenschaft in der [**Win32- \_ Prozess**](win32-process.md) Klasse (die Schlüsseleigenschaft für die-Klasse).</span><span class="sxs-lookup"><span data-stu-id="391cf-161">This value can be found in the handle property in the [**Win32\_Process**](win32-process.md) class (the key property for the class).</span></span> <span data-ttu-id="391cf-162">Wenn Sie einen Wert für die Handle-Eigenschaft angeben, geben Sie einen Pfad zur Instanz der-Klasse an, die Sie beenden möchten.</span><span class="sxs-lookup"><span data-stu-id="391cf-162">By specifying a value for the Handle property, you are supplying a path to the instance of the class that you want to terminate.</span></span> <span data-ttu-id="391cf-163">Weitere Informationen zum Herstellen einer Verbindung mit einem Remote Computer finden Sie unter [Beispiel: erhalten von WMI-Daten von einem Remote Computer aus](/windows/desktop/WmiSdk/example--getting-wmi-data-from-a-remote-computer).</span><span class="sxs-lookup"><span data-stu-id="391cf-163">For more information about connecting to a remote computer, see [Example: Getting WMI Data From a Remote Computer](/windows/desktop/WmiSdk/example--getting-wmi-data-from-a-remote-computer).</span></span>


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



## <a name="requirements"></a><span data-ttu-id="391cf-164">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="391cf-164">Requirements</span></span>



| <span data-ttu-id="391cf-165">Anforderung</span><span class="sxs-lookup"><span data-stu-id="391cf-165">Requirement</span></span> | <span data-ttu-id="391cf-166">Wert</span><span class="sxs-lookup"><span data-stu-id="391cf-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="391cf-167">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="391cf-167">Minimum supported client</span></span><br/> | <span data-ttu-id="391cf-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="391cf-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="391cf-169">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="391cf-169">Minimum supported server</span></span><br/> | <span data-ttu-id="391cf-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="391cf-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="391cf-171">Namespace</span><span class="sxs-lookup"><span data-stu-id="391cf-171">Namespace</span></span><br/>                | <span data-ttu-id="391cf-172">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="391cf-172">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="391cf-173">MOF</span><span class="sxs-lookup"><span data-stu-id="391cf-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="391cf-174"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="391cf-174"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="391cf-175">DLL</span><span class="sxs-lookup"><span data-stu-id="391cf-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="391cf-176"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="391cf-176"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="391cf-177">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="391cf-177">See also</span></span>

<dl> <dt>

<span data-ttu-id="391cf-178">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="391cf-178">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="391cf-179">**Win32- \_ Prozess**</span><span class="sxs-lookup"><span data-stu-id="391cf-179">**Win32\_Process**</span></span>](win32-process.md)
</dt> <dt>

[<span data-ttu-id="391cf-180">WMI-Tasks: Leistungsüberwachung</span><span class="sxs-lookup"><span data-stu-id="391cf-180">WMI Tasks: Performance Monitoring</span></span>](/windows/desktop/WmiSdk/wmi-tasks--performance-monitoring)
</dt> <dt>

[<span data-ttu-id="391cf-181">WMI-Tasks: Prozesse</span><span class="sxs-lookup"><span data-stu-id="391cf-181">WMI Tasks: Processes</span></span>](/windows/desktop/WmiSdk/wmi-tasks--processes)
</dt> </dl>

 

