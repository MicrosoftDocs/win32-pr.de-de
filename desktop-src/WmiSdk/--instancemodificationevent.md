---
description: Meldet ein instanzänderungsereignis, bei dem es sich um einen Typ eines systeminternen Ereignisses handelt, das beim Ändern einer Instanz im Namespace generiert wird.
ms.assetid: aa35f349-8b57-435f-bf82-76daf2b43ec9
ms.tgt_platform: multiple
title: __InstanceModificationEvent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceModificationEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: e644db16b6638bbc87006819e186540a9ce1874e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866904"
---
# <a name="__instancemodificationevent-class"></a>\_\_Instancemodificationevent-Klasse

Die **\_ \_ instancemodificationevent** -System Klasse meldet ein instanzänderungsereignis, bei dem es sich um einen Typ eines systeminternen [Ereignisses](determining-the-type-of-event-to-receive.md) handelt, das beim Ändern einer Instanz im-Namespace generiert wird.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
class __InstanceModificationEvent : __InstanceOperationEvent
{
  object PreviousInstance;
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Member

Die **\_ \_ instancemodificationevent** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ instancemodificationevent** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**PreviousInstance**
</dt> <dd> <dl> <dt>

Datentyp: **Object**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Kopie der Instanz vor der Änderung.

</dd> <dt>

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

Neue Version der geänderten Instanz. Diese Eigenschaft wird von [**\_ \_ instanceoperationevent**](--instanceoperationevent.md)geerbt.

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

Die **\_ \_ instancemodificationevent** -Klasse wird von [**\_ \_ instanceoperationevent**](--instanceoperationevent.md)abgeleitet.

**Änderung einer Ressource: \_ \_ instancemodificationevent**

Angenommen, Sie vermuten, dass eine von Ihnen verwendete Verwaltungs Anwendung fälschlicherweise den Starttyp eines Diensts auf einem der Server ändert. Sie möchten ein WMI-Skript schreiben, um Änderungen zu überwachen, die an der Konfiguration des Dienstanbieter vorgenommen wurden. Sobald eine Änderung an einem Dienst vorgenommen wird, spiegelt die zugehörige TargetInstance die Änderung wider.

Wenn Sie Ihr Interesse bei diesem Ereignis registrieren, führt eine Änderung an der Konfiguration des dienstantrags zur Erstellung einer Instanz der **\_ \_ instancemodificationevent** -Klasse.

Benachrichtigungs Abfragen, die eine Benachrichtigung über die Änderung einer Ressource anfordern und intrinsische Ereignisse verwenden, verwenden alle eine Syntax, die der folgenden ähnelt:

`SELECT * FROM __InstanceModificationEvent WITHIN PollingInterval WHERE TargetInstance ISA 'Win32_Service' and TargetInstance.Name = 'alerter'`

## <a name="examples"></a>Beispiele

Das Beispiel [Monitor Process modificationevent](https://Gallery.TechNet.Microsoft.Com/daa06cdd-c1d9-4179-ba67-83aef2b9a079) VBScript in der TechNet Gallery verwendet **\_ \_ instancemodificationevent** , um das erste Vorkommen eines WMI-instanzänderungsereignisses für den [**Win32- \_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process)zu überwachen.

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

 

