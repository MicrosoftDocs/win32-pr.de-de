---
description: Eine abstrakte Klasse, die von einer Ethernet-Switcherweiterung erfasste Port Laufzeitdaten darstellt.
ms.assetid: bc41ad1d-e7ab-4d04-96a8-26eb68ea6601
title: Msvm_EthernetPortData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortData
- Msvm_EthernetPortData.InstanceID
- Msvm_EthernetPortData.Caption
- Msvm_EthernetPortData.Description
- Msvm_EthernetPortData.ElementName
- Msvm_EthernetPortData.SystemCreationClassName
- Msvm_EthernetPortData.SystemName
- Msvm_EthernetPortData.DeviceCreationClassName
- Msvm_EthernetPortData.DeviceID
- Msvm_EthernetPortData.CreationClassName
- Msvm_EthernetPortData.Name
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 36167d4acad3c0da6b96efb9f9cc1fe58bd41a0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865536"
---
# <a name="msvm_ethernetportdata-class"></a>MSVM \_ ethernetportdata-Klasse

Eine abstrakte Klasse, die von einer Ethernet-Switcherweiterung erfasste Port Laufzeitdaten darstellt. Alle Ethernet-Port Daten Klassen müssen von dieser abstrakten Klasse abgeleitet werden.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortData : CIM_ManagedElement
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string SystemCreationClassName;
  string SystemName;
  string DeviceCreationClassName = "Msvm_EthernetSwitchPort";
  string DeviceID;
  string CreationClassName;
  string Name;
};
```

## <a name="members"></a>Member

Die **MSVM-Klasse " \_ ethernetportdata** " enthält diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM-Klasse " \_ ethernetportdata** " verfügt über diese Eigenschaften.

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

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Der Name der Unterklasse, die bei der Erstellung dieser Port Daten Instanz verwendet wird.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung des -Objekts. Diese Eigenschaft wird von [**CIM \_ managedelta**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)geerbt.

</dd> <dt>

**Geräteklassen Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**propagierter**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ LogicalDevice**](cim-logicaldevice.md).**"Kreationclassname**"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Der Name der Erstellungs Klasse des Bereichs Systems. Diese Eigenschaft ist immer auf "MSVM \_ ethernetzwitchport" festgelegt.

</dd> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**propagierter**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ LogicalDevice**](cim-logicaldevice.md).**De viceid**"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Die Geräte-ID des Ports, der diese Port Daten Instanz eingibt.

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

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Eine Zeichenfolge, die diese Port Daten Instanz innerhalb des Bereichs des Schalters und des Ports eindeutig identifiziert.

</dd> <dt>

**Systemkreationclassname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**propagierter**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM- \_ System**](cim-system.md).**"Kreationclassname**"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Der Name der Erstellungs Klasse des Bereichs Systems.

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**propagierter**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM- \_ System**](cim-system.md).**Name**"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Der Name des virtuellen Switches, der diese Port Daten Instanz eingibt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

