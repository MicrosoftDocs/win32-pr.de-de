---
description: Stellt ein McA-Arbeitsspeicherfehlerereignis (Machine Check Architecture) dar. Diese Klasse ist nur in 64-Bit-Systemen Windows verfügbar.
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
ms.openlocfilehash: f93ac9ddda978a56ceb0e258766c2e60703acc94e92c551e673a9294e2cb984c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120980"
---
# <a name="msmcaevent_memoryerror-class"></a>MSMCAEvent \_ MemoryError-Klasse

Die **MSMCAEvent \_ MemoryError-Klasse** stellt ein McA-Arbeitsspeicherfehlerereignis (Machine Check Architecture) dar. Diese Klasse ist nur in 64-Bit-Systemen Windows verfügbar.

Die folgende Syntax wird durch Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge.

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

Die **MSMCAEvent \_ MemoryError-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSMCAEvent \_ MemoryError-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Aktiv**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**TRUE**, wenn diese Instanz der -Klasse aktiv ist; andernfalls **FALSE**.

</dd> <dt>

**AdditionalErrors**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl zusätzlicher Fehler im MCA-Datensatz.

</dd> <dt>

**BUSSPEZIFISCHE \_ \_ DATEN**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

OEM-spezifische, busabhängige Daten.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

</dd> <dt>

**Cpu**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

CPU, die den Fehler gemeldet hat. Diese Eigenschaft gilt nur für ein Multiprozessorsystem, in dem dem ersten Prozessor die Zahl 0, dem zweiten Prozessor die Zahl 1 zugewiesen wird, und so weiter.

</dd> <dt>

**ErrorSeverity**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Schweregrad des gemeldeten Fehlers.



| Wert                                                                                                | Bedeutung                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Wiederherstellbar<br/> |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Schwerwiegend<br/>       |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Korrigierbar<br/> |



 

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Eindeutiger Bezeichner dieser Instanz der -Klasse.

</dd> <dt>

**LogToEventlog**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Wenn 0 (null) ist, wird dieses Ereignis nicht im Systemereignisprotokoll protokolliert.

</dd> <dt>

**MEM \_ BANK**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Modul- oder RANK-Nummer des Speicherfehlerspeicherorts.

</dd> <dt>

**\_ \_ MEM-BITPOSITION**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Bitposition im Speicherwort, das den Fehler enthält.

</dd> <dt>

**\_MEM-KARTE**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Kartennummer der Speicherfehlerposition.

</dd> <dt>

**\_MEM-SPALTE**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Spaltennummer der Speicherfehlerposition.

</dd> <dt>

**\_MEM-GERÄT**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gerätenummer des Speicherfehlerspeicherorts.

</dd> <dt>

**\_ \_ MEM-FEHLERSTATUS**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Arbeitsspeicherfehlerstatus.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

</dd> <dt>

**\_MEM-MODUL**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Modul- oder Rangnummer des Speicherfehlerspeicherorts.

</dd> <dt>

**\_MEM-KNOTEN**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Knoten, der den Speicherfehler enthält. Diese Eigenschaft gilt nur in einem System mit mehreren Knoten. Diese Eigenschaft ist herstellerspezifisch.

</dd> <dt>

**MEM \_ PHYSICAL \_ ADDR**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Physische Adresse des Arbeitsspeicherfehlers.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

</dd> <dt>

**MEM \_ PHYSICAL \_ MASK**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gültige Adressbits in der physischen 64-Bit-Adresse des Speicherfehlers.

> [!Note]  
> Die physische Maske gibt die Granularität der physischen Adresse an. Die physische Adresse des Arbeitsspeicherfehlers hängt von Hardwareimplementierungsfaktoren ab.

 

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

</dd> <dt>

**MEM \_ ROW**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zeilennummer des Speicherorts für Speicherfehler.

</dd> <dt>

**RawRecord**
</dt> <dd> <dl> <dt>

Datentyp: **uint8-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Bytearray, das den unformatierten Fehlerdatensatz enthält, der von der Systemabstraktionsschicht (SAL) Windows wird. Die Anzahl der Elemente im Array wird von der **Size-Eigenschaft** angegeben.

</dd> <dt>

**Recordid**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Datensatzbezeichner des Fehlerdatensatzes für diesen Fehler.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

</dd> <dt>

**\_ANFORDERER-ID**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Hardwareadresse des Geräts oder der Komponente, das bzw. die die Transaktion initiiert.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

</dd> <dt>

**\_ANTWORT-ID**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Hardwareadresse des Antwortstellers für die Transaktion.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

</dd> <dt>

**Größe**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Größe des unformatierten Fehlerdatensatzes in Bytes.

</dd> <dt>

**\_ZIEL-ID**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Hardwareadresse des beabsichtigten Ziels der Transaktion.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

</dd> <dt>

**Typ**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Typ der Ereignisprotokollmeldung. Diese Nachrichten entsprechen den Ereignisprotokoll-Nachrichtencodes, die vom Windows Ereignisprotokoll-Consumeranbieter zum Einfügen von Ereignisprotokollmeldungen verwendet werden, wenn eines der Ereignisse empfangen wird.

</dd> <dt>

**\_VALIDIERUNGSBITS**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Validierungsbits, die verwendet werden, um die Gültigkeit der nachfolgenden Felder anzugeben.



| Werte                                                                                     | Bedeutung                                                 |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <dt>1 (0x1)</dt> </dl>         | MEM \_ ERROR STATUS ist \_ gültig.<br/>                 |
| <dl> <dt>2 (0x2)</dt> </dl>         | MEM \_ PHYSICAL \_ ADDR ist gültig.<br/>                |
| <dl> <dt>4 (0x4)</dt> </dl>         | MEM \_ ADDR \_ MASK ist gültig.<br/>                    |
| <dl> <dt>8 (0x8)</dt> </dl>         | MEM \_ NODE ist gültig.<br/>                          |
| <dl> <dt>16 (0x10)</dt> </dl>       | MEM \_ CARD ist gültig.<br/>                          |
| <dl> <dt>32 (0x20)</dt> </dl>       | MEM \_ MODULE ist gültig.<br/>                        |
| <dl> <dt>64 (0x40)</dt> </dl>       | MEM \_ BANK ist gültig.<br/>                          |
| <dl> <dt>128 (0x80)</dt> </dl>      | MEM \_ DEVICE ist gültig.<br/>                        |
| <dl> <dt>256 (0x100)</dt> </dl>     | MEM \_ ROW ist gültig.<br/>                           |
| <dl> <dt>512 (0x200)</dt> </dl>     | MEM \_ COLUMN ist gültig.<br/>                        |
| <dl> <dt>1024 (0x400)</dt> </dl>    | MEM \_ BIT POSITION ist \_ gültig.<br/>                 |
| <dl> <dt>2048 (0x800)</dt> </dl>    | DIE MEM \_ PLATFORM \_ \_ REQUESTOR-ID ist gültig.<br/>       |
| <dl> <dt>4096 (0x1000)</dt> </dl>   | DIE MEM \_ PLATFORM \_ \_ RESPONDER-ID ist gültig.<br/>       |
| <dl> <dt>8192 (0x2000)</dt> </dl>   | MEM \_ PLATFORM TARGET ist \_ gültig.<br/>              |
| <dl> <dt>16384 (0x4000)</dt> </dl>  | MEM \_ PLATFORM \_ \_ BUS-SPEZIFISCHE \_ DATEN sind gültig.<br/> |
| <dl> <dt>32768 (0x8000)</dt> </dl>  | DIE MEM \_ \_ PLATFORM-OEM-ID \_ ist gültig.<br/>             |
| <dl> <dt>65536 (0x10000)</dt> </dl> | MEM \_ PLATFORM OEM DATA \_ \_ \_ STRUCT ist gültig.<br/>   |



 

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **MSMCAEvent \_ MemoryError-Klasse** wird von [**WMIEvent**](wmievent.md)abgeleitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003<br/>                                                         |
| Namespace<br/>                | Root \\ wmi<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Wmicore.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wmiprov.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MSMCA-Klassen](msmca-classes.md)
</dt> <dt>

[**WMIEvent**](wmievent.md)
</dt> </dl>

 

