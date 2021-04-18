---
description: Beschreibt die Funktionen und die Verwaltung von Medien, die Daten speichern und den Abruf der Daten ermöglichen. Diese Superklasse wird zur Darstellung von Software-und Hardware-RAID-Komponenten oder einem logischen Bereich physischer Datenträger verwendet.
ms.assetid: 29d105fb-8c34-4824-8679-883aef02a0c9
title: CIM_StorageExtent-Klasse (Hyper-V-Verwaltung)
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
ms.openlocfilehash: a3dc1b58dd97582e229497e754d10c3f307eab76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368754"
---
# <a name="cim_storageextent-class-hyper-v-management"></a>CIM_StorageExtent-Klasse (Hyper-V-Verwaltung)

Beschreibt die Funktionen und die Verwaltung von Medien, die Daten speichern und den Abruf der Daten ermöglichen. Diese Superklasse wird zur Darstellung von Software-und Hardware-RAID-Komponenten oder einem logischen Bereich physischer Datenträger verwendet.

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

Die **CIM \_ storageblock** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ storageblock** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**zugreifen**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Beschreibung der Lese-/Schreibunterstützung des Mediums.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

**Lesbar** (1)


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

**Beschreibbar** (2)


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

**Lese-/Schreibzugriff unterstützt** (3)


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

**Einmal schreiben** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**BlockSize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Host Speicher \| 001,4 "," MIB. IETF \| Host-Resources-MIB. hrstorageallocationunits "," MIF. DMTF- \| Speichergeräte \| 001,5 ")
</dt> </dl>

Die Größe (in Bytes) der Blöcke, die den Speicherblock bilden. Wenn Variablen Blockgrößen verwendet werden, sollte diese Eigenschaft die maximale Blockgröße angeben. Wenn die Blockgröße unbekannt ist oder ein Block Konzept nicht gültig ist (z. b. für **CIM- \_ aggregatblock**, [**CIM- \_ Speicher**](cim-memory.md) oder [**CIM \_ LogicalDisk**](cim-logicaldisk.md)), sollte diese Eigenschaft auf "1" (unbekannt) festgelegt werden.

</dd> <dt>

**Consumableblocks**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die maximale Anzahl von Blöcken, die zur Verwendung bei der Schichten- **CIM- \_ Speicher** Zuweisung mithilfe der [**CIM- \_ BasedOn**](cim-basedon.md) -Klassen Zuordnung verfügbar sind. Diese Eigenschaft hat nur Bedeutung, wenn in der **Vorgänger** Eigenschaft eines **CIM- \_ BasedOn** -Objekts auf den Speicherblock verwiesen wird.

</dd> <dt>

**Dataorganization**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Typ der von den Medien verwendeten Datenorganisation.

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

**Variablen Block** (3)


</dt> <dd></dd> <dt>

<span id="Count_Key_Data"></span><span id="count_key_data"></span><span id="COUNT_KEY_DATA"></span>

**Schlüsseldaten zählen** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**Dataredundancy**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageSet**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting)".**Dataredundancygoal**","**CIM \_ StorageSet**.**Dataredundancymax**","**CIM \_ StorageSet**.**Dataredundancymin**")
</dt> </dl>

Die Anzahl der kompletten Kopien von Daten, die zurzeit verwaltet werden.

</dd> <dt>

**Delta Service**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Prozentsatz"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (100), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM- \_ StorageSet**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting).**Delta-eservationgoal**","**CIM \_ StorageSet**.**Delta Service** Type ","**CIM \_ StorageSet**.**Delta Service** Type ")
</dt> </dl>

Der aktuelle Wert für die Delta Reservierung. Dies ist ein Prozentsatz, der den Speicherplatz angibt, der in einem Replikat reserviert werden soll, um Änderungen zwischenzuspeichern.

</dd> <dt>

**Errormethodmethodologie**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Typ der Fehlererkennung und-Korrektur, der vom Speicherblock unterstützt wird.

</dd> <dt>

**Extentstatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Weitere Statusinformationen.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (0)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (1)


</dt> <dd></dd> <dt>

<span id="None_Not_Applicable"></span><span id="none_not_applicable"></span><span id="NONE_NOT_APPLICABLE"></span>

**Keine/nicht zutreffend** (2)


</dt> <dd></dd> <dt>

<span id="Broken"></span><span id="broken"></span><span id="BROKEN"></span>

**Beschädigt** (3)


</dt> <dd></dd> <dt>

<span id="Data_Lost"></span><span id="data_lost"></span><span id="DATA_LOST"></span>

**Verlust von Daten** (4)


</dt> <dd></dd> <dt>

<span id="Dynamic_Reconfig"></span><span id="dynamic_reconfig"></span><span id="DYNAMIC_RECONFIG"></span>

**Dynamische Neukonfiguration** (5)


</dt> <dd></dd> <dt>

<span id="Exposed"></span><span id="exposed"></span><span id="EXPOSED"></span>

Verfügbar **gemacht (6** )


</dt> <dd></dd> <dt>

<span id="Fractionally_Exposed"></span><span id="fractionally_exposed"></span><span id="FRACTIONALLY_EXPOSED"></span>

In **Bruch Komma Sicht** verfügbar (7)


</dt> <dd></dd> <dt>

<span id="Partially_Exposed"></span><span id="partially_exposed"></span><span id="PARTIALLY_EXPOSED"></span>

**Teilweise** verfügbar (8)


</dt> <dd></dd> <dt>

<span id="Protection_Disabled"></span><span id="protection_disabled"></span><span id="PROTECTION_DISABLED"></span>

**Schutz deaktiviert** (9)


</dt> <dd></dd> <dt>

<span id="Readying"></span><span id="readying"></span><span id="READYING"></span>

**Lesen** (10)


</dt> <dd></dd> <dt>

<span id="Rebuild"></span><span id="rebuild"></span><span id="REBUILD"></span>

**Neu erstellen** (11)


</dt> <dd></dd> <dt>

<span id="Recalculate"></span><span id="recalculate"></span><span id="RECALCULATE"></span>

**Neuberechnen** (12)


</dt> <dd></dd> <dt>

<span id="Spare_in_Use"></span><span id="spare_in_use"></span><span id="SPARE_IN_USE"></span>

**Ersatz in Gebrauch** (13)


</dt> <dd></dd> <dt>

<span id="Verify_In_Progress"></span><span id="verify_in_progress"></span><span id="VERIFY_IN_PROGRESS"></span>

**Überprüfen in** Bearbeitung (14)


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

**DMTF reserviert** (18.. 32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Anbieter reserviert** (32768.65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**Isbasedonunderlyingredundancy**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**true** , wenn die zugrunde liegenden Speicherblöcke Mitglieder einer [**CIM \_ storageredundancygroup**](/windows/desktop/CIMWin32Prov/cim-storageredundancygroup)sind; andernfalls **false**.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SPC. Begints-T10 \| VPD 83, Association 0 \| Identifier "), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ storageblock**".**NameFormat**","**CIM \_ storageblock**.**Namenamespace**")
</dt> </dl>

Ein eindeutiger Bezeichner für den Speicherblock. Die Eigenschaft **NameFormat** gibt das Benennungs Format an, das in der Eigenschaft **Name** verwendet werden soll.

</dd> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ storageblock**".**Name**","**CIM \_ storageblock**.**Namenamespace**","**CIM \_ storageblock**.**Othernameformat**")
</dt> </dl>

Das Benennungs Format für die **Name** -Eigenschaft.

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

**Snvm** (7)


</dt> <dd></dd> <dt>

<span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>

**NoDebug** (8)


</dt> <dd></dd> <dt>

<span id="NAA"></span><span id="naa"></span>

**Naa** (9)


</dt> <dd></dd> <dt>

<span id="EUI64"></span><span id="eui64"></span>

**EUI64** (10)


</dt> <dd></dd> <dt>

<span id="T10VID"></span><span id="t10vid"></span>

**T10VID** (11)


</dt> <dd></dd> <dt>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>

**Betriebssystem-Geräte Name** (12)


</dt> <dd></dd> </dl>

</dd> <dt>

**Namenamespace**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SPC. Begints-T10 \| VPD 83, Association 0 \| Identifier "), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ storageblock**".**Name**","**CIM \_ storageblock**.**Othernamenamespace**","**CIM \_ storageblock**.**NameFormat**")
</dt> </dl>

Der Namespace der Name-Eigenschaft.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


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

**NoDebug** (6)


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

**Snvm** (7)


</dt> <dd></dd> <dt>

<span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>

**Betriebssystem-Geräte Namespace** (8)


</dt> <dd></dd> </dl>

</dd> <dt>

**Nosinglepoinpoffailure**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageSet**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting)".**Nosinglepoinpoffailure**")
</dt> </dl>

**true** , wenn es keine einzelnen Fehlerpunkte gibt. andernfalls **false**.

</dd> <dt>

**NumberOfBlocks**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Host Speicher \| 001,5 "," MIB. IETF \| Host-Resources-MIB. hrstoragesize ")
</dt> </dl>

Die Gesamtanzahl logisch zusammenhängender Blöcke, die den Speicherblock bilden. Die Gesamtgröße des Speicherbereichs wird durch Multiplizieren von **BLOCKSIZE** nach **Anzahl Blöcken** berechnet. Wenn **Block Size** den Wert 1 hat, entspricht diese Eigenschaft der Gesamtgröße des Speicherbereichs.

</dd> <dt>

**Othernameformat**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ storageblock**".**NameFormat**")
</dt> </dl>

Das Format der **Name** -Eigenschaft, wenn die **NameFormat** -Eigenschaft auf "1" (sonstige) festgelegt ist.

</dd> <dt>

**Othernamenamespace**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ storageblock**".**Namenamespace**")
</dt> </dl>

Eine Beschreibung des Namespace der **Name** -Eigenschaft, wenn die **namenamespace** -Eigenschaft auf "1" (sonstige) festgelegt ist.

</dd> <dt>

**Packageredundancy**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ StorageSet**](/previous-versions/windows/desktop/iscsitarg/cim-storagesetting)".**Packageredundancygoal**","**CIM \_ StorageSet**.**Packageredundancymax**","**CIM \_ StorageSet**.**Packageredundancymin**")
</dt> </dl>

Die aktuelle Anzahl von physischen Paketen, die ohne Datenverlust ausfallen können. In einer Speicher Domäne kann dies z. b. die Anzahl der Datenträger Spindeln sein.

</dd> <dt>

**Ursprünglich**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**true** , wenn der Speicherblock ursprünglicher ist. andernfalls **false**.

</dd> <dt>

**Zweck**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. hrstoragedescr ")
</dt> </dl>

Eine Beschreibung der Medien Verwendung.

</dd> <dt>

**SequentialAccess**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**true** , wenn auf den Speicher sequenziell von einem [**CIM \_ mediaaccessdevice**](cim-mediaaccessdevice.md) -Objekt zugegriffen wird, andernfalls **false**.

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

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> </dl>

 

