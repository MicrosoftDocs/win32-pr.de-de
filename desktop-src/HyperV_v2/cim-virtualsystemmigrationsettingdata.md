---
description: Definiert die Einstellungen für die Migration virtueller Systeme, die von einer Instanz der CIM \_ virtualsystemmigrationservice-Klasse verwaltet werden.
ms.assetid: c28ed48b-bacc-49c8-9131-2543c0edb3fd
title: CIM_VirtualSystemMigrationSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationSettingData
- CIM_VirtualSystemMigrationSettingData.MigrationType
- CIM_VirtualSystemMigrationSettingData.Priority
- CIM_VirtualSystemMigrationSettingData.Bandwidth
- CIM_VirtualSystemMigrationSettingData.BandwidthUnit
- CIM_VirtualSystemMigrationSettingData.OtherTransportType
- CIM_VirtualSystemMigrationSettingData.TransportType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0d33479d0148bc4004fbbbda216e508c276c7ee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756271"
---
# <a name="cim_virtualsystemmigrationsettingdata-class"></a>CIM \_ virtualsystemmigrationsettingdata-Klasse

Definiert die Einstellungen für die Migration virtueller Systeme, die von einer Instanz der [**CIM \_ virtualsystemmigrationservice**](cim-virtualsystemmigrationservice.md) -Klasse verwaltet werden.

## <a name="syntax"></a>Syntax

``` syntax
[Experimental, Abstract, Version("2.20.0"), UMLPackagePath("CIM::System::Virtualization"), AMENDMENT]
class CIM_VirtualSystemMigrationSettingData : CIM_SettingData
{
  uint16 MigrationType;
  uint16 Priority;
  uint16 Bandwidth;
  string BandwidthUnit;
  string OtherTransportType;
  uint16 TransportType;
};
```

## <a name="members"></a>Member

Die **CIM- \_ virtualsystemmigrationsettingdata** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ virtualsystemmigrationsettingdata** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Bandwidth**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Messgerät**](/windows/desktop/WmiSdk/standard-qualifiers), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ virtualsystemmigrationsettingdata**.**Bandwidthunit**")
</dt> </dl>

Die Bandbreite, die einem virtuellen System Migrations Vorgang zugewiesen oder angefordert wurde. "0" ist die Standard Bandbreite für Migrations Anforderungen.

Die Eigenschaften **Bandbreite** und **Priorität** können zusammen verwendet werden. Migrationsprozesse mit den höchsten Werten für die gleiche **Priorität** haben die verfügbare Bandbreite basierend auf der angeforderten Bandbreite gemeinsam. Wenn nicht die gesamte Bandbreite von diesem Satz von Prozessen genutzt wird, nutzen Migrationsprozesse mit den nächst niedrigeren Werten mit gleicher **Priorität** die verbleibende Bandbreite gemeinsam. Wenn noch mehr Bandbreite verbleiben, werden Migrationsprozesse mit den nächst niedrigeren Werten der gleichen **Priorität** berücksichtigt.

Die in der **Bandbreiten** Eigenschaft verwendete Einheit wird durch den Wert der **bandwidthunit** -Eigenschaft angegeben.

Wenn der Wert der **bandwidthunit** -Eigenschaft "Prozent" ist, gelten die folgenden Regeln:

-   Der Wert der **Bandbreiten** Eigenschaft muss zwischen "0" und "100" liegen, wobei höhere Werte eine höhere Bandbreite angeben.
-   Der Wert "100" gibt die gesamte verfügbare Bandbreite für die Durchführung von virtuellen System Migrations Vorgängen an.
-   Werte zwischen "1" und "100" sind linear mit dem verfügbaren Bandbreiten Bereich korreliert. Beispielsweise fordert der Wert 50 die Hälfte der verfügbaren Bandbreite an.

</dd> <dt>

**Bandwidthunit**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ virtualsystemmigrationsettingdata**".**Bandbreite**"), **ispunit**
</dt> </dl>

Die Einheit, die von der **Bandbreiten** Eigenschaft verwendet wird. Der Wert dieser Eigenschaft muss ein gültiger Wert des Qualifizierers für programmgesteuerte Einheiten sein, der in Anhang C. 1 von DSP0004 v 2.4 oder höher definiert ist.

> [!Note]  
> Profile wie DMTF DSP1081 definieren, wie Clients die Gruppe von Einheiten ermitteln können, die von einer Implementierung unterstützt werden, und Bereiche und Inkremente für Werte der **Bandbreiten** Eigenschaft.

 

</dd> <dt>

**MigrationType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Typ des auszuführenden Migrations Vorgangs.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Live"></span><span id="live"></span><span id="LIVE"></span>

**Live** (2)


</dt> <dd></dd> <dt>

<span id="Resume"></span><span id="resume"></span><span id="RESUME"></span>

Fort **setzen (3** )


</dt> <dd></dd> <dt>

<span id="Restart"></span><span id="restart"></span><span id="RESTART"></span>

**Neu starten** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**Othertransporttype**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ virtualsystemmigrationsettingdata**".**TransportType**")
</dt> </dl>

Der Transporttyp, der angewendet werden soll, wenn der Wert von **TransportType** "1" (sonstige) ist.

</dd> <dt>

**Priority**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die relative Migrations Wichtigkeit, die von der Implementierung der virtuellen System Migration verwendet werden kann, um mehrere ausstehende Migrations Anforderungen zu sortieren oder zuzuweisen. Je niedriger der Wert, desto höher ist die Priorität. "0" ist die Standard Bandbreite für Migrations Anforderungen.

</dd> <dt>

**TransportType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ virtualsystemmigrationsettingdata**".**Othertransporttype**")
</dt> </dl>

Der Transporttyp, der auf einen virtuellen System Migrations Vorgang angewendet werden soll.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="SSH"></span><span id="ssh"></span>

**SSH** (2)


</dt> <dd></dd> <dt>

<span id="TLS"></span><span id="tls"></span>

**TLS** (3)


</dt> <dd></dd> <dt>

<span id="TLS_Strict"></span><span id="tls_strict"></span><span id="TLS_STRICT"></span>

**TLS Strict** (4)


</dt> <dd></dd> <dt>

<span id="TCP"></span><span id="tcp"></span>

**TCP** (5)


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

**IPC** (6)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reserviert** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Anbieter reserviert** (32768..)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ SettingData**](cim-settingdata.md)
</dt> </dl>

 

