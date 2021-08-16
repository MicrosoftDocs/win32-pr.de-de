---
description: Meldet ein Instanzlöschereignis, bei dem es sich um einen Typ systeminterner Ereignisse handelt, der generiert wird, wenn eine Instanz aus dem Namespace gelöscht wird.
ms.assetid: a370fc95-15e3-49c3-98de-2f40d742f207
ms.tgt_platform: multiple
title: __InstanceDeletionEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceDeletionEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: a210f67e7e71d9980a3eeb88ae54fad7fee3ec62597b81ae7253a2893a437a7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320884"
---
# <a name="__instancedeletionevent-class"></a>\_\_InstanceDeletionEvent-Klasse

Die **\_ \_ InstanceDeletionEvent-Systemklasse** meldet ein Instanzlöschereignis, [](determining-the-type-of-event-to-receive.md) bei dem es sich um einen Typ systeminterner Ereignisse handelt, der generiert wird, wenn eine Instanz aus dem Namespace gelöscht wird.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
class __InstanceDeletionEvent : __InstanceOperationEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Member

Die **\_ \_ InstanceDeletionEvent-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ InstanceDeletionEvent-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**\_SICHERHEITSDESKRIPTOR**
</dt> <dd> <dl> <dt>

Datentyp: **uint8 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Deskriptor, der vom Ereignisanbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können. Diese Eigenschaft wird vom Ereignis [**\_ \_ geerbt.**](--event.md)

</dd> <dt>

**TargetInstance**
</dt> <dd> <dl> <dt>

Datentyp: **Objekt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Kopie der Instanz, die gelöscht wurde. Diese Eigenschaft wird von [**\_ \_ InstanceOperationEvent geerbt.**](--instanceoperationevent.md)

</dd> <dt>

**ZEIT \_ ERSTELLT**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eindeutiger Wert, der den Zeitpunkt angibt, zu dem das Ereignis generiert wurde. Dies ist ein 64-Bit-Wert, der die Anzahl von 100-Nanosekunden-Intervallen nach dem 1. Januar 1601 darstellt. Die Informationen haben das format koordinierte Weltzeit (UTC). Diese Eigenschaft wird vom Ereignis [**\_ \_ geerbt.**](--event.md)

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **\_ \_ InstanceDeletionEvent-Klasse** wird von [**\_ \_ InstanceOperationEvent abgeleitet.**](--instanceoperationevent.md)

**Löschen einer Ressource: \_ \_ InstanceDeletionEvent**

Wenn Sie sicherstellen möchten, dass ein bestimmtes Antivirenprogramm weiterhin auf einem Computer ausgeführt wird, können Sie ein Skript schreiben, das die Prozesse auf dem Computer überwacht, um zu ermitteln, ob eines dieser Programme anhält.

Benachrichtigungsabfragen, die eine Benachrichtigung über das Löschen einer Ressource anfordern und systeminterne Ereignisse verwenden, verwenden eine Syntax ähnlich der folgenden:

`SELECT * FROM __InstanceDeletionEvent WHERE TargetInstance ISA 'Win32_Process' and TargetInstance.Name = 'notepad.exe' `

## <a name="examples"></a>Beispiele

Das [](https://Gallery.TechNet.Microsoft.Com/060a9adb-f99b-4f34-ba65-19b5f5815a38) VBScript-Codebeispiel zum Überwachen des Prozesslöschereignisses im TechNet-Katalog verwendet **\_ \_ InstanceDeletionEvent,** um das erste Vorkommen eines Löschereignisses einer WMI-Instanz für [**den Win32-Prozess \_ zu überwachen.**](/windows/desktop/CIMWin32Prov/win32-process)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_\_InstanceOperationEvent**](/windows/desktop/WmiSdk/--instanceoperationevent)
</dt> <dt>

[WMI-Systemklassen](wmi-system-classes.md)
</dt> </dl>

 

