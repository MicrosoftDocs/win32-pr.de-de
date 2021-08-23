---
description: Stellt den Ressourcenstatus der Switchbandbreite dar.
ms.assetid: 9aa3e57e-9452-4c60-a052-83ae35b3607c
title: Msvm_EthernetSwitchBandwidthData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchBandwidthData
- Msvm_EthernetSwitchBandwidthData.InstanceID
- Msvm_EthernetSwitchBandwidthData.Caption
- Msvm_EthernetSwitchBandwidthData.Description
- Msvm_EthernetSwitchBandwidthData.ElementName
- Msvm_EthernetSwitchBandwidthData.SystemCreationClassName
- Msvm_EthernetSwitchBandwidthData.SystemName
- Msvm_EthernetSwitchBandwidthData.CreationClassName
- Msvm_EthernetSwitchBandwidthData.Name
- Msvm_EthernetSwitchBandwidthData.Capacity
- Msvm_EthernetSwitchBandwidthData.Reservation
- Msvm_EthernetSwitchBandwidthData.DefaultFlowReservationPercentage
- Msvm_EthernetSwitchBandwidthData.DefaultFlowReservation
- Msvm_EthernetSwitchBandwidthData.DefaultFlowWeight
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 422efc93de56c520f0929ca9d7f0b53a5911bcc553f529e2efeb8fbc70d8cf3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119524650"
---
# <a name="msvm_ethernetswitchbandwidthdata-class"></a>Msvm \_ EthernetSwitchBandwidthData-Klasse

Stellt den Ressourcenstatus der Switchbandbreite dar.

Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("8F425906-034D-42AB-BD16-EDB31CEC55EF"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Bandwidth data"), AMENDMENT]
class Msvm_EthernetSwitchBandwidthData : Msvm_EthernetSwitchData
{
  string InstanceID;
  string Caption = "Ethernet Switch Bandwidth data";
  string Description = "Represents the switch bandwidth resource status.";
  string ElementName = "Ethernet Switch Bandwidth data";
  string SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string SystemName;
  string CreationClassName = "Msvm_EthernetSwitchBandwidthData";
  string Name;
  uint64 Capacity = 100000000;
  uint64 Reservation = 100000000;
  uint32 DefaultFlowReservationPercentage = 10;
  uint64 DefaultFlowReservation = 100000000;
  uint64 DefaultFlowWeight = 0;
};
```

## <a name="members"></a>Member

Die **Msvm \_ EthernetSwitchBandwidthData-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ EthernetSwitchBandwidthData-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Capacity**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Die maximale Bandbreite, die für den Switch verfügbar ist.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel,** **MaxLen** (256)
</dt> </dl>

Der Name der Klasse oder Unterklasse, die bei der Erstellung dieser Instanz verwendet wird.

</dd> <dt>

**DefaultFlowReservation**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Die aktuelle absolute Bandbreite, die für den Switch für den Standardflow reserviert ist.

</dd> <dt>

**DefaultFlowReservationPercentage**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Der aktuelle Prozentsatz der Bandbreite, die für den Switch für den Standardflow reserviert ist.

</dd> <dt>

**DefaultFlowWeight**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Die aktuelle Gewichtung für den Standardflow auf dem Switch.

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

Ein Anzeigename für das Objekt. Diese Eigenschaft wird von [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

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

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel,** **Außerkraftsetzung,** **MaxLen** (256)
</dt> </dl>

Der eindeutige Name der Ressource.

</dd> <dt>

**Reservierung**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Die aktuelle Bandbreite, die für den Switch reserviert ist.

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel,** **MaxLen** (256)
</dt> </dl>

Der Name der Erstellungsklasse des Hostingsystems. Diese Eigenschaft wird vom [**\_ CIM-Dienst**](/windows/desktop/CIMWin32Prov/cim-service)geerbt.

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel,** **MaxLen** (256)
</dt> </dl>

Der Name des virtuellen Switches, an den die zugeordnete Ressourceninstanz gebunden ist.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

