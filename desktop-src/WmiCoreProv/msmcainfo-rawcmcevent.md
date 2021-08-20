---
description: Enthält ein CMC-Ereignis (Corrected Machine Check). Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.
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
ms.openlocfilehash: ef8276839d90dbd3aa731d6684055f640cb713d566dc5616093566c888b357f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118821874"
---
# <a name="msmcainfo_rawcmcevent-class"></a>MSMCAInfo \_ RawCMCEvent-Klasse

Die **MSMCAInfo \_ RawCMCEvent-Klasse** enthält ein CMC-Ereignis (Corrected Machine Check). Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.

Die folgende Syntax wird aus Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge sortiert.

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

Die **MSMCAInfo \_ RawCMCEvent-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSMCAInfo \_ RawCMCEvent-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Aktiv**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

TRUE, wenn diese Instanz der -Klasse aktiv ist; Andernfalls **FALSE**.

</dd> <dt>

**Count**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl der Fehlerdatensätze.

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

**Datensätze**
</dt> <dd> <dl> <dt>

Datentyp: **MSMCAInfo \_ Entry-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Array von MCA-Fehlerdatensätzen (Machine Check Architecture). Die Anzahl der MCA-Fehlerdatensätze im Array wird durch die **Count-Eigenschaft** angegeben.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **MSMCAInfo \_ RawCMCEvent-Klasse** wird von [**WMIEvent**](wmievent.md)abgeleitet.

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

 

