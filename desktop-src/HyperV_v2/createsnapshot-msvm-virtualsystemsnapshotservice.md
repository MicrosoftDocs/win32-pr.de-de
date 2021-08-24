---
description: Erstellt eine Momentaufnahme eines virtuellen Computers.
ms.assetid: 2de12fe7-5ec2-49d0-87ff-cd48c34fec46
title: CreateSnapshot-Methode der Msvm_VirtualSystemSnapshotService -Klasse (Dbdaoint.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.CreateSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c6b86f8b6d0b2fc5ff9ed8c968c9c3a321623c81e1613ce82aca18944e9ac6c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682600"
---
# <a name="createsnapshot-method-of-the-msvm_virtualsystemsnapshotservice-class"></a>CreateSnapshot-Methode der Msvm \_ VirtualSystemSnapshotService-Klasse

Erstellt eine Momentaufnahme eines virtuellen Computers.

## <a name="syntax"></a>Syntax


```mof
uint32 CreateSnapshot(
  [in]      CIM_ComputerSystem           REF AffectedSystem,
  [in]      string                           SnapshotSettings,
  [in]      uint16                           SnapshotType,
  [in, out] CIM_VirtualSystemSettingData REF ResultingSnapshot,
  [out]     CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*AffectedSystem* \[ In\]
</dt> <dd>

Ein Verweis auf eine [**\_ CIM-ComputerSystem-Klasse,**](/windows/desktop/CIMWin32Prov/cim-computersystem) die den virtuellen Computer darstellt, von dem eine Momentaufnahme erstellt werden soll.

</dd> <dt>

*SnapshotSettings* \[ In\]
</dt> <dd>

Eine Zeichenfolge, die eine eingebettete Instanz einer [**CIM \_ SettingData-Klasse**](/previous-versions//cc136911(v=vs.85)) enthält, die die Parametereinstellungen für die Momentaufnahme enthält. Dieser Parameter ist optional und kann eine leere Zeichenfolge sein.

</dd> <dt>

*SnapshotType* \[ In\]
</dt> <dd>

Gibt den Typ der angeforderten Momentaufnahme an. Dies muss einer der folgenden Werte sein.

<dt>

<span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>

<span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>**Vollständige Momentaufnahme** (2)


</dt> <dd>

Vollständige Momentaufnahme des virtuellen Computers.

</dd> <dt>

<span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>

<span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>**Datenträgermomentaufnahme** (3)


</dt> <dd>

Momentaufnahme der Datenträger virtueller Computer.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Herstellerspezifisch** (32768..65535)


</dt> <dd></dd> </dl> </dd> <dt>

*ResultingSnapshot* \[ in, out\]
</dt> <dd>

Ein Verweis auf ein [**CIM \_ VirtualSystemSettingData-Objekt,**](/previous-versions//cc136954(v=vs.85)) das die resultierende Momentaufnahme des virtuellen Computers darstellt.

</dd> <dt>

*Auftrag* \[ out\]
</dt> <dd>

Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ ConcreteJob abgeleitet wurde.**](/previous-versions//cc136808(v=vs.85))

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen der folgenden Werte zurück.

<dl> <dt>

**Abgeschlossen ohne Fehler** (0)
</dt> <dt>

**Nicht unterstützt** (1)
</dt> <dt>

**Fehler** (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Ungültiger Parameter** (4)
</dt> <dt>

**Ungültiger Zustand** (5)
</dt> <dt>

**Ungültiger Typ** (6)
</dt> <dt>

**DMTF Reserved** (..)
</dt> <dt>

**Überprüfte Methodenparameter – Auftrag gestartet** (4096)
</dt> <dt>

**Reservierte Methode** (4097..32767)
</dt> <dt>

**Herstellerspezifisch** (32768..65535)
</dt> </dl>

## <a name="examples"></a>Beispiele

Der folgende C#-Beispielcode erstellt einen virtuellen Computer. Die referenzierten Hilfsprogramme finden Sie unter [Allgemeine Hilfsprogramme für die Virtualisierungsbeispiele (V2).](common-utilities-for-the-virtualization-samples-v2.md)

> [!IMPORTANT]
> Damit der folgende Code ordnungsgemäß funktioniert, muss er auf dem Hostserver des virtuellen Computers und mit Administratorrechten ausgeführt werden.

 


```CSharp
public static void CreateSnapshot(string vmName)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject virtualSystemService = Utility.GetServiceObject(scope, "Msvm_VirtualSystemSnapshotService");

    ManagementBaseObject inParams = virtualSystemService.GetMethodParameters("CreateSnapshot");

    // Set the AffectedSystem property.
    ManagementObject vm = Utility.GetTargetComputer(vmName, scope);
    if (null == vm)
    {
        throw new ArgumentException(string.Format("The virtual machine \"{0}\" could not be found.", vmName));
    }

    inParams["AffectedSystem"] = vm.Path.Path;

    // Set the SnapshotSettings property.
#if(true)
    inParams["SnapshotSettings"] = "";
#else
    ManagementObject snapshotSettings = Utility.GetServiceObject(scope, "CIM_SettingData"); 
    inParams["SnapshotSettings"] = snapshotSettings.ToString();
#endif       
    // Set the SnapshotType property.
    inParams["SnapshotType"] = 2; // Full snapshot.

    ManagementBaseObject outParams = virtualSystemService.InvokeMethod("CreateSnapshot", inParams, null);

    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("Snapshot was created successfully.");

            MiscClass.GetAffectedElement(outParams, scope);
        }
        else
        {
            Console.WriteLine("Failed to create snapshot VM");
        }
    }
    else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
    {
        Console.WriteLine("Snapshot was created successfully.");
    }
    else
    {
        Console.WriteLine("Create virtual system snapshot failed with error {0}", outParams["ReturnValue"]);
    }

    inParams.Dispose();
    outParams.Dispose();
    vm.Dispose();
    virtualSystemService.Dispose();
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| Header<br/>                   | <dl> <dt>Dbdaoint.h</dt> </dl>                   |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msvm \_ VirtualSystemSnapshotService**](msvm-virtualsystemsnapshotservice.md)
</dt> <dt>

[**CreateVirtualSystemSnapshot (V1)**](/previous-versions/windows/desktop/virtual/createvirtualsystemsnapshot-msvm-virtualsystemmanagementservice)
</dt> </dl>

 

