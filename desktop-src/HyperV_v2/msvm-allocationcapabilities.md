---
description: Definiert die Mittel, mit denen ein Client den gültigen Bereich von Standardeinstellungen für eine virtuelle Ressource ermitteln kann.
ms.assetid: AC516723-7CD2-4F10-B8BF-EF9D458D3E5B
title: Msvm_AllocationCapabilities-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AllocationCapabilities
- Msvm_AllocationCapabilities.InstanceID
- Msvm_AllocationCapabilities.Caption
- Msvm_AllocationCapabilities.Description
- Msvm_AllocationCapabilities.ElementName
- Msvm_AllocationCapabilities.ResourceType
- Msvm_AllocationCapabilities.OtherResourceType
- Msvm_AllocationCapabilities.ResourceSubType
- Msvm_AllocationCapabilities.RequestTypesSupported
- Msvm_AllocationCapabilities.SharingMode
- Msvm_AllocationCapabilities.SupportedAddStates
- Msvm_AllocationCapabilities.SupportedRemoveStates
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dfdbb9dc884bd84e15e02e004af3cef296ae7723733f572a4525542747449e37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118149320"
---
# <a name="msvm_allocationcapabilities-class"></a>Msvm \_ AllocationCapabilities-Klasse

Definiert die Mittel, mit denen ein Client den gültigen Bereich von Standardeinstellungen für eine virtuelle Ressource ermitteln kann. Jedem Ressourcenpool ist ein **Msvm \_ AllocationCapabilities-Objekt** zugeordnet. Dem **Msvm \_ AllocationCapabilities-Objekt** sind vier [**Msvm \_ ResourceAllocationSettingData-Objekte**](msvm-resourceallocationsettingdata.md) zugeordnet, um die minimalen, maximalen, standardmäßigen und inkrementellen Werte für die Zuordnung der jeweiligen Ressource zu beschreiben. Zusammen beschreiben diese Klassen den gesamten Bereich der unterstützten Funktionen.

Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AllocationCapabilities : CIM_AllocationCapabilities
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  uint16 ResourceType;
  string OtherResourceType;
  string ResourceSubType;
  uint16 RequestTypesSupported;
  uint16 SharingMode;
  uint16 SupportedAddStates[];
  uint16 SupportedRemoveStates[];
};
```

## <a name="members"></a>Member

Die **Msvm \_ AllocationCapabilities-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ AllocationCapabilities-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

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

Ein Anzeigename für das Objekt. Mit dieser Eigenschaft kann jede Instanz zusätzlich zu den Schlüsseleigenschaften, Identitätsdaten und Beschreibungsinformationen einen Anzeigenamen definieren. Die [**Name-Eigenschaft**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement) der **CIM \_ ManagedSystemElement-Klasse** wird auch als Anzeigename definiert. Es wird jedoch häufig als Schlüssel unterklassigt. Es ist nicht sinnvoll, dass die gleiche Eigenschaft sowohl Identität als auch Anzeigename ohne Inkonsistenzen vermitteln kann. Wenn [**Name**](msvm-keyboard.md) vorhanden ist und kein Schlüssel ist (z. B. für Instanzen eines logischen Geräts), können die gleichen Informationen sowohl in den Eigenschaften **Name** als auch **ElementName** vorhanden sein. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein eindeutiger Bezeichner für diesen Ressourcenpool. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**OtherResourceType**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die den Ressourcentyp beschreibt, wenn kein klar definierter Wert verfügbar ist und **ResourceType** den Wert "Other" hat. Diese Eigenschaft wird von [**CIM \_ AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities)geerbt.

</dd> <dt>

**RequestTypesSupported**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob das Anfordern einer bestimmten Ressource unterstützt wird. Diese Eigenschaft wird von [**CIM \_ AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities)geerbt.



| Wert                                                                                                                                                                                                                           | Bedeutung                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Unbekannt**</dt> <dt>0</dt> </dl>     | Unbekannt<br/>                                                         |
| <span id="Specific"></span><span id="specific"></span><span id="SPECIFIC"></span><dl> <dt>**Spezifisch**</dt> <dt>2</dt> </dl> | Die Anforderung kann eine Anforderung für eine bestimmte Ressource enthalten.<br/>      |
| <span id="General"></span><span id="general"></span><span id="GENERAL"></span><dl> <dt>**Allgemein**</dt> <dt>3</dt> </dl>     | Die Anforderung enthält keine Anforderung für eine bestimmte Ressource.<br/> |
| <span id="Both"></span><span id="both"></span><span id="BOTH"></span><dl> <dt>**Beide**</dt> <dt>4</dt> </dl>                 | Sowohl spezifische als auch allgemeine Anforderungen werden unterstützt.<br/>               |



 

</dd> <dt>

**ResourceSubType**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die einen implementierungsspezifischen Untertyp für diese Ressource beschreibt. Dies kann beispielsweise verwendet werden, um verschiedene Modelle desselben Ressourcentyps zu unterscheiden. Diese Eigenschaft wird von [**CIM \_ AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities)geerbt.

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Typ der Ressource, die von dieser Zuordnungseinstellung dargestellt wird. Diese Eigenschaft wird von [**CIM \_ AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities)geerbt.

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

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Diskettenlaufwerk** (14)
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

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB-Controller** (23)
</dt> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Grafikcontroller** (24)
</dt> <dt>

<span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394 Controller** (25)
</dt> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionierbare Einheit** (26)
</dt> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Partitionierbare Basiseinheit** (27)
</dt> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>**Stromversorgung** (28)
</dt> <dt>

<span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>**Kühlkapazität** (29)
</dt> <dt>

<span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Ethernet-Switchport** (30)
</dt> <dt>

<span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Logischer Datenträger** (31)
</dt> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Storage Volume** (32)
</dt> <dt>

<span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernet-Verbindung** (33)
</dt> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Reservierter Anbieter** (0x8000. 0xFFFF )
</dt> </dl>

</dd> <dt>

**SharingMode**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, wie Zugriff auf eine zugrunde liegende Ressource gewährt wird. Diese Eigenschaft wird von [**CIM \_ AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities)geerbt.



| Wert                                                                                                                                                                                                                               | Bedeutung                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Unbekannt**</dt> <dt>0</dt> </dl>         | Unbekannt<br/>                                     |
| <span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span><dl> <dt>**Dedicated**</dt> <dt>2</dt> </dl> | Exklusiver Zugriff auf eine zugrunde liegende Ressource.<br/> |
| <span id="Shared"></span><span id="shared"></span><span id="SHARED"></span><dl> <dt>**Freigegeben**</dt> <dt>3</dt> </dl>             | Freigegebene Verwendung einer zugrunde liegenden Ressource.<br/>       |



 

</dd> <dt>

**SupportedAddStates**
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Zustände an, in denen sich das System, dem die Ressource zugeordnet wird, beim Erstellen einer neuen Ressource befindet. Diese Eigenschaft wird von [**CIM \_ AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities)geerbt.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)
</dt> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (2)
</dt> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (3)
</dt> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunterfahren** (4)
</dt> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (5)
</dt> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Aktiviert, aber offline** (6)
</dt> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (7)
</dt> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Verzögert** (8)
</dt> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Stille** (9)
</dt> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Ab** (10)
</dt> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angehalten** (11)
</dt> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Angehalten** (12)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Reservierter Anbieter** (0x8000. 0xFFFF )
</dt> </dl>

</dd> <dt>

**SupportedRemoveStates**
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Zustände an, in denen sich das System, dem die Ressource zugeordnet ist, beim Entfernen der Ressource befindet. Diese Eigenschaft wird von [**CIM \_ AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities)geerbt.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)
</dt> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Aktiviert** (2)
</dt> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deaktiviert** (3)
</dt> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Herunterfahren** (4)
</dt> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Nicht zutreffend** (5)
</dt> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Aktiviert, aber offline** (6)
</dt> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (7)
</dt> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Verzögert** (8)
</dt> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Stille** (9)
</dt> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Ab** (10)
</dt> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Angehalten** (11)
</dt> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Angehalten** (12)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Reservierter Anbieter** (0x8000. 0xFFFF )
</dt> </dl>

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Zugriff auf die **Msvm \_ AllocationCapabilities-Klasse** kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ AllocationCapabilities**](cim-allocationcapabilities.md)
</dt> <dt>

[**CIM \_ AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities)
</dt> <dt>

[**Msvm \_ AllocationCapabilities (V1)**](/previous-versions/windows/desktop/virtual/msvm-allocationcapabilities)
</dt> <dt>

[Ressourcenverwaltungsklassen](resource-management-classes.md)
</dt> </dl>

 

