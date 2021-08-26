---
description: Eine Anwendung kann geschachtelte Aufträge verwenden, um Teilmengen von Prozessen zu verwalten. Geschachtelte Aufträge ermöglichen auch eine Anwendung, die Aufträge verwendet, um andere Anwendungen zu hosten, die ebenfalls Aufträge verwenden.
ms.assetid: FA22493B-CD29-49A7-BDAC-349FA96B8C9E
title: Geschachtelte Aufträge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fba0a517b71cdc01ec701a4a8f6a4f272f039797c140333e64ecad5532aca23f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032209"
---
# <a name="nested-jobs"></a>Geschachtelte Aufträge

Eine Anwendung kann geschachtelte Aufträge verwenden, um Teilmengen von Prozessen zu verwalten. Geschachtelte Aufträge ermöglichen auch eine Anwendung, die Aufträge verwendet, um andere Anwendungen zu hosten, die ebenfalls Aufträge verwenden.

**Windows 7, Windows Server 2008 R2, Windows XP mit SP3, Windows Server 2008, Windows Vista und Windows Server 2003:** Ein Prozess kann nur einem einzelnen Auftrag zugeordnet werden. Geschachtelte Aufträge wurden in Windows 8 und Windows Server 2012.

Dieses Thema bietet eine Übersicht über die Auftragsschachtelung und das Verhalten geschachtelter Aufträge:

-   [Geschachtelte Auftragshierarchien](#nested-job-hierarchies)
-   [Erstellen einer geschachtelten Auftragshierarchie](#creating-a-nested-job-hierarchy)
-   [Auftragsgrenzwerte und Benachrichtigungen für geschachtelte Aufträge](#job-limits-and-notifications-for-nested-jobs)
-   [Ressourcenabrechnung für geschachtelte Aufträge](#resource-accounting-for-nested-jobs)
-   [Beenden geschachtelter Aufträge](#termination-of-nested-jobs)

Allgemeine Informationen zu Aufträgen und Auftragsobjekten finden Sie unter [Auftragsobjekte.](job-objects.md)

## <a name="nested-job-hierarchies"></a>Geschachtelte Auftragshierarchien

Geschachtelte Aufträge verfügen über eine über- und untergeordnete Beziehung, in der jeder untergeordnete Auftrag eine Teilmenge der Prozesse in seinem übergeordneten Auftrag enthält. Wenn ein Prozess, der sich bereits in einem Auftrag befindet, einem anderen Auftrag hinzugefügt wird, werden die Aufträge standardmäßig geschachtelt, wenn das System eine gültige Auftragshierarchie bilden kann und keiner der Aufträge Benutzeroberflächengrenzwerte [**(SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) mit **JobObjectBasicUIRestrictions)** festgelegt hat.

Abbildung 1 zeigt eine Auftragshierarchie, die eine Struktur von Prozessen mit der Bezeichnung P0 bis P7 enthält. Auftrag 1 ist der *übergeordnete Auftrag* von Auftrag 2 und Auftrag 4 und ein Vorgänger *von* Auftrag 3. Auftrag 2 ist das *unmittelbar übergeordnete Element* von Auftrag 3. Auftrag 3 ist das *unmittelbar untergeordnete Untergeordnete* von Auftrag 2. Die Aufträge 1, 2 und 3 bilden eine Auftragskette,  *in* der Aufträge 1 und 2 die übergeordnete Auftragskette von Auftrag 3 sind. Der Endauftrag in einer Auftragskette ist der *unmittelbare Auftrag* der Prozesse in diesem Auftrag. In Abbildung 1 ist Auftrag 3 der unmittelbare Auftrag der Prozesse P2, P3 und P4.

![Abbildung 1: eine geschachtelte Auftragshierarchie, die eine Prozessstruktur enthält](images/nested-jobs-a.png)

Geschachtelte Aufträge können auch zum Verwalten von Gruppen von Peerprozessen verwendet werden. In der in Abbildung 2 dargestellten Auftragshierarchie ist Auftrag 1 der übergeordnete Auftrag von Auftrag 2. Beachten Sie, dass eine Auftragshierarchie möglicherweise nur einen Teil einer Prozessstruktur enthält. In Abbildung 2 befindet sich P0 nicht in der Hierarchie, aber die untergeordneten Prozesse P1 bis P5 sind.

![Abbildung 2: eine geschachtelte Auftragshierarchie, die Peerprozesse enthält](images/nested-jobs-b.png)

## <a name="creating-a-nested-job-hierarchy"></a>Erstellen einer geschachtelten Auftragshierarchie

Prozesse in einer Auftragshierarchie werden entweder explizit einem Auftragsobjekt mithilfe der [**AssignProcessToJobObject-Funktion**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject) oder implizit während der Prozesserstellung zugeordnet, wie bei eigenständigen Aufträgen. Die Reihenfolge, in der Aufträge erstellt und Prozesse zugewiesen werden, bestimmt, ob eine Hierarchie erstellt werden kann.

Um eine Auftragshierarchie mit expliziter Zuordnung zu erstellen, müssen alle Auftragsobjekte mit [**CreateJobObject**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta)erstellt werden. [**Anschließend muss AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject) mehrmals aufgerufen werden, damit jeder Prozess jedem Auftrag zugeordnet werden kann, zu dem er gehören soll. Um sicherzustellen, dass die Auftragshierarchie gültig ist, weisen Sie zunächst dem Auftrag im Stammverzeichnis der Hierarchie alle Prozesse zu, und weisen Sie dann dem unmittelbar untergeordneten Auftragsobjekt eine Teilmenge der Prozesse zu. Wenn Prozesse Aufträgen in dieser Reihenfolge zugewiesen werden, weist ein untergeordneter Auftrag immer eine Teilmenge von Prozessen im übergeordneten Auftrag auf, während die Hierarchie erstellt wird. Dies ist für die Schachtelung erforderlich. Wenn Prozesse Aufträgen in zufälliger Reihenfolge zugewiesen werden, weist ein untergeordneter Auftrag an einem bestimmten Punkt Prozesse auf, die sich nicht im übergeordneten Auftrag befinden. Dies ist durch die Schachtelung nicht zulässig und verursacht einen **Fehler bei AssignProcessToJobObject.**

Wenn Prozesse während der Prozesserstellung implizit einem Auftrag zugeordnet werden, wird jedem Auftrag in der Auftragskette des übergeordneten Prozesses ein untergeordneter Prozess zugeordnet. Wenn das unmittelbare Auftragsobjekt eine Unterbrechung zulässt, wird der untergeordnete Prozess vom unmittelbaren Auftragsobjekt und von jedem Auftrag in der übergeordneten Auftragskette entfernt und die Hierarchie nach oben bewegt, bis er einen Auftrag erreicht, der keine Unterbrechung zulässt. Wenn das Direktauftragsobjekt keine Unterbrechung zu lässt, wird der untergeordnete Prozess auch dann nicht entfernt, wenn Aufträge in der übergeordneten Auftragskette dies zulassen.

## <a name="job-limits-and-notifications-for-nested-jobs"></a>Auftragsgrenzwerte und Benachrichtigungen für geschachtelte Aufträge

Bei bestimmten Ressourcenlimits bestimmt der für Aufträge  in einer übergeordneten Auftragskette festgelegte Grenzwert den effektiven Grenzwert, der für einen untergeordneten Auftrag erzwungen wird. Der effektive Grenzwert für untergeordneten Auftrag kann restriktiver sein als der Grenzwert des übergeordneten Auftrags, aber nicht weniger restriktiv. Wenn die Prioritätsklasse eines untergeordneten Auftrags z. B. ABOVE NORMAL PRIORITY CLASS und die Prioritätsklasse des übergeordneten Auftrags NORMAL PRIORITY CLASS ist, ist der effektive Grenzwert für Prozesse im untergeordneten Auftrag \_ \_ NORMAL PRIORITY \_ \_ \_ \_ \_ CLASS. Wenn die Prioritätsklasse des untergeordneten Auftrags jedoch BELOW NORMAL PRIORITY CLASS ist, ist der effektive Grenzwert für Prozesse im untergeordneten Auftrag \_ \_ BELOW NORMAL PRIORITY \_ \_ \_ \_ CLASS. Effektive Grenzwerte werden für Prioritätsklasse, Affinität, Commitgebühr, Ausführungszeitlimit pro Prozess, Zeitlimit der Zeitplanungsklasse und Minimal- und Höchstwert des Arbeitssets erzwungen. Weitere Informationen zu bestimmten Ressourcenlimits finden Sie unter [ **SetInformationJobObject.**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject)

Wenn bestimmte Ereignisse auftreten, z. B. die Erstellung eines neuen Prozesses oder eine Verletzung des Ressourcenlimits, wird eine Nachricht an den E/A-Abschlussport gesendet, der einem Auftrag zugeordnet ist. Ein Auftrag kann sich auch registrieren, um Benachrichtigungen zu erhalten, wenn bestimmte Grenzwerte überschritten werden. Bei einem nicht geschachtelten Auftrag wird die Nachricht an den E/A-Abschlussport gesendet, der dem Auftrag zugeordnet ist. Bei einem geschachtelten Auftrag wird die Nachricht an jeden E/A-Abschlussport gesendet, der einem Auftrag in der übergeordneten Auftragskette des Auftrags zugeordnet ist, der die Nachricht ausgelöst hat. Einem untergeordneten Auftrag muss kein E/A-Vervollständigungsport zugeordnet sein, damit Nachrichten, die ausgelöst werden, an die E/A-Abschlussports übergeordneter Aufträge weiter in der Auftragskette gesendet werden. Weitere Informationen zu bestimmten Meldungen finden Sie unter [**JOBOBJECT \_ ASSOCIATE COMPLETION \_ \_ PORT**](/windows/desktop/api/WinNT/ns-winnt-jobobject_associate_completion_port).

## <a name="resource-accounting-for-nested-jobs"></a>Ressourcenabrechnung für geschachtelte Aufträge

Informationen zur Ressourcenbuchhaltung für einen geschachtelten Auftrag beschreiben die Verwendung jedes prozesses, der diesem Auftrag zugeordnet ist, einschließlich Prozesse in untergeordneten Aufträgen. Jeder Auftrag in einer Auftragskette stellt daher die aggregierten Ressourcen dar, die von seinen eigenen Prozessen verwendet werden, und die Prozesse jedes untergeordneten Auftrags darunter in der Auftragskette.

## <a name="termination-of-nested-jobs"></a>Beendigung geschachtelter Aufträge

Wenn ein Auftrag in einer Auftragshierarchie beendet wird, beendet das System Prozesse in diesem Auftrag und allen untergeordneten Aufträgen, beginnend mit dem untergeordneten Auftrag am unteren Rand der Hierarchie. Ausstehende Ressourcen, die von jedem beendeten Prozess verwendet werden, werden dem übergeordneten Auftrag in Rechnung gestellt.

Das Auftragshand handle muss über das Zugriffsrecht JOB \_ OBJECT \_ TERMINATE verfügen, wie bei eigenständigen Aufträgen.

 

 
