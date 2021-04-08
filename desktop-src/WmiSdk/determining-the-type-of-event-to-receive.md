---
description: 'Bevor Sie sich für den Empfang eines Ereignisses registrieren, müssen Sie die Typen der zu empfangenden Ereignisse bestimmen: systeminterne oder extrinsische Ereignisse.'
ms.assetid: 46cdfcfa-42c6-4169-bc4d-725867224889
ms.tgt_platform: multiple
title: Bestimmen des zu empfangenden Ereignis Typs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 477f3d10536e5b0622e1e64b6cec9abdf4183c7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758017"
---
# <a name="determining-the-type-of-event-to-receive"></a>Bestimmen des zu empfangenden Ereignis Typs

Bevor Sie sich für den Empfang eines Ereignisses registrieren, müssen Sie die Typen der zu empfangenden Ereignisse bestimmen: System [interne oder](#intrinsic-events) [extrinsische](#extrinsic-events)Ereignisse. Weitere Informationen zum Empfangen von Ereignissen finden Sie unter [empfangen eines WMI-Ereignisses](receiving-a-wmi-event.md). Weitere Informationen zum Bereitstellen von Ereignissen finden Sie unter [Entwickeln eines WMI-Anbieters](developing-a-wmi-provider.md) und [Schreiben eines Ereignis Anbieters](writing-an-event-provider.md). Weitere Informationen zu den Sicherheitsaspekten beim empfangen und Bereitstellen von Ereignissen finden Sie unter [Sichern von WMI-Ereignissen.](securing-wmi-events.md)

## <a name="intrinsic-events"></a>Systeminterne Ereignisse

Ein System internes Ereignis ist ein Ereignis, das als Reaktion auf eine Änderung im standardmäßigen WMI-Datenmodell auftritt. Jede systeminterne Ereignisklasse stellt einen bestimmten Typ von Änderung dar und tritt auf, wenn ein Namespace, eine Klasse oder eine Klasseninstanz von WMI oder einem Anbieter erstellt, gelöscht oder geändert wird. Beispielsweise würde die Erstellung einer [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) -Instanz zu einer [**\_ \_ instancecreationevent**](--instancecreationevent.md) -Instanz führen.

WMI erstellt systeminterne Ereignisse für Objekte, die im WMI-Repository gespeichert sind. Ein Anbieter generiert systeminterne Ereignisse für dynamische Klassen, aber WMI kann eine Instanz für eine dynamische Klasse erstellen, wenn kein Anbieter verfügbar ist. WMI verwendet Abruf Vorgänge, um die Änderungen zu erkennen. In der folgenden Tabelle werden die System Klassen aufgelistet, die WMI zum Melden System interner Ereignisse verwendet.



| System Klasse                                                           | BESCHREIBUNG                                                                                                                                                                                             |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_\_Classcreationevent**](--classcreationevent.md)                 | Benachrichtigt einen Consumer, wenn eine Klasse erstellt wird.                                                                                                                                                            |
| [**\_\_Classdeletionevent**](--classdeletionevent.md)                 | Benachrichtigt einen Consumer, wenn eine Klasse gelöscht wird.                                                                                                                                                            |
| [**\_\_Classmodificationevent**](--classmodificationevent.md)         | Benachrichtigt einen Consumer, wenn eine Klasse geändert wird.                                                                                                                                                           |
| [**\_\_Instancecreationevent**](--instancecreationevent.md)           | Benachrichtigt einen Consumer, wenn eine Klasseninstanz erstellt wird.                                                                                                                                                   |
| [**\_\_Instanceoperationevent**](--instanceoperationevent.md)         | Benachrichtigt einen Consumer, wenn ein Instanzereignis auftritt, z. b. das Erstellen, löschen oder Ändern der-Instanz. Sie können diese Klasse in Abfragen verwenden, um alle Typen Ereignisse, die einer-Instanz zugeordnet sind, zu erhalten. |
| [**\_\_Instancedeletionevent**](--instancedeletionevent.md)           | Benachrichtigt einen Consumer, wenn eine Instanz gelöscht wird.                                                                                                                                                        |
| [**\_\_Instancemodificationevent**](--instancemodificationevent.md)   | Benachrichtigt einen Consumer, wenn eine Instanz geändert wird.                                                                                                                                                       |
| [**\_\_Namespacecreationevent**](--namespacecreationevent.md)         | Benachrichtigt einen Consumer, wenn ein Namespace erstellt wird.                                                                                                                                                        |
| [**\_\_Namespacedeletionevent**](--namespacedeletionevent.md)         | Benachrichtigt einen Consumer, wenn ein Namespace gelöscht wird.                                                                                                                                                        |
| [**\_\_Namespacemodificationevent**](--namespacemodificationevent.md) | Benachrichtigt einen Consumer, wenn ein Namespace geändert wird.                                                                                                                                                       |
| [**\_\_Consumerfailureevent**](--consumerfailureevent.md)             | Benachrichtigt einen Consumer, wenn ein anderes Ereignis aufgrund eines Fehlers bei einem Ereignisconsumer gelöscht wird.                                                                                                 |
| [**\_\_Eventdroppedevent**](--eventdroppedevent.md)                   | Benachrichtigt einen Consumer, wenn ein anderes Ereignis verworfen wird, anstatt dem anfordernden Ereignisconsumer zugestellt zu werden.                                                                                       |
| [**\_\_Eventqueueoverflowevent**](--eventqueueoverflowevent.md)       | Benachrichtigt einen Consumer, wenn ein Ereignis aufgrund eines Überlauf in der Übermittlungs Warteschlange gelöscht wird.                                                                                                                  |
| [**\_\_Methodinvocationevent**](--methodinvocationevent.md)           | Benachrichtigt einen Consumer, wenn ein Methoden Ereignis aufgerufen wird.                                                                                                                                                    |



 

## <a name="extrinsic-events"></a>Extrinsische Ereignisse

Bei einem extrinsischen Ereignis handelt es sich um ein vordefiniertes vorkommen, das nicht direkt mit Änderungen im WMI-Datenmodell verknüpft werden kann. Daher ermöglicht WMI einem Ereignis Anbieter die Definition einer Ereignisklasse, die das Ereignis beschreibt. Beispielsweise ist ein Ereignis, das einen Computer Wechsel in den Standbymodus beschreibt, ein extrinsisches Ereignis. Ein Anbieter leitet ein System externe-Ereignis von der [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md) -System Klasse ab, bei der es sich um eine Unterklasse der [**\_ \_ Ereignis**](--event.md) System Klasse handelt. Die [System Registrierung](/previous-versions/windows/desktop/regprov/system-registry-provider) und die [SNMP](snmp-provider.md) -Anbieter definieren System externe-Ereignis Klassen, wie z. b. **RegistryKeyChangeEvent**, das einen Consumer benachrichtigt, wenn ein Registrierungsschlüssel geändert wird. Weitere Informationen finden Sie unter [registrieren für System Registrierungs Ereignisse](registering-for-system-registry-events.md) und [Schreiben eines Ereignis Anbieters](writing-an-event-provider.md).

Im folgenden Beispiel meldet ein Ereignis Anbieter Sicherheitsverletzungen an einem oder mehreren Gebäuden. Die folgende Klasse ist möglicherweise für das System externe-Ereignis definiert, das eine Sicherheitsverletzung darstellt.

``` syntax
class SecurityViolationEvent : __ExtrinsicEvent
{
   string Building;           // building where violation occurred
   sint32 EntranceNumber;     // entrance where violation occurred
   datetime TimeOfDetection;  // date and time of violation
}
```

Zum Empfangen der Sicherheits Verletzungs Benachrichtigungen registriert ein Consumer den securityviolationevent-Ereignistyp. Sofern nicht anders angegeben, empfängt ein Consumer in allen Zeiträumen und in allen Gebäuden eine Benachrichtigung über alle Sicherheitsverletzungen. Die-Ereignisklasse enthält auch Informationen, die Consumer verwenden können, um spezifischere Ereignisse anzufordern.

Im folgenden Beispiel registriert die Abfrage den Consumer für Sicherheits Verletzungs Ereignisse nur in Gebäude 24.

`SELECT * FROM SecurityViolationEvent WHERE Building = 24;`

 

 
