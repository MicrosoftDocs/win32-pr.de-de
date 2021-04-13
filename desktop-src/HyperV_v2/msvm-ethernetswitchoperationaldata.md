---
description: Stellt Switch-Betriebsparameter dar.
ms.assetid: f225d321-8f40-4e6c-b30d-8fab3f84761d
title: Msvm_EthernetSwitchOperationalData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchOperationalData
- Msvm_EthernetSwitchOperationalData.InstanceID
- Msvm_EthernetSwitchOperationalData.Caption
- Msvm_EthernetSwitchOperationalData.Description
- Msvm_EthernetSwitchOperationalData.ElementName
- Msvm_EthernetSwitchOperationalData.SystemCreationClassName
- Msvm_EthernetSwitchOperationalData.SystemName
- Msvm_EthernetSwitchOperationalData.CreationClassName
- Msvm_EthernetSwitchOperationalData.Name
- Msvm_EthernetSwitchOperationalData.CurrentSwitchingMode
- Msvm_EthernetSwitchOperationalData.SupportedSwitchingModes
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3d9aacd8380650ddaf2790aeacf4a2327b54f973
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350659"
---
# <a name="msvm_ethernetswitchoperationaldata-class"></a>MSVM \_ ethernetzwitchoperationaldata-Klasse

Stellt Switch-Betriebsparameter dar.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("1D18CDCF-209E-4172-875D-6D208A0A8375"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Modes Supported "), AMENDMENT]
class Msvm_EthernetSwitchOperationalData : Msvm_EthernetSwitchData
{
  string InstanceID;
  string Caption = "Ethernet Switch Modes Supported";
  string Description = "Represents switch operational parameters.";
  string ElementName = "Ethernet Switch Modes Supported";
  string SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string SystemName;
  string CreationClassName = " Msvm_EthernetSwitchOperationalData";
  string Name;
  uint32 CurrentSwitchingMode = 1;
  uint32 SupportedSwitchingModes[] = {1};
};
```

## <a name="members"></a>Member

Die **MSVM \_ ethernetzwitchoperationaldata** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ ethernetzwitchoperationaldata** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine kurze Beschreibung des-Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**"Name der Klassenname"**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Key**, **maxlen** (256)
</dt> </dl>

Der Name der Klasse oder Unterklasse, die bei der Erstellung dieser Instanz verwendet wird. Diese Eigenschaft wird von [**MSVM \_ ethernetzwitchdata**](msvm-ethernetswitchdata.md)geerbt.

</dd> <dt>

**Currentswitchingmode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (1), **interfacetten** (1), **interfakerevision** (0)
</dt> </dl>

Der aktuelle Wechsel Modus auf dem Switch.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="802.1Q"></span><span id="802.1q"></span>

**802.1 q** (1)


</dt> <dd></dd> <dt>

<span id="802.1Qbg"></span><span id="802.1qbg"></span><span id="802.1QBG"></span>

**802.1 qbg** (2)


</dt> <dd></dd> <dt>

<span id="802.1Qbh"></span><span id="802.1qbh"></span><span id="802.1QBH"></span>

**802.1 QBH** (3)


</dt> <dd></dd> </dl>

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

Ein Anzeige Name für das-Objekt. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

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

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Key**, **override**, **maxlen** (256)
</dt> </dl>

Der eindeutige Name der Ressource. Diese Eigenschaft wird von [**MSVM \_ ethernetzwitchdata**](msvm-ethernetswitchdata.md)geerbt.

</dd> <dt>

**Supportedswitchingmodes**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **wmidataid** (2), **interfacetten** (1), **interfakerevision** (0)
</dt> </dl>

Die vom Switch unterstützten Wechsel Modi.

</dd> <dt>

**Systemkreationclassname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Key**, **maxlen** (256)
</dt> </dl>

Der Name der Erstellungs Klasse des hostingsystems. Diese Eigenschaft wird von [**MSVM \_ ethernetzwitchdata**](msvm-ethernetswitchdata.md)geerbt.

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Key**, **maxlen** (256)
</dt> </dl>

Der Name des virtuellen Switchs, an den die zugeordnete Ressourcen Instanz gebunden ist. Diese Eigenschaft wird von [**MSVM \_ ethernetzwitchdata**](msvm-ethernetswitchdata.md)geerbt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

