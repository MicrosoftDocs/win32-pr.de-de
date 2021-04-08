---
description: Stellt einen PCI-Busfehler (Machine Check Architecture, MCA) dar. Diese Klasse ist nur für Computer verfügbar, die auf einem 64-Bit-Windows-Betriebssystem ausgeführt werden.
ms.assetid: d8995909-a91b-4fcc-a37f-011d8df95ce8
title: MSMCAEvent_PCIBusError-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_PCIBusError
- MSMCAEvent_PCIBusError.Active
- MSMCAEvent_PCIBusError.AdditionalErrors
- MSMCAEvent_PCIBusError.Cpu
- MSMCAEvent_PCIBusError.ErrorSeverity
- MSMCAEvent_PCIBusError.InstanceName
- MSMCAEvent_PCIBusError.PCI_BUS_ADDRESS
- MSMCAEvent_PCIBusError.PCI_BUS_CMD
- MSMCAEvent_PCIBusError.PCI_BUS_DATA
- MSMCAEvent_PCIBusError.PCI_BUS_ERROR_STATUS
- MSMCAEvent_PCIBusError.PCI_BUS_ERROR_TYPE
- MSMCAEvent_PCIBusError.PCI_BUS_ID_BusNumber
- MSMCAEvent_PCIBusError.PCI_BUS_ID_SegmentNumber
- MSMCAEvent_PCIBusError.PCI_BUS_REQUESTOR_ID
- MSMCAEvent_PCIBusError.PCI_BUS_RESPONDER_ID
- MSMCAEvent_PCIBusError.RawRecord
- MSMCAEvent_PCIBusError.RecordId
- MSMCAEvent_PCIBusError.Size
- MSMCAEvent_PCIBusError.Type
- MSMCAEvent_PCIBusError.VALIDATION_BITS
- MSMCAEvent_PCIBusError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 7f2b800a07c0b979468a5df5a8be67e6adee39de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751384"
---
# <a name="msmcaevent_pcibuserror-class"></a>Msmcaevent \_ pcibuserror-Klasse

Die **msmcaevent \_ pcibuserror** -Klasse stellt eine MCA-PCI-Busfehler (Machine Check Architecture) dar. Diese Klasse ist nur für Computer verfügbar, die auf einem 64-Bit-Windows-Betriebssystem ausgeführt werden.

Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
class MSMCAEvent_PCIBusError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint64  PCI_BUS_ADDRESS;
  uint64  PCI_BUS_CMD;
  uint64  PCI_BUS_DATA;
  uint64  PCI_BUS_ERROR_STATUS;
  uint16  PCI_BUS_ERROR_TYPE;
  uint8   PCI_BUS_ID_BusNumber;
  uint8   PCI_BUS_ID_SegmentNumber;
  uint64  PCI_BUS_REQUESTOR_ID;
  uint64  PCI_BUS_RESPONDER_ID;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a>Member

Die **msmcaevent \_ pcibuserror** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **msmcaevent \_ pcibuserror** -Klasse verfügt über diese Eigenschaften.

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

**PCI \_ - \_ Busadresse**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Arbeitsspeicher oder e/a-Adresse auf dem PCI-Bus zum Zeitpunkt des Ereignisses.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**PCI- \_ Bus- \_ cmd**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Bus Befehl oder-Vorgang zum Zeitpunkt des Ereignisses.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**PCI \_ - \_ Busdaten**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Daten auf dem PCI-Bus zum Zeitpunkt des Ereignisses.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**PCI \_ - \_ \_ busfehlerstatus**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Busstatus zum Zeitpunkt des Fehlers.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**PCI \_ - \_ \_ busfehlertyp**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Typ des PCI-Busfehlers.



| Wert                                                                                                | Bedeutung                                                     |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Unbekannter oder OEM-System spezifischer Fehler.<br/>            |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Daten Paritätsfehler.<br/>                               |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | System Fehler.<br/>                                    |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Master Abbruch.<br/>                                    |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Bustimeout oder kein Gerät vorhanden (keine devsel \# ).<br/> |
| <span id="5"></span><dl> <dt>**5**</dt> </dl> | Fehler bei der Master Daten Parität.<br/>                        |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | Adress Paritätsfehler.<br/>                            |
| <span id="7"></span><dl> <dt>**7**</dt> </dl> | Befehls Paritätsfehler.<br/>                            |



 

</dd> <dt>

**PCI- \_ Bus- \_ ID \_ Busnummer**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der angegebene Bezeichner für den PCI-Bus, der den Fehler gefunden hat.

</dd> <dt>

**PCI- \_ Bus- \_ ID \_ segmentnumber**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der angegebene Segment Bezeichner für den PCI-Bus, der den Fehler festgelegt hat.

</dd> <dt>

**PCI- \_ Bus- \_ \_ RequestId-ID**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der PCI-Bus-Anforderer Bezeichner zum Zeitpunkt des Ereignisses.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**PCI- \_ Bus- \_ Responder- \_ ID**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der PCI-Bus-Responder-Bezeichner zum Zeitpunkt des Ereignisses.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

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



| Werte                                                                                  | Bedeutung                                          |
|-----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>1 (0x1)</dt> </dl>      | Der Status des PCI- \_ \_ Busfehlers \_ ist gültig.<br/>     |
| <dl> <dt>2 (0x2)</dt> </dl>      | Der PCI- \_ \_ \_ busfehlertyp ist gültig.<br/>       |
| <dl> <dt>4 (0x4)</dt> </dl>      | Die PCI- \_ Bus- \_ ID ist gültig.<br/>                |
| <dl> <dt>8 (0x8)</dt> </dl>      | Die PCI- \_ \_ Busadresse ist gültig.<br/>           |
| <dl> <dt>16 (0x10)</dt> </dl>    | PCI \_ - \_ Busdaten sind gültig.<br/>              |
| <dl> <dt>32 (0x20)</dt> </dl>    | Der PCI- \_ Bus- \_ cmd ist gültig.<br/>               |
| <dl> <dt>64 (0x40)</dt> </dl>    | Die PCI- \_ \_ busrequestid \_ ist gültig.<br/>     |
| <dl> <dt>128 (0x80)</dt> </dl>   | Die PCI- \_ Bus- \_ Responder- \_ ID ist gültig.<br/>     |
| <dl> <dt>256 (0x100)</dt> </dl>  | Die PCI- \_ \_ busziel- \_ ID ist gültig.<br/>        |
| <dl> <dt>512 (0x200)</dt> </dl>  | Die OEM-ID des PCI- \_ Busses \_ \_ ist gültig.<br/>           |
| <dl> <dt>1024 (0x400)</dt> </dl> | Die \_ OEM-Datenstruktur des PCI-Busses \_ \_ \_ ist gültig.<br/> |



 

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **msmcaevent \_ pcibuserror** -Klasse wird von [**wmievent**](wmievent.md)abgeleitet.

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

 

