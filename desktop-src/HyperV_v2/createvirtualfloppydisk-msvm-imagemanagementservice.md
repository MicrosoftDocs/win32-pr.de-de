---
description: Erstellt eine virtuelle Disketten Datei.
ms.assetid: C7B5712C-55DD-4784-8B2E-A8DE02E4CFD8
title: Die Methode "kreatevirtualfloppydisk" der Msvm_ImageManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.CreateVirtualFloppyDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 98781a4f72218ee61a4966dc76b21f7417353e0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355305"
---
# <a name="createvirtualfloppydisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="d3174-103">Die Methode "kreatevirtualfloppydisk" der Klasse "MSVM \_ imagemanagementservice"</span><span class="sxs-lookup"><span data-stu-id="d3174-103">CreateVirtualFloppyDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="d3174-104">Erstellt eine virtuelle Disketten Datei.</span><span class="sxs-lookup"><span data-stu-id="d3174-104">Creates a virtual floppy disk file.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3174-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3174-105">Syntax</span></span>


```mof
uint32 CreateVirtualFloppyDisk(
  [in]  string              Path,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="d3174-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3174-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3174-107">*Pfad* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d3174-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3174-108">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d3174-108">Type: **string**</span></span>

<span data-ttu-id="d3174-109">Ein voll qualifizierter Pfad, der den Speicherort der neuen Datei angibt.</span><span class="sxs-lookup"><span data-stu-id="d3174-109">A fully qualified path that specifies the location of the new file.</span></span>

</dd> <dt>

<span data-ttu-id="d3174-110">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d3174-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3174-111">Typ: **[ **CIM \_ bettejob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="d3174-111">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="d3174-112">Ein Verweis auf den Auftrag (kann **null** sein, wenn die Aufgabe abgeschlossen ist).</span><span class="sxs-lookup"><span data-stu-id="d3174-112">A reference to the job (can be **Null** if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3174-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d3174-113">Return value</span></span>

<span data-ttu-id="d3174-114">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d3174-114">Type: **uint32**</span></span>

<span data-ttu-id="d3174-115">Diese Methode kann einen der folgenden Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="d3174-115">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="d3174-116">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="d3174-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d3174-117">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="d3174-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d3174-118">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="d3174-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="d3174-119">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="d3174-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="d3174-120">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="d3174-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="d3174-121">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="d3174-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="d3174-122">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="d3174-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="d3174-123">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="d3174-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="d3174-124">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="d3174-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="d3174-125">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="d3174-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="d3174-126">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="d3174-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="d3174-127">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="d3174-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="d3174-128">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="d3174-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="d3174-129">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="d3174-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="d3174-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d3174-130">Remarks</span></span>

<span data-ttu-id="d3174-131">Der Zugriff auf die [**MSVM \_ imagemanagementservice**](msvm-imagemanagementservice.md) -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="d3174-131">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="d3174-132">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="d3174-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="d3174-133">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d3174-133">Examples</span></span>

<span data-ttu-id="d3174-134">Im folgenden c#-Beispiel wird eine virtuelle Disketten Datei erstellt.</span><span class="sxs-lookup"><span data-stu-id="d3174-134">The following C# example creates a virtual floppy disk file.</span></span> <span data-ttu-id="d3174-135">Die Dienstprogramme, auf die verwiesen wird, finden Sie unter [Allgemeine Hilfsprogramme für die Virtualisierungsbeispiele (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="d3174-135">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
using System;
using System.Management;

namespace HyperVSamples
{
    class CreateVFD
    {
        static void CreateVirtualFlopy(string vhdPath)
        {
            ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
            ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

            ManagementBaseObject inParams = imageService.GetMethodParameters("CreateVirtualFloppyDisk");
            inParams["Path"] = vhdPath;
            ManagementBaseObject outParams = imageService.InvokeMethod("CreateVirtualFloppyDisk", inParams, null);
            if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
            {
                if (Utility.JobCompleted(outParams, scope))
                {
                    Console.WriteLine("{0} was created successfully.", inParams["Path"]);
                }
                else
                {
                    Console.WriteLine("Unable to create {0}", inParams["Path"]);
                }
            }

            inParams.Dispose();
            outParams.Dispose();
            imageService.Dispose();
        }

        static void Main(string[] args)
        {
            if (args != null && args.Length != 1)
            {
                Console.WriteLine("Usage: CreateVFD path");
                return;
            }
            CreateVirtualFlopy(args[0]);
        }
    }
}

```



<span data-ttu-id="d3174-136">Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel wird eine virtuelle Disketten Datei erstellt.</span><span class="sxs-lookup"><span data-stu-id="d3174-136">The following Visual Basic Scripting Edition (VBScript) example creates a virtual floppy disk file.</span></span>


```VB
option explicit 

dim objWMIService
dim managementService
dim fileSystem


const JobStarting = 3
const JobRunning = 4
const JobCompleted = 7
const wmiStarted = 4096

const method = "CreateVirtualFloppyDisk"
Main()

'-----------------------------------------------------------------
' Main
'-----------------------------------------------------------------
Sub Main()

    dim computer, objArgs, vfdPath

    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    computer = "."
    set objWMIService = GetObject("winmgmts:\\" & computer & "\root\virtualization\v2")
    set managementService = objWMIService.ExecQuery("Select * from Msvm_ImageManagementService").ItemIndex(0)

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 1 then
       vfdPath = objArgs.Unnamed.Item(0)
    else
       WScript.Echo "usage: cscript CreateVFD.vbs VFDFilePath "
       WScript.Quit(1)
    end if

    if CreateVirtualFloppyDisk(vfdPath) then
        WriteLog "Done"
        WScript.Quit(0)
    else
        WriteLog "CreateVFD failed"
        WScript.Quit(1)
    end if

End Sub

'-----------------------------------------------------------------
' Execute CreateVirtualFloppyDisk method
'-----------------------------------------------------------------
Function CreateVirtualFloppyDisk(vfdPath)
    WriteLog Format1("Function CreateVirtualFloppyDisk({0})",  vfdPath)
    
    dim objInParam, objOutParams

    CreateVirtualFloppyDisk = false

    set objInParam = managementService.Methods_("CreateVirtualFloppyDisk").InParameters.SpawnInstance_()
    objInParam.Path = vfdPath

    set objOutParams = managementService.ExecMethod_("CreateVirtualFloppyDisk", objInParam)

    if (WMIMethodStarted(objOutParams)) then
        if (WMIJobCompleted(objOutParams)) then
            WriteLog Format1("VHD {0} was created successfully", vfdPath)
            CreateVirtualFloppyDisk = true
        end if
    end if

End Function


'-----------------------------------------------------------------
' Handle wmi return values
'-----------------------------------------------------------------
Function WMIMethodStarted(outParam)
    WriteLog "Function WMIMethodStarted"
    
    dim wmiStatus
    
    WMIMethodStarted = false

    if Not IsNull(outParam) then
        wmiStatus = outParam.ReturnValue

        if  wmiStatus = wmiStarted then
            WMIMethodStarted = true
        else
            WriteLog Format2("Failed to create VFD {0} ConcreteJob with error {1}", vfdPath, wmiStatus)
        end if
   end if

End Function

'-----------------------------------------------------------------
' Handle wmi Job object
'-----------------------------------------------------------------
Function WMIJobCompleted(outParam)
    WriteLog "Function WMIJobCompleted"
    dim WMIJob, jobState

    set WMIJob = objWMIService.Get(outParam.Job)

    WMIJobCompleted = true

    jobState = WMIJob.JobState

    while jobState = JobRunning or jobState = JobStarting
        WriteLog Format1("In progress... {0}% completed.",WMIJob.PercentComplete)
        WScript.Sleep(1000)
        set WMIJob = objWMIService.Get(outParam.Job)
        jobState = WMIJob.JobState
    wend

    if (jobState <> JobCompleted) then
        WriteLog Format1("ErrorCode:{0}", WMIJob.ErrorCode)
        WriteLog Format1("ErrorDescription:{0}", WMIJob.ErrorDescription)
        WMIJobCompleted = false
    end if

End Function

'-----------------------------------------------------------------
' Create the console log files.
'-----------------------------------------------------------------
Sub WriteLog(line)
    dim fileStream
    set fileStream = fileSystem.OpenTextFile(".\CreateVFD.log", 8, true)
    WScript.Echo line
    fileStream.WriteLine line
    fileStream.Close

End Sub

'------------------------------------------------------------------------------
' The string formatting functions to avoid string concatenation.
'------------------------------------------------------------------------------
Function Format2(myString, arg0, arg1)
    Format2 = Format1(myString, arg0)
    Format2 = Replace(Format2, "{1}", arg1)
End Function

'------------------------------------------------------------------------------
' The string formatting functions to avoid string concatenation.
'------------------------------------------------------------------------------
Function Format1(myString, arg0)
    Format1 = Replace(myString, "{0}", arg0)
End Function
```



## <a name="requirements"></a><span data-ttu-id="d3174-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d3174-137">Requirements</span></span>



| <span data-ttu-id="d3174-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d3174-138">Requirement</span></span> | <span data-ttu-id="d3174-139">Wert</span><span class="sxs-lookup"><span data-stu-id="d3174-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3174-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d3174-140">Minimum supported client</span></span><br/> | <span data-ttu-id="d3174-141">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3174-141">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d3174-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d3174-142">Minimum supported server</span></span><br/> | <span data-ttu-id="d3174-143">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3174-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d3174-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="d3174-144">Namespace</span></span><br/>                | <span data-ttu-id="d3174-145">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="d3174-145">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d3174-146">MOF</span><span class="sxs-lookup"><span data-stu-id="d3174-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d3174-147"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="d3174-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d3174-148">DLL</span><span class="sxs-lookup"><span data-stu-id="d3174-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3174-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d3174-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d3174-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3174-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="d3174-151">[**CIM- \_ concretejob**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d3174-151">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d3174-152">**MSVM \_ imagemanagementservice**</span><span class="sxs-lookup"><span data-stu-id="d3174-152">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

