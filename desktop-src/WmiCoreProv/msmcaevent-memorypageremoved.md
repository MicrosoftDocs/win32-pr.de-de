---
description: Gibt an, dass eine Speicherseite aufgrund übermäßiger ECC-Fehler (Error Checking and Correcting) von der Systemnutzung entfernt wurde. Diese Klasse ist nur in 64-Bit-Systemen Windows verfügbar.
ms.assetid: 364a2520-8d7c-44f2-95f6-eea9a5531975
title: MSMCAEvent_MemoryPageRemoved-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_MemoryPageRemoved
- MSMCAEvent_MemoryPageRemoved.Active
- MSMCAEvent_MemoryPageRemoved.InstanceName
- MSMCAEvent_MemoryPageRemoved.PhysicalAddress
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: d8229848cf1113736e3b9a4e37cd9493b8c724c58c384387536cded4742ca3c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118558467"
---
# <a name="msmcaevent_memorypageremoved-class"></a>MSMCAEvent \_ MemoryPageRemoved-Klasse

Die **MSMCAEvent \_ MemoryPageRemoved-Klasse** gibt an, dass eine Speicherseite aufgrund übermäßiger EcC-Fehler (Error Checking and Correcting) von der Systemnutzung entfernt wurde. Diese Klasse ist nur in 64-Bit-Systemen Windows verfügbar.

Die folgende Syntax wird durch Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
class MSMCAEvent_MemoryPageRemoved : WmiEvent
{
  boolean Active;
  string  InstanceName;
  uint64  PhysicalAddress;
};
```

## <a name="members"></a>Member

Die **MSMCAEvent \_ MemoryPageRemoved-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSMCAEvent \_ MemoryPageRemoved-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Aktiv**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**TRUE**, wenn diese Instanz der -Klasse aktiv ist; **andernfalls FALSE**.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Eindeutiger Bezeichner für diese Instanz der -Klasse.

</dd> <dt>

**PhysicalAddress**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Adresse der Speicherseite, die entfernt wurde.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/previous-versions//aa393262(v=vs.85))

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **MSMCAEvent \_ MemoryPageRemoved-Klasse** wird von [**WMIEvent abgeleitet.**](wmievent.md)

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

 

