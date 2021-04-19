---
description: Dient als Basisklasse für alle systeminternen Ereignisse, die mit einer-Instanz in Beziehung stehen.
ms.assetid: f6d2b6e5-0dca-4cb5-95a5-33b45cd76807
ms.tgt_platform: multiple
title: __InstanceOperationEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceOperationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 1d3111b74c876cc7ffedb959eca7f46812ed92e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352696"
---
# <a name="__instanceoperationevent-class"></a>\_\_Instanceoperationevent-Klasse

Die **\_ \_ instanceoperationevent** -System Klasse fungiert als Basisklasse für alle systeminternen Ereignisse, die sich auf eine Instanz beziehen.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
class __InstanceOperationEvent : __Event
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Member

Die **\_ \_ instanceoperationevent** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ instanceoperationevent** -Klasse verfügt über diese Eigenschaften.

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

Die Instanz, auf die sich das Ereignis auswirkt. Bei Erstellungs Ereignissen handelt es sich hierbei um die neu erstellte Instanz. Bei Änderungs Ereignissen handelt es sich hierbei um die neue Version der geänderten Instanz. Bei Lösch Ereignissen handelt es sich hierbei um die gelöschte Instanz.

</dd> <dt>

**\_Erstellungszeit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eindeutiger Wert, der die Uhrzeit angibt, zu der das Ereignis generiert wurde. Dies ist ein 64-Bit-Wert, der die Anzahl der 100-Nanosecond-Intervalle nach dem 1. Januar 1601 darstellt. Die Informationen liegen im UTC-Format (koordiniert Universal Times) vor. Diese Eigenschaft wird von einem [**\_ \_ Ereignis**](--event.md)geerbt.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **\_ \_ instanceoperationevent** -Klasse wird von [**\_ \_ Event**](--event.md)abgeleitet.

Instanzen von **\_ \_ instanceoperationevent** werden nicht erstellt; es werden nur Instanzen der Unterklassen erstellt. Die folgenden Klassen werden von **\_ \_ instanceoperationevent** abgeleitet:

[**\_\_Instancecreationevent**](--instancecreationevent.md)

[**\_\_Instancemodificationevent**](--instancemodificationevent.md)

[**\_\_Instancedeletionevent**](--instancedeletionevent.md)

**Übersicht**

Ebenso wie eine WMI-Klasse, die jeden Typ von System Ressource darstellt, die mithilfe von WMI verwaltet werden kann, gibt es eine WMI-Klasse, die die einzelnen Arten von WMI-Ereignissen darstellt. Wenn ein Ereignis auftritt, das von WMI überwacht werden kann, wird eine Instanz der entsprechenden WMI-Ereignisklasse erstellt. Ein WMI-Ereignis tritt auf, wenn diese Instanz erstellt wird.

Es gibt drei Haupttypen von WMI-Ereignis Klassen, die alle von der WMI- [**\_ \_ Ereignis**](--event.md) Klasse abgeleitet sind: systeminterne Ereignisse, Extrinsic-Ereignisse und Timer-Ereignisse. Systeminterne Ereignisse werden wiederum durch drei verschiedene Klassen dargestellt, die von der **\_ \_ Ereignis** Klasse abgeleitet werden: [**\_ \_ namespaceoperationevent**](--namespaceoperationevent.md), **\_ \_ instanceoperationevent** und [**\_ \_ classoperationevent**](--classoperationevent.md).

Systeminterne Ereignisse

Systeminterne Ereignisse werden verwendet, um eine Ressource zu überwachen, die von einer Klasse im CIM-Repository repräsentiert wird. Jede Ressource wird durch eine Instanz einer-Klasse dargestellt. Dies bedeutet, dass die Überwachung einer Ressource mithilfe von WMI tatsächlich das Überwachen der Instanzen beinhaltet, die der Ressource entsprechen.

Systeminterne Ereignisse können auch verwendet werden, um Änderungen an einem Namespace oder einer Klasse im Repository zu überwachen. Allerdings ist das Überwachen von Änderungen an Namespaces oder Klassen für Systemadministratoren beschränkt.

Ein System internes Ereignis wird durch eine Instanz einer Klasse dargestellt, die von \_ \_ instanceoperationevent, \_ \_ namespaceoperationevent oder \_ \_ classoperationevent abgeleitet ist. Alle Änderungen an Instanzen in WMI werden durch die \_ \_ instanceoperationevent-Klasse und die daraus abgeleiteten Klassen dargestellt: \_ \_ instancecreationevent, \_ \_ instancemodificationevent und \_ \_ instancedeletionevent.

Das Überwachen von Ressourcen mithilfe von WMI umfasst das Überwachen von Instanzen, und alle Änderungen an den Instanzen werden durch \_ \_ instanceoperationevent und die daraus abgeleiteten Klassen dargestellt. Dies bedeutet, dass Überwachungsressourcen letztendlich das Überwachen von Instanzen von \_ \_ instanceoperationevent-abgeleiteten Klassen beinhalten.

Sie registrieren Interesse an Instanzen einer dieser Klassen, indem Sie eine in WQL ausgedrückte Benachrichtigungs Abfrage ausgeben. Die Abfrage verwendet eine Syntax, die der folgenden ähnelt:

`SELECT * FROM __InstanceOperationEventOrDerivedClass WITHIN PollingInterval WHERE TargetInstance ISA WMIClassName AND TargetInstance.WMIClassPropertyName = Value`

Eine ausführlichere Erläuterung der Verwendung von WMI-Instanzereignissen zum Überwachen von Computeraktivitäten finden Sie unter [wie kann ich unterschiedliche Arten von Ereignissen mit nur einem Skript überwachen?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/04/04/how-can-i-monitor-for-different-types-of-events-with-just-one-script.aspx)

## <a name="examples"></a>Beispiele

Das Codebeispiel für den [Monitor Process Event](https://Gallery.TechNet.Microsoft.Com/94c7dc4c-813a-411d-aa3f-f98982cd2a2f) VBScript in der TechNet Gallery verwendet **\_ \_ instanceoperationevent** , um das erste WMI-Instanzereignis für den [**Win32- \_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process)zu überwachen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_Ereignis**](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[WMI-System Klassen](wmi-system-classes.md)
</dt> <dt>

[Bestimmen des zu empfangenden Ereignis Typs](determining-the-type-of-event-to-receive.md)
</dt> <dt>

[Schreiben in eine Protokolldatei auf Grundlage eines Ereignisses](writing-to-a-log-file-based-on-an-event.md)
</dt> </dl>

 

