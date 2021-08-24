---
description: Stellt die Einstellungsdaten des virtuellen LAN (VLAN) dar.
ms.assetid: c3a49021-5256-4751-a5a5-81bf1c6d6e6d
title: Msvm_EthernetSwitchPortVlanSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortVlanSettingData
- Msvm_EthernetSwitchPortVlanSettingData.InstanceID
- Msvm_EthernetSwitchPortVlanSettingData.Caption
- Msvm_EthernetSwitchPortVlanSettingData.Description
- Msvm_EthernetSwitchPortVlanSettingData.ElementName
- Msvm_EthernetSwitchPortVlanSettingData.OperationMode
- Msvm_EthernetSwitchPortVlanSettingData.AccessVlanId
- Msvm_EthernetSwitchPortVlanSettingData.NativeVlanId
- Msvm_EthernetSwitchPortVlanSettingData.PvlanMode
- Msvm_EthernetSwitchPortVlanSettingData.PrimaryVlanId
- Msvm_EthernetSwitchPortVlanSettingData.SecondaryVlanId
- Msvm_EthernetSwitchPortVlanSettingData.PruneVlanIdArray
- Msvm_EthernetSwitchPortVlanSettingData.TrunkVlanIdArray
- Msvm_EthernetSwitchPortVlanSettingData.SecondaryVlanIdArray
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8c4d9c3c3101cb7593f54e8624a2d7e316cb27378b0ad504cdf8364b03020efb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119523770"
---
# <a name="msvm_ethernetswitchportvlansettingdata-class"></a>Msvm \_ EthernetSwitchPortVlanSettingData-Klasse

Stellt die Einstellungsdaten des virtuellen LAN (VLAN) dar.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("952C5004-4465-451C-8CB8-FA9AB382B773"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port VLAN Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortVlanSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port VLAN Settings";
  string Description = "Represents the vlan setting data.";
  string ElementName = "Ethernet Switch Port VLAN Settings";
  uint32 OperationMode = 0;
  uint16 AccessVlanId = 0;
  uint16 NativeVlanId = 0;
  uint32 PvlanMode = 0;
  uint16 PrimaryVlanId = 0;
  uint16 SecondaryVlanId = 0;
  uint16 PruneVlanIdArray[] = {};
  uint16 TrunkVlanIdArray[] = {};
  uint16 SecondaryVlanIdArray[] = {};
};
```

## <a name="members"></a>Member

Die **Msvm \_ EthernetSwitchPortVlanSettingData-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ EthernetSwitchPortVlanSettingData-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AccessVlanId**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Gibt den VLAN-Bezeichner im Zugriffsmodus an.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement geerbt**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)und immer auf "Ethernet Switch Port VLAN Einstellungen" festgelegt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ ManagedElement geerbt**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)und immer auf "Stellt die Vlan-Einstellungsdaten dar." festgelegt.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeigename für das Objekt. Diese Eigenschaft wird von [**CIM \_ ManagedElement geerbt**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)und immer auf "Ethernet Switch Port VLAN Einstellungen" festgelegt.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Identifiziert eine Instanz dieser Klasse eindeutig. Diese Eigenschaft wird von [**CIM \_ ManagedElement geerbt.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**NativeVlanId**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Gibt den VLAN-Bezeichner im Trunkmodus an.

</dd> <dt>

**OperationMode**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Gibt den VLAN-Betriebsmodus an.

<dt>

<span id="Access"></span><span id="access"></span><span id="ACCESS"></span>

**Zugriff** (1)


</dt> <dd></dd> <dt>

<span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span>

**Trunk** (2)


</dt> <dd></dd> <dt>

<span id="Private"></span><span id="private"></span><span id="PRIVATE"></span>

**Privat** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**PrimaryVlanId**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Gibt den primären VLAN-Bezeichner im privaten Modus an.

</dd> <dt>

**PruneVlanIdArray**
</dt> <dd> <dl> <dt>

Datentyp: **uint16 array**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Gibt die Bezeichnerbitmap des Bezeichners "Prune VLAN" im Trunkmodus an.

</dd> <dt>

**PvlanMode**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Gibt den privaten VLAN-Modus an.

<dt>

<span id="Isolated"></span><span id="isolated"></span><span id="ISOLATED"></span>

**Isoliert** (1)


</dt> <dd></dd> <dt>

<span id="Community"></span><span id="community"></span><span id="COMMUNITY"></span>

**Community** (2)


</dt> <dd></dd> <dt>

<span id="Promiscuous"></span><span id="promiscuous"></span><span id="PROMISCUOUS"></span>

**Promiscuous** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**SecondaryVlanId**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Gibt den sekundären VLAN-Bezeichner im privaten Modus an.

</dd> <dt>

**SecondaryVlanIdArray**
</dt> <dd> <dl> <dt>

Datentyp: **uint16 array**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Gibt die sekundäre VLAN-Bezeichnerbitmap im privaten Modus an.

</dd> <dt>

**TrunkVlanIdArray**
</dt> <dd> <dl> <dt>

Datentyp: **uint16 array**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Gibt die Trunk-VLAN-Bezeichnerbitmap im Trunkmodus an.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

