---
description: Gibt einen plattformspezifischen Fehler der Computerüberprüfungsarchitektur (Machine Check Architecture, MCA) an. Diese Klasse ist nur in 64-Bit-Systemen Windows verfügbar.
ms.assetid: 409641d5-3451-4d26-88d1-bfd0e55db257
title: MSMCAEvent_PlatformSpecificError-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_PlatformSpecificError
- MSMCAEvent_PlatformSpecificError.Active
- MSMCAEvent_PlatformSpecificError.AdditionalErrors
- MSMCAEvent_PlatformSpecificError.Cpu
- MSMCAEvent_PlatformSpecificError.ErrorSeverity
- MSMCAEvent_PlatformSpecificError.InstanceName
- MSMCAEvent_PlatformSpecificError.OEM_COMPONENT_ID
- MSMCAEvent_PlatformSpecificError.PLATFORM_BUS_SPECIFIC_DATA
- MSMCAEvent_PlatformSpecificError.PLATFORM_ERROR_STATUS
- MSMCAEvent_PlatformSpecificError.PLATFORM_REQUESTOR_ID
- MSMCAEvent_PlatformSpecificError.PLATFORM_RESPONDER_ID
- MSMCAEvent_PlatformSpecificError.PLATFORM_TARGET_ID
- MSMCAEvent_PlatformSpecificError.RawRecord
- MSMCAEvent_PlatformSpecificError.RecordId
- MSMCAEvent_PlatformSpecificError.Size
- MSMCAEvent_PlatformSpecificError.Type
- MSMCAEvent_PlatformSpecificError.VALIDATION_BITS
- MSMCAEvent_PlatformSpecificError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 0f85a0828b46826566c406d90b851cec3bbe39ee07a1456065e93542edcda35c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120970"
---
# <a name="msmcaevent_platformspecificerror-class"></a>MSMCAEvent \_ PlatformSpecificError-Klasse

Die **MSMCAEvent \_ PlatformSpecificError-Klasse** weist auf einen plattformspezifischen Fehler der Computerprüfungsarchitektur (Machine Check Architecture, MCA) hin. Diese Klasse ist nur in 64-Bit-Systemen Windows verfügbar.

Die folgende Syntax wird durch Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
class MSMCAEvent_PlatformSpecificError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   OEM_COMPONENT_ID;
  uint64  PLATFORM_BUS_SPECIFIC_DATA;
  uint64  PLATFORM_ERROR_STATUS;
  uint64  PLATFORM_REQUESTOR_ID;
  uint64  PLATFORM_RESPONDER_ID;
  uint64  PLATFORM_TARGET_ID;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a>Member

Die **MSMCAEvent \_ PlatformSpecificError-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSMCAEvent \_ PlatformSpecificError-Klasse** verfügt über diese Eigenschaften.

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

Anzahl zusätzlicher Fehler im Datensatz.

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

Datentyp: **string**
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

Bei 0 (null) wird dieses Ereignis nicht im Systemereignisprotokoll protokolliert.

</dd> <dt>

**\_ \_ OEM-KOMPONENTEN-ID**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eindeutiger Bezeichner der Komponente, die den Fehler meldet.

</dd> <dt>

**\_ \_ PLATTFORMBUSSPEZIFISCHE \_ DATEN**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

OEM-spezifische, busabhängige Daten.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

</dd> <dt>

**\_ \_ PLATTFORMFEHLERSTATUS**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Fehlerstatus der generischen Plattform.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

</dd> <dt>

**PLATFORM \_ REQUESTOR ID (PLATTFORMANFORDERUNGS-ID) \_**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

An anfordernder Bezeichner zum Zeitpunkt des Ereignisses.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

</dd> <dt>

**\_PLATTFORM-RESPONDER-ID \_**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Bezeichner des Antworters zum Zeitpunkt des Ereignisses.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

</dd> <dt>

**\_ \_ PLATTFORMZIEL-ID**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zielbezeichner zum Zeitpunkt des Ereignisses.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

</dd> <dt>

**RawRecord**
</dt> <dd> <dl> <dt>

Datentyp: **uint8 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Bytearray, das den Unformatierungsfehlerdatensatz enthält, der Windows der Systemabstraktionsschicht (SAL) angezeigt wird. Die Anzahl der Elemente im Array wird von der **Size-Eigenschaft** angegeben.

</dd> <dt>

**Recordid**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Datensatzbezeichner des Fehlerdatensatz für diesen Fehler.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

</dd> <dt>

**Größe**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Größe des unformatten Fehlerdatensatz.

</dd> <dt>

**Typ**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Typ der Ereignisprotokollmeldung. Diese Nachrichten entsprechen den Ereignisprotokoll-Nachrichtencodes, die zum Einfügen von Ereignisprotokollmeldungen durch den Windows-Ereignisprotokoll-Consumeranbieter verwendet werden, wenn er eines der Ereignisse empfängt.

</dd> <dt>

**\_VALIDIERUNGSBITS**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Validierungsbits, die verwendet werden, um die Gültigkeit der nachfolgenden Felder anzugeben.



| Wert                                                                                                                                         | Bedeutung                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="1_0x1"></span><span id="1_0X1"></span><dl> <dt>**1 0x1**</dt> </dl>          | **PLATTFORM \_ ERROR \_ STATUS** ist gültig.<br/>            |
| <span id="2_0x2"></span><span id="2_0X2"></span><dl> <dt>**2 0x2**</dt> </dl>          | **PLATTFORM \_ ERROR \_ REQUESTOR \_ ID** ist gültig.<br/>     |
| <span id="4_0x4"></span><span id="4_0X4"></span><dl> <dt>**4 0x4**</dt> </dl>          | **PLATTFORM \_ DIE \_ ERROR \_ RESPONDER-ID** ist gültig.<br/>     |
| <span id="8_0x8"></span><span id="8_0X8"></span><dl> <dt>**8 0x8**</dt> </dl>          | **PLATTFORM \_ \_ \_ FEHLERZIEL-ID** ist gültig.<br/>        |
| <span id="16_0x10"></span><span id="16_0X10"></span><dl> <dt>**16 0x10**</dt> </dl>    | **PLATTFORM \_ ERROR \_ SPECIFIC \_ DATA** ist gültig.<br/>    |
| <span id="32_0x20"></span><span id="32_0X20"></span><dl> <dt>**32 0x20**</dt> </dl>    | **PLATTFORM \_ FEHLER \_ \_ OEM-ID** ist gültig.<br/>           |
| <span id="64_0x40"></span><span id="64_0X40"></span><dl> <dt>**64 0x40**</dt> </dl>    | **PLATTFORM \_ FEHLER: \_ OEM \_ DATA \_ STRUCT** ist gültig.<br/> |
| <span id="128_0x80"></span><span id="128_0X80"></span><dl> <dt>**128 0x80**</dt> </dl> | **PLATTFORM \_ FEHLER: \_ OEM \_ DEVICE \_ PATH** ist gültig.<br/> |



 

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **MSMCAEvent \_ PlatformSpecificError-Klasse** wird von [**WMIEvent abgeleitet.**](wmievent.md)

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

 

