---
description: Stellt den konfigurierten Status der Komponente der Gast Dienst Schnittstelle dar.
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
ms.openlocfilehash: 0ada39e4428040cf7e6732232ce789f7d837c9c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343649"
---
# <a name="msvm_guestserviceinterfacecomponentsettingdata-class"></a>MSVM- \_ guestserviceinterfacetten componentsettingdata-Klasse

Stellt den konfigurierten Status der Komponente der Gast Dienst Schnittstelle dar. Diese Klasse wird von der [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) -Klasse abgeleitet.

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

Die **MSVM \_ guestserviceinterfacecomponentsettingdata** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ guestserviceinterfacecomponentsettingdata** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Adresse**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Adresse der Ressource. Beispielsweise die Mac-Adresse eines Ethernet-Ports.

</dd> <dt>

**Zuordnung von Einheiten**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft gibt die Zuordnungs Einheiten an, die von den Reservierungs-und Limit-Eigenschaften verwendet werden. Wenn z. b. ResourceType = Processor ist, kann zugcationunits auf MHz festgelegt werden. Wenn ResourceType = Memory, kann ' zugcationunits ' auf ' MB ' festgelegt werden.

</dd> <dt>

**Automaticallocation**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft gibt an, ob die Ressource automatisch zugewiesen wird. Wenn z. b. auf true festgelegt ist, wird diese Ressource zugeordnet, wenn das verarbeitende virtuelle Computersystem eingeschaltet ist. Der Wert false gibt an, dass die Ressource explizit zugewiesen werden muss. Die Einstellung kann z. b. ein Wechselmedium (d. h. Rom oder Disketten) darstellen, bei dem die Medien bei der Stromversorgung nicht vorhanden sind. Ein expliziter Vorgang ist erforderlich, um die Ressource zuzuordnen.

</dd> <dt>

**Automaticdeallocation**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft gibt an, ob die Zuordnung der Ressource automatisch aufgehoben wird. Wenn z. b. auf true festgelegt ist, wird die Zuordnung dieser Ressource aufgehoben, wenn das verarbeitende virtuelle Computer ausgeschaltet ist. Wenn false festgelegt ist, bleibt die Ressource reserviert, und die Zuordnung muss explizit aufgehoben werden.

</dd> <dt>

**Connection**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das, mit dem diese Ressource verbunden ist. Beispielsweise ein benanntes Netzwerk oder ein Switchport.

</dd> <dt>

**Consumersichtbarkeit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Beschreibt die Benutzer Sichtbarkeit der zugeordneten Ressource.



| Wert                                                                                                                                                                                                                                                                  | Bedeutung                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Unbekannter**</dt> Wert <dt>0</dt> </dl>                                            | Unbekannt<br/>                                                                                                                                                                                                                                         |
| <span id="Passed-Through"></span><span id="passed-through"></span><span id="PASSED-THROUGH"></span><dl> <dt>**Durchlaufen**</dt> <dt>2</dt> </dl>                | Die zugrunde liegende-oder-Host Ressource wird verwendet und an den Consumer übermittelt, möglicherweise mithilfe der Partitionierung. In der Eigenschaft "Eigenschaft" muss mindestens ein Element vorhanden sein.<br/>                                                                        |
| <span id="Virtualized"></span><span id="virtualized"></span><span id="VIRTUALIZED"></span><dl> <dt>**Virtualisiert**</dt> <dt>3</dt> </dl>                            | Die Ressource ist virtualisiert und darf nicht direkt einer zugrunde liegenden/Host Ressource zugeordnet werden. Einige Implementierungen unterstützen möglicherweise eine bestimmte Zuweisung für virtualisierte Ressourcen. in diesem Fall werden die Host Ressourcen mithilfe der DeviceID-Eigenschaft verfügbar gemacht.<br/> |
| <span id="Not_represented"></span><span id="not_represented"></span><span id="NOT_REPRESENTED"></span><dl> <dt>**Nicht dargestellt**</dt> <dt>4</dt> </dl>            | Eine Darstellung der Ressource ist nicht im Kontext des ressourcenconsumers vorhanden.<br/>                                                                                                                                                     |
| <span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF reserviert**</dt> <dt>..</dt> </dl>                   |                                                                                                                                                                                                                                                             |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <dt>**Hersteller reserviert**</dt> <dt>32767.65535</dt> </dl> |                                                                                                                                                                                                                                                             |



 

</dd> <dt>

**Defaultenabledstatepolicy**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktivierte und deaktivierte Status der Gast Kommunikationsdienste standardmäßig.

Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifyresourcesettings**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.

> [!Note]  
> In Windows 10 hinzugefügt.

 

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

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Anzeige Name für diese Instanz von SettingData. Außerdem kann der Anzeige Name als Index Eigenschaft für eine Suche oder Abfrage verwendet werden. (Hinweis: der Name muss innerhalb eines Namespace nicht eindeutig sein.)

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktivierte und deaktivierte Status eines Elements.

Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mit der [**modifyvirtualsystemresources**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) -Methode (oder mit [**modifyresourcesettings**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) in Windows 10 oder höher) der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.

Gültige Werte sind:

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Aktiviert** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deaktiviert** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**"Hustresource"**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft macht eine bestimmte Zuweisung zu Host-oder zugrunde liegenden Ressourcen verfügbar. Die eingebetteten Instanzen dürfen nur Schlüsseleigenschaften enthalten und als Objekt Pfade behandelt werden. Wenn die virtuelle Ressource möglicherweise für eine Reihe von zugrunde liegenden Ressourcen geplant ist, sollte diese Eigenschaft **null** bleiben. In diesem Fall können die Zuordnungen devicezugedfrompool oder resourcezucationfrompool verwendet werden, um den Pool von Host Ressourcen zu ermitteln, auf dem diese virtuelle Ressource möglicherweise geplant ist. Wenn eine bestimmte Zuweisung verwendet wird, werden alle zugrunde liegenden Ressourcen, die von dieser virtuellen Ressource verwendet werden, in diesem Array aufgeführt. In der Regel enthält das Array ein Element. für Aggregat Zuordnungen, z. b. mehrere Prozessoren, können jedoch mehrere Host Ressourcen angegeben werden.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Im Gültigkeitsbereich des instanziierten Namespaces identifiziert InstanceId verdeckt und identifiziert eine Instanz dieser Klasse eindeutig. Um die Eindeutigkeit innerhalb des Namespaces sicherzustellen, sollte der Wert von InstanceId mit dem folgenden "bevorzugten" Algorithmus erstellt werden: *OrgId*:*localId* , bei der *OrgId* und *localId* durch einen Doppelpunkt (:)) getrennt sind und *OrgId* einen urheberrechtlich geschützten, mit einem Wert gekennzeichneten oder anderweitig eindeutigen Namen enthalten muss, der im Besitz der Geschäfts Entität ist, die die InstanceId erstellt oder definiert, oder bei der es sich um eine registrierte, von einer anerkannten globalen Autorität zugewiesene ID handelt. (Diese Anforderung ähnelt dem Schema *Name* \_ *ClassName* -Struktur von Schema Klassennamen.) Außerdem darf *OrgId* keinen Doppelpunkt (:) enthalten, um die Eindeutigkeit sicherzustellen. Wenn dieser Algorithmus verwendet wird, muss der erste Doppelpunkt, der in InstanceId angezeigt wird, zwischen *OrgId* und *localId* angezeigt werden. *LocalId* wird von der Geschäfts Entität ausgewählt und sollte nicht wieder verwendet werden, um verschiedene zugrunde liegende (reale) Elemente zu identifizieren. Wenn der oben genannte "bevorzugte" Algorithmus nicht verwendet wird, muss die definierende Entität sicherstellen, dass die resultierende InstanceId nicht in allen instanceids wieder verwendet wird, die von diesem oder anderen Anbietern für den Namespace dieser Instanz erstellt werden. Für von DMTF definierte Instanzen muss der "bevorzugte" Algorithmus verwendet werden, wenn die *OrgId* auf CIM festgelegt ist.

</dd> <dt>

**Begrenzung**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft gibt die obere Grenze oder die maximale Menge an Ressourcen an, die für diese Zuweisung gewährt wird. Beispielsweise kann ein System, das die Speicher Auslagerung unterstützt, das Festlegen des Limits einer Speicher Belegung unterhalb der virtualmenge unterstützen, wodurch das Paging für diese Zuweisung erzwungen wird.

</dd> <dt>

**Mappingbehavior**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, wie diese Ressource den zugrunde liegenden Ressourcen zugeordnet wird. Wenn das "custresource"-Array Einträge enthält, gibt diese Eigenschaft an, wie die Ressource diesen spezifischen Ressourcen zugeordnet wird.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)
</dt> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Nicht unterstützt** (1)
</dt> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dediziert** (2)
</dt> <dt>

<span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>**Weiche Affinität** (3)
</dt> <dt>

<span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>**Harte Affinität** (4)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)
</dt> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Hersteller reserviert** (32767.65535)
</dt> </dl>

</dd> <dt>

**Otherresourcetype**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die den Ressourcentyp beschreibt, wenn ein klar definierter Wert nicht verfügbar ist und ResourceType den Wert "Other" hat.

</dd> <dt>

**Parent**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das übergeordnete Element der Ressource. Beispielsweise ein Controller für die aktuelle Zuordnung.

</dd> <dt>

**Poolid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft gibt an, von welchem resourcepool die Ressource derzeit zugeordnet ist, oder welcher resourcepool die Ressource bei der Zuordnung zugewiesen wird.

</dd> <dt>

**Reservierung**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft gibt die Menge der Ressourcen an, die für diese Zuordnung garantiert verfügbar sind. Auf dem System, das eine Überbelegung von Ressourcen unterstützt, wird dieser Wert in der Regel für die Zugangskontrolle verwendet, um zu verhindern, dass eine Zuordnung akzeptiert wird, wodurch Ressourcenmangel verhindert wird.

</dd> <dt>

**ResourceSubType**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die einen Implementierungs spezifischen Untertyp für diese Ressource beschreibt. Dies kann z. b. verwendet werden, um unterschiedliche Modelle desselben Ressourcentyps zu unterscheiden.

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Typ der Ressource, die diese Zuordnungs Einstellung darstellt.

<dl> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)
</dt> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)
</dt> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Prozessor** (3)
</dt> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>Arbeits **Speicher** (4)
</dt> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE-Controller** (5)
</dt> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Paralleler SCSI-HBA** (6)
</dt> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>**FC-HBA** (7)
</dt> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI-HBA** (8)
</dt> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)
</dt> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet-Adapter** (10)
</dt> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Anderer Netzwerk Adapter** (11)
</dt> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>E **/a-Slot** (12)
</dt> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>E **/a-Gerät** (13)
</dt> <dt>

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Diskettenlaufwerk** (14)
</dt> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD-Laufwerk** (15)
</dt> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD-Laufwerk** (16)
</dt> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Seriellen Anschluss** (17)
</dt> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Paralleler Anschluss** (18)
</dt> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB-Controller** (19)
</dt> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Grafikcontroller** (20)
</dt> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Speicher** Block (21)
</dt> <dt>

<span id="Disk"></span><span id="disk"></span><span id="DISK"></span>Daten **Träger (22** )
</dt> <dt>

<span id="Tape"></span><span id="tape"></span><span id="TAPE"></span>**Band** (23)
</dt> <dt>

<span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Anderes Speichergerät** (24)
</dt> <dt>

<span id="Firewire_Controller"></span><span id="firewire_controller"></span><span id="FIREWIRE_CONTROLLER"></span>**Firewire-Controller** (25)
</dt> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionier Bare Einheit** (26)
</dt> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Partitionier bare Basiseinheit** (27)
</dt> <dt>

<span id="Power_Supply"></span><span id="power_supply"></span><span id="POWER_SUPPLY"></span>**Netzteil** (28)
</dt> <dt>

<span id="Cooling_Device"></span><span id="cooling_device"></span><span id="COOLING_DEVICE"></span>**Kühl Gerät** (29)
</dt> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)
</dt> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Hersteller reserviert** (32767.65535)
</dt> </dl>

</dd> <dt>

**VirtualQuantity**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft gibt die Menge der Ressourcen an, die dem Consumer vorgelegt werden. Wenn beispielsweise ResourceType = Processor ist, würde diese Eigenschaft die Anzahl der diskreten Prozessoren widerspiegeln, die dem virtuellen Computersystem präsentiert werden. Wenn ResourceType = Arbeitsspeicher vorhanden ist, kann diese Eigenschaft die Anzahl der MB widerspiegeln, die dem virtuellen Computersystem gemeldet wurden.

</dd> <dt>

**Weight**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Diese Eigenschaft gibt eine relative Priorität für diese Zuordnung in Bezug auf andere Zuordnungen desselben resourcepools an. Diese Eigenschaft hat keine Maßeinheit und ist nur im Vergleich zu anderen Zuordnungen relevant, die für dieselben Host Ressourcen konkurrieren.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ resourcezubesettingdata**](cim-resourceallocationsettingdata.md)
</dt> <dt>

[**CIM \_ resourcezubesettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> </dl>

 

