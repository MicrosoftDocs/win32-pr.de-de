---
description: Stellt Einstellungen für die Zuordnung des virtuellen Speichers dar.
ms.assetid: 128fd3e9-8759-4b2f-a881-d34e89c539ac
title: CIM_StorageAllocationSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageAllocationSettingData
- CIM_StorageAllocationSettingData.VirtualResourceBlockSize
- CIM_StorageAllocationSettingData.VirtualQuantity
- CIM_StorageAllocationSettingData.VirtualQuantityUnits
- CIM_StorageAllocationSettingData.Access
- CIM_StorageAllocationSettingData.HostResourceBlockSize
- CIM_StorageAllocationSettingData.Reservation
- CIM_StorageAllocationSettingData.Limit
- CIM_StorageAllocationSettingData.HostExtentStartingAddress
- CIM_StorageAllocationSettingData.HostExtentName
- CIM_StorageAllocationSettingData.HostExtentNameFormat
- CIM_StorageAllocationSettingData.OtherHostExtentNameFormat
- CIM_StorageAllocationSettingData.HostExtentNameNamespace
- CIM_StorageAllocationSettingData.OtherHostExtentNameNamespace
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e66322f20987e2d1f99042430f0f57cdc2e399d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756619"
---
# <a name="cim_storageallocationsettingdata-class"></a>CIM- \_ Klasse "storagezugegenssettingdata"

Stellt Einstellungen für die Zuordnung des virtuellen Speichers dar.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_StorageAllocationSettingData : CIM_ResourceAllocationSettingData
{
  uint64 VirtualResourceBlockSize;
  uint64 VirtualQuantity;
  string VirtualQuantityUnits = "count(fixed size block)";
  uint16 Access;
  uint64 HostResourceBlockSize;
  uint64 Reservation;
  uint64 Limit;
  uint64 HostExtentStartingAddress;
  string HostExtentName;
  uint16 HostExtentNameFormat;
  string OtherHostExtentNameFormat;
  uint16 HostExtentNameNamespace;
  string OtherHostExtentNameNamespace;
};
```

## <a name="members"></a>Member

Die **CIM \_ storagezugecationsettingdata** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ storagezugecationsettingdata** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**zugreifen**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ storageblock**](cim-storageextent.md)".**Access**")
</dt> </dl>

Die Lese-/Schreibunterstützung der Speicher Belegung.

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

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reserviert** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**Hostextentname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ storagezugecationsettingdata**".**Hostextentnameformat**","**CIM \_ storagezuweisung-dateinsettingdata**.**Hostextentnamenamespace**","[**CIM \_ storageblock**](cim-storageextent.md).**Name**")
</dt> </dl>

Ein eindeutiger Bezeichner des Host Speicher Umfangs.

</dd> <dt>

**Hostextentnameformat**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ storagezugecationsettingdata**".**Hostextentname**","**CIM \_ storagezugecationsettingdata**.**Otherhostextentnameformat**","[**CIM \_ storageblock**](cim-storageextent.md).**NameFormat**")
</dt> </dl>

Das Format des **hostextentname** -Eigenschafts Werts.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

<span id="SNVM"></span><span id="snvm"></span>**Snvm** (7)


</dt> <dd>

Snvm (Serial Number/Vendor/Model) ist 3 Zeichen folgen, die den Herstellernamen, den Produktnamen innerhalb des Namespaces des Anbieters und die Seriennummer im Modell Namespace darstellen. Als Trennzeichen für Zeichen folgen wird "+" verwendet. Leerzeichen können eingeschlossen werden und sind von Bedeutung. Die Seriennummer ist die Textdarstellung der Seriennummer in hexadezimalen Großbuchstaben. Dies stellt den Hersteller und die Modell-ID aus den SCSI-Abfrage Daten dar. das Feld "Vendor" muss 8 Zeichen breit sein, und das Feld "Product" muss 16 Zeichen breit sein. Beispiel:

"Acme \_ \_ \_ \_ + Super Disk \_ \_ \_ \_ \_ \_ + 124437458" ( \_ ist ein Leerzeichen)

</dd> <dt>

<span id="NAA"></span><span id="naa"></span>

<span id="NAA"></span><span id="naa"></span>**Naa** (9)


</dt> <dd>

9 = Naa als generisches Format. Siehe

https://standards.ieee.org/regauth/oui/tutorials/fibrecomp\_id.html. Formatiert als 16 oder 32 nicht getrennte hexadezimal Zeichen (2 pro binäres Byte).

Beispiel: "21000020372d3c73"

</dd> <dt>

<span id="EUI64"></span><span id="eui64"></span>

<span id="EUI64"></span><span id="eui64"></span>**EUI64** (10)


</dt> <dd>

EUI als generisches Format (EUI64) finden Sie unter

https://standards.ieee.org/content/dam/ieee-standards/standards/web/documents/tutorials/eui.pdf.

</dd> <dt>

<span id="T10VID"></span><span id="t10vid"></span>

<span id="T10VID"></span><span id="t10vid"></span>**T10VID** (11)


</dt> <dd>

T10-Hersteller Bezeichnerformat, wie von der SCSI-Abfrage VPD-Seite 83, Bezeichnertyp 1 zurückgegeben Weitere Informationen finden Sie unter T10 SPC-3-Spezifikation. Dies ist die 8-Byte-ASCII-Anbieter-ID aus der T10-Registrierung, gefolgt von einem herstellerspezifischen ASCII-Bezeichner. Leerzeichen sind zulässig. Bei nicht-SCSI-Volumes ist "snvm" möglicherweise die geeignetste Wahl.

</dd> <dt>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>**Betriebssystem-Geräte Name** (12)


</dt> <dd>

Betriebssystem-Geräte Name (für logicaldisks). Ausführliche Informationen finden Sie unter LogicalDisk Name Description.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**Hostextentnamenamespace**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ storagezugecationsettingdata**".**Hostextentname**","**CIM \_ storagezugecationsettingdata**.**Otherhostextentnamenamespace**","**CIM \_ storagezugecationsettingdata**.**Hostextentnameformat**","[**CIM \_ storageblock**](cim-storageextent.md).**Namespace**")
</dt> </dl>

Das Benennungs Format für die **Name** -Eigenschaft.

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


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reserviert** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**Hostextentstartingaddress**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ storagezugecationsettingdata**".**"Hastresourceblocksize**", "[**CIM \_ BasedOn**](cim-basedon.md)".**StartingAddress**")
</dt> </dl>

Die Startadresse des Host Speicherblocks. Ein NULL-Val; ue gibt an, dass es keine direkte Zuordnung zwischen dem virtuellen Speicherblock und dem Host Speicherblock gibt.

</dd> <dt>

**"Hastresourceblocksize"**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ storageblock**](cim-storageextent.md)".**BlockSize**"), **Punit** (" Byte ")
</dt> </dl>

Die Größe (in Bytes) der Blöcke, die auf dem Host für die Speicher Belegung zugeordnet werden. Wenn die Blockgröße variabel ist, muss die maximale Blockgröße in Bytes angegeben werden. Wenn die Blockgröße unbekannt ist oder ein Block Konzept nicht zutrifft, sollte der Wert "1" (unbekannt) verwendet werden.

</dd> <dt>

**Begrenzung**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: über [**Schreiben**](../wmisdk/standard-qualifiers.md) ("Limit"), [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ storagezucationsettingdata**".**"Hastresourceblocksize**")
</dt> </dl>

Die maximale Block Menge, die für die Speicherressourcen Zuordnung auf dem Host erteilt wird. Die Blockgröße wird durch die Eigenschaft " **hustresourceblocksize** " angegeben.

</dd> <dt>

**Otherhostextentnameformat**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ storagezugecationsettingdata**".**Hostextentnameformat**")
</dt> </dl>

Das Format der **hostextentname** -Eigenschaft, wenn die-Eigenschaft auf "1" (sonstige) festgelegt ist.

</dd> <dt>

**Otherhostextentnamenamespace**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ storagezugecationsettingdata**".**Hostextentnamenamespace**")
</dt> </dl>

Eine Zeichenfolge, die den Namespace der **hostextentname** -Eigenschaft beschreibt, wenn der Wert der **hostextentnamenamespace** -Eigenschaft "1" (sonstige) ist.

</dd> <dt>

**Reservierung**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](../wmisdk/standard-qualifiers.md) Setzung ("Reservierung"), [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ storagezugecationsettingdata**".**"Hastresourceblocksize**")
</dt> </dl>

Die Anzahl der Blöcke, die garantiert für die Speicherressourcen Zuordnung auf dem Host verfügbar sind. Die Blockgröße wird durch die Eigenschaft " **hustresourceblocksize** " angegeben.

</dd> <dt>

**VirtualQuantity**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: über [**Schreiben**](../wmisdk/standard-qualifiers.md) ("virtualmenge"), [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ storageblock**](cim-storageextent.md)".**"Anzahlungsblöcke**", "**CIM \_ storagezugecationsettingdata**".**Virtualquantityunits**")
</dt> </dl>

Die Anzahl der Blöcke, die die Speicher Belegung für den Consumer darstellt.

> [!Note]  
> Die **virtualmenge** -Eigenschaft kann eine Blockgröße von "1" angeben, auch wenn " **virtualresourceblocksize** " unbekannt ist.

 

</dd> <dt>

**Virtualquantityunits**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: über [**Schreiben**](../wmisdk/standard-qualifiers.md) ("virtualquantityunits"), [**modelkorrespondenz**](../wmisdk/standard-qualifiers.md) ("**CIM \_ storagezugegenationsettingdata**".**Virtualmenge**"), **ispunit**
</dt> </dl>

Die Einheiten, die von der **virtualmenge** -Eigenschaft verwendet werden. Dieser Wert muss auf "count (Block mit fester Größe)" oder "Byte" festgelegt werden. Der Standardwert "count (Block mit fester Größe)" sollte für eine Blockgröße mit fester Größe verwendet werden, und "Byte" sollte für eine unbekannte oder Variable Blockgröße verwendet werden.

</dd> <dt>

**Virtualresourceblocksize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ storageblock**](cim-storageextent.md)".**BlockSize**"), **Punit** (" Byte ")
</dt> </dl>

Die Größe (in Bytes) der Blöcke, die die Speicher Belegungs Anforderung bilden. Wenn die Blockgröße variabel ist, muss die maximale Blockgröße angegeben werden. Wenn die Blockgröße unbekannt ist oder ein Block Konzept nicht zutrifft, sollte die Blockgröße "1" (unbekannt) lauten.

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

[**CIM \_ resourcezubesettingdata**](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

