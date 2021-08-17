---
description: 'Bevor Sie sich für den Empfang eines Ereignisses registrieren, müssen Sie die Zu empfangenden Ereignistypen bestimmen: systeminterne oder extrinsische Ereignisse.'
ms.assetid: 46cdfcfa-42c6-4169-bc4d-725867224889
ms.tgt_platform: multiple
title: Bestimmen des Zu empfangenden Ereignistyps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9172e3246a31cb42ada3b9f5099bc3b0575959c125dedd44d7c6ed745134a4a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119374650"
---
# <a name="determining-the-type-of-event-to-receive"></a>Bestimmen des Zu empfangenden Ereignistyps

Bevor Sie sich für den Empfang eines Ereignisses registrieren, müssen Sie die Typen der zu empfangenden Ereignisse bestimmen: [systeminterne](#intrinsic-events) oder [extrinsische](#extrinsic-events). Weitere Informationen zum Empfangen von Ereignissen finden Sie unter [Empfangen eines WMI-Ereignisses.](receiving-a-wmi-event.md) Weitere Informationen zum Bereitstellen von Ereignissen finden Sie unter [Entwickeln eines WMI-Anbieters](developing-a-wmi-provider.md) und [Schreiben eines Ereignisanbieters.](writing-an-event-provider.md) Weitere Informationen zu den Sicherheitsbedenken beim Empfangen und Bereitstellen von Ereignissen finden Sie unter [Schützen von WMI-Ereignissen.](securing-wmi-events.md)

## <a name="intrinsic-events"></a>Systeminterne Ereignisse

Ein systeminternes Ereignis ist ein Ereignis, das als Reaktion auf eine Änderung im WMI-Standarddatenmodell auftritt. Jede systeminterne Ereignisklasse stellt einen bestimmten Typ von Änderung dar und tritt auf, wenn ein Namespace, eine Klasse oder eine Klasseninstanz von WMI oder einem Anbieter erstellt, gelöscht oder geändert wird. Beispielsweise würde die Erstellung einer [**Win32 \_ LogicalDisk-Instanz**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) zu einer [**\_ \_ InstanceCreationEvent-Instanz**](--instancecreationevent.md) führen.

WMI erstellt systeminterne Ereignisse für Objekte, die im WMI-Repository gespeichert sind. Ein Anbieter generiert systeminterne Ereignisse für dynamische Klassen, WMI kann jedoch eine Instanz für eine dynamische Klasse erstellen, wenn kein Anbieter verfügbar ist. WMI verwendet Abrufe, um die Änderungen zu erkennen. In der folgenden Tabelle sind die Systemklassen aufgeführt, die WMI zum Melden systeminterner Ereignisse verwendet.



| Systemklasse                                                           | BESCHREIBUNG                                                                                                                                                                                             |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_\_ClassCreationEvent**](--classcreationevent.md)                 | Benachrichtigt einen Consumer, wenn eine Klasse erstellt wird.                                                                                                                                                            |
| [**\_\_ClassDeletionEvent**](--classdeletionevent.md)                 | Benachrichtigt einen Consumer, wenn eine Klasse gelöscht wird.                                                                                                                                                            |
| [**\_\_ClassModificationEvent**](--classmodificationevent.md)         | Benachrichtigt einen Consumer, wenn eine Klasse geändert wird.                                                                                                                                                           |
| [**\_\_InstanceCreationEvent**](--instancecreationevent.md)           | Benachrichtigt einen Consumer, wenn eine Klasseninstanz erstellt wird.                                                                                                                                                   |
| [**\_\_InstanceOperationEvent**](--instanceoperationevent.md)         | Benachrichtigt einen Consumer, wenn ein Instanzereignis auftritt, z. B. Erstellung, Löschung oder Änderung der Instanz. Sie können diese Klasse in Abfragen verwenden, um alle Typenereignisse zu erhalten, die einer Instanz zugeordnet sind. |
| [**\_\_InstanceDeletionEvent**](--instancedeletionevent.md)           | Benachrichtigt einen Consumer, wenn eine Instanz gelöscht wird.                                                                                                                                                        |
| [**\_\_InstanceModificationEvent**](--instancemodificationevent.md)   | Benachrichtigt einen Consumer, wenn eine Instanz geändert wird.                                                                                                                                                       |
| [**\_\_NamespaceCreationEvent**](--namespacecreationevent.md)         | Benachrichtigt einen Consumer, wenn ein Namespace erstellt wird.                                                                                                                                                        |
| [**\_\_NamespaceDeletionEvent**](--namespacedeletionevent.md)         | Benachrichtigt einen Consumer, wenn ein Namespace gelöscht wird.                                                                                                                                                        |
| [**\_\_NamespaceModificationEvent**](--namespacemodificationevent.md) | Benachrichtigt einen Consumer, wenn ein Namespace geändert wird.                                                                                                                                                       |
| [**\_\_ConsumerFailureEvent**](--consumerfailureevent.md)             | Benachrichtigt einen Consumer, wenn ein anderes Ereignis aufgrund eines Fehlers eines Ereignisverbraucher gelöscht wird.                                                                                                 |
| [**\_\_EventDroppedEvent**](--eventdroppedevent.md)                   | Benachrichtigt einen Consumer, wenn ein anderes Ereignis gelöscht und nicht an den anfordernden Ereignis consumer übermittelt wird.                                                                                       |
| [**\_\_EventQueueOverflowEvent**](--eventqueueoverflowevent.md)       | Benachrichtigt einen Consumer, wenn ein Ereignis als Folge eines Überlaufs der Übermittlungswarteschlange gelöscht wird.                                                                                                                  |
| [**\_\_MethodInvocationEvent**](--methodinvocationevent.md)           | Benachrichtigt einen Consumer, wenn ein Methodenaufrufereignis auftritt.                                                                                                                                                    |



 

## <a name="extrinsic-events"></a>Extrinsische Ereignisse

Ein extrinsisches Ereignis ist ein vordefiniertes Ereignis, das nicht direkt mit Änderungen im WMI-Datenmodell verknüpft werden kann. Daher ermöglicht WMI einem Ereignisanbieter das Definieren einer Ereignisklasse, die das Ereignis beschreibt. Beispielsweise ist ein Ereignis, das einen Computer beschreibt, der in den Stand-by-Modus wechselt, ein extrinsisches Ereignis. Ein Anbieter leitet ein extrinsisches Ereignis von der [**\_ \_ ExtrinsicEvent-Systemklasse**](--extrinsicevent.md) ab, die eine Unterklasse der [**\_ \_ Event-Systemklasse**](--event.md) ist. Die [Systemregistrierungs-](/previous-versions/windows/desktop/regprov/system-registry-provider) und [SNMP-Anbieter](snmp-provider.md) definieren extrinsische Ereignisklassen, z. B. **RegistryKeyChangeEvent,** die einen Consumer benachrichtigt, wenn ein Registrierungsschlüssel geändert wird. Weitere Informationen finden Sie unter [Registrieren für Systemregistrierungsereignisse](registering-for-system-registry-events.md) und [Schreiben eines Ereignisanbieters.](writing-an-event-provider.md)

Im folgenden Beispiel berichtet ein Ereignisanbieter Sicherheitsverletzungen an ein oder mehrere Gebäude. Die folgende Klasse kann für das extrinsische Ereignis definiert werden, das eine Sicherheitsverletzung darstellt.

``` syntax
class SecurityViolationEvent : __ExtrinsicEvent
{
   string Building;           // building where violation occurred
   sint32 EntranceNumber;     // entrance where violation occurred
   datetime TimeOfDetection;  // date and time of violation
}
```

Um Benachrichtigungen zu Sicherheitsverletzungen zu erhalten, registriert sich ein Consumer für den SecurityViolationEvent-Ereignistyp. Sofern nicht anders angegeben, erhält ein Consumer eine Benachrichtigung über alle Sicherheitsverletzungen während aller Zeiträume und in allen Gebäuden. Die Ereignisklasse enthält auch Informationen, mit denen Benutzer spezifischere Ereignisse erfragen können.

Im folgenden Beispiel registriert die Abfrage den Consumer nur in Gebäude 24 für Sicherheitsverletzungsereignisse.

`SELECT * FROM SecurityViolationEvent WHERE Building = 24;`

 

 
