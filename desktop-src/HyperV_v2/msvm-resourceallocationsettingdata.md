---
description: Stellt den aktuellen und aufgezeichneten Zuordnungszustände einer virtuellen Ressource dar.
ms.assetid: 5C180933-2013-4E16-A9BD-653D5426F468
title: Msvm_ResourceAllocationSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourceAllocationSettingData
- Msvm_ResourceAllocationSettingData.InstanceID
- Msvm_ResourceAllocationSettingData.Caption
- Msvm_ResourceAllocationSettingData.Description
- Msvm_ResourceAllocationSettingData.ElementName
- Msvm_ResourceAllocationSettingData.ResourceType
- Msvm_ResourceAllocationSettingData.OtherResourceType
- Msvm_ResourceAllocationSettingData.ResourceSubType
- Msvm_ResourceAllocationSettingData.PoolID
- Msvm_ResourceAllocationSettingData.ConsumerVisibility
- Msvm_ResourceAllocationSettingData.HostResource
- Msvm_ResourceAllocationSettingData.AllocationUnits
- Msvm_ResourceAllocationSettingData.VirtualQuantity
- Msvm_ResourceAllocationSettingData.Reservation
- Msvm_ResourceAllocationSettingData.Limit
- Msvm_ResourceAllocationSettingData.Weight
- Msvm_ResourceAllocationSettingData.AutomaticAllocation
- Msvm_ResourceAllocationSettingData.AutomaticDeallocation
- Msvm_ResourceAllocationSettingData.Parent
- Msvm_ResourceAllocationSettingData.Connection
- Msvm_ResourceAllocationSettingData.Address
- Msvm_ResourceAllocationSettingData.MappingBehavior
- Msvm_ResourceAllocationSettingData.AddressOnParent
- Msvm_ResourceAllocationSettingData.VirtualQuantityUnits
- Msvm_ResourceAllocationSettingData.VirtualSystemIdentifiers
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d79da0eabb193c7f71e1c327263831e62edf13c44b9bed33af02a1f46be34934
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068470"
---
# <a name="msvm_resourceallocationsettingdata-class"></a>Msvm \_ ResourceAllocationSettingData-Klasse

Stellt den aktuellen und aufgezeichneten Zuordnungszustände einer virtuellen Ressource dar.

Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourceAllocationSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string  Caption;
  string  Description;
  string  ElementName;
  uint16  ResourceType;
  string  OtherResourceType;
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility;
  string  HostResource[];
  string  AllocationUnits;
  uint64  VirtualQuantity;
  uint64  Reservation;
  uint64  Limit;
  uint32  Weight;
  boolean AutomaticAllocation;
  boolean AutomaticDeallocation;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
  string  VirtualSystemIdentifiers[] = { "GUID" };
};
```

## <a name="members"></a>Member

Die **Msvm \_ ResourceAllocationSettingData-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ ResourceAllocationSettingData-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Adresse**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Adresse der Ressource. Diese Eigenschaft wird von [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

Dies ist eine schreibgeschützte Eigenschaft, aber wenn die **ResourceType-Eigenschaft** 20 (Grafikcontroller) ist, kann sie mit der [**ModifyResourceSettings-Methode**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) der [**Msvm \_ VirtualSystemManagementService-Klasse**](msvm-virtualsystemmanagementservice.md) geändert werden.

</dd> <dt>

**AddressOnParent**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Beschreibt die Adresse dieser Ressource im Kontext des übergeordneten Elements. Die Eigenschaften **Parent** und **AddressOnParent** werden verwendet, um die Controllerbeziehung sowie die Reihenfolge der Geräte auf einem Controller zu beschreiben. Diese Eigenschaft wird von [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

</dd> <dt>

**AllocationUnits**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Zuordnungseinheit, die von den Eigenschaften **Reservierung** und **Limit** verwendet wird. Diese Eigenschaft wird von [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

</dd> <dt>

**AutomaticAllocation**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Ressource automatisch zugeordnet wird. Diese Eigenschaft wird von [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

</dd> <dt>

**AutomaticDeallocation**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Zuordnung der Ressource automatisch freigegeben wird. Diese Eigenschaft wird von [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **MaxLen** (64)
</dt> </dl>

Eine kurze Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Connection**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Gerät, mit dem diese Ressource verbunden ist. Diese Eigenschaft wird von [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

Dies ist eine schreibgeschützte Eigenschaft. Wenn die **ResourceType-Eigenschaft** jedoch 21 (serieller Port) und die **ResourceSubType-Eigenschaft** "Microsoft:Hyper-V:Serial Port" lautet, kann die **Connection-Eigenschaft** mithilfe der [**ModifyResourceSettings-Methode**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) der [**Msvm \_ VirtualSystemManagementService-Klasse**](msvm-virtualsystemmanagementservice.md) geändert werden.

</dd> <dt>

**ConsumerVisibility**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Sichtbarkeit des Consumers für die zugeordnete Ressource. Diese Eigenschaft wird von [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeigename für das Objekt. Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt. Wenn Sie diese Eigenschaft ändern, ändert sich der Elementname der zugeordneten logischen Geräteableitung.

Dies ist eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**ModifyResourceSettings-Methode**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) der [**Msvm \_ VirtualSystemManagementService-Klasse**](msvm-virtualsystemmanagementservice.md) geändert werden kann.

</dd> <dt>

**HostResource**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Jedem Gerät auf dem virtuellen Computer kann nur eine Hostressource zugewiesen werden, sodass nur das erste Element dieses Arrays festgelegt werden kann. Legen Sie für Geräte, die dieses Feature unterstützen, das erste Element des **HostResource-Arrays** so fest, dass es einen Verweis auf die zugrunde liegende Hostressource enthält, die zugewiesen werden soll. Diese Eigenschaft wird von [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

Dies ist eine schreibgeschützte Eigenschaft. Wenn die **ResourceType-Eigenschaft** jedoch 17 (Datenträger) ist und die **ResourceSubType-Eigenschaft** "Microsoft:Hyper-V:Physical Disk Drive" lautet, kann die **HostResource-Eigenschaft** mithilfe der [**ModifyResourceSettings-Methode**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) der [**Msvm \_ VirtualSystemManagementService-Klasse**](msvm-virtualsystemmanagementservice.md) geändert werden.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Identifiziert eine Instanz dieser Klasse eindeutig. Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt und immer auf "Microsoft:*GUID* \\ *DeviceSpecificData"* festgelegt.

</dd> <dt>

**Begrenzung**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die maximale Menge an Ressourcen, die für diese Zuordnung gewährt wird. Die Maßeinheit für diese Eigenschaft wird von der **VirtualQuantityUnits-Eigenschaft** angegeben. Diese Eigenschaft wird von [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

</dd> <dt>

**MappingBehavior**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, wie diese Ressource zugrunde liegenden Ressourcen zugeordnet wird. Diese Eigenschaft wird von [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

</dd> <dt>

**OtherResourceType**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die den Ressourcentyp beschreibt, wenn kein klar definierter Wert verfügbar ist und [**ResourceType**](msvm-processorsettingdata.md) den Wert 1(Other) hat. Diese Eigenschaft wird von [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

</dd> <dt>

**Parent**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das übergeordnete Element der Ressource. Diese Eigenschaft wird von [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

</dd> <dt>

**PoolID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Bezeichner des Ressourcenpools, aus dem diese Ressource zugeordnet wurde. Bei Instanzen, die einem virtuellen Computer zugeordnet sind, ist dies "Microsoft:*GUID-gerätespezifische* \\ *Daten".* Für Instanzen, die potenzielle Einstellungen für einen virtuellen Computer definieren, ist dies "Microsoft:Definition \\ *GUID* \\ *Type",* wobei *Type* eine von "Maximum", "Minimum", "Default" oder "Increment" sein kann. Diese Eigenschaft wird von [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

</dd> <dt>

**Reservierung**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Menge der Ressource, die für diese Zuordnung garantiert verfügbar ist. Die Maßeinheit für diese Eigenschaft wird von der **VirtualQuantityUnits-Eigenschaft** angegeben. Diese Ressourcen sind garantiert für die Nutzung durch den virtuellen Computer verfügbar. Diese Eigenschaft wird von [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

</dd> <dt>

**ResourceSubType**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die einen implementierungsspezifischen Untertyp für diese Ressource beschreibt. Dies kann beispielsweise verwendet werden, um verschiedene Modelle desselben Ressourcentyps zu unterscheiden. Diese Eigenschaft wird von [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Typ der Ressource, die von dieser Zuordnungseinstellung dargestellt wird. Diese Eigenschaft wird von [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

<dl> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Andere** (1)
</dt> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computersystem** (2)
</dt> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Prozessor** (3)
</dt> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Arbeitsspeicher** (4)
</dt> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE-Controller** (5)
</dt> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Paralleler SCSI-HBA** (6)
</dt> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)
</dt> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI-HBA** (8)
</dt> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)
</dt> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet-Adapter** (10)
</dt> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Anderer Netzwerkadapter** (11)
</dt> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**E/A-Slot** (12)
</dt> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**E/A-Gerät** (13)
</dt> <dt>

<span id="Diskette_Drive"></span><span id="diskette_drive"></span><span id="DISKETTE_DRIVE"></span>**Diskettenlaufwerk** (14)
</dt> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD-Laufwerk** (15)
</dt> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD-Laufwerk** (16)
</dt> <dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Laufwerk** (17)
</dt> <dt>

<span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Bandlaufwerk** (18)
</dt> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (19)
</dt> <dt>

<span id="Other_Storage_Device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other Storage Device** (20)
</dt> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serieller Anschluss** (21)
</dt> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Paralleler Port** (22)
</dt> <dt>

<span id="USB_controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB-Controller** (23)
</dt> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Grafikcontroller** (24)
</dt> <dt>

<span id="IEEE_1394_controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394 Controller** (25)
</dt> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionierbare Einheit** (26)
</dt> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Partitionierbare Basiseinheit** (27)
</dt> <dt>

<span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Stromversorgung** (28)
</dt> <dt>

<span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Kühlgerät** (29)
</dt> <dt>

<span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Ethernet-Switchport** (30)
</dt> <dt>

<span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Logischer Datenträger** (31)
</dt> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Storage Volume** (32)
</dt> <dt>

<span id="Ethernet_connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernetverbindung** (33)
</dt> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (30 32767)
</dt> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Reservierter Anbieter** (32768 65535)
</dt> </dl>

</dd> <dt>

**VirtualQuantity**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Menge der Ressourcen an, die dem Consumer angezeigt werden. Die Maßeinheit für diese Eigenschaft wird von der **VirtualQuantityUnits-Eigenschaft** angegeben. Diese Eigenschaft wird von [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

</dd> <dt>

**VirtualQuantityUnits**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Maßeinheit für diese Ressourcenzuordnung an. Der Wert dieser Eigenschaft muss ein rechtlicher Wert des Qualifizierers "Programmgesteuerte Einheiten" sein, wie in Anhang C.1 von DSP0004 V2.5 oder höher definiert. Diese Eigenschaft wird von [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

</dd> <dt>

**VirtualSystemIdentifiers**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indiziert")
</dt> </dl>

Ein Zeichenfolgenarray mit Bezeichnern dieser Ressource, das dem Betriebssystem des virtuellen Computers angezeigt wird. Diese Werte werden nur verwendet, wenn die **ResourceType-Eigenschaft** auf 6 (Parallel SCSI HBA) und die **ResourceSubType-Eigenschaft** auf "Microsoft Synthetic SCSI Controller" festgelegt ist. Diese Eigenschaft ist auf *"GUID"* festgelegt.

Dies ist eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**ModifyResourceSettings-Methode**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) der [**Msvm \_ VirtualSystemManagementService-Klasse**](msvm-virtualsystemmanagementservice.md) geändert werden kann.

</dd> <dt>

**Weight**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine ganze Zahl, die die relative Gewichtung für jeden VM-Prozessor definiert. Nachdem alle Reserven erreicht wurden, wird die verbleibende physische Prozessorkapazität der Hostingplattform virtuellen Computern basierend auf deren relativen Gewichtungen zugeordnet. Diese Eigenschaft wird von [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

Bereich: 0 1000

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Zugriff auf die **Msvm \_ ResourceAllocationSettingData-Klasse** kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md)
</dt> <dt>

[**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> <dt>

[**Msvm \_ ResourceAllocationSettingData (V1)**](/previous-versions/windows/desktop/virtual/msvm-resourceallocationsettingdata)
</dt> <dt>

[Ressourcenverwaltungsklassen](resource-management-classes.md)
</dt> </dl>

 

