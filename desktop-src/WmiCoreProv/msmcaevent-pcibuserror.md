---
description: Stellt einen MCA-PCI-Busfehler (Machine Check Architecture) dar. Diese Klasse ist nur für Computer verfügbar, die auf einem 64-Bit-Windows Betriebssystem ausgeführt werden.
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
ms.openlocfilehash: 4b3ae66c684ab6a0e2573e2c82d6087a3405ce3d8bef5704bb392337699daaea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051278"
---
# <a name="msmcaevent_pcibuserror-class"></a>MSMCAEvent \_ PCIBusError-Klasse

Die **MSMCAEvent \_ PCIBusError-Klasse** stellt einen MCA-PCI-Busfehler (Machine Check Architecture) dar. Diese Klasse ist nur für Computer verfügbar, die auf einem 64-Bit-Windows Betriebssystem ausgeführt werden.

Die folgende Syntax wird aus Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge sortiert.

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

Die **MSMCAEvent \_ PCIBusError-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSMCAEvent \_ PCIBusError-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Aktiv**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**TRUE**, wenn diese Instanz der -Klasse aktiv ist; Andernfalls **FALSE**.

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

CPU, die den Fehler gemeldet hat. Diese Eigenschaft gilt nur für ein Multiprozessorsystem, in dem dem ersten Prozessor die Zahl 0, dem zweiten Prozessor die Zahl 1 usw. zugewiesen wird.

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

Wenn 0 (null) ist, wird dieses Ereignis nicht im Systemereignisprotokoll protokolliert.

</dd> <dt>

**\_ \_ PCI-BUSADRESSE**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Arbeitsspeicher- oder E/A-Adresse im PCI-Bus zum Zeitpunkt des Ereignisses.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

</dd> <dt>

**\_ \_ PCI-BUS-CMD**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Busbefehl oder -vorgang zum Zeitpunkt des Ereignisses.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

</dd> <dt>

**\_ \_ PCI-BUSDATEN**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Daten im PCI-Bus zum Zeitpunkt des Ereignisses.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

</dd> <dt>

**\_ \_ PCI-BUS-FEHLERSTATUS \_**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Busstatus zum Zeitpunkt des Fehlers.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

</dd> <dt>

**\_ \_ PCI-BUSFEHLERTYP \_**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Typ des PCI-Busfehlers.



| Wert                                                                                                | Bedeutung                                                     |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Unbekannter oder OEM-systemspezifischer Fehler.<br/>            |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Datenparitätsfehler.<br/>                               |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Systemfehler.<br/>                                    |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Masterabbruch.<br/>                                    |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Bustime out or No Device Present (NO DEVSEL ) (Bustime out or No Device Present (KEIN \# DEVSEL))<br/> |
| <span id="5"></span><dl> <dt>**5**</dt> </dl> | MasterDatenparitätsfehler.<br/>                        |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | Adressparitätsfehler.<br/>                            |
| <span id="7"></span><dl> <dt>**7**</dt> </dl> | Befehlsparitätsfehler.<br/>                            |



 

</dd> <dt>

**PCI \_ BUS \_ ID \_ BusNumber**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der angegebene Bezeichner für den PCI-Bus, bei dem der Fehler aufgetreten ist.

</dd> <dt>

**PCI \_ BUS \_ ID \_ SegmentNumber**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der angegebene Segmentbezeichner für den PCI-Bus, bei dem der Fehler aufgetreten ist.

</dd> <dt>

**\_ \_ PCI-BUS-ANFORDERER-ID \_**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

PCI-Bus-Anfordererbezeichner zum Zeitpunkt des Ereignisses.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

</dd> <dt>

**\_ \_ \_ PCI-BUS-ANTWORTER-ID**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

PCI-Busantworterbezeichner zum Zeitpunkt des Ereignisses.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

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

**Größe**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Größe des unformatierten Fehlerdatensatzes.

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

Validierungsbits, die verwendet werden, um die Gültigkeit der nachfolgenden Felder anzugeben.



| Werte                                                                                  | Bedeutung                                          |
|-----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>1 (0x1)</dt> </dl>      | DER \_ \_ PCI-BUS-FEHLERSTATUS \_ ist gültig.<br/>     |
| <dl> <dt>2 (0x2)</dt> </dl>      | PCI \_ BUS ERROR TYPE ist \_ \_ gültig.<br/>       |
| <dl> <dt>4 (0x4)</dt> </dl>      | DIE \_ PCI-BUS-ID \_ ist gültig.<br/>                |
| <dl> <dt>8 (0x8)</dt> </dl>      | PCI \_ BUS ADDRESS ist \_ gültig.<br/>           |
| <dl> <dt>16 (0x10)</dt> </dl>    | PCI \_ BUS DATA ist \_ gültig.<br/>              |
| <dl> <dt>32 (0x20)</dt> </dl>    | PCI \_ BUS \_ CMD ist gültig.<br/>               |
| <dl> <dt>64 (0x40)</dt> </dl>    | Die PCI \_ BUS \_ \_ REQUESTOR-ID ist gültig.<br/>     |
| <dl> <dt>128 (0x80)</dt> </dl>   | DIE PCI \_ BUS \_ \_ RESPONDER-ID ist gültig.<br/>     |
| <dl> <dt>256 (0x100)</dt> </dl>  | DIE PCI \_ \_ BUS-ZIEL-ID \_ ist gültig.<br/>        |
| <dl> <dt>512 (0x200)</dt> </dl>  | DIE \_ \_ PCI-BUS-OEM-ID \_ ist gültig.<br/>           |
| <dl> <dt>1024 (0x400)</dt> </dl> | DIE \_ \_ PCI-BUS-OEM-DATENSTRUKTUR \_ \_ ist gültig.<br/> |



 

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **MSMCAEvent \_ PCIBusError-Klasse** wird von [**WMIEvent**](wmievent.md)abgeleitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003<br/>                                                         |
| Namespace<br/>                | Root \\ wmi<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Wmicore.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wmiprov.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[MSMCA-Klassen](msmca-classes.md)
</dt> <dt>

[**WMIEvent**](wmievent.md)
</dt> </dl>

 

