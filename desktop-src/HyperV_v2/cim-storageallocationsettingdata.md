---
description: Stellt Einstellungen für die Zuordnung von virtuellem Speicher dar.
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
ms.openlocfilehash: fe380b03daced6ca98a44c189c52b5842862aa2e033bf66a04f8dd1466968449
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899670"
---
# <a name="cim_storageallocationsettingdata-class"></a>CIM \_ StorageAllocationSettingData-Klasse

Stellt Einstellungen für die Zuordnung von virtuellem Speicher dar.

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

Die **CIM \_ StorageAllocationSettingData-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ StorageAllocationSettingData-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**zugreifen**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**Zugriff**")
</dt> </dl>

Die Lese-/Schreibunterstützung der Speicherzuordnung.

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

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF Reserved** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**HostExtentName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentNameFormat**", "**CIM \_ StorageAllocationSettingData**.**HostExtentNameNamespace**", "[**CIM \_ StorageExtent**](cim-storageextent.md).**Name**")
</dt> </dl>

Ein eindeutiger Bezeichner des Speicherumfangs des Hosts.

</dd> <dt>

**HostExtentNameFormat**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentName**", "**CIM \_ StorageAllocationSettingData**.**OtherHostExtentNameFormat**", "[**CIM \_ StorageExtent**](cim-storageextent.md).**NameFormat**")
</dt> </dl>

Das Format des **HostExtentName-Eigenschaftswerts.**

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Andere** (1)


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

<span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)


</dt> <dd>

Serial Number/Vendor/Model (SNVM) SNVM besteht aus drei Zeichenfolgen, die den Herstellernamen, den Produktnamen innerhalb des Anbieternamespace und die Seriennummer im Modellnamespace darstellen. Zeichenfolgen werden durch ein "+" getrennt. Leerzeichen können eingeschlossen werden und sind von Bedeutung. Die Seriennummer ist die Textdarstellung der Seriennummer in hexadezimaler Großschreibung. Dies stellt die Anbieter- und Modell-ID aus SCSI-Abfragedaten dar. Das Herstellerfeld MUSS 8 Zeichen breit sein, und das Produktfeld MUSS 16 Zeichen breit sein. Beispiel:

"ACME \_ \_ \_ \_ +SUPER DISK \_ \_ \_ \_ \_ \_ +124437458" ( \_ ist ein Leerzeichen)

</dd> <dt>

<span id="NAA"></span><span id="naa"></span>

<span id="NAA"></span><span id="naa"></span>**NAA** (9)


</dt> <dd>

9 = NAA als generisches Format. Siehe

https://standards.ieee.org/regauth/oui/tutorials/fibrecomp\_id.html. Formatiert als 16 oder 32 nicht analysierte hexadezimale Großbuchstaben (2 pro binärem Byte).

Beispiel: "21000020372D3C73"

</dd> <dt>

<span id="EUI64"></span><span id="eui64"></span>

<span id="EUI64"></span><span id="eui64"></span>**EUI64** (10)


</dt> <dd>

EUI als generisches Format (EUI64) Siehe

https://standards.ieee.org/content/dam/ieee-standards/standards/web/documents/tutorials/eui.pdf.

</dd> <dt>

<span id="T10VID"></span><span id="t10vid"></span>

<span id="T10VID"></span><span id="t10vid"></span>**T10VID** (11)


</dt> <dd>

T10 vendor identifier format as returned by SCSI Inquiry VPD page 83, identifier type 1. Siehe T10 SPC-3-Spezifikation. Dies ist die 8-Byte-ASCII-Anbieter-ID aus der T10-Registrierung gefolgt von einem anbieterspezifischen ASCII-Bezeichner. Leerzeichen sind zulässig. Für Nicht-SCSI-Volumes ist "SNVM" möglicherweise die am besten geeignete Wahl.

</dd> <dt>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>**Name des Betriebssystemgeräts** (12)


</dt> <dd>

Name des Betriebssystemgeräts (für LogicalDisks). Weitere Informationen finden Sie unter LogicalDisk Name description (Beschreibung des Logischen Datenträgernamens).

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**HostExtentNameNamespace**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentName**", "**CIM \_ StorageAllocationSettingData**.**OtherHostExtentNameNamespace**", "**CIM \_ StorageAllocationSettingData**.**HostExtentNameFormat**", "[**CIM \_ StorageExtent**](cim-storageextent.md).**Namespace**")
</dt> </dl>

Das Benennungsformat für die **Name-Eigenschaft.**

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


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF Reserved** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**HostExtentStartingAddress**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostResourceBlockSize**", "[**CIM \_ BasedOn**](cim-basedon.md).**StartingAddress**")
</dt> </dl>

Die Startadresse im Speicherumfang des Hosts. Null val;ue gibt an, dass es keine direkte Zuordnung zwischen dem virtuellen Speicherumfang und dem Hostspeicherumfang gibt.

</dd> <dt>

**HostResourceBlockSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**BlockSize**"), **PUnit** ("byte")
</dt> </dl>

Die Größe der Blöcke in Bytes, die auf dem Host für die Speicherbelegung zugeordnet sind. Wenn die Blockgröße variabel ist, sollte die maximale Blockgröße in Bytes angegeben werden. Wenn die Blockgröße unbekannt ist oder ein Blockkonzept nicht zutrifft, sollte der Wert "1" (unbekannt) verwendet werden.

</dd> <dt>

**Begrenzung**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](../wmisdk/standard-qualifiers.md) ("Limit"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostResourceBlockSize**")
</dt> </dl>

Die maximale Anzahl von Blöcken, die für die Speicherressourcenzuordnung auf dem Host gewährt werden. Die Blockgröße wird von der **HostResourceBlockSize-Eigenschaft** angegeben.

</dd> <dt>

**OtherHostExtentNameFormat**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentNameFormat**")
</dt> </dl>

Das Format der **HostExtentName-Eigenschaft,** wenn die -Eigenschaft auf "1" (andere) festgelegt ist.

</dd> <dt>

**OtherHostExtentNameNamespace**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentNameNamespace**")
</dt> </dl>

Eine Zeichenfolge, die den Namespace der **HostExtentName-Eigenschaft** beschreibt, wenn der Wert der **HostExtentNameNamespace-Eigenschaft** "1" (andere) ist.

</dd> <dt>

**Reservierung**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](../wmisdk/standard-qualifiers.md) [**("Reservierung"), ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostResourceBlockSize**")
</dt> </dl>

Die Menge der Blöcke, die garantiert für die Speicherressourcenzuordnung auf dem Host verfügbar sind. Die Blockgröße wird von der **HostResourceBlockSize-Eigenschaft** angegeben.

</dd> <dt>

**VirtualQuantity**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](../wmisdk/standard-qualifiers.md) ("VirtualQuantity"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**NumberOfBlocks**", "**CIM \_ StorageAllocationSettingData**.**VirtualQuantityUnits**")
</dt> </dl>

Die Anzahl der Blöcke, die dem Consumer von der Speicherbelegung präsentiert werden.

> [!Note]  
> Die **VirtualQuantity-Eigenschaft** kann eine Blockgröße von "1" angeben, auch wenn **VirtualResourceBlockSize** unbekannt ist.

 

</dd> <dt>

**VirtualQuantityUnits**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](../wmisdk/standard-qualifiers.md) ("VirtualQuantityUnits"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**VirtualQuantity**"), **IsPUnit**
</dt> </dl>

Die von der **VirtualQuantity-Eigenschaft verwendeten** Einheiten. Dieser Wert muss auf "count(fixed size block)" oder "byte" festgelegt werden. Der Standardwert "count(fixed size block)" sollte für eine feste Blockgröße und "byte" für eine unbekannte oder variable Blockgröße verwendet werden.

</dd> <dt>

**VirtualResourceBlockSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**BlockSize**"), **PUnit** ("byte")
</dt> </dl>

Die Größe der Blöcke in Bytes, die die Speicherbelegungsanforderung bilden. Wenn die Blockgröße variabel ist, sollte die maximale Blockgröße angegeben werden. Wenn die Blockgröße unbekannt ist oder kein Blockkonzept gilt, sollte die Blockgröße "1" (unbekannt) sein.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

