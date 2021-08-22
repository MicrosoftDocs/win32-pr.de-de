---
description: Stellt Switchbetriebsparameter dar.
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
ms.openlocfilehash: 50c248d2ffc3832e72d029329c07440e87436d8718643b202304a92f1d8fea6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119531410"
---
# <a name="msvm_ethernetswitchoperationaldata-class"></a>Msvm \_ EthernetSwitchOperationalData-Klasse

Stellt Switchbetriebsparameter dar.

Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

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

Die **Msvm \_ EthernetSwitchOperationalData-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ EthernetSwitchOperationalData-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

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

Der Name der Klasse oder Unterklasse, die bei der Erstellung dieser Instanz verwendet wird. Diese Eigenschaft wird von [**Msvm \_ EthernetSwitchData**](msvm-ethernetswitchdata.md)geerbt.

</dd> <dt>

**CurrentSw standbyMode**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Der aktuelle Umschaltmodus des Schalters.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="802.1Q"></span><span id="802.1q"></span>

**802.1Q** (1)


</dt> <dd></dd> <dt>

<span id="802.1Qbg"></span><span id="802.1qbg"></span><span id="802.1QBG"></span>

**802.1Qbg** (2)


</dt> <dd></dd> <dt>

<span id="802.1Qbh"></span><span id="802.1qbh"></span><span id="802.1QBH"></span>

**802.1Qbh** (3)


</dt> <dd></dd> </dl>

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

Der eindeutige Name der Ressource. Diese Eigenschaft wird von [**Msvm \_ EthernetSwitchData**](msvm-ethernetswitchdata.md)geerbt.

</dd> <dt>

**SupportedSw standbyModes**
</dt> <dd> <dl> <dt>

Datentyp: **uint32-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Die vom Switch unterstützten Wechselmodi.

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel,** **MaxLen** (256)
</dt> </dl>

Der Name der Erstellungsklasse des Hostingsystems. Diese Eigenschaft wird von [**Msvm \_ EthernetSwitchData**](msvm-ethernetswitchdata.md)geerbt.

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel,** **MaxLen** (256)
</dt> </dl>

Der Name des virtuellen Switches, an den die zugeordnete Ressourceninstanz gebunden ist. Diese Eigenschaft wird von [**Msvm \_ EthernetSwitchData**](msvm-ethernetswitchdata.md)geerbt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

