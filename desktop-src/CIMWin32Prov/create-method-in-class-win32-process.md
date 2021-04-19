---
description: Die CREATE&\# 8194; Die WMI-Klassenmethode erstellt einen neuen Prozess.
ms.assetid: be80abec-fab4-4403-bc29-d0d4a38e3c87
ms.tgt_platform: multiple
title: Create-Methode der Win32_Process-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 42c675f61fc8b42790aeb811ec275554b355a392
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342761"
---
# <a name="create-method-of-the-win32_process-class"></a><span data-ttu-id="81861-103">Create-Methode der Win32- \_ Prozess Klasse</span><span class="sxs-lookup"><span data-stu-id="81861-103">Create method of the Win32\_Process class</span></span>

<span data-ttu-id="81861-104">Die **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) -Methode erstellt einen neuen Prozess.</span><span class="sxs-lookup"><span data-stu-id="81861-104">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method creates a new process.</span></span>

<span data-ttu-id="81861-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="81861-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="81861-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="81861-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="81861-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="81861-107">Syntax</span></span>


```mof
uint32 Create(
  [in]  string               CommandLine,
  [in]  string               CurrentDirectory,
  [in]  Win32_ProcessStartup ProcessStartupInformation,
  [out] uint32               ProcessId
);
```



## <a name="parameters"></a><span data-ttu-id="81861-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="81861-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81861-109">*Befehlszeile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="81861-109">*CommandLine* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81861-110">Die auszuführende Befehlszeile.</span><span class="sxs-lookup"><span data-stu-id="81861-110">Command line to execute.</span></span> <span data-ttu-id="81861-111">Das System fügt der Befehlszeile ein NULL-Zeichen hinzu, wobei die Zeichenfolge bei Bedarf gekürzt wird, um anzugeben, welche Datei tatsächlich verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="81861-111">The system adds a null character to the command line, trimming the string if necessary, to indicate which file was actually used.</span></span>

</dd> <dt>

<span data-ttu-id="81861-112">*CurrentDirectory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="81861-112">*CurrentDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81861-113">Aktuelles Laufwerk und Verzeichnis für den untergeordneten Prozess.</span><span class="sxs-lookup"><span data-stu-id="81861-113">Current drive and directory for the child process.</span></span> <span data-ttu-id="81861-114">Für die Zeichenfolge muss das aktuelle Verzeichnis zu einem bekannten Pfad aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="81861-114">The string requires that the current directory resolves to a known path.</span></span> <span data-ttu-id="81861-115">Ein Benutzer kann einen absoluten Pfad oder einen Pfad relativ zum aktuellen Arbeitsverzeichnis angeben.</span><span class="sxs-lookup"><span data-stu-id="81861-115">A user can specify an absolute path or a path relative to the current working directory.</span></span> <span data-ttu-id="81861-116">Wenn dieser Parameter **null** ist, weist der neue Prozess denselben Pfad wie der aufrufende Prozess auf.</span><span class="sxs-lookup"><span data-stu-id="81861-116">If this parameter is **NULL**, the new process will have the same path as the calling process.</span></span> <span data-ttu-id="81861-117">Diese Option wird in erster Linie für Shells bereitgestellt, die eine Anwendung starten müssen, und das Anfangs Laufwerk und Arbeitsverzeichnis der Anwendung angeben.</span><span class="sxs-lookup"><span data-stu-id="81861-117">This option is provided primarily for shells that must start an application and specify the application's initial drive and working directory.</span></span>

</dd> <dt>

<span data-ttu-id="81861-118">*Processstartupinformation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="81861-118">*ProcessStartupInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81861-119">Die Startkonfiguration eines Windows-Prozesses.</span><span class="sxs-lookup"><span data-stu-id="81861-119">The startup configuration of a Windows process.</span></span> <span data-ttu-id="81861-120">Weitere Informationen finden Sie unter [**Win32 \_ processstartup**](win32-processstartup.md).</span><span class="sxs-lookup"><span data-stu-id="81861-120">For more information, see [**Win32\_ProcessStartup**](win32-processstartup.md).</span></span>

</dd> <dt>

<span data-ttu-id="81861-121">*ProcessID* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="81861-121">*ProcessId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81861-122">Die globale Prozess-ID, die zum Identifizieren eines Prozesses verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="81861-122">Global process identifier that can be used to identify a process.</span></span> <span data-ttu-id="81861-123">Der Wert ist ab dem Zeitpunkt gültig, zu dem der Prozess erstellt wird, bis zu dem Zeitpunkt, zu dem der Prozess beendet wird.</span><span class="sxs-lookup"><span data-stu-id="81861-123">The value is valid from the time the process is created until the time the process is terminated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81861-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="81861-124">Return value</span></span>

<span data-ttu-id="81861-125">Gibt den Wert 0 (null) zurück, wenn der Prozess erfolgreich erstellt wurde, und jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="81861-125">Returns a value of 0 (zero) if the process was successfully created, and any other number to indicate an error.</span></span> <span data-ttu-id="81861-126">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="81861-126">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="81861-127">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="81861-127">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="81861-128">**Erfolgreicher Abschluss** (0)</span><span class="sxs-lookup"><span data-stu-id="81861-128">**Successful completion** (0)</span></span>
</dt> <dt>

<span data-ttu-id="81861-129">**Zugriff verweigert** (2)</span><span class="sxs-lookup"><span data-stu-id="81861-129">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="81861-130">**Unzureichende Berechtigungen** (3)</span><span class="sxs-lookup"><span data-stu-id="81861-130">**Insufficient privilege** (3)</span></span>
</dt> <dt>

<span data-ttu-id="81861-131">**Unbekannter Fehler** (8)</span><span class="sxs-lookup"><span data-stu-id="81861-131">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="81861-132">Der **Pfad wurde nicht gefunden** (9).</span><span class="sxs-lookup"><span data-stu-id="81861-132">**Path not found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="81861-133">**Ungültiger Parameter** (21)</span><span class="sxs-lookup"><span data-stu-id="81861-133">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="81861-134">**Sonstige** (22 4294967295)</span><span class="sxs-lookup"><span data-stu-id="81861-134">**Other** (22 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="81861-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="81861-135">Remarks</span></span>

<span data-ttu-id="81861-136">Sie können eine Instanz der Win32-Klasse " [**\_ processstartup**](win32-processstartup.md) " erstellen, um den Prozess zu konfigurieren, bevor Sie diese Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="81861-136">You can create an instance of the [**Win32\_ProcessStartup**](win32-processstartup.md) class to configure the process before calling this method.</span></span>

<span data-ttu-id="81861-137">Ein voll qualifizierter Pfad muss in Fällen angegeben werden, in denen das zu startende Programm nicht im Suchpfad Winmgmt.exe ist.</span><span class="sxs-lookup"><span data-stu-id="81861-137">A fully qualified path must be specified in cases where the program to be launched is not in the search path of Winmgmt.exe.</span></span> <span data-ttu-id="81861-138">Wenn der neu erstellte Prozess versucht, mit Objekten auf dem Zielsystem ohne die entsprechenden Zugriffsberechtigungen zu interagieren, wird er ohne Benachrichtigung an diese Methode beendet.</span><span class="sxs-lookup"><span data-stu-id="81861-138">If the newly created process attempts to interact with objects on the target system without the appropriate access privileges, it is terminated without notification to this method.</span></span>

<span data-ttu-id="81861-139">Aus Sicherheitsgründen kann die **Win32 \_ Process. Create** -Methode nicht zum Remote Starten eines interaktiven Prozesses verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="81861-139">For security reasons the **Win32\_Process.Create** method cannot be used to start an interactive process remotely.</span></span>

<span data-ttu-id="81861-140">Prozesse, die mit der **Win32 \_ Process. Create** -Methode erstellt wurden, sind durch das Auftrags Objekt beschränkt, es sei denn, das Flag **Create \_ breakoff \_ from \_ Job** ist angegeben.</span><span class="sxs-lookup"><span data-stu-id="81861-140">Processes created with the **Win32\_Process.Create** method are limited by the job object unless the **CREATE\_BREAKAWAY\_FROM\_JOB** flag is specified.</span></span> <span data-ttu-id="81861-141">Weitere Informationen finden Sie unter [**Win32 \_ processstartup**](win32-processstartup.md) und [**\_ \_ providerhostquotaconfiguration**](/windows/desktop/WmiSdk/--providerhostquotaconfiguration).</span><span class="sxs-lookup"><span data-stu-id="81861-141">For more information, see [**Win32\_ProcessStartup**](win32-processstartup.md) and [**\_\_ProviderHostQuotaConfiguration**](/windows/desktop/WmiSdk/--providerhostquotaconfiguration).</span></span>

## <a name="examples"></a><span data-ttu-id="81861-142">Beispiele</span><span class="sxs-lookup"><span data-stu-id="81861-142">Examples</span></span>

<span data-ttu-id="81861-143">Das folgende VBScript-Beispiel veranschaulicht, wie eine CIM-Methode aufgerufen wird, als ob es sich um eine Automatisierungs Methode von "errbemubject" handelt.</span><span class="sxs-lookup"><span data-stu-id="81861-143">The following VBScript example demonstrates how to invoke a CIM method as if it were an automation method of SWbemObject.</span></span>


```VB
on error resume next

set process = GetObject("winmgmts:Win32_Process")

result = process.Create ("notepad.exe",null,null,processid)

WScript.Echo "Method returned result = " & result
WScript.Echo "Id of new process is " & processid

if err <>0 then
 WScript.Echo Err.Description, "0x" & Hex(Err.Number)
end if
```



<span data-ttu-id="81861-144">Das folgende perl-Beispiel veranschaulicht, wie Sie eine CIM-Methode aufrufen, als ob es sich um eine Automatisierungs Methode von "errbemubject" handelt.</span><span class="sxs-lookup"><span data-stu-id="81861-144">The following Perl example demonstrates how to invoke a CIM method as if it were an automation method of SWbemObject.</span></span>


```VB
use strict;
use Win32::OLE;

my ($process, $outParam, $processid, $inParam, $objMethod);

eval { $process = 
 Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2:Win32_Process"); };

if (!$@ && defined $process)
{
 $objMethod = $process->Methods_("Create");

 #Spawn an instance of inParameters and assign the values.
 $inParam = $objMethod->inParameters->SpawnInstance_ if (defined $objMethod);
 $inParam->{CommandLine} = "notepad.exe";
 $inParam->{CurrentDirectory} = undef;
 $inParam->{ProcessStartupInformation} = undef;

 $outParam = $process->ExecMethod_("Create", $inParam) if (defined $inParam);
 if ($outParam->{ReturnValue})
 {
  print STDERR Win32::OLE->LastError, "\n";
 }
 else
 {
  print "Method returned result = $outParam->{ReturnValue}\n";
  print "Id of new process is $outParam->{ProcessId}\n"
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="81861-145">Im folgenden VBScript-Codebeispiel wird ein Notepad-Prozess auf dem lokalen Computer erstellt.</span><span class="sxs-lookup"><span data-stu-id="81861-145">The following VBScript code example creates a Notepad process on the local computer.</span></span> <span data-ttu-id="81861-146">[**Win32 \_ Processstartup**](win32-processstartup.md) wird verwendet, um die Prozesseinstellungen zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="81861-146">[**Win32\_ProcessStartup**](win32-processstartup.md) is used to configure the process settings.</span></span>


```VB
Const SW_NORMAL = 1
strComputer = "."
strCommand = "Notepad.exe" 
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" _
    & strComputer & "\root\cimv2")

' Configure the Notepad process to show a window
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.ShowWindow = SW_NORMAL

' Create Notepad process
Set objProcess = objWMIService.Get("Win32_Process")
intReturn = objProcess.Create _
    (strCommand, Null, objConfig, intProcessID)
If intReturn <> 0 Then
    Wscript.Echo "Process could not be created." & _
        vbNewLine & "Command line: " & strCommand & _
        vbNewLine & "Return value: " & intReturn
Else
    Wscript.Echo "Process created." & _
        vbNewLine & "Command line: " & strCommand & _
        vbNewLine & "Process ID: " & intProcessID
End If
```



## <a name="requirements"></a><span data-ttu-id="81861-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="81861-147">Requirements</span></span>



| <span data-ttu-id="81861-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="81861-148">Requirement</span></span> | <span data-ttu-id="81861-149">Wert</span><span class="sxs-lookup"><span data-stu-id="81861-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81861-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="81861-150">Minimum supported client</span></span><br/> | <span data-ttu-id="81861-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="81861-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="81861-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="81861-152">Minimum supported server</span></span><br/> | <span data-ttu-id="81861-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="81861-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="81861-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="81861-154">Namespace</span></span><br/>                | <span data-ttu-id="81861-155">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="81861-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="81861-156">MOF</span><span class="sxs-lookup"><span data-stu-id="81861-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81861-157"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="81861-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="81861-158">DLL</span><span class="sxs-lookup"><span data-stu-id="81861-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81861-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81861-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81861-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81861-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="81861-161">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="81861-161">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="81861-162">**Win32- \_ Prozess**</span><span class="sxs-lookup"><span data-stu-id="81861-162">**Win32\_Process**</span></span>](win32-process.md)
</dt> <dt>

[<span data-ttu-id="81861-163">WMI-Tasks: Prozesse</span><span class="sxs-lookup"><span data-stu-id="81861-163">WMI Tasks: Processes</span></span>](/windows/desktop/WmiSdk/wmi-tasks--processes)
</dt> </dl>

 

