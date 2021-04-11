---
title: Taskplaner 2,0-Enumerationstypen
description: Beschreibt die Enumerationstypen, die die Konstanten definieren, die von den Taskplaner 2,0-APIs verwendet werden.
ms.assetid: d59f017e-df32-4826-954d-9ba338282d0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db410564ab97f0477ecac8aeda2b54b8fd655d62
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104316851"
---
# <a name="task-scheduler-20-enumerated-types"></a>Taskplaner 2,0-Enumerationstypen

Beschreibt die Enumerationstypen, die die Konstanten definieren, die von den Taskplaner 2,0-APIs verwendet werden.


Die folgenden Enumerationstypen werden in Taskplaner 2,0 eingeführt.



| Enumeration                                                                  | Beschreibung                                                                                                      |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**Task \_ \_ Aktionstyp**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)                               | Definiert die Art von Aktionen, die von einer Aufgabe durchgeführt werden können.                                                             |
| [**Aufgaben \_ Kompatibilität**](/windows/desktop/api/taskschd/ne-taskschd-task_compatibility)                            | Definiert, welche Versionen von Taskplaner oder den at-Befehl, mit dem die Aufgabe kompatibel ist.                      |
| [**Task \_ Erstellung**](/windows/desktop/api/taskschd/ne-taskschd-task_creation)                                       | Definiert, wie der Taskplaner-Dienst die Aufgabe erstellt, aktualisiert oder deaktiviert.                                   |
| [**\_taskaufgabenflags \_**](/windows/desktop/api/taskschd/ne-taskschd-task_enum_flags)                                 | Definiert, wie die Taskplaner durch registrierte Tasks aufzählt.                                              |
| [**Task \_ Instanzen \_ Richtlinie**](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy)                     | Definiert, wie die Taskplaner vorhandene Instanzen der Aufgabe behandelt, wenn eine neue Instanz der Aufgabe gestartet wird. |
| [**Task \_ Anmeldetyp**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type)                                  | Definiert, welche Anmelde Methode zum Ausführen einer Aufgabe erforderlich ist.                                                          |
| [**Task \_ processtokensid- \_ Typ**](/windows/win32/api/taskschd/ne-taskschd-task_processtokensid_type)             | Definiert die Typen der Prozess-sid, die von Tasks verwendet werden können.                                                      |
| [**\_ \_ tasktestflags**](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags)                                   | Definiert, wie eine Aufgabe ausgeführt wird.                                                                                       |
| [**\_taskrunlevel- \_ Typ**](/windows/win32/api/taskschd/ne-taskschd-task_runlevel_type)                           | Definiert Lua-Erweiterungs Flags, die angeben, welche Berechtigungsebene für die Aufgabe ausgeführt wird.                         |
| [**\_ \_ Status \_ \_ Änderungstyp für Task Sitzung**](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type) | Definiert, welche Arten von Terminal Server-Sitzungs Statusänderungen Sie verwenden können, um einen Task zu starten.               |
| [**Task \_ Status**](/windows/desktop/api/taskschd/ne-taskschd-task_state)                                            | Definiert die verschiedenen Zustände, in denen sich eine registrierte Aufgabe befinden kann.                                                   |
| [**Task \_ - \_ Typ2**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)                                  | Definiert den Typ der Trigger, die von Tasks verwendet werden können.                                                          |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> <dt>

[Taskplaner Referenz](task-scheduler-reference.md)
</dt> </dl>

 

 




