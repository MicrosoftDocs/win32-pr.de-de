---
description: Fügt einem virtuellen Computer Schlüssel-Wert-Paare hinzu.
ms.assetid: D952EC3D-24EB-4A68-8527-5BF522957CB6
title: Addkvpitems-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddKvpItems
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e9e01a02615b8bb395a589160a765dec4e08526e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349867"
---
# <a name="addkvpitems-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="cd5cd-103">Addkvpitems-Methode der MSVM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="cd5cd-103">AddKvpItems method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="cd5cd-104">Fügt einem virtuellen Computer Schlüssel-Wert-Paare hinzu.</span><span class="sxs-lookup"><span data-stu-id="cd5cd-104">Adds key-value pairs to a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd5cd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd5cd-105">Syntax</span></span>


```mof
uint32 AddKvpItems(
  [in]  CIM_ComputerSystem REF TargetSystem,
  [in]  string                 DataItems[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="cd5cd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd5cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd5cd-107">*TARGETSYSTEM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cd5cd-107">*TargetSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd5cd-108">Typ: **[ **CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)**</span><span class="sxs-lookup"><span data-stu-id="cd5cd-108">Type: **[**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)**</span></span>

<span data-ttu-id="cd5cd-109">Ein Verweis auf ein [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Objekt, das den virtuellen Computer darstellt, auf dem die Schlüssel-Wert-Paare hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="cd5cd-109">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) object that represents the virtual machine on which the key-value pairs will be added.</span></span>

</dd> <dt>

<span data-ttu-id="cd5cd-110">*DataItems* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cd5cd-110">*DataItems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd5cd-111">Typ: **Zeichen \[ \] Folge**</span><span class="sxs-lookup"><span data-stu-id="cd5cd-111">Type: **string\[\]**</span></span>

<span data-ttu-id="cd5cd-112">Ein Array von Schlüssel-Wert-Paaren, die hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cd5cd-112">An array of key-value pairs to be added.</span></span> <span data-ttu-id="cd5cd-113">Jedes Element des Arrays ist eine eingebettete Instanz der [**MSVM-Klasse \_ kvpexchangedataitem**](msvm-kvpexchangedataitem.md) .</span><span class="sxs-lookup"><span data-stu-id="cd5cd-113">Each element of the array is an embedded instance of the [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) class.</span></span> <span data-ttu-id="cd5cd-114">Diese Methode schlägt fehl, wenn eines der angegebenen Schlüssel-Wert-Paare bereits auf dem Zielsystem vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="cd5cd-114">This method fails if any of the specified key-value pairs already exists on the target system.</span></span> <span data-ttu-id="cd5cd-115">Dieses Array kann höchstens 128 Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="cd5cd-115">This array can contain at most 128 elements.</span></span>

</dd> <dt>

<span data-ttu-id="cd5cd-116">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cd5cd-116">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd5cd-117">Typ: **[ **CIM \_ bettejob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="cd5cd-117">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="cd5cd-118">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="cd5cd-118">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd5cd-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cd5cd-119">Return value</span></span>

<span data-ttu-id="cd5cd-120">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd5cd-120">Type: **uint32**</span></span>

<span data-ttu-id="cd5cd-121">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="cd5cd-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="cd5cd-122">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="cd5cd-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cd5cd-123">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="cd5cd-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="cd5cd-124">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="cd5cd-124">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="cd5cd-125">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="cd5cd-125">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="cd5cd-126">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="cd5cd-126">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="cd5cd-127">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="cd5cd-127">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="cd5cd-128">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="cd5cd-128">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="cd5cd-129">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="cd5cd-129">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="cd5cd-130">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="cd5cd-130">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="cd5cd-131">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="cd5cd-131">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="cd5cd-132">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="cd5cd-132">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="cd5cd-133">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="cd5cd-133">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="cd5cd-134">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="cd5cd-134">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="cd5cd-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cd5cd-135">Remarks</span></span>

<span data-ttu-id="cd5cd-136">Der Zugriff auf die [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="cd5cd-136">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="cd5cd-137">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="cd5cd-137">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="cd5cd-138">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cd5cd-138">Examples</span></span>

<span data-ttu-id="cd5cd-139">Im folgenden c#-Beispiel werden Schlüssel-Wert-Paare zu einem virtuellen Computer hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd5cd-139">The following C# sample adds key-value pairs to a virtual machine.</span></span> <span data-ttu-id="cd5cd-140">Die Dienstprogramme, auf die verwiesen wird, finden Sie unter [Allgemeine Hilfsprogramme für die Virtualisierungsbeispiele (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="cd5cd-140">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cd5cd-141">Der folgende Code muss auf dem Host Server des virtuellen Computers ausgeführt werden, und er muss mit Administrator Rechten ausgeführt werden, um ordnungsgemäß zu funktionieren.</span><span class="sxs-lookup"><span data-stu-id="cd5cd-141">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
public static void AddKvpItems(string vmName, string itemName, string itemValue)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject virtualSystemService = Utility.GetServiceObject(scope, "Msvm_VirtualSystemManagementService");
    ManagementBaseObject inParams = virtualSystemService.GetMethodParameters("AddKvpItems");
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

    ManagementBaseObject outParams = virtualSystemService.InvokeMethod("AddKvpItems", inParams, null);

    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("Resources were added successfully.");

        }
        else
        {
            Console.WriteLine("Failed to add resources");
        }
    }
    else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
    {
        Console.WriteLine("Resources were added successfully.");
    }
    else
    {
        Console.WriteLine("Add virtual system Kvp items failed with error {0}", outParams["ReturnValue"]);
    }

    if (inParams != null)
    {
        inParams.Dispose();
    }

    if (outParams != null)
    {
        outParams.Dispose();
    }
}
```



<span data-ttu-id="cd5cd-142">Im folgenden Visual Basic Scripting Edition Beispiel (VBScript) werden einem virtuellen Computer Schlüssel-Wert-Paare hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="cd5cd-142">The following Visual Basic Scripting Edition (VBScript) sample adds key-value pairs to a virtual machine.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cd5cd-143">Der folgende Code muss auf dem Host Server des virtuellen Computers ausgeführt werden, und er muss mit Administrator Rechten ausgeführt werden, um ordnungsgemäß zu funktionieren.</span><span class="sxs-lookup"><span data-stu-id="cd5cd-143">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


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

    if AddKvpItems(myVm, itemName, itemValue) then

        WriteLog "Done"
        WScript.Quit(0)

    else
        WriteLog "AddKvpItems failed"
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
' AddKvpItems
'-----------------------------------------------------------------
Function AddKvpItems(computerSystem, itemName, itemValue)

    dim dataItem, dataItems, objInParam, objOutParams
    
    AddKvpItems = false
    
    set dataItem = objWMIService.Get("Msvm_KvpExchangeDataItem").SpawnInstance_()
    dataItem.Data = itemValue
    dataItem.Name = itemName
    dataItem.Source = 0
    
    dataItems = Array(1)
    dataItems(0) = dataItem.GetText_(1)
    
    set objInParam = managementService.Methods_("AddKvpItems").InParameters.SpawnInstance_()
    objInParam.TargetSystem = computerSystem.Path_.Path
    objInParam.DataItems = dataItems
    
    set objOutParams = managementService.ExecMethod_("AddKvpItems", objInParam)

    if objOutParams.ReturnValue = wmiStarted then
        if (WMIJobCompleted(objOutParams)) then
            AddKvpItems = true
        end if
    elseif (objOutParams.ReturnValue = wmiSuccessful) then
        AddKvpItems = true
    else
        WriteLog Format1("AddKvpItem failed with error {0}", objOutParams.ReturnValue)
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
    set fileStream = fileSystem.OpenTextFile(".\AddKvpItems.log", 8, true)
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



## <a name="requirements"></a><span data-ttu-id="cd5cd-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cd5cd-144">Requirements</span></span>



| <span data-ttu-id="cd5cd-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cd5cd-145">Requirement</span></span> | <span data-ttu-id="cd5cd-146">Wert</span><span class="sxs-lookup"><span data-stu-id="cd5cd-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd5cd-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cd5cd-147">Minimum supported client</span></span><br/> | <span data-ttu-id="cd5cd-148">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cd5cd-148">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="cd5cd-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cd5cd-149">Minimum supported server</span></span><br/> | <span data-ttu-id="cd5cd-150">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cd5cd-150">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cd5cd-151">Namespace</span><span class="sxs-lookup"><span data-stu-id="cd5cd-151">Namespace</span></span><br/>                | <span data-ttu-id="cd5cd-152">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="cd5cd-152">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="cd5cd-153">MOF</span><span class="sxs-lookup"><span data-stu-id="cd5cd-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd5cd-154"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="cd5cd-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd5cd-155">DLL</span><span class="sxs-lookup"><span data-stu-id="cd5cd-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd5cd-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cd5cd-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cd5cd-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd5cd-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd5cd-158">**MSVM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="cd5cd-158">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

