---
description: Beschreibt die Funktionen und die Verwaltung von Medien, die Daten speichern und das Abrufen der Daten ermöglichen. Diese Superklasse wird verwendet, um Software- und Hardware-RAID-Komponenten oder einen unformatten logischen Umfang physischer Medien zu darstellen.
ms.assetid: 29d105fb-8c34-4824-8679-883aef02a0c9
title: CIM_StorageExtent -Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageExtent
- CIM_StorageExtent.DataOrganization
- CIM_StorageExtent.Purpose
- CIM_StorageExtent.Access
- CIM_StorageExtent.ErrorMethodology
- CIM_StorageExtent.BlockSize
- CIM_StorageExtent.NumberOfBlocks
- CIM_StorageExtent.ConsumableBlocks
- CIM_StorageExtent.IsBasedOnUnderlyingRedundancy
- CIM_StorageExtent.SequentialAccess
- CIM_StorageExtent.ExtentStatus
- CIM_StorageExtent.NoSinglePointOfFailure
- CIM_StorageExtent.DataRedundancy
- CIM_StorageExtent.PackageRedundancy
- CIM_StorageExtent.DeltaReservation
- CIM_StorageExtent.Primordial
- CIM_StorageExtent.Name
- CIM_StorageExtent.NameFormat
- CIM_StorageExtent.NameNamespace
- CIM_StorageExtent.OtherNameNamespace
- CIM_StorageExtent.OtherNameFormat
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2ce3126cf208032e4d43e9ce1866e1cd0ab42c17930684c98d4ad351de88713b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118647368"
---
# <a name="cim_storageextent-class-hyper-v-management"></a>CIM_StorageExtent -Klasse (Hyper-V-Verwaltung)

Beschreibt die Funktionen und die Verwaltung von Medien, die Daten speichern und das Abrufen der Daten ermöglichen. Diese Superklasse wird verwendet, um Software- und Hardware-RAID-Komponenten oder einen unformatten logischen Umfang physischer Medien zu darstellen.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.13.0"), UMLPackagePath("CIM::Core::StorageExtent"), AMENDMENT]
class CIM_StorageExtent : CIM_LogicalDevice
{
  uint16  DataOrganization;
  string  Purpose;
  uint16  Access;
  string  ErrorMethodology;
  uint64  BlockSize;
  uint64  NumberOfBlocks;
  uint64  ConsumableBlocks;
  boolean IsBasedOnUnderlyingRedundancy;
  boolean SequentialAccess;
  uint16  ExtentStatus[];
  boolean NoSinglePointOfFailure;
  uint16  DataRedundancy;
  uint16  PackageRedundancy;
  uint8   DeltaReservation;
  boolean Primordial = FALSE;
  string  Name;
  uint16  NameFormat;
  uint16  NameNamespace;
  string  OtherNameNamespace;
  string  OtherNameFormat;
};
```

## <a name="members"></a>Member

Die **CIM \_ StorageExtent-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ StorageExtent-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**zugreifen**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung der Lese-/Schreibunterstützung der Medien.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

**Lesbar** (1)


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

**Schreibbar** (2)


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

**Lese-/Schreibzugriff unterstützt** (3)


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

**Einmal schreiben** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**Blöcke**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Host Storage \| 001.4", "MIB. IETF \| HOST-RESOURCES-MIB.hrStorageAllocationUnits", "MIF. DMTF \| Storage Devices \| 001.5")
</dt> </dl>

Die Größe der Blöcke in Bytes, die den Speicherblock bilden. Wenn variablen Blockgrößen verwendet werden, sollte diese Eigenschaft die maximale Blockgröße angeben. Wenn die Blockgröße unbekannt ist oder ein Blockkonzept ungültig ist (z. B. für **CIM \_ AggregateExtent,** [**CIM \_ Memory**](cim-memory.md) oder [**CIM \_ LogicalDisk),**](cim-logicaldisk.md)sollte diese Eigenschaft auf "1" (unknow) festgelegt werden.

</dd> <dt>

**ConsumableBlocks**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die maximale Anzahl von Blöcken, die bei der Überlagerung von **CIM \_ StorageExtent mithilfe** der [**CIM \_ BasedOn-Klassenabsicht verwendet**](cim-basedon.md) werden können. Diese Eigenschaft hat nur dann eine Bedeutung, wenn in der **Eigenschaft Antecedent** in einem **CIM \_ BasedOn-Objekt auf** den Speicher extent verwiesen wird.

</dd> <dt>

**DataOrganization**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Typ der datenorganisation, die von den Medien verwendet wird.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (0)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (1)


</dt> <dd></dd> <dt>

<span id="Fixed_Block"></span><span id="fixed_block"></span><span id="FIXED_BLOCK"></span>

**Fester Block** (2)


</dt> <dd></dd> <dt>

<span id="Variable_Block"></span><span id="variable_block"></span><span id="VARIABLE_BLOCK"></span>

**Variablenblock** (3)


</dt> <dd></dd> <dt>

<span id="Count_Key_Data"></span><span id="count_key_data"></span><span id="COUNT_KEY_DATA"></span>

**Count Key Data** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**DataRedundancy**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**DataRedundancyGoal**", "**CIM \_ StorageSetting**.**DataRedundancyMax**", "**CIM \_ StorageSetting**.**DataRedundancyMin**")
</dt> </dl>

Die Anzahl der vollständigen Kopien von Daten, die derzeit verwaltet werden.

</dd> <dt>

**DeltaReservation**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Prozentsatz"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (100), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**DeltaReservationGoal**", "**CIM \_ StorageSetting**.**DeltaReservationMax**", "**CIM \_ StorageSetting**.**DeltaReservationMin**")
</dt> </dl>

Der aktuelle Wert für die Deltareservierung. Dies ist ein Prozentsatz, der den Speicherplatz angibt, der in einem Replikat für das Zwischenspeichern von Änderungen reserviert werden soll.

</dd> <dt>

**ErrorMethodology**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Typ der Fehlererkennung und -korrektur, die vom Speicherspeicher extent unterstützt wird.

</dd> <dt>

**ExtentStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zusätzliche Statusinformationen.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (0)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (1)


</dt> <dd></dd> <dt>

<span id="None_Not_Applicable"></span><span id="none_not_applicable"></span><span id="NONE_NOT_APPLICABLE"></span>

**Keine/Nicht zutreffend** (2)


</dt> <dd></dd> <dt>

<span id="Broken"></span><span id="broken"></span><span id="BROKEN"></span>

**Unterbrochen** (3)


</dt> <dd></dd> <dt>

<span id="Data_Lost"></span><span id="data_lost"></span><span id="DATA_LOST"></span>

**Verlorene Daten** (4)


</dt> <dd></dd> <dt>

<span id="Dynamic_Reconfig"></span><span id="dynamic_reconfig"></span><span id="DYNAMIC_RECONFIG"></span>

**Dynamische Neukonfiguration** (5)


</dt> <dd></dd> <dt>

<span id="Exposed"></span><span id="exposed"></span><span id="EXPOSED"></span>

**Verfügbar** gemacht (6)


</dt> <dd></dd> <dt>

<span id="Fractionally_Exposed"></span><span id="fractionally_exposed"></span><span id="FRACTIONALLY_EXPOSED"></span>

**Fractionally Exposed** (7)


</dt> <dd></dd> <dt>

<span id="Partially_Exposed"></span><span id="partially_exposed"></span><span id="PARTIALLY_EXPOSED"></span>

**Teilweise verfügbar** gemacht (8)


</dt> <dd></dd> <dt>

<span id="Protection_Disabled"></span><span id="protection_disabled"></span><span id="PROTECTION_DISABLED"></span>

**Schutz deaktiviert** (9)


</dt> <dd></dd> <dt>

<span id="Readying"></span><span id="readying"></span><span id="READYING"></span>

**Readying** (10)


</dt> <dd></dd> <dt>

<span id="Rebuild"></span><span id="rebuild"></span><span id="REBUILD"></span>

**Neuerstellen** (11)


</dt> <dd></dd> <dt>

<span id="Recalculate"></span><span id="recalculate"></span><span id="RECALCULATE"></span>

**Neu berechnen** (12)


</dt> <dd></dd> <dt>

<span id="Spare_in_Use"></span><span id="spare_in_use"></span><span id="SPARE_IN_USE"></span>

**Ersatz in Verwendung** (13)


</dt> <dd></dd> <dt>

<span id="Verify_In_Progress"></span><span id="verify_in_progress"></span><span id="VERIFY_IN_PROGRESS"></span>

**Überprüfen in Bearbeitung** (14)


</dt> <dd></dd> <dt>

<span id="In-Band_Access_Granted"></span><span id="in-band_access_granted"></span><span id="IN-BAND_ACCESS_GRANTED"></span>

**In-Band-Zugriff gewährt** (15)


</dt> <dd></dd> <dt>

<span id="Imported"></span><span id="imported"></span><span id="IMPORTED"></span>

**Importiert** (16)


</dt> <dd></dd> <dt>

<span id="Exported"></span><span id="exported"></span><span id="EXPORTED"></span>

**Exportiert** (17)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF Reserved** (18..32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Anbieter reserviert** (32768..65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**IsBasedOnUnderlyingRedundancy**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**TRUE,** wenn die zugrunde liegenden Speicherwertewerte Mitglieder einer [**CIM \_ StorageRedundancyGroup**](/windows/desktop/CIMWin32Prov/cim-storageredundancygroup)sind, andernfalls **FALSE.**

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SPC. INCITS-T10 \| VPD 83, Association 0 \| Identifier"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ StorageExtent**.**NameFormat**", "**CIM \_ StorageExtent**.**NameNamespace**")
</dt> </dl>

Ein eindeutiger Bezeichner für den Speicherbezeichner. Die **NameFormat-Eigenschaft** gibt das Benennungsformat an, das in der **Name-Eigenschaft verwendet werden** soll.

</dd> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ StorageExtent**.**Name**", "**CIM \_ StorageExtent**.**NameNamespace**", "**CIM \_ StorageExtent**.**OtherNameFormat**")
</dt> </dl>

Das Benennungsformat für die **Name-Eigenschaft.**

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="VPD83NAA6"></span><span id="vpd83naa6"></span>

**VPD83NAA6** (2)


</dt> <dd></dd> <dt>

<span id="VPD83NAA5"></span><span id="vpd83naa5"></span>

**VPD83NAA5** (3)


</dt> <dd></dd> <dt>

<span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>

**VPD83Type2** (4)


</dt> <dd></dd> <dt>

<span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>

**VPD83Type1** (5)


</dt> <dd></dd> <dt>

<span id="VPD83Type0"></span><span id="vpd83type0"></span><span id="VPD83TYPE0"></span>

**VPD83Type0** (6)


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

**SNVM** (7)


</dt> <dd></dd> <dt>

<span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>

**NodeWWN** (8)


</dt> <dd></dd> <dt>

<span id="NAA"></span><span id="naa"></span>

**NAA** (9)


</dt> <dd></dd> <dt>

<span id="EUI64"></span><span id="eui64"></span>

**EUI64** (10)


</dt> <dd></dd> <dt>

<span id="T10VID"></span><span id="t10vid"></span>

**T10VID** (11)


</dt> <dd></dd> <dt>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>

**Name des Betriebssystemgeräts** (12)


</dt> <dd></dd> </dl>

</dd> <dt>

**NameNamespace**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SPC. INCITS-T10 \| VPD 83, Association 0 \| Identifier"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ StorageExtent**.**Name**", "**CIM \_ StorageExtent**.**OtherNameNamespace**", "**CIM \_ StorageExtent**.**NameFormat**")
</dt> </dl>

Der Namespace der Name-Eigenschaft.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Andere** (1)


</dt> <dd></dd> <dt>

<span id="VPD83Type3"></span><span id="vpd83type3"></span><span id="VPD83TYPE3"></span>

**VPD83Type3** (2)


</dt> <dd></dd> <dt>

<span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>

**VPD83Type2** (3)


</dt> <dd></dd> <dt>

<span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>

**VPD83Type1** (4)


</dt> <dd></dd> <dt>

<span id="VPD80"></span><span id="vpd80"></span>

**VPD80** (5)


</dt> <dd></dd> <dt>

<span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>

**NodeWWN** (6)


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

**SNVM** (7)


</dt> <dd></dd> <dt>

<span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>

**Betriebssystemgerätenamespace** (8)


</dt> <dd></dd> </dl>

</dd> <dt>

**NoSinglePointOfFailure**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**NoSinglePointOfFailure**")
</dt> </dl>

**TRUE,** wenn keine einzelnen Fehlerpunkte vorhanden sind; andernfalls **FALSE.**

</dd> <dt>

**NumberOfBlocks**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|DMTF-Host Storage \| 001.5", "MIB. IETF \| HOST-RESOURCES-MIB.hrStorageSize")
</dt> </dl>

Die Gesamtanzahl logisch zusammenhängender Blöcke, die den Speicherblock bilden. Die Gesamtgröße des Speicherblocks wird berechnet, indem **BlockSize** mit **NumberOfBlocks** multipliziert wird. Wenn **BlockSize** "1" ist, ist diese Eigenschaft die Gesamtgröße des Speicherblocks.

</dd> <dt>

**OtherNameFormat**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ StorageExtent**.**NameFormat**")
</dt> </dl>

Das Format der **Name-Eigenschaft,** wenn die **NameFormat-Eigenschaft** auf "1" (Other) festgelegt ist.

</dd> <dt>

**OtherNameNamespace**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ StorageExtent**.**NameNamespace**")
</dt> </dl>

Eine Beschreibung des Namespace der **Name-Eigenschaft,** wenn die **NameNamespace-Eigenschaft** auf "1" (Sonstige) festgelegt ist.

</dd> <dt>

**PackageRedundancy**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageSetting**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**PackageRedundancyGoal**", "**CIM \_ StorageSetting**.**PackageRedundancyMax**", "**CIM \_ StorageSetting**.**PackageRedundancyMin**")
</dt> </dl>

Die aktuelle Anzahl physischer Pakete, die ohne Datenverlust fehlschlagen können. In einer Speicherdomäne kann dies beispielsweise die Anzahl der Datenträgerspindeln sein.

</dd> <dt>

**Ursprünglich**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**TRUE,** wenn der Speicherumfang unerzwendlich ist; andernfalls **FALSE.**

</dd> <dt>

**Zweck**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| HOST-RESOURCES-MIB.hrStorageDescr")
</dt> </dl>

Eine Beschreibung der Mediennutzung.

</dd> <dt>

**SequentialAccess**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**TRUE,** wenn ein CIM [**\_ MediaAccessDevice-Objekt**](cim-mediaaccessdevice.md) sequenziell auf den Speicher zugreift, andernfalls **FALSE.**

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> </dl>

 

