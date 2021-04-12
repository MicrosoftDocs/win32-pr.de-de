---
description: Gibt einen MCA-System-BIOS-Fehler (Machine Check Architecture) an. Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.
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
ms.openlocfilehash: 709d480e8865c5d5bde2a9f5e8de45f138e66548
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217611"
---
# <a name="msmcaevent_smbioserror-class"></a>Msmcaevent \_ smbioserror-Klasse

Die **msmcaevent \_ smbioserror** -Klasse gibt einen MCA-System-BIOS-Fehler (Machine Check Architecture) an. Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.

Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.

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

Die **msmcaevent \_ smbioserror** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **msmcaevent \_ smbioserror** -Klasse verfügt über diese Eigenschaften.

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

**Größe**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Größe des unformatierten Fehler Datensatzes.

</dd> <dt>

**SMBIOS \_ - \_ Ereignistyp**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Ereignistyp.



| Wert                                                                                                  | Bedeutung                                                                                                                     |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl>   | Reserviert.<br/>                                                                                                        |
| <span id="1"></span><dl> <dt>**1**</dt> </dl>   | Single-Bit-ECC-Speicherfehler.<br/>                                                                                     |
| <span id="2"></span><dl> <dt>**2**</dt> </dl>   | Multibit-ECC-Speicherfehler.<br/>                                                                                   |
| <span id="3"></span><dl> <dt>**3**</dt> </dl>   | Fehler bei Paritäts Arbeitsspeicher.<br/>                                                                                             |
| <span id="4"></span><dl> <dt>**4**</dt> </dl>   | Bustimeout.<br/>                                                                                                    |
| <span id="5"></span><dl> <dt>**5**</dt> </dl>   | Überprüfung des e/a-Kanals.<br/>                                                                                               |
| <span id="6"></span><dl> <dt>**6**</dt> </dl>   | Software-NMI.<br/>                                                                                                    |
| <span id="7"></span><dl> <dt>**7**</dt> </dl>   | Größe des Arbeitsspeichers nach dem Arbeitsspeicher<br/>                                                                                              |
| <span id="8"></span><dl> <dt>**8**</dt> </dl>   | Fehler nach dem Fehler.<br/>                                                                                                      |
| <span id="9"></span><dl> <dt>**9**</dt> </dl>   | PCI-Paritätsfehler.<br/>                                                                                                |
| <span id="10"></span><dl> <dt>**10**</dt> </dl> | PCI-System Fehler.<br/>                                                                                                |
| <span id="11"></span><dl> <dt>**11:**</dt> </dl> | CPU-Fehler.<br/>                                                                                                     |
| <span id="12"></span><dl> <dt>**12.12.2016**</dt> </dl> | Timeout des EISA-Failsafe-Timers.<br/>                                                                                    |
| <span id="13"></span><dl> <dt>**13**</dt> </dl> | Das korrigierbare Speicher Protokoll ist deaktiviert.<br/>                                                                                 |
| <span id="14"></span><dl> <dt>**14**</dt> </dl> | Die Protokollierung für einen bestimmten Ereignistyp ist deaktiviert. In kurzer Zeit wurden zu viele Fehler desselben Typs empfangen.<br/> |
| <span id="15"></span><dl> <dt>**17.15**</dt> </dl> | Reserviert.<br/>                                                                                                        |
| <span id="16"></span><dl> <dt>**Uhr**</dt> </dl> | Das System Limit wurde überschritten (z. b. Spannung oder Temperaturschwellen Wert überschritten).<br/>                                  |
| <span id="17"></span><dl> <dt>**Uhr**</dt> </dl> | Der asynchrone Hardware-Timer ist abgelaufen und hat eine System Zurücksetzung ausgegeben.<br/>                                                   |
| <span id="18"></span><dl> <dt>**Jahren**</dt> </dl> | System Konfigurationsinformationen.<br/>                                                                                |
| <span id="19"></span><dl> <dt>**19.07.2016**</dt> </dl> | Festplatten Informationen.<br/>                                                                                           |
| <span id="20"></span><dl> <dt>**20**</dt> </dl> | Das System wurde neu konfiguriert.<br/>                                                                                             |
| <span id="21"></span><dl> <dt>**21**</dt> </dl> | Nicht korrigierbare CPU-komplexer Fehler.<br/>                                                                                 |
| <span id="22"></span><dl> <dt>**22**</dt> </dl> | Der Protokollbereich wurde zurückgesetzt oder gelöscht.<br/>                                                                                       |
| <span id="23"></span><dl> <dt>**23**</dt> </dl> | System Start. Bei Implementierung ist dieser Protokolleintrag garantiert der erste, der bei jedem Systemstart geschrieben wird.<br/>        |



 

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

Validierungs Bits zum Angeben der Gültigkeit der nachfolgenden Felder. Der Wert 1 (0x1) bedeutet, dass das **SMBIOS- \_ Ereignis** gültig ist.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **msmcaevent \_ smbioserror** -Klasse wird von [**wmievent**](wmievent.md)abgeleitet.

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

 

