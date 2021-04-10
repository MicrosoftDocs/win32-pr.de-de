---
title: Taskplaner für Entwickler
description: Der Taskplaner ermöglicht Ihnen das automatische Ausführen von Routineaufgaben auf einem ausgewählten Computer. Taskplaner dies durch die Überwachung der von Ihnen gewählten Kriterien (als Trigger bezeichnet) und anschließendes Ausführen der Aufgaben, wenn diese Kriterien erfüllt sind.
ms.assetid: 15970a51-c139-48b8-b82b-605728d0f386
keywords:
- Taskplaner für Entwickler
- Taskplaner für die Entwicklung
- Entwickeln mit Taskplaner
- Taskplaner, Portalseite
ms.topic: article
ms.date: 10/18/2019
ms.openlocfilehash: dfbfb76145e38003e7c501b98c817f4aaca3ff09
ms.sourcegitcommit: 087843ef08ddcd8bce9ed647b610035925da2b3e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/19/2019
ms.locfileid: "104100826"
---
# <a name="task-scheduler-for-developers"></a>Taskplaner für Entwickler

> [!IMPORTANT]
> Dieses Thema und die anderen Themen in diesem Abschnitt sind für eine Entwicklergruppe. Wenn Sie die Taskplaner Komponente in ihrer Kapazität als Administrator oder als IT-Experte verwenden möchten, finden Sie weitere Informationen unter [Taskplaner](/dynamics365/business-central/dev-itpro/developer/devenv-task-scheduler).

## <a name="about-the-task-scheduler"></a>Informationen zum Taskplaner

Der Taskplaner ermöglicht Ihnen das automatische Ausführen von Routineaufgaben auf einem ausgewählten Computer. Taskplaner dies durch die Überwachung der von Ihnen gewählten Kriterien (als Trigger bezeichnet) und anschließendes Ausführen der Aufgaben, wenn diese Kriterien erfüllt sind.

Sie können den Taskplaner verwenden, um Aufgaben wie das Starten einer Anwendung, das Senden einer e-Mail-Nachricht oder das zeigen eines Meldungs Felds auszuführen. Aufgaben können so geplant werden, dass Sie als Reaktion auf diese Ereignisse oder Trigger ausgeführt werden. 

- Wenn ein bestimmtes System Ereignis auftritt.
- Zu einem bestimmten Zeitpunkt.
- Zu einem bestimmten Zeitpunkt nach einem täglichen Zeitplan.
- Zu einer bestimmten Zeit in einem wöchentlichen Zeitplan.
- Zu einem bestimmten Zeitpunkt nach einem monatlichen Zeitplan.
- Zu einem bestimmten Zeitpunkt an einem monatlichen Wochentag.
- Wenn der Computer in den Leerlauf wechselt.
- Wenn die Aufgabe registriert ist.
- Wenn das System gestartet wird.
- Wenn sich ein Benutzer anmeldet.
- Wenn sich der Status einer Terminal Server Sitzung ändert.

## <a name="developers"></a>Entwickler

Der Taskplaner stellt APIs in diesen Formularen bereit.

- Taskplaner 2,0: Schnittstellen und Objekte werden für C++ und für die Skript Entwicklung bereitgestellt.
- Taskplaner 1,0: für die C++-Entwicklung werden Schnittstellen bereitgestellt.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Der Taskplaner erfordert die folgenden Betriebssysteme:

- Taskplaner 2,0: für den Client ist Windows Vista oder höher erforderlich. Der Server erfordert Windows Server 2008 oder höher.
- Taskplaner 1,0: der Client erfordert Windows Vista oder Windows XP. Der Server erfordert Windows Server 2008 oder Windows Server 2003.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | BESCHREIBUNG |
|-|-|
| [Neues in Taskplaner](what-s-new-in-task-scheduler.md) | Zusammenfassung der neuen Funktionen, die von der Taskplaner eingeführt wurden. |
| [Informationen zum Taskplaner](about-the-task-scheduler.md) | Allgemeine konzeptionelle Informationen zur Taskplaner-API. |
| [Verwenden des Taskplaner](using-the-task-scheduler.md) | Code Beispiele, die zeigen, wie die Taskplaner-APIs verwendet werden. |
| [Taskplaner Referenz](task-scheduler-reference.md) | Ausführliche Referenzinformationen für Taskplaner-APIs und das Taskplaner-Schema. |