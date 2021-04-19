---
description: Simuliert einen Klick auf die Schaltfläche der angegebenen Geräte Schaltfläche.
ms.assetid: 1153BF91-F1F6-4E0A-8100-7625A3C73BB3
title: ClickButton-Methode der Msvm_SyntheticMouse-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse.ClickButton
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2f5ea8e1f5984bd7e4b77222d6cbd8a05d1ed40b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368810"
---
# <a name="clickbutton-method-of-the-msvm_syntheticmouse-class"></a><span data-ttu-id="53033-103">ClickButton-Methode der MSVM- \_ syntheticmouse-Klasse</span><span class="sxs-lookup"><span data-stu-id="53033-103">ClickButton method of the Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="53033-104">Simuliert einen Klick auf die Schaltfläche der angegebenen Geräte Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="53033-104">Simulates a button click of the specified device button.</span></span>

## <a name="syntax"></a><span data-ttu-id="53033-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="53033-105">Syntax</span></span>


```mof
uint32 ClickButton(
  [in] uint32 buttonIndex
);
```



## <a name="parameters"></a><span data-ttu-id="53033-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="53033-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53033-107">*ButtonIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53033-107">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53033-108">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="53033-108">Type: **uint32**</span></span>

<span data-ttu-id="53033-109">Der 1-basierte Index der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="53033-109">The 1-based index of the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53033-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="53033-110">Return value</span></span>

<span data-ttu-id="53033-111">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="53033-111">Type: **uint32**</span></span>

<span data-ttu-id="53033-112">Der Rückgabewert 0 (null) gibt den Erfolg an.</span><span class="sxs-lookup"><span data-stu-id="53033-112">A return value of zero indicates success.</span></span> <span data-ttu-id="53033-113">Ein Wert ungleich NULL gibt an, dass der Zustand der Schaltfläche nicht geändert werden konnte.</span><span class="sxs-lookup"><span data-stu-id="53033-113">A nonzero value indicates a failure to modify the button state.</span></span>

<dl> <dt>

<span data-ttu-id="53033-114">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="53033-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="53033-115">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="53033-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="53033-116">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="53033-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="53033-117">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="53033-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="53033-118">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="53033-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="53033-119">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="53033-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="53033-120">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="53033-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="53033-121">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="53033-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="53033-122">Das **System wird verwendet** (32774).</span><span class="sxs-lookup"><span data-stu-id="53033-122">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="53033-123">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="53033-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="53033-124">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="53033-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="53033-125">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="53033-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="53033-126">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="53033-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="53033-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="53033-127">Remarks</span></span>

<span data-ttu-id="53033-128">Der Zugriff auf die [**MSVM \_ syntheticmouse**](msvm-syntheticmouse.md) -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="53033-128">Access to the [**Msvm\_SyntheticMouse**](msvm-syntheticmouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="53033-129">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="53033-129">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="53033-130">Beispiele</span><span class="sxs-lookup"><span data-stu-id="53033-130">Examples</span></span>

<span data-ttu-id="53033-131">Im folgenden c#-Beispiel wird ein Klick auf eine Schaltfläche simuliert.</span><span class="sxs-lookup"><span data-stu-id="53033-131">The following C# sample simulates a button click.</span></span> <span data-ttu-id="53033-132">Die Dienstprogramme, auf die verwiesen wird, finden Sie unter [Allgemeine Hilfsprogramme für die Virtualisierungsbeispiele (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="53033-132">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
using System;
using System.Management;

namespace HyperVSamples
{
    class ClickButtonClass
    {
        static ManagementObject GetComputerMouse(ManagementObject vm)
        {
            ManagementObjectCollection mouseCollection = vm.GetRelated
            (
                "Msvm_SyntheticMouse",
                "Msvm_SystemDevice",
                null,
                null,
                "PartComponent",
                "GroupComponent",
                false,
                null
            );

            ManagementObject mouse = null;

            foreach (ManagementObject instance in mouseCollection)
            {
                mouse = instance;
                break;
            }

            return mouse;
        }

        static ManagementObject GetVideoHead(ManagementObject vm)
        {
            ManagementObjectCollection videoControllers = vm.GetRelated
             (
                 "Msvm_SyntheticDisplayController",
                 "Msvm_SystemDevice",
                 null,
                 null,
                 "PartComponent",
                 "GroupComponent",
                 false,
                 null
             );

            ManagementObject videoController = null;

            foreach (ManagementObject instance in videoControllers)
            {
                videoController = instance;
                break;
            }

            ManagementObjectCollection videoHeads = videoController.GetRelated
             (
                 "Msvm_VideoHead",
                 "Msvm_VideoHeadOnController",
                 null,
                 null,
                 "Dependent",
                 "Antecedent",
                 false,
                 null
             );

            ManagementObject videoHead = null;

            foreach (ManagementObject instance in videoHeads)
            {
                videoHead = instance;
                break;
            }

            videoController.Dispose();

            return videoHead;
        }

        static bool SetMousePosition(ManagementObject mouse, ManagementObject video)
        {
            bool passed = false;
            
            ManagementBaseObject inParams = mouse.GetMethodParameters("setAbsolutePosition");

            inParams["horizontalPosition"] = 1;
            inParams["verticalPosition"] = Convert.ToInt32(video["CurrentVerticalResolution"]) - 1;

            ManagementBaseObject outParams = mouse.InvokeMethod("setAbsolutePosition", inParams, null);

            if ((UInt16)outParams["ReturnValue"] == ReturnCode.Completed)
            {
                Console.WriteLine("Mouse position is set at (1,{0})", inParams["verticalPosition"]);
                passed = true;
            }
            else
            {
                Console.WriteLine("setAbsolutePosition operation failed with {0} error.", outParams["ReturnValue"]);
            }

            inParams.Dispose();
            outParams.Dispose();

            return passed;

        }

        static void ClickButton(string vmName, int buttonIndex)
        {
            ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
            ManagementObject vm = Utility.GetTargetComputer(vmName, scope);
            ManagementObject videoHead = GetVideoHead(vm);
            ManagementObject mouse = GetComputerMouse(vm);

            if (!SetMousePosition(mouse, videoHead))
            {
                return;
            }

            ManagementBaseObject inParams = mouse.GetMethodParameters("ClickButton");

            inParams["buttonIndex"] = buttonIndex;

            ManagementBaseObject outParams = mouse.InvokeMethod("ClickButton", inParams, null);

            if ((UInt16)outParams["ReturnValue"] == ReturnCode.Completed)
            {
                string.Format("Button {0} was clicked on {1}", buttonIndex, vm["ElementName"]);
            }
            else
            {
                string.Format("Unable to click button {0}' on {1}", buttonIndex, vm["ElementName"]);
            }

            inParams.Dispose();
            outParams.Dispose();
            mouse.Dispose();
            vm.Dispose();
        }

        static void Main(string[] args)
        {
            if (args != null && args.Length != 2)
            {
                Console.WriteLine("Usage: ClickButton vmName buttonIndex");
                return;
            }
            ClickButton(args[0], Convert.ToInt32(args[1]));
        }
    }
}
```



<span data-ttu-id="53033-133">Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel wird ein Klick auf eine Schaltfläche simuliert.</span><span class="sxs-lookup"><span data-stu-id="53033-133">The following Visual Basic Scripting Edition (VBScript) sample simulates a button click.</span></span>


```VB
option explicit 

dim objWMIService
dim fileSystem

const wmiSuccessful = 0

Main()

'-----------------------------------------------------------------
' Main routine
'-----------------------------------------------------------------
Sub Main()
    
    dim vmName, computer, objArgs, mouse, video, computerSystem, buttonIndex
    
    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    computer = "."
    set objWMIService = GetObject("winmgmts:\\" & computer & "\root\virtualization\v2")

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 2 then
       vmName= objArgs.Unnamed.Item(0)
       buttonIndex = objArgs.Unnamed.Item(1)
    else
       WScript.Echo "usage: cscript ClickButton.vbs vmName buttonIndex"
       WScript.Quit
    end if
    
    set computerSystem = GetComputerSystem(vmName)
    set mouse = GetComputerMouse(computerSystem)
    set video = GetComputerVideoHead(computerSystem)

    if ClickButton(mouse, buttonIndex, video) then

        WriteLog "Done"
        WScript.Quit(0)
    else
        WriteLog "ClickButton failed"
        WScript.Quit(1)
    end if

End Sub

'-----------------------------------------------------------------
' Retrieve Msvm_VirtualComputerSystem from base on its ElementName
'-----------------------------------------------------------------
Function GetComputerSystem(vmElementName)
    On Error Resume Next
    dim query
    query = Format1("select * from Msvm_ComputerSystem where ElementName = '{0}'", vmElementName)
    set GetComputerSystem = objWMIService.ExecQuery(query).ItemIndex(0)
    if (Err.Number <> 0) then
        WriteLog Format1("Err.Number: {0}", Err.Number)
        WriteLog Format1("Err.Description:{0}",Err.Description)
        WScript.Quit(1)
    end if
End Function


'-----------------------------------------------------------------
' Retrieve Msvm_SyntheticMouse from given computer system
'-----------------------------------------------------------------
Function GetComputerMouse(computerSystem)
    On Error Resume Next
    dim query
    query = Format1("ASSOCIATORS OF {{0}} WHERE resultClass = Msvm_SyntheticMouse", computerSystem.Path_.Path)
    set GetComputerMouse = objWMIService.ExecQuery(query).ItemIndex(0)
    if (Err.Number <> 0) then
        WriteLog Format1("Err.Number: {0}", Err.Number)
        WriteLog Format1("Err.Description:{0}",Err.Description)
        WScript.Quit(1)
    end if
End Function


'-----------------------------------------------------------------
' Retrieve Msvm_VideoHead from given computer system
'-----------------------------------------------------------------
Function GetComputerVideoHead(computerSystem)
    On Error Resume Next
    dim query, controller
    query = Format1("ASSOCIATORS OF {{0}} WHERE resultClass = Msvm_SyntheticDisplayController", computerSystem.Path_.Path)
    set controller = objWMIService.ExecQuery(query).ItemIndex(0)
    if (Err.Number <> 0) then
        WriteLog Format1("Err.Number: {0}", Err.Number)
        WriteLog Format1("Err.Description:{0}",Err.Description)
        WScript.Quit(1)
    end if
    
    query = Format1("ASSOCIATORS OF {{0}} WHERE resultClass = Msvm_VideoHead", controller.Path_.Path)
    set GetComputerVideoHead = objWMIService.ExecQuery(query).ItemIndex(0)
    if (Err.Number <> 0) then
        WriteLog Format1("Err.Number: {0}", Err.Number)
        WriteLog Format1("Err.Description:{0}",Err.Description)
        WScript.Quit(1)
    end if    
End Function
'-----------------------------------------------------------------
' set mouse relative position on a virtual machine
'-----------------------------------------------------------------
Function setAbsolutePosition(mouse, video)
    WriteLog Format1("setAbsolutePosition({0})", mouse.ElementName)
    
    dim objInParam, objOutParams
    
    setAbsolutePosition = false
    set objInParam = mouse.Methods_("setAbsolutePosition").InParameters.SpawnInstance_()
    objInParam.horizontalPosition = 1
    objInParam.verticalPosition = video.CurrentVerticalResolution - 1

    set objOutParams = mouse.ExecMethod_("setAbsolutePosition", objInParam)

    if objOutParams.ReturnValue = wmiSuccessful then
        WriteLog Format1("Mouse position is set at (1,{0})", objInParam.verticalPosition)
        setAbsolutePosition = true
    end if

End Function

'-----------------------------------------------------------------
' Click mouse on a virtual machine
'-----------------------------------------------------------------
Function ClickButton(mouse, buttonIndex, video)
    WriteLog Format2("ClickButton({0}, {1})", mouse.ElementName, buttonIndex)
    
    dim objInParam, objOutParams
    
    ClickButton = false
    if Not setAbsolutePosition(mouse, video) then
        Exit Function
    end if


    set objInParam = mouse.Methods_("ClickButton").InParameters.SpawnInstance_()
    objInParam.buttonIndex = buttonIndex

    set objOutParams = mouse.ExecMethod_("ClickButton", objInParam)

    if objOutParams.ReturnValue = wmiSuccessful then
        WriteLog Format2("{0} button {1} was clicked.", mouse.ElementName, buttonIndex)
        ClickButton = true
    end if

End Function

'-----------------------------------------------------------------
' Create the console log files.
'-----------------------------------------------------------------
Sub WriteLog(line)
    dim fileStream
    set fileStream = fileSystem.OpenTextFile(".\clickButton.log", 8, true)
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



## <a name="requirements"></a><span data-ttu-id="53033-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53033-134">Requirements</span></span>



| <span data-ttu-id="53033-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="53033-135">Requirement</span></span> | <span data-ttu-id="53033-136">Wert</span><span class="sxs-lookup"><span data-stu-id="53033-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53033-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="53033-137">Minimum supported client</span></span><br/> | <span data-ttu-id="53033-138">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="53033-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="53033-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="53033-139">Minimum supported server</span></span><br/> | <span data-ttu-id="53033-140">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="53033-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="53033-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="53033-141">Namespace</span></span><br/>                | <span data-ttu-id="53033-142">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="53033-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="53033-143">MOF</span><span class="sxs-lookup"><span data-stu-id="53033-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="53033-144"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="53033-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="53033-145">DLL</span><span class="sxs-lookup"><span data-stu-id="53033-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53033-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="53033-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="53033-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53033-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53033-148">**MSVM \_ syntheticmouse**</span><span class="sxs-lookup"><span data-stu-id="53033-148">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)
</dt> </dl>

 

