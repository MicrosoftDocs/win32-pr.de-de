---
description: Eine Anwendung kann für die Verwaltung von Teilmengen von Prozessen mithilfe von mit einem Netz ersteten Aufträgen arbeiten Durch die Verwendung von geclusterte Aufträgen kann eine Anwendung, die Aufträge verwendet, andere Anwendungen hosten, die auch Aufträge verwenden.
ms.assetid: FA22493B-CD29-49A7-BDAC-349FA96B8C9E
title: Genetzte Aufträge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abf105c70ec8e83b395fcce56c6274d4838358bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104561176"
---
# <a name="nested-jobs"></a>Genetzte Aufträge

Eine Anwendung kann für die Verwaltung von Teilmengen von Prozessen mithilfe von mit einem Netz ersteten Aufträgen arbeiten Durch die Verwendung von geclusterte Aufträgen kann eine Anwendung, die Aufträge verwendet, andere Anwendungen hosten, die auch Aufträge verwenden.

**Windows 7, Windows Server 2008 R2, Windows XP mit SP3, Windows Server 2008, Windows Vista und Windows Server 2003:** Ein Prozess kann nur einem einzelnen Auftrag zugeordnet werden. In Windows 8 und Windows Server 2012 wurden in der Liste eingefügte Aufträge eingeführt.

Dieses Thema enthält eine Übersicht über die Auftrags Schachtelung und das Verhalten geschachtelter Aufträge:

-   [Hierarchien von in einem Netz erten Auftrag](#nested-job-hierarchies)
-   [Erstellen einer Hierarchie mit einem Hierarchie](#creating-a-nested-job-hierarchy)
-   [Auftrags Limits und Benachrichtigungen für geclusterte Aufträge](#job-limits-and-notifications-for-nested-jobs)
-   [Ressourcen Erfassung für genetztete Aufträge](#resource-accounting-for-nested-jobs)
-   [Beendigung von in der Liste](#termination-of-nested-jobs)

Allgemeine Informationen zu Aufträgen und Auftrags Objekten finden Sie unter [Auftrags Objekte](job-objects.md).

## <a name="nested-job-hierarchies"></a>Hierarchien von in einem Netz erten Auftrag

Bei der über-/Unterordnungsbeziehung der einzelnen untergeordneten Aufträge werden in einem untergeordneten Auftrag eine Teilmenge der Prozesse in seinem übergeordneten Auftrag enthalten. Wenn ein Prozess, der bereits in einem Auftrag vorhanden ist, einem anderen Auftrag hinzugefügt wird, sind die Aufträge standardmäßig aktiviert, wenn das System eine gültige Auftrags Hierarchie bilden kann und keines der beiden Aufträge die Benutzeroberflächen Limits festlegt ([**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) mit **jobobjectbasicuirestrictions**).

Abbildung 1 zeigt eine Auftrags Hierarchie, die eine Struktur von Prozessen mit der Bezeichnung P0 bis P7 enthält. Job 1 ist der über *geordnete Auftrag* von Job 2 und Job 4 und ist ein *Vorgänger* von Job 3. Auftrag 2 ist das *unmittelbar übergeordnete* Element von Job 3; Job 3 ist das *unmittelbare* untergeordnete Element von Job 2. Die Aufträge 1, 2 und 3 bilden eine *Auftrags Kette* , in der die Aufträge 1 und 2 die über *geordnete Auftrags Kette* von Auftrag 3 sind. Der Endauftrag in einer Auftrags Kette ist der *unmittelbare Auftrag* der Prozesse in diesem Auftrag. In Abbildung 1 ist Job 3 der unmittelbare Auftrag der Prozesse P2, P3 und P4.

![Abbildung 1. eine Hierarchie mit einer Hierarchie, die einen Prozess Baum enthält.](images/nested-jobs-a.png)

Mithilfe von mit einem Namen verknüpften Aufträgen können auch Gruppen von Peer Prozessen verwaltet werden. In der in Abbildung 2 gezeigten Auftrags Hierarchie ist Auftrag 1 der übergeordnete Auftrag von Auftrag 2. Beachten Sie, dass eine Auftrags Hierarchie nur einen Teil eines Prozess Baums enthalten kann. In Abbildung 2 ist P0 nicht in der Hierarchie, aber die untergeordneten Prozesse P1 bis P5 sind.

![Abbildung 2. eine Hierarchie mit einer Hierarchie, die Peer Prozesse enthält.](images/nested-jobs-b.png)

## <a name="creating-a-nested-job-hierarchy"></a>Erstellen einer Hierarchie mit einem Hierarchie

Prozesse in einer Auftrags Hierarchie sind entweder explizit einem Auftrags [**Objekt zugeordnet, indem die Funktion**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject) "Zuordnungs Funktion" oder "implizit" während der Prozesserstellung zugeordnet wird. Dies gilt auch für eigenständige Aufträge. Die Reihenfolge, in der Aufträge erstellt und Prozesse zugewiesen werden, bestimmt, ob eine Hierarchie erstellt werden kann.

Zum Erstellen einer Auftrags Hierarchie mithilfe der expliziten Zuordnung müssen alle Auftrags Objekte mithilfe von " [**foratejobobject**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta)" erstellt werden. Anschließend muss "zuordnungsesstojobobject" für jeden Prozess mehrmals aufgerufen werden, um den Prozess jedem Auftrag zuzuordnen, zu dem er gehören soll. [](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject) Um sicherzustellen, dass die Auftrags Hierarchie gültig ist, weisen Sie zunächst alle Prozesse dem Auftrag im Stammverzeichnis der Hierarchie zu, und weisen Sie dann dem direkt untergeordneten Auftrags Objekt eine Teilmenge von Prozessen zu usw. Wenn Prozesse in dieser Reihenfolge Aufträgen zugewiesen werden, verfügt ein untergeordneter Auftrag immer über eine Teilmenge der Prozesse in seinem übergeordneten Auftrag, während die Hierarchie erstellt wird, die für die Schachtelung erforderlich ist. Wenn Prozesse Aufträgen in zufälliger Reihenfolge zugewiesen werden, verfügt ein untergeordneter Auftrag über Prozesse, die sich nicht in seinem übergeordneten Auftrag befinden. Dies ist durch die Schachtelung nicht zulässig und bewirkt, dass "zubei **zutragprocesstojobobject** " fehlschlägt.

Wenn Prozesse während der Prozesserstellung implizit einem Auftrag zugeordnet sind, wird jedem Auftrag in der Auftrags Kette des übergeordneten Prozesses ein untergeordneter Prozess zugeordnet. Wenn das unmittelbare Auftrags Objekt einen Abbruch zulässt, wird der untergeordnete Prozess vom unmittelbaren Auftrags Objekt und von jedem Auftrag in der übergeordneten Auftrags Kette unterbrochen. die Hierarchie wird so lange verschoben, bis ein Auftrag erreicht wird, der keine Breakaway zulässt. Wenn das unmittelbare Auftrags Objekt keinen Abbruch zulässt, wird der untergeordnete Prozess nicht unterbrochen, auch wenn Aufträge in der übergeordneten Auftrags Kette dies zulassen.

## <a name="job-limits-and-notifications-for-nested-jobs"></a>Auftrags Limits und Benachrichtigungen für geclusterte Aufträge

Für bestimmte Ressourcen Limits bestimmt der für Aufträge in einer übergeordneten Auftrags Kette festgelegte Grenzwert das *effektive Limit* , das für einen untergeordneten Auftrag erzwungen wird. Das effektive Limit für untergeordnete Aufträge kann restriktiver sein als die Begrenzung des übergeordneten Auftrags, kann jedoch nicht weniger restriktiv sein. Wenn die Prioritäts Klasse eines untergeordneten Auftrags beispielsweise oberhalb der \_ normalen \_ Prioritäts Klasse \_ und die Prioritäts Klasse des übergeordneten Auftrags eine normale \_ Prioritäts Klasse ist \_ , ist der effektive Grenzwert für Prozesse im untergeordneten Auftrag die normale \_ Prioritäts \_ Klasse. Wenn die Prioritäts Klasse des untergeordneten Auftrags jedoch unter der \_ normalen \_ Prioritäts Klasse liegt \_ , liegt das effektive Limit für Prozesse im untergeordneten Auftrag unter der \_ normalen \_ Prioritäts \_ Klasse. Effektive Grenzwerte werden für die Prioritäts Klasse, Affinität, Commit-Gebühr, prozessübergreifende Ausführungszeit Limit, Zeit Limit für die Planung und Workingset (minimal und Maximum) erzwungen. Weitere Informationen zu bestimmten Ressourcen Limits finden Sie unter [ **SetInformationJobObject.**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject)

Wenn bestimmte Ereignisse auftreten, z. b. eine neue Prozesserstellung oder eine Verletzung des Ressourcen Limits, wird eine Nachricht an den e/a-Abschlussport gesendet, der einem Auftrag zugeordnet ist. Ein Auftrag kann auch registriert werden, um Benachrichtigungen zu empfangen, wenn bestimmte Grenzwerte überschritten werden. Bei einem nicht-in-netsted-Auftrag wird die Nachricht an den e/a-Abschlussport gesendet, der dem Auftrag zugeordnet ist. Bei einem in einem Vorgang ausgefallenen Auftrag wird die Nachricht an jeden e/a-Abschlussport gesendet, der einem Auftrag in der übergeordneten Auftrags Kette des Auftrags zugeordnet ist, der die Nachricht ausgelöst hat. Einem untergeordneten Auftrag muss kein e/a-Abschlussport zugeordnet sein, damit Nachrichten, die er auslöst, an die e/a-Abschlussports der übergeordneten Aufträge in der Auftrags Kette gesendet werden. Weitere Informationen zu bestimmten Nachrichten finden Sie unter [**JobObject \_ Zuordnen des \_ Vervollständigungs \_ Ports**](/windows/desktop/api/WinNT/ns-winnt-jobobject_associate_completion_port).

## <a name="resource-accounting-for-nested-jobs"></a>Ressourcen Erfassung für genetztete Aufträge

Informationen zur Ressourcen Erfassung für einen in einem Zusammenhang eingefügten Auftrag beschreiben die Verwendung jedes Prozesses, der diesem Auftrag zugeordnet ist, einschließlich der Prozesse in untergeordneten Aufträgen. Jeder Auftrag in einer Auftrags Kette stellt daher die aggregierten Ressourcen dar, die von den eigenen Prozessen und den Prozessen der einzelnen untergeordneten Aufträge in der Auftrags Kette verwendet werden.

## <a name="termination-of-nested-jobs"></a>Beendigung von in der Liste

Wenn ein Auftrag in einer Auftrags Hierarchie beendet wird, beendet das System Prozesse in diesem Auftrag und alle seine untergeordneten Aufträge, beginnend mit dem untergeordneten Auftrag unten in der Hierarchie. Ausstehende Ressourcen, die von jedem beendeten Prozess verwendet werden, werden dem übergeordneten Auftrag in Rechnung gestellt.

Für das Auftrags Handle muss das Auftrags \_ Objekt das \_ Zugriffsrecht beenden, wie bei eigenständigen Aufträgen.

 

 
