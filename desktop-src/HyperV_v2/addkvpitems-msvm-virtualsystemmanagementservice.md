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
# <a name="addkvpitems-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Addkvpitems-Methode der MSVM \_ virtualsystemmanagementservice-Klasse

Fügt einem virtuellen Computer Schlüssel-Wert-Paare hinzu.

## <a name="syntax"></a>Syntax


```mof
uint32 AddKvpItems(
  [in]  CIM_ComputerSystem REF TargetSystem,
  [in]  string                 DataItems[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*TARGETSYSTEM* \[ in\]
</dt> <dd>

Typ: **[ **CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)**

Ein Verweis auf ein [**CIM \_ Computersystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) -Objekt, das den virtuellen Computer darstellt, auf dem die Schlüssel-Wert-Paare hinzugefügt werden.

</dd> <dt>

*DataItems* \[ in\]
</dt> <dd>

Typ: **Zeichen \[ \] Folge**

Ein Array von Schlüssel-Wert-Paaren, die hinzugefügt werden sollen. Jedes Element des Arrays ist eine eingebettete Instanz der [**MSVM-Klasse \_ kvpexchangedataitem**](msvm-kvpexchangedataitem.md) . Diese Methode schlägt fehl, wenn eines der angegebenen Schlüssel-Wert-Paare bereits auf dem Zielsystem vorhanden ist. Dieses Array kann höchstens 128 Elemente enthalten.

</dd> <dt>

*Auftrag* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **CIM \_ bettejob**](/previous-versions//cc136808(v=vs.85))**

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **UInt32**

Diese Methode gibt einen der folgenden Werte zurück.

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

**System wird verwendet** (32774)
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

Der Zugriff auf die [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Beispiele

Im folgenden c#-Beispiel werden Schlüssel-Wert-Paare zu einem virtuellen Computer hinzugefügt. Die Dienstprogramme, auf die verwiesen wird, finden Sie unter [Allgemeine Hilfsprogramme für die Virtualisierungsbeispiele (v2)](common-utilities-for-the-virtualization-samples-v2.md).

> [!IMPORTANT]
> Der folgende Code muss auf dem Host Server des virtuellen Computers ausgeführt werden, und er muss mit Administrator Rechten ausgeführt werden, um ordnungsgemäß zu funktionieren.

 


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



Im folgenden Visual Basic Scripting Edition Beispiel (VBScript) werden einem virtuellen Computer Schlüssel-Wert-Paare hinzugefügt.

> [!IMPORTANT]
> Der folgende Code muss auf dem Host Server des virtuellen Computers ausgeführt werden, und er muss mit Administrator Rechten ausgeführt werden, um ordnungsgemäß zu funktionieren.

 


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

[**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

