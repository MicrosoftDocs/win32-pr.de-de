---
description: Stellt den allgemeinen Header dar, der von allen msmcaevent-Klassen verwendet wird. Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.
ms.assetid: ff20522c-f805-47dc-bef2-4176211de698
title: MSMCAEvent_Header-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_Header
- MSMCAEvent_Header.AdditionalErrors
- MSMCAEvent_Header.Cpu
- MSMCAEvent_Header.ErrorSeverity
- MSMCAEvent_Header.RecordId
- MSMCAEvent_Header.Type
- MSMCAEvent_Header.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 426f943014f3b6cfbdba5a25d331c0ea621048cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352228"
---
# <a name="msmcaevent_header-class"></a>Msmcaevent- \_ Header Klasse

Die **msmcaevent- \_ Header** Klasse stellt den allgemeinen Header dar, der von allen [MSMCA-Klassen](msmca-classes.md) verwendet wird. Die Header Dateien werden verwendet, sodass C-und C++-Code über eine Datenstruktur verfügen können, die den allgemeinen Header für alle Ereignisse beschreibt. Diese Klasse ist für die interne Verwendung reserviert. Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.

Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
class MSMCAEvent_Header
{
  uint32 AdditionalErrors;
  uint32 Cpu;
  uint8  ErrorSeverity;
  uint64 RecordId;
  uint32 Type;
  uint32 LogToEventlog;
};
```

## <a name="members"></a>Member

Die **msmcaevent- \_ Header** Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **msmcaevent- \_ Header** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Additionalerrors**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl zusätzlicher Fehler im MCA-Datensatz.

</dd> <dt>

**CPU**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

CPU, die den Fehler meldet. Diese Eigenschaft gilt nur für ein Multiprozessorsystem, dem dem ersten Prozessor die Zahl 0 zugewiesen ist, dem zweiten Prozessor die Zahl 1 zugewiesen wird usw.

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

**Logtoeventlog**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Wenn 0 (null) ist, wird dieses Ereignis nicht im System Ereignisprotokoll protokolliert.

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

**Type**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Typ der Ereignisprotokoll Meldung. Diese Meldungen entsprechen den Ereignisprotokoll-Nachrichten Codes, die zum Einfügen von Ereignisprotokoll Meldungen vom Windows-Ereignisprotokoll-Consumeranbieter verwendet werden, wenn ein Ereignis empfangen wird.

</dd> </dl>

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

[WMI-C++-Klassen](/windows/desktop/WmiSdk/wmi-c-classes)
</dt> </dl>

 

