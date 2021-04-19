---
description: Stellt die Einstellungen des virtuellen Prozessors für eine virtuelle Maschine dar.
ms.assetid: 2B299793-E1CD-49D4-898C-AE60B49F44F5
title: Msvm_ProcessorSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ProcessorSettingData
- Msvm_ProcessorSettingData.InstanceID
- Msvm_ProcessorSettingData.Caption
- Msvm_ProcessorSettingData.Description
- Msvm_ProcessorSettingData.ElementName
- Msvm_ProcessorSettingData.ResourceType
- Msvm_ProcessorSettingData.OtherResourceType
- Msvm_ProcessorSettingData.ResourceSubType
- Msvm_ProcessorSettingData.PoolID
- Msvm_ProcessorSettingData.ConsumerVisibility
- Msvm_ProcessorSettingData.HostResource
- Msvm_ProcessorSettingData.AllocationUnits
- Msvm_ProcessorSettingData.VirtualQuantity
- Msvm_ProcessorSettingData.Reservation
- Msvm_ProcessorSettingData.Limit
- Msvm_ProcessorSettingData.Weight
- Msvm_ProcessorSettingData.AutomaticAllocation
- Msvm_ProcessorSettingData.AutomaticDeallocation
- Msvm_ProcessorSettingData.Parent
- Msvm_ProcessorSettingData.Connection
- Msvm_ProcessorSettingData.Address
- Msvm_ProcessorSettingData.MappingBehavior
- Msvm_ProcessorSettingData.AddressOnParent
- Msvm_ProcessorSettingData.VirtualQuantityUnits
- Msvm_ProcessorSettingData.LimitCPUID
- Msvm_ProcessorSettingData.HwThreadsPerCore
- Msvm_ProcessorSettingData.LimitProcessorFeatures
- Msvm_ProcessorSettingData.MaxProcessorsPerNumaNode
- Msvm_ProcessorSettingData.MaxNumaNodesPerSocket
- Msvm_ProcessorSettingData.EnableHostResourceProtection
- Msvm_ProcessorSettingData.CpuGroupId
- Msvm_ProcessorSettingData.HideHypervisorPresent
- Msvm_ProcessorSettingData.ExposeVirtualizationExtensions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5154105c4deab13f93bb65078a5c9527283620e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106367976"
---
# <a name="msvm_processorsettingdata-class"></a>MSVM \_ processorsettingdata-Klasse

Stellt die Einstellungen des virtuellen Prozessors für eine virtuelle Maschine dar.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ProcessorSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Processor";
  string  Description = "A logical processor of the hypervisor running on the host computer system.";
  string  ElementName;
  uint16  ResourceType = 3;
  string  OtherResourceType;
  string  ResourceSubType = "Microsoft:Hyper-V:Processor";
  string  PoolID;
  uint16  ConsumerVisibility;
  string  HostResource[];
  string  AllocationUnits = "percent / 1000";
  uint64  VirtualQuantity = "count";
  uint64  Reservation = 0;
  uint64  Limit = 100000;
  uint32  Weight = 100;
  boolean AutomaticAllocation = True;
  boolean AutomaticDeallocation = True;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
  boolean LimitCPUID;
  uint64  HwThreadsPerCore;
  boolean LimitProcessorFeatures;
  uint64  MaxProcessorsPerNumaNode;
  uint64  MaxNumaNodesPerSocket;
  boolean EnableHostResourceProtection;
  string  CpuGroupId;
  boolean HideHypervisorPresent;
  boolean ExposeVirtualizationExtensions;
};
```

## <a name="members"></a>Member

Die **MSVM \_ processorsettingdata** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ processorsettingdata** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Adresse**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Adresse der Ressource. Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

</dd> <dt>

**Addressonparent**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Beschreibt die Adresse dieser Ressource im Kontext des übergeordneten Elements. Die über **geordneten** und **addressonparent** -Eigenschaften werden verwendet, um die Controller Beziehung sowie die Reihenfolge von Geräten auf einem Controller zu beschreiben. Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

</dd> <dt>

**Zuordnung von Einheiten**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Zuordnungs Einheiten, die von den **Reservierungs** -und **Limit** -Eigenschaften verwendet werden. Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

</dd> <dt>

**Automaticallocation**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Ressource automatisch zugewiesen wird. Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

</dd> <dt>

**Automaticdeallocation**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Zuordnung der Ressource automatisch aufgehoben wird. Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **maxlen** (64)
</dt> </dl>

Eine kurze Beschreibung des-Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Connection**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Gerät, mit dem diese Ressource verbunden ist. Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

</dd> <dt>

**Consumersichtbarkeit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Beschreibt die Sichtbarkeit der Consumer der zugeordneten Ressource. Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

</dd> <dt>

**Cpugroupid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die CPU-Gruppen-ID, an die diese VM gebunden ist. Wenn der Wert 0 ist, bedeutet dies, dass er nicht an eine bestimmte CPU-Gruppe gebunden ist.

> [!Note]  
> Diese Eigenschaft wurde in Windows 10, Version 1703, hinzugefügt.

 

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeige Name für das-Objekt. Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt. Durch Ändern dieser Eigenschaft wird der **ElementName** der zugeordneten logischen Geräte Ableitung geändert.

</dd> <dt>

**Enablehustresourceprotection**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die VM Features aktivieren soll, mit denen der Schutz von Host Ressourcen von der Arbeitsauslastung auf dem virtuellen Computer erhöht wird.

> [!Note]  
> In Windows 10 hinzugefügt.

 

</dd> <dt>

**Expoabvirtualizationextensions**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob Hyper-V virtualisierte hardwarevirtualisierungserweiterungen für die VM verfügbar machen soll.

> [!Note]  
> Diese Eigenschaft wurde in Windows 10, Version 1703, hinzugefügt.

 

</dd> <dt>

**Hidehypervisorpresent**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob Hyper-V angeben soll, dass ein Hypervisor für den verbundenen Gast vorhanden ist.

> [!Note]  
> Diese Eigenschaft wurde in Windows 10, Version 1703, hinzugefügt.

 

</dd> <dt>

**"Hustresource"**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Macht eine bestimmte Zuweisung zum Hosten von oder zugrunde liegenden Ressourcen verfügbar. Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) geerbt und ist immer auf **null** festgelegt.

</dd> <dt>

**Hwthreadspercore**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Anzahl der SMT-Threads pro Kern an, die dem Gast gemeldet wurden. Diese Berichterstellung ist unabhängig davon, ob die Hardware für SMT vorhanden ist.

> [!Note]  
> Diese Eigenschaft wurde in Windows 10, Version 1703, hinzugefügt.

 

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Identifiziert eine Instanz dieser Klasse eindeutig. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Begrenzung**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die maximale Menge an CPU-Ressourcen, die vom virtuellen Computer genutzt werden kann. Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

100.000

Bereich: 0 100000

</dd> <dt>

**Limitcpuid**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der virtuelle Computer den CPU-Bezeichner verringern soll. Bei einigen älteren Betriebssystemen ist es möglicherweise erforderlich, die Prozessor Funktionalität auf diese Weise zu begrenzen, damit Sie ausgeführt werden kann.

</dd> <dt>

**Limitprocessorfeatures**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der virtuelle Computer die für das Betriebssystem verfügbar gemachten CPU-Features einschränken soll. Durch das Einschränken der Prozessor Features kann der virtuelle Computer auf unterschiedliche Host Computersysteme mit unterschiedlichen Prozessoren migriert werden. Das Migrieren virtueller Maschinen zwischen Computern mit Prozessoren von unterschiedlichen Anbietern wird nicht unterstützt.

</dd> <dt>

**Mappingbehavior**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, wie diese Ressource den zugrunde liegenden Ressourcen zugeordnet wird. Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

</dd> <dt>

**Maxnumanodespersocket**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die maximale Anzahl von NUMA-Knoten, die innerhalb des virtuellen Computers beobachtet werden können, wenn er zu einem einzelnen Prozessor Socket gehört.

</dd> <dt>

**Maxprocessorspernumanode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die maximale Anzahl virtueller Prozessoren, die innerhalb des virtuellen Computers beobachtet werden können, wenn Sie zu einem einzelnen virtuellen NUMA-Knoten gehören.

</dd> <dt>

**Otherresourcetype**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die den Ressourcentyp beschreibt, wenn ein klar definierter Wert nicht verfügbar ist und **ResourceType** den Wert 1 (sonstige) aufweist. Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

</dd> <dt>

**Parent**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das übergeordnete Element der Ressource. Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

</dd> <dt>

**Poolid**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Bezeichner des Ressourcenpools, von dem diese Ressource zugewiesen wurde. Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

</dd> <dt>

**Reservierung**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Menge der CPU-Ressourcen, die für die Verwendung durch den virtuellen Computer reserviert sind. Diese Ressourcen sind garantiert für den Verbrauch durch den virtuellen Computer verfügbar. Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

0

Bereich: 0 100000

</dd> <dt>

**ResourceSubType**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die einen Implementierungs spezifischen Untertyp für diese Ressource beschreibt. Dies kann z. b. verwendet werden, um unterschiedliche Modelle desselben Ressourcentyps zu unterscheiden. Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Typ der Ressource, die diese Zuordnungs Einstellung darstellt. Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

</dd> <dt>

**VirtualQuantity**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Gesamtanzahl der Kerne auf dem virtuellen Computer. Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

</dd> <dt>

**Virtualquantityunits**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Maßeinheit für diese Ressourcenzuweisung an. Der Wert dieser Eigenschaft muss ein gültiger Wert des Qualifizierers für programmgesteuerte Einheiten sein, wie in Anhang C. 1 von DSP0004 v 2.5 oder höher definiert. Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

</dd> <dt>

**Weight**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Gewichtung für jeden Prozessor der virtuellen Maschine. Nachdem alle Reserven erfüllt wurden, wird die verbleibende physische Prozessor Kapazität der Hostingplattform virtuellen Computern basierend auf ihren relativen Gewichtungen zugewiesen. Diese Eigenschaft wird von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

100

Bereich: 0 10000

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die **MSVM \_ processorsettingdata** -Klasse kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**CIM \_ resourcezubesettingdata**](cim-resourceallocationsettingdata.md)
</dt> <dt>

[**CIM \_ resourcezubesettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)
</dt> <dt>

[Prozessor Klassen](processor-classes.md)
</dt> </dl>

 

