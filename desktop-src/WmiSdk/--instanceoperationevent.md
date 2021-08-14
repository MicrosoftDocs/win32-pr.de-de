---
description: Dient als Basisklasse für alle systeminternen Ereignisse, die sich auf eine -Instanz beziehen.
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
ms.openlocfilehash: a4e988f26b64d0d8bd4a23f853b7bf9dc92f2610936239b4363439d5c7d70170
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320807"
---
# <a name="__instanceoperationevent-class"></a>\_\_InstanceOperationEvent-Klasse

Die **\_ \_ InstanceOperationEvent-Systemklasse** dient als Basisklasse für alle systeminternen Ereignisse, die sich auf eine -Instanz beziehen.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

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

Die **\_ \_ InstanceOperationEvent-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ InstanceOperationEvent-Klasse** verfügt über diese Eigenschaften.

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

Instanz, die vom Ereignis betroffen ist. Bei Erstellungsereignissen ist dies die neu erstellte Instanz. Bei Änderungsereignissen ist dies die neue Version der geänderten Instanz. Bei Löschereignissen ist dies die gelöschte Instanz.

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

Die **\_ \_ InstanceOperationEvent-Klasse** wird von Event [**\_ \_ abgeleitet.**](--event.md)

Instanzen von **\_ \_ InstanceOperationEvent** werden nicht erstellt, sondern nur Instanzen ihrer Unterklassen. Die folgenden Klassen werden von **\_ \_ InstanceOperationEvent ableiten:**

[**\_\_InstanceCreationEvent**](--instancecreationevent.md)

[**\_\_InstanceModificationEvent**](--instancemodificationevent.md)

[**\_\_InstanceDeletionEvent**](--instancedeletionevent.md)

**Übersicht**

Genau wie es eine WMI-Klasse gibt, die jeden Typ von Systemressource darstellt, der mit WMI verwaltet werden kann, gibt es eine WMI-Klasse, die jeden Typ von WMI-Ereignis darstellt. Wenn ein Ereignis auftritt, das von WMI überwacht werden kann, wird eine Instanz der entsprechenden WMI-Ereignisklasse erstellt. Ein WMI-Ereignis tritt auf, wenn diese Instanz erstellt wird.

Es gibt drei Haupttypen von WMI-Ereignisklassen, die alle von der [**\_ \_**](--event.md) WMI-Ereignisklasse abgeleitet werden: Systeminterne Ereignisse, extrinsische Ereignisse und Timerereignisse. Systeminterne Ereignisse werden wiederum durch drei unterschiedliche Klassen dargestellt, die von der **\_ \_ Event-Klasse** abgeleitet werden: [**\_ \_ NamespaceOperationEvent,**](--namespaceoperationevent.md) **\_ \_ InstanceOperationEvent** und [**\_ \_ ClassOperationEvent**](--classoperationevent.md).

Systeminterne Ereignisse

Systeminterne Ereignisse werden verwendet, um eine Ressource zu überwachen, die durch eine Klasse im CIM-Repository dargestellt wird. Jede Ressource wird durch eine Instanz einer Klasse dargestellt. Dies bedeutet, dass die Überwachung einer Ressource mit WMI tatsächlich die Überwachung der Instanzen umfasst, die der Ressource entsprechen.

Systeminterne Ereignisse können auch verwendet werden, um Änderungen an einem Namespace oder einer Klasse im Repository zu überwachen. Die Überwachung von Änderungen an Namespaces oder Klassen ist für Systemadministratoren jedoch von begrenztem Nutzen.

Ein systeminternes Ereignis wird durch eine Instanz einer Klasse dargestellt, die von \_ \_ InstanceOperationEvent, \_ \_ NamespaceOperationEvent oder \_ \_ ClassOperationEvent abgeleitet wird. Alle Änderungen an Instanzen in WMI werden durch die InstanceOperationEvent-Klasse und die von ihr abgeleiteten Klassen \_ \_ dargestellt: \_ \_ InstanceCreationEvent, \_ \_ InstanceModificationEvent und \_ \_ InstanceDeletionEvent.

Die Überwachung von Ressourcen mithilfe von WMI umfasst die Überwachung von -Instanzen, und alle Änderungen an -Instanzen werden durch InstanceOperationEvent und die daraus \_ \_ abgeleiteten Klassen dargestellt. Dies bedeutet, dass die Überwachung von Ressourcen letztendlich die Überwachung von Instanzen von \_ \_ von InstanceOperationEvent abgeleiteten Klassen umfasst.

Sie registrieren Interesse an Instanzen einer dieser Klassen, indem Sie eine in WQL ausgedrückte Benachrichtigungsabfrage ausführen. Die Abfrage verwendet eine Syntax ähnlich der folgenden:

`SELECT * FROM __InstanceOperationEventOrDerivedClass WITHIN PollingInterval WHERE TargetInstance ISA WMIClassName AND TargetInstance.WMIClassPropertyName = Value`

Eine längere Erörterung der Verwendung der WMI-Instanzereignisse zum Überwachen der Computeraktivität finden Sie unter How Can I Monitor for Different Types of Events With Just One Script? (Wie kann ich mit nur einem Skript auf verschiedene [Ereignistypen überwachen?).](https://blogs.technet.com/b/heyscriptingguy/archive/2005/04/04/how-can-i-monitor-for-different-types-of-events-with-just-one-script.aspx)

## <a name="examples"></a>Beispiele

Das [](https://Gallery.TechNet.Microsoft.Com/94c7dc4c-813a-411d-aa3f-f98982cd2a2f) VBScript-Codebeispiel für das Monitorprozessereignis im TechNet-Katalog verwendet **\_ \_ InstanceOperationEvent,** um das erste WMI-Instanzereignis für [**den Win32-Prozess zu \_ überwachen.**](/windows/desktop/CIMWin32Prov/win32-process)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_\_Ereignis**](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[WMI-Systemklassen](wmi-system-classes.md)
</dt> <dt>

[Bestimmen des Zu empfangenden Ereignistyps](determining-the-type-of-event-to-receive.md)
</dt> <dt>

[Schreiben in eine Protokolldatei basierend auf einem Ereignis](writing-to-a-log-file-based-on-an-event.md)
</dt> </dl>

 

