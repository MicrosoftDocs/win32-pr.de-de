---
description: Stellt einen Ressourcenpool dar, bei dem es sich um eine logische Entität handelt, die vom Hostsystem zum Zuordnen und Zuweisen von Ressourcen bereitgestellt wird.
ms.assetid: c8e0b701-1814-4409-a073-017f8fea841a
title: CIM_ResourcePool-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePool
- CIM_ResourcePool.InstanceID
- CIM_ResourcePool.PoolID
- CIM_ResourcePool.Primordial
- CIM_ResourcePool.Capacity
- CIM_ResourcePool.Reserved
- CIM_ResourcePool.ResourceType
- CIM_ResourcePool.OtherResourceType
- CIM_ResourcePool.ResourceSubType
- CIM_ResourcePool.AllocationUnits
- CIM_ResourcePool.ConsumedResourceUnits
- CIM_ResourcePool.CurrentlyConsumedResource
- CIM_ResourcePool.MaxConsumableResource
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d87a78d5a8ea43cc8a1a59bbabf5b8091948d153420dbdf91ba7e14fc1616b7e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980960"
---
# <a name="cim_resourcepool-class"></a>CIM \_ ResourcePool-Klasse

Stellt einen Ressourcenpool dar, bei dem es sich um eine logische Entität handelt, die vom Hostsystem zum Zuordnen und Zuweisen von Ressourcen bereitgestellt wird.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_ResourcePool : CIM_LogicalElement
{
  string  InstanceID;
  string  PoolID;
  boolean Primordial = FALSE;
  uint64  Capacity;
  uint64  Reserved;
  uint16  ResourceType;
  string  OtherResourceType;
  string  ResourceSubType;
  string  AllocationUnits;
  string  ConsumedResourceUnits = "count";
  uint64  CurrentlyConsumedResource;
  uint64  MaxConsumableResource;
};
```

## <a name="members"></a>Member

Die **CIM \_ ResourcePool-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ ResourcePool-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AllocationUnits**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **IsPUnit**
</dt> </dl>

Die Zuordnungseinheiten, die von den **Eigenschaften Reservierung** und **Limit verwendet** werden. Wenn **ResourceType** beispielsweise auf "Processor" festgelegt ist, kann **AllocationUnits** auf "hertz \* 10^6" oder "percent" festgelegt werden. Der Wert dieser Eigenschaft sollte ein rechtlicher Wert des Qualifizierers Programmatic Units aus Anhang C.1 von *DSP0004 V2.4* oder höher sein.

</dd> <dt>

**Capacity**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die maximale Anzahl von Reservierungen, die der Ressourcenpool unterstützen kann. Die **AllocationUnits-Eigenschaft** gibt den Einheitentyp an.

</dd> <dt>

**ConsumedResourceUnits**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourcePool**.**MaxConsumableResource**", "**CIM \_ ResourcePool**.**CurrentlyConsumedResource**"), **IsPUnit**
</dt> </dl>

Die Einheiten für die **Eigenschaften MaxConsumable** und **Consumed.**

</dd> <dt>

**CurrentlyConsumedResource**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourcePool**.**ConsumedResourceUnits**")
</dt> </dl>

Die Menge der Ressource, die der Ressourcenpool derzeit ressourcenverbrauchern präsentiert. Diese Eigenschaft ist  anders als die Reserved-Eigenschaft, da sie die Ansicht consumers der Ressource beschreibt, während die **Reserved-Eigenschaft** die Producers-Ansicht der Ressource beschreibt.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**Überschreibung**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")
</dt> </dl>

Identifiziert eine Instanz dieser Klasse eindeutig innerhalb des Bereichs des enthaltenden Namespace.

> [!IMPORTANT]
>
> Um die Eindeutigkeit innerhalb des Namespace sicherzustellen, sollte der Wert der **InstanceID-Eigenschaft** im folgenden Muster erstellt werden: *OrgID*:*LocalID*
>
> -   *OrgID* muss einen urheberrechtlich geschützten, markengebundenen oder anderweitig eindeutigen Namen enthalten, der im Besitz der Geschäftsentität ist, die die **InstanceID-Eigenschaft** definiert, oder eine registrierte ID sein, die von einer erkannten globalen Autorität zugewiesen wird.
> -   *OrgID* darf keinen Doppelpunkt enthalten. Der erste Doppelpunkt in **InstanceID** muss zwischen *OrgID* und *LocalID liegen.*
> -   *LocalID* wird von der Geschäftsentität ausgewählt und sollte nicht erneut verwendet werden, um verschiedene zugrunde liegende reale Elemente zu identifizieren.
> -   Wenn das oben genannte Muster nicht verwendet wird, muss die definierende Entität sicherstellen, dass der resultierende **InstanceID-Wert** nicht für **InstanceID-Eigenschaften** erneut verwendet wird, die von diesem Anbieter oder anderen Anbietern für diesen Namespace erstellt werden.
> -   Für DMTF-definierte Instanzen muss das Muster verwendet werden, und die *OrgID* muss auf "CIM" festgelegt sein.

 

</dd> <dt>

**MaxConsumableResource**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourcePool**.**ConsumedResourceUnits**")
</dt> </dl>

Die maximale Menge an verfügbaren Ressourcen, die der Ressourcenpool Ressourcenverbrauchern zur Verfügung stellen kann. Diese Eigenschaft ist  anders als die Capacity-Eigenschaft, da sie die Ansicht consumers der Ressource beschreibt, während die **Capacity-Eigenschaft** die Ansicht "Producers" der Ressource beschreibt.

</dd> <dt>

**OtherResourceType**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourcePool**.**ResourceType**")
</dt> </dl>

Der Ressourcentyp, wenn die **ResourceType-Eigenschaft** auf "0" (andere) festgelegt ist.

</dd> <dt>

**PoolID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**PoolId**")
</dt> </dl>

Ein nicht transparenter Bezeichner für den Pool. Diese Eigenschaft wird verwendet, um Korrelation beim Speichern und Wiederherstellen von Konfigurationsdaten im zugrunde liegenden persistenten Speicher zu ermöglichen.

</dd> <dt>

**Ursprünglich**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**TRUE,** wenn der Ressourcenpool vom Ursprünglichen ist. **FALSE,** wenn der Ressourcenpool ein konkretes Ressourcenpool ist. Ein unerreichter Ressourcenpool ist ein Ressourcenpool, der nicht von den Ressourcenverbrauchern erstellt oder gelöscht wird. Ein konkretes Ressourcenpool kann von Ressourcenzuordnungsdiensten aktualisiert werden.

</dd> <dt>

**Reserved**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die aktuelle Anzahl von Reservierungen, die auf alle aktiven Zuordnungen aus diesem Pool verteilt sind. In einer hierarchischen Konfiguration stellt dies die Summe aller aktuellen Nachfolgerreservierungen dar. Die **AllocationUnits-Eigenschaft** gibt den Einheitentyp an.

</dd> <dt>

**ResourceSubType**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourcePool**.**ResourceType**")
</dt> </dl>

Der implementierungsspezifische Untertyp für den Ressourcenpool. Dies kann beispielsweise verwendet werden, um verschiedene Modelle desselben Ressourcentyps zu unterscheiden.

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ResourcePool**.**OtherResourceType**", "**CIM \_ ResourcePool**.**ResourceSubType**")
</dt> </dl>

Der Vom Ressourcenpool zugeordnete Ressourcentyp.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>

**Computersystem** (2)


</dt> <dd></dd> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>

**Prozessor** (3)


</dt> <dd></dd> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>

**Arbeitsspeicher** (4)


</dt> <dd></dd> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>

**IDE-Controller** (5)


</dt> <dd></dd> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>

**Paralleler SCSI-HBA** (6)


</dt> <dd></dd> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>

**FC HBA** (7)


</dt> <dd></dd> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>

**iSCSI HBA** (8)


</dt> <dd></dd> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>

**IB HCA** (9)


</dt> <dd></dd> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>

**Ethernet-Adapter** (10)


</dt> <dd></dd> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>

**Anderer Netzwerkadapter** (11)


</dt> <dd></dd> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>

**E/A-Slot** (12)


</dt> <dd></dd> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>

**E/A-Gerät** (13)


</dt> <dd></dd> <dt>

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>

**Diskettenlaufwerk** (14)


</dt> <dd></dd> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>

**CD-Laufwerk** (15)


</dt> <dd></dd> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>

**DVD-Laufwerk** (16)


</dt> <dd></dd> <dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

**Laufwerk** (17)


</dt> <dd></dd> <dt>

<span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>

**Bandlaufwerk** (18)


</dt> <dd></dd> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>

**Storage Extent** (19)


</dt> <dd></dd> <dt>

<span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>

**Anderes Speichergerät** (20)


</dt> <dd></dd> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>

**Serieller** Port (21)


</dt> <dd></dd> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

**Paralleler** Port (22)


</dt> <dd></dd> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>

**USB-Controller** (23)


</dt> <dd></dd> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>

**Grafikcontroller** (24)


</dt> <dd></dd> <dt>

<span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>

**IEEE 1394 Controller** (25)


</dt> <dd></dd> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>

**Partitionierbare Einheit** (26)


</dt> <dd></dd> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>

**Partitionierbare Basiseinheit** (27)


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

**Power** (28)


</dt> <dd></dd> <dt>

<span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>

**Kühlkapazität** (29)


</dt> <dd></dd> <dt>

<span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>

**Ethernet-Switchport** (30)


</dt> <dd></dd> <dt>

<span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>

**Logischer** Datenträger (31)


</dt> <dd></dd> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>

**Storage Volume** (32)


</dt> <dd></dd> <dt>

<span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>

**Ethernetverbindung** (33)


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reserved** (.)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Reservierter Anbieter** (0x8000. 0xFFFF)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ LogicalElement**](cim-logicalelement.md)
</dt> </dl>

 

