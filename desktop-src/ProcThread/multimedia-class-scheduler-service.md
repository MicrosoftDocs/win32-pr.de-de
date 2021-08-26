---
description: Mit dem Multimedia Class Scheduler-Dienst (MMCSS) können Multimediaanwendungen sicherstellen, dass ihre zeitsensible Verarbeitung priorisierten Zugriff auf CPU-Ressourcen erhält.
ms.assetid: a7169938-1c72-4c4c-881a-cb08ad6182c7
title: Multimedia-Klassenplanerdienst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf0744883180c361d5656cf7c182f538d93617be7f6bbdc6a05ff93efa732b53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032440"
---
# <a name="multimedia-class-scheduler-service"></a>Multimedia-Klassenplanerdienst

Mit dem Multimedia Class Scheduler-Dienst (MMCSS) können Multimediaanwendungen sicherstellen, dass ihre zeitsensible Verarbeitung priorisierten Zugriff auf CPU-Ressourcen erhält. Mit diesem Dienst können Multimediaanwendungen so viel CPU wie möglich nutzen, ohne CPU-Ressourcen für Anwendungen mit niedrigerer Priorität zu verweigern.

MMCSS verwendet in der Registrierung gespeicherte Informationen, um unterstützte Aufgaben zu identifizieren und die relative Priorität von Threads zu bestimmen, die diese Aufgaben ausführen. Jeder Thread, der Arbeiten im Zusammenhang mit einer bestimmten Aufgabe vor sich hat, ruft die [**AvSetMmMaxThreadCharacteristics-**](/windows/desktop/api/Avrt/nf-avrt-avsetmmmaxthreadcharacteristicsa) oder [**AvSetMmThreadCharacteristics-Funktion**](/windows/desktop/api/Avrt/nf-avrt-avsetmmthreadcharacteristicsa) auf, um MMCSS darüber zu informieren, dass sie an dieser Aufgabe arbeitet.

Ein Beispiel für ein Programm, das MMCSS verwendet, finden Sie unter [Exclusive-Mode Streams.](/previous-versions//bb614507(v=vs.85))

**Windows Server 2003 und Windows XP:** MMCSS ist nicht verfügbar.

## <a name="registry-settings"></a>Registrierungseinstellungen

Die MMCSS-Einstellungen werden im folgenden Registrierungsschlüssel gespeichert:

**HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion Multimedia \\ \\ SystemProfile**

Dieser Schlüssel enthält einen **REG \_ DWORD-Wert** mit dem Namen **SystemResponsiveness,** der den Prozentsatz der CPU-Ressourcen bestimmt, der für Tasks mit niedriger Priorität garantiert werden soll. Wenn dieser Wert beispielsweise 20 beträgt, sind 20 % der CPU-Ressourcen für Aufgaben mit niedriger Priorität reserviert. Beachten Sie, dass Werte, die nicht gleichmäßig durch 10 teilbar sind, auf das nächste Vielfache von 10 aufgerundet werden. Der Wert 0 wird ebenfalls als 10 behandelt.

Der Schlüssel enthält auch einen Unterschlüssel namens **Tasks,** der die Liste der Aufgaben enthält. Standardmäßig unterstützt Windows folgende Aufgaben:

-   **Audio**
-   **Capture**
-   **Distribution**
-   **Spiele**
-   **Wiedergabe**
-   **Pro Audio**
-   **Fenster-Manager**

OEMs können bei Bedarf zusätzliche Aufgaben hinzufügen.

Jeder Taskschlüssel enthält die folgenden Werte, die Merkmale darstellen, die auf Threads angewendet werden sollen, die dem Task zugeordnet sind.

| Wert                   | Format         | Mögliche Werte                                                                                                                                                                                                                                                                                                                                                         |
|-------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Affinität**            | **REG \_ DWORD** | Eine Bitmaske, die die Prozessoraffinität angibt. Sowohl 0x00 als auch 0xFFFFFFFF, dass die Prozessoraffinität nicht verwendet wird.                                                                                                                                                                                                                                                 |
| **Nur Hintergrund**     | **REG \_ SZ**    | Gibt an, ob es sich um eine Hintergrundaufgabe (keine Benutzeroberfläche) handelt. Die Threads einer Hintergrundaufgabe ändern sich aufgrund einer Änderung des Fensterfokus nicht. Dieser Wert kann auf True oder False festgelegt werden.                                                                                                                                                                            |
| **BackgroundPriority**  | **REG \_ DWORD** | Die Hintergrundpriorität. Der Wertebereich liegt zwischen 1 und 8.                                                                                                                                                                                                                                                                                                                    |
| **Taktfrequenz**          | **REG \_ DWORD** | Ein Hinweis, der von MMCSS verwendet wird, um die Granularität der Prozessorressourcenplanung zu bestimmen. **Windows Server 2008 und Windows Vista:** Die maximale garantierte Taktrate, die das System verwendet, wenn ein Thread diese Aufgabe in Intervallen von 100 Nanosekunden verbindet. Ab Windows 7 und Windows Server 2008 R2 wurde diese Garantie entfernt, um den Energieverbrauch des Systems zu reduzieren.<br/> |
| **GPU-Priorität**        | **REG \_ DWORD** | Die GPU-Priorität. Der Wertebereich ist 0-31. Diese Priorität wird noch nicht verwendet.                                                                                                                                                                                                                                                                                           |
| **Priority**            | **REG \_ DWORD** | Die Aufgabenpriorität. Der Wertebereich ist 1 (niedrig) bis 8 (hoch). Bei Aufgaben mit der **Planungskategorie** "Hoch" wird dieser Wert immer als 2 behandelt.<br/>                                                                                                                                                                                                           |
| **Planungskategorie** | **REG \_ SZ**    | Die Planungskategorie. Dieser Wert kann auf Hoch, Mittel oder Niedrig festgelegt werden.                                                                                                                                                                                                                                                                                                 |
| **SFIO-Priorität**       | **REG \_ SZ**    | Die geplante E/A-Priorität. Dieser Wert kann auf Idle, Low, Normal oder High festgelegt werden. Dieser Wert wird nicht verwendet.                                                                                                                                                                                                                                                                |



 

> [!Note]  
> Um Energie zu sparen, sollten Anwendungen die Auflösung des systemweiten Timers nur auf einen kleinen Wert festlegen, wenn dies unbedingt erforderlich ist. Weitere Informationen finden Sie unter [Leistung](../win7devguide/performance.md) im [Windows 7 Developers Guide](../win7devguide/windows-7-developer-guide.md).

 

## <a name="thread-priorities"></a>Threadprioritäten

Die MMCSS erhöht die Priorität von Threads, die an Multimediaaufgaben mit hoher Priorität arbeiten.

MMCSS bestimmt die Priorität eines Threads anhand der folgenden Faktoren:

-   Die Basispriorität der Aufgabe.
-   Der *Priority-Parameter* der [**AvSetMmThreadPriority-Funktion.**](/windows/desktop/api/Avrt/nf-avrt-avsetmmthreadpriority)
-   Gibt an, ob sich die Anwendung im Vordergrund befindet.
-   Wie viel CPU-Zeit von den Threads in jeder Kategorie verbraucht wird.

MMCSS legt die Priorität von Clientthreads abhängig von ihrer Planungskategorie fest.

| Kategorie | Priorität | BESCHREIBUNG                                                                                                                               |
|----------|----------|-------------------------------------------------------------------------------------------------------------------------------------------|
| High     | 23-26    | Diese Threads werden mit einer Threadpriorität ausgeführt, die niedriger als nur bestimmte Tasks auf Systemebene ist. Diese Kategorie ist für Pro Audioaufgaben konzipiert. |
| Medium   | 16-22    | Diese Threads sind Teil der Anwendung, die sich im Vordergrund befindet.                                                                      |
| Niedrig      | 8-15     | Diese Kategorie enthält den Rest der Threads. Bei Bedarf wird ihnen ein Mindestprozentsatz der CPU-Ressourcen garantiert.           |
|          | 1-7      | Diese Threads haben ihr Kontingent an CPU-Ressourcen verwendet. Sie können weiterhin ausgeführt werden, wenn keine Threads mit niedriger Priorität ausgeführt werden können.                |



 

 

 
