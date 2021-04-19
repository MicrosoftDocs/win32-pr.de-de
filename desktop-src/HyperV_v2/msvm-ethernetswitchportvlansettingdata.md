---
description: Stellt die Einstellungsdaten für das virtuelle LAN (VLAN) dar.
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
ms.openlocfilehash: 6fce6416696a99e5d928b774e2ba2a05b1dc21d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364266"
---
# <a name="msvm_ethernetswitchportvlansettingdata-class"></a>MSVM \_ ethernetzwitchportvlansettingdata-Klasse

Stellt die Einstellungsdaten für das virtuelle LAN (VLAN) dar.

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

Die **MSVM \_ ethernetzwitchportvlansettingdata** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ ethernetzwitchportvlansettingdata** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Accessvlanid**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **wmidataid** (2), **interfacetten** (1), **interfakerevision** (0)
</dt> </dl>

Gibt die VLAN-Kennung im Zugriffsmodus an.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des-Objekts. Diese Eigenschaft wird vom [**CIM- \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Ethernet Switch Port VLAN Settings" festgelegt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "stellt die VLAN-Einstellungsdaten" fest.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeige Name für das-Objekt. Diese Eigenschaft wird vom [**CIM- \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Ethernet Switch Port VLAN Settings" festgelegt.

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

**Nativevlanid**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **wmidataid** (3), **interfacetten** (1), **interfakerevision** (0)
</dt> </dl>

Gibt die VLAN-Kennung im trunk Modus an.

</dd> <dt>

**OperationMode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **wmidataid** (1), **interfacetten** (1), **interfakerevision** (0)
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

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **wmidataid** (5), **interfacetten** (1), **interfakerevision** (0)
</dt> </dl>

Gibt den primären VLAN-Bezeichner im privaten Modus an.

</dd> <dt>

**Prunevlanidarray**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **wmidataid** (7), **interfacetten** (1), **interfakerevision** (0)
</dt> </dl>

Gibt die Bitmap des VLAN-Bezeichners im trunk Modus an.

</dd> <dt>

**Pvlanmode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **wmidataid** (4), **interfacetten** (1), **interfakerevision** (0)
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

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **wmidataid** (6), **interfacetten** (1), **interfakerevision** (0)
</dt> </dl>

Gibt den sekundären VLAN-Bezeichner im privaten Modus an.

</dd> <dt>

**Secondaryvlanidarray**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **wmidataid** (9), **interfacetten** (1), **interfakerevision** (0)
</dt> </dl>

Gibt die sekundäre VLAN-bezeichnerbitmap im privaten Modus an.

</dd> <dt>

**Trunkvlanidarray**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **wmidataid** (8), **interfacetten** (1), **interfakerevision** (0)
</dt> </dl>

Gibt die Bitmap des trunk-VLAN-Bezeichners im trunk Modus an.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

