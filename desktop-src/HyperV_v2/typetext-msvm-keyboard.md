---
description: Simuliert eine Reihe von typisierten Zeichen.
ms.assetid: 5D4C9F27-84AA-4131-A9A3-2C72DB2E8909
title: TypeText-Methode der Msvm_Keyboard-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.TypeText
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 37e8227a545975a6193be63a8bd363e10e9805f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351483"
---
# <a name="typetext-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="148fd-103">TypeText-Methode der MSVM- \_ Tastatur Klasse</span><span class="sxs-lookup"><span data-stu-id="148fd-103">TypeText method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="148fd-104">Simuliert eine Reihe von typisierten Zeichen.</span><span class="sxs-lookup"><span data-stu-id="148fd-104">Simulates a series of typed characters.</span></span> <span data-ttu-id="148fd-105">Dies entspricht dem Aufrufen von [**Press Key**](presskey-msvm-keyboard.md) gefolgt von [**releasekey**](releasekey-msvm-keyboard.md) für jedes Zeichen in der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="148fd-105">This is equivalent to calling [**PressKey**](presskey-msvm-keyboard.md) followed by [**ReleaseKey**](releasekey-msvm-keyboard.md) for each character in the string.</span></span>

## <a name="syntax"></a><span data-ttu-id="148fd-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="148fd-106">Syntax</span></span>


```mof
uint32 TypeText(
  [in] string asciiText
);
```



## <a name="parameters"></a><span data-ttu-id="148fd-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="148fd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="148fd-108">*asciitext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="148fd-108">*asciiText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="148fd-109">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="148fd-109">Type: **string**</span></span>

<span data-ttu-id="148fd-110">Die Reihe von ASCII-oder Unicode-Zeichen, die eingegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="148fd-110">The series of ASCII or Unicode characters to type.</span></span> <span data-ttu-id="148fd-111">Die maximale Länge dieser Zeichenfolge hängt vom Typ der Zeichen in der Zeichenfolge ab.</span><span class="sxs-lookup"><span data-stu-id="148fd-111">The maximum length of this string depends on the type of characters in the string.</span></span>



| <span data-ttu-id="148fd-112">Zeichenfolgentyp</span><span class="sxs-lookup"><span data-stu-id="148fd-112">String type</span></span>        | <span data-ttu-id="148fd-113">Maximale Zeichen Anzahl</span><span class="sxs-lookup"><span data-stu-id="148fd-113">Maximum characters</span></span>                                                               |
|--------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="148fd-114">ASCII</span><span class="sxs-lookup"><span data-stu-id="148fd-114">ASCII</span></span><br/>   | <span data-ttu-id="148fd-115">512</span><span class="sxs-lookup"><span data-stu-id="148fd-115">512</span></span><br/>                                                                   |
| <span data-ttu-id="148fd-116">Unicode</span><span class="sxs-lookup"><span data-stu-id="148fd-116">Unicode</span></span><br/> | <span data-ttu-id="148fd-117">256 bis 512, abhängig von der Anzahl der Ersatz Zeichenpaare in der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="148fd-117">256 to 512, depending on the number of surrogate pairs in the string.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="148fd-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="148fd-118">Return value</span></span>

<span data-ttu-id="148fd-119">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="148fd-119">Type: **uint32**</span></span>

<span data-ttu-id="148fd-120">Der Rückgabewert 0 (null) gibt den Erfolg an.</span><span class="sxs-lookup"><span data-stu-id="148fd-120">A return value of zero indicates success.</span></span> <span data-ttu-id="148fd-121">Der Rückgabewert 1 gibt einen Fehler an, der durch nicht übersetzbare Zeichen in der Eingabe Zeichenfolge verursacht wird.</span><span class="sxs-lookup"><span data-stu-id="148fd-121">A return value of one indicates a failure caused by nontranslatable characters in the input string.</span></span> <span data-ttu-id="148fd-122">Alle anderen Werte ungleich 0 (null) geben an, dass der Schlüssel Zustand nicht geändert werden konnte.</span><span class="sxs-lookup"><span data-stu-id="148fd-122">All other nonzero values indicate a failure to modify the key state.</span></span>

<dl> <dt>

<span data-ttu-id="148fd-123">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="148fd-123">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="148fd-124">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="148fd-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="148fd-125">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="148fd-125">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="148fd-126">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="148fd-126">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="148fd-127">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="148fd-127">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="148fd-128">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="148fd-128">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="148fd-129">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="148fd-129">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="148fd-130">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="148fd-130">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="148fd-131">Das **System wird verwendet** (32774).</span><span class="sxs-lookup"><span data-stu-id="148fd-131">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="148fd-132">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="148fd-132">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="148fd-133">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="148fd-133">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="148fd-134">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="148fd-134">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="148fd-135">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="148fd-135">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="148fd-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="148fd-136">Remarks</span></span>

<span data-ttu-id="148fd-137">Der Zugriff auf die [**MSVM- \_ Tastatur**](msvm-keyboard.md) Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="148fd-137">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="148fd-138">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="148fd-138">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="148fd-139">Beispiele</span><span class="sxs-lookup"><span data-stu-id="148fd-139">Examples</span></span>

<span data-ttu-id="148fd-140">Im folgenden c#-Beispiel wird die Eingabe von Text simuliert.</span><span class="sxs-lookup"><span data-stu-id="148fd-140">The following C# sample simulates typing text.</span></span> <span data-ttu-id="148fd-141">Die Dienstprogramme, auf die verwiesen wird, finden Sie unter [Allgemeine Hilfsprogramme für die Virtualisierungsbeispiele (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="148fd-141">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
using System;
using System.Management;

namespace HyperVSamples
{
    class TypeTextClass
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

        static void TypeText(string vmName, string text)
        {
            ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
            ManagementObject vm = Utility.GetTargetComputer(vmName, scope);
            ManagementObject keyboard = GetComputerKeyboard(vm);

            ManagementBaseObject inParams = keyboard.GetMethodParameters("TypeText");

            inParams["asciiText"] = text;

            ManagementBaseObject outParams = keyboard.InvokeMethod("TypeText", inParams, null);

            if ((UInt16)outParams["ReturnValue"] == ReturnCode.Completed)
            {
                string.Format("Text {0} was typed on {1}", text, vm["ElementName"]);
            }
            else
            {
                string.Format("Unable to type '{0}' on {1}", text, vm["ElementName"]);
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
                Console.WriteLine("Usage: TypeText vmName Text");
                return;
            }
            TypeText(args[0], args[1]);
        }
    }
}

```



<span data-ttu-id="148fd-142">Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel wird die Eingabe von Text simuliert.</span><span class="sxs-lookup"><span data-stu-id="148fd-142">The following Visual Basic Scripting Edition (VBScript) sample simulates typing text.</span></span>


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
    dim computer, objArgs, vmName, computerSystem, text, keyboard
    
    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    computer = "."
    set objWMIService = GetObject("winmgmts:\\" & computer & "\root\virtualization\v2")

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 2 then
       vmName= objArgs.Unnamed.Item(0)
       text = objArgs.Unnamed.Item(1)
    else
       WScript.Echo "usage: cscript TypeText.vbs vmName text"
       WScript.Quit
    end if
    
    set computerSystem = GetComputerSystem(vmName)
    set keyboard = GetComputerKeyboard(computerSystem)

    if TypeText(keyboard, text) then

        WriteLog "Done"
        WScript.Quit(0)
    else
        WriteLog "TypeText operation failed"
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
' Type the given text to the given keyboard
'-----------------------------------------------------------------
Function TypeText(keyboard, text)
    WriteLog Format2("TypeText({0}, {1})", keyboard.ElementName, text)
    
    dim objInParam, objOutParams

    TypeText = false
    set objInParam = keyboard.Methods_("TypeText").InParameters.SpawnInstance_()
    objInParam.asciiText = text

    set objOutParams = keyboard.ExecMethod_("TypeText", objInParam)

    if objOutParams.ReturnValue = wmiSuccessful then
        WriteLog Format2("'{0}' was typed on {1}", text, keyboard.ElementName)
        TypeText = true
    end if

End Function

'-----------------------------------------------------------------
' Create the console log files.
'-----------------------------------------------------------------
Sub WriteLog(line)
    dim fileStream
    set fileStream = fileSystem.OpenTextFile(".\Typetext.log", 8, true)
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



## <a name="requirements"></a><span data-ttu-id="148fd-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="148fd-143">Requirements</span></span>



| <span data-ttu-id="148fd-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="148fd-144">Requirement</span></span> | <span data-ttu-id="148fd-145">Wert</span><span class="sxs-lookup"><span data-stu-id="148fd-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="148fd-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="148fd-146">Minimum supported client</span></span><br/> | <span data-ttu-id="148fd-147">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="148fd-147">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="148fd-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="148fd-148">Minimum supported server</span></span><br/> | <span data-ttu-id="148fd-149">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="148fd-149">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="148fd-150">Namespace</span><span class="sxs-lookup"><span data-stu-id="148fd-150">Namespace</span></span><br/>                | <span data-ttu-id="148fd-151">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="148fd-151">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="148fd-152">MOF</span><span class="sxs-lookup"><span data-stu-id="148fd-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="148fd-153"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="148fd-153"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="148fd-154">DLL</span><span class="sxs-lookup"><span data-stu-id="148fd-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="148fd-155"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="148fd-155"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="148fd-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="148fd-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="148fd-157">**MSVM- \_ Tastatur**</span><span class="sxs-lookup"><span data-stu-id="148fd-157">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> </dl>

 

