---
description: Simuliert einen Tastendruck.
ms.assetid: 42C11F92-6143-40D7-9C07-56A6514EB4D1
title: Presskey-Methode der Msvm_Keyboard-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.PressKey
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5e9f196c5af3f8946460564e56bb425ffc24b51c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351591"
---
# <a name="presskey-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="256b3-103">Presskey-Methode der MSVM- \_ Tastatur Klasse</span><span class="sxs-lookup"><span data-stu-id="256b3-103">PressKey method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="256b3-104">Simuliert einen Tastendruck.</span><span class="sxs-lookup"><span data-stu-id="256b3-104">Simulates a key press.</span></span> <span data-ttu-id="256b3-105">Bei erfolgreicher Ausführung wird der Schlüssel im Zustand "herunter" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="256b3-105">When successful the key will be in the down state.</span></span>

## <a name="syntax"></a><span data-ttu-id="256b3-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="256b3-106">Syntax</span></span>


```mof
uint32 PressKey(
  [in] uint32 keyCode
);
```



## <a name="parameters"></a><span data-ttu-id="256b3-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="256b3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="256b3-108">*Keycode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="256b3-108">*keyCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="256b3-109">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="256b3-109">Type: **uint32**</span></span>

<span data-ttu-id="256b3-110">Der Code für den virtuellen Schlüssel des zu druckenden Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="256b3-110">The virtual-key code of the key to press.</span></span> <span data-ttu-id="256b3-111">Die Liste der Codes für virtuelle Schlüssel finden Sie unter [**Code für virtuelle**](../inputdev/virtual-key-codes.md)Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="256b3-111">For the list for virtual-key codes, see [**Virtual-Key Codes**](../inputdev/virtual-key-codes.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="256b3-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="256b3-112">Return value</span></span>

<span data-ttu-id="256b3-113">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="256b3-113">Type: **uint32**</span></span>

<span data-ttu-id="256b3-114">Der Rückgabewert 0 (null) gibt den Erfolg an.</span><span class="sxs-lookup"><span data-stu-id="256b3-114">A return value of zero indicates success.</span></span> <span data-ttu-id="256b3-115">Ein Wert ungleich 0 (null) gibt an, dass der Schlüssel Zustand nicht geändert werden konnte.</span><span class="sxs-lookup"><span data-stu-id="256b3-115">A nonzero value indicates a failure to modify the key state.</span></span>

<dl> <dt>

<span data-ttu-id="256b3-116">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="256b3-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="256b3-117">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="256b3-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="256b3-118">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="256b3-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="256b3-119">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="256b3-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="256b3-120">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="256b3-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="256b3-121">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="256b3-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="256b3-122">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="256b3-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="256b3-123">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="256b3-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="256b3-124">Das **System wird verwendet** (32774).</span><span class="sxs-lookup"><span data-stu-id="256b3-124">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="256b3-125">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="256b3-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="256b3-126">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="256b3-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="256b3-127">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="256b3-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="256b3-128">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="256b3-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="256b3-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="256b3-129">Remarks</span></span>

<span data-ttu-id="256b3-130">Die **presskey** -Methode ordnet Verweise auf das **VK- \_ Menü** (18), das **VK- \_ Steuer** Element (17) und die **VK- \_ UMSCHALT** **Taste \_ (** 16) auf " **VK \_ lmenu** (164)", " **VK \_ lcontrol** (162)" und " **VK \_ LShift** (160)" **zu \_** **\_**</span><span class="sxs-lookup"><span data-stu-id="256b3-130">The **PressKey** method maps references to the **VK\_MENU** (18), **VK\_CONTROL** (17), and **VK\_SHIFT** (16) to **VK\_LMENU** (164), **VK\_LCONTROL** (162), and **VK\_LSHIFT** (160), respectively, because the **VK\_MENU**, **VK\_CONTROL**, and **VK\_SHIFT** virtual key codes do not represent real keys on a keyboard.</span></span>

<span data-ttu-id="256b3-131">Der Zugriff auf die [**MSVM- \_ Tastatur**](msvm-keyboard.md) Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="256b3-131">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="256b3-132">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="256b3-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="256b3-133">Beispiele</span><span class="sxs-lookup"><span data-stu-id="256b3-133">Examples</span></span>

<span data-ttu-id="256b3-134">Im folgenden c#-Beispiel wird ein Tastendruck simuliert.</span><span class="sxs-lookup"><span data-stu-id="256b3-134">The following C# sample simulates a key press.</span></span> <span data-ttu-id="256b3-135">Die Dienstprogramme, auf die verwiesen wird, finden Sie unter [Allgemeine Hilfsprogramme für die Virtualisierungsbeispiele (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="256b3-135">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
using System;
using System.Management;

namespace HyperVSamples
{
    class PressKeyClass
    {
        static ManagementObject GetComputerKeyboard(ManagementObject vm)
        {
            ManagementObjectCollection keyboardCollection = vm.GetRelated
            (
                "Msvm_Keyboard",
                "Msvm_SystemDevice",
                null,
                null,
                "PartComponent",
                "GroupComponent",
                false,
                null
            );

            ManagementObject keyboard = null;

            foreach (ManagementObject instance in keyboardCollection)
            {
                keyboard = instance;
                break;
            }

            return keyboard;
        }

        static void PressKey(string vmName, int keyCode)
        {
            ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
            ManagementObject vm = Utility.GetTargetComputer(vmName, scope);
            ManagementObject keyboard = GetComputerKeyboard(vm);

            ManagementBaseObject inParams = keyboard.GetMethodParameters("PressKey");

            inParams["keyCode"] = keyCode;

            ManagementBaseObject outParams = keyboard.InvokeMethod("PressKey", inParams, null);

            if ((UInt16)outParams["ReturnValue"] == ReturnCode.Completed)
            {
                string.Format("Key {0} was pressed on {1}", keyCode, vm["ElementName"]);
            }
            else
            {
                string.Format("Unable to press key {0}' on {1}", keyCode, vm["ElementName"]);
            }

            inParams.Dispose();
            outParams.Dispose();
            keyboard.Dispose();
            vm.Dispose();
        }

        static void Main(string[] args)
        {
            if (args != null && args.Length != 2)
            {
                Console.WriteLine("Usage: PressKey vmName keyCode");
                return;
            }
            string vmName = args[0];
            int keyCode = int.Parse(args[1]);
            PressKey(args[0], keyCode);
        }

    }
}

```



<span data-ttu-id="256b3-136">Das folgende Visual Basic Scripting Edition (VBScript)-Beispiel simuliert einen Tastendruck.</span><span class="sxs-lookup"><span data-stu-id="256b3-136">The following Visual Basic Scripting Edition (VBScript) sample simulates a key press.</span></span>


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
    
    dim computer, objArgs, vmName, computerSystem, keycode, keyboard
    
    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    computer = "."
    set objWMIService = GetObject("winmgmts:\\" & computer & "\root\virtualization\v2")

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 2 then
       vmName= objArgs.Unnamed.Item(0)
       keycode = objArgs.Unnamed.Item(1)
    else
       WScript.Echo "usage: cscript PressKey.vbs vmName keycode"
       WScript.Quit
    end if
    
    set computerSystem = GetComputerSystem(vmName)
    set keyboard = GetComputerKeyboard(computerSystem)

    if PressKey(keyboard, keycode) then

        WriteLog "Done"
        WScript.Quit(0)
    else
        WriteLog "PressKey failed"
        WScript.Quit(1)
    end if

End Sub

'-----------------------------------------------------------------
' Retrieve Msvm_VirtualComputerSystem from base on its ElementName
' 
'-----------------------------------------------------------------
Function GetComputerSystem(vmElementName)
    dim query
    On Error Resume Next
    query = Format1("select * from Msvm_ComputerSystem where ElementName = '{0}'", vmElementName)
    set GetComputerSystem = objWMIService.ExecQuery(query).ItemIndex(0)
    if (Err.Number <> 0) then
        WriteLog Format1("Err.Number: {0}", Err.Number)
        WriteLog Format1("Err.Description:{0}",Err.Description)
        WScript.Quit(1)
    end if
End Function


'-----------------------------------------------------------------
' Retrieve Msvm_Keyboard from given computer system
' 
'-----------------------------------------------------------------
Function GetComputerKeyboard(computerSystem)
    dim query
    On Error Resume Next
    query = Format1("ASSOCIATORS OF {{0}} WHERE resultClass = Msvm_Keyboard", computerSystem.Path_.Path)
    set GetComputerKeyboard = objWMIService.ExecQuery(query).ItemIndex(0)
    if (Err.Number <> 0) then
        WriteLog Format1("Err.Number: {0}", Err.Number)
        WriteLog Format1("Err.Description:{0}",Err.Description)
        WScript.Quit(1)
    end if
End Function

'-----------------------------------------------------------------
' Press the key with the given key code on the given keyboard
'-----------------------------------------------------------------
Function PressKey(keyboard, keyCode)
    WriteLog Format2("PressKey({0}, {1})", keyboard.ElementName, keyCode)
    
    dim objInParam, objOutParams
    
    PressKey = false
    set objInParam = keyboard.Methods_("PressKey").InParameters.SpawnInstance_()
    objInParam.keyCode = keyCode

    set objOutParams = keyboard.ExecMethod_("PressKey", objInParam)

    if objOutParams.ReturnValue = wmiSuccessful then
        WriteLog Format2("The key with code '{0}' is typed on {1}.", keyCode, keyboard.ElementName)
        PressKey = true
    end if

End Function

'-----------------------------------------------------------------
' Create the console log files.
'-----------------------------------------------------------------
Sub WriteLog(line)
    dim fileStream
    set fileStream = fileSystem.OpenTextFile(".\PressKey.log", 8, true)
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



## <a name="requirements"></a><span data-ttu-id="256b3-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="256b3-137">Requirements</span></span>



| <span data-ttu-id="256b3-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="256b3-138">Requirement</span></span> | <span data-ttu-id="256b3-139">Wert</span><span class="sxs-lookup"><span data-stu-id="256b3-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="256b3-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="256b3-140">Minimum supported client</span></span><br/> | <span data-ttu-id="256b3-141">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="256b3-141">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="256b3-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="256b3-142">Minimum supported server</span></span><br/> | <span data-ttu-id="256b3-143">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="256b3-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="256b3-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="256b3-144">Namespace</span></span><br/>                | <span data-ttu-id="256b3-145">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="256b3-145">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="256b3-146">MOF</span><span class="sxs-lookup"><span data-stu-id="256b3-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="256b3-147"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="256b3-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="256b3-148">DLL</span><span class="sxs-lookup"><span data-stu-id="256b3-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="256b3-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="256b3-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="256b3-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="256b3-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="256b3-151">**MSVM- \_ Tastatur**</span><span class="sxs-lookup"><span data-stu-id="256b3-151">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> <dt>

[<span data-ttu-id="256b3-152">**Codes von virtuellen Schlüsseln**</span><span class="sxs-lookup"><span data-stu-id="256b3-152">**Virtual-Key Codes**</span></span>](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

