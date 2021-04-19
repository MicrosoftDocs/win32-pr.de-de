---
description: Enthält ein korrigiertes Computer Überprüfung-Ereignis (CMC). Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.
ms.assetid: e12efbf7-7d53-415a-bc48-90d33e4ce16d
title: MSMCAInfo_RawCMCEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo_RawCMCEvent
- MSMCAInfo_RawCMCEvent.Active
- MSMCAInfo_RawCMCEvent.Count
- MSMCAInfo_RawCMCEvent.InstanceName
- MSMCAInfo_RawCMCEvent.Records
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 1bb60d5fbcf004b924a91e640d8cd8a8c5ad3c25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352254"
---
# <a name="msmcainfo_rawcmcevent-class"></a>Msmcainfo \_ rawcmcevent-Klasse

Die **msmcainfo \_ rawcmcevent** -Klasse enthält ein "korrigiertes Computer Überprüfung (CMC)"-Ereignis. Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.

Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
class MSMCAInfo_RawCMCEvent : WMIEvent
{
  boolean         Active;
  uint32          Count;
  string          InstanceName;
  MSMCAInfo_Entry Records[];
};
```

## <a name="members"></a>Member

Die **msmcainfo \_ rawcmcevent** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **msmcainfo \_ rawcmcevent** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Aktiv**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

TRUE, wenn diese Instanz der-Klasse aktiv ist. andernfalls **false**.

</dd> <dt>

**Count**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl der Fehler Datensätze.

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

**Datensätze**
</dt> <dd> <dl> <dt>

Datentyp: **msmcainfo- \_ Eingabe** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Array von MCA-Fehler Datensätzen (Machine Check Architecture). Die Anzahl der MCA-Fehler Datensätze im Array wird durch die **count** -Eigenschaft angegeben.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **msmcainfo \_ rawcmcevent** -Klasse wird von [**wmievent**](wmievent.md)abgeleitet.

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

 

