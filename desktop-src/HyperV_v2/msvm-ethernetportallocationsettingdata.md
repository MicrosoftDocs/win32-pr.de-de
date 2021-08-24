---
description: Stellt eine Zuordnungsanforderung für einen statischen oder dynamischen Switchport dar oder stellt die aktive Konfiguration eines derzeit zugewiesenen statischen oder dynamischen Switchports dar.
ms.assetid: ef70b72f-75a0-448e-a648-6a28c12f0da1
title: Msvm_EthernetPortAllocationSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortAllocationSettingData
- Msvm_EthernetPortAllocationSettingData.InstanceID
- Msvm_EthernetPortAllocationSettingData.Caption
- Msvm_EthernetPortAllocationSettingData.Description
- Msvm_EthernetPortAllocationSettingData.ElementName
- Msvm_EthernetPortAllocationSettingData.ResourceType
- Msvm_EthernetPortAllocationSettingData.OtherResourceType
- Msvm_EthernetPortAllocationSettingData.ResourceSubType
- Msvm_EthernetPortAllocationSettingData.PoolID
- Msvm_EthernetPortAllocationSettingData.ConsumerVisibility
- Msvm_EthernetPortAllocationSettingData.HostResource
- Msvm_EthernetPortAllocationSettingData.AllocationUnits
- Msvm_EthernetPortAllocationSettingData.VirtualQuantity
- Msvm_EthernetPortAllocationSettingData.Reservation
- Msvm_EthernetPortAllocationSettingData.Limit
- Msvm_EthernetPortAllocationSettingData.Weight
- Msvm_EthernetPortAllocationSettingData.AutomaticAllocation
- Msvm_EthernetPortAllocationSettingData.AutomaticDeallocation
- Msvm_EthernetPortAllocationSettingData.Parent
- Msvm_EthernetPortAllocationSettingData.Connection
- Msvm_EthernetPortAllocationSettingData.Address
- Msvm_EthernetPortAllocationSettingData.MappingBehavior
- Msvm_EthernetPortAllocationSettingData.AddressOnParent
- Msvm_EthernetPortAllocationSettingData.VirtualQuantityUnits
- Msvm_EthernetPortAllocationSettingData.DesiredVLANEndpointMode
- Msvm_EthernetPortAllocationSettingData.OtherEndpointMode
- Msvm_EthernetPortAllocationSettingData.EnabledState
- Msvm_EthernetPortAllocationSettingData.LastKnownSwitchName
- Msvm_EthernetPortAllocationSettingData.RequiredFeatures
- Msvm_EthernetPortAllocationSettingData.RequiredFeatureHints
- Msvm_EthernetPortAllocationSettingData.TestReplicaPoolID
- Msvm_EthernetPortAllocationSettingData.TestReplicaSwitchName
- Msvm_EthernetPortAllocationSettingData.CompartmentGuid
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: be3968f52065259cb69ad35721dffd3ac606da98e4189edaad1b762120f5a008
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681580"
---
# <a name="msvm_ethernetportallocationsettingdata-class"></a>Msvm \_ EthernetPortAllocationSettingData-Klasse

Stellt eine Zuordnungsanforderung für einen statischen oder dynamischen Switchport dar oder stellt die aktive Konfiguration eines derzeit zugewiesenen statischen oder dynamischen Switchports dar. Eine Zuordnungsanforderung für einen dynamischen Switchport wird auch als Verbindungsanforderung bezeichnet.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortAllocationSettingData : CIM_EthernetPortAllocationSettingData
{
  string  InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string  Caption = "Ethernet Switch Port Settings";
  string  Description = "Ethernet Switch Port Settings";
  string  ElementName;
  uint16  ResourceType = 33;
  string  OtherResourceType;
  string  ResourceSubType;
  string  PoolID;
  uint16  ConsumerVisibility = 3;
  string  HostResource[];
  string  AllocationUnits;
  uint64  VirtualQuantity;
  uint64  Reservation;
  uint64  Limit;
  uint32  Weight = 0;
  boolean AutomaticAllocation;
  boolean AutomaticDeallocation;
  string  Parent;
  string  Connection[];
  string  Address;
  uint16  MappingBehavior;
  string  AddressOnParent;
  string  VirtualQuantityUnits = "count";
  uint16  DesiredVLANEndpointMode;
  string  OtherEndpointMode;
  uint16  EnabledState;
  string  LastKnownSwitchName;
  string  RequiredFeatures[];
  string  RequiredFeatureHints[];
  string  TestReplicaPoolID;
  string  TestReplicaSwitchName;
  string  CompartmentGuid;
};
```

## <a name="members"></a>Member

Die **Msvm \_ EthernetPortAllocationSettingData-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ EthernetPortAllocationSettingData-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Adresse**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Adresse der Ressource. Diese Eigenschaft wird von [**CIM \_ ResourceAllocationSettingData geerbt.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**AddressOnParent**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Beschreibt die Adresse dieser Ressource im Kontext des übergeordneten Elements. Die **Eigenschaften Parent** und **AddressOnParent** werden verwendet, um die Controllerbeziehung sowie die Reihenfolge der Geräte auf einem Controller zu beschreiben. Diese Eigenschaft wird von [**CIM \_ ResourceAllocationSettingData geerbt.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**AllocationUnits**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Zuordnungseinheit, die von den **Eigenschaften Reservierung** und **Limit verwendet** wird. Diese Eigenschaft wird von [**CIM \_ ResourceAllocationSettingData geerbt.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**AutomaticAllocation**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Ressource automatisch zugeordnet wird. Diese Eigenschaft wird von [**CIM \_ ResourceAllocationSettingData geerbt.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**AutomaticDeallocation**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Ressourcenzuordnung automatisch gelöscht wird. Diese Eigenschaft wird von [**CIM \_ ResourceAllocationSettingData geerbt.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **MaxLen** (64)
</dt> </dl>

Eine kurze Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement geerbt**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)und immer auf "Ethernet Switch Port Einstellungen" festgelegt.

</dd> <dt>

**CompartmentGuid**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Diese Eigenschaft gibt das Zielnetzwerkdepartment für den Port an. Dies wird nur für interne Adapter unterstützt.

> [!Note]  
> Eigenschaft, die in Windows 10.

 

</dd> <dt>

**Connection**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Gerät, mit dem diese Ressource verbunden ist. Diese Eigenschaft wird von [**CIM \_ ResourceAllocationSettingData geerbt.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

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

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement geerbt**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)und immer auf "Ethernet Switch Port Einstellungen" festgelegt.

</dd> <dt>

**DesiredVLANEndpointMode**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der gewünschte Konfigurationsmodus für den VLAN-Endpunkt. Mit dieser Eigenschaft wird der anfängliche **OperationalEndpointMode-Eigenschaftswert** in der Instanz der [**Msvm \_ VLANEndpoint-Klasse**](msvm-vlanendpoint.md) festgelegt, die dem Ziel-Ethernetport zugeordnet ist. Mögliche Werte finden Sie in der **OperationalEndpointMode-Eigenschaft** der **Msvm \_ VLANEndpoint-Klasse.** Diese Eigenschaft wird von **CIM \_ EthernetPortAllocationSettingData geerbt.**

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeigename für das Objekt. Diese Eigenschaft wird von [**CIM \_ SettingData geerbt.**](/previous-versions//cc136911(v=vs.85)) Wenn Sie diese Eigenschaft ändern, ändert sich der Elementname der zugehörigen logischen Geräteerleitung.

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Zuordnungsanforderung aktiviert oder deaktiviert ist. Wenn eine Zuordnungsanforderung als Deaktiviert (3) markiert ist, wird die Zuordnung nicht verarbeitet. Der **EnabledState für** eine aktive Konfiguration ist immer als Aktiviert (2) gekennzeichnet.

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

Jedem Gerät im virtuellen Switch kann nur eine Hostressource zugewiesen werden, sodass nur das erste Element dieses Arrays festgelegt werden kann. Legen Sie für Geräte, die dieses Feature unterstützen, das erste Element des **HostResource-Arrays** so fest, dass es einen Verweis auf die zugrunde liegende Hostressource enthält, die zugewiesen werden soll. Diese Eigenschaft wird von [**CIM \_ ResourceAllocationSettingData geerbt.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Identifiziert eine Instanz dieser Klasse eindeutig. Diese Eigenschaft wird von [**CIM \_ SettingData geerbt**](/previous-versions//cc136911(v=vs.85))und immer auf "Microsoft:*GUID* \\ *DeviceSpecificData"* festgelegt.

</dd> <dt>

**LastKnownSwitchName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der letzte bekannte Anzeigename des Schalters, mit dem dieser Port ggf. eine harte Affinität hatte.

> [!Note]  
> In Windows 10 hinzugefügte Eigenschaft.

 

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

**OtherEndpointMode**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Zeichenfolge, die den Typ des VLAN-Endpunktmodells beschreibt, das von diesem VLAN-Endpunkt unterstützt wird. Diese Eigenschaft wird nur verwendet, wenn die **DesiredVLANEndpointMode-Eigenschaft** auf 1 (Other) festgelegt ist. Diese Eigenschaft sollte auf **NULL** festgelegt werden, wenn die **DesiredVLANEndpointMode-Eigenschaft** ein anderer Wert als 1 ist. Diese Eigenschaft wird von **CIM \_ EthernetPortAllocationSettingData** geerbt.

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

**RequiredFeatureHints**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Liste der Anzeigenamen, die den einzelnen Einträgen im **RequiredFeatures-Array** entsprechen.

</dd> <dt>

**RequiredFeatures**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die Liste der Featurebezeichner, die alle Features darstellen, die für einen Port erforderlich sind.

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

**TestReplicaPoolID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt den Netzwerkressourcenpool an, aus dem dem Testreplikatsystem beim Erstellen eine Verbindung zugeordnet wird.

</dd> <dt>

**TestReplicaSwitchName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Gibt den Anzeigenamen des virtuellen Netzwerkswitches an, dem beim Erstellen eine Verbindung für das Testreplikatsystem zugeordnet wird.

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



 

