---
description: Meldet ein instanzlöschungsereignis, bei dem es sich um einen Typ eines systeminternen Ereignisses handelt, das beim Löschen einer Instanz aus dem Namespace generiert wird.
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
ms.openlocfilehash: 018bac665aa95393fc1a9c7e51ad42038e8b27c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360697"
---
# <a name="__instancedeletionevent-class"></a>\_\_Instancedeletionevent-Klasse

Die **\_ \_ instancedeletionevent** -System Klasse meldet ein instanzlöschungsereignis, bei dem es sich um einen Typ eines systeminternen [Ereignisses](determining-the-type-of-event-to-receive.md) handelt, das beim Löschen einer Instanz aus dem-Namespace generiert wird.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

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

Die **\_ \_ instancedeletionevent** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ instancedeletionevent** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Sicherheits \_ Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Deskriptor, der vom Ereignis Anbieter verwendet wird, um zu bestimmen, welche Benutzer das Ereignis empfangen können. Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.

</dd> <dt>

**TargetInstance**
</dt> <dd> <dl> <dt>

Datentyp: **Object**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Kopie der-Instanz, die gelöscht wurde. Diese Eigenschaft wird von [**\_ \_ instanceoperationevent**](--instanceoperationevent.md)geerbt.

</dd> <dt>

**\_Erstellungszeit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eindeutiger Wert, der die Uhrzeit angibt, zu der das Ereignis generiert wurde. Dies ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Intervalle nach dem 1. Januar 1601 darstellt. Die Informationen liegen im UTC-Format (koordinierte Weltzeit) vor. Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **\_ \_ instancedeletionevent** -Klasse wird von [**\_ \_ instanceoperationevent**](--instanceoperationevent.md)abgeleitet.

**Löschen einer Ressource: \_ \_ instancedeletionevent**

Wenn Sie sicherstellen möchten, dass ein bestimmtes antivirenüberprüfungs Programm weiterhin auf einem Computer ausgeführt wird, können Sie ein Skript schreiben, mit dem die Prozesse auf dem Computer überwacht werden, um zu bestimmen, ob die Prozesse angehalten werden.

Benachrichtigungs Abfragen, die eine Benachrichtigung über das Löschen einer Ressource anfordern und systeminterne Ereignisse verwenden, verwenden alle eine Syntax ähnlich der folgenden:

`SELECT * FROM __InstanceDeletionEvent WHERE TargetInstance ISA 'Win32_Process' and TargetInstance.Name = 'notepad.exe' `

## <a name="examples"></a>Beispiele

Im Codebeispiel für das [Monitor Process](https://Gallery.TechNet.Microsoft.Com/060a9adb-f99b-4f34-ba65-19b5f5815a38) Delete-Ereignis VBScript in der TechNet Gallery wird **\_ \_ instancedeletionevent** verwendet, um das erste Vorkommen eines Lösch Ereignisses für eine WMI-Instanz für den [**Win32- \_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process)zu überwachen

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_Instanceoperationevent**](/windows/desktop/WmiSdk/--instanceoperationevent)
</dt> <dt>

[WMI-System Klassen](wmi-system-classes.md)
</dt> </dl>

 

