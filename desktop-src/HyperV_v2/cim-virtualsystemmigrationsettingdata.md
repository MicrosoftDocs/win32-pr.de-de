---
description: Definiert die Einstellungen für die Migration virtueller Systeme, die von einer Instanz der CIM \_ VirtualSystemMigrationService-Klasse verwaltet werden.
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
ms.openlocfilehash: 24a48877a4195d17398457912314186d0220ace8016a4c9cc3edd3e06c378ee4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950669"
---
# <a name="cim_virtualsystemmigrationsettingdata-class"></a>CIM \_ VirtualSystemMigrationSettingData-Klasse

Definiert die Einstellungen für die Migration virtueller Systeme, die von einer Instanz der [**CIM \_ VirtualSystemMigrationService-Klasse verwaltet**](cim-virtualsystemmigrationservice.md) werden.

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

Die **CIM \_ VirtualSystemMigrationSettingData-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ VirtualSystemMigrationSettingData-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Bandbreite**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Messgerät**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VirtualSystemMigrationSettingData**.**BandwidthUnit**")
</dt> </dl>

Die Bandbreite, die einem Migrationsvorgang des virtuellen Systems zugewiesen oder angefordert wurde. "0" ist die Standardbandbreite für Migrationsanforderungen.

Die **Eigenschaften Bandbreite** und **Priorität** können in Verbindung verwendet werden. Migrationsprozesse mit den höchsten **prioritätsbasierten** Werten teilen sich die verfügbare Bandbreite basierend auf der angeforderten Bandbreite. Wenn nicht die ganze Bandbreite von dieser Gruppe von Prozessen  verbraucht wird, teilen sich Migrationsprozesse mit den nächsten niedrigeren Prioritätswerten die verbleibende Bandbreite. Wenn mehr Bandbreite verbleibt, werden Migrationsprozesse mit den nächsten niedrigeren **Prioritätswerten** berücksichtigt.

Die in der **Bandwidth-Eigenschaft** verwendete Einheit wird durch den Wert der **BandwidthUnit-Eigenschaft** angegeben.

Wenn der Wert der **BandwidthUnit-Eigenschaft** "percent" ist, gelten die folgenden Regeln:

-   Der Wert der **Bandwidth-Eigenschaft** muss zwischen "0" und "100" liegen, und höhere Werte geben eine höhere Bandbreite an.
-   Der Wert "100" gibt die verfügbare Bandbreite für die Durchführung von Migrationsvorgängen für virtuelle Systeme an.
-   Werte zwischen "1" und "100" korrelieren linear mit dem verfügbaren Bandbreitenbereich. Beispielsweise fordert ein Wert von 50 die Hälfte der verfügbaren Bandbreite an.

</dd> <dt>

**BandwidthUnit**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VirtualSystemMigrationSettingData**.**Bandbreite**"), **IsPUnit**
</dt> </dl>

Die von der **Bandwidth-Eigenschaft verwendete** Einheit. Der Wert dieser Eigenschaft muss ein rechtlicher Wert des in Anhang C.1 von DSP0004 V2.4 oder höher definierten Qualifizierers Programmatic Units sein.

> [!Note]  
> Profile wie DMTF DSP1081 definieren, wie Clients den Satz von Einheiten, die von einer Implementierung unterstützt werden, sowie Bereiche und Inkremente für Werte der **Bandwidth-Eigenschaft entdecken** können.

 

</dd> <dt>

**MigrationType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Typ des durchzuführenden Migrationsvorgang.

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

**Fortsetzen** (3)


</dt> <dd></dd> <dt>

<span id="Restart"></span><span id="restart"></span><span id="RESTART"></span>

**Neustart** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**OtherTransportType**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VirtualSystemMigrationSettingData**.**TransportType**")
</dt> </dl>

Der Transporttyp, der angewendet werden soll, wenn der Wert von **TransportType** "1" (sonstige) ist.

</dd> <dt>

**Priority**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die relative Migrationsanforderung, die die Implementierung der Migration des virtuellen Systems verwenden kann, um mehrere ausstehende Migrationsanforderungen zu ordnen oder zu bevorzugen. Je niedriger der Wert, desto höher die Priorität. "0" ist die Standardbandbreite für Migrationsanforderungen.

</dd> <dt>

**TransportType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VirtualSystemMigrationSettingData**.**OtherTransportType**")
</dt> </dl>

Der Transporttyp, der auf einen Migrationsvorgang des virtuellen Systems angewendet werden soll.

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

**DMTF Reserved** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Anbieter reserviert** (32768.)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> </dl>

 

