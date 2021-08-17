---
title: Taskplaner für Entwickler
description: Mit dem Taskplaner können Sie automatisch Routineaufgaben auf einem ausgewählten Computer ausführen. Taskplaner überwacht dazu die von Ihnen gewählten Kriterien (als Trigger bezeichnet) und führt dann die Aufgaben aus, wenn diese Kriterien erfüllt sind.
ms.assetid: 15970a51-c139-48b8-b82b-605728d0f386
keywords:
- Taskplaner für Entwickler
- Taskplaner für die Entwicklung
- Entwickeln mit Taskplaner
- Taskplaner, Portalseite
ms.topic: article
ms.date: 10/18/2019
ms.openlocfilehash: 05edababae87c760f5506d8a40d18ef8dcc59ab35fa78b692cc76b5ad3b46579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118357743"
---
# <a name="task-scheduler-for-developers"></a>Taskplaner für Entwickler

> [!IMPORTANT]
> Dieses thema und die anderen Themen in diesem Abschnitt gelten für eine Entwicklergruppe. Wenn Sie die Taskplaner-Komponente als Administrator oder IT-Professional verwenden möchten, finden Sie weitere Informationen unter [Taskplaner](/dynamics365/business-central/dev-itpro/developer/devenv-task-scheduler).

## <a name="about-the-task-scheduler"></a>Informationen zum Taskplaner

Mit dem Taskplaner können Sie automatisch Routineaufgaben auf einem ausgewählten Computer ausführen. Taskplaner überwacht dazu die von Ihnen gewählten Kriterien (als Trigger bezeichnet) und führt dann die Aufgaben aus, wenn diese Kriterien erfüllt sind.

Sie können die Taskplaner verwenden, um Aufgaben wie das Starten einer Anwendung, das Senden einer E-Mail-Nachricht oder das Anzeigen eines Meldungsfelds auszuführen. Aufgaben können so geplant werden, dass sie als Reaktion auf diese Ereignisse oder Trigger ausgeführt werden. 

- Wenn ein bestimmtes Systemereignis auftritt.
- Zu einem bestimmten Zeitpunkt.
- Zu einem bestimmten Zeitpunkt nach einem täglichen Zeitplan.
- Zu einem bestimmten Zeitpunkt nach einem wöchentlichen Zeitplan.
- Zu einem bestimmten Zeitpunkt nach einem monatlichen Zeitplan.
- Zu einem bestimmten Zeitpunkt nach einem monatlichen Wochentagszeitplan.
- Wenn der Computer in den Leerlauf wechselt.
- Wenn der Task registriert ist.
- Wenn das System gestartet wird.
- Wenn sich ein Benutzer anmeldet.
- Wenn sich der Zustand einer Terminalserversitzung ändert.

## <a name="developers"></a>Entwickler

Der Taskplaner stellt APIs in diesen Formen bereit.

- Taskplaner 2.0: Schnittstellen und Objekte werden für C++ bzw. für die Skriptentwicklung bereitgestellt.
- Taskplaner 1.0: Schnittstellen werden für die C++-Entwicklung bereitgestellt.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Die Taskplaner erfordert die folgenden Betriebssysteme.

- Taskplaner 2.0: Der Client erfordert Windows Vista oder höher. Server erfordert Windows Server 2008 oder höher.
- Taskplaner 1.0: Der Client erfordert Windows Vista oder Windows XP. Server erfordert Windows Server 2008 oder Windows Server 2003.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | BESCHREIBUNG |
|-|-|
| [Neuerungen in Taskplaner](what-s-new-in-task-scheduler.md) | Zusammenfassung der neuen Funktionen, die durch die Taskplaner eingeführt wurden. |
| [Informationen zum Taskplaner](about-the-task-scheduler.md) | Allgemeine konzeptionelle Informationen zur Taskplaner-API. |
| [Verwenden der Taskplaner](using-the-task-scheduler.md) | Codebeispiele, die zeigen, wie die Taskplaner-APIs verwendet werden. |
| [Taskplaner Referenz](task-scheduler-reference.md) | Ausführliche Referenzinformationen für Taskplaner-APIs und das Taskplaner Schema. |