---
description: Meldet ein instanzerstellungs-Ereignis, bei dem es sich um einen Typ eines systeminternen Ereignisses handelt, das generiert wird, wenn dem Namespace eine neue Instanz hinzugefügt wird.
ms.assetid: 41976479-70e3-4914-a56a-fa94a1fd31c7
ms.tgt_platform: multiple
title: __InstanceCreationEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceCreationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 29bdefbe1db20cd8b55b74433061b6c0cf152378
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217975"
---
# <a name="__instancecreationevent-class"></a>\_\_Instancecreationevent-Klasse

Die **\_ \_ instancecreationevent** -System Klasse meldet ein instanzerstellungs Ereignis, bei dem es sich um einen Typ eines systeminternen [Ereignisses](determining-the-type-of-event-to-receive.md) handelt, das generiert wird, wenn dem Namespace eine neue Instanz hinzugefügt wird.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
class __InstanceCreationEvent : __InstanceOperationEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Member

Die **\_ \_ instancecreationevent** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ instancecreationevent** -Klasse verfügt über diese Eigenschaften.

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

Kopie der erstellten Instanz. Diese Eigenschaft wird von [**\_ \_ instanceoperationevent**](--instanceoperationevent.md)geerbt.

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

Die **\_ \_ instancecreationevent** -Klasse wird von [**\_ \_ instanceoperationevent**](--instanceoperationevent.md)abgeleitet.

**Erstellung einer Ressource: \_ \_ instancecreationevent**

Angenommen, Sie möchten eine Benachrichtigung erhalten, wenn Notepad auf einem bestimmten Computer ausgeführt wird. Wenn Notepad ausgeführt wird, wird ein entsprechender Prozess erstellt. Prozesse können mithilfe von WMI verwaltet werden und werden durch die Win32- \_ Prozess Klasse dargestellt. Wenn Notepad gestartet wird, wird eine entsprechende Instanz der Win32- \_ Prozess Klasse über WMI verfügbar. Wenn Sie Ihr Interesse an diesem Ereignis registriert haben (indem Sie die entsprechende Ereignis Benachrichtigungs Abfrage ausgeben), führt die Verfügbarkeit dieser Instanz zur Erstellung einer Instanz der **\_ \_ instancecreationevent** -Klasse.

Benachrichtigungs Abfragen, die eine Benachrichtigung über die Erstellung einer Ressource anfordern und systeminterne Ereignisse verwenden, verwenden alle eine Syntax ähnlich der folgenden:

`SELECT * FROM __InstanceCreationEvent WITHIN PollingInterval WHERE TargetInstance ISA 'Win32_Process' and TargetInstance.Name = 'notepad.exe'`

Eine ausführlichere Erläuterung der Verwendung von **\_ \_ instancecreationevent** als Möglichkeit zum Überwachen von Dateisystemen finden Sie unter [WMI und Datei System Überwachung](https://www.codeproject.com/Articles/42212/WMI-and-File-System-Monitoring) für Code Project.

## <a name="examples"></a>Beispiele

Das PowerShell-Beispiel zur [Erstellung dauerhafter WMI-Ereignis Registrierung zum Überwachen von Dateien](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) in der TechNet Gallery verwendet **\_ \_ instancecreationevent** als Teil eines komplexen Skripts, um eine permanente WMI-Ereignis Registrierung einzurichten.

Das PowerShell-Beispiel PowerShell-PowerShell für [permanente Ereignisse](https://Gallery.TechNet.Microsoft.Com/PowerShell-WMI-Permanent-7e17f262) in der TechNet Gallery verwendet **\_ \_ instancecreationevent** als Teil eines Demonstrations Skripts zum Einrichten einer permanenten Ereignis Registrierung.

Im VBScript-Beispiel für das [Monitor Prozess Erstellungs Ereignis](https://Gallery.TechNet.Microsoft.Com/6f137d9e-f00a-4f0a-ad07-7d752ff5251d) auf der TechNet-Instanz wird **\_ \_ instancecreationevent** verwendet, um das erste Ereignis Erstellungs Ereignis für [**Win32- \_ Prozesse**](/windows/desktop/CIMWin32Prov/win32-process)zu überwachen

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

 

