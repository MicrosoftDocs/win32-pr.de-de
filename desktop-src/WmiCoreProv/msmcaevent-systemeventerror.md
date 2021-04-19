---
description: Gibt an, dass ein Intelligent Platform Management Interface (IPMI)-System Ereignis aufgetreten ist. Der Fehler wird in das SMBIOS-System Ereignisprotokoll (SEL) geschrieben. Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.
ms.assetid: 1964f850-ac55-4639-9205-2eb0996dbaae
title: MSMCAEvent_SystemEventError-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_SystemEventError
- MSMCAEvent_SystemEventError.Active
- MSMCAEvent_SystemEventError.AdditionalErrors
- MSMCAEvent_SystemEventError.Cpu
- MSMCAEvent_SystemEventError.ErrorSeverity
- MSMCAEvent_SystemEventError.InstanceName
- MSMCAEvent_SystemEventError.RawRecord
- MSMCAEvent_SystemEventError.RecordId
- MSMCAEvent_SystemEventError.SEL_DATA1
- MSMCAEvent_SystemEventError.SEL_DATA2
- MSMCAEvent_SystemEventError.SEL_DATA3
- MSMCAEvent_SystemEventError.SEL_EVENT_DIR_TYPE
- MSMCAEvent_SystemEventError.SEL_EVM_REV
- MSMCAEvent_SystemEventError.SEL_GENERATOR_ID
- MSMCAEvent_SystemEventError.SEL_RECORD_ID
- MSMCAEvent_SystemEventError.SEL_RECORD_TYPE
- MSMCAEvent_SystemEventError.SEL_SENSOR_NUM
- MSMCAEvent_SystemEventError.SEL_SENSOR_TYPE
- MSMCAEvent_SystemEventError.SEL_TIME_STAMP
- MSMCAEvent_SystemEventError.Size
- MSMCAEvent_SystemEventError.Type
- MSMCAEvent_SystemEventError.VALIDATION_BITS
- MSMCAEvent_SystemEventError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: f20f95fb5e1b1bf07b0f70c25d54122642b13569
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362629"
---
# <a name="msmcaevent_systemeventerror-class"></a>Msmcaevent \_ systemeventerror-Klasse

Die **msmcaevent \_ systemeventerror** -Klasse gibt an, dass ein Management Interface (IPMI)-System Ereignis aufgetreten ist. Der Fehler wird in das SMBIOS-System Ereignisprotokoll (SEL) geschrieben. Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.

Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
class MSMCAEvent_SystemEventError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   RawRecord[];
  uint64  RecordId;
  uint8   SEL_DATA1;
  uint8   SEL_DATA2;
  uint8   SEL_DATA3;
  uint8   SEL_EVENT_DIR_TYPE;
  uint8   SEL_EVM_REV;
  uint16  SEL_GENERATOR_ID;
  uint16  SEL_RECORD_ID;
  uint8   SEL_RECORD_TYPE;
  uint8   SEL_SENSOR_NUM;
  uint8   SEL_SENSOR_TYPE;
  uint64  SEL_TIME_STAMP;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a>Member

Die **msmcaevent \_ systemeventerror** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **msmcaevent \_ systemeventerror** -Klasse verfügt über diese Eigenschaften.

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

Anzahl zusätzlicher Fehler im Datensatz.

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

Wenn 0 (null) ist, wird dieses Ereignis nicht im System Ereignisprotokoll protokolliert.

</dd> <dt>

**Rawrecord**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Bytearray, das den unformatierten Fehler Daten Satz enthält. Die Anzahl von Elementen im Array, die von der **size** -Eigenschaft angegeben wird.

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

**SEL \_ data1**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ereignisdaten Feld 1.

</dd> <dt>

**SEL \_ data2**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ereignisdaten Feld 2.

</dd> <dt>

**SEL \_ data3**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ereignisdaten Feld 3.

</dd> <dt>

**SEL- \_ Ereignis \_ dir- \_ Typ**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Ereignis Verzeichnistyp.

</dd> <dt>

**SEL \_ EVM \_ Rev**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Format Version der Fehlermeldung.

</dd> <dt>

**SEL \_ Generator- \_ ID**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Software Bezeichner, wenn das Ereignis Software generiert wurde.

</dd> <dt>

**SEL- \_ Datensatz- \_ ID**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Datensatz-ID für den Zugriff auf das SMBIOS-System Ereignisprotokoll (SEL).

</dd> <dt>

**SEL- \_ Daten Satz \_ Typen**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Datensatztyp.

</dd> <dt>

**SEL- \_ Sensor \_ NUM**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Sensor Nummer, die das Ereignis generiert hat.

</dd> <dt>

**SEL \_ - \_ Sensortyp**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Sensortyp Code des Sensors, der das Ereignis generiert hat.

</dd> <dt>

**SEL- \_ Zeit \_ Stempel**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Zeitstempel des Ereignis Protokolls.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**Größe**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Größe des unformatierten Fehler Datensatzes.

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



| Wert                                                                                                                                            | Bedeutung                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="1_0x1"></span><span id="1_0X1"></span><dl> <dt>**1 0x1**</dt> </dl>             | **SEL \_ Die Datensatz- \_ ID** ist gültig.<br/>    |
| <span id="2_0x2"></span><span id="2_0X2"></span><dl> <dt>**2 0x2**</dt> </dl>             | **SEL \_ Der \_ Typ des Datensatzes** ist gültig.<br/>  |
| <span id="4_0x4"></span><span id="4_0X4"></span><dl> <dt>**4 0x4**</dt> </dl>             | **SEL \_ Die Generator- \_ ID** ist gültig.<br/> |
| <span id="8_0x8"></span><span id="8_0X8"></span><dl> <dt>**8 0x8**</dt> </dl>             | **SEL \_ EVM- \_ Rev** ist gültig.<br/>      |
| <span id="16_0x10"></span><span id="16_0X10"></span><dl> <dt>**16 0x10**</dt> </dl>       | **SEL \_ Der \_ Sensortyp** ist gültig.<br/>  |
| <span id="32_0x20"></span><span id="32_0X20"></span><dl> <dt>**32 0x20**</dt> </dl>       | **SEL \_ Der Sensor " \_ NUM** " ist gültig.<br/>   |
| <span id="64_0x40"></span><span id="64_0X40"></span><dl> <dt>**64 0x40**</dt> </dl>       | **SEL \_ Das \_ Ereignis** Verzeichnis ist gültig.<br/>    |
| <span id="128_0x80"></span><span id="128_0X80"></span><dl> <dt>**128 0x80**</dt> </dl>    | **SEL \_ Das Ereignis \_ data1** ist gültig.<br/>  |
| <span id="256_0x100"></span><span id="256_0X100"></span><dl> <dt>**256 0x100**</dt> </dl> | **SEL \_ Das Ereignis \_ data2** ist gültig.<br/>  |
| <span id="512_0x200"></span><span id="512_0X200"></span><dl> <dt>**512 0x200**</dt> </dl> | **SEL \_ Das Ereignis \_ data3** ist gültig.<br/>  |



 

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **msmcaevent \_ systemeventerror** -Klasse wird von [**wmievent**](wmievent.md)abgeleitet.

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

 

