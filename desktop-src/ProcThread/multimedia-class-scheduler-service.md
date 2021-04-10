---
description: Der Multimedia Class Scheduler Service (MMCSS) ermöglicht Multimediaanwendungen, sicherzustellen, dass die Zeit empfindliche Verarbeitung den priorisierten Zugriff auf CPU-Ressourcen erhält.
ms.assetid: a7169938-1c72-4c4c-881a-cb08ad6182c7
title: Multimedia-Class Scheduler-Dienst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80656276af30495c084d0964534a04e11896bcd2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961134"
---
# <a name="multimedia-class-scheduler-service"></a>Multimedia-Class Scheduler-Dienst

Der Multimedia Class Scheduler Service (MMCSS) ermöglicht Multimediaanwendungen, sicherzustellen, dass die Zeit empfindliche Verarbeitung den priorisierten Zugriff auf CPU-Ressourcen erhält. Mit diesem Dienst können Multimediaanwendungen so viel CPU wie möglich nutzen, ohne dass CPU-Ressourcen für Anwendungen mit niedrigerer Priorität verweigert werden.

MMCSS verwendet Informationen, die in der Registrierung gespeichert sind, um unterstützte Aufgaben zu identifizieren und die relative Priorität der Threads zu ermitteln, die diese Aufgaben ausführen. Jeder Thread, der Aufgaben im Zusammenhang mit einer bestimmten Aufgabe ausführt, ruft die [**avsetmmmaxthreadcharacteristics**](/windows/desktop/api/Avrt/nf-avrt-avsetmmmaxthreadcharacteristicsa) -Funktion oder die [**avsetmmthreadcharacteristics**](/windows/desktop/api/Avrt/nf-avrt-avsetmmthreadcharacteristicsa) -Funktion auf, um MMCSS darüber zu informieren, dass Sie an dieser Aufgabe arbeitet.

Ein Beispiel für ein Programm, das MMCSS verwendet, finden Sie unter Daten [Ströme im exklusiven Modus](/previous-versions//bb614507(v=vs.85)).

**Windows Server 2003 und Windows XP:** MMCSS ist nicht verfügbar.

## <a name="registry-settings"></a>Registrierungseinstellungen

Die MMCSS-Einstellungen werden im folgenden Registrierungsschlüssel gespeichert:

**HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Multimedia \\ Systemprofile**

Dieser Schlüssel enthält einen **reg \_ DWORD** -Wert mit dem Namen **systemreaktionsfähigkeit** , der den Prozentsatz der CPU-Ressourcen bestimmt, die für Aufgaben mit niedriger Priorität garantiert werden sollten. Wenn dieser Wert z. b. 20 beträgt, sind 20% der CPU-Ressourcen für Aufgaben mit niedriger Priorität reserviert. Beachten Sie, dass Werte, die nicht gleichmäßig durch 10 sichtbar sind, auf das nächste Vielfache von 10 aufgerundet werden. Der Wert 0 wird auch als 10 behandelt.

Der Schlüssel enthält auch einen Unterschlüssel mit dem Namen **Tasks** , der die Liste der Aufgaben enthält. Standardmäßig unterstützt Windows die folgenden Aufgaben:

-   **Audio**
-   **Capture**
-   **Distribution**
-   **Spiele**
-   **Wiedergabe**
-   **Pro-Audiodatei**
-   **Fenster-Manager**

OEMs können nach Bedarf zusätzliche Aufgaben hinzufügen.

Jeder Task Schlüssel enthält die folgenden Werte, die Eigenschaften darstellen, die auf die dem Task zugeordneten Threads angewendet werden sollen.

| Wert                   | Format         | Mögliche Werte                                                                                                                                                                                                                                                                                                                                                         |
|-------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Affinitäts**            | **REG \_ DWORD** | Eine Bitmaske, die die Prozessor Affinität angibt. Sowohl "0x00" als auch "0xffffffff" geben an, dass die Prozessor Affinität nicht verwendet wird.                                                                                                                                                                                                                                                 |
| **Nur Hintergrund**     | **REG- \_ SZ**    | Gibt an, ob es sich um eine Hintergrundaufgabe handelt (keine Benutzeroberfläche). Die Threads einer Hintergrundaufgabe ändern sich aufgrund einer Änderung im Fenster Fokus nicht. Dieser Wert kann auf "true" oder "false" festgelegt werden.                                                                                                                                                                            |
| **Backgroundpriority**  | **REG \_ DWORD** | Die Hintergrund Priorität. Der Wertebereich ist 1-8.                                                                                                                                                                                                                                                                                                                    |
| **Taktfrequenz**          | **REG \_ DWORD** | Ein Hinweis, der von MMCSS zum Ermitteln der Granularität der Prozessorressourcen Planung verwendet wird. **Windows Server 2008 und Windows Vista:** Die maximale garantierte Taktrate, die das System verwendet, wenn ein Thread dieser Aufgabe in 100-Nanosekunden-Intervallen Beitritt. Ab Windows 7 und Windows Server 2008 R2 wurde diese Garantie entfernt, um den Energieverbrauch des Systems zu reduzieren.<br/> |
| **GPU-Priorität**        | **REG \_ DWORD** | Die GPU-Priorität. Der Wertebereich ist 0-31. Diese Priorität wird noch nicht verwendet.                                                                                                                                                                                                                                                                                           |
| **Priority**            | **REG \_ DWORD** | Die Aufgaben Priorität. Der Wertebereich ist 1 (niedrig) bis 8 (hoch). Bei Aufgaben mit der **planungskategorie** hoch wird dieser Wert immer als 2 behandelt.<br/>                                                                                                                                                                                                           |
| **Planungskategorie** | **REG- \_ SZ**    | Die Zeit planungskategorie. Dieser Wert kann auf hoch, Mittel oder niedrig festgelegt werden.                                                                                                                                                                                                                                                                                                 |
| **SFI-Priorität**       | **REG- \_ SZ**    | Die geplante e/a-Priorität. Dieser Wert kann auf Leerlauf, niedrig, normal oder hoch festgelegt werden. Dieser Wert wird nicht verwendet.                                                                                                                                                                                                                                                                |



 

> [!Note]  
> Um Energie zu sparen, sollten Anwendungen die Auflösung des systemweiten Timers nicht auf einen kleinen Wert festlegen, sofern dies nicht unbedingt erforderlich ist. Weitere Informationen finden Sie unter [Leistung](../win7devguide/performance.md) im [Windows 7-Entwicklerhandbuch](../win7devguide/windows-7-developer-guide.md).

 

## <a name="thread-priorities"></a>Threadprioritäten

Das MMCSS steigert die Priorität von Threads, die an Multimedia-Aufgaben mit hoher Priorität arbeiten.

MMCSS bestimmt die Priorität eines Threads mit den folgenden Faktoren:

-   Die Basis Priorität der Aufgabe.
-   Der *Priority* -Parameter der [**avsetmmthreadpriority**](/windows/desktop/api/Avrt/nf-avrt-avsetmmthreadpriority) -Funktion.
-   Gibt an, ob sich die Anwendung im Vordergrund befindet.
-   Gibt an, wie viel CPU-Zeit von den Threads in jeder Kategorie verbraucht wird.

MMCSS legt die Priorität der Clientthreads abhängig von ihrer planungskategorie fest.

| Category | Priorität | BESCHREIBUNG                                                                                                                               |
|----------|----------|-------------------------------------------------------------------------------------------------------------------------------------------|
| High     | 23-26    | Diese Threads werden mit einer Thread Priorität ausgeführt, die niedriger ist als nur bestimmte Aufgaben auf Systemebene. Diese Kategorie ist für pro-Audioaufgaben konzipiert. |
| Medium   | 16-22    | Diese Threads sind Teil der Anwendung im Vordergrund.                                                                      |
| Niedrig      | 8-15     | Diese Kategorie enthält den Rest der Threads. Bei Bedarf wird ein minimaler Prozentsatz der CPU-Ressourcen garantiert.           |
|          | 1-7      | Diese Threads haben Ihr Kontingent an CPU-Ressourcen verwendet. Sie können weiterhin ausgeführt werden, wenn keine Threads mit niedriger Priorität für die Durchführung bereit sind.                |



 

 

 
