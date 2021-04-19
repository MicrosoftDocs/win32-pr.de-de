---
description: Stellt die Einstellungen für die Port Bandbreite dar.
ms.assetid: 62a42c4c-8ea1-47c6-8ae6-e9252f2ed0e4
title: Msvm_EthernetSwitchPortBandwidthSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortBandwidthSettingData
- Msvm_EthernetSwitchPortBandwidthSettingData.InstanceID
- Msvm_EthernetSwitchPortBandwidthSettingData.Caption
- Msvm_EthernetSwitchPortBandwidthSettingData.Description
- Msvm_EthernetSwitchPortBandwidthSettingData.ElementName
- Msvm_EthernetSwitchPortBandwidthSettingData.Reservation
- Msvm_EthernetSwitchPortBandwidthSettingData.Weight
- Msvm_EthernetSwitchPortBandwidthSettingData.Limit
- Msvm_EthernetSwitchPortBandwidthSettingData.BurstLimit
- Msvm_EthernetSwitchPortBandwidthSettingData.BurstSize
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 932207a8157e34c5f42894c31efa78090a6a80f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362896"
---
# <a name="msvm_ethernetswitchportbandwidthsettingdata-class"></a>MSVM \_ ethernetzwitchportbandwidthsettingdata-Klasse

Stellt die Einstellungen für die Port Bandbreite dar.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, UUID("24AD3CE1-69BD-4978-B2AC-DAAD389D699C"), Provider("VmmsWmiInstanceAndMethodProvider"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Bandwidth Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortBandwidthSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port Bandwidth Settings";
  string Description = "Represents the port bandwidth settings.";
  string ElementName = "Ethernet Switch Port Bandwidth Settings";
  uint64 Reservation = 0;
  uint64 Weight = 0;
  uint64 Limit = 0;
  uint64 BurstLimit = 0;
  uint64 BurstSize = 0;
};
```

## <a name="members"></a>Member

Die **MSVM \_ ethernetzwitchportbandwidthsettingdata** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ ethernetzwitchportbandwidthsettingdata** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Burstlimit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **wmidataid** (4), **interfacetten** (1), **interfakerevision** (0)
</dt> </dl>

Die vom Port zulässige Spitzen Bandbreite während des auftretende.

</dd> <dt>

**Burstsize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **wmidataid** (5), **interfacetten** (1), **interfakerevision** (0)
</dt> </dl>

Die maximal zulässige Burst Größe.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des-Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Ethernet Switch Port Bandwidth Settings" festgelegt.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "stellt die Einstellungen für die Port Bandbreite" fest.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Anzeige Name für das-Objekt. Diese Eigenschaft wird von [**CIM \_ managedelta Element**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt und ist immer auf "Ethernet Switch Port Bandwidth Settings" festgelegt.

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

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **wmidataid** (3), **interfacetten** (1), **interfakerevision** (0)
</dt> </dl>

Die für den Port zulässige Bandbreitenbegrenzung.

</dd> <dt>

**Reservierung**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **wmidataid** (1), **interfacetten** (1), **interfakerevision** (0)
</dt> </dl>

Die minimale absolute Bandbreite, die für den Port garantiert wird.

</dd> <dt>

**Weight**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: **wmidataid** (2), **interfacetten** (1), **interfakerevision** (0)
</dt> </dl>

Die minimale Bandbreite, die für den Port garantiert ist.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

