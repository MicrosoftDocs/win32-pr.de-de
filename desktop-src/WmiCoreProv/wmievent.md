---
description: Die wmievent-Klasse ist eine Basisklasse, von der alle WMI-Ereignis Klassen abgeleitet werden.
ms.assetid: 0393d3fc-7566-4eda-940e-248d622a903a
title: Wmievent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WMIEvent
- WMIEvent.SECURITY_DESCRIPTOR
- WMIEvent.TIME_CREATED
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 99f6804ef1dad4f37bd2727da2e91e801fb0ece2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050346"
---
# <a name="wmievent-class"></a>Wmievent-Klasse

Die **wmievent** -Klasse ist eine Basisklasse, von der alle WMI-Ereignis Klassen abgeleitet werden.

Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
[]
class WMIEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Member

Die **wmievent** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **wmievent** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Sicherheits \_ Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Deskriptor, der vom Ereignis Anbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können. Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](/windows/desktop/WmiSdk/--event)geerbt. Weitere Informationen zu Konstanten, die verwendet werden, um diese Sicherheits Beschreibung festzulegen, finden Sie unter [WMI-Sicherheits Konstanten](/windows/desktop/WmiSdk/wmi-security-constants).

</dd> <dt>

**\_Erstellungszeit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eindeutiger Wert, der die Uhrzeit angibt, zu der das Ereignis generiert wurde. Dies ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Intervalle nach dem 1. Januar 1601 darstellt. Die Informationen liegen im UTC-Format (koordiniert Universal Times) vor. Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](/windows/desktop/WmiSdk/--event)geerbt.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **wmievent** -Klasse wird von [**\_ \_ ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent)abgeleitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003<br/>                                                                                                                        |
| Namespace<br/>                | WMI-Stammdatei \\<br/>                                                                                                                                  |
| MOF<br/>                      | <dl> <dt>WMI. MOF; </dt> <dt>WMI Core. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl>                                                                |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MSMCA-Klassen](msmca-classes.md)
</dt> <dt>

[**\_\_ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> </dl>

 

