---
description: Meldet ein Instanzänderungsereignis, bei dem es sich um einen Typ systeminterner Ereignisse handelt, der generiert wird, wenn sich eine Instanz im Namespace ändert.
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
ms.openlocfilehash: fffc8508eff24181201792207a151f5effd28a3022fec56506953b55d3e59deb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557757"
---
# <a name="__instancemodificationevent-class"></a>\_\_InstanceModificationEvent-Klasse

Die **\_ \_ InstanceModificationEvent-Systemklasse** meldet ein Instanzänderungsereignis, bei dem es sich um einen Typ systeminterner Ereignisse handelt, der generiert wird, wenn sich eine Instanz im Namespace ändert. [](determining-the-type-of-event-to-receive.md)

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

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

Die **\_ \_ InstanceModificationEvent-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ InstanceModificationEvent-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**PreviousInstance**
</dt> <dd> <dl> <dt>

Datentyp: **Objekt**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Kopie der -Instanz vor der Änderung.

</dd> <dt>

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

Neue Version der geänderten Instanz. Diese Eigenschaft wird von [**\_ \_ InstanceOperationEvent geerbt.**](--instanceoperationevent.md)

</dd> <dt>

**ZEIT \_ ERSTELLT**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eindeutiger Wert, der den Zeitpunkt angibt, zu dem das Ereignis generiert wurde. Dies ist ein 64-Bit-Wert, der die Anzahl von 100-Nanosekunden-Intervallen nach dem 1. Januar 1601 darstellt. Die Informationen sind im UTC-Format (Coordinated Universal Times) angegeben. Diese Eigenschaft wird vom Ereignis [**\_ \_ geerbt.**](--event.md)

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **\_ \_ InstanceModificationEvent-Klasse** wird von [**\_ \_ InstanceOperationEvent abgeleitet.**](--instanceoperationevent.md)

**Änderung einer Ressource: \_ \_ InstanceModificationEvent**

Angenommen, Sie vermuten, dass eine von Ihnen verwendete Verwaltungsanwendung fälschlicherweise den Starttyp eines Diensts auf einem Ihrer Server ändert. Sie möchten ein WMI-Skript schreiben, um änderungen an der Konfiguration des Diensts zu überwachen. Sobald eine Änderung an einem Dienst vorgenommen wird, spiegelt die entsprechende TargetInstance die Änderung wider.

Wenn Sie Ihr Interesse an diesem Ereignis registrieren, führt eine Änderung der Konfiguration des Diensts zur Erstellung einer Instanz der **\_ \_ InstanceModificationEvent-Klasse.**

Benachrichtigungsabfragen, die eine Benachrichtigung über die Änderung einer Ressource anfordern und systeminterne Ereignisse verwenden, verwenden eine Syntax ähnlich der folgenden:

`SELECT * FROM __InstanceModificationEvent WITHIN PollingInterval WHERE TargetInstance ISA 'Win32_Service' and TargetInstance.Name = 'alerter'`

## <a name="examples"></a>Beispiele

Das [VBScript-Beispiel](https://Gallery.TechNet.Microsoft.Com/daa06cdd-c1d9-4179-ba67-83aef2b9a079) zum Überwachen des Prozessänderungsereignisses im TechNet-Katalog verwendet **\_ \_ InstanceModificationEvent,** um das erste Vorkommen eines Änderungsereignisses einer WMI-Instanz für [**den Win32-Prozess \_ zu überwachen.**](/windows/desktop/CIMWin32Prov/win32-process)

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

 

