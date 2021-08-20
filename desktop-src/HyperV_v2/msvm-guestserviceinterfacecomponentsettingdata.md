---
description: Stellt den konfigurierten Zustand der Gastdienstschnittstellenkomponente dar.
ms.assetid: 82B58459-9819-4F51-BEE5-AB57E444CF55
title: Msvm_GuestServiceInterfaceComponentSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceComponentSettingData
- Msvm_GuestServiceInterfaceComponentSettingData.ElementName
- Msvm_GuestServiceInterfaceComponentSettingData.InstanceID
- Msvm_GuestServiceInterfaceComponentSettingData.ResourceType
- Msvm_GuestServiceInterfaceComponentSettingData.OtherResourceType
- Msvm_GuestServiceInterfaceComponentSettingData.ResourceSubType
- Msvm_GuestServiceInterfaceComponentSettingData.PoolID
- Msvm_GuestServiceInterfaceComponentSettingData.ConsumerVisibility
- Msvm_GuestServiceInterfaceComponentSettingData.HostResource
- Msvm_GuestServiceInterfaceComponentSettingData.AllocationUnits
- Msvm_GuestServiceInterfaceComponentSettingData.VirtualQuantity
- Msvm_GuestServiceInterfaceComponentSettingData.Reservation
- Msvm_GuestServiceInterfaceComponentSettingData.Limit
- Msvm_GuestServiceInterfaceComponentSettingData.Weight
- Msvm_GuestServiceInterfaceComponentSettingData.AutomaticAllocation
- Msvm_GuestServiceInterfaceComponentSettingData.AutomaticDeallocation
- Msvm_GuestServiceInterfaceComponentSettingData.Parent
- Msvm_GuestServiceInterfaceComponentSettingData.Connection
- Msvm_GuestServiceInterfaceComponentSettingData.Address
- Msvm_GuestServiceInterfaceComponentSettingData.MappingBehavior
- Msvm_GuestServiceInterfaceComponentSettingData.EnabledState
- Msvm_GuestServiceInterfaceComponentSettingData.DefaultEnabledStatePolicy
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6e1171e5f303d5b122f0d2202978415206a26e94c15e69f09af73b811c33dcb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118147806"
---
# <a name="msvm_guestserviceinterfacecomponentsettingdata-class"></a>Msvm \_ GuestServiceInterfaceComponentSettingData-Klasse

Stellt den konfigurierten Zustand der Gastdienstschnittstellenkomponente dar. Diese Klasse wird von der [**\_ CIM-Klasse ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) ableiten.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestServiceInterfaceComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  ElementName;
  string  InstanceID;
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
  uint16  EnabledState = 3;
  uint16  DefaultEnabledStatePolicy = 2;
};
```

## <a name="members"></a>Member

Die **Msvm \_ GuestServiceInterfaceComponentSettingData-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ GuestServiceInterfaceComponentSettingData-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Adresse**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Adresse der Ressource. Beispiel: die MAC-Adresse eines Ethernet-Ports.

</dd> <dt>

**AllocationUnits**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft gibt die Zuordnungseinheiten an, die von den Eigenschaften Reservierung und Limit verwendet werden. Wenn beispielsweise ResourceType=Processor, kann AllocationUnits auf MHz festgelegt werden. Wenn ResourceType=Memory, kann AllocationUnits auf MB festgelegt werden.

</dd> <dt>

**AutomaticAllocation**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft gibt an, ob die Ressource automatisch zugeordnet wird. Wenn sie beispielsweise auf TRUE festgelegt ist, wird diese Ressource zugeordnet, wenn das systemaufwändige virtuelle Computer eingeschaltet ist. Der Wert false gibt an, dass die Ressource explizit zugeordnet werden muss. Die Einstellung kann z. B. Wechselmedien (d. h. Zung oder Diskette) darstellen, bei denen das Medium bei der Energieversorgung nicht vorhanden ist. Zum Zuordnen der Ressource ist ein expliziter Vorgang erforderlich.

</dd> <dt>

**AutomaticDeallocation**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft gibt an, ob die Ressourcenzuordnung automatisch entfernt wird. Wenn sie z. B. auf TRUE festgelegt ist, wird die Ressourcenzuordnung bei ausgeschalteten virtuellen Computersystemen wieder eingestellt. Wenn false festgelegt ist, bleibt die Ressource zugeordnet und muss explizit wieder zugeordnet werden.

</dd> <dt>

**Connection**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das, mit dem diese Ressource verbunden ist. Beispielsweise ein benanntes Netzwerk oder ein Switchport.

</dd> <dt>

**ConsumerVisibility**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Beschreibt die Sichtbarkeit des Consumers für die zugeordnete Ressource.



| Wert                                                                                                                                                                                                                                                                  | Bedeutung                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Unbekannt**</dt> <dt>0</dt> </dl>                                            | Unbekannt<br/>                                                                                                                                                                                                                                         |
| <span id="Passed-Through"></span><span id="passed-through"></span><span id="PASSED-THROUGH"></span><dl> <dt>**Übergebene Durch übergebene**</dt> <dt>2</dt> </dl>                | Die zugrunde liegende - oder -Hostressource wird verwendet und an den Consumer übergeben, möglicherweise mithilfe der Partitionierung. In der DeviceID-Eigenschaft muss mindestens ein Element vorhanden sein.<br/>                                                                        |
| <span id="Virtualized"></span><span id="virtualized"></span><span id="VIRTUALIZED"></span><dl> <dt>**Virtualisiert**</dt> <dt>3</dt> </dl>                            | Die Ressource wird virtualisiert und ist möglicherweise nicht direkt einer zugrunde liegenden/Hostressource zuordnen. Einige Implementierungen unterstützen möglicherweise eine bestimmte Zuweisung für virtualisierte Ressourcen. In diesem Fall werden die Hostressourcen mithilfe der DeviceID-Eigenschaft verfügbar gemacht.<br/> |
| <span id="Not_represented"></span><span id="not_represented"></span><span id="NOT_REPRESENTED"></span><dl> <dt>**Nicht dargestellt**</dt> <dt>4</dt> </dl>            | Eine Darstellung der Ressource ist im Kontext des Ressourcenverbraucher nicht vorhanden.<br/>                                                                                                                                                     |
| <span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**RESERVIERTE**</dt> <dt>DMTF-Datei.</dt> </dl>                   |                                                                                                                                                                                                                                                             |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <dt>**Anbieter reserviert**</dt> <dt>32767..65535</dt> </dl> |                                                                                                                                                                                                                                                             |



 

</dd> <dt>

**DefaultEnabledStatePolicy**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktivierte und deaktivierte Zustände von Gastkommunikationsdiensten standardmäßig.

Dies ist eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**ModifyResourceSettings-Methode**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) der [**Msvm \_ VirtualSystemManagementService-Klasse geändert werden**](msvm-virtualsystemmanagementservice.md) kann.

> [!Note]  
> Hinzugefügt in Windows 10.

 

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Aktiviert** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deaktiviert** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Anzeigename für diese Instanz von SettingData. Darüber hinaus kann der Anzeigename als Indexeigenschaft für eine Suche oder Abfrage verwendet werden. (Hinweis: Der Name muss innerhalb eines Namespaces nicht eindeutig sein.)

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktivierte und deaktivierte Zustände eines Elements.

Dies ist eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**ModifyVirtualSystemResources-Methode**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) (oder [**ModifyResourceSettings**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) in Windows 10 oder höher) der [**Msvm \_ VirtualSystemManagementService-Klasse**](msvm-virtualsystemmanagementservice.md) geändert werden kann.

Gültige Werte sind:

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Aktiviert** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deaktiviert** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**HostResource**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft macht eine bestimmte Zuweisung zum Hosten oder zu zugrunde liegenden Ressourcen verfügbar. Die eingebetteten Instanzen dürfen nur Schlüsseleigenschaften enthalten und als Objektpfade behandelt werden. Wenn die virtuelle Ressource für eine Reihe von zugrunde liegenden Ressourcen geplant werden kann, sollte diese Eigenschaft **NULL bleiben.** In diesem Fall können die Zuordnungen DeviceAllocatedFromPool oder ResourceAllocationFromPool verwendet werden, um den Pool von Hostressourcen zu bestimmen, für den diese virtuelle Ressource geplant werden kann. Wenn eine bestimmte Zuweisung verwendet wird, müssen alle zugrunde liegenden Ressourcen, die von dieser virtuellen Ressource verwendet werden, in diesem Array aufgeführt werden. In der Regel enthält das Array ein Element. Für Aggregatzuordnungen, z. B. mehrere Prozessoren, können jedoch mehrere Hostressourcen angegeben werden.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Im Gültigkeitsbereich des instanziierenden Namespace identifiziert InstanceID eine Instanz dieser Klasse undurchsichtig und eindeutig. Um die Eindeutigkeit innerhalb des NameSpace sicherzustellen, sollte der Wert von InstanceID mit dem folgenden "bevorzugten" Algorithmus erstellt *werden: OrgID*:*LocalID,* wobei *OrgID* und *LocalID* durch einen Doppelpunkt (:)) getrennt sind und *wobei OrgID* einen urheberrechtlich geschützten, markengebundenen oder anderweitig eindeutigen Namen enthalten muss, der im Besitz der Geschäftseinheit ist, die die InstanceID erstellt oder definiert oder eine registrierte ID ist, die der Geschäftseinheit von einer anerkannten globalen Autorität zugewiesen wurde. (Diese Anforderung ähnelt *schemaName.* \_ *ClassName-Struktur* von Schemaklassennamen.) Um die Eindeutigkeit sicherzustellen, darf *OrgID* außerdem keinen Doppelpunkt (:). Bei Verwendung dieses Algorithmus muss der erste Doppelpunkt, der in InstanceID angezeigt wird, zwischen *OrgID* und *LocalID angezeigt werden.* *LocalID* wird von der Geschäftsentität ausgewählt und sollte nicht wiederverwendet werden, um verschiedene zugrunde liegende (reale) Elemente zu identifizieren. Wenn der oben genannte "bevorzugte" Algorithmus nicht verwendet wird, muss die definierende Entität sicherstellen, dass die resultierende InstanceID nicht für InstanceIDs wiederverwendet wird, die von diesem oder anderen Anbietern für den NameSpace dieser Instanz erzeugt werden. Für DMTF-definierte Instanzen muss der "bevorzugte" Algorithmus verwendet werden, und die *OrgID muss* auf CIM festgelegt sein.

</dd> <dt>

**Begrenzung**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft gibt die Obergrenze oder die maximale Menge an Ressourcen an, die für diese Zuordnung gewährt werden. Beispielsweise kann ein System, das Speicher paging unterstützt, das Festlegen des Grenzwerts für eine Speicherzuweisung unterhalb des VirtualQuantity-Grenzwerts unterstützen, wodurch die Auslagerung für diese Zuordnung erzwungen wird.

</dd> <dt>

**MappingBehavior**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, wie diese Ressource zugrunde liegenden Ressourcen zu ordnet. Wenn das HostResource-Array Einträge enthält, spiegelt diese Eigenschaft wider, wie die Ressource diesen spezifischen Ressourcen entspricht.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)
</dt> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)
</dt> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (2)
</dt> <dt>

<span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>**Soft Affinity** (3)
</dt> <dt>

<span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>**Hard Affinity** (4)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)
</dt> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Reservierter Anbieter** (32767..65535)
</dt> </dl>

</dd> <dt>

**OtherResourceType**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die den Ressourcentyp beschreibt, wenn ein klar definierter Wert nicht verfügbar ist und ResourceType den Wert "Other" hat.

</dd> <dt>

**Parent**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das übergeordnete Element der Ressource. Beispiel: ein Controller für die aktuelle Zuordnung.

</dd> <dt>

**PoolID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft gibt an, aus welchem ResourcePool die Ressource derzeit zugeordnet ist oder von welchem ResourcePool die Ressource zugeordnet wird, wenn die Zuordnung erfolgt.

</dd> <dt>

**Reservierung**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft gibt die Menge der Ressource an, die für diese Zuordnung garantiert verfügbar ist. Auf einem System, das eine überzubelegung von Ressourcen unterstützt, wird dieser Wert in der Regel für die Zugangssteuerung verwendet, um zu verhindern, dass eine Zuordnung akzeptiert wird, wodurch eine Ressourcenaufbelegung verhindert wird.

</dd> <dt>

**ResourceSubType**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die einen implementierungsspezifischen Untertyp für diese Ressource beschreibt. Dies kann beispielsweise verwendet werden, um verschiedene Modelle desselben Ressourcentyps zu unterscheiden.

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Ressourcentyp, den diese Zuordnungseinstellung darstellt.

<dl> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)
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

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)
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

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serieller** Anschluss (17)
</dt> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Paralleler** Port (18)
</dt> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB-Controller** (19)
</dt> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Grafikcontroller** (20)
</dt> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (21)
</dt> <dt>

<span id="Disk"></span><span id="disk"></span><span id="DISK"></span>**Datenträger** (22)
</dt> <dt>

<span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Band** (23)
</dt> <dt>

<span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Anderes Speichergerät** (24)
</dt> <dt>

<span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Firewire Controller** (25)
</dt> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionierbare Einheit** (26)
</dt> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Partitionierbare Basiseinheit** (27)
</dt> <dt>

<span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Stromversorgung** (28)
</dt> <dt>

<span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Kühlgerät** (29)
</dt> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (.)
</dt> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Reservierter Anbieter** (32767..65535)
</dt> </dl>

</dd> <dt>

**VirtualQuantity**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft gibt die Menge der Ressourcen an, die dem Consumer präsentiert werden. Wenn beispielsweise ResourceType=Processor verwendet wird, spiegelt diese Eigenschaft die Anzahl der diskreten Prozessoren wider, die dem virtuellen Computersystem präsentiert werden. Wenn ResourceType=Memory, könnte diese Eigenschaft die Anzahl von MB widerspiegeln, die an das virtuelle Computersystem gemeldet werden.

</dd> <dt>

**Weight**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft gibt eine relative Priorität für diese Zuordnung in Bezug auf andere Zuordnungen aus demselben ResourcePool an. Diese Eigenschaft verfügt über keine Maßeinheit und ist nur relevant im Vergleich zu anderen Zuordnungen, die um die gleichen Hostressourcen konkurrieren.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Nur Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 Nur \[ R2-Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md)
</dt> <dt>

[**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

