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
# <a name="clickbutton-method-of-the-msvm_syntheticmouse-class"></a>ClickButton-Methode der MSVM- \_ syntheticmouse-Klasse

Simuliert einen Klick auf die Schaltfläche der angegebenen Geräte Schaltfläche.

## <a name="syntax"></a>Syntax


```mof
uint32 ClickButton(
  [in] uint32 buttonIndex
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ButtonIndex* \[ in\]
</dt> <dd>

Typ: **UInt32**

Der 1-basierte Index der Schaltfläche.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Der Rückgabewert 0 (null) gibt den Erfolg an. Ein Wert ungleich NULL gibt an, dass der Zustand der Schaltfläche nicht geändert werden konnte.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)
</dt> <dt>

Fehler **(32768** )
</dt> <dt>

**Zugriff verweigert** (32769)
</dt> <dt>

**Nicht unterstützt** (32770)
</dt> <dt>

Der **Status ist "Unknown** " (32771).
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Ungültiger Parameter** (32773)
</dt> <dt>

Das **System wird verwendet** (32774).
</dt> <dt>

**Ungültiger Status für diesen Vorgang** (32775).
</dt> <dt>

**Falscher Datentyp** (32776).
</dt> <dt>

Das **System ist nicht verfügbar** (32777).
</dt> <dt>

**Nicht** genügend Arbeitsspeicher (32778)
</dt> </dl>

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die [**MSVM \_ syntheticmouse**](msvm-syntheticmouse.md) -Klasse kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Beispiele

Im folgenden c#-Beispiel wird ein Klick auf eine Schaltfläche simuliert. Die Dienstprogramme, auf die verwiesen wird, finden Sie unter [Allgemeine Hilfsprogramme für die Virtualisierungsbeispiele (v2)](common-utilities-for-the-virtualization-samples-v2.md).


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



Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel wird ein Klick auf eine Schaltfläche simuliert.


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



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM \_ syntheticmouse**](msvm-syntheticmouse.md)
</dt> </dl>

 

