---
description: Quality of Service gibt die Leistung und Energieeffizienz eines Threads an, die sich auf die Threadplanung und die Prozessorleistungsverwaltung auswirken können.
title: Quality of Service (QoS, Dienstqualität)
ms.topic: article
ms.date: 07/09/2021
ms.openlocfilehash: c506e810bafad41e9a5f14112c1398b0d6fb3ffc
ms.sourcegitcommit: 2805e19a2738a408d3c5ab69a8d84ec92ca25e36
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/14/2021
ms.locfileid: "113989791"
---
# <a name="quality-of-service"></a>Quality of Service (QoS, Dienstqualität)

Die einem Thread zugeordnete Quality of Service (QoS) wird verwendet, um die gewünschte Leistung und Energieeffizienz anzugeben. Jeder Thread wird einer QoS-Ebene zugewiesen. Während die Zeitplanungspriorität die Hauptmetrik bleibt, anhand derer das System bestimmt, welcher Thread als Nächstes geplant werden soll, kann QoS die Kernauswahl und die Prozessorleistungsverwaltung beeinflussen. Auf Plattformen mit heterogenen Prozessoren kann der QoS eines Threads die Zeitplanung auf eine Teilmenge von Prozessoren einschränken oder eine Einstellung für eine bestimmte Prozessorklasse angeben.

Entwickler verwenden möglicherweise bereits andere Einrichtungen, um zu steuern, wann die Ausführung erfolgen soll, z. B. wenn der Benutzer nicht vorhanden ist, nur bei Wechselstrom/Ladevorgang oder je nach Akkustand. QoS bietet eine Möglichkeit, die Ausführung zu beeinflussen. Diese Einrichtung kann dazu beitragen, die CPU-Effizienz zu verbessern und so die Akkulaufzeit zu verlängern. Darüber hinaus kann dieser Prozess dazu beitragen, den CPU-Energieverbrauch zu reduzieren, während der Wechselstrom betrieben wird, um die wärmeren Ausgaben zu reduzieren, was zu hohem Lüfterrauschen oder sogar einer Wärmedrosselung führen kann.

## <a name="quality-of-service-levels"></a>Quality of Service Ebenen

Das System verwaltet mehrere QoS-Ebenen mit jeweils unterschiedlicher Leistung und Energieeffizienz. Windows bietet Standardeinstellungen für die Planung und Prozessorleistungsverwaltung für jede QoS-Ebene. Die genaue Optimierung jeder QoS-Ebene für die Prozessorleistungsverwaltung und heterogene Planung kann durch Windows Bereitstellung geändert werden. Weitere Informationen zur Leistungsoptimierung und -bereitstellung finden Sie unter [Prozessor-Energieverwaltungsoptionen.](/windows-hardware/customize/power-settings/configure-processor-power-management-options)

| QoS-Ebene | BESCHREIBUNG|Leistung und Leistung | Release |
| --- | --- | --- | --- |
| High | Fensteranwendungen, die sich im Vordergrund und im Fokus oder hörbar befinden | Hohe Standardleistung |1709 |
| Medium | Fensteranwendungen, die möglicherweise für den Endbenutzer sichtbar sind, sich aber nicht im Fokus befinden | Variiert je nach Plattform, zwischen Hoch und Niedrig | 1709 |
| Niedrig | Fensteranwendungen, die für den Endbenutzer nicht sichtbar oder hörbar sind | Wählt bei Akkubetrieb die effizienteste CPU-Frequenz aus und plant effiziente Kerne. | 1709 |
| Eco | Anwendungen, die Prozesse explizit mit [SetProcessInformation](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessinformation) oder Threads mit [SetThreadInformation](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessinformation) markieren | Wählt immer die effizienteste CPU-Häufigkeit und Zeitpläne für effiziente Kerne aus. | Windows 11 |
| Medien | Threads, die explizit vom [Multimedia Class Scheduler Service](/windows/desktop/procthread/multimedia-class-scheduler-service) markiert wurden, um die Multimediabatchpufferung zu kennzeichnen | Cpu-Häufigkeit für effiziente Batchverarbeitung reduziert | 2004 |
| Stichtag | Von Multimedia [Class Scheduler Service](/windows/desktop/procthread/multimedia-class-scheduler-service) explizit markierte Threads, um zu kennzeichnen, dass Audiothreads Leistung erfordern, um Stichtage zu erfüllen | Hohe Leistung zum Einhalten von Medienstichtagen | 2004 |

## <a name="quality-of-service-classification"></a>Quality of Service Klassifizierung

Die folgende Tabelle zeigt die unterstützten QoS-Klassifizierungen.

| `Source` | BESCHREIBUNG |
| --- | --- |
| Multimedia Foundation | Der [Multimedia Class Scheduler Service](/windows/desktop/procthread/multimedia-class-scheduler-service) priorisiert CPU-Ressourcen für Multimediaszenarien. Der Dienst kennzeichnet bestimmte Threads, die für die Multimediaverarbeitung mithilfe der QoS-Ebenen "Media" und "Deadline" verantwortlich sind, um Energieeffizienz zu erzielen und gleichzeitig Leistungsstichtage einzuhalten.  |
| API | [Mit SetProcessInformation](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessinformation) können Entwickler einen Prozess explizit als HighQoS oder EcoQoS markieren, indem sie das `PROCESS_POWER_THROTTLING_EXECUTION_SPEED` Feature in **ProcessPowerThrottling umstellen.**</br>[Mit SetThreadInformation](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessinformation) können Entwickler einen Thread explizit als HighQoS oder EcoQoS markieren, indem sie das `THREAD_POWER_THROTTLING_EXECUTION_SPEED` Feature in **ThreadPowerThrottling umstellen.**  |
| Hörbar | Prozesse, die als Audiowiedergabe bestimmt werden, sind HighQoS. |
| Sichtbar | Prozessen, die direkt ein Fenster besitzen (oder Nachfolger von Prozessen mit Fensterbesitz sind), wird je nach Sichtbarkeit und Fokuszustand eine QoS-Ebene zugewiesen:</br></br><table><tr><th>Fensterzustand</th><th>Quality of Service (QoS, Dienstqualität)</th></tr><tr><td>Im Fokus</td><td>High</td></tr><tr><td>Sichtbar</td><td>Medium</td></tr><tr><td>Minimiert oder vollständig verdeckt</td><td>Niedrig</td></tr></table> |
| Heuristik | Threads, die nicht von den oben genannten Quellen klassifiziert werden, werden vom System automatisch eine QoS-Ebene zugewiesen. Diese Heuristiken umfassen die Threadpriorität (sind aber nicht darauf beschränkt), wobei Threads, die mit reduzierter Threadpriorität ausgeführt werden, eine niedrigere QoS-Ebene implizieren können. |
