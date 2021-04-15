---
description: Stellt die Funktionen und die Verwaltung von speicherbezogenen logischen Geräten dar.
ms.assetid: 802c1c0e-7eab-4a17-9a29-6502ece6cb24
title: CIM_Memory-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Memory
- CIM_Memory.Volatile
- CIM_Memory.ErrorMethodology
- CIM_Memory.StartingAddress
- CIM_Memory.EndingAddress
- CIM_Memory.ErrorInfo
- CIM_Memory.OtherErrorDescription
- CIM_Memory.CorrectableError
- CIM_Memory.ErrorTime
- CIM_Memory.ErrorAccess
- CIM_Memory.ErrorTransferSize
- CIM_Memory.ErrorData
- CIM_Memory.ErrorDataOrder
- CIM_Memory.ErrorAddress
- CIM_Memory.SystemLevelAddress
- CIM_Memory.ErrorResolution
- CIM_Memory.AdditionalErrorData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 410d580542421aee153b610726bed1f438efbcde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529504"
---
# <a name="cim_memory-class-hyper-v-management"></a>CIM_Memory-Klasse (Hyper-V-Verwaltung)

Stellt die Funktionen und die Verwaltung von speicherbezogenen logischen Geräten dar.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.8.0"), UMLPackagePath("CIM::Device::Memory"), AMENDMENT]
class CIM_Memory : CIM_StorageExtent
{
  boolean  Volatile;
  string   ErrorMethodology;
  uint64   StartingAddress;
  uint64   EndingAddress;
  uint16   ErrorInfo;
  string   OtherErrorDescription;
  boolean  CorrectableError;
  datetime ErrorTime;
  uint16   ErrorAccess;
  uint32   ErrorTransferSize;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  uint64   ErrorAddress;
  boolean  SystemLevelAddress;
  uint64   ErrorResolution;
  uint8    AdditionalErrorData[];
};
```

## <a name="members"></a>Member

Die **CIM- \_ Speicher** Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM- \_ Speicher** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**AdditionalErrorData**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. AdditionalErrorData"), **octetstring**, [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 005,18 "," MIF. Physisches DMTF- \| Speicher Array \| 001,13 ")
</dt> </dl>

Ein Array von Oktetten, das zusätzliche Fehlerinformationen enthält. Ein Beispiel hierfür ist ECC-Syndrom oder die Rückgabe der Kontroll Bits, wenn eine CRC-basierte Fehler Methodik verwendet wird. Wenn in letzterem Fall ein Single-Bit-Fehler erkannt wird und der CRC-Algorithmus bekannt ist, können Sie das genaue Bit ermitteln, bei dem ein Fehler aufgetreten ist.

Wenn die **errorInfo** -Eigenschaft den Wert "3" (OK) enthält, wird diese Eigenschaft nicht verwendet.

</dd> <dt>

**Korrektur Fehler**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. correctableerror"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Physisches DMTF- \| Speicher Array \| 001,8 ")
</dt> </dl>

**true** , wenn der letzte Fehler korrigiert werden kann. andernfalls **false**. Wenn die **errorInfo** -Eigenschaft den Wert "3" (OK) enthält, wird diese Eigenschaft nicht verwendet.

</dd> <dt>

**"Endadresse"**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Kilobyte"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Das DMTF- \| Speicher Array hat die Adressen \| 001,4 "," MIF "zugeordnet. DMTF- \| Speichergerät, zugeordnete Adressen \| 001,5 "), **Punit** (" Byte \* 10 ^ 3 ")
</dt> </dl>

Die Endadresse, auf die von einer Anwendung oder einem Betriebssystem verwiesen wird und die von einem Speichercontroller für das Speicher Objekt zugeordnet wird. Die Endadresse wird in Kilobyte angegeben.

</dd> <dt>

**ErrorAccess**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorAccess"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Physisches DMTF- \| Speicher Array \| 001,10 ")
</dt> </dl>

Der Speicherzugriffs Vorgang, der den letzten Fehler verursacht hat. Wenn die **errorInfo** -Eigenschaft den Wert "3" (OK) enthält, wird diese Eigenschaft nicht verwendet.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (2)


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

**Lesen** (3)


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

**Schreiben** (4)


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

**Partieller Schreibvorgang** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**ErrorAddress**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. StartingAddress"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 005,19 "," MIF. Physisches DMTF- \| Speicher Array \| 001,14 ")
</dt> </dl>

Die Adresse des letzten Speicher Fehlers. Der Fehlertyp wird von der **errorInfo** -Eigenschaft beschrieben. Wenn die **errorInfo** -Eigenschaft den Wert "3" (OK) enthält, wird diese Eigenschaft nicht verwendet.

</dd> <dt>

**ErrorData**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorData"), **octetstring**, [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Physisches DMTF- \| Speicher Array \| 001,12 ")
</dt> </dl>

Ein Array, das Daten enthält, die während des letzten fehlerhaften Speicherzugriffs aufgezeichnet wurden. Die Daten belegen die ersten n Oktette des Arrays, die die Anzahl der Bits enthalten muss, die von der **ErrorTransferSize** -Eigenschaft angegeben werden.

Wenn die **ErrorTransferSize** -Eigenschaft den Wert "0" (OK) enthält, wird diese Eigenschaft nicht verwendet.

</dd> <dt>

**ErrorDataOrder**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorDataOrder")
</dt> </dl>

Die Reihenfolge der in der **ErrorData** -Eigenschaft gespeicherten Daten. Es kann "least signifikanter Byte First" (Value = 1) oder "Most signifikanter Byte First" (2) angegeben werden. Wenn die **ErrorTransferSize** -Eigenschaft den Wert "0" (OK) enthält, wird diese Eigenschaft nicht verwendet.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

**Am wenigsten signifikantes Byte zuerst** (1)


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

**Signifikanteste Byte First** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**ErrorInfo**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorInfo"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 005,12 "," MIF. DMTF \| physikalisches Speicher Array \| 001,8 "), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM-Arbeits **\_ Speicher**".**Othererrordescription**")
</dt> </dl>

Der Typ des letzten Fehlers, der auftreten soll.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (2)


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

**OK** (3)


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

Ungültiger **Lese** Vorgang (4)


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

**Paritätsfehler** (5)


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

**Einzelbit-Fehler** (6)


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

**Doppelbit-Fehler** (7)


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

**Multi-Bit-Fehler** (8)


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

**Nibble-Fehler** (9)


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

**Prüfsummen Fehler** (10)


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

**CRC-Fehler** (11)


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

Nicht **definiert** (12)


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

Nicht **definiert** (13)


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

Nicht **definiert** (14)


</dt> <dd></dd> </dl>

</dd> <dt>

**Errormethodmethodologie**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("errormethod"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Physisches DMTF- \| Speicher Array \| 001,7 ")
</dt> </dl>

Gibt an, ob Paritäts Algorithmen, CRC-Algorithmen, ECC oder andere Mechanismen vom Speicher Objekt verwendet werden. Details zum Algorithmus können auch bereitgestellt werden.

</dd> <dt>

**ErrorResolution**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorResolution"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| Speichergerät \| 005,21 "," MIF. DMTF \| physikalisches Speicher Array \| 001,15 "), **Punit** (" Byte ")
</dt> </dl>

Der Bereich in Bytes, in dem der letzte Fehler aufgelöst werden kann. Wenn z. b. Fehler Adressen in Bit 11 aufgelöst werden, z. b. auf einer typischen Seite, Anschließend können die Fehler in 4K-Begrenzungen aufgelöst werden, und diese Eigenschaft wird auf "4000" festgelegt. Wenn die **errorInfo** -Eigenschaft den Wert "3" (OK) enthält, wird diese Eigenschaft nicht verwendet.

</dd> <dt>

**ErrorTime**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. errortime")
</dt> </dl>

Der Zeitpunkt, zu dem der letzte Speicherfehler aufgetreten ist. Wenn die **errorInfo** -Eigenschaft den Wert "3" (OK) enthält, wird diese Eigenschaft nicht verwendet.

</dd> <dt>

**ErrorTransferSize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. ErrorTransferSize"), [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| physikalisches Speicher Array \| 001,11 "), **Punit** (" Bit ")
</dt> </dl>

Die Größe der Datenübertragung in Bits, die den letzten Fehler verursacht hat. "0" gibt keinen Fehler an. Wenn die **errorInfo** -Eigenschaft den Wert "3" (OK) enthält, wird diese Eigenschaft nicht verwendet.

</dd> <dt>

**Othererrordescription**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ MemoryError. othererrordescription"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Speicher**.**ErrorInfo**")
</dt> </dl>

Eine Beschreibung des Fehler Typs, wenn die **ErrorType** -Eigenschaft auf "1" (sonstige) festgelegt ist.

</dd> <dt>

**StartingAddress**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Kilobyte"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". Das DMTF- \| Speicher Array hat die Adressen \| 001,3 "," MIF "zugeordnet. DMTF- \| Speichergerät, zugeordnete Adressen \| 001,4 "), **Punit** (" Byte \* 10 ^ 3 ")
</dt> </dl>

Die Startadresse, auf die von einer Anwendung oder einem Betriebssystem verwiesen wird und die von einem Speichercontroller für das Speicher Objekt zugeordnet wird. Die Startadresse wird in Kilobyte angegeben.

</dd> <dt>

**SystemLevelAddress**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_MemoryError.Systemleveladdress")
</dt> </dl>

**true** , wenn die Adressinformationen in der **ErrorAddress** -Eigenschaft eine Adresse auf Systemebene sind, **false** , wenn es sich um eine physische Adresse handelt.

</dd> <dt>

**Ständigem**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**true** , wenn der Arbeitsspeicher flüchtig ist. andernfalls **false**.

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

[**CIM- \_ storageblock**](cim-storageextent.md)
</dt> </dl>

 

