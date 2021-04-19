---
description: Ändert vorhandene Schlüssel-Wert-Paare auf einem virtuellen Computer.
ms.assetid: A014F681-4429-4982-95AA-DF371925BB3B
title: Modifykvpitems-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyKvpItems
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6269e1a7794b6f04de606d13c90ef8dac1777369
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368900"
---
# <a name="modifykvpitems-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="0f4f4-103">Modifykvpitems-Methode der MSVM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="0f4f4-103">ModifyKvpItems method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="0f4f4-104">Ändert vorhandene Schlüssel-Wert-Paare auf einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="0f4f4-104">Modifies existing key-value pairs on a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f4f4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f4f4-105">Syntax</span></span>


```mof
uint32 ModifyKvpItems(
  [in]  CIM_ComputerSystem REF TargetSystem,
  [in]  string                 DataItems[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="0f4f4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f4f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f4f4-107">*TARGETSYSTEM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0f4f4-107">*TargetSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f4f4-108">Typ: **[ **CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)**</span><span class="sxs-lookup"><span data-stu-id="0f4f4-108">Type: **[**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)**</span></span>

<span data-ttu-id="0f4f4-109">Ein Verweis auf den virtuellen Computer, auf dem die Schlüssel-Wert-Paare geändert werden.</span><span class="sxs-lookup"><span data-stu-id="0f4f4-109">A reference to the virtual machine on which the key-value pairs will be modified.</span></span>

</dd> <dt>

<span data-ttu-id="0f4f4-110">*DataItems* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0f4f4-110">*DataItems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f4f4-111">Typ: **Zeichen \[ \] Folge**</span><span class="sxs-lookup"><span data-stu-id="0f4f4-111">Type: **string\[\]**</span></span>

<span data-ttu-id="0f4f4-112">Ein Array von Schlüssel-Wert-Paaren, die geändert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0f4f4-112">An array of key-value pairs to be modified.</span></span> <span data-ttu-id="0f4f4-113">Jedes Element des Arrays ist eine eingebettete Instanz der [**MSVM-Klasse \_ kvpexchangedataitem**](msvm-kvpexchangedataitem.md) .</span><span class="sxs-lookup"><span data-stu-id="0f4f4-113">Each element of the array is an embedded instance of the [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) class.</span></span> <span data-ttu-id="0f4f4-114">Diese Methode schlägt fehl, wenn eines der angegebenen Schlüssel-Wert-Paare nicht auf dem Zielsystem vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0f4f4-114">This method fails if any of the specified key-value pairs does not exist on the target system.</span></span> <span data-ttu-id="0f4f4-115">Dieses Array kann höchstens 128 Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="0f4f4-115">This array can contain at most 128 elements.</span></span>

</dd> <dt>

<span data-ttu-id="0f4f4-116">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0f4f4-116">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f4f4-117">Typ: **[ **CIM \_ bettejob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="0f4f4-117">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="0f4f4-118">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="0f4f4-118">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f4f4-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0f4f4-119">Return value</span></span>

<span data-ttu-id="0f4f4-120">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0f4f4-120">Type: **uint32**</span></span>

<span data-ttu-id="0f4f4-121">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="0f4f4-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="0f4f4-122">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="0f4f4-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0f4f4-123">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="0f4f4-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="0f4f4-124">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="0f4f4-124">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="0f4f4-125">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="0f4f4-125">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="0f4f4-126">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="0f4f4-126">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="0f4f4-127">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="0f4f4-127">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="0f4f4-128">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="0f4f4-128">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="0f4f4-129">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="0f4f4-129">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="0f4f4-130">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="0f4f4-130">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="0f4f4-131">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="0f4f4-131">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="0f4f4-132">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="0f4f4-132">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="0f4f4-133">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="0f4f4-133">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="0f4f4-134">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="0f4f4-134">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="0f4f4-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0f4f4-135">Remarks</span></span>

<span data-ttu-id="0f4f4-136">Der Zugriff auf die [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="0f4f4-136">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="0f4f4-137">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="0f4f4-137">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="0f4f4-138">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0f4f4-138">Examples</span></span>

<span data-ttu-id="0f4f4-139">Im folgenden c#-Beispiel werden Schlüssel-Wert-Paare auf einem virtuellen Computer geändert.</span><span class="sxs-lookup"><span data-stu-id="0f4f4-139">The following C# sample modifies key-value pairs on a virtual machine.</span></span> <span data-ttu-id="0f4f4-140">Die Dienstprogramme, auf die verwiesen wird, finden Sie unter [Allgemeine Hilfsprogramme für die Virtualisierungsbeispiele (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="0f4f4-140">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0f4f4-141">Der folgende Code muss auf dem Host Server des virtuellen Computers ausgeführt werden, und er muss mit Administrator Rechten ausgeführt werden, um ordnungsgemäß zu funktionieren.</span><span class="sxs-lookup"><span data-stu-id="0f4f4-141">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
using System;
using System.Management;

namespace HyperVSamples
{
    class ModifyKvpItemsClass
    {
        static void ModifyKvpItems(string vmName, string itemName, string itemValue)
        {
            ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
            ManagementObject virtualSystemService = Utility.GetServiceObject(scope, "Msvm_VirtualSystemManagementService");
            ManagementBaseObject inParams = virtualSystemService.GetMethodParameters("ModifyKvpItems");
            ManagementClass kvpExchangeDataItem = new ManagementClass(scope, new ManagementPath("Msvm_KvpExchangeDataItem"), null);

            ManagementObject dataItem = kvpExchangeDataItem.CreateInstance();
            
            dataItem["Data"] = itemValue;
            dataItem["Name"] = itemName;
            dataItem["Source"] = 0;

            string[] dataItems = new string[1];
            dataItems[0] = dataItem.GetText(TextFormat.CimDtd20);

            ManagementObject vm = Utility.GetTargetComputer(vmName, scope);
            inParams["TargetSystem"] = vm.Path.Path;
            inParams["DataItems"] = dataItems;

            ManagementBaseObject outParams = virtualSystemService.InvokeMethod("ModifyKvpItems", inParams, null);

            if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
            {
                if (Utility.JobCompleted(outParams, scope))
                {
                    Console.WriteLine("KvpItems were modified successfully.");
                }
                else
                {
                    Console.WriteLine("Failed to modify KvpItems");
                }
            }
            else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
            {
                Console.WriteLine("KvpItems were modified successfully.");
            }
            else
            {
                Console.WriteLine("Modify virtual system kvp items failed with error {0}", outParams["ReturnValue"]);
            }

            inParams.Dispose();
            outParams.Dispose();
            vm.Dispose();
            dataItem.Dispose();
            virtualSystemService.Dispose();
        }

        static void Main(string[] args)
        {
            if (args != null && args.Length != 3)
            {
                Console.WriteLine("Usage: ModifyKvpItems vmName itemName itemValue");
                return;
            }
            ModifyKvpItems(args[0], args[1], args[2]);
        }
    }
}
```



<span data-ttu-id="0f4f4-142">Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel werden Schlüssel-Wert-Paare auf einem virtuellen Computer geändert.</span><span class="sxs-lookup"><span data-stu-id="0f4f4-142">The following Visual Basic Scripting Edition (VBScript) sample modifies key-value pairs on a virtual machine.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0f4f4-143">Der folgende Code muss auf dem Host Server des virtuellen Computers ausgeführt werden, und er muss mit Administrator Rechten ausgeführt werden, um ordnungsgemäß zu funktionieren.</span><span class="sxs-lookup"><span data-stu-id="0f4f4-143">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```VB
option explicit 

dim objWMIService
dim managementService
dim fileSystem


const JobStarting = 3
const JobRunning = 4
const JobCompleted = 7
const wmiStarted = 4096
const wmiSuccessful = 0

Main()

'-----------------------------------------------------------------
' Main
'-----------------------------------------------------------------
Sub Main()

    dim computer, vmName, itemName, itemValue, myVm, objArgs
    
    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    computer = "."

    set objWMIService = GetObject("winmgmts:\\" & computer & "\root\virtualization\v2")
    set managementService = objWMIService.ExecQuery("select * from Msvm_VirtualSystemManagementService").ItemIndex(0)

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 3 then
        vmName = objArgs.Unnamed.Item(0)
        itemName = objArgs.Unnamed.Item(1)
        itemValue = objArgs.Unnamed.Item(2)
    else
        WScript.Echo "usage: cscript AddKvpItems.vbs vmName itemName itemValue"
        WScript.Quit(1)
    end if

    set myVm = GetComputerSystem(vmName)

    if ModifyKvpItems(myVm, itemName, itemValue) then

        WriteLog "Done"
        WScript.Quit(0)

    else
        WriteLog "ModifyKvpItems failed"
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
' RemoveVirtualSystemResource
'-----------------------------------------------------------------
Function ModifyKvpItems(computerSystem, itemName, itemValue)

    dim dataItem, dataItems, objInParam, objOutParams
    
    ModifyKvpItems = false
    
    set dataItem = objWMIService.Get("Msvm_KvpExchangeDataItem").SpawnInstance_()
    
    dataItem.Data = itemValue
    dataItem.Name = itemName
    dataItem.Source = 0
    
    dataItems = Array(1)
    dataItems(0) = dataItem.GetText_(1)
    
    set objInParam = managementService.Methods_("ModifyKvpItems").InParameters.SpawnInstance_()
    objInParam.TargetSystem = computerSystem.Path_.Path
    objInParam.dataItems = dataItems
    
    set objOutParams = managementService.ExecMethod_("ModifyKvpItems", objInParam)

    if objOutParams.ReturnValue = wmiStarted then
        if (WMIJobCompleted(objOutParams)) then
            ModifyKvpItems = true
        end if
    elseif objOutParams.ReturnValue = wmiSuccessful then
        ModifyKvpItems = true
    else
        WriteLog Format1("ModifyKvpItems failed with {0}", objOutParams.ReturnValue)
    end if

End Function

'-----------------------------------------------------------------
' Handle wmi Job object
'-----------------------------------------------------------------
Function WMIJobCompleted(outParam)

    dim WMIJob, jobState
    WMIJobCompleted = true

    set WMIJob = objWMIService.Get(outParam.Job)
    
    jobState = WMIJob.JobState

    while jobState = JobRunning or jobState = JobStarting
        WriteLog Format1("In progress... {0}% completed.",WMIJob.PercentComplete)
        WScript.Sleep(1000)
        set WMIJob = objWMIService.Get(outParam.Job)
        jobState = WMIJob.JobState
    wend

    if (WMIJob.JobState <> JobCompleted) then
        WriteLog Format1("ErrorDescription:{0}", WMIJob.ErrorDescription)
        WriteLog Format1("ErrorCode:{0}", WMIJob.ErrorCode)
        WMIJobCompleted = false
    end if
    
End Function

'-----------------------------------------------------------------
' Create the console log files.
'-----------------------------------------------------------------
Sub WriteLog(line)
    dim fileStream
    set fileStream = fileSystem.OpenTextFile(".\ModifyKvpItems.log", 8, true)
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



## <a name="requirements"></a><span data-ttu-id="0f4f4-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f4f4-144">Requirements</span></span>



| <span data-ttu-id="0f4f4-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0f4f4-145">Requirement</span></span> | <span data-ttu-id="0f4f4-146">Wert</span><span class="sxs-lookup"><span data-stu-id="0f4f4-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f4f4-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0f4f4-147">Minimum supported client</span></span><br/> | <span data-ttu-id="0f4f4-148">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0f4f4-148">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0f4f4-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0f4f4-149">Minimum supported server</span></span><br/> | <span data-ttu-id="0f4f4-150">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0f4f4-150">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0f4f4-151">Namespace</span><span class="sxs-lookup"><span data-stu-id="0f4f4-151">Namespace</span></span><br/>                | <span data-ttu-id="0f4f4-152">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="0f4f4-152">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0f4f4-153">MOF</span><span class="sxs-lookup"><span data-stu-id="0f4f4-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f4f4-154"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0f4f4-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0f4f4-155">DLL</span><span class="sxs-lookup"><span data-stu-id="0f4f4-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f4f4-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0f4f4-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0f4f4-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f4f4-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f4f4-158">**Modifykvpitems (v1)**</span><span class="sxs-lookup"><span data-stu-id="0f4f4-158">**ModifyKvpItems (V1)**</span></span>](/previous-versions/windows/desktop/virtual/modifykvpitems-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="0f4f4-159">**MSVM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="0f4f4-159">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

