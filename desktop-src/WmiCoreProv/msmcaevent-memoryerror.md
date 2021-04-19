---
description: Stellt ein MCA-Speicherfehler Ereignis dar. Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.
ms.assetid: 0db1d526-e2c3-4e48-90c8-cbcd9121040e
title: MSMCAEvent_MemoryError-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_MemoryError
- MSMCAEvent_MemoryError.Active
- MSMCAEvent_MemoryError.AdditionalErrors
- MSMCAEvent_MemoryError.BUS_SPECIFIC_DATA
- MSMCAEvent_MemoryError.Cpu
- MSMCAEvent_MemoryError.ErrorSeverity
- MSMCAEvent_MemoryError.InstanceName
- MSMCAEvent_MemoryError.MEM_BANK
- MSMCAEvent_MemoryError.MEM_BIT_POSITION
- MSMCAEvent_MemoryError.MEM_CARD
- MSMCAEvent_MemoryError.MEM_COLUMN
- MSMCAEvent_MemoryError.MEM_ERROR_STATUS
- MSMCAEvent_MemoryError.MEM_MODULE
- MSMCAEvent_MemoryError.MEM_NODE
- MSMCAEvent_MemoryError.MEM_PHYSICAL_ADDR
- MSMCAEvent_MemoryError.MEM_PHYSICAL_MASK
- MSMCAEvent_MemoryError.MEM_ROW
- MSMCAEvent_MemoryError.RawRecord
- MSMCAEvent_MemoryError.RecordId
- MSMCAEvent_MemoryError.REQUESTOR_ID
- MSMCAEvent_MemoryError.RESPONDER_ID
- MSMCAEvent_MemoryError.Size
- MSMCAEvent_MemoryError.TARGET_ID
- MSMCAEvent_MemoryError.Type
- MSMCAEvent_MemoryError.VALIDATION_BITS
- MSMCAEvent_MemoryError.MEM_DEVICE
- MSMCAEvent_MemoryError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 8dce82b8fa7a87676c34a9c6f26f43e4db10e227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353884"
---
# <a name="msmcaevent_memoryerror-class"></a>Msmcaevent \_ MemoryError-Klasse

Die **msmcaevent \_ MemoryError** -Klasse stellt ein MCA-Speicherfehler Ereignis dar. Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.

Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
class MSMCAEvent_MemoryError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint64  BUS_SPECIFIC_DATA;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint16  MEM_BANK;
  uint16  MEM_BIT_POSITION;
  uint16  MEM_CARD;
  uint16  MEM_COLUMN;
  uint64  MEM_ERROR_STATUS;
  uint16  MEM_MODULE;
  uint16  MEM_NODE;
  uint64  MEM_PHYSICAL_ADDR;
  uint64  MEM_PHYSICAL_MASK;
  uint16  MEM_ROW;
  uint8   RawRecord[];
  uint64  RecordId;
  uint64  REQUESTOR_ID;
  uint64  RESPONDER_ID;
  uint32  Size;
  uint64  TARGET_ID;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint16  MEM_DEVICE;
  uint32  LogToEventlog;
};
```

## <a name="members"></a>Member

Die **msmcaevent \_ MemoryError** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **msmcaevent \_ MemoryError** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Aktiv**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True**, wenn diese Instanz der-Klasse aktiv ist. andernfalls **false**.

</dd> <dt>

**Additionalerrors**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl zusätzlicher Fehler im MCA-Datensatz.

</dd> <dt>

**\_Busspezifische \_ Daten**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

OEM-spezifische, Bus abhängige Daten.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**CPU**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

CPU, die den Fehler gemeldet hat. Diese Eigenschaft gilt nur für ein Multiprozessorsystem, dem dem ersten Prozessor die Zahl 0 zugewiesen ist, dem zweiten Prozessor die Zahl 1 zugewiesen wird usw.

</dd> <dt>

**Errorschwere Grad**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Schweregrad des gemeldeten Fehlers.



| Wert                                                                                                | Bedeutung                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Wiederherstellbar<br/> |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | FAT<br/>       |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | KORRIGIER barer<br/> |



 

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Eindeutiger Bezeichner dieser Instanz der Klasse.

</dd> <dt>

**Logtoeventlog**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Wenn der Wert NULL ist, wird dieses Ereignis nicht im System Ereignisprotokoll protokolliert.

</dd> <dt>

**Arbeitsspeicher- \_ Bank**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Modul oder die Rang Nummer des Speicherfehler Speicher Orts.

</dd> <dt>

**Arbeitsspeicher- \_ \_ Bitposition**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Bitposition im Arbeitsspeicher Wort, die den Fehler enthält.

</dd> <dt>

**Arbeitsspeicher \_ Karte**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Kartennummer des Speicherfehler Speicher Orts.

</dd> <dt>

**Arbeitsspeicher \_ Spalte**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Spaltennummer des Speicherfehler Speicher Orts.

</dd> <dt>

**Arbeits \_ Speichergerät**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gerätenummer des Speicherfehler Speicher Orts.

</dd> <dt>

**Status des Arbeitsspeicher \_ Fehlers \_**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Fehlerstatus des Speichers.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**Arbeitsspeicher \_ Modul**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Modul oder Rang Nummer des Speicherfehler Speicher Orts.

</dd> <dt>

**\_Knoten "Knoten"**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Knoten, der den Arbeitsspeicher Fehler enthält. Diese Eigenschaft ist nur in einem System mit mehreren Knoten anwendbar. Diese Eigenschaft ist Anbieter spezifisch.

</dd> <dt>

**physische Arbeitsspeicher- \_ \_ addr**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die physische Adresse des Arbeitsspeicher Fehlers.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**physische Arbeitsspeicher \_ \_ Maske**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gültige Adress Bits in der physischen 64-Bit-Adresse des Arbeitsspeicher Fehlers.

> [!Note]  
> Die physische Maske gibt die Granularität der physischen Adresse an. Die physische Adresse des Arbeitsspeicher Fehlers hängt von den Hardware Implementierungs Faktoren ab.

 

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**Arbeitsspeicher \_ Zeile**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Zeilennummer des Speicherfehler Speicher Orts.

</dd> <dt>

**Rawrecord**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Bytearray, das den unformatierten Fehler Daten Satz enthält, wie Windows von der System Abstraktion Layer (SAL) dargestellt wird. Die Anzahl der Elemente im Array wird durch die **size** -Eigenschaft angegeben.

</dd> <dt>

**Datensatz**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Datensatz-ID des Fehler Datensatzes für diesen Fehler.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**\_RequestId-ID**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Hardware Adresse des Geräts oder der Komponente, von der die Transaktion initiiert wird.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**Responder- \_ ID**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Hardware Adresse des Responders für die Transaktion.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**Größe**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Größe des unformatierten Fehler Datensatzes in Byte.

</dd> <dt>

**Ziel- \_ ID**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Hardware Adresse des beabsichtigten Ziels der Transaktion.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**Type**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Typ der Ereignisprotokoll Meldung. Diese Meldungen entsprechen den Ereignisprotokoll-Nachrichten Codes, die zum Einfügen von Ereignisprotokoll Meldungen vom Windows-Ereignisprotokoll-Consumeranbieter verwendet werden, wenn ein Ereignis empfangen wird.

</dd> <dt>

**Validierungs \_ Bits**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Validierungs Bits zum Angeben der Gültigkeit der nachfolgenden Felder.



| Werte                                                                                     | Bedeutung                                                 |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <dt>1 (0x1)</dt> </dl>         | Der Status des Arbeitsspeicher \_ Fehlers \_ ist gültig.<br/>                 |
| <dl> <dt>2 (0x2)</dt> </dl>         | Die physische Arbeitsspeicher- \_ \_ addr ist gültig.<br/>                |
| <dl> <dt>4 (0x4)</dt> </dl>         | Die "Mem \_ addr \_ Mask" ist gültig.<br/>                    |
| <dl> <dt>8 (0x8)</dt> </dl>         | Der Arbeitsspeicher \_ Knoten ist gültig.<br/>                          |
| <dl> <dt>16 (0x10)</dt> </dl>       | Die Arbeitsspeicher \_ Karte ist gültig.<br/>                          |
| <dl> <dt>32 (0x20)</dt> </dl>       | Das Speicher \_ Modul ist gültig.<br/>                        |
| <dl> <dt>64 (0x40)</dt> </dl>       | Die Arbeitsspeicher- \_ Bank ist gültig.<br/>                          |
| <dl> <dt>128 (0x80)</dt> </dl>      | Das Arbeits \_ Speichergerät ist gültig.<br/>                        |
| <dl> <dt>256 (0x100)</dt> </dl>     | Die Arbeitsspeicher \_ Zeile ist gültig.<br/>                           |
| <dl> <dt>512 (0x200)</dt> </dl>     | Die Arbeitsspeicher \_ Spalte ist gültig.<br/>                        |
| <dl> <dt>1024 (0x400)</dt> </dl>    | Die Arbeitsspeicher- \_ \_ Bitposition ist gültig.<br/>                 |
| <dl> <dt>2048 (0x800)</dt> </dl>    | Die ID der Arbeitsspeicher \_ Plattform \_ \_ ist gültig.<br/>       |
| <dl> <dt>4096 (0x1000)</dt> </dl>   | Die \_ Antwort-ID der Arbeitsspeicher Plattform \_ \_ ist gültig.<br/>       |
| <dl> <dt>8192 (0x2000)</dt> </dl>   | Das Ziel der G4- \_ Plattform \_ ist gültig.<br/>              |
| <dl> <dt>16384 (0x4000)</dt> </dl>  | Die \_ spezifischen Daten des G4-Platt Form \_ Busses \_ \_ sind gültig.<br/> |
| <dl> <dt>32768 (0X8000)</dt> </dl>  | Die OEM-ID der Arbeitsspeicher \_ Plattform \_ \_ ist gültig.<br/>             |
| <dl> <dt>65536 (0x10000)</dt> </dl> | Die \_ OEM-Datenstruktur der Arbeitsspeicher Plattform \_ \_ \_ ist gültig.<br/>   |



 

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **msmcaevent \_ MemoryError** -Klasse wird von [**wmievent**](wmievent.md)abgeleitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003<br/>                                                         |
| Namespace<br/>                | WMI-Stammdatei \\<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WMI Core. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wmiprov.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MSMCA-Klassen](msmca-classes.md)
</dt> <dt>

[**WMIEvent**](wmievent.md)
</dt> </dl>

 

