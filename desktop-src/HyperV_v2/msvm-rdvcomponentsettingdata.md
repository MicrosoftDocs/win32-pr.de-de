---
description: Stellt den konfigurierten Zustand der RDV-Komponente (Remotedesktop Virtualization) dar. Der Standardstatus ist Aktiviert.
ms.assetid: 058432d7-4439-47ec-9909-82a405d69a6e
title: Msvm_RdvComponentSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RdvComponentSettingData
- Msvm_RdvComponentSettingData.InstanceID
- Msvm_RdvComponentSettingData.Caption
- Msvm_RdvComponentSettingData.Description
- Msvm_RdvComponentSettingData.ElementName
- Msvm_RdvComponentSettingData.ResourceType
- Msvm_RdvComponentSettingData.OtherResourceType
- Msvm_RdvComponentSettingData.ResourceSubType
- Msvm_RdvComponentSettingData.PoolID
- Msvm_RdvComponentSettingData.ConsumerVisibility
- Msvm_RdvComponentSettingData.HostResource
- Msvm_RdvComponentSettingData.AllocationUnits
- Msvm_RdvComponentSettingData.VirtualQuantity
- Msvm_RdvComponentSettingData.Reservation
- Msvm_RdvComponentSettingData.Limit
- Msvm_RdvComponentSettingData.Weight
- Msvm_RdvComponentSettingData.AutomaticAllocation
- Msvm_RdvComponentSettingData.AutomaticDeallocation
- Msvm_RdvComponentSettingData.Parent
- Msvm_RdvComponentSettingData.Connection
- Msvm_RdvComponentSettingData.Address
- Msvm_RdvComponentSettingData.MappingBehavior
- Msvm_RdvComponentSettingData.AddressOnParent
- Msvm_RdvComponentSettingData.VirtualQuantityUnits
- Msvm_RdvComponentSettingData.EnabledState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3b99b0949ef8a6a45c10913719d18596439ba073efb1bc6e14c1816332ab4d61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789640"
---
# <a name="msvm_rdvcomponentsettingdata-class"></a>Msvm \_ RdvComponentSettingData-Klasse

Stellt den konfigurierten Zustand der RDV-Komponente (Remotedesktop Virtualization) dar. Der Standardstatus ist Aktiviert.

Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_RdvComponentSettingData : CIM_ResourceAllocationSettingData
{
  string  InstanceID;
  string  Caption = "Remote Desktop Virtualization Service Default Settings";
  string  Description = "Describes the default settings for the Remote Desktop Virtualization Service resources.";
  string  ElementName;
  uint16  ResourceType = 33;
  string  OtherResourceType;
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource[];
  string  AllocationUnits = "count";
  uint64  VirtualQuantity = 1;
  uint64  Reservation = 1;
  uint64  Limit = 1;
  uint32  Weight = 0;
  boolean AutomaticAllocation = True;
  boolean AutomaticDeallocation = True;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
  uint16  EnabledState = 2;
};
```

## <a name="members"></a>Member

Die **Msvm \_ RdvComponentSettingData-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ RdvComponentSettingData-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Adresse**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Adresse der Ressource. Diese Eigenschaft wird von [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

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

Eine kurze Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und immer auf "Ethernet Switch Port Einstellungen" festgelegt.

</dd> <dt>

**Connection**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Gerät, mit dem diese Ressource verbunden ist. Diese Eigenschaft wird von [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

</dd> <dt>

**ConsumerVisibility**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Sichtbarkeit des Consumers für die zugeordnete Ressource. Diese Eigenschaft wird von [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt und immer auf 3 (virtualisiert) festgelegt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und immer auf "Ethernet Switch Port Einstellungen" festgelegt.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeigename für das Objekt. Diese Eigenschaft wird von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))geerbt. Wenn Sie diese Eigenschaft ändern, ändert sich der Elementname der zugeordneten logischen Geräteableitung.

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der aktivierte und deaktivierte Status eines Elements. Gültige Werte sind 2 (aktiviert) und 3 (deaktiviert). Der Standardwert ist 2 (aktiviert). Dies ist eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**ModifyVirtualSystemResources-Methode**](/previous-versions/windows/desktop/virtual/modifyvirtualsystemresources-msvm-virtualsystemmanagementservice) der [**Msvm \_ VirtualSystemManagementService-Klasse**](msvm-virtualsystemmanagementservice.md) geändert werden kann.

</dd> <dt>

**HostResource**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Jedem Gerät im virtuellen Switch kann nur eine Hostressource zugewiesen werden, sodass nur das erste Element dieses Arrays festgelegt werden kann. Legen Sie für Geräte, die dieses Feature unterstützen, das erste Element des **HostResource-Arrays** so fest, dass es einen Verweis auf die zugrunde liegende Hostressource enthält, die zugewiesen werden soll. Diese Eigenschaft wird von [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Identifiziert eine Instanz dieser Klasse eindeutig. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Begrenzung**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die maximale Menge der entsprechenden Hostressourcen, die vom virtuellen Switch genutzt werden können. Diese Eigenschaft wird von [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

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

Eine Zeichenfolge, die den Ressourcentyp beschreibt, wenn kein klar definierter Wert verfügbar ist und [**ResourceType**](msvm-processorsettingdata.md) den Wert 1 (Sonstige) auf hat. Diese Eigenschaft wird von [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt und nicht verwendet.

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

Der Bezeichner des Ressourcenpools, aus dem diese Ressource zugeordnet wurde. Diese Eigenschaft wird von [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

</dd> <dt>

**Reservierung**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Menge der Ressourcen, die für die Verwendung durch den virtuellen Switch reserviert sind. Diese Eigenschaft wird von [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

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

Der Typ der Ressource, die von dieser Zuordnungseinstellung dargestellt wird. Diese Eigenschaft wird von [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt und immer auf 33 (Ethernetverbindung) festgelegt.

</dd> <dt>

**VirtualQuantity**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Gesamtzahl der Ports im virtuellen Switch. Diese Eigenschaft wird von [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

</dd> <dt>

**VirtualQuantityUnits**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die Maßeinheit für die **VirtualQuantity-Eigenschaft** an. Der Wert dieser Eigenschaft muss ein rechtlicher Wert des Qualifizierers "Programmgesteuerte Einheiten" sein, wie in Anhang C.1 von DSP0004 V2.5 oder höher definiert. Diese Eigenschaft wird von [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

</dd> <dt>

**Weight**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine ganze Zahl, die die Gewichtung für jeden virtuellen Switch definiert. Diese Eigenschaft wird von [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)geerbt.

Bereich: 0 1000

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

