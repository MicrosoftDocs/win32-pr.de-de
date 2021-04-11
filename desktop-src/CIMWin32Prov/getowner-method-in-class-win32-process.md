---
description: Die GetOwner-&\# 8194; WMI-Klassenmethode Ruft den Benutzernamen und den Domänen Namen ab, unter dem der Prozess ausgeführt wird.
ms.assetid: bbd6d22b-ca54-42f3-8098-d3034048ec4d
ms.tgt_platform: multiple
title: GetOwner-Methode der Win32_Process-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.GetOwner
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 007acbe997f555e9a439ed27740a447d3bf7fe4d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126482"
---
# <a name="getowner-method-of-the-win32_process-class"></a><span data-ttu-id="81100-103">GetOwner-Methode der Win32- \_ Prozess Klasse</span><span class="sxs-lookup"><span data-stu-id="81100-103">GetOwner method of the Win32\_Process class</span></span>

<span data-ttu-id="81100-104">Die **GetOwner** - [WMI-Klassen](/windows/desktop/WmiSdk/retrieving-a-class) Methode ruft den Benutzernamen und den Domänen Namen ab, unter dem der Prozess ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="81100-104">The **GetOwner** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method retrieves the user name and domain name under which the process is running.</span></span>

<span data-ttu-id="81100-105">In diesem Thema wird die MOF-Syntax (Managed Object Format) verwendet.</span><span class="sxs-lookup"><span data-stu-id="81100-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="81100-106">Weitere Informationen zum Verwenden dieser Methode finden Sie unter [Aufrufen einer Methode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="81100-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="81100-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="81100-107">Syntax</span></span>


```mof
uint32 GetOwner(
  [out] string User,
  [out] string Domain
);
```



## <a name="parameters"></a><span data-ttu-id="81100-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="81100-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81100-109">*Benutzer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="81100-109">*User* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81100-110">Gibt den Benutzernamen des Besitzers dieses Prozesses zurück.</span><span class="sxs-lookup"><span data-stu-id="81100-110">Returns the user name of the owner of this process.</span></span>

</dd> <dt>

<span data-ttu-id="81100-111">*Domäne* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="81100-111">*Domain* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81100-112">Gibt den Domänen Namen zurück, unter dem der Prozess ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="81100-112">Returns the domain name under which this process is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81100-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="81100-113">Return value</span></span>

<span data-ttu-id="81100-114">Gibt NULL (0) zurück, um den Erfolg anzugeben.</span><span class="sxs-lookup"><span data-stu-id="81100-114">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="81100-115">Jede andere Zahl gibt einen Fehler an.</span><span class="sxs-lookup"><span data-stu-id="81100-115">Any other number indicates an error.</span></span> <span data-ttu-id="81100-116">Weitere Fehlercodes finden Sie unter [**WMI-Fehler Konstanten**](/windows/desktop/WmiSdk/wmi-error-constants) oder [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="81100-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="81100-117">Allgemeine **HRESULT** -Werte finden Sie unter [System Fehler Codes](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="81100-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="81100-118">**Erfolgreicher Abschluss** (0)</span><span class="sxs-lookup"><span data-stu-id="81100-118">**Successful completion** (0)</span></span>
</dt> <dt>

<span data-ttu-id="81100-119">**Zugriff verweigert** (2)</span><span class="sxs-lookup"><span data-stu-id="81100-119">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="81100-120">**Unzureichende Berechtigungen** (3)</span><span class="sxs-lookup"><span data-stu-id="81100-120">**Insufficient privilege** (3)</span></span>
</dt> <dt>

<span data-ttu-id="81100-121">**Unbekannter Fehler** (8)</span><span class="sxs-lookup"><span data-stu-id="81100-121">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="81100-122">Der **Pfad wurde nicht gefunden** (9).</span><span class="sxs-lookup"><span data-stu-id="81100-122">**Path not found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="81100-123">**Ungültiger Parameter** (21)</span><span class="sxs-lookup"><span data-stu-id="81100-123">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="81100-124">**Sonstige** (22 4294967295)</span><span class="sxs-lookup"><span data-stu-id="81100-124">**Other** (22 4294967295)</span></span>
</dt> </dl>

## <a name="examples"></a><span data-ttu-id="81100-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="81100-125">Examples</span></span>

<span data-ttu-id="81100-126">[Die Monitor Prozess-CPU PCT nach Name mit Besitzer](https://Gallery.TechNet.Microsoft.Com/Monitor-Process-CPU-Pct-by-0f3a5a1c) VBScript-Beispiel erfasst die CPU-oder Prozessorauslastung in Prozent und sucht den Prozess Besitzer.</span><span class="sxs-lookup"><span data-stu-id="81100-126">[The Monitor Process CPU Pct by Name with Owner](https://Gallery.TechNet.Microsoft.Com/Monitor-Process-CPU-Pct-by-0f3a5a1c) VBScript sample collects the CPU or Processor utilization percent and looks up the process owner.</span></span>

<span data-ttu-id="81100-127">Das Beispiel abrufen [aller Server, auf denen eine Liste von Benutzern](https://Gallery.TechNet.Microsoft.Com/Get-all-servers-that-a-aecc07ef) bei PowerShell angemeldet ist WMI für den Besitzer aller explorer.exe Prozesse.</span><span class="sxs-lookup"><span data-stu-id="81100-127">The [Get all servers that a list of users is logged onto](https://Gallery.TechNet.Microsoft.Com/Get-all-servers-that-a-aecc07ef) PowerShell sample querys WMI for the owner of all explorer.exe processes.</span></span>

<span data-ttu-id="81100-128">Im folgenden VBScript-Codebeispiel wird der Besitzer für jeden laufenden Prozess abgerufen.</span><span class="sxs-lookup"><span data-stu-id="81100-128">The following VBScript code example obtains the owner for each running process.</span></span>


```VB
strComputer = "."
Set colProcesses = GetObject("winmgmts:" & _
   "{impersonationLevel=impersonate}!\\" & strComputer & _
   "\root\cimv2").ExecQuery("Select * from Win32_Process")

For Each objProcess in colProcesses

    Return = objProcess.GetOwner(strNameOfUser)
    If Return <> 0 Then
        Wscript.Echo "Could not get owner info for process " & _  
            objProcess.Name & VBNewLine _
            & "Error = " & Return
    Else 
        Wscript.Echo "Process " _
            & objProcess.Name & " is owned by " _ 
            & "\" & strNameOfUser & "."
    End If
Next
```



## <a name="requirements"></a><span data-ttu-id="81100-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="81100-129">Requirements</span></span>



| <span data-ttu-id="81100-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="81100-130">Requirement</span></span> | <span data-ttu-id="81100-131">Wert</span><span class="sxs-lookup"><span data-stu-id="81100-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81100-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="81100-132">Minimum supported client</span></span><br/> | <span data-ttu-id="81100-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="81100-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="81100-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="81100-134">Minimum supported server</span></span><br/> | <span data-ttu-id="81100-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="81100-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="81100-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="81100-136">Namespace</span></span><br/>                | <span data-ttu-id="81100-137">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="81100-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="81100-138">MOF</span><span class="sxs-lookup"><span data-stu-id="81100-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81100-139"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="81100-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="81100-140">DLL</span><span class="sxs-lookup"><span data-stu-id="81100-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81100-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81100-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81100-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81100-142">See also</span></span>

<dl> <dt>

<span data-ttu-id="81100-143">[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="81100-143">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="81100-144">**Win32- \_ Prozess**</span><span class="sxs-lookup"><span data-stu-id="81100-144">**Win32\_Process**</span></span>](win32-process.md)
</dt> </dl>

 

