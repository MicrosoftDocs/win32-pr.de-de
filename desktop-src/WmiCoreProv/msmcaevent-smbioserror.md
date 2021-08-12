---
description: Gibt einen SYSTEM-BIOS-Fehler (Machine Check Architecture, MCA) an. Diese Klasse ist nur in 64-Bit-Systemen Windows verfügbar.
ms.assetid: b451ca45-6208-4445-b9f1-b4e3174837a4
title: MSMCAEvent_SMBIOSError-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_SMBIOSError
- MSMCAEvent_SMBIOSError.Active
- MSMCAEvent_SMBIOSError.AdditionalErrors
- MSMCAEvent_SMBIOSError.Cpu
- MSMCAEvent_SMBIOSError.ErrorSeverity
- MSMCAEvent_SMBIOSError.InstanceName
- MSMCAEvent_SMBIOSError.RawRecord
- MSMCAEvent_SMBIOSError.RecordId
- MSMCAEvent_SMBIOSError.Size
- MSMCAEvent_SMBIOSError.SMBIOS_EVENT_TYPE
- MSMCAEvent_SMBIOSError.Type
- MSMCAEvent_SMBIOSError.VALIDATION_BITS
- MSMCAEvent_SMBIOSError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: fccb38a73585db71c6418929a35458f26b9749159e537de47a298d920b318e08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118558395"
---
# <a name="msmcaevent_smbioserror-class"></a>MSMCAEvent \_ SMBIOSError-Klasse

Die **MSMCAEvent \_ SMBIOSError-Klasse** weist auf einen BIOS-Systemfehler der Computerprüfungsarchitektur (Machine Check Architecture, MCA) hin. Diese Klasse ist nur in 64-Bit-Systemen Windows verfügbar.

Die folgende Syntax wird durch Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
class MSMCAEvent_SMBIOSError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint8   SMBIOS_EVENT_TYPE;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a>Member

Die **MSMCAEvent \_ SMBIOSError-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSMCAEvent \_ SMBIOSError-Klasse** verfügt über diese Eigenschaften.

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

**RawRecord**
</dt> <dd> <dl> <dt>

Datentyp: **uint8 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Bytearray, das den unformatten Fehlerdatensatz enthält. Die Anzahl der Elemente im Array, die von der **Size-Eigenschaft** angegeben werden.

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

**\_SMBIOS-EREIGNISTYP \_**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Ereignistyp.



| Wert                                                                                                  | Bedeutung                                                                                                                     |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl>   | Reserviert.<br/>                                                                                                        |
| <span id="1"></span><dl> <dt>**1**</dt> </dl>   | ECC-Arbeitsspeicherfehler mit einzelnem Bit.<br/>                                                                                     |
| <span id="2"></span><dl> <dt>**2**</dt> </dl>   | ECC-Arbeitsspeicherfehler mit mehreren Bit.<br/>                                                                                   |
| <span id="3"></span><dl> <dt>**3**</dt> </dl>   | Paritätsspeicherfehler.<br/>                                                                                             |
| <span id="4"></span><dl> <dt>**4**</dt> </dl>   | Bus-Time out.<br/>                                                                                                    |
| <span id="5"></span><dl> <dt>**5**</dt> </dl>   | E/A-Kanalüberprüfung.<br/>                                                                                               |
| <span id="6"></span><dl> <dt>**6**</dt> </dl>   | Software-NMI.<br/>                                                                                                    |
| <span id="7"></span><dl> <dt>**7**</dt> </dl>   | Größe des Arbeitsspeichers nach der Größenvergrößerung.<br/>                                                                                              |
| <span id="8"></span><dl> <dt>**8**</dt> </dl>   | POST-Fehler.<br/>                                                                                                      |
| <span id="9"></span><dl> <dt>**9**</dt> </dl>   | PCI-Paritätsfehler.<br/>                                                                                                |
| <span id="10"></span><dl> <dt>**10**</dt> </dl> | PCI-Systemfehler.<br/>                                                                                                |
| <span id="11"></span><dl> <dt>**11**</dt> </dl> | CPU-Fehler.<br/>                                                                                                     |
| <span id="12"></span><dl> <dt>**12**</dt> </dl> | TIMER-Time out für EISA Failsafe.<br/>                                                                                    |
| <span id="13"></span><dl> <dt>**13**</dt> </dl> | Korrigierende Speicherprotokoll deaktiviert.<br/>                                                                                 |
| <span id="14"></span><dl> <dt>**14**</dt> </dl> | Protokollierung für einen bestimmten Ereignistyp deaktiviert. Zu viele Fehler desselben Typs wurden in kurzer Zeit empfangen.<br/> |
| <span id="15"></span><dl> <dt>**15**</dt> </dl> | Reserviert.<br/>                                                                                                        |
| <span id="16"></span><dl> <dt>**16**</dt> </dl> | Das Systemlimit wurde überschritten (z. B. die Belastung oder der Temperaturschwellenwert überschritten).<br/>                                  |
| <span id="17"></span><dl> <dt>**17**</dt> </dl> | Der asynchrone Hardwaretimer ist abgelaufen und hat eine Systemrücksetzung ausgegeben.<br/>                                                   |
| <span id="18"></span><dl> <dt>**18**</dt> </dl> | Systemkonfigurationsinformationen.<br/>                                                                                |
| <span id="19"></span><dl> <dt>**19**</dt> </dl> | Informationen zur Festplatte.<br/>                                                                                           |
| <span id="20"></span><dl> <dt>**20**</dt> </dl> | System neu konfiguriert.<br/>                                                                                             |
| <span id="21"></span><dl> <dt>**21**</dt> </dl> | Unbesenkbarer CPU-komplexer Fehler.<br/>                                                                                 |
| <span id="22"></span><dl> <dt>**22**</dt> </dl> | Zurücksetzen des Protokollbereichs oder Löschen.<br/>                                                                                       |
| <span id="23"></span><dl> <dt>**23**</dt> </dl> | Systemstart. Bei Implementierung ist dieser Protokolleintrag garantiert der erste, der beim Systemstart geschrieben wurde.<br/>        |



 

</dd> <dt>

**Typ**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Typ der Ereignisprotokollmeldung. Diese Nachrichten entsprechen den Ereignisprotokollmeldungscodes, die verwendet werden, um Ereignisprotokollmeldungen vom Windows Ereignisprotokoll-Consumeranbieter einzufügen, wenn er eines der Ereignisse empfängt.

</dd> <dt>

**\_VALIDIERUNGSBITS**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Validierungsbits, die verwendet werden, um die Gültigkeit der nachfolgenden Felder anzugeben. Der Wert 1 (0x1) bedeutet, dass das **\_ SMBIOS-EREIGNIS** gültig ist.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **MSMCAEvent \_ SMBIOSError-Klasse** wird von [**WMIEvent**](wmievent.md)abgeleitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003<br/>                                                         |
| Namespace<br/>                | Root \\ wmi<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Wmicore.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wmiprov.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[MSMCA-Klassen](msmca-classes.md)
</dt> <dt>

[**WMIEvent**](wmievent.md)
</dt> </dl>

 

