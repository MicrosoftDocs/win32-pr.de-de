---
description: Quality of Service gibt die Leistung und Energieeffizienz eines Threads an, die sich auf die Threadplanung und die Prozessorleistungsverwaltung auswirken können.
title: Quality of Service (QoS, Dienstqualität)
ms.topic: article
ms.date: 07/09/2021
ms.openlocfilehash: ec4e92360d23a427d526a36a81bfdb0667c1cb6fb5f60ddcefd578c4918ba5d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117793464"
---
# <a name="quality-of-service"></a>Quality of Service (QoS, Dienstqualität)

Die Quality of Service (QoS), die einem Thread zugeordnet ist, wird verwendet, um die gewünschte Leistung und Energieeffizienz anzugeben. Jeder Thread wird einer QoS-Ebene zugewiesen. Die Planungspriorität bleibt die Hauptmetrik, mit der das System bestimmt, welcher Thread als Nächstes geplant werden soll. QoS kann jedoch die Kernauswahl und die Energieverwaltung des Prozessors beeinflussen. Auf Plattformen mit heterogenen Prozessoren kann die QoS eines Threads die Planung auf eine Teilmenge von Prozessoren beschränken oder eine Einstellung für eine bestimmte Prozessorklasse angeben.

Entwickler verwenden möglicherweise bereits andere Einrichtungen, um zu steuern, wann sie ausgeführt werden müssen, z. B. wenn der Benutzer nicht vorhanden ist, nur bei Wechselstrom/Ladevorgang oder je nach Akkustand. QoS bietet eine Möglichkeit, die Ausführung zu beeinflussen. Diese Einrichtung kann zur Verbesserung der CPU-Effizienz und somit zur Verlängerung der Akkulebensdauer beitragen. Darüber hinaus kann dieser Prozess bei der Reduzierung des CPU-Energieverbrauchs beim Betrieb mit Wechselstrom helfen, um die wärmeren Ausgaben zu reduzieren, was zu hohem Lüfterrauschen oder sogar einer wärmeren Drosselung führen kann.

## <a name="quality-of-service-levels"></a>Quality of Service Ebenen

Das System verwaltet mehrere QoS-Ebenen mit jeweils unterschiedlicher Leistung und Energieeffizienz. Windows stellt Standardeinstellungen für die Planung und Prozessorleistungsverwaltung für jede QoS-Ebene zur Verfügung. Die genaue Optimierung der einzelnen QoS-Ebene für die Prozessorleistungsverwaltung und heterogene Planung kann über die Windows geändert werden. Weitere Informationen zur Leistungsoptimierung und -bereitstellung finden Sie unter [Prozessor-Energieverwaltungsoptionen.](/windows-hardware/customize/power-settings/configure-processor-power-management-options)

| QoS-Ebene | Beschreibung|Leistung und Leistung | Freigabe |
| --- | --- | --- | --- |
| Hoch | Fensteranwendungen, die sich im Vordergrund und im Fokus oder hörbar befinden und Prozesse explizit mit [SetProcessInformation](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessinformation) oder Threads mit [SetThreadInformation markieren](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadinformation) | Hohe Standardleistung. |1709 |
| Medium | Anwendungen mit Fenstern, die möglicherweise für den Endbenutzer sichtbar sind, sich aber nicht im Fokus befinden. | Variiert je nach Plattform, zwischen Hoch und Niedrig. | 1709 |
| Niedrig | Anwendungen mit Fenstern, die für den Endbenutzer nicht sichtbar oder hörbar sind. | Bei Akku wählt die effizienteste CPU-Frequenz und zeitplanungs für effiziente Kerne aus. | 1709 |
| Eco | Anwendungen, die Prozesse explizit mit [SetProcessInformation](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessinformation) markieren, oder Threads mit [SetThreadInformation](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadinformation). | Wählt immer die effizienteste CPU-Frequenz und Zeitpläne für effiziente Kerne aus. | Windows 11 |
| Medien | Threads, die explizit vom [Multimedia-Klassenplanerdienst markiert wurden,](/windows/desktop/procthread/multimedia-class-scheduler-service) um die Multimediabatchpufferung zu bezeichnen. | Die CPU-Frequenz wurde für eine effiziente Batchverarbeitung reduziert. | 2004 |
| Stichtag | Threads, die explizit vom [Multimedia-Klassenplanerdienst](/windows/desktop/procthread/multimedia-class-scheduler-service) gekennzeichnet wurden, um zu bezeichnen, dass Audiothreads Leistung erfordern, um Stichtage zu erfüllen. | Hohe Leistung, um Medientermine zu erfüllen. | 2004 |

## <a name="quality-of-service-classification"></a>Quality of Service Klassifizierung

Die folgende Tabelle zeigt die unterstützten QoS-Klassifizierungen.

| Quelle | Beschreibung |
| --- | --- |
| Multimedia Foundation | Der [Multimedia-Klassenplanerdienst](/windows/desktop/procthread/multimedia-class-scheduler-service) priorisiert CPU-Ressourcen für Multimediaszenarien. Der Dienst markiert bestimmte Threads, die für die Multimediaverarbeitung mithilfe der QoS-Ebenen Media und Deadline verantwortlich sind, um Energieeffizienz zu gewährleisten und gleichzeitig Leistungstermine zu erfüllen.  |
| API | [Mit SetProcessInformation](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessinformation) können Entwickler einen Prozess explizit als HighQoS oder EcoQoS markieren, indem sie das Feature `PROCESS_POWER_THROTTLING_EXECUTION_SPEED` in **ProcessPowerThrottling umbenennen.**</br>[Mit SetThreadInformation](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessinformation) können Entwickler einen Thread explizit als HighQoS oder EcoQoS markieren, indem sie das Feature `THREAD_POWER_THROTTLING_EXECUTION_SPEED` in **ThreadPowerThrottling umbenennen.**  |
| Hörbar | Prozesse, die als Audiowiedergabe bestimmt sind, sind HighQoS. |
| Sichtbar | Prozessen, die direkt ein Fenster besitzen (oder Nachfolger von Fensteren besitzenden Prozessen sind), wird eine QoS-Ebene entsprechend ihrem Sichtbarkeits- und Fokuszustand zugewiesen:</br></br><table><tr><th>Fensterzustand</th><th>Quality of Service (QoS, Dienstqualität)</th></tr><tr><td>Im Fokus</td><td>Hoch</td></tr><tr><td>Sichtbar</td><td>Medium</td></tr><tr><td>Minimiert oder vollständig okkluded</td><td>Niedrig</td></tr></table> |
| Heuristik | Threads, die nicht von den oben genannten Quellen klassifiziert werden, wird automatisch vom System eine QoS-Ebene zugewiesen. Diese Heuristiken umfassen (aber nicht beschränkt auf) Threadpriorität, wobei Threads, die mit einer niedrigeren Threadpriorität ausgeführt werden, eine niedrigere QoS-Ebene implizieren können. |
